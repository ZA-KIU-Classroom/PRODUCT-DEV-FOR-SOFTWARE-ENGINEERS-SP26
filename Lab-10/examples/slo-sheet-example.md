# SLO Sheet — StudySpace Finders

> **This is a worked example for Lab 10. It uses the fictional StudySpace Finders product.
> Your team must write your own SLO sheet with targets calibrated to your actual product and infrastructure.**

**Product:** StudySpace Finders
**Team:** StudySpace Finders (fictional reference team)
**Date:** 21 May 2026
**Review cadence:** Monthly, and after every SEV1 or SEV2 incident

---

## SLO 1: Availability

**SLI definition:**
- Metric: Percentage of HTTP requests to our deployed application that return a 2xx or 3xx response code
- Formula: (requests returning 2xx or 3xx) / (total requests) x 100
- Measured by: UptimeRobot monitoring our deployment URL at studyspace-finders.vercel.app with a 5-minute check interval, plus Vercel function invocation logs
- Measurement frequency: Every 5 minutes via UptimeRobot
- Current measured value: 99.4% over the last 30 days (3 incidents totalling approximately 248 minutes of degraded availability)

**SLO target:**
- Target: 99% availability
- Time window: Rolling 30 days
- Why this target is achievable: Vercel hobby plan has historically delivered approximately 99.9% infrastructure availability. Our application-level incidents (deployment failures, database connection issues) account for the gap between infrastructure uptime and our own. Setting our SLO at 99% rather than 99.9% gives us an error budget that reflects our actual reliability capability at this stage.

**Error budget:**
```
SLO target: 99%
Allowed downtime rate: 1 - 0.99 = 0.01 = 1%

Time window: 30 days
30 x 24 x 60 = 43,200 minutes

Error budget: 0.01 x 43,200 = 432 minutes per 30-day window
Equivalent in hours: 432 / 60 = 7.2 hours per month
```

**Current error budget status (May 2026):**
- Budget: 432 minutes
- Consumed: 248 minutes (from three incidents: deployment failure 45 min, Supabase connection timeout 120 min, Vercel edge function cold start issues 83 min)
- Remaining: 184 minutes
- Status: AMBER (43% remaining)

---

## SLO 2: Core Flow Success Rate

**SLI definition:**
- Metric: Percentage of booking_attempted events that are followed by a booking_completed event within 60 seconds for the same user session
- Formula: (sessions with booking_completed within 60s of booking_attempted) / (sessions with booking_attempted) x 100
- Measured by: Mixpanel funnel: booking_attempted to booking_completed, segmented by session ID, with a 60-second conversion window
- Measurement frequency: Calculated daily from Mixpanel event data and reviewed weekly
- Current measured value: 96.8% over the last 30 days

**SLO target:**
- Target: 95% core flow success rate
- Time window: Rolling 30 days
- Why this target is achievable: Current measured rate is 96.8%. Setting the target at 95% provides a reasonable buffer for known causes of booking failure (space becomes unavailable between search and booking attempt, network timeout on slow mobile connections) without tolerating systematic issues.

**Error budget:**
```
SLO target: 95%
Allowed failure rate: 1 - 0.95 = 0.05 = 5%

This SLO operates on a transaction basis, not a time basis.
Over 30 days we receive approximately 500 booking_attempted events.

Error budget: 0.05 x 500 = 25 failed booking attempts per 30-day window

If we receive more than 25 booking_attempted events without a corresponding
booking_completed in 60 seconds, we have exhausted this budget.

Current consumption: 500 x (1 - 0.968) = 16 failed attempts
Remaining: 25 - 16 = 9 attempts
Status: AMBER (36% remaining)
```

---

## SLO 3: Latency

**SLI definition:**
- Metric: p95 response time for POST /api/bookings (the booking creation endpoint)
- Formula: 95th percentile of response time in milliseconds across all invocations of the booking creation serverless function
- Measured by: Vercel function duration logs, sampled daily
- Measurement frequency: Daily review of Vercel function metrics
- Current measured value: p95 = 380ms over the last 7 days

**SLO target:**
- Target: p95 response time below 2000ms for booking creation
- Time window: Rolling 7 days
- Why this target is achievable: Current p95 is 380ms. Vercel serverless functions have a cold start penalty of approximately 200 to 500ms on the hobby plan. Setting the threshold at 2000ms provides ample headroom while still catching genuine performance regressions.

**Error budget:**
```
SLO target: p95 below 2000ms
This is a threshold-based SLO.

Over 7 days we receive approximately 115 booking_attempted events.
5% of those may exceed the 2000ms threshold.

Error budget: 0.05 x 115 = 5.75 requests, round to 5 requests per 7-day window.

Current consumption: 115 x (1 - 0.997) = approximately 0 requests above 2000ms
Remaining: 5 requests
Status: GREEN (budget essentially untouched)
```

---

## Error Budget Policy

| Budget remaining | Action |
|-----------------|--------|
| More than 50% | Normal operations. Feature development continues. Risky deployments allowed with rollback plan documented. |
| 10% to 50% | Amber alert. At least one reliability improvement item added to the current sprint. No deployments during peak usage hours (09:00 to 18:00 on weekdays) without a tested rollback procedure. |
| Less than 10% | Red alert. Feature freeze. All engineering effort pivots to reliability. Incident review required before any production push, including hotfixes. |
| 0% or negative | Hard freeze. No deployments of any kind. Root cause analysis required and documented. SLO target may need to be revised for the next window. |

**Who owns the budget freeze decision:** David Kvaratskhelia (Tech Lead). In his absence, the on-call team member for the week.

---

## Severity Definitions

### SEV1: Core flow completely down

**Criteria for StudySpace Finders:**
- The deployment URL is unreachable (Vercel returns 500 or 503 for more than 50% of requests over 5 minutes)
- OR no user can complete a booking attempt (POST /api/bookings returns 5xx for more than 50% of requests over 5 minutes)
- OR authentication is completely broken (no user can log in)

**Response:** All team members interrupted immediately.
**Communication:** Message in team Whatsapp group within 5 minutes of detection.
**Target time to acknowledge:** 15 minutes
**Target time to mitigate:** 2 hours (restore service, even in degraded mode)
**Target time to resolve:** 24 hours (identify and fix root cause)

---

### SEV2: Degraded experience, core flow partially affected

**Criteria for StudySpace Finders:**
- Booking success rate drops below 90% for 30 or more minutes
- OR search results take more than 5 seconds to load for more than 10% of users
- OR a key feature is completely broken (e.g. search filters return no results regardless of input, email notifications fail for all users)
- OR availability drops below 99% for the current rolling 30-day window (error budget amber threshold breached)

**Response:** On-call team member investigates. Others notified in team channel but not interrupted.
**Communication:** Message in team Whatsapp within 30 minutes.
**Target time to acknowledge:** 30 minutes
**Target time to mitigate:** 8 hours

---

### SEV3: Minor issue, no or minimal user impact

**Criteria for StudySpace Finders:**
- A non-critical feature is broken but the core flow (search and booking) works (e.g. booking history page shows an error, admin space management panel is slow)
- OR error rate on non-core endpoints is elevated but below 5%
- OR a single user reports an issue that cannot be reproduced
- OR analytics events are missing for some sessions but core functionality is unaffected

**Response:** Issue logged as a GitHub issue with the label `sev3`. Scheduled for the next working session.
**Communication:** GitHub issue only. No interruption of team members.
**Target time to acknowledge:** Next working day
**Target time to fix:** Current or next sprint

---

## On-Call Rotation

| Week | On-call | Backup |
|------|---------|--------|
| 18 to 24 May 2026 | David Kvaratskhelia | Nino Tsiklauri |
| 25 to 31 May 2026 | Nino Tsiklauri | Ana Beridze |
| 1 to 7 June 2026 | Ana Beridze | David Kvaratskhelia |

**On-call responsibilities:**
- Check deployment URL once per day (morning)
- Respond to SEV1 alerts within 15 minutes, SEV2 within 30 minutes
- Create a GitHub issue for every alert, even if it resolves without intervention
- Hand off any open incidents to the incoming on-call member at the start of their week
