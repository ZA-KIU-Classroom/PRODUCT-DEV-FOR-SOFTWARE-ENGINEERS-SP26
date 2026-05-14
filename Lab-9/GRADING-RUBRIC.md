# Lab 9 Grading Rubric

**Course:** CS-PD-2026 | Spring 2026
**Instructor:** Zeshan Ahmad
**Lab:** Lab 9 -- Growth Modeling
**Sessions:** Group A: Thursday 14 May 2026 at 14:00 | Group B: Friday 15 May 2026 at 13:00
**Total marks:** 14

---

## Overview

Lab 9 is a quantitative lab. Marks are awarded for the presence of correct structure, visible arithmetic, sourced inputs, and honest assessment of assumptions. Marks are deducted for missing calculations, unsourced numbers, hockey-stick projections without named mechanisms, and documents that describe a different product than the one the team is building.

Participation marks are awarded based on progress observed at the 0:30, 1:00, and 1:40 in-lab checkpoints. Students who are not present for a checkpoint and have not committed any work during that period receive zero participation credit for that checkpoint.

---

## Component 1: Growth Strategy Document (4 marks)

**File:** `04-gtm/growth-strategy.md`

### 4 marks -- Full credit

- Three acquisition channels named, each with its type stated (paid, organic, viral, or sales)
- Each channel justified with a specific reason tied to the product's audience and use case, not a generic statement
- Channels ranked by priority with a one-sentence rationale for the ranking
- Activation metric stated as: a specific user action + a specific number threshold + a specific time window
- The document describes this team's actual product, not a generic SaaS product

### 3 marks -- Good

- Three channels named with types, justification present but one channel's justification is weak or generic
- Activation metric present but missing one of the three required elements (action, number, or time window)

### 2 marks -- Acceptable

- Fewer than three channels, or channels named without types
- Activation metric vague (describes an action but no number or time window)
- Justifications are copy-pasted from the lecture or generic

### 1 mark -- Minimal

- Only one or two channels with minimal justification
- No activation metric or activation metric is not product-specific

### 0 marks

- File not committed, or file does not contain channel or activation metric content

---

## Component 2: Unit Economics Analysis (3 marks)

**File:** `04-gtm/financials/unit-economics.md`

### 3 marks -- Full credit

- CAC calculated for each channel with arithmetic shown (not just a result)
- Each input sourced: either "from our dashboard", a named benchmark source, or labelled as an assumption to be replaced
- LTV calculated with ARPU, gross margin, and average lifetime in months all stated explicitly
- For free products, monetisable value substitute is defined and justified
- LTV:CAC ratio computed per channel and as a blended figure
- Payback period in months calculated and present
- If LTV:CAC is below 3:1, the team has noted this and described what they will do about it

### 2 marks -- Good

- CAC and LTV present for at least two channels with arithmetic shown
- LTV:CAC present but payback period missing, or vice versa
- Most inputs sourced but one or two are unexplained numbers

### 1 mark -- Minimal

- Numbers present but no arithmetic shown; results only
- Only one channel analysed
- LTV:CAC ratio not computed

### 0 marks

- File not committed, or contains only template placeholders with no team-specific numbers

---

## Component 3: Six-Month Growth Projection (4 marks)

**File:** `04-gtm/growth-projection.xlsx`

### 4 marks -- Full credit

- Spreadsheet contains all required columns: Month, Channel, Spend, Visitors, Signups, Activated, Retained D30, CAC, LTV, Cumulative users
- All six months populated for the expected case
- Three scenarios present: expected, best case, worst case, each clearly labelled
- Best and worst cases state which single variable differs and by how much
- All conversion rate inputs have a source cited in a notes column or a separate assumptions tab
- No month-over-month growth doubles without a named causal mechanism
- The model is internally consistent: Activated is always less than or equal to Signups, Retained D30 is always less than or equal to Activated

### 3 marks -- Good

- All required columns present, at least four of six months populated in the expected case
- Three scenarios present but best and worst cases do not clearly state the variable that changes
- Most inputs sourced, a few unlabelled assumptions

### 2 marks -- Acceptable

- Required columns present, at least two months populated
- Only one scenario (expected case)
- Some inputs sourced

### 1 mark -- Minimal

- Spreadsheet exists with partial structure but fewer than two months of data
- No sources for any inputs

### 0 marks

- No spreadsheet committed, or spreadsheet is a copied worked example with no team-specific numbers

---

## Component 4: Loop and Moat Narrative (3 marks)

**File:** `04-gtm/loops-and-moats.md`

### 3 marks -- Full credit

- Viral loop section: loop is either diagrammed as a step sequence OR honestly declared absent with explanation
- If loop exists: K-factor estimated with arithmetic (invitations per user x conversion rate), and significance explained even if K is below 1
- Network effects section: type identified (direct, two-sided, data, or local) with a specific example from the product, OR honestly declared absent
- If local network effect: critical mass threshold stated as a specific number for a specific community
- Moat narrative: one paragraph that names the moat and either evidences it as strong or honestly acknowledges it as weak at current scale
- The analysis applies to this team's actual product

### 2 marks -- Good

- Loop and network effect assessed but K-factor arithmetic missing, or threshold not quantified
- Moat narrative present but either overconfident without evidence or too vague to be actionable

### 1 mark -- Minimal

- One section present and partially complete, others missing or empty
- Analysis is generic and does not describe the actual product

### 0 marks

- File not committed, or file contains only template placeholders

---

## In-Lab Participation (assessed at checkpoints, reflected in component marks)

The instructor circulates and observes at the following times:

| Checkpoint | Time | What is checked |
|------------|------|----------------|
| Checkpoint 1 | 0:30 | Growth strategy document in progress. Team can state channels and activation metric verbally. |
| Checkpoint 2 | 1:00 | Unit economics file has at least one channel with arithmetic shown. Spreadsheet is open with column headers created. |
| Checkpoint 3 | 1:40 | Spreadsheet has at least M1 and M2 populated. Loop and moat document is open and being worked on. |

Students who have committed no files and cannot demonstrate in-lab progress at a checkpoint will have their component marks capped at 1 for any component not yet started at that checkpoint.

---

## Grading Summary Table

| Component | File | Marks |
|-----------|------|-------|
| Growth Strategy Document | `04-gtm/growth-strategy.md` | /4 |
| Unit Economics Analysis | `04-gtm/financials/unit-economics.md` | /3 |
| Six-Month Growth Projection | `04-gtm/growth-projection.xlsx` | /4 |
| Loop and Moat Narrative | `04-gtm/loops-and-moats.md` | /3 |
| **Total** | | **/14** |

---

## Late Submission

Lab 9 deliverables must be committed and tagged `lab-9-submission` by the end of the session. Late commits up to 48 hours after the session will be accepted with a 2-mark deduction. After 48 hours, only work committed during the session is graded.

---

## Academic Integrity Note

Unit economics and growth projections must reflect your team's actual product and real or honestly sourced data. Copying numbers from another team's documents or from worked examples without adapting them to your product is academic misconduct. The instructor reviews commit history and file content. Identical numbers across multiple teams' submissions will be investigated.
