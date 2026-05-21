# Consent Flow Design

**Product:** [Your product name]
**Team:** [Your team name]
**Date:** [Date]
**Related file:** `08-legal/privacy-notice.md`

---

## Overview

This document describes how our product obtains, records, and allows withdrawal of user consent under GDPR. Consent under GDPR must satisfy six requirements: freely given, specific, informed, unambiguous, withdrawable, and documented.

**Current state:** [Choose one and delete the others]
- Our consent mechanism is fully implemented and described below
- Our consent mechanism is partially implemented. Gaps are explicitly noted in each section.
- Our consent mechanism does not yet exist. This document describes our intended implementation and the timeline for building it.

---

## 1. What Requires Consent

Not all data processing requires consent. Processing necessary for a contract (e.g. account creation) uses the contract lawful basis. Processing based on legitimate interest does not require consent but requires a legitimate interest assessment. Consent is specifically required for:

| Processing activity | Why consent is needed (not another lawful basis) |
|--------------------|-------------------------------------------------|
| [e.g. Sending marketing emails] | Marketing requires explicit opt-in consent, cannot rely on legitimate interest |
| [e.g. Sharing data with third-party analytics providers beyond legitimate interest scope] | [Reason] |
| [Add every processing activity in your product that requires consent] | |

If your product has no processing that requires consent (all processing uses contract or legitimate interest), state that here and explain why. This is a valid answer if it is correct.

---

## 2. Where Consent Is Obtained: The Consent Moment

Describe where in your user journey the consent moment appears. Be specific about the screen, the user action, and the UI element.

**Location in the flow:**
[e.g. After the user fills in their email and password on the signup screen, before they click the Create Account button]

**What the user sees:**
[Describe the UI element in words. If you have a wireframe, describe it. If you have a screenshot, link it.]

Example format:
```
Below the signup form, before the submit button:

  [ ] I agree to receive product updates and tips by email (optional)

  By creating an account, you agree to our Terms of Service. 
  We process your data to provide the service (legitimate interest). 
  For details, see our Privacy Notice.

  [Create Account]
```

**Key requirements to verify in your design:**

- [ ] The consent checkbox is NOT pre-ticked (a pre-ticked box is not valid consent under GDPR)
- [ ] Analytics consent and marketing consent are SEPARATE checkboxes, not bundled
- [ ] Consent to terms of service (contract) is separate from consent to marketing (consent)
- [ ] The user can create an account and use the product without ticking the optional consent boxes
- [ ] The privacy notice is linked and accessible before the user consents

---

## 3. Consent Categories

List each distinct consent category separately. Do not bundle purposes.

### Category 1: [e.g. Marketing communications]

**Purpose:** [e.g. Sending product updates, tips, and promotional content by email]
**Is it optional?** [Yes or No. Marketing consent must always be optional.]
**Default state:** [e.g. Unchecked by default]
**UI element:** [e.g. Checkbox with label "I would like to receive product updates by email"]
**What happens if the user declines:** [e.g. Account is created normally. User does not receive marketing emails.]

---

### Category 2: [e.g. Analytics data processing beyond legitimate interest]

**Purpose:** [e.g. Using detailed behavioural analytics to build a profile for product personalisation]
**Is it optional?** [Yes or No]
**Default state:** [e.g. Unchecked by default]
**UI element:** [Describe the UI element]
**What happens if the user declines:** [Describe the fallback]

---

[Add a section for each consent category. If your product uses analytics solely for product improvement under legitimate interest, you do not need a consent category for it, but you must document the legitimate interest assessment in your privacy notice.]

---

## 4. Withdrawal Mechanism

Consent must be as easy to withdraw as it was to give. If consent was one click, withdrawal must also be one click.

**Where can a user withdraw consent?**
[e.g. Settings > Privacy > Manage consent preferences]

**How many steps does withdrawal take?**
[e.g. Two steps: navigate to settings, toggle off the consent switch]

**Current state of the withdrawal UI:**
[Choose one: Implemented and accessible at [URL/path] | In progress, expected by [date] | Not yet built, gap acknowledged]

**What happens to data collected before withdrawal?**
[e.g. Event data already sent to Mixpanel remains there subject to Mixpanel's data retention policy. No new events will be sent.]

---

## 5. Consent Storage Record

You must be able to prove consent was given, when, to what version of the privacy notice, and what action the user took.

**Where is the consent record stored?**
[e.g. In the `users` table in our Supabase database, in a `consent` JSONB column]

**Schema:**
```
consent: {
  marketing_email: {
    given: true / false,
    timestamp: ISO 8601 datetime,
    privacy_notice_version: "1.0",
    method: "checkbox on signup screen"
  },
  [other consent categories]
}
```

**Current state:**
[Choose one: Implemented and storing consent records | In progress | Not yet implemented, gap acknowledged]

**How long do you retain consent records?**
[e.g. Consent records are retained for the life of the account plus 2 years, to handle any disputes about whether consent was given]

---

## 6. Gaps and Remediation Plan

List every gap between your current implementation and full GDPR compliance. For each gap, name an owner and a date.

| Gap | Owner | Target completion date |
|-----|-------|----------------------|
| [e.g. Withdrawal UI not yet built] | [Name] | [Date] |
| [e.g. Consent record not stored in database] | [Name] | [Date] |
| [Add all gaps. An empty table here means you are fully compliant or you have not looked carefully enough.] | | |
