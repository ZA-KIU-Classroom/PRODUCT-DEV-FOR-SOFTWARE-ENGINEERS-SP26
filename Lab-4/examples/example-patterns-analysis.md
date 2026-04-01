# Example: Pattern Analysis

**Team:** StudySpace Finders  
**Date:** April 3, 2026  
**Based on:** 10 interviews across March 12 to March 28

---

## Frequency Table

| Rank | Pattern Name | Interviews Mentioning | Percentage | Pain Intensity (1-5) | Combined Score |
|------|-------------|----------------------|-----------|---------------------|---------------|
| 1 | Time wasted on room hunting | 8 / 10 | 80% | 4 | 3.2 |
| 2 | Unreliable availability information | 7 / 10 | 70% | 4 | 2.8 |
| 3 | Group coordination friction | 6 / 10 | 60% | 3 | 1.8 |
| 4 | Peak period anxiety | 5 / 10 | 50% | 3 | 1.5 |
| 5 | Quality mismatch of spaces | 4 / 10 | 40% | 2 | 0.8 |

---

## Pattern 1: Time Wasted on Room Hunting (Rank #1)

**Frequency:** 8 of 10 interviews (P01, P02, P03, P05, P06, P07, P09, P10)

**Pain Intensity:** 4 / 5

**Supporting quotes:**

1. "I walked to three buildings last Tuesday before I found an empty room. Took me 35 minutes." (P03)
2. "I waste at least 20 minutes every single time. That is probably 2 hours a week." (P02)
3. "I have a 90-minute gap and I spend half of it just finding a place to sit." (P07)

**Emotional language observed:** "waste," "frustrating," "ridiculous," "gave up"

**Consequences reported:**
- Time impact: 20 to 40 minutes per incident, 1 to 3 times per week (P02, P07)
- Academic impact: Less productive study time, lower quality work (P05)
- Emotional impact: Frustration, resignation, sense of wasted effort (P03, P09)

### Five Whys for Pattern 1

**Surface problem:** Students spend 20 to 40 minutes per attempt looking for available study spaces.

**Why #1:** Why do students spend so much time looking?  
Answer: They do not know which rooms are available before walking there. They have to physically check each location. (P02, P03, P07)

**Why #2:** Why do they not know which rooms are available?  
Answer: There is no real-time information system. The university website shows class schedules for rooms but not whether walk-in study spaces are occupied. (P03, P07)

**Why #3:** Why is there no real-time information?  
Answer: The university tracks room reservations but not actual walk-in occupancy. Most students do not reserve rooms for informal study. (P01, P04)

**Why #4:** Why do students not reserve rooms?  
Answer: The reservation system requires booking 24 hours in advance through a three-step login process. Student study needs are spontaneous, not planned. (P04, P06)

**Why #5:** Why is the system designed for advance booking only?  
Answer: It was built for faculty course scheduling, not student ad-hoc study. The use case was never part of the requirements.

**Root cause:** The room management system was architected for predictable, scheduled faculty use. Spontaneous student study was never a design consideration, creating a structural gap between available infrastructure and actual usage patterns.

### Current Workarounds

| Workaround | Who Uses It | How Well It Works | Why It Falls Short |
|-----------|------------|------------------|-------------------|
| Text friends already on campus | P04, P08, P10 | Sometimes works if a friend is nearby | Depends on having a friend in the right place at the right time |
| Arrive 30+ min early | P02, P05 | Guarantees a spot but wastes time | Loses the same time they are trying to save |
| Check library Instagram | P08 | Rough visual estimate of crowd | Photos are old, do not show specific rooms, unreliable |

---

## Cross-Pattern Analysis

Patterns 1 and 2 are directly connected: time is wasted (Pattern 1) because information is unreliable (Pattern 2). Fixing information reliability would directly reduce time wasted.

Pattern 3 (group coordination) is partially independent. Even if students could find individual spaces easily, coordinating group study involves scheduling complexity on top of space finding.

The strongest product signal comes from the intersection of Patterns 1 and 2: a solution that provides real-time, reliable space availability would address the two highest-ranked patterns simultaneously.

---

## Team Sign-Off

- [x] Ana K. - April 3, 2026
- [x] Giorgi M. - April 3, 2026
- [x] Luka T. - April 3, 2026
- [x] Nino S. - April 3, 2026
