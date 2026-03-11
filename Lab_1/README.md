# Lab 1: Team Formation and Problem Brainstorming

**Course:** CS-PD-2026 Product Development for Software Engineers  
**Instructor:** Zeshan Ahmad | zeshan.ahmad@kiu.edu.ge  
**Office Hours:** Book via email for Google Meet  

| | Group A | Group B |
|---|---|---|
| **Lab Date** | Thursday, March 13, 2026 | Friday, March 14, 2026 |
| **Time** | 14:00 -- 16:00 | 13:00 -- 15:00 |
| **Submission Deadline** | **Thursday, March 19, 2026 at 11:59 PM** | **Thursday, March 19, 2026 at 11:59 PM** |

---

## What This Lab Is About

Lab 1 has one purpose: get your team together and generate a rich, honest pool of candidate problems worth solving.

You will leave this lab without a chosen problem. That is intentional and correct.

In the previous semester we watched teams pick a problem in the first 20 minutes and spend the rest of the semester quietly doubting it. The research on startup failure is clear: teams that rush problem selection build solutions nobody wants. This semester we are engineering a better outcome. You will explore a wide problem space individually today, share what you found with your team, and commit to nothing until you have the Four Filters framework -- which comes in Lab 2.

The single most important output of this lab is a genuine, evidence-based list of problems that real people actually experience, written before your team has had a chance to lobby for any particular direction.

---

## What You Will NOT Do Today

This is as important as the list of deliverables.

- You will **not** select a team problem statement today.
- You will **not** define a single Ideal Customer Profile today.
- You will **not** write an interview script today.
- You will **not** vote on whose problem idea is strongest.

These things happen in Lab 2 after you have learned and applied the Four Filters framework. Any team that submits a committed single problem statement as a Lab 1 deliverable will be asked to redo the work. Premature convergence is not efficiency -- it is the most expensive mistake in product development.

---

## Learning Objectives

By the end of this lab and its associated homework you will be able to:

1. Form a functional team with defined roles and a written operating agreement.
2. Generate problem statements grounded in direct personal observation using the 3H brainstorming framework.
3. Distinguish between a strong, specific, observable problem statement and a weak, vague, or hypothetical one.
4. Set up a professional GitHub repository that will serve as your team's evidence base for the entire semester.
5. Hold multiple candidate problems open simultaneously without collapsing to a single direction under social pressure.

---

## In-Lab Schedule (120 minutes)

| Time | Activity | Output |
|------|----------|--------|
| 0:00 -- 0:20 | Team formation, introductions, role assignment | Team name confirmed, roles assigned |
| 0:20 -- 0:45 | **Individual silent 3H brainstorming** (no cross-talk) | Each person has 3 written problem statements |
| 0:45 -- 1:05 | Round-robin sharing: each person presents, team listens | Team has heard all 9-12 candidate problems |
| 1:05 -- 1:25 | GitHub repository setup and access confirmation | Repo live, all members have push access |
| 1:25 -- 1:50 | Begin drafting `team-contract.md` together | Contract shell committed to GitHub |
| 1:50 -- 2:00 | Wrap-up, deadline confirmation, Lab 2 preview | Open questions answered |

**Important note on the sharing round (0:45 -- 1:05):** Each person presents their 3 problems. The rest of the team listens and may only ask clarifying questions: "Where did you see that?" or "Who specifically is affected?" No voting, no advocating for a favourite, no "that's a great idea." The quality of your Lab 2 Four Filters discussion depends entirely on how honestly and broadly you explore the space today.

---

## Deliverables

### Must Be Committed Before You Leave Lab

| File | Location in Your Repo |
|------|----------------------|
| Repository folder structure (see below) | Root of repo |
| `team-contract.md` (shell with roles filled in) | `00-foundation/team-contract.md` |
| `all-problem-statements.md` (all members' problems present) | `00-foundation/all-problem-statements.md` |

### Must Be Committed by Thursday March 19 at 11:59 PM

| File | Location in Your Repo | Notes |
|------|----------------------|-------|
| `team-contract.md` (fully complete) | `00-foundation/team-contract.md` | All sections filled in |
| `all-problem-statements.md` (polished) | `00-foundation/all-problem-statements.md` | 3H structure, quality bar met |
| `team-icp.md` | `00-foundation/team-icp.md` | Two candidate ICP profiles, one per top problem |
| `milestones/week-02-milestone.md` | `milestones/week-02-milestone.md` | Completed from template |
| `README.md` (updated) | Root | Team names, repo purpose |

---

## Repository Structure

Your team repository must have this folder structure before you leave lab today:

```
product-capstone-2026/
├── README.md
├── .gitignore
├── 00-foundation/
│   ├── team-contract.md
│   └── all-problem-statements.md
├── 01-discovery/
│   └── .gitkeep
└── milestones/
    └── .gitkeep
```

By Thursday March 19 the structure should also include:

```
├── 00-foundation/
│   ├── team-contract.md
│   ├── all-problem-statements.md
│   └── team-icp.md
└── milestones/
    └── week-02-milestone.md
```

Do not create folders beyond this structure today. Folders for design, build, and analytics phases will be introduced in the labs that cover those phases. An empty folder structure with no content creates a false impression of progress and makes the repo harder to navigate for the instructor during grading.

---

## Team Roles

Every team has exactly three roles. A team of four assigns the role with the highest current workload to two people.

| Role | Primary Accountability |
|------|----------------------|
| **Program Lead** | Deadlines, submissions, team health, conflict resolution tiebreaker |
| **Discovery Lead** | Interview quality, synthesis quality, customer insight |
| **Tech Lead** | Repository integrity, code quality, architecture decisions |

If a team member becomes unavailable: Program Lead covers Discovery Lead's work; Discovery Lead covers Tech Lead's; Tech Lead covers Program Lead's.

Each role is documented in your team contract and in your repository `README.md`. Roles are not cosmetic titles -- they determine who is accountable if something is missing at grading time.

---

## The 3H Brainstorming Framework

You were introduced to 3H in Thursday's lecture. Here is the reference version for lab use.

Each person generates **exactly three problem statements**, one for each H:

**Hairband** -- A problem you personally live with. Something in your own daily life that is genuinely annoying, that you have learned to work around or accept. The bar is low: it does not have to be a billion-dollar opportunity. It just has to be real and yours.

**Headache** -- A problem you have directly observed in someone else. A friend, family member, classmate, or colleague who struggles with something repeatedly. You have witnessed the frustration firsthand, not read about it in an article.

**Heartburn** -- A problem that keeps recurring in a context you understand: your university, your community, your industry, a domain you have worked in. Something that causes ongoing pain for a recognisable group of people, not just one person on one occasion.

The rule that makes this framework work: **every problem statement must trace back to something you have personally seen or experienced.** AI-generated problems, problems sourced from blog posts, and problems you invented because they sounded commercially impressive all fail the quality bar. They will be returned without grade credit.

For worked examples and common failure modes, see `resources/3h-framework.md`.

---

## Problem Statement Quality Bar

**Weak:** "Students have trouble with group projects."

**Strong:** "Third-year CS students at KIU lose an average of four hours per deadline week chasing down teammates who went silent on the group chat after accepting a task."

The difference is specificity. A strong Lab 1 problem statement answers:
- **Who** exactly is affected (specific segment, not a broad category)
- **What** specifically happens (a behaviour or failure mode, not an abstract concept)
- **When and where** the problem occurs
- **Why it matters** to the person who experiences it

You do not need to achieve all four dimensions perfectly today. The closer you get, the more productive your Lab 2 discussion will be. See `resources/problem-statement-quality-bar.md` for a calibration guide.

---

## Submitting Your Work

Submission is via your team GitHub repository. There is no LMS upload required.

For the in-lab commit:
```bash
git add 00-foundation/ milestones/ README.md .gitignore
git commit -m "[LAB-1] Initial repository structure, team formation, problem brainstorm"
git push origin main
```

For the final deadline submission on Thursday March 19:
```bash
git add .
git commit -m "[LAB-1] Complete submission: contract, problem statements, ICP candidates, milestone"
git tag lab-1-submission
git push origin main --tags
```

Then email zeshan.ahmad@kiu.edu.ge with:
- Your team name
- Your repository URL
- Confirmation that the `lab-1-submission` tag is visible on GitHub

---

## Getting Help

**During lab:** The instructor runs checkpoint rounds at 30 min, 60 min, and 105 min. Raise your hand at any point.

**After lab:** Book a Google Meet slot via email. Do not wait until the day before the deadline -- contact early and the problem is almost always solvable.

**Common situations:**

*"We already know what we want to build."* Write it as a Heartburn statement and also generate your other two H's. You may feel differently after running it through Four Filters in Lab 2. Many teams that felt certain in Lab 1 pivoted twice by Week 4.

*"One person's problems are much stronger."* Every person still submits three. The diversity of the pool is the point. A weak problem from one person often triggers the team's best idea when viewed differently in Lab 2.

*"We cannot agree on which problems to explore further."* Correct. You are not supposed to agree yet. Write all of them down. The Four Filters framework in Lab 2 is specifically designed to create a structured, evidence-based convergence conversation.

---

## What Comes Next

| When | What |
|------|------|
| Thursday Mar 12 (done) | Week 2 lecture: Customer Discovery, Mom Test, JTBD, 3H, Four Filters, problem quality bar |
| **This lab** | Team formation, 3H brainstorm, GitHub setup, contract draft |
| Due Thu Mar 19 | Polished contract, problem statements, two-candidate ICP, milestone doc |
| Thu Mar 19 | Week 3 lecture: ICP deep-dive, problem validation, interview script theory |
| Thu Mar 20 / Fri Mar 21 | **Lab 2:** team selects one problem via Four Filters, commits ICP, writes interview script v1 |
| Week 4 | **Checkpoint 1 (10 points):** 10+ interview logs, affinity map, final evidence-based problem statement |

---

## File Index

| File | What It Is |
|------|-----------|
| `README.md` | This document |
| `QUICKSTART.md` | 2-minute reference card for lab day |
| `INSTRUCTOR-GUIDE.md` | Word-for-word instructor script |
| `GRADING-RUBRIC.md` | Full grading rubric |
| `templates/team-contract-template.md` | Fill-in team contract |
| `templates/all-problem-statements-template.md` | 3H brainstorming template |
| `templates/team-icp-candidates-template.md` | Two-candidate ICP template |
| `resources/3h-framework.md` | Full 3H guide with examples |
| `resources/problem-statement-quality-bar.md` | Strong vs. weak calibration guide |
| `resources/github-setup-guide.md` | Step-by-step repository setup |
| `examples/example-team-contract.md` | Completed example contract |
| `examples/example-problem-statements.md` | Completed example 3H statements |
| `examples/example-icp-candidates.md` | Completed example two-candidate ICP |

---

*CS-PD-2026 | Kutaisi International University | Spring 2026*
