# SLO Sheet

**Product:** [Your product name]
**Team:** [Your team name]
**Date:** [Date]
**Review cadence:** [e.g. Monthly, or after every incident]

---

## Overview

This document defines our Service Level Indicators, Service Level Objectives, and severity definitions. These are internal commitments, not customer-facing SLAs. They exist to make reliability visible and to give us a principled way to decide when to stop shipping features and invest in stability instead.

---

## Glossary

**SLI (Service Level Indicator):** A specific metric we measure. The raw number.
**SLO (Service Level Objective):** The target we set for an SLI over a time window. An internal commitment.
**SLA (Service Level Agreement):** A contractual commitment to a customer with consequences for breach. Most student-stage products do not have SLAs yet.
**Error budget:** The amount of unreliability the SLO allows. Budget = (1 - SLO target) x time window.

---

## SLI and SLO Definitions

### SLO 1: [e.g. Availability]

**SLI definition:**
- Metric: [e.g. Percentage of HTTP requests that return a 2xx or 3xx response code]
- Formula: [e.g. successful_requests / total_requests x 100]
- Measured by: [e.g. Vercel deployment analytics / UptimeRobot / our custom health check endpoint]
- Measurement frequency: [e.g. Every 5 minutes]
- Current measured value: [e.g. 99.2% over the last 30 days, or "not yet measured"]

**SLO target:**
- Target: [e.g. 99% availability]
- Time window: [e.g. Rolling 30 days]
- Why this target is achievable: [e.g. Vercel hobby plan guarantees approximately 99.5% uptime. We set our SLO below the infrastructure ceiling.]

**Error budget:**
```
SLO target: 99%
Time window: 30 days = 30 x 24 x 60 = 43,200 minutes
Error budget = (1 - 0.99) x 43,200 = 432 minutes per 30-day window
```

**Current error budget remaining this window:** [e.g. 432 minutes (full budget, no incidents this window) / or calculate based on known downtime]

---

### SLO 2: [e.g. Core flow success rate]

**SLI definition:**
- Metric: [e.g. Percentage of [core user action] attempts that complete without a 5xx error]
- Formula: [e.g. successful_booking_attempts / total_booking_attempts x 100]
- Measured by: [e.g. Mixpanel funnel: booking_attempted to booking_completed, excluding sessions where a 5xx was logged]
- Measurement frequency: [e.g. Calculated daily from event data]
- Current measured value: [e.g. 97.8% over the last 30 days, or "not yet measured"]

**SLO target:**
- Target: [e.g. 98% core flow success rate]
- Time window: [e.g. Rolling 30 days]
- Why this target is achievable: [e.g. Based on current event data, we average 97.8%. Setting the target at 98% creates slight pressure to improve without being unreachable.]

**Error budget:**
```
SLO target: 98%
Time window: 30 days = 43,200 minutes
Error budget = (1 - 0.98) x 43,200 = 864 minutes per 30-day window
```

**Current error budget remaining this window:** [Calculate or state "not yet tracked"]

---

### SLO 3 (optional): [e.g. Latency]

**SLI definition:**
- Metric: [e.g. p95 response time for the core API endpoint]
- Formula: [e.g. 95th percentile of response times in milliseconds across all requests to POST /api/bookings]
- Measured by: [e.g. Vercel function logs, or a custom timing middleware]
- Current measured value: [e.g. p95 = 340ms, or "not yet measured"]

**SLO target:**
- Target: [e.g. p95 response time below 2000ms]
- Time window: [e.g. Rolling 7 days]
- Why this target is achievable: [e.g. Current p95 is 340ms. The 2000ms target allows significant headroom for peak load.]

**Error budget:**
```
SLO target: p95 below 2000ms
This is a threshold SLO, not a percentage SLO.
Budget: no more than 5% of requests in a 7-day window may exceed 2000ms.
7 days = 7 x 24 x 60 = 10,080 minutes
Budget time above threshold = 0.05 x 10,080 = 504 minutes
```

---

## Error Budget Policy

When any SLO error budget is exhausted in a given window:

1. No new feature deployments until the window resets or the budget is partially restored through improved reliability
2. Engineering effort in the next sprint pivots to reliability improvement, not feature work
3. An incident review is mandatory before the next production push, even if no single incident caused the budget exhaustion

**Who owns the error budget decision:** [Name the team member who calls the freeze]

---

## Severity Definitions

Calibrate these to your actual product. A study space booking app has different criteria than a content platform.

### SEV1: Core flow completely down

**Definition for [your product]:** [e.g. No user can complete a booking. The primary search or booking endpoint returns 5xx for more than 50% of requests. Or the entire deployment is unreachable.]

**Response:** All hands. Interrupt whatever you are doing.
**Communication:** Post in team Slack or group chat immediately. Inform teammates within 5 minutes.
**Target time to acknowledge:** 15 minutes
**Target time to mitigate:** 2 hours

### SEV2: Degraded experience, core flow partially affected

**Definition for [your product]:** [e.g. Some users cannot complete bookings. Error rate above 5% on core endpoints. Or a key feature (e.g. search filters) is broken but bookings still work.]

**Response:** On-call team member investigates. Others notified but not interrupted.
**Communication:** Post in team channel within 30 minutes.
**Target time to acknowledge:** 30 minutes
**Target time to mitigate:** 8 hours

### SEV3: Minor issue, no user impact or minimal impact

**Definition for [your product]:** [e.g. A non-critical feature is broken (e.g. email notifications not sending). Error rate elevated but below 1% on core endpoints. Performance degraded but within SLO.]

**Response:** Logged and scheduled for next working session.
**Communication:** GitHub issue created with SEV3 label.
**Target time to acknowledge:** Next working day
**Target time to fix:** Next sprint

---

## On-Call Rotation

Even as a student team, assign an on-call week per person rotating. This distributes the burden and ensures every team member understands the operational side of what they have built.

| Week | On-call | Backup |
|------|---------|--------|
| [Week] | [Name] | [Name] |
| [Week] | [Name] | [Name] |
| [Week] | [Name] | [Name] |

**On-call responsibilities:** Check the deployment URL once per day. Respond to SEV1 and SEV2 alerts within the target times above. Create a GitHub issue for any alert that fires, even if it resolves on its own.
