# Lab 6: Product Roadmap and Sprint Planning

**Course:** CS-PD-2026 | Product Development for Software Engineers  
**Instructor:** Zeshan Ahmad | zeshan.ahmad@kiu.edu.ge  
**Group A:** Thursday 16 April 2026 | 14:00 to 16:00  
**Group B:** Friday 17 April 2026 | 13:00 to 15:00  
**Deadline:** Wednesday 22 April 2026 at 23:59

---

## What This Lab Is About

You have completed discovery. You understand your user. You have a problem statement backed by 10 or more interviews, a value proposition, and a prototype direction from Lab 5. You have also just sat through a lecture on Agile and Scrum, estimation, sprint ceremonies, and AI-assisted development.

Now you plan the build.

Lab 6 is a planning lab. By the end of these two hours your team will have made every major product decision needed to start Sprint 1 in Lab 8. You will define what your MVP actually is, plan the eight-week development arc across four sprints, write your Sprint 1 backlog with real user stories and acceptance criteria, and map the workflow your team will follow from story pulled to story shipped.

This is not busywork. Teams that arrive at Lab 8 without a real sprint plan do not start Sprint 1. They spend the first hour of every sprint arguing about what to build. You are doing that work now so that Lab 8 is purely execution.

---

## What You Have Coming In

Before Lab 6 starts, your team should have:

- [ ] Final problem statement committed to repo
- [ ] 10 or more interview logs in `01-discovery/interview-logs/`
- [ ] Patterns analysis and final problem statement in `01-discovery/synthesis/`
- [ ] JTBD statement and value proposition canvas from Checkpoint 1
- [ ] North Star Metric drafted in `03-build/analytics/north-star-metric.md` (from Lab 5)
- [ ] Event schema draft in `03-build/analytics/event-schema.md` (from Lab 5)
- [ ] Stitch prototype link in `02-design/prototypes/high-fidelity/stitch-prototype-link.md` (from Lab 5)
- [ ] HW1 individual interview logs submitted by Thursday 16 April at 23:59

If any of these are missing, do not wait until the lab to sort it out. Email the instructor before arriving.

---

## Learning Objectives

By the end of this lab, your team will:

1. Define your MVP scope with an explicit in-scope and out-of-scope boundary
2. Write 8 to 12 user stories that are interview-evidence-backed and INVEST-compliant
3. Assign story points to all Sprint 1 stories using the Fibonacci scale
4. Write acceptance criteria for every Sprint 1 story in Given-When-Then format
5. Build an 8-week product roadmap across four sprints with realistic capacity
6. Document your team's AI-assisted development workflow as a process map
7. Assign AI tools per story in your Sprint 1 backlog before work begins

---

## Lab Timeline (120 minutes)

| Time | Activity | Output |
|------|----------|--------|
| 0:00 to 0:15 | Part 1: MVP scope definition | MVP boundary documented |
| 0:15 to 0:45 | Part 2: User story writing and estimation | 8 to 12 stories with points |
| 0:45 to 1:15 | Part 3: Product roadmap and sprint allocation | 8-week roadmap committed |
| 1:15 to 1:45 | Part 4: Sprint 1 planning in full | Sprint 1 backlog with AC |
| 1:45 to 2:00 | Part 5: Process map and commit | All files committed to GitHub |

---

## Part 1: MVP Scope Definition (0:00 to 0:15)

### Why This Comes First

Every team that tries to build everything ends up shipping nothing. Your MVP is the minimum set of features that allows a real user to experience the core value your product promises. Defining the boundary now prevents scope creep from the first commit.

This is a product decision, not a technical one. The Product Owner makes the call. The team can debate for 10 minutes. After that the PO decides and you move on.

### The MVP Boundary Test

For every feature your team considers, apply this test:

**Question 1: Does a user need this feature to reach the activation moment?**
If no, it is not in the MVP. Put it in Sprint 2 or Sprint 3.

**Question 2: Is there interview evidence that users want this feature?**
If you invented the feature without interview support, it is not in the MVP. Put it in a future phase and note that it needs validation.

**Question 3: Can your team build this in the 8-week sprint arc?**
If honest estimation puts it beyond Sprint 4, it is not in the MVP. Be honest now rather than discovering this in Sprint 3.

### How to Structure Your MVP Definition

Write it in three lists:

**In scope (Sprint 1 to Sprint 4):**
Features a user needs to reach the activation moment and return. These go in your roadmap.

**Out of scope (MVP phase):**
Features that are desirable but not required for the activation moment. These go on the backlog for after the course ends or after Demo Day.

**Explicitly rejected:**
Features that came up in discovery but do not match the problem you are solving. Document why you rejected them. Auditors at Checkpoint 2 check this. Teams that cannot explain what they decided NOT to build look like they never thought seriously about scope.

### Deliverable

There is no standalone template for MVP scope. Capture it in the header of your `03-build/roadmap/product-roadmap.md` before you build the roadmap. The roadmap template at `templates/product-roadmap-template.md` has the MVP scope section built in.

---

## Part 2: User Story Writing and Estimation (0:15 to 0:45)

### What a User Story Is

A user story is not a task. It is a value statement written from the user's perspective:

```
As a [type of user], I want [some goal] so that [some reason].
```

The reason clause is not optional. It tells every team member why the feature exists. When a developer is building and hits an ambiguity, the reason clause resolves it. If you cannot write the reason clause, you do not understand why you are building the feature.

### INVEST Criteria

Every story must pass all six INVEST tests before it enters the backlog:

| Letter | Criterion | Test |
|--------|-----------|------|
| I | Independent | Can this story be built without depending on another story being done first? |
| N | Negotiable | Is the implementation detail flexible, not locked? |
| V | Valuable | Does completing this story deliver visible value to a user? |
| E | Estimable | Can the team put a story point number on it with confidence? |
| S | Small | Can this story be completed within a single sprint by one or two developers? |
| T | Testable | Can you write acceptance criteria that produce a pass or fail result? |

If a story fails any INVEST criterion, rewrite it or split it before it enters the backlog.

### Evidence Requirement

Every story in your MVP backlog must trace back to an interview. You do not need to quote the interview verbatim in the story, but you must be able to answer: which interview revealed the need for this feature? If you cannot answer that, the story should not be in your MVP.

Write the interview reference as a comment in your sprint plan:

```
Source: Interview 4 (student, Kutaisi, March 2026) -- "I always waste time searching for a space that turns out to be full."
```

### Story Points

Use the Fibonacci scale: 1, 2, 3, 5, 8, 13, 21.

- **1 point:** A single, obvious change. One file. No logic complexity.
- **3 points:** A clear feature with a defined implementation path. Some edge cases.
- **5 points:** A non-trivial feature requiring multiple components or integration.
- **8 points:** A complex feature with significant uncertainty. Consider splitting.
- **13+:** This story needs to be split before it enters a sprint.

**With AI tools on your team:** Estimate the full cycle, not just the generation step. A story that Stitch generates in 10 minutes still requires review, testing, edge case handling, and PO acceptance. A story that takes 10 minutes to generate and 3 hours to review is a 3-point story, not a 1-point story.

**Calibration anchor for your team:** Before estimating your backlog, agree on one 1-point story, one 3-point story, and one 5-point story as anchors. All subsequent estimates are relative to those anchors.

### How Many Stories

For an 8-week, 4-sprint MVP with a 3 to 4 person team using AI tools:

- Total backlog: 20 to 30 stories
- Sprint 1 commitment: 8 to 14 story points (calibrate after Sprint 1)
- Stories per sprint: typically 4 to 7

Write your full backlog in Part 2. Allocate stories to sprints in Part 3.

### Deliverable

Write all user stories in `03-build/roadmap/sprint-1-plan.md` (Sprint 1 stories with full detail) and reference the full backlog allocation in `03-build/roadmap/product-roadmap.md`. Use `templates/sprint-plan-template.md` for Sprint 1.

---

## Part 3: Product Roadmap (0:45 to 1:15)

### The Four-Sprint Structure

Your MVP development runs across four two-week sprints. This is fixed by the course calendar:

| Sprint | Dates | Theme |
|--------|-------|-------|
| Sprint 1 | Apr 24 to May 7 | Foundation -- core user flow working end to end |
| Sprint 2 | May 8 to May 21 | Instrumentation and data -- analytics live, usability tested |
| Sprint 3 | May 22 to Jun 4 | Growth features and polish -- experiments running |
| Sprint 4 | Jun 5 to Jun 11 | Demo Day preparation -- pitch-ready, repo complete |

**Note on Sprint 1 and the midterm:** Sprint 1 development begins in Lab 8 on April 24th. The midterm exam is April 30th. Sprint 1 does not pause for the midterm. Teams maintain async standup cadence and continue committing code during midterm week. This is not optional.

### Sprint Themes

Each sprint has a theme that describes what the user can do by the end of that sprint. Write the theme as a user-facing capability statement, not a technical task list.

**Strong theme:** "By the end of Sprint 1, a user can sign up, complete the core action, and see a confirmation that proves the action happened."

**Weak theme:** "In Sprint 1 we will build the backend and frontend."

The theme is what you demo at Sprint Review. If you cannot demo it live in front of the instructor, the sprint did not close.

### Capacity Planning

For a 3 to 4 person team using AI tools, do not commit to more than 60% of theoretical maximum capacity per sprint. Buffer exists for:

- AI output review time (always non-zero)
- Blockers and dependencies
- Checkpoint 2 submission work (due April 22nd, before Sprint 1 begins)
- Midterm preparation (Sprint 1 overlaps with midterm week)

A team that over-commits Sprint 1 and fails to deliver demoable software has no velocity data for Sprint 2. That cascades to Demo Day.

### Roadmap Format

The roadmap must contain for each sprint:

1. Sprint goal in one sentence
2. User-facing capability statement (the demo)
3. List of user stories allocated to this sprint with point values
4. Sprint capacity calculation (points committed vs theoretical max)
5. Key risks for this sprint
6. Checkpoint or milestone alignment

Use `templates/product-roadmap-template.md`.

### High-Fidelity Prototype Iteration

Lab 6 also includes iterating your high-fidelity prototype from Lab 5 based on the critique feedback you received. This is not a separate major workstream -- it is 15 to 20 minutes of work. Use the final 20 minutes of Part 3 to:

1. Open your Stitch prototype
2. Apply the top 1 to 2 pieces of critique feedback
3. Update the Stitch link in `02-design/prototypes/high-fidelity/stitch-prototype-link.md` with the revised version

If your Stitch prototype is already solid, use this time to confirm it maps correctly to your Sprint 1 user stories. Every story in Sprint 1 should have a corresponding screen or flow in the prototype.

### Deliverable

`03-build/roadmap/product-roadmap.md` — completed using `templates/product-roadmap-template.md`.

---

## Part 4: Sprint 1 Planning in Full (1:15 to 1:45)

### This Is Your Most Important 30 Minutes

Sprint 1 begins in Lab 8 on April 24th. Every story in your Sprint 1 backlog must be ready for a developer to pull and start immediately. A story is ready when it has:

- A clear user story in As a / I want / So that format
- Acceptance criteria in Given-When-Then format (minimum 2 AC per story)
- A story point estimate agreed by the team
- A named developer assigned
- An AI tool noted if the story will use one

A story without acceptance criteria is not in the sprint. It is on the backlog. Do not commit it until it has AC.

### Writing Acceptance Criteria

Use Given-When-Then format without exception:

```
Given [some context],
When [some action occurs],
Then [some observable outcome].
```

Each AC must be falsifiable. You can run a test that either passes or fails. If it contains the words "should work well" or "looks nice" or "is fast" without a specific threshold, it is not an AC. Rewrite it.

**Minimum AC per story:** 2
**Recommended:** 3 to 4 for any story that touches the activation flow

### AI Tool Assignment

For every story in Sprint 1, note which AI tool will be used. This goes in the sprint plan before work begins, not after.

| Story | AI Tool | Why |
|-------|---------|-----|
| Build onboarding screen | Google Stitch | UI generation from AC prompt |
| Set up authentication endpoint | Claude Code | Multi-file backend logic |
| Integrate event tracking | GitHub Copilot | Boilerplate instrumentation code |
| Build AI feature (if applicable) | Google AI Studio | Prompt prototyping first |

This is a planning decision, not an implementation constraint. The developer can change the tool if a better choice emerges. But having no tool assignment means the developer starts cold on Day 1 of the sprint.

### Sprint 1 Ceremony Assignments

Before you leave Lab 6, assign the following for Sprint 1:

- **Product Owner:** [Name] -- owns the Sprint 1 backlog, accepts or rejects stories at Sprint Review
- **Scrum Master:** [Name] -- facilitates standups, runs Sprint Planning in Lab 8, runs Retrospective after Sprint 1
- **Standup cadence:** [Async via GitHub Issues / Slack / other -- specify channel and time]
- **Sprint Review date:** Week 10 lecture session (May 7th, Google Meet -- instructor abroad)
- **Sprint 1 Retrospective date:** To be confirmed

Document all of this in your `03-build/roadmap/sprint-1-plan.md`.

### Deliverable

`03-build/roadmap/sprint-1-plan.md` -- completed using `templates/sprint-plan-template.md`. Every story has a user story, AC, point estimate, assignee, and AI tool note.

---

## Part 5: Process Map and Commit (1:45 to 2:00)

### Process Map

Your process map is the written agreement between team members on how work flows from idea to shipped increment. It does not need to be long. It needs to be specific enough that a new team member could follow it without asking anyone questions.

It must cover:

- How a story moves from backlog to in-progress to done
- Who reviews AI-generated code before it is merged
- What the Definition of Done is for your team (use the AI edition from today's lecture)
- How blockers are communicated
- Where standups happen and when
- How the ai-usage-log.md gets updated

Write it in `03-build/workflow/process-map.md`. Use `templates/process-map-template.md`.

### Commit Checklist

Before you leave lab, every team must commit:

```
03-build/roadmap/product-roadmap.md          (required)
03-build/roadmap/sprint-1-plan.md            (required)
03-build/workflow/process-map.md             (required)
02-design/prototypes/high-fidelity/stitch-prototype-link.md  (update with revised prototype)
```

Use this commit message:
```
[LAB-6] roadmap, sprint 1 plan, process map
```

Tag the commit:
```
git tag lab-6-submission
git push origin lab-6-submission
```

---

## Deliverables Summary

| File | Path | Due |
|------|------|-----|
| Product Roadmap | `03-build/roadmap/product-roadmap.md` | Wednesday 22 April at 23:59 |
| Sprint 1 Plan | `03-build/roadmap/sprint-1-plan.md` | Wednesday 22 April at 23:59 |
| Process Map | `03-build/workflow/process-map.md` | Wednesday 22 April at 23:59 |
| Stitch Prototype (revised) | `02-design/prototypes/high-fidelity/stitch-prototype-link.md` | Wednesday 22 April at 23:59 |

All of the above are also required inputs to **Checkpoint 2 (10 points)** due Wednesday 22 April at 23:59.

---

## Connection to Checkpoint 2

Checkpoint 2 is due the same night as the Lab 6 deadline: Wednesday 22 April at 23:59.

The Lab 6 deliverables form the Product Roadmap section of Checkpoint 2 (2 points). The technical architecture package you build in Lab 7 (same day, different session) forms the Technical Architecture section (4 points). Your Stitch prototype and usability findings form the Prototype section (4 points).

Everything you produce today feeds directly into Wednesday's submission. Do not treat Lab 6 and Checkpoint 2 as separate workstreams. They are the same workstream.

---

## Grading

Lab 6 participation is assessed on in-lab output quality observed during the session.

| Component | What We Look For |
|-----------|-----------------|
| MVP scope | Clear in-scope and out-of-scope boundary. Rejections explained. Product Owner can defend every decision. |
| User stories | Stories follow As a / I want / So that format. INVEST criteria met. Interview evidence cited per story. |
| Story points | Fibonacci scale used. Calibration anchors agreed. Points reflect complexity not hours. AI review time included. |
| Product roadmap | Four sprints with themes, stories allocated, capacity calculated. Sprint 1 commitment is realistic. |
| Sprint 1 plan | Every story has AC in Given-When-Then format. Minimum 2 AC per story. AI tool assigned per story. |
| Process map | Definition of Done documented. AI review process described. Standup cadence committed. |
| GitHub commit | All required files committed with correct paths and commit message before leaving lab. |

---

## Getting Help

**During lab:** Raise your hand. The instructor circulates every 15 minutes.

**Story point debates:** If your team cannot agree on an estimate, run Planning Poker. If still deadlocked after two rounds, take the higher estimate and note the uncertainty in the sprint plan.

**Scope debates:** If your team cannot agree on whether something is in the MVP, apply the boundary test from Part 1. If it fails Question 1 (user does not need it to reach activation moment), it is out of scope.

**After lab:** Email zeshan.ahmad@kiu.edu.ge with subject line `[LAB-6] [Your Team Name] question`. Office hours available via Google Meet booked by email.

---

*Lab 6 | CS-PD-2026 | Spring 2026 | Kutaisi International University*
