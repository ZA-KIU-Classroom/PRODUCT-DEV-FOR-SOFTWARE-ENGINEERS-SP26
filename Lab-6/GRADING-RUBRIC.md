# Lab 6 Grading Rubric

**Course:** CS-PD-2026 | Spring 2026  
**Instructor:** Zeshan Ahmad  
**Deadline:** Wednesday 22 April 2026 at 23:59

---

## Overview

Lab 6 deliverables are assessed as part of Checkpoint 2 (10 points total, due Wednesday 22 April at 23:59) and the Lab 6 participation grade. In-lab participation points are awarded based on output quality observed during the session. Deliverable quality is assessed after the deadline against submitted files.

---

## Participation (In-Lab, Observed by Instructor)

Instructor circulates and checks progress at 0:15, 0:45, 1:15, and 1:50.

| Checkpoint | What Is Checked | Full Credit | Partial Credit | No Credit |
|------------|----------------|-------------|---------------|-----------|
| 0:15 | MVP scope defined | In-scope list, out-of-scope list, and rejected features all documented. PO can explain every decision. | Scope partially defined. Team cannot explain one or more rejection decisions. | Not started or no distinction between in-scope and out-of-scope. |
| 0:45 | User stories drafted | 8 or more stories written with story points. Each story traces to an interview. INVEST criteria applied. | 5 to 7 stories. Some missing interview citations or story points. | Fewer than 5 stories or no evidence of INVEST criteria. |
| 1:15 | Roadmap and Sprint 1 plan in progress | Roadmap has all 4 sprints with goals and story allocations. Sprint 1 stories have AC drafted. | Roadmap has 2 to 3 sprints completed. Sprint 1 AC missing on some stories. | Roadmap not started or Sprint 1 has no AC. |
| 1:50 | GitHub commit | All four required files committed with correct paths and correct commit message. Tag pushed. | Files committed but wrong paths or missing one file. | Nothing committed. |

---

## Deliverable Quality (Assessed After Deadline)

### Product Roadmap (35% of Lab 6 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| MVP scope | Clear in-scope and out-of-scope boundary. Rejected features listed with reasons. | Scope defined but no rejected features documented or reasons missing. | No scope boundary. Everything is "in scope". |
| Sprint structure | All four sprints have a goal, a user-facing capability statement, and a realistic story allocation. | Two to three sprints have goals. One or more sprints are just a task list. | Single sprint or no sprint structure. |
| Capacity calculation | Each sprint shows committed points versus theoretical capacity. Commitment is 60% or below of maximum. | Capacity mentioned but not calculated. Commitment appears unrealistic. | No capacity calculation. Sprints are over-committed. |
| Risk identification | Each sprint has at least one identified risk with a mitigation approach. | Risks identified but no mitigations. | No risks documented. |
| Checkpoint alignment | Checkpoint 2 (April 22), Midterm (April 30), and Checkpoint 3 (May 21) are correctly referenced in the roadmap timeline. | One or two checkpoints referenced. | No checkpoint alignment. |

### Sprint 1 Plan (40% of Lab 6 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| User story format | Every story follows As a / I want / So that format. The So that clause is present and meaningful. | Most stories correct. 1 to 2 missing So that clauses. | Stories are task descriptions, not user stories. |
| INVEST compliance | Every story passes all six INVEST criteria. Stories are independent, estimable, and small enough to finish in one sprint. | Most stories pass INVEST. 1 to 2 are too large or not independently deliverable. | Stories regularly fail INVEST. Multiple stories over 8 points with no plan to split. |
| Interview evidence | Every story cites the interview or interviews that support the need for this feature. | Most stories cited. 2 to 3 missing citations. | No interview citations. Stories appear invented without discovery evidence. |
| Story points | Fibonacci scale used throughout. Team calibration anchors documented. AI review time included in estimates. | Fibonacci scale used but no calibration anchors. Estimates may undercount review time. | Not using Fibonacci scale or no estimates present. |
| Acceptance criteria | Every Sprint 1 story has at least 2 AC in Given-When-Then format. Each AC is falsifiable. | Most stories have AC. 1 to 2 stories missing AC or AC not falsifiable. | No acceptance criteria or free-text criteria that cannot be tested. |
| AI tool assignment | Every Sprint 1 story has an AI tool noted with a brief rationale for the choice. | Most stories have tool assignments. Some missing or unspecific (just says "AI"). | No AI tool assignments in Sprint 1 plan. |
| Role assignments | Sprint 1 PO and SM named. Standup cadence documented. Sprint Review date noted. | Roles assigned but cadence not specified. | No role assignments. |

### Process Map (15% of Lab 6 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Definition of Done | DoD is explicit and includes: human code review, AC confirmed by PO, AI-generated code annotated, usage logged, feature works in deployed environment. | DoD present but missing 1 to 2 required elements. | No DoD or it is too vague to enforce. |
| AI review process | Document describes specifically who reviews AI-generated output, when, and what the review covers. | AI review mentioned but not specific about who or when. | No AI review process documented. |
| Workflow coverage | Document covers: story lifecycle (backlog to done), branching and PR process, blocker communication, standup format and location. | Two to three workflow elements covered. One missing. | Single workflow element or none. |
| Specificity | A new team member could follow this document without asking anyone questions. | Some steps are clear but others are vague or assumed. | Document is too high-level to be actionable. |

### GitHub Commit Quality (10% of Lab 6 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| File paths | All four required files at exact correct paths. | 1 file at wrong path or in wrong folder. | 2 or more files missing or at wrong paths. |
| Commit message | Follows format: `[LAB-6] description`. | Descriptive but wrong format. | Generic or no meaningful message. |
| Submission tag | `lab-6-submission` tag pushed to remote. | Tag created but not pushed. | No tag. |

---

## Late Submission Policy

The Lab 6 deadline is Wednesday 22 April at 23:59. This is also the Checkpoint 2 deadline.

One resubmission is permitted within one week of the deadline (by Wednesday 29 April at 23:59) for up to 80% of lost marks. After that window closes, the marks are gone.

**Note:** A late Lab 6 submission also means a late Checkpoint 2 submission. Both penalties apply independently.

---

## What Instructors Are Looking For

The most common failures in Lab 6 are:

**Scope failures:**
- No out-of-scope list. Teams that say "everything is in scope" have not defined an MVP. They have defined a product fantasy.
- No explanation for rejected features. A good PM can explain what they said no to and why.

**User story failures:**
- Missing the So that clause. Teams write "As a user I want to log in." That is a task, not a story.
- No interview evidence cited. If a story has no interview behind it, the feature was invented, not discovered.
- Stories that are too large to complete in one sprint. An 8-point story with no plan to split will carry over and damage velocity.

**Sprint plan failures:**
- AC written as feature descriptions instead of testable conditions. "The login page should look good" is not an AC.
- No AI tool assignments. Teams arrive at Lab 8 not knowing which tool to use and waste the first hour of Sprint 1.
- Over-committed Sprint 1. Teams that commit 25 points in Sprint 1 without velocity data are guessing. They will miss. Take 60% of max capacity.

**Process map failures:**
- No Definition of Done. Without a shared DoD, one developer considers a story done when it compiles. Another considers it done when it is deployed. This disagreement surfaces at Sprint Review.
- No AI review process. Teams using AI tools without a defined review step will ship bugs that a 5-minute review would have caught.

---

*Lab 6 Rubric | CS-PD-2026 | Spring 2026 | Kutaisi International University*
