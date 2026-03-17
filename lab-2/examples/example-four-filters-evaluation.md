# Example: Four Filters Evaluation

> This is an annotated worked example. Use it to understand what a strong evaluation looks like. Do not copy it.

**Team Name:** Team Spotlight (example)
**Date:** 19 March 2026
**Members present:** Anna, Giorgi, Mariam, David

---

## Problem Candidates Being Evaluated

| # | Problem Candidate | Proposed by |
|---|-------------------|-------------|
| 1 | Finding quiet study spaces on campus during class gaps | Anna, Giorgi |
| 2 | Coordinating group project work across different schedules | Mariam |
| 3 | Tracking gym progress without a personal trainer | David |
| 4 | Getting feedback on code assignments between office hours | Giorgi |
| 5 | Managing multiple food delivery order tracking across apps | Anna |

---

## Evaluations

### Problem 1: Finding quiet study spaces on campus during class gaps

**Real and Recurring**
- Score: 3/3
- Justification: All four team members have personally experienced this in the past two weeks. Two of us have had it happen on the same day we are writing this evaluation. We can name at least 15 classmates immediately who would recognise this problem. It happens multiple times per week for anyone with a non-consecutive timetable.

> **Annotation:** A score of 3 here requires that you can name specific people who experience it, and that it happens frequently. "All four of us have experienced this today" is strong evidence. Do not give yourself a 3 if the only evidence is "it seems like it would happen."

**Painful Enough to Act**
- Score: 3/3
- Known workaround: Messaging 3-4 WhatsApp group chats, checking the library booking portal (which only shows full-room reservations, not individual seats), and eventually settling for the corridor near Room 214 or the ground-floor cafeteria. This process takes 20-40 minutes.
- Justification: The workaround is active and specific. People are spending significant time on it every time it occurs. The fact that they have developed a multi-step process to cope with it confirms the pain is real and acute enough to motivate behaviour.

> **Annotation:** A vague workaround ("they just deal with it") scores a 1. A precisely described workaround scores a 3. The more specific you can be about what people are actually doing, the stronger your evidence.

**Underserved Today**
- Score: 3/3
- Existing solutions: The university library booking system exists but only allows full-room reservations and shows no real-time seat availability. Google Maps shows building locations but nothing about available indoor workspace. No tool shows current occupancy of informal spaces (corridors, lounges, labs).
- Justification: We spent 20 minutes genuinely trying to solve this problem with existing free tools before scoring this filter. We could not find a satisfactory solution. The library system is the closest thing to a solution and it does not address the core need.

> **Annotation:** You must actually try the existing solutions before scoring this filter. If you can solve the problem with a five-minute Google search, you do not have a real gap.

**Accessible to You**
- Score: 3/3
- Who could you interview this week: We can name 12 students right now who match our ICP and are reachable by WhatsApp. Three team members are CS students who see these people daily. We plan to conduct interviews between classes tomorrow.
- Justification: Perfect accessibility. We are the target user. Our network is full of people who experience this problem. No special access or domain knowledge is required beyond what we already have.

**Total: 12/12**
**Recommendation: Strong candidate. Pursue this problem.**

---

### Problem 2: Coordinating group project work across different schedules

**Real and Recurring**
- Score: 2/3
- Justification: This problem exists but is intermittent. It occurs mainly around deadlines and when a new project starts. Three of us have experienced it, but not consistently throughout the semester. When it is not deadline season, it largely goes away.

> **Annotation:** A score of 2 here reflects genuine uncertainty about frequency. The problem is real but not reliably recurring. This is honest scoring.

**Painful Enough to Act**
- Score: 2/3
- Known workaround: WhatsApp groups, Telegram, and sometimes shared Google Docs. Some teams use Notion or Trello.
- Justification: People have workarounds but they are often functional enough. Existing tools like WhatsApp and Notion partially address this problem. The pain is present but many people have adapted reasonably well.

**Underserved Today**
- Score: 1/3
- Existing solutions: WhatsApp, Telegram, Google Calendar, Notion, Trello, Asana, Monday.com, and many more tools all partially or fully address this problem for most users.
- Justification: This space is genuinely crowded. The gap between existing solutions and user needs is small for most people in our target group. Building here means competing with established tools with large user bases.

**Accessible to You**
- Score: 3/3
- Who could you interview this week: Any student doing group coursework. Easy to access.
- Justification: Excellent accessibility, but this does not rescue a problem that fails other filters.

**Total: 8/12**
**Recommendation: Possible candidate. However, the low score on Underserved is a significant concern. Existing tools are adequate for most users. Do not pursue unless you can identify a specific segment where existing tools fail in a way that is not currently served.**

---

### Problem 5: Managing multiple food delivery order tracking across apps

**Real and Recurring**
- Score: 1/3
- Justification: This happens to one team member occasionally. We cannot name other people who experience this as a consistent frustration. It seems like a minor convenience issue rather than a real recurring problem for a specific segment.

**Painful Enough to Act**
- Score: 1/3
- Known workaround: None beyond opening each app individually.
- Justification: The workaround is trivial. People are not distressed by this. It does not cause them to lose significant time or face significant consequences.

**Underserved Today**
- Score: 2/3
- Existing solutions: Some attempt has been made by apps like Uber Eats to consolidate, but cross-platform aggregation does not exist.

**Accessible to You**
- Score: 2/3
- Justification: We could find people who order food frequently, but the population who uses multiple apps simultaneously is small.

**Total: 6/12**
**Recommendation: Drop. Fails on pain and frequency. Not a serious candidate.**

---

## Summary Scorecard

| Problem | R&R | P2A | Underserved | Accessible | Total | Recommendation |
|---------|-----|-----|-------------|------------|-------|----------------|
| 1 — Study spaces | 3 | 3 | 3 | 3 | 12/12 | Strong candidate |
| 2 — Group coordination | 2 | 2 | 1 | 3 | 8/12 | Possible — underserved concern |
| 3 — Gym tracking | 2 | 2 | 2 | 2 | 8/12 | Possible |
| 4 — Code feedback | 3 | 2 | 2 | 3 | 10/12 | Strong candidate |
| 5 — Food delivery tracking | 1 | 1 | 2 | 2 | 6/12 | Drop |

---

## Team Discussion Notes

> **Annotation:** This section matters for grading. Show your reasoning, not just your conclusions.

We had a significant debate about Problem 2 (group coordination). David felt strongly that the problem is underserved and that existing tools are too complex. The rest of the team felt the existing tools are actually functional enough for most students, and that we were at risk of building a simpler version of tools that already exist. We resolved this by applying the Underserved filter strictly: when we sat down and tried to coordinate a group project using Notion for 15 minutes, it worked. That killed the argument for a 3.

We also considered Problem 4 (code feedback) as a serious candidate — it scored 10/12. It was narrowly beaten by Problem 1 because the accessibility advantage of Problem 1 is significant: we are the target user and can start interviews tomorrow with no friction.

---

## Decision

Our committed problem for Lab 2 is: **Finding quiet study spaces on campus during class gaps (12/12)**

The runner-up problem we are keeping alive as our secondary ICP candidate is: **Getting feedback on code assignments between office hours (10/12)**
