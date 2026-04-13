# Sprint 1 Plan

**Team:** [Your Team Name]  
**Product:** [Your Product Name]  
**Sprint:** 1 of 4  
**Dates:** April 24 to May 7 2026  
**Product Owner:** [Name]  
**Scrum Master:** [Name]  
**Version:** 1.0

---

## Sprint Goal

[One sentence. What can a real user do by the end of Sprint 1 that they could not do before? Write this as a user-facing capability, not a technical milestone.]

Example: "A user can sign up, complete a study space booking, and receive a confirmation -- end to end -- in a deployed application."

---

## Sprint Ceremonies

| Ceremony | When | Where | Who Facilitates |
|----------|------|-------|----------------|
| Sprint Planning | Lab 8, Apr 24/25 | In person | Scrum Master |
| Daily Standup | [Time] every [day(s)] | [Slack channel / GitHub Issues / other] | Async -- each member posts |
| Sprint Review | Week 10, May 7 (Google Meet) | Google Meet | Product Owner |
| Retrospective | May 7 or 8 | [Location] | Scrum Master |

**Async standup format:**
```
Yesterday: [what I completed]
Today: [what I am working on]
Blocker: [anything stopping me -- or "none"]
AI note: [what AI generated yesterday and whether it was accepted/modified/discarded]
```

**Blocker escalation:** If a blocker is not resolved within 24 hours, [Name] pings the team in [channel].

---

## Definition of Done

A story is Done when all of the following are true:

- [ ] Code reviewed by at least one other team member (not the original author)
- [ ] Pull request merged to `main` via GitHub PR -- no direct pushes to main
- [ ] Acceptance criteria confirmed as met by the Product Owner
- [ ] If AI-generated: code annotated with comments explaining the logic
- [ ] If AI-generated: entry added to `docs/ai-usage-log.md` (tool, task, files changed, review notes)
- [ ] Feature works in the deployed environment, not just locally
- [ ] No known bugs introduced into the main branch

---

## Calibration Anchors

Agree these before estimating any stories.

| Points | What It Looks Like for Our Team |
|--------|--------------------------------|
| 1 | [A single, obvious change. One file. No logic complexity. Example: change a button label.] |
| 3 | [A clear feature with a defined path. Some edge cases. Example: add a form with validation.] |
| 5 | [A non-trivial feature requiring multiple components or a third-party integration.] |
| 8 | [A complex feature with significant uncertainty. Consider splitting before committing.] |

---

## Sprint 1 Backlog

### Story S1-01

**User Story:**  
As a [type of user], I want [goal] so that [reason].

**Interview Evidence:**  
Source: Interview [#] ([participant description], [date]) -- "[verbatim quote or close paraphrase]"

**Story Points:** [n]  
**Assignee:** [Name]  
**AI Tool:** [Google Stitch / Claude Code / GitHub Copilot / Google AI Studio / None]  
**AI Tool Rationale:** [One sentence -- why this tool for this story?]

**Acceptance Criteria:**

```
AC1:
Given [context],
When [action],
Then [observable outcome].

AC2:
Given [context],
When [action],
Then [observable outcome].

AC3 (if needed):
Given [context],
When [action],
Then [observable outcome].
```

**Notes:** [Any implementation notes, dependencies, or technical considerations]

---

### Story S1-02

**User Story:**  
As a [type of user], I want [goal] so that [reason].

**Interview Evidence:**  
Source: Interview [#] -- "[quote or paraphrase]"

**Story Points:** [n]  
**Assignee:** [Name]  
**AI Tool:** [Tool]  
**AI Tool Rationale:** [One sentence]

**Acceptance Criteria:**

```
AC1:
Given [context],
When [action],
Then [observable outcome].

AC2:
Given [context],
When [action],
Then [observable outcome].
```

**Notes:** [Notes]

---

### Story S1-03

**User Story:**  
As a [type of user], I want [goal] so that [reason].

**Interview Evidence:**  
Source: Interview [#] -- "[quote or paraphrase]"

**Story Points:** [n]  
**Assignee:** [Name]  
**AI Tool:** [Tool]  
**AI Tool Rationale:** [One sentence]

**Acceptance Criteria:**

```
AC1:
Given [context],
When [action],
Then [observable outcome].

AC2:
Given [context],
When [action],
Then [observable outcome].
```

**Notes:** [Notes]

---

### Story S1-04

**User Story:**  
As a [type of user], I want [goal] so that [reason].

**Interview Evidence:**  
Source: Interview [#] -- "[quote or paraphrase]"

**Story Points:** [n]  
**Assignee:** [Name]  
**AI Tool:** [Tool]  
**AI Tool Rationale:** [One sentence]

**Acceptance Criteria:**

```
AC1:
Given [context],
When [action],
Then [observable outcome].

AC2:
Given [context],
When [action],
Then [observable outcome].
```

**Notes:** [Notes]

---

### Story S1-05 (if applicable)

**User Story:**  
As a [type of user], I want [goal] so that [reason].

**Interview Evidence:**  
Source: Interview [#] -- "[quote or paraphrase]"

**Story Points:** [n]  
**Assignee:** [Name]  
**AI Tool:** [Tool]  
**AI Tool Rationale:** [One sentence]

**Acceptance Criteria:**

```
AC1:
Given [context],
When [action],
Then [observable outcome].

AC2:
Given [context],
When [action],
Then [observable outcome].
```

---

## Sprint 1 Summary

| Story ID | Summary | Points | Assignee | AI Tool | Status |
|----------|---------|--------|----------|---------|--------|
| S1-01 | | | | | Not started |
| S1-02 | | | | | Not started |
| S1-03 | | | | | Not started |
| S1-04 | | | | | Not started |
| S1-05 | | | | | Not started |
| **Total** | | **[n]** | | | |

**Capacity check:** [n] points committed out of approximately [n] maximum ([n]% -- target 60% or below)

---

## Sprint Review Criteria

At Sprint Review (May 7, Google Meet), the team will demo:

1. [Specific screen or flow from Sprint 1 goal]
2. [Specific screen or flow]
3. [What the PO will accept or reject]

The demo must be live. No screenshots. No pre-recorded video. The application runs in front of the reviewer.

---

## AI Usage Log Reference

All AI-assisted work in Sprint 1 must be logged in `docs/ai-usage-log.md`.

Entry format:
```
Date: [YYYY-MM-DD]
Story: [Story ID and summary]
Tool: [Tool name]
Task: [What AI was asked to do]
Files changed: [List of files]
Accepted / Modified / Discarded: [Which]
Review notes: [What was checked, what was changed from the AI output]
Reviewer: [Name]
```

---

## Change Log

| Date | Changes | Author |
|------|---------|--------|
| [Date] | Sprint 1 plan created | [Name] |

---

*Sprint 1 Plan | [Team Name] | CS-PD-2026 | Spring 2026*
