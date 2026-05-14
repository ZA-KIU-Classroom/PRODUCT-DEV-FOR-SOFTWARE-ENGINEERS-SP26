# Unit Economics Analysis

**Team:** [Your team name]
**Product:** [Your product name]
**Date:** [Date]
**Version:** 1.0

---

## Formulas Used

```
CAC = total spend on acquiring users through this channel / number of users acquired

LTV = ARPU x gross margin percentage x average customer lifetime in months

LTV:CAC ratio = LTV / CAC

Payback period = CAC / (ARPU x gross margin percentage)  expressed in months
```

For free products where ARPU is zero, substitute monetisable value per user per month (see note below).

---

## Free Product Monetisable Value Note

If your product is currently free, you must define the monetisable value per user. Choose one of the following and justify it:

- **Ad inventory value:** estimated CPM for your audience x average monthly page views per user
- **Data value:** what a business would pay for aggregated, anonymised data from your user base per user per month
- **B2B upsell potential:** if you will eventually charge institutions, what is the expected contract value divided by the number of users that value supports
- **Willingness to pay (from interviews):** the median price your interviewees said they would pay for this product per month

**Our monetisable value per user per month:** [Amount and unit]
**Justification:** [One to two sentences]
**Source:** [Interview data / benchmark / assumption]

---

## Channel 1: [Channel name]

**Channel type:** [Paid / Organic / Viral / Sales]

### Customer Acquisition Cost

| Input | Value | Source |
|-------|-------|--------|
| Total spend this month | [Amount in USD] | [Our budget / benchmark / assumption] |
| Customers acquired | [Number] | [Our dashboard / estimate based on conversion rates below] |
| **CAC** | **[Total spend / customers acquired]** | |

**Arithmetic shown:**
CAC = [spend amount] / [customers acquired] = [result]

**Conversion funnel for this channel:**
| Stage | Rate | Source |
|-------|------|--------|
| Click-through rate | [X%] | [Source] |
| Visitor to signup | [X%] | [Source] |
| Signup to activation | [X%] | [Source] |

---

### Lifetime Value

| Input | Value | Source |
|-------|-------|--------|
| ARPU (or monetisable value substitute) | [Amount per month] | [Source] |
| Gross margin | [X%] | [Source -- typical SaaS is 70-80%] |
| Average customer lifetime | [X months] | [Source -- from retention data or benchmark] |
| **LTV** | **[ARPU x gross margin x lifetime]** | |

**Arithmetic shown:**
LTV = [ARPU] x [gross margin] x [lifetime months] = [result]

---

### Ratio and Payback

| Metric | Value | Assessment |
|--------|-------|------------|
| LTV:CAC ratio | [LTV / CAC] | [At least 3:1 is healthy; below 1:1 is burning money] |
| Payback period | [CAC / (ARPU x gross margin)] months | [Under 12 months for SaaS is strong] |

**If LTV:CAC is below 3:1, explain the path to improving it:**
[What changes -- pricing, channel shift, retention improvement -- will move this ratio up and on what timeline?]

---

## Channel 2: [Channel name]

**Channel type:** [Paid / Organic / Viral / Sales]

### Customer Acquisition Cost

| Input | Value | Source |
|-------|-------|--------|
| Total spend this month | [Amount] | [Source] |
| Customers acquired | [Number] | [Source] |
| **CAC** | **[Result]** | |

**Arithmetic shown:**
CAC = [spend] / [customers] = [result]

**Conversion funnel:**
| Stage | Rate | Source |
|-------|------|--------|
| [Relevant first stage for this channel] | [X%] | [Source] |
| Visitor to signup | [X%] | [Source] |
| Signup to activation | [X%] | [Source] |

### Lifetime Value

Same LTV as Channel 1 unless channel mix changes the quality of users acquired. If users from this channel have materially different retention, document it here.

| Input | Value | Source |
|-------|-------|--------|
| ARPU or substitute | [Amount] | [Source] |
| Gross margin | [X%] | [Source] |
| Average lifetime | [X months] | [Source] |
| **LTV** | **[Result]** | |

### Ratio and Payback

| Metric | Value | Assessment |
|--------|-------|------------|
| LTV:CAC ratio | [Result] | |
| Payback period | [Result] months | |

---

## Channel 3: [Channel name]

**Channel type:** [Paid / Organic / Viral / Sales]

### Customer Acquisition Cost

| Input | Value | Source |
|-------|-------|--------|
| Total spend this month | [Amount] | [Source] |
| Customers acquired | [Number] | [Source] |
| **CAC** | **[Result]** | |

**Arithmetic shown:**
CAC = [spend] / [customers] = [result]

### Lifetime Value

| Input | Value | Source |
|-------|-------|--------|
| ARPU or substitute | [Amount] | [Source] |
| Gross margin | [X%] | [Source] |
| Average lifetime | [X months] | [Source] |
| **LTV** | **[Result]** | |

### Ratio and Payback

| Metric | Value | Assessment |
|--------|-------|------------|
| LTV:CAC ratio | [Result] | |
| Payback period | [Result] months | |

---

## Blended Summary

| Channel | CAC | LTV | LTV:CAC | Payback (months) | Weight in mix |
|---------|-----|-----|---------|-----------------|---------------|
| [Channel 1] | | | | | [X% of acquisition budget] |
| [Channel 2] | | | | | [X% of acquisition budget] |
| [Channel 3] | | | | | [X% of acquisition budget] |
| **Blended** | **[weighted avg]** | **[same LTV]** | **[blended ratio]** | **[weighted avg]** | 100% |

**Blended CAC arithmetic:**
Blended CAC = (CAC1 x weight1) + (CAC2 x weight2) + (CAC3 x weight3) = [result]

---

## Assumptions Register

List every input that is labelled as an assumption rather than a measured or benchmarked figure, along with the plan to replace it with real data:

| Assumption | Current value | Plan to validate | Target date |
|------------|---------------|-----------------|-------------|
| [Input name] | [Value] | [How you will measure it] | [Date] |
| | | | |
| | | | |
