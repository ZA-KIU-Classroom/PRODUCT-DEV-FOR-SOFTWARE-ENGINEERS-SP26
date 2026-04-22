# Lab 7 Grading Rubric

**Course:** CS-PD-2026 | Spring 2026  
**Instructor:** Zeshan Ahmad  
**Assessment Use:** Weekly labwork evaluation, Sprint 1 readiness check, later reference for build checkpoint review

---

## Overview

Lab 7 is judged on two things:

1. What the team produces during the session
2. Whether the submitted artifacts are strong enough to support Sprint 1 without preventable confusion

This rubric is built for labwork quality and implementation readiness. It is not only a formatting check.

---

## Participation, In Lab, Observed by Instructor

Instructor checks at 0:20, 0:55, 1:25, and 1:55.

| Checkpoint | What Is Checked | Full Credit | Partial Credit | No Credit |
|------------|----------------|-------------|---------------|-----------|
| 0:20 | Core request and architecture boundary | Team can state the single Sprint 1 request, what is in scope, and what is out. | Scope partly clear, but boundary still fuzzy. | Team still discussing broad product vision with no concrete Sprint 1 request. |
| 0:55 | System design and stack draft | Components, data flow, and stack decisions are written. Alternatives are being discussed seriously. | System draft exists, but stack rationale is thin or incomplete. | Little or no written design progress. |
| 1:25 | Diagram and risk register | Diagram has labeled arrows. Top risks are technical and specific. | Diagram exists but is vague, or risks are generic. | No usable diagram or risk work. |
| 1:55 | Experiment and commit readiness | Hypothesis has numbers. Launch path exists. Files are nearly ready to commit. | Experiment exists but has no real launch path or weak thresholds. | No real experiment plan or no evidence of commit preparation. |

---

## Deliverable Quality, Assessed After the Lab

### System Design Document, 25%

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Component clarity | Every major component has a clear responsibility. | Most components clear, but one or two remain vague. | Components listed with no real explanation. |
| Request lifecycle | End to end user request path is described clearly from browser to storage and back. | Lifecycle present but skips key steps. | No usable request lifecycle. |
| Sprint 1 boundary | Document clearly states what is in Sprint 1 and what is deferred. | Boundary partly stated. | No boundary. Future work mixed into Sprint 1. |
| AI touchpoints | AI use in the team or product is annotated and governed. | AI mentioned but not governed. | AI omitted even though team depends on it. |
| Build readiness | A developer could start implementation from this document. | Document is partly actionable. | Document is too abstract to guide a build. |

### Tech Stack Selection, 20%

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Selection by layer | Frontend, backend, data, auth, analytics, hosting, and key tooling are all covered. | Most layers covered. One or two missing. | Stack is fragmentary. |
| Written justification | Every selected technology has a concrete reason tied to product or team fit. | Some rows justified, some generic. | Mostly unexplained choices. |
| Alternatives rejected | Major alternatives considered and rejected with reasons. | Alternatives mentioned but reasons thin. | No alternatives discussed. |
| No TBD entries | The stack is ready for Sprint 1 execution. | One or two choices still undecided. | Multiple TBDs remain. |

### Architecture Diagram, 20%

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Coverage | Diagram includes user, client, server, data, auth, analytics, and external services as needed. | Most pieces present. Some missing. | Diagram incomplete. |
| Arrow logic | Arrows are labeled and show how data or actions move. | Arrows present but unclear. | Diagram is mostly floating boxes. |
| Alignment with document | Diagram matches the written system design. | Minor mismatch. | Major mismatch between diagram and document. |
| Readability | Another team could understand the system from the diagram alone. | Mostly readable. | Cluttered or ambiguous. |

### Risk Register, 10%

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Technical specificity | Risks are concrete system risks, not vague project worries. | Mixed quality. | Risks are generic. |
| Mitigation quality | Each risk has a mitigation, spike, or fallback. | Some mitigations weak. | No mitigation logic. |
| Ownership | Every major risk has an owner. | Some ownership gaps. | No ownership. |

### Experiment Plan, 20%

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Hypothesis quality | Hypothesis is specific, measurable, and tied to one assumption. | Hypothesis partly specific. | Hypothesis is a preference statement. |
| Thresholds | Success and failure thresholds are numeric and defined before launch. | One threshold weak or missing. | No usable thresholds. |
| Method fit | Chosen method is the cheapest credible test for the assumption. | Method reasonable but not sharp. | Method does not test the stated assumption. |
| Launch realism | Team has a real path to putting the test in front of target users. | Launch path weak. | No real users or no launch path. |

### Git and Submission Quality, 5%

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Correct paths | Required files exist in correct folders. | One file misplaced. | Multiple missing or misplaced. |
| Commit quality | Commit message is descriptive and meaningful. | Commit exists but naming weak. | No meaningful commit. |
| Version hygiene | Files are readable, named clearly, and free of placeholder junk. | Minor cleanup issues. | Obvious placeholders or unfinished junk remain. |

---

## What Strong Work Looks Like

Strong Lab 7 work has these traits:

- one clear Sprint 1 request
- architecture and diagram say the same thing
- no major stack choice left undecided
- risk register surfaces what could really break the sprint
- experiment has numbers and a real distribution channel
- AI usage is governed, not casual

---

## Common Failure Modes

- architecture document becomes a product essay
- diagram has no labeled arrows
- stack document says tools are chosen because they are "easy"
- risk register lists only schedule worries
- experiment uses teammates as target users
- success threshold gets rewritten after results appear

---

*Lab 7 Rubric | CS-PD-2026 | Spring 2026 | Kutaisi International University*
