# Growth Projection Spreadsheet Reference

**StudySpace Finders -- Expected Case**
**This is a structural reference only. Build your own numbers.**

---

## Spreadsheet Structure

Create three tabs in your Google Sheet:
1. `Expected Case`
2. `Best Case`
3. `Worst Case`

Within each tab, use the following column structure:

| Column | Header | Notes |
|--------|--------|-------|
| A | Month | M1 through M6 |
| B | Channel | One row per channel per month |
| C | Spend (USD) | Budget for this channel this month |
| D | Visitors | Estimated visitors from this channel |
| E | Signups | D x signup conversion rate |
| F | Activated | E x activation rate |
| G | Retained D30 | F x D30 retention rate |
| H | CAC (USD) | C / G (spend divided by retained users) |
| I | LTV (USD) | From unit economics document |
| J | LTV:CAC | I / H |
| K | Cum Users | Running total of retained users |

Add an **Assumptions** tab that lists every rate used in columns D through G with its source.

---

## StudySpace Finders Expected Case (reference numbers only)

### Month 1

| Month | Channel | Spend | Visitors | Signups | Activated | Retained D30 | CAC | LTV | Cum Users |
|-------|---------|-------|----------|---------|-----------|-------------|-----|-----|-----------|
| M1 | Organic (community) | $30 | 300 | 66 | 20 | 10 | $3.00 | $7.65 | 10 |
| M1 | Sales (supply side) | $296 | -- | -- | -- | -- | $29.60/space | -- | 10 spaces listed |
| M1 | **Blended** | **$326** | **300** | **66** | **20** | **10** | **$32.60** | | **10** |

Notes on Month 1:
- Organic CAC shown as spend divided by retained (not just acquired) users: $30 / 10 = $3.00
- Sales channel acquires supply (spaces), not demand (users). Tracked separately.
- Viral row not included in M1 because loop is not yet built.

---

### Month 2

| Month | Channel | Spend | Visitors | Signups | Activated | Retained D30 | CAC | LTV | Cum Users |
|-------|---------|-------|----------|---------|-----------|-------------|-----|-----|-----------|
| M2 | Organic (community) | $60 | 450 | 99 | 31 | 18 | $3.33 | $7.65 | 28 |
| M2 | Viral (K=0.2) | $0 | -- | 6 | 2 | 1 | $0 | $7.65 | 29 |
| M2 | Sales (supply) | $296 | -- | -- | -- | -- | $29.60/space | -- | 20 spaces listed |
| M2 | **Blended** | **$356** | **450** | **105** | **33** | **19** | **$18.74** | | **29** |

Notes on Month 2:
- Organic spend doubles as team expands from 2 to 5 group chats targeted.
- Viral row added once shareable calendar link is shipped (assumed mid-Month 2). K=0.2 applied to 10 existing retained users each month: 10 x 0.8 shares x 25% conversion x 31% activation x 50% D30 = approximately 1 additional retained user. Shown as 1 for simplicity.
- Blended CAC improves because viral channel adds users at zero cost.

---

### Month 3

| Month | Channel | Spend | Visitors | Signups | Activated | Retained D30 | CAC | LTV | Cum Users |
|-------|---------|-------|----------|---------|-----------|-------------|-----|-----|-----------|
| M3 | Organic (community) | $90 | 550 | 121 | 37 | 22 | $4.09 | $7.65 | 51 |
| M3 | Viral (K=0.2) | $0 | -- | 12 | 4 | 2 | $0 | $7.65 | 53 |
| M3 | Sales (supply) | $148 | -- | -- | -- | -- | $14.80/space | -- | 28 spaces (self-serve kicking in) |
| M3 | **Blended** | **$238** | **550** | **133** | **41** | **24** | **$9.92** | | **53** |

Notes on Month 3:
- Organic visitor growth slows as easiest group chats are saturated. Growth from 450 to 550 vs 300 to 450 in Month 2.
- Sales spend drops by 50% as self-serve onboarding for space hosts is shipped mid-Month 3, reducing manual outreach time.
- Viral contribution grows because base of retained users grows (29 in M2, each generating 0.2 x 0.8 shares).

---

### Months 4 through 6 (structure only)

Continue the same pattern. Key variables to model:
- Organic visitor growth rate decays: assume 10% month-over-month growth rate falls to 5% by Month 6 as group chat audiences saturate.
- Activation rate improves: as onboarding is refined from usability test findings, assume activation rate rises from 31% in M1 to 45% by M4. Document the specific onboarding changes that drive this.
- D30 retention improves: as product improves, assume D30 retention rises from 50% in M1 to 60% by M5.
- Viral contribution compounds: as retained user base grows, viral acquired users per month grow proportionally.

---

## Best Case vs Expected Case (Month 3 comparison)

**Variable that differs:** Activation rate.

| Metric | Expected (31% activation) | Best (45% activation) |
|--------|--------------------------|----------------------|
| Signups M3 | 133 | 133 |
| Activated | 41 | 60 |
| Retained D30 | 24 | 36 |
| Cumulative users | 53 | 65 |
| Blended CAC | $9.92 | $6.61 |

---

## Worst Case vs Expected Case (Month 3 comparison)

**Variable that differs:** Organic visitor volume (WhatsApp group access lost).

| Metric | Expected (550 visitors) | Worst (275 visitors) |
|--------|------------------------|---------------------|
| Visitors | 550 | 275 |
| Signups | 133 | 67 |
| Activated | 41 | 21 |
| Retained D30 | 24 | 12 |
| Cumulative users | 53 | 29 |
| Blended CAC | $9.92 | $19.83 |

---

## Assumptions Tab Reference

Include a tab in your spreadsheet with the following columns:

| Input | Value used | Source | Confidence |
|-------|-----------|--------|------------|
| Visitor to signup conversion | 22% | Our landing page analytics (213 visitors, 47 signups) | High -- measured |
| Signup to activation | 31% | Our event schema: booking_completed within 60s | Medium -- 2 weeks of data |
| D30 retention | 50% | Assumption. No 30-day cohort data yet. Benchmark: 40-60% for local utility apps | Low -- assumption |
| Avg invitations per user (viral) | 0.8 | Assumption. No sharing feature built yet. | Low -- assumption |
| Viral invitation conversion | 25% | Proxy from landing page conversion rate | Low -- assumption |
| Organic CAC Month 1 | $0.64 | Calculated: $30 spend / 47 users | High -- measured |
| ARPU (monetisable value) | $1.50 | Conservative estimate from willingness-to-pay interviews (median $1.85) | Medium |
| Gross margin | 85% | Assumption based on Vercel free tier + future infrastructure estimate | Medium |
| Customer lifetime | 6 months | Proxy for academic semester length | Medium -- no churn data yet |
