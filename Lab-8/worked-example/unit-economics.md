# Unit Economics Analysis -- StudySpace Finders

**Team:** StudySpace Finders
**Product:** Real-time campus study space finder
**Document version:** 1.0
**Last updated:** 7 May 2026

---

## 1. Lifetime Value (LTV)

The product is currently free for students. We use a value proxy because there is no revenue model in the MVP. The proxy reflects the value we create for users (time saved) and what that value is worth to the university or potential sponsors.

### Inputs

**Value proxy per user per month:** $4.00

Source: Estimated as follows. Average user does 5 study sessions per week. Without our product, each session costs ~15 minutes hunting for a space (from our 12 interviews). With our product, ~1 minute. Time saved: 14 minutes per session times 5 sessions per week times 4 weeks = 280 minutes per month. At a notional student-time value of $0.85 per hour (which is the regional minimum-wage equivalent), that is $3.97 per user per month. We round to $4.00. We acknowledge this is a soft estimate; the real monetisable value would come from B2B partnerships with the university or sponsorship by relevant brands, neither of which is in scope for the MVP.

**Gross Margin:** 92%

Calculation:
- Revenue (proxy) per user per month: $4.00
- Cost to serve per user per month: $0.32
  - Vercel hosting at the free tier: $0
  - Mixpanel analytics free tier (within free limits up to 100k events): $0
  - Database (Supabase free tier): $0
  - Allocation of supporting infra and tooling per user at scale: $0.32 (estimated)
- Gross margin = (4.00 - 0.32) / 4.00 = 92%

**Average Lifetime:** 8 months

Source: We do not have retention data yet. Estimate based on the academic calendar: an average user signs up midway through a semester and uses the product through to the end of the next semester. Two semesters at KIU is approximately 8 months including breaks. We acknowledge this is a placeholder and will be replaced with a measured retention curve once we have 12 weeks of data.

### Calculation

```
LTV = $4.00 × 92% × 8 months = $29.44
```

We round to **$29.44** for the model.

---

## 2. Customer Acquisition Cost (CAC) per Channel

### Channel 1 -- KIU CS Discord and Reddit (r/KIU)

| Item | Value |
|------|-------|
| Ad spend | $0 |
| Founder/team time (4 hours/week × 2 weeks × 2 people × $5/hour student rate) | $80 |
| Tooling specific to this channel | $0 (already using existing accounts) |
| Agency fees | $0 |
| **Total spend** | **$80** |
| Customers acquired (target, expected case) | 80 |
| **CAC** | **$1.00** |

Source for spend: Our team time at student labour rate. We use $5 per hour as a defensible internal opportunity cost.

Source for customers acquired: Estimated from r/KIU and Discord member counts times an estimated 5 to 10% engagement rate times an estimated 8 to 12% signup conversion. Will be replaced with actual data after 2 weeks.

---

### Channel 2 -- Faculty Mailing List

| Item | Value |
|------|-------|
| Ad spend | $0 |
| Founder/team time (6 hours drafting, approval cycles, follow-up at $5/hour) | $30 |
| Tooling | $0 (existing email account) |
| Agency fees | $0 |
| **Total spend** | **$30** |
| Customers acquired (expected case) | 70 |
| **CAC** | **$0.43** |

Source: Single send to 312 students. Industry benchmark for opt-in academic email is 30 to 45% open rate and 5 to 15% click rate, so we estimate 90 to 140 visitors and 50 to 90 signups (because these are highly trusted introductions).

---

### Channel 3 -- Physical Posters

| Item | Value |
|------|-------|
| Print cost (20 A4 colour posters at $1.25 each) | $25 |
| Founder time (1 hour to put up, 1 hour weekly to refresh × 4 weeks at $5/hour) | $25 |
| Tooling | $0 |
| Agency fees | $0 |
| **Total spend** | **$50** |
| Customers acquired (expected case, 4-week period) | 40 |
| **CAC** | **$1.25** |

Source: Estimated scan rate at our 7 poster locations of 30 to 50 per week, with 60% completing signup based on the high intent of someone scanning a poster at the moment they need a study space.

---

### Blended CAC

```
Blended CAC = ($80 + $30 + $50) / (80 + 70 + 40) = $160 / 190 = $0.84
```

---

## 3. LTV to CAC Ratio

### Per Channel

| Channel | LTV | CAC | Ratio | Interpretation |
|---------|-----|-----|-------|----------------|
| Discord and Reddit | $29.44 | $1.00 | 29.4x | Very healthy, but the LTV proxy is soft |
| Faculty mailing list | $29.44 | $0.43 | 68.5x | Healthiest, but one-shot channel |
| Physical posters | $29.44 | $1.25 | 23.6x | Healthy if the scan rate holds |

### Blended

LTV : Blended CAC = $29.44 : $0.84 = **35x**

### Interpretation

The ratios look exceptional, and that is honest given that our channels are organic and free. But the LTV is a soft estimate, not measured revenue. If we replace the value proxy with a more conservative number (e.g., $1.50 per user per month based on what a student would pay if asked, which we have not validated), the LTV becomes $11.04 and the blended ratio drops to 13x. Still healthy, but a useful reminder that LTV:CAC is sensitive to the LTV input.

The bigger concern is not the ratio. It is the channel saturation. r/KIU has 1,247 members. After 4 to 8 weeks, we will have hit most of the addressable Reddit audience. We need to add new channels by Sprint 3 or growth flatlines.

---

## 4. Payback Period

```
Payback = CAC / (Value proxy × Gross Margin per month)
```

### Per Channel

| Channel | CAC | Monthly margin per user | Payback (months) |
|---------|-----|-------------------------|------------------|
| Discord and Reddit | $1.00 | $3.68 | 0.27 |
| Faculty mailing list | $0.43 | $3.68 | 0.12 |
| Physical posters | $1.25 | $3.68 | 0.34 |

### Target

For a typical SaaS, under 12 months. For a free product with a value proxy, the payback is essentially instant once a user is activated. This metric becomes more meaningful when we add a real revenue model in a future iteration.

---

## 5. Assumptions and Sources

| Assumption | Value | Source | Confidence |
|------------|-------|--------|------------|
| Value proxy per user per month | $4.00 | Internal calculation from time saved | Low |
| Gross margin | 92% | Free-tier infra costs estimated | Medium |
| Average lifetime | 8 months | Academic calendar estimate, no data yet | Low |
| Discord/Reddit signup conversion | 8 to 12% | Mailchimp 2024 industry email benchmark for tech audiences (placeholder for community signup) | Low |
| Faculty email open rate | 30 to 45% | Higher Education email benchmark from CASE 2023 report | Medium |
| Faculty email click rate | 5 to 15% | Same source | Medium |
| Poster scan rate | 30 to 50 per week | Estimate, no data | Low |
| Poster scan-to-signup | 60% | Estimate based on high intent | Low |

---

## 6. Sensitivity Analysis

**Riskiest assumption:** Average lifetime of 8 months.

**Current value:** 8 months

**If it is half what we expect (4 months):** LTV becomes $14.72, blended ratio drops to 17.5x. Still healthy, no strategic change.

**If it is double (16 months):** LTV becomes $58.88, blended ratio is 70x. Same conclusion: ratio is comfortable.

**Why this is the riskiest assumption:** Most users may use the app for one semester only, then forget about it. We have no evidence either way. The estimate is based on the academic calendar, not on user behaviour.

**What we will do to validate this assumption in Sprint 2:** Monitor D30 retention starting with the first cohort that signs up after 14 May. Cohort analysis at week 12 will give us a real curve.

---

## 7. What We Will Refine and When

| Number | Currently | Replace by | How |
|--------|-----------|------------|-----|
| Visit-to-signup conversion (Reddit/Discord) | 8 to 12% (industry benchmark) | Wed 13 May | First two weeks of Reddit posts gives us actual conversion |
| Email open and click rate | Industry benchmark | Mon 18 May | Faculty email send is Fri 15 May; results visible by following Monday |
| Poster scan rate | 30 to 50 per week (estimate) | Tue 19 May | One week of UTM data after posters go up |
| Average lifetime | 8 months (calendar estimate) | End of semester | Need a full retention curve, only available in retrospective |
| Value proxy ($4/month) | Internal estimate | If we pivot to monetisation | Currently fine as a proxy for free product value |

---

**Filed by:** Nino, David, Mariam, Luka
