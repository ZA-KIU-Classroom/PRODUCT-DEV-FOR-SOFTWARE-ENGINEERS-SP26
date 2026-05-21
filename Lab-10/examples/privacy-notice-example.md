# Privacy Notice — StudySpace Finders

> **This is a worked example for Lab 10. It uses the fictional StudySpace Finders product.
> Your team must write your own privacy notice describing your actual product.**

**Product:** StudySpace Finders
**Team:** StudySpace Finders (fictional reference team)
**Version:** 1.0
**Date:** 21 May 2026
**Effective from:** 1 April 2026

---

## 1. Who We Are

StudySpace Finders is a mobile and web application that helps students at Kutaisi International University find and book available study spaces on campus. It is developed by the StudySpace Finders team, a student team at Kutaisi International University as part of CS-PD-2026.

**Data controller contact:**
Name: Ana Beridze (Discovery Lead)
Email: ana.beridze@student.kiu.edu.ge

---

## 2. What Personal Data We Collect and Why

### 2.1 Account and Identity Data

| Data category | Specific fields | Why we collect it | Lawful basis | Who can access it |
|---------------|----------------|-------------------|--------------|------------------|
| Account credentials | Email address, bcrypt-hashed password | To create and authenticate your account | Contract: necessary to provide the service | Supabase auth service only. Plaintext password never stored. |
| Student identifier | KIU student ID number (optional, entered by user) | To verify eligibility for booking university spaces | Legitimate interest: ensuring only eligible students access university resources | Internal team only, not shared with third parties |
| Display name | First name only (user-provided) | To personalise the app interface | Contract: necessary to provide the service | Visible to the user in their own session only |

### 2.2 Usage and Behavioural Data

| Data category | Specific fields | Why we collect it | Lawful basis | Third-party processor |
|---------------|----------------|-------------------|--------------|----------------------|
| Event data | space_searched (with query string and filter selections), space_viewed (with space_id), booking_attempted (with space_id and time slot), booking_completed (with space_id, time slot, duration), booking_cancelled (with space_id and reason if provided) | To understand how users find and book spaces, to improve search relevance, and to measure our core activation metric | Legitimate interest: product improvement and operating the service | Mixpanel Inc., 405 Howard Street, San Francisco CA 94105 |
| Session data | Session ID, timestamp of session start and end, device type (mobile or desktop), browser type, operating system | To maintain your logged-in session and to diagnose errors | Legitimate interest: operating the service and diagnosing errors | Supabase (session storage), Vercel (server logs) |
| Location data | Approximate campus location derived from user-selected building (not GPS coordinates) | To show study spaces near the user's current or intended location on campus | Legitimate interest: core feature of the product | Not shared with third parties. Stored in Supabase alongside booking records. |
| Error logs | Error type, stack trace (server-side only, not user-readable), request path, timestamp | To diagnose and fix product errors | Legitimate interest: operating and improving the product | Vercel (function logs, retained 7 days by default) |

### 2.3 Booking Records

| Data category | Specific fields | Why we collect it | Lawful basis | Third-party processor |
|---------------|----------------|-------------------|--------------|----------------------|
| Booking records | User ID, space ID, booking date and time, duration, booking status (confirmed, cancelled, completed) | To confirm and manage study space bookings | Contract: necessary to fulfil the booking service | Stored in Supabase. Not shared with third parties. |

---

## 3. Third-Party Processors

| Processor | Service type | Data they receive | Their privacy policy |
|-----------|-------------|-------------------|---------------------|
| Supabase Inc. | Database (PostgreSQL) and authentication | All user account data, booking records, session tokens | supabase.com/privacy |
| Vercel Inc. | Hosting, serverless API functions, CDN | Server request logs including IP addresses, error logs | vercel.com/legal/privacy-policy |
| Mixpanel Inc. | Product analytics | Event data (space_searched, booking_attempted, etc.), session identifiers, device type, approximate location (campus building) | mixpanel.com/legal/privacy-policy |

We do not use Google Analytics, Facebook Pixel, or any advertising network. We do not sell user data to any third party.

---

## 4. How Long We Keep Your Data

| Data category | Retention period | What triggers deletion |
|---------------|-----------------|----------------------|
| Account credentials and profile | Until account deletion request + 30 days | User submits deletion request via email |
| Booking records | 12 months from the booking date | Automatic deletion on a monthly schedule |
| Event analytics data (Mixpanel) | 12 months rolling | Mixpanel data retention setting, configured in our project settings |
| Session tokens | Session duration + 24 hours (for token refresh) | Automatic expiry |
| Server logs (Vercel) | 7 days | Automatic deletion by Vercel |
| Error logs | 30 days | Automatic deletion by Vercel |

---

## 5. Your Rights

| Right | What it means | How to exercise it | Our response time |
|-------|--------------|-------------------|------------------|
| Right to access | Request a copy of all personal data we hold about you | Email ana.beridze@student.kiu.edu.ge with subject "Data Access Request - StudySpace Finders" | Within 30 days |
| Right to erasure | Request deletion of your personal data | Email with subject "Erasure Request - StudySpace Finders". We will delete your account, booking records, and request deletion of your Mixpanel data via the Mixpanel user deletion API. | Within 30 days |
| Right to rectification | Request correction of inaccurate data | Email with subject "Rectification Request - StudySpace Finders" | Within 30 days |
| Right to restriction | Request we stop certain processing | Email with subject "Processing Restriction - StudySpace Finders" | Within 30 days |
| Right to portability | Request your data in a machine-readable format | Email with subject "Data Portability Request". We will export your account data and booking history as a JSON file. | Within 30 days |
| Right to object | Object to processing based on legitimate interest | Email with subject "Processing Objection". Note: objecting to analytics processing will not affect your ability to use the product. | Within 30 days |

---

## 6. Data Breach Procedure

In the event of a personal data breach:

1. We will assess the breach within 24 hours of becoming aware of it
2. We will notify the relevant supervisory authority within 72 hours if the breach is likely to result in a risk to the rights and freedoms of natural persons
3. We will notify affected users without undue delay if the breach is likely to result in a high risk

**Person responsible for breach response:** Ana Beridze, ana.beridze@student.kiu.edu.ge

---

## 7. Cookies and Tracking Technologies

| Cookie or tracker | Purpose | Duration | Can you opt out? |
|-------------------|---------|----------|-----------------|
| `sb-auth-token` (Supabase) | Maintains your login session | Session + 24 hours | No, required for login to function |
| `mp_[token]_mixpanel` | Mixpanel analytics identifier, persists your analytics user ID across sessions | 1 year | Yes. Email us with subject "Analytics Opt-Out" and we will delete your Mixpanel identity and stop sending events for your user ID. |

---

## 8. Changes to This Notice

We will update this notice when our data practices change. We will notify users of material changes by in-app notification at next login. The version number and effective date at the top of this document will be updated.

---

## 9. Contact

**Name:** Ana Beridze
**Email:** ana.beridze@student.kiu.edu.ge
**Response time:** Within 5 business days for general questions, within 30 days for formal rights requests

*This privacy notice was last updated on 21 May 2026. Version 1.0.*
