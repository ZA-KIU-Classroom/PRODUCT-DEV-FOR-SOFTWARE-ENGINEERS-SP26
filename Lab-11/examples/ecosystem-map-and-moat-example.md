# Ecosystem Map — StudySpace Finders (Worked Example)

**Team:** StudySpace Finders
**Product:** StudySpace Finders — cross-campus real-time study space discovery
**Date:** 28 May 2026

> **Note for students:** This is a worked example. Your ecosystem map must name actual organisations relevant to your product in your actual market. Generic entries earn no marks.

---

## 1. Complements

| Complement | Description | Why it makes us more valuable |
|------------|-------------|-------------------------------|
| Notion | Note-taking and knowledge management tool used by a significant portion of our target user segment | Students using Notion for study session planning benefit from knowing where they will work before they open Notion. A reliable space-finding experience makes planned study sessions more likely to happen. |
| Google Calendar | Calendar tool where students schedule study blocks | A student who has blocked time on their calendar to study has already committed to a session. Finding a space quickly converts that commitment into action. Friction in finding a space causes rescheduling. |
| Toggl / Pomodoro apps | Focus and time-tracking applications used by productivity-focused students | Students who track their focus sessions care about the quality of their environment. Knowing a space is quiet before they commit to a session makes their tracking more reliable. |
| University timetabling system | The official system students use to manage their class schedule | Students look for study space in gaps between classes. Access to class schedules (even self-reported) helps users identify their available windows and plan space searches in advance. |

---

## 2. Partners

| Organisation | What they provide | Relationship status | Next action |
|-------------|-------------------|--------------------|----|
| KIU Library Services | Access to formal space occupancy data and booking system API integration | In discussion | Meeting scheduled with library IT coordinator for 2 June. Objective: data sharing agreement covering formal room availability. |
| KIU Student Union | Distribution to student population, endorsement credibility, event space data | Identified | Draft partnership proposal to be sent by 5 June. Offering occupancy data for SU-managed spaces in exchange for newsletter promotion to 4,000 student subscribers. |
| Campus Hospitality (cafes and common areas) | Real-time data on cafe capacity and opening hours | Identified | Informal conversation with campus hospitality manager on 15 May. Interest expressed. Formal proposal pending. |
| Google for Startups | Technical mentorship, cloud credits, potential accelerator programme access | Identified | Application to Google for Startups Campus programme drafted. Requires MVP analytics to be live and evidenced. Submitting after Demo Day. |

---

## 3. Threats

| Threat | Type | Likelihood | Our counter-strategy |
|--------|------|-----------|----------------------|
| Google Maps adds campus-specific occupancy layer | Platform threat | Low | Google Maps does not have campus-level occupancy data for informal spaces and is unlikely to invest in this for a niche use case. If they do, we compete on amenity depth (noise, sockets, light) and community-verified accuracy that a platform-level solution cannot deliver. |
| KIU builds its own space-finding feature in the university app | Institutional threat | Medium | We approach KIU IT and library services as partners before they build independently. A data-sharing agreement that gives them occupancy analytics in exchange for data access makes us a supplier rather than a competitor. Already in discussion (see Partners above). |
| A well-funded EdTech startup enters campus space-finding | Direct competitor | Low | The market is small enough that it is unattractive to well-funded generalists. If a direct competitor emerges, our response is to accelerate university partnership agreements, which create a data moat the competitor cannot replicate without repeating our outreach from scratch. |
| University installs IoT occupancy sensors in all buildings | Technology shift | Medium (2-3 year horizon) | Sensor infrastructure without community intelligence still lacks noise level, amenity data, and personalisation. We expand our amenity tagging and personalisation features to ensure our product offers dimensions that sensor data alone cannot provide. We also position ourselves as the data layer on top of sensor infrastructure rather than a competitor to it. |

---

## 4. Complementors

| Complementor | How they increase demand for us | Priority for engagement |
|-------------|-------------------------------|------------------------|
| EdTech productivity platforms (Coursera, Udemy, university-licensed tools) | As students invest more in self-directed learning, they spend more time outside of structured class hours studying independently. More independent study time creates more demand for reliable study space discovery. | Low (no direct engagement needed; trend benefits us passively) |
| Campus events organisers (SU events, departmental seminars) | Events that fill common areas and cafes create demand for alternative spaces. A busy campus day is our highest-demand day. Event calendars could seed predictive availability features. | Medium (explore integration of event calendar data into our occupancy predictions) |
| Study group coordination tools (Doodle, When2meet) | Students coordinating group study sessions need to find spaces that accommodate groups. Group session coordination creates demand for group-appropriate space filtering in our product. | Medium (group filtering is a planned feature; complementors drive demand for it) |
| Mental health and wellbeing services | University campaigns encouraging students to take breaks and find productive environments implicitly endorse the behaviour our product facilitates. | Low (no direct engagement; brand alignment is positive) |

---

## Strategic Priorities

The partner relationship we should prioritise in the next 90 days is the KIU Library Services data sharing agreement. The library controls formal room availability data for the largest and most in-demand spaces on campus. An agreement that gives us read access to their booking system occupancy data would immediately improve the accuracy of our coverage for the spaces students most frequently search for. In return, we offer the library anonymised aggregate occupancy analytics that help them understand peak usage patterns and plan staffing accordingly. The meeting scheduled for 2 June is the critical next step. If the agreement is in place before Demo Day, it constitutes a cornered resource that significantly strengthens our competitive position.

The threat most likely to materialise is the university deciding to build its own space-finding feature within the existing university app. We rate this as medium likelihood because the library and IT departments have already expressed awareness of student frustration with space discovery in preliminary conversations. Our counter-strategy is not to outrun the institutional build but to be inside it before it happens. By establishing a formal data sharing agreement with the library, we create a supplier relationship. If the university builds their own feature, they need our community-verified data to make it accurate. We become infrastructure rather than a competitor.

The complementor we could engage for a lightweight co-promotion is the KIU Student Union. The SU communicates directly with all 4,000 enrolled students through a weekly newsletter. A brief feature in the newsletter costs us nothing and gives us direct access to our exact target segment. In exchange, we offer the SU access to our occupancy data for SU-managed spaces, which helps them optimise space allocation for SU events. The conversation has already been initiated informally. A formal proposal with a clear value exchange should be sent before 5 June.

---

# Moat Statement — StudySpace Finders (Worked Example)

**Team:** StudySpace Finders
**Product:** StudySpace Finders — cross-campus real-time study space discovery
**Date:** 28 May 2026

> **Note for students:** This example shows a moat statement for a product with partial evidence and a parallel hypothesis for the element not yet confirmed. Your document should clearly reflect your actual current state.

---

## The Power

**Primary Helmer Power claimed:** Switching Costs (primary) with a Network Effects component emerging

We are claiming Switching Costs as our primary moat because it is the power we can evidence most directly from our current repository data. We acknowledge that Network Effects are emerging as a secondary power as our user base grows, but we do not yet have the data volume to evidence this rigorously.

---

## The Mechanism

When a student uses StudySpace Finders, they build a personal history: spaces they have visited, spaces they rated highly, preferences they have set for noise level and required amenities, and booking history in spaces that offer reservation. This accumulated history makes our product more accurate and less effortful for returning users than for first-time users. A student who has used our product for six weeks has a personalised view that reflects their specific schedule, their preferred campus areas, and their historical engagement with specific spaces. Recreating that history in a new product would require starting over. The longer a student uses our product, the higher the cost of switching to an alternative.

---

## The Evidence

**Evidence 1:**

- **Type:** Retention analytics
- **Description:** Mixpanel cohort analysis showing that 67% of users who completed their first search session returned within 7 days for a second session. Of those returning users, 82% used the filter preferences set during their first session, demonstrating engagement with personalisation features that creates history they would not want to recreate elsewhere.
- **Repository link:** `03-build/analytics/retention-cohort-may2026.png`

**Evidence 2:**

- **Type:** User quote demonstrating lock-in
- **Description:** Interview quote from a returning beta user during usability testing in Lab 5: "I've got my filters set exactly how I like it — quiet, near the engineering building, must have sockets. I'd have to set all that up again if I used something else. It's probably not that much effort but it's annoying to think about." This quote directly evidences the switching cost perception among users who have built history in our product.
- **Repository link:** `02-design/user-testing/usability-findings.md` (line 47)

**Evidence 3:**

- **Type:** Feature engagement data
- **Description:** Of 43 registered users in our beta cohort, 31 (72%) have saved at least one space to their favourites list. 18 (42%) have set at least three preference filters. These features create user-specific data that exists only in our product and would require effort to recreate in any alternative.
- **Repository link:** `03-build/analytics/feature-engagement-may2026.md`

---

## The Path Forward

Over the next 60 days, we will strengthen our switching costs moat through two specific actions. First, we will ship the personal study session history feature by 4 June, which gives users a log of every space they have visited, how long they stayed, and their rating of the experience. This deepens the personal history component of the switching cost and gives users a reason to return to our product even when they are not actively searching. Second, we will approach three additional universities (TBC: Georgian Technical University, Tbilisi State University, and Ilia State University) for beta access agreements before Demo Day, which will expand the geographic scope of our community data and make our product useful to a user who studies across campuses, a use case no other product addresses. A user who benefits from cross-campus data has a higher switching cost because no alternative currently provides this.
