# Competitive Analysis — StudySpace Finders (Worked Example)

**Team:** StudySpace Finders
**Product:** StudySpace Finders — cross-campus real-time study space discovery
**Date:** 28 May 2026
**Version:** 1.0 — Lab 11 submission

> **Note for students:** This is a worked example using the fictional reference team. Your analysis must reflect your actual product, your actual competitors, and your actual user research. Copying this example without adapting it to your product will earn zero marks.

---

## Source Document

This analysis builds on the competitive landscape seed compiled in Lab 4:
`01-discovery/synthesis/competitive-landscape-seed.md`

The seed document listed 11 alternatives mentioned by interviewees across 14 interviews. The most frequently mentioned were: Google Maps (mentioned by 9 of 14 users), the university library booking system (mentioned by 7), WhatsApp group chats for space tips (mentioned by 6), walking around campus (mentioned by all 14), and a student-built Instagram page listing study spots (mentioned by 3).

---

## Competitor Matrix

| Dimension | Google Maps | Library Booking System | University App | WhatsApp Groups | Walking Around | StudySpace Finders |
|-----------|-------------|----------------------|----------------|-----------------|----------------|-------------------|
| Core feature: discovers study spaces | 3 | 2 | 2 | 3 | 5 | 5 |
| Real-time occupancy data | 0 | 2 | 1 | 1 | 5 | 5 |
| Reservation capability | 0 | 5 | 3 | 0 | 0 | 4 |
| Noise level and amenity data | 0 | 0 | 0 | 2 | 5 | 5 |
| Cross-campus coverage | 5 | 1 | 2 | 2 | 1 | 4 |
| Mobile experience quality | 5 | 1 | 2 | 4 | 0 | 5 |
| Personalisation and user history | 3 | 1 | 1 | 0 | 0 | 4 |
| Switching cost and user lock-in | 2 | 1 | 1 | 1 | 0 | 3 |
| Zero cost to student | 5 | 5 | 5 | 5 | 5 | 5 |
| Integration with institutional systems | 2 | 5 | 5 | 0 | 0 | 2 |

---

## Competitor Profiles

### Google Maps

**Type:** Indirect competitor (general location discovery, not study-space-specific)
**Description:** Google Maps is the dominant location discovery tool globally. Students use it to find campus buildings and coffee shops but not specifically to discover study spaces or evaluate real-time suitability.
**Primary strengths:** Unmatched geographic coverage, excellent mobile UX, trusted brand, rich points of interest data, user reviews.
**Primary weaknesses:** Zero awareness of real-time occupancy for informal spaces, no noise level data, no reservation capability for study spaces, not designed for the student use case.
**Why users choose them:** "I use Maps to find where the library is but it doesn't tell me if it's packed right now." (Interview 3, Student, 19 March)

---

### Library Booking System

**Type:** Direct competitor (formal study space reservation)
**Description:** The university library's online booking system for reserving formal study rooms. Used primarily by postgraduate students for group sessions.
**Primary strengths:** Binding reservations with real-time availability for formal spaces, institutional integration and credibility, free.
**Primary weaknesses:** Covers only formal library rooms, no informal spaces, minimal mobile experience, no noise or amenity data, cross-campus coverage is zero.
**Why users choose them:** "If I need a group room for a seminar presentation practice, I use the library system. But for just finding somewhere to sit, it's useless." (Interview 7, Postgraduate, 22 March)

---

### University App

**Type:** Indirect competitor (general campus information)
**Description:** The official university mobile app covering timetables, campus maps, news, and some space availability information.
**Primary strengths:** Institutional trust, existing installation on student devices, some campus map functionality.
**Primary weaknesses:** Space information is static and rarely updated, designed as a general app not a space-finding tool, poor UX for the discovery use case, no real-time data.
**Why users choose them:** "I downloaded it for timetables but I've never used it to find a study spot. I didn't even know it had that." (Interview 11, Undergraduate, 26 March)

---

### WhatsApp Groups

**Type:** Indirect competitor (social information sharing)
**Description:** Student cohort WhatsApp groups where students informally share tips about quiet spaces, empty lecture halls, and available rooms.
**Primary strengths:** Real human knowledge, noise and context information that apps do not capture, trusted community source, already part of student workflow.
**Primary weaknesses:** Not searchable, information expires instantly, requires active participation to receive value, no reservation capability, no discovery for spaces outside your immediate social network.
**Why users choose them:** "I asked in our group chat if anyone knew a quiet spot and two people replied immediately. It's faster than searching online." (Interview 4, Undergraduate, 19 March)

---

### Walking Around

**Type:** Substitute (zero-technology)
**Description:** The behaviour of physically walking through campus buildings to find an available study space by direct observation.
**Primary strengths:** Perfect real-time accuracy (you see exactly what is there), full noise and amenity sensing, free, no technology dependency.
**Primary weaknesses:** Significant time cost (interview data: average 12 minutes per search session), range limited to what you can walk to, no advance planning or reservation, effort required before every session.
**Why users choose it:** "Sometimes I just walk around. At least you know it's accurate." (Interview 2, Undergraduate, 12 March)

---

## Synthesis

The greatest Porter force threat to our product is the threat of substitutes, rated as high pressure. Walking around campus is not a weak substitute: it provides perfect real-time accuracy and full sensory information about noise and crowding that no app can replicate at launch. Every student interview confirmed that students walk around sometimes specifically because they do not trust digital information to be current. Our product does not eliminate the substitute; it has to consistently outperform it on time cost and reliability for the substitute to become less attractive. If our occupancy data is stale or inaccurate, students will revert to walking immediately.

The two dimensions that create our most defensible competitive gap are real-time occupancy data and combined noise-plus-amenity information. On both dimensions, every named competitor scores zero or one. Google Maps has no mechanism to capture real-time occupancy for informal campus spaces. The library system covers only formal rooms. WhatsApp groups carry informal knowledge but it evaporates instantly and cannot be searched. Our product creates a persistent, searchable, user-verified record of current conditions that no existing tool provides. These dimensions matter specifically to our target segment because undergraduates in their first two years of university are the least familiar with campus geography and the most time-constrained between classes, making the cost of a failed search significantly higher for them than for experienced students who know the campus well.

The gap in real-time occupancy data would close if Google decided to add crowdsourcing or sensor integration to Maps for campus spaces, or if the university invested in sensor infrastructure and made the data publicly accessible through their own app. Neither event is imminent, but the second scenario is a medium-term institutional threat worth monitoring. A university that installs occupancy sensors in all buildings and exposes that data via their app would replicate our core value proposition with institutional credibility. Our counter-strategy is to build the depth of our community data and the richness of our amenity tagging before that infrastructure exists, so our product offers dimensions (noise levels, socket density, community ratings, cross-building comparison) that sensor data alone cannot provide.
