# Lab 10 Grading Rubric

**Course:** CS-PD-2026 Product Development for Software Engineers
**Lab:** Lab 10 -- Growth Modeling
**Total points:** 4 (rolls into weekly Participation/Labwork allocation)

This lab is graded across four deliverables. Each deliverable scores 0, 0.5, or 1 point. The lab also feeds directly into the Combined Checkpoint 2+3, where the same artefacts are graded again with higher stakes.

---

## Deliverable 1 -- Growth Strategy Document (1 pt)

**File:** `04-gtm/growth-strategy.md`

| Score | Criteria |
|-------|----------|
| 1.0 | Three channels named with type classification. Each channel has a written justification covering fit, speed, and cost. One rejected channel documented with rationale. |
| 0.5 | Channels named but classification missing or shallow. Justification thin (one sentence per channel). Rejected channel missing. |
| 0.0 | Document missing, fewer than three channels, or no rationale provided. |

**Excellent example signals:**
- Channel ranking explicitly justified (why is channel 1 ranked above channel 2?).
- Audience analysis present (where does the target user actually spend time?).
- Acknowledgement of when each channel is wrong (e.g., "we are not picking paid because we have $0 budget for ads in Sprint 2").

**Failure signals:**
- Channels picked without naming the audience.
- All three channels of the same type.
- Generic justifications that could apply to any product.

---

## Deliverable 2 -- Unit Economics Analysis (1 pt)

**File:** `04-gtm/financials/unit-economics.md`

| Score | Criteria |
|-------|----------|
| 1.0 | CAC per channel with calculation shown. LTV with assumptions on ARPU, gross margin, and retention. LTV:CAC ratio per channel and blended. Payback period calculated. Every assumption sourced. |
| 0.5 | Most numbers present but one or more assumptions unsourced. Math may have minor errors. Payback period missing. |
| 0.0 | No CAC or LTV calculation, or numbers fabricated without any reasoning. |

**Excellent example signals:**
- Sources cited inline (link to industry benchmark or pointer to own dashboard).
- Honest acknowledgement of uncertainty ("we use 1.8% as a placeholder until we have 2,000+ visitors").
- LTV:CAC ratio interpreted in context, not just stated.

**Failure signals:**
- "We think CAC is around $20" with no calculation.
- Industry benchmark quoted as the team's own number.
- LTV:CAC ratio calculated but not interpreted.

---

## Deliverable 3 -- Six-Month Growth Projection (1 pt)

**File:** `04-gtm/financials/growth-projection.xlsx`

| Score | Criteria |
|-------|----------|
| 1.0 | Six months filled in for all three channels. Three scenarios (best, expected, worst) with a toggle. Conversion rates as formulas. Chart of cumulative users. No errors on submission. |
| 0.5 | Expected case filled in but best and worst cases missing. Some hardcoded numbers. Chart missing or one of the columns missing. |
| 0.0 | Spreadsheet missing, or contains errors throughout, or has only one channel modelled. |

**Excellent example signals:**
- Formulas use named ranges for clarity.
- Inputs tab, calculations tab, and output tab separated.
- Stress test documented in a comment cell ("if conversion halves, cumulative users at month 6 falls from 180 to 95").
- Realistic numbers, not hockey-stick fantasy.

**Failure signals:**
- All numbers hardcoded.
- One scenario only.
- #REF! or #DIV/0! errors anywhere.
- Expected case shows 100x growth in six months with no mechanism named.

---

## Deliverable 4 -- Loops and Moats Narrative (1 pt)

**File:** `04-gtm/loops-and-moats.md`

| Score | Criteria |
|-------|----------|
| 1.0 | Loop analysis with K-factor estimate (math shown) or honest "no loop yet". Network effect type identified with threshold. Defensibility assessment. Riskiest assumption named. |
| 0.5 | Some sections present but shallow. K-factor stated without math. Defensibility section missing. |
| 0.0 | Document missing or fewer than two of the four sections present. |

**Excellent example signals:**
- Loop diagrammed in Mermaid or ASCII art.
- K-factor honest ("we estimate K = 0.2 because most users do not invite, but 1 in 5 do because the product gets better with two users").
- Network effect threshold concrete ("network effects kick in once we have 50 active users in a single university").
- Defensibility argument grounded ("not much yet; our moat will be data once we have 6 months of usage").

**Failure signals:**
- "Yes we have a viral loop" with no description.
- K = 1.5 claimed without any math.
- Network effects claimed for a product that has no inter-user interaction.
- Defensibility section answered with "our team is great".

---

## Late Policy

- Submitted by the next Sunday 23:59: full marks possible.
- One resubmission allowed within one week for up to 80% of lost marks per the syllabus.
- Beyond that: instructor approval required.

---

## How This Connects to Combined Checkpoint 2+3

The four artefacts produced in this lab map directly to Combined CP 2+3 sections:

| Lab 10 deliverable | CP 2+3 section | CP 2+3 weight |
|---|---|---|
| Growth strategy | Unit economics and growth model | Part of 3 pts |
| Unit economics | Unit economics and growth model | Part of 3 pts |
| Growth projection (6-month) | Unit economics and growth model | Part of 3 pts |
| Loops and moats | Unit economics and growth model | Part of 3 pts |

In addition, the **twelve-month financial model** (`04-gtm/financials/12-month-model.xlsx`) is required for CP 2+3 but is **not** produced in this lab. Build it during the week of 12 to 19 May using the six-month projection as the foundation and extending to twelve months. Lab 12 also touches the financial model.

A team that earns 4/4 on Lab 10 has banked roughly 80% of the financial half of the CP 2+3 work. A team that scores 2/4 has visible debt going into the checkpoint deadline.

---

## Grading Process

1. TA reviews each team's repository at end of session.
2. TA fills the rubric scoring sheet (see `instructor-facilitation-guide.md`).
3. Marks posted in LMS within 7 days.
4. Detailed feedback in the Pull Request comments where applicable.

---

## Common Final Score Distribution (Reference, Past Cohorts)

This is rough guidance for what marks tend to look like. It is not a curve; every team can earn full marks if every team meets the criteria.

| Score | Approximate share of teams |
|-------|----------------------------|
| 4.0 | 15-25% |
| 3.5 | 30-40% |
| 3.0 | 25-30% |
| 2.0 to 2.5 | 10-20% |
| Below 2.0 | 5-10% |

Teams scoring below 2.0 should book office hours within the week.

---

**Rubric Author:** Zeshan Ahmad
**Last Updated:** 5 May 2026
