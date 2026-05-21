# Lab 10: Compliance, Security, and Reliability Audit

**Course:** CS-PD-2026 | Product Development for Software Engineers
**Instructor:** Zeshan Ahmad
**Session:** Week 12 lab slot | Group A: Thursday 21 May 2026 at 14:00 | Group B: Friday 22 May 2026 at 13:00
**Location:** In person, standard lab room
**Duration:** 120 minutes
**Repo folder:** `Lab-10/` in the classroom organisation

---

## Overview

Your product is deployed. Real users can reach it. That means real legal obligations, real attack surface, and real consequences if it goes down at the wrong moment.

Lab 10 is an audit lab. You are not building new features. You are examining what you have already built through four lenses: privacy law, consent design, security threat modelling, and reliability planning. Every document you produce today must describe your actual product. A generic template filled with placeholder text earns zero marks on specificity.

This lab connects directly to the Week 11 lecture on Legal, IP, Privacy, Security, and Reliability. GDPR and CCPA, STRIDE threat modelling, OWASP Top 10, SLOs, and error budgets from that lecture are the conceptual input for every activity today. If you did not attend or have not reviewed the slides, read them before your session starts.

---

## What You Will Build

| File | Location in your team repo | Points |
|------|---------------------------|--------|
| Privacy Notice | `08-legal/privacy-notice.md` | 4 |
| Consent Flow Design | `03-build/privacy-security/consent-form.md` | 3 |
| Security Tabletop | `03-build/privacy-security/security-tabletop.md` | 4 |
| SLO Sheet and Error Budget | `03-build/reliability/slo-sheet.md` + `error-budget.md` | 3 |
| **Total** | | **14** |

Participation is assessed on in-lab progress at the 0:20, 0:50, 1:20, and 1:50 checkpoints. Work must be visible in your repo by the end of the session.

---

## Prerequisites

Before you arrive you must have:

- [ ] Attended or reviewed the Week 11 lecture (Legal, IP, Privacy, Security, and Reliability)
- [ ] Your live deployment URL accessible and working
- [ ] Your event schema open in a browser tab so you know exactly what data you collect
- [ ] Your team's `03-build/privacy-security/` and `03-build/reliability/` folders created in your repo
- [ ] Your `08-legal/` folder created in your repo

Folder setup (run this if you have not already):

```bash
mkdir -p 08-legal
mkdir -p 03-build/privacy-security
mkdir -p 03-build/reliability
touch 08-legal/privacy-notice.md
touch 03-build/privacy-security/consent-form.md
touch 03-build/privacy-security/security-tabletop.md
touch 03-build/reliability/slo-sheet.md
touch 03-build/reliability/error-budget.md
```

---

## Lab Structure

| Time | Part | Activity | Deliverable |
|------|------|----------|-------------|
| 0:00 to 0:10 | Setup | Folder check, deployment URL confirmed, event schema open | Team aligned on data collected |
| 0:10 to 0:40 | Part 1 | Privacy Notice | `08-legal/privacy-notice.md` drafted |
| 0:40 to 1:00 | Part 2 | Consent Flow Design | `03-build/privacy-security/consent-form.md` drafted |
| 1:00 to 1:30 | Part 3 | Security Tabletop | `03-build/privacy-security/security-tabletop.md` drafted |
| 1:30 to 1:50 | Part 4 | SLO Sheet and Error Budget | Both reliability files drafted |
| 1:50 to 2:00 | Commit | All files committed and pushed | Submission tag applied |

---

## Part 1: Privacy Notice (30 minutes)

### Goal

Write a privacy notice that describes what your product actually does with user data. Not a generic template. Not a copy from another app. Your product.

### File

`08-legal/privacy-notice.md`

Use the template at `Lab-10/templates/privacy-notice-template.md`.

### What must be in this document

**Data inventory.** List every category of personal data your product collects. For each category:
- What the data is (email, location, booking behaviour, device type, session duration, etc.)
- Why you collect it (lawful basis: legitimate interest, contract, consent, or legal obligation)
- Where it is stored and with which third-party processors (Supabase, Firebase, Vercel, Mixpanel, Amplitude, etc.)
- How long you retain it and what triggers deletion

**User rights section.** Under GDPR, users have the right to access, erasure, rectification, restriction, portability, and objection. For each right, state how a user exercises it: the contact method and the response time you commit to.

**Data breach procedure.** You must notify the supervisory authority within 72 hours of becoming aware of a breach. State this and name the person on your team who owns this responsibility.

**Contact details.** Name and email of the person responsible for data-related requests.

### Common mistakes to avoid

Copying a privacy notice from another app or from a generator. If your policy says you do not share data with third parties and you use Mixpanel, your policy is incorrect. Regulators check this.

Writing "we may collect" instead of "we collect." Vague language does not satisfy GDPR. If you collect it, state it.

Ignoring third-party processors. Every SDK, analytics tool, hosting provider, and authentication service that touches user data must be named.

### Instructor checkpoint at 0:40

The instructor will ask each team to name: every category of personal data collected, every third-party processor, and the lawful basis for each processing activity. Teams who cannot answer without reading from a generator output need to go back and write from first principles.

---

## Part 2: Consent Flow Design (20 minutes)

### Goal

Design and document the consent mechanism in your onboarding flow. Consent under GDPR must be freely given, specific, informed, unambiguous, withdrawable, and documented. Your consent flow must satisfy all six requirements.

### File

`03-build/privacy-security/consent-form.md`

Use the template at `Lab-10/templates/consent-form-template.md`.

### What must be in this document

**Wireframe description.** Describe in words (or ASCII if you prefer) where in your onboarding flow the consent moment appears, what the user sees, and what action they take. A pre-ticked checkbox is invalid under GDPR. Silence is not consent. Continued use of a site is not consent.

**Consent categories.** Separate consent for each distinct purpose. Analytics consent is not the same as marketing consent. If you bundle them, the consent is invalid.

**Withdrawal mechanism.** How does a user withdraw consent after giving it? It must be as easy as giving consent. If consent was one click, withdrawal must also be one click. Document where this is in your product.

**Storage record.** How do you store the fact that consent was given? You must be able to prove: who consented, when, to what version of your privacy notice, and what action they took. Name the database table or log file.

### What kills marks

Describing a consent flow that does not exist in your product yet without flagging it as a gap to be closed.

Treating this as a design exercise. This document must describe reality or name the delta between reality and compliance.

---

## Part 3: Security Tabletop (30 minutes)

### Goal

Apply the STRIDE threat model to your five highest-traffic user flows. For every threat you identify, you must either name the mitigation in place or explicitly accept the risk with a written rationale.

### File

`03-build/privacy-security/security-tabletop.md`

Use the template at `Lab-10/templates/security-tabletop-template.md`.

### The five user flows to analyse

Pick your five highest-traffic flows. For most products these are: signup or login, the core action (booking, posting, searching, etc.), profile or settings update, payment or upgrade (if applicable), and data export or account deletion. If your product is different, choose the five flows that carry the most user data or have the most potential for harm if compromised.

### STRIDE applied to each flow

For each flow, work through all six STRIDE categories:

| Category | Question to ask |
|----------|----------------|
| **S - Spoofing** | Can an attacker impersonate a legitimate user or system component in this flow? |
| **T - Tampering** | Can data be modified in transit or at rest without detection in this flow? |
| **R - Repudiation** | Can a user deny performing an action in this flow, and do you have an audit trail to prove otherwise? |
| **I - Information Disclosure** | Can sensitive data be exposed to unauthorised parties through this flow? |
| **D - Denial of Service** | Can this flow be abused to make the service unavailable to legitimate users? |
| **E - Elevation of Privilege** | Can a user gain capabilities beyond their permission level through this flow? |

For each threat identified, write:
- The specific threat (one sentence)
- The mitigation already in place (or "not mitigated")
- If not mitigated: accepted risk with rationale, or action item with owner and date

### Dependency audit

Run `npm audit` or `pip-audit` on your project. Document:
- Number of critical and high severity findings
- The three highest-priority findings with the specific package, CVE if available, and your remediation plan
- Date audit was run

### Secrets check

Check your git history for committed secrets:

```bash
git log --all --full-history -- "**/.env"
git log -p | grep -i "api_key\|secret\|password\|token" | head -20
```

State the result: clean or compromised. If compromised, state which secrets, when they were committed, and what you have done (rotate the key, scrub the history, or accept the risk with rationale).

### Instructor checkpoint at 1:30

Each team must have at least three flows completed with STRIDE applied and the dependency audit run. Teams still on flow one at this checkpoint should narrow to three flows only and complete those.

---

## Part 4: SLO Sheet and Error Budget (20 minutes)

### Goal

Define measurable reliability targets for your product and calculate the error budget those targets imply. An SLO is not a feeling. It is a number with a time window.

### Files

`03-build/reliability/slo-sheet.md` and `03-build/reliability/error-budget.md`

Use the templates at `Lab-10/templates/slo-sheet-template.md`.

### SLO Sheet: what must be in this document

**At least two SLIs with measurement method.** An SLI is a specific metric you measure. For each SLI:
- The metric definition (exact formula, e.g. successful requests / total requests)
- Where it is measured (your analytics tool, server logs, uptime monitor)
- Current measured value if available, or "not yet measured" if not

**SLO targets for each SLI.** An SLO is the target you set for your SLI over a time window. For each:
- The target percentage or value
- The time window (rolling 30 days is standard)
- Why this target is achievable given your current infrastructure

**Severity definitions.** Define SEV1, SEV2, and SEV3 for your product:
- SEV1: core flow completely down, all hands
- SEV2: degraded experience, on-call investigates
- SEV3: minor issue, fix in next working session

Calibrate these to your actual product. A booking app has different SEV1 criteria than a content platform.

### Error Budget: what must be in this document

For each SLO, calculate the error budget:

```
Error budget = (1 - SLO target) x time window in minutes

Example: SLO = 99% over 30 days
Time window = 30 x 24 x 60 = 43,200 minutes
Error budget = 0.01 x 43,200 = 432 minutes
```

State what happens when the budget is exhausted:
- No new feature deployments until the window resets
- Engineering effort redirects to reliability improvement
- Incident review is mandatory before the next push

### What kills marks

An SLO of 100%. This means no error budget. No error budget means you cannot ship anything without violating your SLO. 100% is not a target. It is a lie.

SLOs that cannot be measured with your current tooling. If you have no uptime monitor and no server logging, you cannot measure availability. Either set up the measurement or set an SLO only for what you can actually measure.

---

## Committing Your Work

At the end of the session, commit all files with the following convention:

```bash
git add 08-legal/ 03-build/privacy-security/ 03-build/reliability/
git commit -m "[LAB-10] Compliance, security, and reliability audit"
git push origin main
git tag lab-10-submission
git push origin lab-10-submission
```

Every team member must have at least one commit in this session. The instructor reviews the commit history. A team where only one person committed all files will have individual participation marks reviewed.

---

## Grading Rubric Summary

| Component | Marks | Key criteria |
|-----------|-------|-------------|
| Privacy Notice | 4 | Data inventory covers every category collected, lawful basis stated for each, all third-party processors named, user rights section actionable |
| Consent Flow Design | 3 | Six GDPR requirements addressed, separate consent categories, withdrawal mechanism documented, storage record described |
| Security Tabletop | 4 | Five flows with STRIDE applied, every threat mitigated or accepted with rationale, dependency audit run and documented, secrets check completed |
| SLO Sheet and Error Budget | 3 | At least two SLIs with measurement method, SLO targets with time window, error budget calculated with arithmetic shown, severity definitions calibrated to product |
| **Total** | **14** | |

Full rubric with mark descriptors at `Lab-10/GRADING-RUBRIC.md`.

---

## Connection to Combined Checkpoint 2+3

The documents you produce today feed directly into Combined Checkpoint 2+3 and into the final repository review at Demo Day (Week 15). Specifically:

- `privacy-notice.md` is a required document for the checkpoint privacy and legal criterion
- `consent-form.md` demonstrates that your product handles user consent correctly before real users sign up
- `security-tabletop.md` is required evidence of security review
- `slo-sheet.md` and `error-budget.md` satisfy the reliability plan learning outcome assessed at Demo Day

Do not treat this lab as separate from your checkpoint work. These documents go directly into the repo that judges review at Demo Day.

---

## Resources

- Week 11 lecture slides: on Teams
- OWASP Top 10: owasp.org/Top10
- STRIDE reference: Microsoft Threat Modelling Tool documentation
- GDPR text: gdpr-info.eu
- Sample size and SLO calculator: availability-calculator.com
- Templates folder: `Lab-10/templates/`
- Worked examples: `Lab-10/examples/`
- Office hours: book via email at zeshan.ahmad@kiu.edu.ge

---

## Questions During Lab

Raise your hand. The instructor circulates at the 0:20, 0:50, 1:20, and 1:50 checkpoints and is available between checkpoints for individual team questions. If you are blocked on a specific data category or threat, write "TBD - needs investigation" and move on. Do not let one gap stop you from completing the rest of the audit.
