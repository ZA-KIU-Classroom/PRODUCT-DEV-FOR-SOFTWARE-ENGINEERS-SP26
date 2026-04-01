# Lab 4: Discovery Synthesis and Prototyping

**Course:** CS-PD-2026 Product Development for Software Engineers  
**Semester:** Spring 2026  
**Lab Sessions:** Group A Thursday April 2, 14:00 to 16:00 | Group B Friday April 3, 13:00 to 15:00  
**Instructor:** Zeshan Ahmad (zeshan.ahmad@kiu.edu.ge)

---

## Overview

Lab 4 is the culmination of your discovery phase. You will take the raw interview data you have collected over the past three weeks and transform it into three things: validated patterns, an evidence-based problem statement, and a first prototype sketch. You will also compile a competitive landscape seed document that becomes the foundation for your full competitive analysis in Week 13.

This is the most important synthesis work of the semester. Everything you build from here forward depends on the quality of what you produce today.

---

## Prerequisites

Before you arrive at lab, you must have:

- At least 8 completed interview logs (10+ is the target) in `/01-discovery/interview-logs/`
- Each interview log with 3 or more verbatim quotes
- All completed interviews committed to your GitHub repository
- Your laptop and interview notes
- Your ICP document reviewed and up to date (`/00-foundation/team-icp.md`)
- Interview script v2 committed (`/01-discovery/interview-script-v2.md`)

If you do not have at least 8 interviews, use the first 30 minutes of lab for emergency catch-up. See `templates/emergency-interview-template.md`.

---

## Lab Timeline (2 Hours)

| Time | Phase | Activity | Template |
|------|-------|----------|----------|
| 0:00 to 0:10 | Setup | Readiness checklist, folder creation | `templates/synthesis-readiness-checklist.md` |
| 0:10 to 0:50 | Affinity Mapping | Extract insights, cluster, label | `templates/affinity-map-template.md` |
| 0:50 to 1:20 | Pattern Analysis | Frequency, intensity, Five Whys | `templates/patterns-analysis-template.md` |
| 1:20 to 1:40 | Problem Statement | Assemble evidence-based statement | `templates/final-problem-statement-template.md` |
| 1:40 to 1:50 | Prototype Sketching | Paper sketches or Figma wireframes | See guide |
| 1:50 to 2:00 | Competitive Landscape Seed | List alternatives from interviews | `templates/competitive-landscape-seed-template.md` |

Instructor checkpoints happen at 0:30, 1:00, and 1:30. Raise your hand if you are stuck at any point.

---

## Deliverables

### Due at End of Lab (commit before you leave)

1. **Affinity map documentation** with photo evidence (`/01-discovery/synthesis/affinity-map.md` + `affinity-map-photo.jpg` or `.png`)
2. **Pattern analysis** with frequency table and Five Whys for top 3 patterns (`/01-discovery/synthesis/patterns-analysis.md`)
3. **Final problem statement** draft (`/01-discovery/synthesis/final-problem-statement.md`)
4. **Competitive landscape seed** (`/01-discovery/synthesis/competitive-landscape-seed.md`)

### Due Tuesday April 8 at 23:59 (Team Deliverables)

All lab deliverables above, revised and finalized:

- Affinity map documentation complete with 50+ insights, 5 to 8 clusters, photo evidence
- Pattern analysis with frequency table, pain intensity ratings, Five Whys for top 3 patterns
- Final problem statement citing 8+ interviews with quantified impact
- Competitive landscape seed with all alternatives mentioned by interviewees
- Updated ICP document reflecting what you learned from interviews
- Low-fidelity prototype v1 (paper sketches or Figma wireframes, screenshots in repo)

### Due Tuesday April 8 at 23:59 (Individual: HW1, 5 Points)

Each student individually submits evidence of personally conducting and documenting at least 3 customer discovery interviews. See `GRADING-RUBRIC.md` for full details.

---

## Repository Structure

After Lab 4, your repo should contain these files:

```
/00-foundation/
    team-contract.md
    team-icp.md                          <-- updated based on interviews

/01-discovery/
    interview-script-v1.md
    interview-script-v2.md               <-- refined version
    interview-logs/
        interview-01.md
        interview-02.md
        ...
        interview-10.md                  <-- minimum 10 logs
    synthesis/
        affinity-map.md                  <-- NEW in Lab 4
        affinity-map-photo.jpg           <-- NEW in Lab 4
        patterns-analysis.md             <-- NEW in Lab 4
        final-problem-statement.md       <-- NEW in Lab 4
        competitive-landscape-seed.md    <-- NEW in Lab 4
```

---

## Folder Contents

```
Lab-4/
    README.md                    <-- You are here
    QUICKSTART.md                <-- 2-minute setup guide
    GRADING-RUBRIC.md            <-- Rubrics for team and individual homework
    templates/
        synthesis-readiness-checklist.md
        affinity-map-template.md
        patterns-analysis-template.md
        final-problem-statement-template.md
        competitive-landscape-seed-template.md
        emergency-interview-template.md
    guides/
        affinity-mapping-guide.md
        five-whys-guide.md
        prototype-sketching-guide.md
    examples/
        example-affinity-map.md
        example-patterns-analysis.md
        example-problem-statement.md
        example-competitive-landscape-seed.md
```

---

## Quality Standards

### Affinity Map
- 50 to 80 sticky notes or digital insights extracted
- 5 to 8 distinct clusters identified and labeled
- Each cluster has a clear, descriptive name (not "Cluster 1")
- Photo or export evidence included
- Outlier insights documented

### Pattern Analysis
- Frequency count for each pattern (how many interviews mentioned it)
- Pain intensity rating (1 to 5) with supporting quotes
- Five Whys completed for top 3 patterns
- Patterns ranked by combined frequency and intensity
- Current workarounds documented per pattern

### Problem Statement
- All 5 components present: WHO, WHAT, WHEN/WHERE, WHY, IMPACT
- Cites 8 or more interviews with specific verbatim quotes
- Includes quantified impact (time lost, money spent, frequency)
- Passes the "stranger test": someone outside your team can read it and understand the problem
- Team sign-off with all member names

### Competitive Landscape Seed
- Lists all current solutions, workarounds, and alternatives mentioned by interviewees
- Includes direct competitors, indirect competitors, and manual workarounds
- Each entry has at least one interview quote or reference
- Organized in a table format

---

## Common Mistakes

1. **Affinity map with only 20 notes.** You need 50 to 80. Extract more. Every quote, behavior, frustration, workaround, and desire is a separate note.
2. **Patterns without evidence.** Every pattern must cite specific interview numbers. "Users are frustrated" is not a pattern. "7 of 10 interviewees described wasting 20+ minutes per week on manual scheduling" is a pattern.
3. **Problem statement that reads like a solution pitch.** Your problem statement describes the problem, not your product. If it mentions your app name, it is wrong.
4. **Missing Five Whys.** Surface complaints are not root causes. Keep asking why until you reach the structural reason the problem exists.
5. **No photo evidence for affinity map.** If you did physical sticky notes, photograph the board. If you used Miro, export a high-resolution PNG. No photo means no evidence of the work.

---

## Getting Help

- Raise your hand during lab for instructor checkpoints
- Office hours: book via email for Google Meet
- Email: zeshan.ahmad@kiu.edu.ge
- Review the guides in `guides/` for step-by-step instructions
- Review the examples in `examples/` for what good output looks like

---

## What Comes Next

- **Week 5 Lecture (Thursday April 2):** Analytics Foundations, AARRR framework, event schema design. Quiz 1 happens during this lecture.
- **Lab 5 (Week 5 slot):** Analytics planning and user testing. You will design your event schema and test your prototype with 5+ users.
- **HW1 due Tuesday April 8 at 23:59:** Individual interview contribution log (5 points).
- **Team deliverables due Tuesday April 8 at 23:59:** All synthesis documents finalized.

---

**The quality of your discovery determines the quality of everything that follows. Get this right and the rest of the semester gets easier. Get this wrong and you will spend 10 weeks building something nobody wants.**
