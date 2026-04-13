# EXAMPLE: North Star Metric
## StudySpace Finders | CS-PD-2026 Example Team

*This is a worked example to show what a completed NSM document looks like. Do not copy this. Your metric must come from your own synthesis.*

---

## Our North Star Metric

```
Weekly study sessions booked per active user
```

---

## Why This Metric

**Question 1: What is the core action a user takes that proves they got value from our product?**

Our users are KIU students who need a verified quiet study space on short notice. The moment they get value is not when they search for a space. It is not even when they view the results. The moment they get value is when they successfully complete a booking and arrive at a confirmed space to study. Everything before that is friction we need to reduce. Everything after that is the outcome we need to sustain.

We chose "booked" rather than "arrived" because arrival is difficult to measure without geolocation, and booking completion is a discrete, unambiguous event that we can instrument reliably.

**Question 2: Can we measure it? Is it a discrete, countable event?**

Yes. The event `booking_completed` fires exactly once per successful booking. We can count the number of `booking_completed` events per `user_id` per 7-day rolling window. This gives us a clean weekly rate per active user. An "active user" for this metric is defined as any user who has fired at least one event in the past 14 days.

**Question 3: Does it change when our product gets better or worse?**

Yes. If we ship a release that breaks the booking flow, the booking completion rate drops immediately. If we improve the search results ranking so better spaces appear first, we expect the booking rate to increase because users find suitable spaces faster. If we add a cancellation feature that allows users to rebook, we expect the weekly rate to increase for users who previously had to abandon a booking attempt.

A metric that does not move when the product changes is not measuring the right thing. This one does.

---

## What Our NSM Is Not

| Alternative Metric | Why We Rejected It |
|-------------------|--------------------|
| Total signups | Measures acquisition only. A user can sign up and never search. Does not reflect product value. |
| Daily active users | Active doing what? A user who opens the app and immediately closes it counts as active. Not useful. |
| Search sessions started | Measures intent, not completion. A user could search 10 times and never book. That is a failure state. |
| Total spaces listed | This measures supply-side growth, not user value. We care about whether students book, not whether spaces exist. |
| Session duration | Time in app does not mean value. A confused user spends more time in the app trying to complete a booking. |

---

## Connection to AARRR

**Stage:** Activation (and the unit of Retention measurement)

Our NSM sits primarily in Activation because it measures the first time a user completes the core value action. It also serves as the Retention measurement because we track it weekly -- a user who books every week is a retained user. A user who booked once six weeks ago and has not booked since is a churned user.

---

## Connection to Prototype

**Screen name:** Booking Confirmation

**What the user does on that screen:** Taps "Confirm Booking" after reviewing the space name, date, time slot, and price.

**Event that fires:** `booking_completed`

**How that event feeds the NSM:** Each `booking_completed` event increments the weekly booking count for the associated `user_id`. Our analytics dashboard will show a chart: average `booking_completed` events per user per 7-day window, updated daily.

---

## Team Sign-Off

| Name | Role | Agreement |
|------|------|-----------|
| Lekso | Product Lead | Agreed |
| Dato | Engineering Lead | Agreed |
| Nino | Design Lead | Agreed |
| Ana | Research Lead | Agreed |

**Date agreed:** 9 April 2026

---

*Example Document | StudySpace Finders | CS-PD-2026 | Spring 2026*
