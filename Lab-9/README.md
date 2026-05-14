# Lab 9: Growth Modeling

**Course:** CS-PD-2026 | Product Development for Software Engineers
**Instructor:** Zeshan Ahmad
**Session:** Week 10 lab slot | Group A: Thursday 14 May 2026 at 14:00 | Group B: Friday 15 May 2026 at 13:00
**Location:** In person, standard lab room
**Duration:** 120 minutes
**Repo folder:** `Lab-9/` in the classroom organisation

---

## Overview

You have a product. You have users. Now you need to explain, in numbers, how those users grow.

Lab 9 is a quantitative lab. You will build four documents that, together, form the go-to-market foundation of your Combined Checkpoint 2+3 submission. Every assumption you write down must have a source: a benchmark you can cite, a number from your own dashboard, or a clearly labelled estimate you will replace with real data.

This lab connects directly to the Week 10 lecture on Growth Strategy and Scaling. If you did not attend or have not reviewed it, read your notes before arriving. The channel categories, CAC and LTV formulas, K-factor mechanics, and network effects taxonomy from that lecture are the conceptual input for every activity today.

---

## What You Will Build

| File | Location in your team repo | Points |
|------|---------------------------|--------|
| Growth Strategy Document | `04-gtm/growth-strategy.md` | 4 |
| Unit Economics Analysis | `04-gtm/financials/unit-economics.md` | 3 |
| Six-Month Growth Projection | `04-gtm/growth-projection.xlsx` | 4 |
| Loop and Moat Narrative | `04-gtm/loops-and-moats.md` | 3 |
| **Total** | | **14** |

Participation is assessed on in-lab progress at the 0:30, 1:00, and 1:40 checkpoints. Work must be visible in your repo by the end of the session.

---

## Prerequisites

Before you arrive you must have:

- [ ] Attended or reviewed the Week 10 lecture (Growth Strategy and Scaling)
- [ ] Your live deployment URL accessible and working
- [ ] Your event schema and analytics dashboard open in a browser tab
- [ ] Your experiment results from Sprint 1 (at least partial data, even if Sprint 1 close-out is not yet submitted)
- [ ] Your team's activation metric defined with a specific number and time window
- [ ] Your `04-gtm/` folder created in your repo with the sub-folders listed above

**Folder setup (run this if you have not already):**

```bash
mkdir -p 04-gtm/financials
mkdir -p 04-gtm/traction
touch 04-gtm/growth-strategy.md
touch 04-gtm/financials/unit-economics.md
touch 04-gtm/loops-and-moats.md
```

The `.xlsx` file you will create manually in Google Sheets and export, or build directly in Excel.

---

## Lab Structure

| Time | Part | Activity | Deliverable |
|------|------|----------|-------------|
| 0:00 to 0:10 | Setup | Folder check, data review, activation metric confirmed | Team aligned on numbers entering the lab |
| 0:10 to 0:40 | Part 1 | Growth Strategy Document | `04-gtm/growth-strategy.md` drafted |
| 0:40 to 1:00 | Part 2 | Unit Economics Analysis | `04-gtm/financials/unit-economics.md` drafted |
| 1:00 to 1:30 | Part 3 | Six-Month Growth Projection | `04-gtm/growth-projection.xlsx` built |
| 1:30 to 1:50 | Part 4 | Loop and Moat Narrative | `04-gtm/loops-and-moats.md` drafted |
| 1:50 to 2:00 | Commit | All files committed and pushed | Submission tag applied |

---

## Part 1: Growth Strategy Document (30 minutes)

### Goal

Name your three acquisition channels, justify each one, rank them by priority, and define your activation metric precisely.

### File

`04-gtm/growth-strategy.md`

Use the template at `Lab-9/templates/growth-strategy-template.md`.

### What must be in this document

**Three named acquisition channels**, each with:
- The channel type: paid, organic, viral, or sales
- Why this channel fits your product and your specific audience
- Why you are NOT using the other channel types, or why they are lower priority
- One-sentence priority ranking rationale

**Your activation metric**, stated as:
- A specific user action
- A specific number threshold
- A specific time window

Example from StudySpace Finders: "A student who finds and books a study space within 60 seconds of opening the app for the first time."

**Common mistakes to avoid:**
- Listing all four channel types as your strategy. You have one Sprint 2. Pick two channels at most and go deep on one.
- Writing "social media" as a channel. That is not a channel. Instagram organic content is a channel. Twitter paid ads is a channel. Be specific.
- Defining your activation metric without a number. "User who completes onboarding" is not an activation metric. It is a description.

### Instructor checkpoint at 0:40

The instructor will ask each team: what are your three channels, what type is each, and what is your activation metric stated as a number and time window. Teams who cannot answer these questions without reading from their document need to go back and simplify.

---

## Part 2: Unit Economics Analysis (20 minutes)

### Goal

Calculate CAC and LTV for each of your three channels with the arithmetic shown. Compute the LTV:CAC ratio per channel and blended. Calculate payback period.

### File

`04-gtm/financials/unit-economics.md`

Use the template at `Lab-9/templates/unit-economics-template.md`.

### The formulas

```
CAC = total spend on acquiring users through that channel / number of users acquired

LTV = ARPU x gross margin x average customer lifetime in months

LTV:CAC ratio = LTV / CAC  (target: at least 3:1)

Payback period = CAC / (ARPU x gross margin)  expressed in months
```

For free products where ARPU is zero, substitute monetisable value: ad inventory per user per month, data value, or B2B upsell potential. You must still assign a number and justify it.

### What you must show

For each of your three channels:
- CAC with the calculation written out, not just the result
- Source for each input: "industry benchmark from [source]", "our dashboard shows", or "assumption, will replace with data"
- LTV with assumptions on ARPU, gross margin, and retention explicitly stated
- LTV:CAC ratio
- Payback period in months

Then a blended row across all three channels.

### What kills marks

- Writing a CAC number with no calculation shown
- Using "SaaS averages 2% conversion" as your own conversion number without labelling it as a benchmark
- An LTV:CAC ratio below 1:1 with no acknowledgement of why and what you will do about it
- Ignoring payback period entirely

### Instructor checkpoint at 1:00

Each team must have numbers on the page, even if some are labelled as benchmarks. Empty cells at this checkpoint indicate the team has not attempted the calculation and marks will be reduced.

---

## Part 3: Six-Month Growth Projection (30 minutes)

### Goal

Build a spreadsheet that projects your user growth month by month across your channels for six months, with best, expected, and worst case scenarios.

### File

`04-gtm/growth-projection.xlsx`

Use the worked example at `Lab-9/examples/growth-projection-worked-example.md` as a reference for structure. Build your own numbers, do not copy the example.

### Minimum columns required

Your spreadsheet must contain at minimum:

| Column | Description |
|--------|-------------|
| Month | M1 through M6 |
| Channel | One row per channel per month |
| Spend | Budget allocated to this channel this month |
| Visitors | Estimated visitors from this channel |
| Signups | Visitors x signup conversion rate |
| Activated | Signups x activation rate |
| Retained D30 | Activated x D30 retention rate |
| CAC | Spend / customers acquired |
| LTV | As calculated in unit economics |
| Cumulative users | Running total of retained users |

### The three scenarios

Build three tabs or three clearly labelled sections:
- **Expected case:** Your honest best estimate with defensible assumptions
- **Best case:** If one key variable is 50% better than expected (state which variable)
- **Worst case:** If that same variable is 50% worse than expected

### Inputs you must justify

Every rate you enter must have a source:
- Click-through rate: cite an industry benchmark for your channel
- Visitor-to-signup rate: use your landing page data if you have it, otherwise a benchmark
- Signup-to-activation rate: use your event schema data if firing, otherwise a benchmark
- D30 retention: use your cohort data if you have it, otherwise a benchmark
- Cost per click or per outbound message: use your actual spend or a platform benchmark

### Assumptions that will lose marks

- Conversion rates that are three times higher than benchmarks with no justification
- Retention that holds flat across all six months with no natural decay modelled
- A K-factor pulled from nowhere with no loop described in your product
- Month-over-month growth that doubles every month with no causal mechanism named

### Instructor checkpoint at 1:30

Each team must have a working spreadsheet with M1 and M2 populated and the structure for M3 through M6 in place. Teams who are still on month one at this checkpoint should drop to a single scenario and complete the expected case only.

---

## Part 4: Loop and Moat Narrative (20 minutes)

### Goal

Describe whether your product has a viral loop, estimate its K-factor with the arithmetic, identify which type of network effect you have (if any), and name what protects you against a copycat competitor.

### File

`04-gtm/loops-and-moats.md`

Use the template at `Lab-9/templates/loops-and-moats-template.md`.

### What this document must contain

**Viral loop assessment**
- Does your product have a loop? A loop is a sequence where a user takes an action that ends with another user starting the same sequence. If it does not exist, say so honestly and explain why.
- If a loop exists, diagram it as a simple sequence: User does X, which causes Y, which causes new user to do X.
- Estimated K-factor with the arithmetic shown: K = invitations sent per user x conversion rate of invitations.
- If K is below 1, explain why the loop still matters: it reduces your blended CAC.

**Network effects analysis**
- Which type of network effect does your product have, if any: direct, two-sided, data, or local?
- For local network effects (which most student products have): what is the critical mass threshold for your specific geography or community? For StudySpace Finders, the threshold is the number of KIU students needed on the platform for the app to feel useful to any individual student.
- If your product has no network effects, say so and explain what your moat is instead.

**Moat narrative**
- What protects you at 10 times your current size against a well-funded copycat?
- One honest paragraph. Weak moats (we will be first, our design is better) must be acknowledged as weak. Strong moats (data network effect, switching costs, regulatory approval) must be evidenced.

---

## Committing Your Work

At the end of the session, commit all files with the following convention:

```bash
git add 04-gtm/
git commit -m "[LAB-9] Growth modeling: strategy, unit economics, projection, loops"
git push origin main
git tag lab-9-submission
git push origin lab-9-submission
```

Every team member must have at least one commit in this session. The instructor reviews the commit history. A team where only one person committed all files will have individual participation marks reviewed.

---

## Grading Rubric Summary

| Component | Marks | Key criteria |
|-----------|-------|-------------|
| Growth Strategy Document | 4 | Three named channels with type and justification, activation metric with number and time window, priority ranking with rationale |
| Unit Economics Analysis | 3 | CAC shown with arithmetic, LTV with stated assumptions, LTV:CAC per channel and blended, payback period |
| Six-Month Growth Projection | 4 | All required columns present, inputs sourced or labelled as benchmarks, three scenarios, no unsupported hockey-stick assumptions |
| Loop and Moat Narrative | 3 | Loop present or honestly absent, K-factor with arithmetic, network effect type identified, moat named and assessed honestly |
| **Total** | **14** | |

Full rubric with descriptors at `Lab-9/GRADING-RUBRIC.md`.

---

## Connection to Combined Checkpoint 2+3

The four documents you produce today feed directly into the Combined Checkpoint 2+3 submission due Thursday 21 May at 23:59. Specifically:

- `growth-strategy.md` contributes to the unit economics and growth model criterion (3 pts in the CP rubric)
- `unit-economics.md` is a required component of that same criterion
- `growth-projection.xlsx` is the six-month projection required for the checkpoint
- `loops-and-moats.md` supports the traction evidence criterion and the repo discipline criterion

Do not treat this as a lab that is separate from your checkpoint work. These are the same documents. Finish them to checkpoint standard today and you will not need to rebuild them next week.

---

## Sprint 1 Close-Out Reminder

Sprint 1 close-out is due Wednesday 13 May at 23:59. That is before both lab sessions this week. If your deployment is not live, your event schema is not firing, or your experiment write-up is not committed, that is your priority before this lab and you must communicate the gap to your team immediately.

---

## Resources

- Week 10 lecture slides: on Teams
- Google Sheets: for building the growth projection spreadsheet
- Benchmark sources: a16z SaaS benchmarks, First Round Review growth articles, OpenView SaaS metrics report
- Templates folder: `Lab-9/templates/`
- Worked example: `Lab-9/examples/`
- Office hours: book via email at zeshan.ahmad@kiu.edu.ge

---

## Questions During Lab

Raise your hand. The instructor circulates at the 0:30, 1:00, and 1:30 checkpoints and is available between checkpoints for individual team questions. If you are blocked on a number and genuinely cannot find a benchmark, label the cell "TBD - benchmark needed" and move on. Do not let one missing input stop you from building the rest of the model.
