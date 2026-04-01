# Five Whys Guide

**Time required:** 10 minutes per pattern (do this for your top 3 patterns)  
**Purpose:** Move from surface complaints to root causes using interview evidence.

---

## What Is Five Whys?

Five Whys is a technique originally developed by Toyota to find the root cause of manufacturing defects. In product development, you use it to understand why a problem exists at a structural level, not just what users complain about.

The surface complaint is rarely the real problem. The real problem is usually 3 to 5 layers deeper.

---

## How It Works

1. Start with the surface problem as described by interviewees.
2. Ask "Why does this happen?" and answer using interview data.
3. Take that answer and ask "Why?" again.
4. Repeat until you reach a cause that is structural, systemic, or fundamental.
5. You may reach the root cause in 3 whys or 7 whys. Five is a guideline, not a rule.

---

## Example: Study Space Finding

**Surface problem:** "Students waste time looking for study spaces on campus."

**Why #1:** Why do students waste time looking for study spaces?  
Answer: They do not know which rooms are available before walking there. (P02, P05, P07)

**Why #2:** Why do they not know which rooms are available?  
Answer: There is no real-time information about room occupancy. The university website shows the schedule but not actual usage. (P03, P07)

**Why #3:** Why is there no real-time occupancy information?  
Answer: The university's room booking system tracks reservations but not walk-in usage. Most students do not reserve rooms. (P01, P04, P09)

**Why #4:** Why do students not reserve rooms?  
Answer: The reservation system requires logging in through three screens and booking 24 hours in advance. By then, plans have changed. (P04, P06)

**Why #5:** Why is the reservation system so cumbersome?  
Answer: It was designed for faculty scheduling, not student ad-hoc use. The use case was never considered.

**Root cause:** The room management infrastructure was built for scheduled faculty use, not for the ad-hoc, spontaneous study patterns of students. The gap is structural, not a missing feature.

---

## Rules for Good Five Whys

1. **Ground every answer in interview data.** Do not speculate. If you cannot answer a "why" with evidence from interviews, that is a signal your interviews did not go deep enough. Note the gap and plan follow-up questions.

2. **Use conversational phrasing.** "Why does this happen?" not "Why is the system bad?" Neutral phrasing prevents leading yourself to a predetermined conclusion.

3. **Stop when you reach something structural.** The root cause is usually a systemic issue: a misaligned incentive, a design assumption from a different era, a resource constraint, or a behavioral pattern that no one has addressed. If your root cause is "because people are lazy," you have not gone deep enough.

4. **Distinguish symptoms from causes.** "Users are frustrated" is a symptom. "The system sends 40 notifications per day with no priority ranking, making all of them feel unimportant" is a cause.

5. **Do not force exactly five.** Sometimes the root cause emerges at Why #3. Sometimes it takes Why #7. The number is a minimum target, not a fixed requirement.

---

## Common Mistakes

- **Circular reasoning:** "Why do users not use the tool? Because it is bad. Why is it bad? Because users do not use it." Each level must introduce new information.
- **Jumping to solutions:** "Why is this a problem? Because there is no app for it." That is a solution masquerading as a cause. Ask instead: why has no one built a solution?
- **Speculating without evidence:** Every answer should reference specific interview data. If you write "probably because..." you are guessing, not analyzing.
- **Stopping too early:** "Users do not know about the existing solution" is a surface cause. Why do they not know? Is it a marketing problem, a discoverability problem, or does the solution not actually work well enough for word of mouth?
