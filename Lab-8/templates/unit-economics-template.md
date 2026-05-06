# Unit Economics Analysis

**Team:** [Team name]
**Product:** [Product name]
**Document version:** 1.0
**Last updated:** [Date]

---

## 1. Lifetime Value (LTV)

LTV is the total value a customer generates across their entire relationship with your product.

### Formula

```
LTV = ARPU × Gross Margin × Lifetime
```

### Inputs

**ARPU (Average Revenue Per User per Month):** $[amount]

Source: [How you got this number. Own dashboard? Industry benchmark? Estimate from interviews?]

**Gross Margin:** [%]

Calculation: (Revenue minus cost to serve) / Revenue
- Revenue per user per month: $[amount]
- Cost to serve per user per month: $[amount] (infrastructure, support, transaction fees, third-party APIs)
- Gross margin = ([revenue] - [cost]) / [revenue] = [%]

**Average Lifetime:** [months]

Source: [Retention curve from your dashboard, or industry benchmark, or honest estimate]

### Calculation

```
LTV = $[ARPU] × [margin %] × [lifetime months]
LTV = $[result]
```

### If Your Product Is Free (Value Proxy)

Replace ARPU with monetisable value per user per month:
- Ad-equivalent revenue: $[amount]
- Data value: $[amount]
- B2B upsell potential: $[amount]
- Other: $[amount]

Total monetisable value per user per month: $[amount]

LTV (proxy) = $[amount] × [margin %] × [lifetime] = $[result]

---

## 2. Customer Acquisition Cost (CAC) per Channel

### Channel 1 -- [Name]

| Item | Value |
|------|-------|
| Ad spend | $[amount] |
| Founder/team time (hours × rate) | $[amount] |
| Tooling specific to this channel | $[amount] |
| Agency or contractor fees | $[amount] |
| **Total spend** | **$[amount]** |
| Customers acquired | [number] |
| **CAC** | **$[amount]** |

**Source for spend:** [Where the numbers come from]

**Source for customers acquired:** [Dashboard? Manual count?]

---

### Channel 2 -- [Name]

| Item | Value |
|------|-------|
| Ad spend | $[amount] |
| Founder/team time | $[amount] |
| Tooling | $[amount] |
| Agency fees | $[amount] |
| **Total spend** | **$[amount]** |
| Customers acquired | [number] |
| **CAC** | **$[amount]** |

---

### Channel 3 -- [Name]

| Item | Value |
|------|-------|
| Ad spend | $[amount] |
| Founder/team time | $[amount] |
| Tooling | $[amount] |
| Agency fees | $[amount] |
| **Total spend** | **$[amount]** |
| Customers acquired | [number] |
| **CAC** | **$[amount]** |

---

### Blended CAC

```
Blended CAC = total spend across all channels / total customers acquired
Blended CAC = $[amount] / [number] = $[amount]
```

---

## 3. LTV to CAC Ratio

### Per Channel

| Channel | LTV | CAC | Ratio | Interpretation |
|---------|-----|-----|-------|----------------|
| [Name] | $[amount] | $[amount] | [X]:1 | [Healthy / borderline / unhealthy] |
| [Name] | $[amount] | $[amount] | [X]:1 | [interpretation] |
| [Name] | $[amount] | $[amount] | [X]:1 | [interpretation] |

### Blended

LTV : Blended CAC = $[LTV] : $[CAC] = [X]:1

### Interpretation

A ratio above 3:1 is healthy. Below 3:1 means margin is thin. Below 1:1 means you lose money on every customer.

[Two to three sentences on what your numbers tell you about your business model.]

---

## 4. Payback Period

Time until you earn back the cost of acquiring a customer.

```
Payback = CAC / (ARPU × Gross Margin per month)
```

### Per Channel

| Channel | CAC | Monthly margin per user | Payback (months) |
|---------|-----|-------------------------|------------------|
| [Name] | $[amount] | $[amount] | [number] |
| [Name] | $[amount] | $[amount] | [number] |
| [Name] | $[amount] | $[amount] | [number] |

### Target

- SaaS: under 12 months
- Enterprise: under 18 months
- Consumer: varies, but usually under 6 months

### Interpretation

[How does your payback period compare to targets? What does it imply for your runway?]

---

## 5. Assumptions and Sources

Every assumption must have a source. Acceptable sources:

- Your own analytics dashboard (best)
- Industry benchmark with link
- Defensible estimate with reasoning

| Assumption | Value | Source | Confidence |
|------------|-------|--------|------------|
| [e.g., signup conversion rate] | [%] | [Mailchimp 2024 industry report (link)] | Low/Medium/High |
| [next assumption] | [value] | [source] | [confidence] |

---

## 6. Sensitivity Analysis

What happens if the riskiest assumption is wrong?

**Riskiest assumption:** [Name it]

**Current value:** [number]

**If it is half what we expect:** [What happens to LTV:CAC?]

**If it is double what we expect:** [What happens to LTV:CAC?]

**What we will do to validate this assumption in Sprint 2:** [Concrete action]

---

## 7. What We Will Refine and When

Many of these numbers are placeholders. Document when you will replace each with real data.

| Number | Currently | Replace by | How |
|--------|-----------|------------|-----|
| [e.g., signup conversion rate] | [Industry benchmark 1.8%] | [Wed 13 May] | [After 2,000 visitors via Reddit posts] |

---

**Filed by:** [Names]
