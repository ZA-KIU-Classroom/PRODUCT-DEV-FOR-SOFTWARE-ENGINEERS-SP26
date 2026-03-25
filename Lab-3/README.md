# Lab 3: Interviews and Synthesis

**Course:** CS-PD-2026 Product Development for Software Engineers  
**Institution:** Kutaisi International University (KIU)  
**Instructor:** Zeshan Ahmad (zeshan.ahmad@kiu.edu.ge)  
**GitHub Org:** ZA-KIU-Classroom/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS-SP26

---

## Lab Dates

| Group | Day | Date | Time |
|-------|-----|------|------|
| Group A | Thursday | March 26, 2026 | 14:00 to 16:00 |
| Group B | Friday | March 27, 2026 | 13:00 to 15:00 |

**Important for Group A:** The Week 4 lecture (JTBD and Value Proposition Design) runs this same morning at 12:00 to 14:00. Lab 3 begins immediately after at 14:00. You will be applying JTBD framing to your interview data within hours of hearing it for the first time.

**Lectures that inform this lab:**
- Week 3 (Thursday March 19): Design Thinking and Prototyping
- Week 4 (Thursday March 26): Jobs-to-be-Done and Value Proposition Design

---

## Deadlines

| Deliverable | Type | Due |
|-------------|------|-----|
| Lab 3 team deliverables (all files below) | Team | **Wednesday April 1 at 23:59** |
| Homework 1: Individual Interview Contribution Log | Individual | **Wednesday April 8 at 23:59** |

Apply the submission tag `lab-3-submission` at the time of your final push.

---

## Lab Purpose

You committed to a problem in Lab 2 and left with an interview script and an outreach plan. Now you come back with data.

This lab has three purposes:

1. **Hold you accountable for real interviews.** Not scheduled. Not almost done. Conducted, logged, and committed to your repository.
2. **Teach you to synthesize qualitative data.** Raw quotes are not insights. Affinity mapping transforms raw quotes into patterns you can act on.
3. **Build the foundation for Checkpoint 1.** Every deliverable produced today feeds directly into your CP1 submission.

By the end of this lab your team must have a minimum of 4 to 5 interview logs committed to GitHub, a first-pass affinity map, and a revised interview script v2.

---

## Learning Objectives

By the end of Lab 3 students will be able to:

- Document a customer interview to a professional standard with verbatim quotes and structured analysis
- Group qualitative data using affinity mapping and name clusters as problem statements
- Diagnose weaknesses in an interview script and produce an improved version grounded in actual interview data
- Distinguish between a symptom quote and a root-cause quote
- Connect interview findings to the JTBD framework introduced in the Week 4 lecture

---

## Prerequisites: Status Check Before Starting Lab 3

The first 10 minutes of the lab are a structured status check. The instructor will circulate and spot-check repositories. Teams self-report first.

### What Must Be Complete from Lab 1 (Week 2 slot, March 13/14)

| Deliverable | File Path | Minimum Standard |
|-------------|-----------|-----------------|
| Team contract | `00-foundation/team-contract.md` | Signed by all members, roles defined, communication norms agreed |
| ICP document | `00-foundation/team-icp.md` | At least one ICP defined with demographic, behavioral, and pain context |
| Repository README | `README.md` (repo root) | Team name, member names with GitHub usernames, problem space, folder structure |
| Individual commits | Any file | Every team member has committed at least once |

### What Must Be Complete from Lab 2 (Week 3 slot, March 19/20)

Lab 2 team deliverables were due **Wednesday March 25 at 23:59**. The following must be present and committed:

| Deliverable | File Path | Minimum Standard |
|-------------|-----------|-----------------|
| Problem statement | `00-foundation/team-problem-statement.md` | Chosen via Four Filters, rationale documented |
| Interview script v1 | `01-discovery/interview-script-v1.md` | Opening, 5+ open-ended core questions, closing. No leading questions, no solution-pitching |
| Outreach tracker | `01-discovery/outreach-tracker.md` | At least 5 people contacted, at least 3 interviews confirmed or completed |
| Minimum 1 completed interview | `01-discovery/interview-logs/` | A team arriving at Lab 3 with zero conducted interviews is behind schedule |

### Red Flags Requiring Immediate Instructor Conversation

The following are structural failures that put the team's ability to meet the Wednesday April 1 deadline at risk:

- No commits beyond the initial repo scaffold
- ICP is aspirational (based on assumption, not any real conversation with a real person)
- Interview script contains hypothetical questions ("Would you use a product that...?"), closed questions, or solution descriptions
- Zero interviews conducted or confirmed
- Team contract unsigned or missing members
- Any team member has never committed to the repository

---

## Lab Structure (120 minutes)

| Time Block | Activity | Output |
|------------|----------|--------|
| 0:00 to 0:10 | Status check | Instructor assessment, team self-report |
| 0:10 to 0:35 | Interview log clinic | `01-discovery/interview-logs/interview-[N]-*.md` |
| 0:35 to 1:05 | Affinity mapping session | `01-discovery/synthesis/affinity-map-draft-[YYYYMMDD].png` + `affinity-map-notes.md` |
| 1:05 to 1:35 | Interview script v2 workshop | `01-discovery/interview-script-v2.md` |
| 1:35 to 1:55 | Outreach sprint planning | Updated `01-discovery/outreach-tracker.md` |
| 1:55 to 2:00 | Commit, push, tag | All files in repository |

---

## Part 1: Status Check (0:00 to 0:10)

Teams self-report answers to these three questions before the instructor checks the repository:

1. How many interviews has your team completed and logged?
2. Is your interview script committed and free of leading questions?
3. Did anything in your interviews change your thinking about the problem?

The instructor will open two or three team repositories on the projector for a live spot-check.

Teams with zero completed interviews will not do affinity mapping today. They use the full lab session for outreach calling and scheduling, and must submit at least 4 logs before the **Wednesday April 1 at 23:59** deadline.

---

## Part 2: Interview Log Clinic (0:10 to 0:35)

### Purpose

Every interview that has been conducted must be logged to the standard format before the lab ends. Use this 25 minutes to finalize any logs that exist only as raw notes or voice memos.

### Quality Standard for a Passing Log

1. **Participant profile** -- role, context, how recruited, date and duration, ICP fit assessment
2. **At least 3 verbatim quotes** -- word-for-word, in quotation marks, not paraphrased
3. **Key observations** -- non-verbal cues, emotional responses, contradictions, hesitation
4. **Preliminary insights** -- what this interview suggests about the problem (stated as hypotheses, not facts)
5. **Open questions** -- what you still do not know after this interview

### What Does Not Count

- A paragraph summary of what the person said
- Bullet points with no verbatim quotes
- A file containing only the participant's name and date

### JTBD Connection

When writing the insights section of each log, attempt to frame at least one insight in JTBD language:

> "The participant is hiring [current solution or workaround] to do the job of [functional outcome] when [context or trigger]. The emotional job is [how they want to feel]. The social job is [how they want to be seen]."

### File Naming Convention

```
01-discovery/interview-logs/interview-[N]-[pseudonym-or-initials]-[YYYYMMDD].md
```

Example: `interview-03-AR-20260324.md`

Template: `Lab-3/templates/interview-log-template.md`

---

## Part 3: Affinity Mapping Session (0:35 to 1:05)

### What Is Affinity Mapping

Affinity mapping takes individual data points -- quotes, observations, moments from interviews -- and groups them by theme. The goal is to let patterns emerge from data rather than confirm patterns you assumed before you started.

### Tools

- **Miro** (recommended): miro.com, free board, one sticky per quote or observation
- **FigJam**: same approach
- **Physical**: Post-it notes on a wall or table, photograph and upload

### Protocol

**Step 1 -- Extraction (10 min)**  
Each team member independently reviews all committed interview logs and copies every quote, observation, and insight onto a separate sticky. One idea per sticky. Do not group yet. Aim for 5 to 8 stickies per interview.

**Step 2 -- Silent sort (10 min)**  
Working in silence, team members move stickies into groups by similarity. No discussion. If you disagree with a placement, move it. If it gets moved back, duplicate it into both groups.

**Step 3 -- Name and discuss (10 min)**  
Name each cluster as a problem statement, not a category label.

Not this: "Scheduling"  
This: "Users do not know whether a space is available until they have already arrived and wasted the commute"

Discuss the two or three largest clusters. What surprised you? Which cluster most directly confirms or contradicts your original problem hypothesis?

### Deliverables

```
01-discovery/synthesis/affinity-map-draft-[YYYYMMDD].png
01-discovery/synthesis/affinity-map-notes.md
```

The notes file must include: cluster names, sticky count per cluster, and explicit reflection on what the map confirmed and what it contradicted.

Template: `Lab-3/templates/affinity-map-notes-template.md`

---

## Part 4: Interview Script v2 Workshop (1:05 to 1:35)

### Why You Are Rewriting the Script

Your v1 script was written before you had spoken to anyone. Every interview revealed something: a question that produced generic answers, a topic the participant wanted to explore more, an off-script question that worked better than anything you planned. This is how discovery is supposed to work.

### Protocol

**Step 1 -- Score every v1 question (10 min)**  
Open `01-discovery/interview-script-v1.md`. For each question, assign: Keep / Drop / Rephrase.

- **Keep:** Produced specific, story-based, emotionally honest answers
- **Drop:** Produced generic, short, or yes/no answers
- **Rephrase:** Good topic, poor framing

**Step 2 -- Add questions from affinity map clusters (10 min)**  
Identify the two or three clusters needing more data. Write one new question per cluster. Each question must be open-ended, past-tense, and contain no reference to your solution.

**Step 3 -- Finalize and commit (10 min)**  
Produce `01-discovery/interview-script-v2.md` with a changelog documenting what changed and why.

Template: `Lab-3/templates/interview-script-v2-template.md`

---

## Part 5: Outreach Sprint Planning (1:35 to 1:55)

### The Target

**Homework 1 (individual, due Wednesday April 8 at 23:59)** requires each student to submit evidence of personally conducting at least 3 interviews. Your team needs a minimum of 10 total interviews to build a credible affinity map. If you have 4 to 5 after Lab 3, you need 5 to 6 more before the **Wednesday April 1 team deadline**.

### Activity

Update `01-discovery/outreach-tracker.md` with planned contacts:
- Name or pseudonym of each person to contact
- Channel (email, WhatsApp, LinkedIn, in-person)
- Date of planned contact
- Owner (which team member is responsible)

Before leaving the lab: every team member must own at least one new outreach with a specific channel and deadline.

### What Counts as an Interview

- Participant genuinely matches your ICP
- At least 15 minutes long
- Logged with 3+ verbatim quotes and committed to the repository

---

## Lab 3 Deliverables Summary

All files committed, pushed, and tagged `lab-3-submission` by **Wednesday April 1 at 23:59**.

| Deliverable | File Path | Minimum Standard |
|-------------|-----------|-----------------|
| Interview logs (4 to 5 minimum) | `01-discovery/interview-logs/interview-[N]-*.md` | 3+ verbatim quotes, participant profile, observations, insights |
| Affinity map image | `01-discovery/synthesis/affinity-map-draft-[YYYYMMDD].png` | All current interview data represented |
| Affinity map notes | `01-discovery/synthesis/affinity-map-notes.md` | Cluster names, counts, contradiction analysis |
| Interview script v2 | `01-discovery/interview-script-v2.md` | Changelog from v1, improved questions, no solution language |
| Updated outreach tracker | `01-discovery/outreach-tracker.md` | New contacts planned, owners assigned |

### How to Submit

```bash
git add .
git commit -m "[LAB-3] Interviews, affinity map, script v2, outreach plan"
git push origin main
git tag lab-3-submission
git push origin lab-3-submission
```

---

## Looking Ahead

**Homework 1 -- Individual Interview Contribution Log**  
Due: **Wednesday April 8 at 23:59** (individual submission)  
Each student submits evidence of personally conducting and documenting at least 3 customer discovery interviews. Full spec in the course repository.

**Checkpoint 1 -- Discovery (10 points)**  
Due: **Wednesday April 1 at 23:59** (same deadline as Lab 3 team deliverables)  
Requires: 10+ completed and logged interviews, affinity map, evidence-based problem statement, ICP document, interview script v2. Lab 3 deliverables are the primary inputs. Full rubric in `checkpoints/checkpoint-1-rubric.md`.

**Lab 4 -- Discovery Synthesis and Prototyping**  
Group A: Thursday April 2 at 14:00 / Group B: Friday April 3 at 13:00  
Complete interviews (10+ total), final affinity mapping, pattern analysis, evidence-based problem statement, low-fidelity prototype v1, competitive landscape seed exercise.

---

## Resources

| Resource | Link |
|----------|------|
| The Mom Test (Rob Fitzpatrick) | https://themomtest.com |
| Affinity Diagramming (Nielsen Norman Group) | https://www.nngroup.com/articles/affinity-diagram/ |
| Miro affinity mapping template | https://miro.com/templates/affinity-diagram/ |
| JTBD interview techniques | https://jtbd.info/2-what-is-jobs-to-be-done-jtbd-796b82081cca |
| Design Thinking (Tim Brown, HBR) | https://hbr.org/2008/06/design-thinking |

---

Office hours: book via email at zeshan.ahmad@kiu.edu.ge

**File:** `Lab-3/README.md` | **Course:** CS-PD-2026 / CS7161 | **Semester:** Spring 2026
