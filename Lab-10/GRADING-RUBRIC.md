# Lab 10 Grading Rubric

**Course:** CS-PD-2026 | Spring 2026
**Instructor:** Zeshan Ahmad
**Lab session:** Week 12 lab slot | Group A: Thu 21 May 14:00 | Group B: Fri 22 May 13:00
**Total marks:** 14

---

## Overview

Lab 10 is assessed on four components. Each component is graded on specificity and completeness. Documents that describe your actual product score full marks. Documents that use placeholder text, copy generic templates, or describe a different product score zero on specificity regardless of length.

Participation marks are assessed by the instructor at four checkpoints during the session: 0:20, 0:50, 1:20, and 1:50. Each checkpoint is binary: either you have made visible progress in your repo, or you have not.

---

## Component 1: Privacy Notice (4 marks)

**File:** `08-legal/privacy-notice.md`

| Mark | Descriptor |
|------|-----------|
| 4 | Data inventory lists every category of personal data with lawful basis, third-party processor, and retention schedule for each. User rights section names the specific contact method and response time. Data breach procedure names an owner. Contact details are present. The document could be published as a real privacy notice without modification. |
| 3 | Data inventory is complete but one category is missing a lawful basis, or one processor is unnamed. User rights are present but one right is missing or the contact method is vague. Document describes the actual product. |
| 2 | Data inventory covers the main categories but misses one or more significant data type (e.g. event data sent to analytics, auth tokens, log files). Lawful basis is present but generic. Third-party processors are partially listed. |
| 1 | Document is present but substantially incomplete. Data inventory has more gaps than content. Lawful basis is missing for most categories. The document does not describe the actual product in any specific way. |
| 0 | Not submitted, empty file, or generic template with no product-specific content. |

**Specificity check:** The instructor will ask each team to point to the line in the document that names their analytics provider and the lawful basis for sending event data to it. If that line does not exist, the document scores a maximum of 2.

---

## Component 2: Consent Flow Design (3 marks)

**File:** `03-build/privacy-security/consent-form.md`

| Mark | Descriptor |
|------|-----------|
| 3 | All six GDPR consent requirements addressed (freely given, specific, informed, unambiguous, withdrawable, documented). Consent categories are separated. Withdrawal mechanism is described with the same specificity as the consent mechanism. Storage record names the specific database table or log. Document is actionable: a developer could implement it from this description alone. |
| 2 | Five of the six requirements addressed. Consent categories exist but may be partially bundled. Withdrawal is mentioned but mechanism is vague. Storage record is present but incomplete. |
| 1 | Document is present. Consent is described but does not satisfy the GDPR requirements (e.g. pre-ticked boxes, bundled consent, no withdrawal mechanism). Describes an aspired state rather than the current product. |
| 0 | Not submitted, empty file, or describes a consent flow that is identical across all teams with no product-specific content. |

**Specificity check:** The instructor will ask each team how a user withdraws consent after giving it, and where the consent record is stored. If the team cannot answer from their document, maximum score is 1.

---

## Component 3: Security Tabletop (4 marks)

**File:** `03-build/privacy-security/security-tabletop.md`

| Mark | Descriptor |
|------|-----------|
| 4 | Five user flows documented with all six STRIDE categories applied to each. Every threat is either mitigated (with the specific mitigation named) or explicitly accepted (with a written rationale and owner). Dependency audit run with date, critical and high findings listed, and remediation plan for the top three. Secrets check completed with a clear result stated. Document demonstrates genuine security thinking applied to this specific product. |
| 3 | Four or five flows with STRIDE applied, but one or two STRIDE categories are missing from some flows. Mitigations are mostly present but one or two threats are neither mitigated nor explicitly accepted. Dependency audit is present. Secrets check completed. |
| 2 | Three flows with partial STRIDE application. Mitigations are described at a high level without specific implementation detail. Dependency audit may be missing. Secrets check present or absent. |
| 1 | Document present but STRIDE is applied to fewer than three flows, or STRIDE categories are confused or mislabelled. No dependency audit. Threats are listed without mitigations or acceptance rationale. |
| 0 | Not submitted, empty file, or generic STRIDE explanation with no application to any specific product flow. |

**Specificity check:** The instructor will name one of the team's user flows and ask them to state the Elevation of Privilege threat for that flow and the mitigation. If the team cannot answer, maximum score is 2.

---

## Component 4: SLO Sheet and Error Budget (3 marks)

**Files:** `03-build/reliability/slo-sheet.md` and `03-build/reliability/error-budget.md`

| Mark | Descriptor |
|------|-----------|
| 3 | At least two SLIs defined with exact measurement formula and measurement location. SLO targets set with time window. Each SLO is plausibly achievable given the stated infrastructure. Error budget calculated with arithmetic shown for each SLO. Error budget exhaustion policy stated (no new deployments, reliability sprint, mandatory review). Severity definitions (SEV1, SEV2, SEV3) are calibrated to the specific product and its actual user impact. |
| 2 | Two SLIs defined but one measurement method is vague or the measurement location is unspecified. SLO targets present. Error budget calculated but arithmetic not shown. Severity definitions present but generic rather than product-specific. |
| 1 | One SLI defined or both SLIs are present but stated as aspirational rather than measurable. SLO target present but no error budget calculation. Severity definitions missing or copied from lecture slides without adaptation. |
| 0 | Not submitted, empty files, or SLO set at 100% for all metrics. |

**Specificity check:** The instructor will ask each team to state their availability SLO target, the error budget in minutes over 30 days, and what their SEV1 definition is. Arithmetic must be on the page, not performed on the spot.

---

## Participation (assessed at four checkpoints)

The instructor circulates at 0:20, 0:50, 1:20, and 1:50. At each checkpoint, the instructor checks that the team's work is visible in their GitHub repo (or clearly in progress in their editor with commits imminent).

Participation is not a separate mark but informs the specificity assessment. A team that produces all four documents in the last ten minutes of the session will have documents that lack specificity. The instructor can see the commit timestamps.

---

## Late Submission Policy

Lab deliverables committed after the session ends but before 23:59 the same day: full marks available.

Deliverables committed after 23:59: minus 10% per 24 hours, consistent with the course late policy.

After 72 hours: instructor approval required before submission is accepted.

---

## Academic Integrity

Every document must describe your actual product. Copying a privacy notice from another team, from a generator, or from a real company's published notice is academic misconduct under KIU policy. The instructor checks all privacy notices against the known set of third-party tools used by each team. Notices that name processors your product does not use, or that omit processors your product does use, will be flagged for review.
