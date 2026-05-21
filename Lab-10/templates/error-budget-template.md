# Error Budget

**Product:** [Your product name]
**Team:** [Your team name]
**Window:** [e.g. 1 May 2026 to 31 May 2026]
**Date last updated:** [Date]

---

## Error Budget Summary

| SLO | Target | Window | Budget (minutes) | Consumed | Remaining | Status |
|-----|--------|--------|-----------------|----------|-----------|--------|
| [e.g. Availability] | [e.g. 99%] | 30 days | [e.g. 432 min] | [e.g. 0 min] | [e.g. 432 min] | [Green / Amber / Red] |
| [e.g. Core flow success] | [e.g. 98%] | 30 days | [e.g. 864 min] | [e.g. 0 min] | [e.g. 864 min] | [Green / Amber / Red] |
| [SLO 3 if applicable] | | | | | | |

**Status key:**
- Green: more than 50% of budget remaining
- Amber: 10% to 50% of budget remaining
- Red: less than 10% of budget remaining, or budget exhausted

---

## Budget Calculation

Show all arithmetic for each SLO.

### SLO 1: [e.g. Availability]

```
SLO target: [e.g. 99%]
Allowed downtime rate: 1 - 0.99 = 0.01 = 1%

Window in minutes:
[e.g. 30 days] x 24 hours x 60 minutes = [e.g. 43,200] minutes

Error budget:
0.01 x 43,200 = 432 minutes per 30-day window

Equivalent in hours: 432 / 60 = 7.2 hours
Equivalent in days: 7.2 / 24 = 0.3 days
```

### SLO 2: [e.g. Core flow success rate]

```
SLO target: [e.g. 98%]
Allowed failure rate: 1 - 0.98 = 0.02 = 2%

Window in minutes:
[e.g. 30 days] x 24 hours x 60 minutes = [e.g. 43,200] minutes

Error budget:
0.02 x 43,200 = 864 minutes per 30-day window

Equivalent in hours: 864 / 60 = 14.4 hours
```

---

## Incident Log for This Window

Record every incident that consumed error budget. If no incidents occurred, write "No incidents this window."

| Incident | Date | Duration | SLOs affected | Budget consumed | Postmortem link |
|----------|------|----------|--------------|----------------|----------------|
| [e.g. Deployment failure - booking endpoint 503] | [Date] | [e.g. 45 min] | [e.g. Availability, Core flow] | [e.g. 45 min from each budget] | [link or "not yet written"] |
| [Add a row for every incident] | | | | | |

**Total budget consumed this window:**

| SLO | Budget consumed | Budget remaining | % remaining |
|-----|----------------|-----------------|-------------|
| [SLO 1] | [X min] | [Y min] | [Z%] |
| [SLO 2] | [X min] | [Y min] | [Z%] |

---

## Error Budget Policy

State what actions are triggered at each threshold.

| Budget remaining | Action |
|-----------------|--------|
| More than 50% | Normal operations. Feature development continues. |
| 10% to 50% | Amber alert. Reliability items added to next sprint. No risky deployments without rollback plan. |
| Less than 10% | Red alert. Feature freeze. Engineering effort pivots to reliability. On-call review mandatory before any production push. |
| 0% or negative | Hard freeze. No deployments. Incident review required. SLO target may need revision. |

**Who owns the budget freeze decision:** [Name]

---

## Planned Maintenance

Planned maintenance consumes error budget just like unplanned incidents. Log it here.

| Maintenance activity | Date | Duration | SLOs affected | Budget consumed |
|--------------------|------|----------|--------------|----------------|
| [e.g. Database migration] | [Date] | [e.g. 20 min] | [e.g. Availability] | [e.g. 20 min] |

---

## Next Window

**Next window:** [e.g. 1 June 2026 to 30 June 2026]
**Budget resets:** [e.g. 1 June 2026]

Budget does not roll over. A full budget on the first of the month does not compensate for an exhausted budget last month. Each window is evaluated independently.
