# Problem Statement Quality Bar

**Course:** CS-PD-2026  
**Used in:** Lab 1 and throughout the semester  

---

## Why This Document Exists

The quality of every downstream decision in this course -- your ICP, your interview script, your solution design, your MVP scope -- depends on the quality of your problem statement. A vague problem statement produces vague interviews. Vague interviews produce vague insights. Vague insights produce products nobody uses.

Use this guide to calibrate your Lab 1 problem statements and to evaluate them again before Lab 2.

---

## The Four Dimensions of a Strong Problem Statement

### Dimension 1: Specificity of WHO

The person experiencing the problem must be described precisely enough that you could identify them if you walked into a room.

| Weak | Strong |
|------|--------|
| "Students" | "Third-year CS students at KIU who are enrolled in three or more project-based courses simultaneously" |
| "Small business owners" | "Georgian restaurant owners who have fewer than 5 staff and take both cash and card payments" |
| "Older people" | "Adults over 60 in Tbilisi who are primary caregivers for a grandchild and manage household expenses independently" |
| "Developers" | "Junior backend developers in their first job at a company with no dedicated DevOps team" |

**Test:** Could two different people independently identify the same person from your WHO description? If yes, it is specific enough. If one person would picture a student and another would picture a professional, it is too vague.

---

### Dimension 2: Specificity of WHAT

The problem must describe a specific behaviour, failure mode, or unmet need -- not a general theme or abstract concept.

| Weak | Strong |
|------|--------|
| "trouble coordinating" | "lose visibility into which tasks teammates have picked up after a task list is agreed, leading to duplicated work or dropped tasks discovered only at the submission deadline" |
| "difficulty managing finances" | "overspend their monthly budget in the first two weeks because income and expenses are tracked across three separate apps that do not sync" |
| "communication problems" | "receive conflicting instructions from two supervisors on the same task and have no established protocol for resolving the conflict without going over one person's head" |
| "bad user experience" | "abandon a form on the third page because the error message does not tell them which field failed validation, only that something went wrong" |

**Test:** Could you write an interview question that would reveal whether this WHAT is actually happening? If yes, it is specific enough. If it is too abstract to ask about directly, make it more concrete.

---

### Dimension 3: Context (WHEN and WHERE)

Problems do not occur in a vacuum. The context in which a problem occurs is often as important as the problem itself -- it determines who you interview, what triggers you look for, and what solution constraints apply.

| Weak | Strong |
|------|--------|
| "when they are busy" | "in the 72 hours before a project submission deadline, when team communication volume is highest" |
| "at work" | "during the onboarding period for a new client, before the project management system has been set up for that account" |
| "sometimes" | "every time they receive a payment in a foreign currency" |
| "in stressful situations" | "when they receive a message after 22:00 from a family member that requires a response but the topic is emotionally charged" |

**Test:** Does your context specify either a time or a place (or both) that you could observe? Could you tell a user "describe the last time this happened" and have them give you a concrete answer?

---

### Dimension 4: Consequence (WHY IT MATTERS)

This is where pain lives. Without a real consequence, a problem is an inconvenience -- not something worth solving with a product.

Consequences fall into three categories:
- **Time:** They lose significant time regularly
- **Money:** They lose money, overpay, or forgo income
- **Emotional or social:** They experience stress, embarrassment, damaged relationships, or lost confidence

| Weak | Strong |
|------|--------|
| "it is annoying" | "they lose approximately 45 minutes per week recreating information they already captured once in a different format" |
| "it causes problems" | "they have missed two assignment deadlines this semester because they were waiting on a teammate and did not want to escalate" |
| "it is inefficient" | "the workaround takes twice as long as the actual task and causes them to defer the task until the last possible moment, increasing error rate" |
| "people do not like it" | "three of their regular customers have switched to a competitor in the past two months and cited this as the reason when asked" |

**Test:** Would you pay money or significantly change your behaviour to eliminate this consequence? If yes, the pain is real. If you are not sure, the consequence is probably not specific enough.

---

## The Full Scoring Guide

Score your problem statement on each dimension before submitting it.

| Dimension | 0 | 1 | 2 |
|-----------|---|---|---|
| **WHO** | A category, not a segment | A segment but could be more specific | Could identify this person in a room |
| **WHAT** | A theme or concept | A behaviour but underspecified | A specific failure mode or unmet need |
| **WHEN/WHERE** | Absent or "sometimes" | Partially contextualised | Specific trigger, time, or place |
| **WHY** | Absent or "it's annoying" | Vague consequence | Specific, quantified or emotional cost |

**Total out of 8:**
- 7-8: Strong problem statement, ready for Lab 2
- 5-6: Solid foundation, add specificity to the weakest dimension
- 3-4: Needs significant work before Lab 2 -- interview the person you have in mind before committing to this problem
- 0-2: Return to observation. This problem has not been grounded yet.

---

## Before and After Examples

### Example 1

**Before:** "People have trouble managing their time during exams."

**After:** "KIU students in the final two weeks of semester who are sitting four or more exams in six calendar days do not have a reliable way to estimate how long study for each subject will take, causing them to under-prepare for the later exams in their schedule, which they report noticing only after sitting the first two exams and realising they have less revision time than assumed."

**What changed:** WHO became specific (KIU students in a specific exam period), WHAT became a specific failure (inability to estimate study time distribution), WHEN became specific (the final two weeks with a dense exam schedule), and WHY became a real consequence (under-preparation for later exams, realised too late to correct).

---

### Example 2

**Before:** "Freelancers have problems with invoicing."

**After:** "Georgian freelance web developers with 3-8 clients per month who invoice in both GEL and USD spend 2-3 hours per month manually calculating exchange rates, redoing invoice formatting for different clients, and following up on unpaid invoices via personal WhatsApp messages because they do not use professional invoicing software -- primarily because the options they have found are either too expensive or not localised for the Georgian banking context."

**What changed:** Freelancers became a specific type of freelancer in a specific country with a specific client load. "Problems with invoicing" became specific pain points with named causes. The WHY became specific (time spent, the WhatsApp follow-up behaviour, the reason they do not use existing tools).

---

## Common Failure Modes

**The Solution-Flavoured Problem**  
"People need a better app for tracking their gym workouts." This is not a problem -- it is a solution with "people need" in front of it. Rewrite it by asking: what specifically does someone fail to do, lose, or suffer without this solution?

**The Trend-Derived Problem**  
"With the rise of AI, professionals need to upskill quickly." This comes from an article, not an observation. If you cannot describe the specific person you watched struggle with this specific consequence in this specific context, you do not yet have a problem statement.

**The Complaint Without Consequence**  
"University canteen food is bad." A complaint is the starting point for a problem statement, not the statement itself. Follow it with "and this matters because..." until you find a real consequence.

**The Wish Disguised as a Problem**  
"There should be an easier way to find apartments in Tbilisi." This is a wish. Convert it: "Recent KIU graduates searching for apartments in Tbilisi with a budget below 700 GEL per month lose 10-20 hours of search time per successful placement because listings on Facebook marketplace are often out of date, lack floor plans, and do not specify whether utilities are included, requiring individual follow-up on each one before a viewing can be arranged."

---

*CS-PD-2026 | Kutaisi International University | Spring 2026*
