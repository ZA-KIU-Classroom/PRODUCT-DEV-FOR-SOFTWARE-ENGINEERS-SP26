# Security Tabletop

**Product:** [Your product name]
**Team:** [Your team name]
**Date:** [Date]
**Audit run date:** [Date you ran npm audit or pip-audit]

---

## Overview

This document applies the STRIDE threat model to our five highest-traffic user flows. For every threat identified, we either name the mitigation in place or explicitly accept the risk with a written rationale. Unexamined threats are not low risks. They are unknown risks.

**STRIDE reference:**

| Letter | Category | The question |
|--------|----------|-------------|
| S | Spoofing | Can an attacker impersonate a legitimate user or system component? |
| T | Tampering | Can data be modified in transit or at rest without detection? |
| R | Repudiation | Can a user deny performing an action, with no audit trail to prove otherwise? |
| I | Information Disclosure | Can sensitive data be exposed to unauthorised parties? |
| D | Denial of Service | Can this flow be abused to make the service unavailable to legitimate users? |
| E | Elevation of Privilege | Can a user gain capabilities beyond their permission level? |

---

## Five User Flows Selected

List the five flows you are analysing and justify why they are the five highest-traffic or highest-risk flows.

| # | Flow name | Why selected |
|---|-----------|-------------|
| 1 | [e.g. User signup and email verification] | [e.g. Entry point for all users. Compromise here exposes all downstream data.] |
| 2 | [e.g. User login and session management] | [e.g. Authentication is the primary attack surface for account takeover.] |
| 3 | [e.g. Core product action: booking a study space] | [e.g. Highest traffic flow. Carries booking data and payment intent.] |
| 4 | [e.g. Profile update including email change] | [e.g. Email change can be used for account hijack.] |
| 5 | [e.g. Account deletion and data export] | [e.g. Data export exposes all stored personal data in one request.] |

---

## Flow 1: [Flow name]

**Description:** [One sentence describing what happens in this flow from the user's perspective]

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | [e.g. Attacker could register with someone else's email address and gain access to their account if email is not verified] | [e.g. Email verification required before account activation. Unverified accounts cannot access core features.] | Mitigated |
| Tampering | [e.g. Registration form data could be tampered with in transit] | [e.g. HTTPS enforced on all routes. Vercel enforces HTTPS by default.] | Mitigated |
| Repudiation | [e.g. User could deny completing signup and claim they never agreed to terms] | [e.g. Signup timestamp and IP recorded in users table. Terms version logged at signup.] | Mitigated |
| Information Disclosure | [e.g. Error messages on failed signup could reveal whether an email is already registered, enabling enumeration] | [e.g. Currently our error message says "Email already in use." This is a known gap.] | NOT MITIGATED - accepted risk: low severity at current scale, will address before external launch |
| Denial of Service | [e.g. Attacker could submit thousands of signup requests to exhaust database connections] | [e.g. No rate limiting currently on signup endpoint.] | NOT MITIGATED - action item: add rate limiting to POST /auth/signup by [date], owner: [name] |
| Elevation of Privilege | [e.g. Newly registered user could attempt to access admin routes] | [e.g. Admin routes protected by role check middleware. Role is set server-side at account creation, not client-supplied.] | Mitigated |

---

## Flow 2: [Flow name]

**Description:** [One sentence describing this flow]

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | [Threat] | [Mitigation or gap] | [Mitigated / NOT MITIGATED + reason or action] |
| Tampering | [Threat] | [Mitigation or gap] | |
| Repudiation | [Threat] | [Mitigation or gap] | |
| Information Disclosure | [Threat] | [Mitigation or gap] | |
| Denial of Service | [Threat] | [Mitigation or gap] | |
| Elevation of Privilege | [Threat] | [Mitigation or gap] | |

---

## Flow 3: [Flow name]

**Description:** [One sentence describing this flow]

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | | | |
| Tampering | | | |
| Repudiation | | | |
| Information Disclosure | | | |
| Denial of Service | | | |
| Elevation of Privilege | | | |

---

## Flow 4: [Flow name]

**Description:** [One sentence describing this flow]

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | | | |
| Tampering | | | |
| Repudiation | | | |
| Information Disclosure | | | |
| Denial of Service | | | |
| Elevation of Privilege | | | |

---

## Flow 5: [Flow name]

**Description:** [One sentence describing this flow]

| STRIDE category | Threat identified | Mitigation in place | Status |
|----------------|------------------|--------------------|---------| 
| Spoofing | | | |
| Tampering | | | |
| Repudiation | | | |
| Information Disclosure | | | |
| Denial of Service | | | |
| Elevation of Privilege | | | |

---

## Dependency Audit

### Audit run

**Command used:** [e.g. `npm audit` or `pip-audit`]
**Date run:** [Date]
**Working directory:** [e.g. root of repo, or `src/frontend/`]

**Summary:**
```
[Paste the summary output from the audit tool here]
e.g.
found 12 vulnerabilities (2 low, 7 moderate, 2 high, 1 critical)
```

### Three highest-priority findings

**Finding 1 (Critical or High):**
- Package: [package name and version]
- CVE: [CVE number if available]
- Vulnerability: [One sentence description]
- Remediation: [e.g. Update to version X.X.X. Command: npm install package@X.X.X]
- Owner: [Name]
- Target date: [Date]
- Status: [Fixed / In progress / Accepted with rationale]

**Finding 2:**
- Package: [package name and version]
- CVE: [CVE number if available]
- Vulnerability: [One sentence]
- Remediation: [Action]
- Owner: [Name]
- Target date: [Date]
- Status:

**Finding 3:**
- Package: [package name and version]
- CVE: [CVE number if available]
- Vulnerability: [One sentence]
- Remediation: [Action]
- Owner: [Name]
- Target date: [Date]
- Status:

---

## Secrets Check

### Commands run

```bash
git log --all --full-history -- "**/.env"
git log -p | grep -i "api_key\|secret\|password\|token" | head -40
```

### Result

**Clean or compromised:** [Clean: no secrets found in history | Compromised: secrets found (see below)]

**If compromised, for each secret found:**

| Secret | When committed | What we did |
|--------|---------------|------------|
| [e.g. Supabase service role key] | [e.g. Commit abc1234 on 15 March 2026] | [e.g. Key rotated on [date]. Git history rewritten with git filter-branch. Force pushed. All team members re-cloned.] |

**Current .env status:**
- [ ] `.env` file exists locally
- [ ] `.env` is listed in `.gitignore`
- [ ] `.env.example` exists in the repo with placeholder values only
- [ ] No `.env` file has ever been committed (verified by secrets check above)

---

## Top Three Vulnerabilities Summary

After completing STRIDE and the dependency audit, list your three highest-priority vulnerabilities.

| Priority | Vulnerability | Flow or component | Mitigation or action | Owner | Date |
|----------|--------------|------------------|---------------------|-------|------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
