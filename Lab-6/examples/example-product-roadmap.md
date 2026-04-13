# Product Roadmap — Example

**Team:** StudySpace Finders  
**Product:** StudySpace  
**Date:** 16 April 2026  
**Version:** 1.0  
**Sprint Arc:** April 24 to June 11 2026

> **Note to students:** This is a worked example using the fictional StudySpace Finders team. Use it to understand the expected level of depth and format. Do not copy it. Your roadmap must reflect your actual product, your actual interviews, and your actual team capacity.

---

## MVP Scope

### What We Are Building

StudySpace is a mobile-first web application that helps university students in Kutaisi find and book verified quiet study spaces on short notice. Students currently waste time travelling to spaces that are full or unsuitable, with no reliable way to check availability in advance. StudySpace solves this by surfacing real-time availability and enabling one-tap booking confirmations.

### North Star Metric

> Weekly study sessions booked per active user

### In Scope (Sprints 1 to 4)

| Feature | Sprint | Interview Evidence |
|---------|--------|--------------------|
| User signup and login (email or university SSO) | Sprint 1 | Interviews 2, 5, 8 -- students said they would not use an app requiring a new account |
| Space search by location, date, and time slot | Sprint 1 | Interviews 1, 3, 4, 7 -- primary pain point was not knowing availability before travelling |
| Space detail view (noise level, availability, distance) | Sprint 1 | Interviews 3, 6 -- students needed enough info to judge before booking |
| Booking creation and confirmation screen | Sprint 1 | Core activation moment -- drives NSM directly |
| Booking history view | Sprint 2 | Interviews 2, 9 -- students wanted to track their study sessions |
| User profile and study goal setting | Sprint 2 | Interviews 5, 10 -- secondary need after initial booking validated |
| Analytics instrumentation (all events firing, dashboard live) | Sprint 2 | Required for Checkpoint 3 evaluation |
| Push notification for booking reminder | Sprint 3 | Interviews 4, 7 -- students forget they made bookings |
| Space owner dashboard (manage availability) | Sprint 3 | Interviews 11, 12 -- supply-side needed for product to function at scale |
| Invite a friend to study together | Sprint 4 | Interview 3 -- referral mechanic noted as desirable |

### Out of Scope (MVP Phase)

| Feature | Reason Out of Scope |
|---------|---------------------|
| Payment processing for paid spaces | No interview evidence of willingness to pay at MVP stage. Will validate in Sprint 3 pricing experiment. |
| iOS / Android native apps | Web app sufficient for MVP. Mobile web performs adequately for the core booking flow. |
| AI-powered space recommendation engine | Insufficient data at MVP to train a meaningful model. Add post-course once usage data exists. |
| Rating and review system | Desirable but not required for activation moment. Sprint 5 if course continued. |

### Explicitly Rejected

| Feature | Why Rejected |
|---------|-------------|
| Social feed (share study photos) | Interview evidence consistently showed students want utility, not community. Three interviewees explicitly said they "do not want another social app." |
| Gamification (badges, leaderboards) | One interviewee suggested it. Nine did not. No pattern support. |
| Calendar integration (auto-import university timetable) | Technical complexity exceeds 8-week arc. Dependency on third-party university systems creates unacceptable risk. |

---

## Sprint Overview

| Sprint | Dates | Theme | Key Deliverable | Checkpoint |
|--------|-------|-------|-----------------|-----------|
| Sprint 1 | Apr 24 to May 7 | Foundation | A user can search for a study space and complete a booking -- end to end, deployed | Midterm Apr 30 -- dev continues async |
| Sprint 2 | May 8 to May 21 | Instrumentation | Analytics live, booking history working, first real users tested | Checkpoint 3 May 21 |
| Sprint 3 | May 22 to Jun 4 | Growth | Notifications live, space owner dashboard, pricing experiment running | Peer Assessment Jun 4 |
| Sprint 4 | Jun 5 to Jun 11 | Demo Day | Pitch-ready, repo complete, venture packet submitted | Demo Day Jun 11 |

---

## Sprint 1: Foundation

**Dates:** April 24 to May 7 2026  
**Sprint Goal:** A real user can sign up, search for a study space, and complete a booking -- from a publicly accessible URL.  
**Demo:** Live booking completed in front of instructor at Sprint Review (May 7, Google Meet).

### Capacity

| Team Member | Available Hours (excl. midterm prep) | Story Points Max |
|-------------|--------------------------------------|-----------------|
| Ana | 14 hrs | ~10 pts |
| David | 12 hrs | ~8 pts |
| Nino | 16 hrs | ~11 pts |
| **Total** | **42 hrs** | **~29 pts max** |

**Sprint 1 commitment:** 16 story points (55% of maximum)

**Rationale:** Sprint 1 overlaps with the midterm exam on April 30th. All three team members have reduced availability in the last 4 days of the sprint. We have also not yet measured team velocity with AI tools. 55% capacity is conservative and appropriate for Sprint 1.

### Stories Allocated to Sprint 1

| Story ID | Story (summary) | Points | Assignee | AI Tool |
|----------|----------------|--------|----------|---------|
| S1-01 | User can sign up with email | 3 | Ana | Google Stitch (signup UI) + Claude Code (auth backend) |
| S1-02 | User can log in and maintain session | 2 | Ana | GitHub Copilot |
| S1-03 | User can search spaces by location and time slot | 5 | David | Claude Code |
| S1-04 | User can view space detail with availability | 3 | Nino | Google Stitch |
| S1-05 | User can create a booking and see confirmation | 3 | David | Claude Code + GitHub Copilot |
| **Sprint 1 Total** | | **16** | | |

### Sprint 1 Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| Midterm overlaps with Sprint 1 -- development slows days 7 to 10 | High | Medium | Front-load development. S1-01 and S1-02 completed by Day 4. S1-03 by Day 6. |
| Stitch-generated UI requires significant manual editing to match AC | Medium | Low | Review Stitch output against AC before committing. Budget 30 min review per screen. |
| No real study space data available for demo | Medium | High | Seed 5 to 10 fictional spaces in the database before Sprint Review. Note to user: "Demo data -- live data in Sprint 2." |
| Authentication library has breaking changes since last used | Low | High | David confirms auth library version in Day 1 technical spike. If issue found, raise immediately. |

---

## Sprint 2: Instrumentation

**Dates:** May 8 to May 21 2026  
**Sprint Goal:** All analytics events are firing in the deployed application, booking history is working, and 5 real users have tested the product and provided feedback.  
**Demo:** Live dashboard in Mixpanel showing real events from real user sessions.  
**Checkpoint 3 due:** May 21 at 23:59

### Capacity

**Sprint 2 commitment:** 18 story points (adjust after Sprint 1 velocity is measured)

### Stories Allocated to Sprint 2

| Story ID | Story (summary) | Points | Assignee | AI Tool |
|----------|----------------|--------|----------|---------|
| S2-01 | All analytics events fire on correct triggers | 5 | Nino | GitHub Copilot |
| S2-02 | Mixpanel dashboard live with core funnel | 3 | Nino | None |
| S2-03 | User can view booking history | 3 | Ana | Google Stitch |
| S2-04 | User can set study goal (weekly session target) | 3 | David | Claude Code |
| S2-05 | Usability testing with 5 users completed and documented | 4 | All | None |
| **Sprint 2 Total** | | **18** | | |

### Sprint 2 Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| Recruiting 5 real users is time-consuming | High | High | Ana begins outreach in Week 8 (before Sprint 2 starts). Target: 5 sessions booked before May 8. |
| Mixpanel free tier limits event count | Low | Low | PostHog as backup if Mixpanel limits hit. Decision in Sprint Planning. |

---

## Sprint 3: Growth

**Dates:** May 22 to June 4 2026  
**Sprint Goal:** Push notification for booking reminders is live, the space owner dashboard allows availability management, and a pricing experiment is running.  
**Demo:** Space owner adds a new space and student finds and books it in the same session.

### Capacity

**Sprint 3 commitment:** 18 story points (adjust after Sprint 2 velocity)

### Stories Allocated to Sprint 3

| Story ID | Story (summary) | Points | Assignee | AI Tool |
|----------|----------------|--------|----------|---------|
| S3-01 | User receives push notification 1 hour before booking | 5 | David | Claude Code |
| S3-02 | Space owner can log in and manage their space availability | 8 | Ana + Nino | Claude Code + Google Stitch |
| S3-03 | Pricing experiment: 50% of users see premium tier prompt | 5 | David | GitHub Copilot |
| **Sprint 3 Total** | | **18** | | |

### Sprint 3 Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| S3-02 space owner dashboard is more complex than estimated | Medium | High | Split into S3-02a (login only) and S3-02b (availability management) if needed. Descope S3-02b to Sprint 4 if Sprint 3 capacity is tight. |

---

## Sprint 4: Demo Day

**Dates:** June 5 to June 11 2026  
**Sprint Goal:** Product is pitch-ready, repository is complete, and the venture packet is submitted.  
**Demo Day:** June 11 2026

### Capacity

**Sprint 4 commitment:** 10 story points (shorter sprint -- Demo Day prep is primary activity)

### Stories Allocated to Sprint 4

| Story ID | Story (summary) | Points | Assignee | AI Tool |
|----------|----------------|--------|----------|---------|
| S4-01 | Invite a friend to study together | 5 | Ana | Claude Code |
| S4-02 | Repository documentation complete (README, architecture, AI log) | 3 | Nino | None |
| S4-03 | One-pager and pitch deck updated with real data | 2 | David | None |
| **Sprint 4 Total** | | **10** | | |

---

## Full Backlog Summary

| Story ID | Summary | Sprint | Points |
|----------|---------|--------|--------|
| S1-01 | User signup | 1 | 3 |
| S1-02 | User login | 1 | 2 |
| S1-03 | Space search | 1 | 5 |
| S1-04 | Space detail view | 1 | 3 |
| S1-05 | Booking creation and confirmation | 1 | 3 |
| S2-01 | Analytics events firing | 2 | 5 |
| S2-02 | Mixpanel dashboard | 2 | 3 |
| S2-03 | Booking history | 2 | 3 |
| S2-04 | Study goal setting | 2 | 3 |
| S2-05 | Usability testing | 2 | 4 |
| S3-01 | Push notification | 3 | 5 |
| S3-02 | Space owner dashboard | 3 | 8 |
| S3-03 | Pricing experiment | 3 | 5 |
| S4-01 | Invite a friend | 4 | 5 |
| S4-02 | Repo documentation | 4 | 3 |
| S4-03 | One-pager and deck | 4 | 2 |

**Total story points across all sprints:** 62  
**Unallocated backlog points:** 0

---

## Milestone Alignment

| Milestone | Date | What Our Product Must Be Able to Do |
|-----------|------|--------------------------------------|
| Checkpoint 2 | Wed 22 Apr | Roadmap submitted, prototype testable, event schema committed |
| Sprint 1 Review | May 7 (Google Meet) | Core booking flow working and deployed |
| Checkpoint 3 | Thu 21 May | MVP functional, analytics dashboard live, 5 user tests complete |
| Peer Assessment | Thu 4 Jun | Product can be demoed without explanation |
| Demo Day | Thu 11 Jun | 7-minute pitch and live demo ready |

---

## Change Log

| Date | Version | Changes | Author |
|------|---------|---------|--------|
| 16 Apr 2026 | 1.0 | Initial roadmap created in Lab 6 | Ana |

---

*Product Roadmap Example | StudySpace Finders | CS-PD-2026 | Spring 2026*  
*This is a worked example for instructional purposes. Not a real student submission.*
