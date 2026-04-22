# Lab 7 Quickstart

Use this file the moment the lab begins.

---

## 1. Open or Create the Required Paths

```text
03-build/architecture/system-design.md
03-build/architecture/tech-stack.md
03-build/architecture/architecture-diagram.png
03-build/architecture/risk-register.md
03-build/experiments/experiment-plan.md
```

If the folders do not exist yet:

```bash
mkdir -p 03-build/architecture
mkdir -p 03-build/experiments
```

---

## 2. Assign Owners in the First 3 Minutes

- Product Owner: final approval on system scope and experiment logic
- Scrum Master: keeps time, enforces decisions, checks that files are committed
- Developer 1: leads system design draft
- Developer 2: leads tech stack and risk register
- Developer 3 or shared role: leads diagram and experiment setup

If your team has four members, split the experiment setup from the diagram work.

---

## 3. Decide the Core Sprint 1 Request

Write one sentence and pin it in your team chat or on the board.

**Format:**

```text
A [target user] does [core action] and receives [observable result].
```

Do not move into architecture until this sentence is agreed.

---

## 4. Build in This Order

1. `system-design.md`
2. `tech-stack.md`
3. `risk-register.md`
4. `architecture-diagram.png`
5. `experiment-plan.md`

This order matters. The diagram should come from the written system, not the reverse.

---

## 5. Minimum Output Standard

### `system-design.md`
Must include:
- component table
- request lifecycle
- data flow
- Sprint 1 boundary
- AI touchpoints

### `tech-stack.md`
Must include:
- chosen tool per layer
- why chosen
- rejected alternative
- deployment target
- approved AI tools

### `risk-register.md`
Must include:
- top 3 technical risks
- likelihood
- impact
- mitigation or spike
- owner

### `architecture-diagram.png`
Must show:
- user
- frontend
- backend
- database
- auth
- analytics
- external services
- arrows with labels

### `experiment-plan.md`
Must include:
- full hypothesis
- assumption being tested
- method
- success threshold
- failure threshold
- time window
- sample size
- launch channel

---

## 6. Experiment Rule

Before the lab ends, one of these must be true:

- landing page published
- form published
- ad or post scheduled
- outreach message sent to real users
- prototype test sessions booked with real target users

If none of these happened, the experiment is not live enough.

---

## 7. Final 10 Minute Check

Before commit, ask another team member:

- Does the diagram match the document?
- Does the stack document explain tradeoffs?
- Does the risk register list system risks, not vague worries?
- Does the experiment have a number?
- Does everyone know what coding starts first?

---

## 8. Commit

Recommended commit message:

```text
[LAB-7] architecture package and experiment plan
```

Recommended tag:

```text
lab-7-submission
```

---

## 9. If You Finish Early

- improve diagram clarity
- tighten the request lifecycle
- remove any stack choice marked TBD
- strengthen the experiment threshold logic
- update `docs/ai-usage-log.md`
