# Combined Checkpoint 2+3: Design, Architecture, and MVP Build
## Grading Rubric

**Course:** CS-PD-2026 | Product Development for Software Engineers
**Instructor:** Zeshan Ahmad | Kutaisi International University
**Submission deadline:** Thursday 21 May 2026 at 23:59
**Total points:** 20
**Submission type:** Team
**Submission method:** GitHub repository tag `cp2-3-submission` pushed before the deadline

---

## Context and Background

The Combined Checkpoint 2+3 absorbs the scope of two originally separate checkpoints:

- **Original CP2 scope (10 pts):** Design and Architecture -- high-fidelity prototype, event schema plan, technical architecture document, tech stack justification, eight-week product roadmap, Sprint 1 plan, process map.
- **Original CP3 scope (10 pts):** MVP Build -- working deployed product, live analytics dashboard, Sprint 1 experiment results written up, six-month growth projection with unit economics, twelve-month financial model, traction evidence.

The two checkpoints were combined because the original CP2 deadline of 22 April was extended for the cohort, causing CP2 and CP3 work to overlap in time. The total point value (10 + 10 = 20) is preserved. The full scope of both checkpoints is preserved. What changed is the submission moment: one gate, one grading event, Thursday 21 May at 23:59.

---

## How This Rubric Works

Each component has a full descriptor at four levels: Full Credit, Good, Acceptable, and Minimal or Zero. Marks are awarded based on what is actually present and functional in the repository at the time of the submission deadline. Work committed after the tag is applied will not be graded.

The rubric is published to students. There are no hidden criteria.

**Late submission policy:** Minus 10% of the total item score per 24 hours late, for up to 72 hours. After 72 hours, submission requires instructor approval before grading. A 20-point submission that arrives 24 hours late is capped at 18 points before component-level assessment begins.

---

## Component 1: Design and Prototype Quality
### 3 points | Files: `02-design/` in your team repo

This component assesses the quality of the high-fidelity prototype and the rigour of the usability testing that validated it.

### Templates and examples to reference

- **Lab-5:** `templates/event-schema-template.md`, `templates/nsm-template.md` -- for the analytics layer connected to the prototype activation flow
- **Lab-6:** `templates/sprint-plan-template.md`, `examples/example-product-roadmap.md`, `examples/example-sprint-planning.md` -- for sprint planning context around prototype iteration
- **Prototyping tool:** Google Stitch at stitch.withgoogle.com for high-fidelity prototype generation from your interview synthesis

### What must be present

- A high-fidelity prototype accessible via a Stitch link, Figma link, or equivalent, committed to `02-design/prototypes/high-fidelity/figma-link.md` or equivalent file
- Usability testing conducted with at least five real users who are not team members
- A usability findings document at `02-design/user-testing/usability-findings.md` with findings documented per participant, not as a generalised summary
- Evidence that at least one usability finding was acted upon: a design change documented with the specific finding that motivated it

### Mark descriptors

**3 points -- Full Credit**
High-fidelity prototype covers the core user flow end to end and is navigable without explanation. Usability testing was conducted with five or more real users outside the team. Findings document contains specific, attributed observations from each participant (not paraphrased generalisations). At least one design change is documented with a before and after description and the specific finding that motivated it. The prototype reflects the design changes made in response to testing.

**2 points -- Good**
Prototype is high-fidelity and covers the core flow. Usability testing conducted with fewer than five users (minimum three to reach this level), or findings are partially attributed to specific participants. Design changes mentioned but the connection between finding and change is vague.

**1 point -- Acceptable**
Prototype exists and is accessible but is low or medium fidelity, or covers only part of the core flow. Usability testing conducted with one or two users, or findings reported as a generic list without participant attribution. No documented design changes in response to findings.

**0 points**
No prototype link committed, or link is broken at the time of grading. No evidence of any usability testing conducted.

---

## Component 2: Technical Architecture
### 3 points | Files: `03-build/architecture/` in your team repo

This component assesses the completeness and specificity of the system design documentation.

### Templates and examples to reference

- **Lab-7:** `templates/system-design-template.md` -- full system design document template covering architecture pattern, component breakdown, data flow, and hosting decisions
- **Lab-7:** `templates/tech-stack-template.md` -- technology selection template with justification fields per component
- **Lab-7:** `templates/risk-spikes-template.md` -- risk identification and spike planning template
- **Lab-7:** `examples/example-system-design.md` -- StudySpace Finders worked architecture example
- **Lab-7:** `examples/example-tech-stack.md` -- worked tech stack justification with reasoning per choice

### What must be present

- System design document at `03-build/architecture/system-design.md` describing the overall architecture pattern, component breakdown, and data flow
- Tech stack document at `03-build/architecture/tech-stack.md` with every technology choice justified (not just listed)
- Architecture diagram at `03-build/architecture/architecture-diagram.png` or equivalent image format, showing the relationships between components
- AI tool touchpoints annotated: for every component where an AI tool was used, the document notes which tool, what it was used for, and whether the output was accepted, modified, or discarded

### Mark descriptors

**3 points -- Full Credit**
System design document describes the architecture pattern and explains why it fits this product's requirements and team size. Every technology in the tech stack has a written justification referencing specific product requirements, team expertise, or performance needs. Architecture diagram is readable and accurately reflects the actual running system, not a theoretical design. AI tool usage is annotated at the component level with tool name, task, and disposition of output.

**2 points -- Good**
System design document present and covers major components. Tech stack listed with partial justifications -- some choices explained, some not. Architecture diagram present but may not accurately reflect the final system. AI tool annotations present but incomplete.

**1 point -- Acceptable**
System design document is a brief overview with minimal depth. Tech stack is a list with no justifications. Architecture diagram present but generic or copied from a template without customisation. No AI tool annotations.

**0 points**
One or more required files missing from the repository. No architecture diagram. No tech stack document.

---

## Component 3: Working MVP Deployed
### 5 points | Evidence: Live URL committed in your team repo README

This is the highest-weighted component. A working deployment is the non-negotiable core of the checkpoint. All other components support and contextualise this one.

### Templates and examples to reference

- **Lab-6:** `README.md` -- full build and deploy guide covering Google AI Studio Apps integration and Vercel deployment
- **Lab-6:** `QUICKSTART.md` -- step-by-step deployment checklist
- **Lab-7:** `templates/sprint-plan-template.md` -- the Sprint 1 plan from which the MVP features were drawn
- **Lab-8:** `README.md` -- Sprint 1 review guide covering what constitutes a shippable MVP at this stage
- **Lab-8:** `templates/validation-sprint-template.md` -- sprint execution template with daily standup format, success criteria, and definition of done
- **Lab-8:** `examples/` -- worked sprint examples from StudySpace Finders showing what a completed Sprint 1 looks like in a repo

### What must be present

- A live URL committed in your team project README, accessible to anyone without a team account
- A real user (not a team member) must be able to complete the core user flow without assistance from the team
- An analytics dashboard link committed at `03-build/analytics/dashboard-link.md`, showing real event data from real users
- The core flow must fire at least one event schema event visible in the analytics dashboard

### Mark descriptors

**5 points -- Full Credit**
Deployment URL works at the time of grading. A non-team user can complete the core flow independently without guidance. Analytics dashboard shows real data from real user sessions, not test or seeded data. At least one event schema event fires during a real user session and is visible in the dashboard. Deployed version matches the prototype design in all primary screens.

**4 points -- Good**
Deployment URL works. Core flow is completable but one step requires a workaround or has a minor bug. Analytics dashboard is live with real data but event coverage is incomplete (some events fire, not all that were planned). Minor discrepancy between prototype and deployed product.

**3 points -- Acceptable**
Deployment URL works. Core flow is partially functional -- user can start but cannot complete without hitting an error or dead end. Analytics dashboard present but shows only test data or no data. Product is recognisably the product described in the team's design documents.

**2 points -- Minimal**
Deployment URL works but the application is in a very early state -- login page or landing page only, no functional core flow. No analytics dashboard or dashboard shows no data.

**1 point -- Barely present**
A deployment URL exists and resolves to something, but the product is not functional in any meaningful sense.

**0 points**
No deployment URL committed in README, or URL returns a 404 or equivalent error at the time of grading.

---

## Component 4: Experiment Evidence
### 3 points | Files: `03-build/experiments/` in your team repo

This component assesses whether the team designed a real hypothesis, ran a real experiment with real users, and made a documented decision based on the results.

### Templates and examples to reference

- **Lab-7:** `templates/hypothesis-template.md` -- hypothesis formatting guide with the required "We believe / We will know this is true when" structure
- **Lab-7:** `templates/experiment-plan-template.md` -- experiment design template covering method, sample size, success threshold, and data collection plan
- **Lab-8:** `templates/validation-sprint-template.md` -- covers the full two-week experiment execution cycle including daily tracking, data compilation, analysis day, and decision meeting
- **Lab-8:** `README.md` -- pivot or persevere decision framework with the required reasoning format
- **Lab-8:** `examples/example-experiment-results.md` -- StudySpace Finders worked experiment write-up showing the complete hypothesis-to-decision chain with real data format

### What must be present

- Experiment write-up at `03-build/experiments/experiment-results.md` covering hypothesis, method, results, and decision
- Hypothesis in the standard format: "We believe [action] will cause [outcome] for [user segment]. We will know this is true when [measurable signal] reaches [specific threshold]."
- Results including real data from real users, not projected or estimated figures
- A pivot or persevere decision documented with the reasoning and the specific number that drove it

### Mark descriptors

**3 points -- Full Credit**
Hypothesis stated in the correct format with a specific measurable signal and specific threshold. Experiment conducted with real users over a defined time window. Results contain actual data: number of participants, the measured signal, whether the threshold was reached, and the observed value. Pivot or persevere decision documented with the specific number and a clear reasoning chain from number to decision. If inconclusive, the team explains why and what they would change in the next experiment.

**2 points -- Good**
Hypothesis present and mostly well-formed but missing either the specific threshold or the specific measurable signal. Results contain real data but the connection between data and decision is not fully articulated. Decision is present.

**1 point -- Acceptable**
Hypothesis is vague or not in the required format. Results present but thin (fewer than five data points, or data mixed with estimates). Decision mentioned but not justified with data.

**0 points**
No experiment write-up committed, or the write-up contains no real data. No documented decision.

---

## Component 5: Unit Economics and Growth Model
### 3 points | Files: `04-gtm/` in your team repo

This component assesses the quality of the financial model and growth projection built in Lab 9.

### Templates and examples to reference

- **Lab-9:** `templates/growth-strategy-template.md` -- full template for the growth strategy document including channel selection, type classification, justification fields, priority ranking table, and activation metric format
- **Lab-9:** `templates/unit-economics-template.md` -- unit economics template with formula blocks for CAC, LTV, LTV:CAC ratio, and payback period, including the monetisable value substitute section for free products and the assumptions register
- **Lab-9:** `templates/loops-and-moats-template.md` -- viral loop diagram template, K-factor arithmetic block, network effect classification table, critical mass threshold section, and moat narrative format
- **Lab-9:** `examples/growth-modeling-worked-example.md` -- complete StudySpace Finders worked example covering all four documents with real numbers, honest acknowledgement of weak unit economics, and a detailed loop analysis
- **Lab-9:** `examples/growth-projection-worked-example.md` -- spreadsheet structure reference with month-by-month data for M1 through M3, best and worst case comparisons, and a full assumptions tab reference showing exactly how to source and label every input

### What must be present

- Growth strategy document at `04-gtm/growth-strategy.md` with three named acquisition channels, types, justifications, and priority ranking
- Unit economics analysis at `04-gtm/financials/unit-economics.md` with CAC and LTV per channel with arithmetic shown, LTV:CAC ratio, and payback period
- Six-month growth projection at `04-gtm/growth-projection.xlsx` with all required columns and three scenarios
- Twelve-month financial model extending the six-month projection with revenue or monetisable value projections and a cost structure

### Mark descriptors

**3 points -- Full Credit**
All four files present and complete. Unit economics shows CAC and LTV for each acquisition channel with arithmetic visible and inputs sourced. LTV:CAC ratio computed per channel and blended. Six-month projection has all required columns populated for all six months with three scenarios (expected, best, worst) and sourced or labelled inputs. Twelve-month model extends this with revenue or monetisable value projections and a credible cost structure. Assumptions that cannot yet be measured are clearly labelled as benchmarks or estimates with sources cited.

**2 points -- Good**
Unit economics present with arithmetic for at least two channels. Six-month projection structurally complete but some inputs unsourced. Twelve-month model present but thin -- less than a full cost breakdown or revenue projections are generic.

**1 point -- Acceptable**
Unit economics present but numbers only, no arithmetic shown. Six-month projection has fewer than four months populated or only one scenario. No twelve-month model, or twelve-month model is a mechanical extension of the six-month projection with no additional assumptions.

**0 points**
Unit economics file missing or contains only template placeholders with no team-specific numbers. No growth projection spreadsheet committed.

---

## Component 6: Traction Evidence
### 2 points | Files: `04-gtm/traction/` in your team repo

This component assesses whether the team can demonstrate that real people outside the team have engaged with the product in a meaningful way.

### Templates and examples to reference

- **Lab-8:** `templates/validation-sprint-template.md` -- the section on success criteria and data quality standards applies directly to traction evidence; real data requirements described there carry through here
- **Lab-9:** `examples/growth-modeling-worked-example.md` -- the traction section shows how waitlist data, usage growth, and design partner commitments should be documented and formatted for credibility

### What must be present

At least one of the following committed to `04-gtm/traction/`:

- A signed Design Partner MOU or Letter of Intent from a real external user or organisation committing to use or pilot the product
- A waitlist document showing signups with concrete numbers, acquisition source, and date range, committed as a CSV or markdown table (not a screenshot)
- Measurable usage growth from real users evidenced by analytics data showing a positive trend in at least one retention metric over at least two weeks

### Mark descriptors

**2 points -- Full Credit**
At least one form of traction evidence is committed and credible. An MOU or LOI is signed by a real external party and specifies what they are committing to. A waitlist document shows at least 20 signups with sources and dates. Usage growth evidence shows at least two weeks of data with a positive trend in at least one retention metric.

**1 point -- Partial**
Traction evidence present but thin. Fewer than 10 waitlist signups with no source attribution. Usage growth covers fewer than two weeks. An MOU exists but is unsigned or internal to the team.

**0 points**
No traction evidence committed. Or evidence committed is fabricated, untraceable, or contradicts other data in the repository (e.g. a waitlist claiming 50 signups while the analytics dashboard shows 3 unique users).

---

## Component 7: Repo Discipline
### 1 point | Evidence: Commit history, README, `docs/ai-usage-log.md` in your team repo

This component assesses whether the repository reflects a team that has been working consistently and transparently throughout Sprint 1.

### Templates and examples to reference

- **Lab-6:** `templates/sprint-plan-template.md` -- contains the AI usage log entry format under the AI Tool and AI Tool Rationale fields per story; the full log inherits this structure
- **Lab-7:** `templates/sprint-plan-template.md` -- standup format and cadence definition (daily async standup, what I did, what I am doing, any blockers); standup log inherits this format
- **Lab-8:** `templates/validation-sprint-template.md` -- the daily standup schedule and week-by-week commit expectations are defined here; the commit history for Sprint 1 should match the rhythm described in this template
- **Lab-8:** `README.md` -- the Sprint 1 close-out checklist defines exactly what must be in the repo by Wednesday 13 May at 23:59; that checklist is the baseline for this component

### What must be present

- `docs/ai-usage-log.md` updated with an entry for every Sprint 1 AI tool usage in the required format: date, story, tool, task, files changed, disposition (accepted, modified, or discarded), reviewer name
- Commits distributed across the Sprint 1 window (23 April to 13 May), not clustered the night before the deadline
- Standup history visible in GitHub Issues or in a committed `docs/standup-log.md`, covering at least three standups during Sprint 1
- README updated to point to all major deliverables with working links: deployment URL, analytics dashboard, prototype, and key documents

### Mark descriptors

**1 point -- Full Credit**
AI usage log present with entries covering Sprint 1 development. Each entry includes all required fields. Commits are distributed across the Sprint 1 window with meaningful commit messages. Standup history covers at least three standups during Sprint 1. README links to the deployment URL, analytics dashboard, prototype, and key documents.

**0.5 points -- Partial**
AI usage log present but missing entries for some Sprint 1 work. Commit history partially distributed but shows a significant cluster in the last 48 hours. Standup history covers only one or two standups. README has some but not all required links.

**0 points**
No AI usage log committed, or log is empty. All commits within 24 hours of the deadline. No standup history. README not updated since Week 6.

---

## Summary Table

| Component | Points | File location in your team repo |
|-----------|--------|---------------------------------|
| Design and prototype quality | 3 | `02-design/` |
| Technical architecture | 3 | `03-build/architecture/` |
| Working MVP deployed | 5 | Live URL in README |
| Experiment evidence | 3 | `03-build/experiments/` |
| Unit economics and growth model | 3 | `04-gtm/` |
| Traction evidence | 2 | `04-gtm/traction/` |
| Repo discipline | 1 | Commit history, `docs/` |
| **Total** | **20** | |

---

## Lab Materials Reference

The following lab packages in the course repo contain the templates, examples, and guides that produced each component. Open the relevant lab folder, read the README for context, use the templates as your starting point, and calibrate against the examples.

| Lab | What it produced | Key files inside |
|-----|-----------------|-----------------|
| Lab-5 | Analytics plan, NSM, event schema | `templates/event-schema-template.md`, `templates/nsm-template.md` |
| Lab-6 | Prototype iteration, sprint planning, roadmap, deployment | `templates/sprint-plan-template.md`, `examples/example-product-roadmap.md`, `examples/example-sprint-planning.md` |
| Lab-7 | System architecture, tech stack, risk spikes, hypothesis, experiment plan | `templates/system-design-template.md`, `templates/tech-stack-template.md`, `templates/risk-spikes-template.md`, `templates/hypothesis-template.md`, `templates/experiment-plan-template.md`, `examples/example-system-design.md`, `examples/example-tech-stack.md` |
| Lab-8 | Sprint 1 execution, experiment results, pivot or persevere decision, Sprint 1 close-out | `templates/validation-sprint-template.md`, `README.md`, `examples/example-experiment-results.md` |
| Lab-9 | Growth strategy, unit economics, six-month projection, loop and moat narrative | `templates/growth-strategy-template.md`, `templates/unit-economics-template.md`, `templates/loops-and-moats-template.md`, `examples/growth-modeling-worked-example.md`, `examples/growth-projection-worked-example.md` |

---

## What Graders Check First

Grading follows this sequence:

1. Does the deployment URL work? Open it on a device not logged into any team account. Attempt to complete the core flow. If the URL is broken, Component 3 receives 0 points and the grader notes this before moving on.

2. Is the submission tag `cp2-3-submission` present and pushed before 23:59 on 21 May? If not, the late penalty applies before any component is assessed.

3. Is every required file present at the required path? A file at the wrong path is treated as missing for grading purposes.

4. Is the content team-specific? A document that could describe any generic SaaS product receives zero marks on specificity within its component.

---

## What Kills Marks Across All Components

**Fabricated data.** Analytics screenshots that do not match the deployed product's actual usage. Waitlist numbers inconsistent with user counts elsewhere in the repo. Experiment results with suspiciously round numbers and no variance. Graders are trained to look for these and any suspected fabrication is escalated to the instructor.

**Copied templates with placeholders unfilled.** Any file still containing `[Your product name]`, `[Insert here]`, or `[Team Name]` receives zero for that component. The Lab templates are starting points, not deliverables. Every field must be replaced with content specific to your product.

**Generic content that does not describe the actual product.** An architecture diagram showing a generic three-tier web app with no product-specific components. A unit economics document with the same ARPU and gross margin as the Lab-9 worked example without any explanation of why those numbers apply. A growth strategy document listing channels that are obviously mismatched with the product's actual audience.

**One team member who committed everything.** The commit history is reviewed. If 90% or more of commits are from a single team member, the instructor reviews participation logs and lab records and may adjust individual grades within the team grade.

---

## How to Submit

In your team's capstone repository:

```bash
git add .
git commit -m "[CP2-3] Final submission -- all deliverables committed"
git push origin main
git tag cp2-3-submission
git push origin cp2-3-submission
```

The tag must be pushed before Thursday 21 May at 23:59. The grader checks out the repository at the time the tag was created. Any commits made after the tag will not be visible to the grader unless you delete and re-tag before the deadline.

If you need to correct something after tagging but before the deadline:

```bash
git tag -d cp2-3-submission
git push origin :refs/tags/cp2-3-submission
git add .
git commit -m "[CP2-3] Pre-submission correction"
git push origin main
git tag cp2-3-submission
git push origin cp2-3-submission
```

---

## Questions

Send questions about the rubric or submission requirements to zeshan.ahmad@kiu.edu.ge before Tuesday 19 May at 23:59. Questions received after that time cannot be guaranteed a response before the deadline.

Office hours are available by appointment via email.

---

*Combined Checkpoint 2+3 Rubric | CS-PD-2026 | Spring 2026 | Kutaisi International University*
