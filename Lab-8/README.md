# Lab 10 -- Growth Modeling

**Course:** CS-PD-2026 Product Development for Software Engineers
**Cohort:** Spring 2026
**Lab Week:** Week 10
**Lecture Reference:** Week 10 -- Growth Strategy and Scaling

---

## Session Information

| Group | Day | Date | Time | Location |
|-------|-----|------|------|----------|
| Group A | Thursday | 7 May 2026 | 14:00 to 16:00 
| Group B | Friday | 8 May 2026 | 16:00 to 18:00 

The Week 10 lecture earlier in the day is delivered via Google Meet (instructor abroad)
---

## What You Are Building

Four deliverables that together form your team's growth strategy package. Every artefact lives in your team repo under `04-gtm/` and feeds directly into the Combined Checkpoint 2+3 due Thursday 21 May.

| Deliverable | File | Purpose |
|-------------|------|---------|
| Growth Strategy Document | `04-gtm/growth-strategy.md` | Three named acquisition channels with type, ranking, and rationale |
| Unit Economics Analysis | `04-gtm/financials/unit-economics.md` | CAC and LTV per channel, blended ratio, payback period |
| Six-Month Growth Projection | `04-gtm/financials/growth-projection.xlsx` | Monthly cohort spreadsheet with three scenarios |
| Loops and Moats Narrative | `04-gtm/loops-and-moats.md` | K-factor estimate, network effects analysis, defensibility |

Templates for each are in this lab folder under `templates/`. A complete worked example using StudySpace Finders is under `worked-example/`.

---

## Why This Lab Matters

Up to this point, the course has been about product discovery and product build. Lab 10 is the first lab where the question is not "is the product right" but "where do the users come from, and at what cost".

This is the lab that separates teams who will pitch confidently at Demo Day from teams who will pitch a product with no plan to acquire users. Investors do not invest in products. They invest in companies, and a company is a product plus a working acquisition mechanism. That mechanism is what you model here.

---

## Pre-Lab Checklist

Complete these before walking into the lab, or you will spend the first hour catching up while your teammates work:

- Have your activation metric defined (the aha moment with a specific number).
- Have your event schema instrumented and at least one event firing in production.
- Have your live experiment from the 23 April to 7 May window with at least preliminary numbers (visitors, signups, conversion rate).
- Have at least three candidate acquisition channels in mind, even rough ones.
- Have one team member with a laptop ready to build a spreadsheet (Google Sheets or Excel).

---

## Session Structure (2 hours)

| Time | Block | What you do |
|------|-------|-------------|
| 0:00 to 0:15 | Welcome, instructor Q&A via Meet | Live questions from the lecture, clarification on Lab 10 scope |
| 0:15 to 0:45 | Activity 1 -- Channel Selection | Team picks three channels with written rationale |
| 0:45 to 1:15 | Activity 2 -- CAC and LTV per Channel | Team calculates unit economics with sources for every assumption |
| 1:15 to 1:45 | Activity 3 -- Six-Month Spreadsheet | Team builds growth projection with three scenarios |
| 1:45 to 2:00 | Activity 4 -- Loops and Moats Narrative | Team writes the defensibility story; instructor or TA reviews submissions |

---

## Activity 1 -- Channel Selection (30 min)

**Goal:** Identify the three most credible acquisition channels for your product, ranked by priority.

**Steps:**

1. Open `templates/growth-strategy-template.md`. Copy it to `04-gtm/growth-strategy.md` in your repo.
2. Brainstorm channels for 5 minutes individually. Write every channel anyone proposes, no filtering.
3. As a team, classify each channel into one of the four types (paid, organic, viral, sales).
4. Rank channels using these three criteria:
   - **Fit:** Does this channel reach your target user where they already spend time?
   - **Speed:** Can you start running it within two weeks?
   - **Cost:** Can you afford the upfront investment with the budget you have?
5. Pick the top three. Write a one-paragraph justification per channel covering all three criteria.
6. Identify one channel you considered and rejected. Write one sentence on why.

**Common mistakes in this activity:**

- Picking channels because they are trendy (TikTok, Product Hunt) rather than because they fit the user.
- Picking three channels of the same type. Your top three should ideally cover at least two different types.
- Skipping the rejected channel. Knowing what you said no to is as important as knowing what you said yes to.

---

## Activity 2 -- CAC and LTV per Channel (30 min)

**Goal:** Calculate the unit economics for each of your three channels.

**Steps:**

1. Open `templates/unit-economics-template.md`. Copy it to `04-gtm/financials/unit-economics.md`.
2. For each channel, calculate **CAC**:
   - Total spend (ad budget plus founder time at an hourly rate plus tooling).
   - Customers acquired.
   - CAC = total spend divided by customers acquired.
3. Calculate **LTV** for your product as a whole (or per segment if you have segments):
   - ARPU (average revenue per user) per month, or value proxy if your MVP is free.
   - Gross margin (revenue minus cost to serve, divided by revenue).
   - Average customer lifetime in months (use retention curve to estimate).
   - LTV = ARPU times gross margin times lifetime.
4. Compute **LTV:CAC ratio** per channel and blended.
5. Compute **payback period**: CAC divided by monthly gross margin per customer. Target under 12 months for SaaS, under 18 for enterprise.

**Sourcing assumptions:**

Every number must have a source. Acceptable sources are:

- Your own dashboard (best).
- Industry benchmark cited with a link.
- A defensible estimate with the reasoning written out.

"We think it is around 5%" is not a source. "Mailchimp's 2024 industry report shows email signup conversion of 1.8% for tech audiences (link); we use 1.8% as a placeholder and will replace with our own number once we have 2,000+ visitors" is a source.

---

## Activity 3 -- Six-Month Spreadsheet (30 min)

**Goal:** Build a monthly cohort projection covering the next six months across your three channels.

**Steps:**

1. Open `templates/growth-projection-template.xlsx`. Copy to `04-gtm/financials/growth-projection.xlsx`.
2. Set up the columns from the template: Month, Channel, Spend, Visitors, Signups, Activated, Retained D30, CAC, LTV, Cumulative users.
3. Fill in months 1 through 6 for each of your three channels.
4. Use formulas, not hardcoded numbers. The conversion rate in cell H4 should be a formula, not the number 0.05 typed in.
5. Build three scenarios: best case, expected case, worst case. Use a scenario toggle (a single cell that switches all assumption values).
6. Plot cumulative users by month for the expected case as a chart inside the spreadsheet.
7. Stress test: what happens to cumulative users if your top channel's conversion rate halves? Document the result.

**Spreadsheet hygiene:**

- Inputs in one tab, calculations in another, outputs in a third.
- Every input cell coloured (yellow is conventional) so the reviewer knows which cells to change.
- One sentence at the top of each tab describing what is in it.
- No #REF!, #DIV/0!, or #N/A errors anywhere on submission.

---

## Activity 4 -- Loops and Moats Narrative (15 min)

**Goal:** Write the story of why your growth is defensible.

**Steps:**

1. Open `templates/loops-and-moats-template.md`. Copy to `04-gtm/loops-and-moats.md`.
2. Answer: does your product have a viral loop?
   - If yes: diagram the loop in text or with a Mermaid diagram. Estimate K-factor with the math.
   - If no: write "no loop yet" honestly. Identify whether one could be added.
3. Answer: does your product have network effects?
   - Pick one of the four types covered in the lecture (direct, two-sided, data, local).
   - Write the threshold at which network effects kick in for your product.
4. Answer: what protects you against a copycat at 10x your size?
   - Brand, data, switching costs, regulatory, distribution lock-in, or honest "not much yet"?
5. Submit by committing the document and pasting the commit URL in the lab Teams channel before leaving.

---

## Submission Requirements

By the end of the lab session, all four files must be committed to your team's repository:

```
04-gtm/
├── growth-strategy.md
├── loops-and-moats.md
└── financials/
    ├── unit-economics.md
    └── growth-projection.xlsx
```

**Commit message convention:** `[LAB-10] Growth modeling deliverables`

**Submission tag:** `lab-10-submission`

**Verification:** Paste the commit URL in the Lab 10 Teams thread before leaving the lab room.

---

## Grading

This lab is graded as part of weekly Participation/Labwork. Detailed rubric in `grading-rubric.md` in this folder.

The four documents produced in this lab also feed directly into the Combined Checkpoint 2+3 (due Thursday 21 May, 20 points). Doing the lab well is the cheapest way to bank points toward CP 2+3.

---

## What If We Cannot Finish in Two Hours?

The activities are designed to fit two hours if the team is prepared. If you fall behind:

- Submit what you have at the end of the session.
- Continue working async during the week.
- Final versions must be in the repo by Wednesday 13 May 23:59 (Sprint 1 close-out deadline).
- One resubmission allowed for up to 80% of lost participation marks per the syllabus.


---

## Resources

- Week 10 lecture deck (Google Meet recording posted to Teams within 24 hours).
- Lecture key terms: CAC, LTV, payback period, K-factor, AARRR (Acquisition Activation Retention Referral Revenue), PLG.
- Worked example: `worked-example/` folder in this lab. StudySpace Finders growth model end to end.

---

**Lab Author:** Zeshan Ahmad
**Last Updated:** 5 May 2026
