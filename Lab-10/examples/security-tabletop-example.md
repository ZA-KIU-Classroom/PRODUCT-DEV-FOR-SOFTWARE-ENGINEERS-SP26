# Security Tabletop — StudySpace Finders

> **This is a worked example for Lab 10. It uses the fictional StudySpace Finders product.
> Your team must complete your own security tabletop for your actual product and user flows.**

**Product:** StudySpace Finders
**Team:** StudySpace Finders (fictional reference team)
**Date:** 21 May 2026
**Audit run date:** 21 May 2026

---

## Five User Flows Selected

| # | Flow name | Why selected |
|---|-----------|-------------|
| 1 | User signup and email verification | Entry point for all users. Compromise here exposes all downstream data. |
| 2 | User login and session management | Primary authentication surface. Account takeover originates here. |
| 3 | Study space search | Highest traffic flow. Processes location context and query data. |
| 4 | Booking creation and confirmation | Core transactional flow. Carries booking records tied to user identity. |
| 5 | Account deletion and data export | Exposes all stored personal data in a single request. High value for an attacker. |

---

## Flow 1: User Signup and Email Verification

**Description:** User enters email and password, submits the signup form, receives a verification email, clicks the link, and gains access to the product.

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | Attacker registers with another user's email address to associate a controlled password with that address | Email verification required before account activation. Supabase auth enforces this. Unverified accounts cannot access any booking features. | Mitigated |
| Tampering | Signup form data tampered with in transit (e.g. email address swapped between browser and server) | HTTPS enforced on all routes. Vercel enforces HTTPS and redirects HTTP. TLS 1.2 minimum. | Mitigated |
| Repudiation | User denies completing signup and claims they never agreed to terms | Signup timestamp and IP address recorded in Supabase `users` table. Terms of service version logged at signup in `consent` column. | Mitigated |
| Information Disclosure | Error message "Email already in use" on failed signup reveals whether an email is registered, enabling account enumeration | Current implementation returns specific error. This is a known gap. An attacker can enumerate which emails have accounts. | NOT MITIGATED. Accepted risk: low severity at current scale (under 100 users). Will change to generic "If this email is not registered, you will receive a verification email" before external launch. Owner: David. Date: before Week 15. |
| Denial of Service | Attacker submits thousands of signup requests to exhaust database connections or trigger rate limits on the Supabase free tier | No rate limiting currently on POST /auth/signup endpoint | NOT MITIGATED. Action item: add rate limiting middleware (e.g. express-rate-limit, 10 requests per IP per minute on auth endpoints). Owner: David. Target date: 28 May 2026. |
| Elevation of Privilege | Newly registered user attempts to access admin routes (e.g. GET /api/admin/spaces) before their role is set | Admin routes protected by `requireAdmin` middleware that checks `role` column in the users table server-side. Role is set to `user` at account creation. Client cannot supply or modify their role. | Mitigated |

---

## Flow 2: User Login and Session Management

**Description:** User enters email and password, Supabase validates credentials and issues a JWT, JWT is stored in an httpOnly cookie, subsequent requests include the cookie.

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | Attacker uses stolen credentials to log in as another user | No additional MFA currently. Password requirement: minimum 8 characters. Supabase enforces bcrypt hashing. | PARTIALLY MITIGATED. Weak mitigation: no brute force protection on login endpoint. Action item: add rate limiting to POST /auth/login. Owner: David. Date: 28 May 2026. |
| Tampering | JWT tampered with to escalate privileges (e.g. change role claim from user to admin) | JWT is signed with Supabase's secret key. Tampered JWTs fail signature validation and are rejected. Role claims are re-validated server-side on every request. | Mitigated |
| Repudiation | User denies performing actions taken during their session | Session ID tied to user ID in server logs. All booking actions logged with user ID and timestamp. Supabase RLS policies enforce that users can only modify their own records. | Mitigated |
| Information Disclosure | JWT stored in localStorage is accessible to any JavaScript on the page, including injected scripts (XSS) | JWT stored in httpOnly cookie, not localStorage. httpOnly cookies are not accessible to JavaScript. | Mitigated |
| Denial of Service | Attacker floods login endpoint with requests, causing legitimate users to be locked out or slowing the service | No rate limiting on login endpoint currently. | NOT MITIGATED. Same action item as Flow 1: rate limiting on auth endpoints. Owner: David. Date: 28 May 2026. |
| Elevation of Privilege | Expired or invalid session used to make requests | Supabase JWT has a 1-hour expiry. Refresh tokens expire after 7 days of inactivity. Server validates JWT on every request. Expired tokens are rejected. | Mitigated |

---

## Flow 3: Study Space Search

**Description:** User enters a search query (building name, space type, or time slot), the app queries the Supabase spaces table, and results are returned and rendered.

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | Not applicable to a read-only search query | N/A | N/A |
| Tampering | Search query parameters tampered with to inject malicious SQL (SQL injection) | Supabase client uses parameterised queries. Raw SQL strings are not constructed from user input in our codebase. Verified by code review on 21 May 2026. | Mitigated |
| Repudiation | User denies submitting a specific search | All search events logged as `space_searched` in Mixpanel with user ID and query string. | Mitigated |
| Information Disclosure | Search results reveal spaces that the requesting user does not have permission to see (e.g. restricted faculty spaces) | Supabase RLS policy on `spaces` table: `WHERE is_restricted = false OR user_role = 'faculty'`. Restricted spaces are filtered server-side, not client-side. | Mitigated |
| Denial of Service | Attacker sends rapid search requests with complex queries to slow the database | No query rate limiting or query complexity limit. Free-text search scans the full spaces table. | NOT MITIGATED. Accepted risk: database has under 200 rows currently. Performance degradation would not be user-visible. Will add index on commonly searched columns before scaling. Owner: Nino. Date: when table exceeds 1000 rows. |
| Elevation of Privilege | Search endpoint used to probe internal database structure | Error messages in production return generic "Something went wrong" with no stack trace or schema information. Verified by testing POST /api/search with malformed input. | Mitigated |

---

## Flow 4: Booking Creation and Confirmation

**Description:** User selects a space and time slot, submits a booking request, the server validates availability, creates a booking record, and returns a confirmation.

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | User creates a booking under another user's ID by manipulating the request body | `user_id` in booking records is set server-side from the validated JWT, not from the request body. Client cannot supply a different user ID. Supabase RLS enforces this at the database level. | Mitigated |
| Tampering | Two users submit overlapping booking requests simultaneously, resulting in a double booking | Database constraint: UNIQUE on (space_id, time_slot). The second insert will fail with a unique constraint violation. Server returns a clear error to the second user. | Mitigated |
| Repudiation | User denies making a booking, disputes a no-show charge (if fees implemented later) | Booking record contains user_id, space_id, time slot, and created_at timestamp. IP address of booking request logged in server function logs. | Mitigated |
| Information Disclosure | Booking confirmation response leaks other users' booking data (e.g. in a list of all bookings for a space) | GET /api/spaces/:id/bookings returns only time slots (busy or free), not the names or IDs of users who made those bookings. User identity is not exposed in any public-facing response. | Mitigated |
| Denial of Service | User or bot floods the booking endpoint with requests, filling all available slots with fake bookings | No rate limiting on booking creation. A malicious user could book all slots. | NOT MITIGATED. Action item: rate limit booking creation to 5 bookings per user per hour. Owner: David. Date: 28 May 2026. |
| Elevation of Privilege | Regular user attempts to delete or modify another user's booking via the API | DELETE /api/bookings/:id and PATCH /api/bookings/:id check that the booking's user_id matches the requesting user's ID from the JWT. Supabase RLS additionally enforces this at the database level. Tested manually on 20 May 2026. | Mitigated |

---

## Flow 5: Account Deletion and Data Export

**Description:** User submits an account deletion request via email, the team manually processes the deletion by removing records from Supabase and requesting deletion from Mixpanel.

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | Someone requests deletion of another user's account by impersonating them via email | Deletion requests are only accepted from the email address associated with the account. Team verifies the from address against the Supabase users table before processing. | Mitigated (manual process) |
| Tampering | Deletion request intercepted and modified (e.g. to delete a different account) | Deletions are manual processes by the team. The team member processing the deletion verifies the user ID before running the delete command. | Mitigated |
| Repudiation | User denies requesting deletion after data has been removed | Deletion request emails are retained in the team inbox for 90 days after processing. | Mitigated |
| Information Disclosure | Data export contains more data than the user is entitled to (e.g. other users' booking records) | Data exports are generated by querying WHERE user_id = [requesting user's ID] only. Output is reviewed by a team member before sending. | Mitigated (manual review) |
| Denial of Service | Attacker floods the deletion request email to overwhelm the manual process | At current scale (under 100 users), this is not a material risk. If automated, would add rate limiting. | Accepted risk at current scale |
| Elevation of Privilege | Not applicable: deletion reduces, not increases, privileges | N/A | N/A |

---

## Dependency Audit

**Command used:** `npm audit`
**Date run:** 21 May 2026
**Working directory:** `/src/frontend/`

**Summary output:**
```
found 3 vulnerabilities (1 low, 1 moderate, 1 high)
```

**Finding 1 (High):**
- Package: `nth-check` version 1.0.2 (transitive dependency via `react-scripts`)
- CVE: CVE-2021-3803
- Vulnerability: Inefficient regular expression complexity that can cause ReDoS (Regular Expression Denial of Service)
- Remediation: This is a transitive dependency introduced by `react-scripts`. Direct fix requires upgrading `react-scripts` to 5.0.1 or above. We are on 5.0.0. Running `npm install react-scripts@5.0.1`.
- Owner: Nino
- Target date: 28 May 2026
- Status: In progress

**Finding 2 (Moderate):**
- Package: `loader-utils` version 2.0.3 (transitive dependency)
- CVE: CVE-2022-37601
- Vulnerability: Prototype pollution
- Remediation: Addressed in react-scripts upgrade above. Will resolve when Finding 1 is fixed.
- Owner: Nino
- Target date: 28 May 2026
- Status: Dependent on Finding 1 fix

**Finding 3 (Low):**
- Package: `postcss` version 7.0.39
- CVE: CVE-2023-44270
- Vulnerability: Line return parsing issue, low exploitability
- Remediation: Transitive dependency. Will update when a non-breaking upgrade path is available.
- Owner: Nino
- Target date: Week 14 review
- Status: Accepted at current severity

---

## Secrets Check

**Commands run:**
```bash
git log --all --full-history -- "**/.env"
git log -p | grep -i "api_key\|secret\|password\|token" | head -40
```

**Result:** CLEAN. No `.env` files in git history. No API keys, secrets, or tokens found in any commit.

**Current .env status:**
- [x] `.env` file exists locally with all keys
- [x] `.env` is listed in `.gitignore`
- [x] `.env.example` exists in the repo with placeholder values only (e.g. `SUPABASE_URL=your_supabase_url_here`)
- [x] No `.env` file has ever been committed (verified by secrets check above)

---

## Top Three Vulnerabilities Summary

| Priority | Vulnerability | Flow or component | Mitigation or action | Owner | Date |
|----------|--------------|------------------|---------------------|-------|------|
| 1 | No rate limiting on login and booking endpoints | Flows 1, 2, 4 | Add express-rate-limit to auth and booking routes | David | 28 May 2026 |
| 2 | nth-check ReDoS vulnerability in transitive dependency | Frontend build | Upgrade react-scripts to 5.0.1 | Nino | 28 May 2026 |
| 3 | Email enumeration via specific error messages on signup | Flow 1 | Change to generic "check your email" response | David | Before Week 15 |
