# Lab 7: Technical Architecture and Live Experiment Setup

**Course:** CS-PD-2026 | Product Development for Software Engineers  
**Instructor:** Zeshan Ahmad | zeshan.ahmad@kiu.edu.ge  
**Group A:** Thursday 23 April 2026 | 14:00 to 16:00  
**Group B:** Friday 24 April 2026 | 13:00 to 15:00  
**Submission Mode:** Commit before leaving the lab. Sprint 1 starts immediately after the session.

---

## What This Lab Is About

Lab 6 answered product questions. Lab 7 answers implementation questions.

By the end of this session, your team should know exactly what system you are building, what technology sits in each layer, where your AI tools enter the workflow, what technical risks could slow Sprint 1, and what live experiment you are running while the sprint is in motion.

This is a production lab. Do not spend two hours debating hypothetical future features. Focus on the smallest working system that supports your Sprint 1 goal and the single experiment that tests your riskiest assumption.

---

## What You Should Have Coming In

Before Lab 7 starts, your team should already have:

- [ ] Product roadmap from Lab 6 committed
- [ ] Sprint 1 plan with user stories and acceptance criteria committed
- [ ] Process map and Definition of Done committed
- [ ] Updated team roles, including Product Owner and Sprint 1 Scrum Master
- [ ] Event schema draft from earlier work
- [ ] High fidelity or testable prototype link
- [ ] Clear understanding of your activation moment

If one or more of these are missing, fix them first. Architecture without a clear product target becomes guesswork.

---

## Learning Objectives

By the end of this lab, your team will:

1. Produce a system design document for the core Sprint 1 flow
2. Choose a tech stack with written justification and rejected alternatives
3. Create an architecture diagram that matches the written design
4. Identify top technical risks and define spikes or mitigations
5. Write one experiment plan with a numeric success threshold and a numeric failure threshold
6. Launch the experiment before the lab ends, or get as close to live as the instructor approves
7. Prepare Sprint 1 to run through midterm week without confusion about ownership or tooling

---

## Required Repo Outputs

Commit these files to your capstone repository during the lab:

- `03-build/architecture/system-design.md`
- `03-build/architecture/tech-stack.md`
- `03-build/architecture/architecture-diagram.png`
- `03-build/architecture/risk-register.md`
- `03-build/experiments/experiment-plan.md`

Optional, but recommended:

- `03-build/architecture/architecture-diagram-source.md`
- `docs/ai-usage-log.md` update if AI output was used during the session

---

## Lab Timeline, 120 Minutes

| Time | Activity | Output |
|------|----------|--------|
| 0:00 to 0:10 | Part 1: Architecture boundary | Core request and Sprint 1 boundary agreed |
| 0:10 to 0:40 | Part 2: System design document | Components, request lifecycle, data flow documented |
| 0:40 to 1:00 | Part 3: Tech stack selection | Chosen stack and rejected alternatives documented |
| 1:00 to 1:20 | Part 4: Diagram and risk register | Visual architecture and top risks drafted |
| 1:20 to 1:50 | Part 5: Experiment plan | Hypothesis, method, thresholds, sample, channel documented |
| 1:50 to 2:00 | Part 6: Launch and commit | Experiment live or queued, files committed |

---

## Part 1: Architecture Boundary

Start with one sentence:

**What is the single core user request Sprint 1 must support end to end?**

Example:

> A student signs up, searches for a study space, books a slot, and receives confirmation.

If your architecture does not clearly support a single core request, the design is too wide.

Write down:

- What the user does first
- What the system must do in response
- What data must be stored
- What event must be logged
- What is explicitly out of Sprint 1

---

## Part 2: System Design Document

Your system design document must explain the build in plain language.

At minimum, include:

- Frontend, backend, database, auth, analytics, and external APIs
- Clear responsibilities for each component
- The request lifecycle from browser to database and back
- Where AI tools help the team build, and where AI sits in the product, if relevant
- Any dependency that would block Sprint 1 if delayed

Use the template in `templates/system-design-template.md`.

---

## Part 3: Tech Stack Selection

A stack list is not enough. Each choice needs a reason.

For every major layer, write:

- What you selected
- Why it fits your product and team
- What alternative you considered
- Why you rejected the alternative
- Who owns setup and maintenance

Also specify:

- Hosting target
- Database and auth choice
- Analytics platform
- AI tools approved for team use in Sprint 1
- Any tool you are explicitly not using yet

Use the template in `templates/tech-stack-template.md`.

---

## Part 4: Architecture Diagram and Risk Register

Your diagram should match the written design. No orphan boxes. No unlabeled arrows.

The diagram must show:

- User and client entry point
- Frontend layer
- Backend or server layer
- Database or state layer
- Auth
- Analytics events
- External services or APIs
- AI touchpoints, if they exist in the product or team workflow

At the same time, document the top technical risks.

Good technical risk examples:

- Real time availability data may not exist yet
- Search performance may collapse once filters are combined
- Auth flow may add too much friction to first time activation

Weak technical risk examples:

- We might run out of time
- Team communication could be hard

Time and communication matter, but those are project management issues. The risk register in this lab is about system risk.

---

## Part 5: Experiment Plan

Your experiment should test the riskiest assumption, not the easiest thing to launch.

Every valid experiment plan includes:

- A full hypothesis sentence
- The specific assumption being tested
- The experiment method, such as smoke test, Wizard of Oz, concierge MVP, or prototype test
- A numeric success threshold set before launch
- A numeric failure threshold set before launch
- A time window and sample size target
- The channel you will use to get real users
- A clear rule for what decision follows the result

Do not run the experiment on teammates. Do not change the threshold after seeing results.

Use `templates/experiment-plan-template.md` and the guide in `guides/experiment-design-guide.md`.

---

## Definition of Done for Lab 7

Lab 7 is Done when all of the following are true:

- [ ] System design document committed
- [ ] Tech stack document committed
- [ ] Architecture diagram exported and committed
- [ ] Risk register committed
- [ ] Experiment plan committed
- [ ] Product Owner and Sprint 1 Scrum Master can both explain the design
- [ ] One experiment asset is live, queued, or sent for review with instructor approval
- [ ] Team knows what coding starts first after the lab

---

## Common Failure Patterns

### 1. Diagram with boxes but no logic
If the arrows do not tell a story, the diagram is decoration, not architecture.

### 2. Tech stack with no tradeoffs
If every row says "easy" or "popular," the team has not made a real decision.

### 3. Hypothesis with no number
"Users will like this" is not testable.

### 4. Experiment on friends who already know the product
That gives politeness, not signal.

### 5. Sprint 1 architecture that includes future features
If the feature is not needed for the core request, move it out.

### 6. AI tools named but not governed
If a story uses AI, say which tool, why that tool, and how output gets reviewed.

---

## Commit Format

Recommended commit message:

```text
[LAB-7] architecture package and experiment plan
```

Recommended tag:

```text
lab-7-submission
```

---

## Final Instruction

Leave the lab with a buildable architecture, a live learning loop, and zero confusion about what Sprint 1 starts with.
