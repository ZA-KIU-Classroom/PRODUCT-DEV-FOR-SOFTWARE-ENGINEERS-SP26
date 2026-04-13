# Team Development Process Map

**Team:** [Your Team Name]  
**Product:** [Your Product Name]  
**Last Updated:** [Date]  
**Version:** 1.0

---

## Overview

This document describes how work flows through our team from idea to deployed increment. It is the operational agreement all team members commit to for the duration of the sprint arc. If a process step is unclear, this document is the source of truth.

---

## Scrum Roles

| Role | Name | Responsibilities |
|------|------|-----------------|
| Product Owner | [Name] | Owns and orders the backlog. Accepts or rejects sprint increments. Reviews AI-generated features against user interview evidence. |
| Scrum Master (Sprint 1) | [Name] | Facilitates standups, planning, review, and retrospective. Runs AI output review at each standup. Maintains ai-usage-log.md currency. |
| Scrum Master (Sprint 2) | [Name] | [Rotates after Sprint 1] |

---

## Story Lifecycle

A story moves through these states. Only the state changes listed below are permitted -- a story cannot skip states.

```
Backlog → Refined → Sprint Backlog → In Progress → In Review → Done
```

| State | Meaning | Who Sets It |
|-------|---------|------------|
| Backlog | Exists but not yet ready for a sprint | PO |
| Refined | Has a user story, AC, story points, and interview evidence. Ready to be committed to a sprint. | PO after team refinement |
| Sprint Backlog | Committed to the current sprint. Developer and AI tool assigned. | SM after Sprint Planning |
| In Progress | Developer has started work | Developer who pulled the story |
| In Review | PR raised. Awaiting human review. | Developer |
| Done | All DoD criteria met. PO has confirmed AC. Merged to main. | PO |

---

## Definition of Done

A story is Done when every item below is confirmed:

- [ ] Code reviewed by at least one team member who is not the original author
- [ ] Pull request merged to `main` via GitHub PR -- no direct pushes to main
- [ ] Acceptance criteria confirmed as met by the Product Owner -- not by the developer who built it
- [ ] If AI-generated: all AI-generated code is annotated with comments explaining the logic
- [ ] If AI-generated: entry added to `docs/ai-usage-log.md`
- [ ] Feature works in the deployed environment (not just locally on the developer's machine)
- [ ] No new known bugs introduced to the main branch

A story that is "mostly done" or "done except for one thing" is not Done. It remains In Review.

---

## AI Review Process

All team members use AI tools. The following process applies to every piece of AI-generated output before it is committed.

### Review Steps

1. **Generate:** Developer uses the designated AI tool for the story.
2. **Read every line:** Developer reads the entire output before accepting any of it. No Tab-to-accept without reading.
3. **Check against AC:** For every acceptance criterion, confirm the generated output produces a pass result. If any AC fails, edit the output until it passes.
4. **Security and privacy check:** For any endpoint, form, or data-handling code, confirm no security vulnerability and no PII in logs or storage.
5. **Annotate:** Add inline comments to AI-generated blocks explaining the logic in the developer's own words.
6. **Log:** Add an entry to `docs/ai-usage-log.md` before raising the PR.
7. **PR review:** The human reviewer checks the annotation and the log entry as part of their review. A PR from AI-generated code with no annotation is returned without merge.

### AI Tool Assignment

| Story Type | Default AI Tool | Why |
|-----------|----------------|-----|
| UI screens and components | Google Stitch | Fastest path from AC to working UI |
| Complex multi-file backend logic | Claude Code | Best at understanding codebase context |
| AI features (chatbot, summariser, classifier) | Google AI Studio | Prompt prototyping before API integration |
| Boilerplate, repetitive patterns, docstrings | GitHub Copilot | Ambient completion -- always on |

Tool assignments are made at Sprint Planning. Developers can change the tool during execution if a better choice emerges. The change must be noted in the ai-usage-log.md entry.

---

## Branching and Pull Request Process

### Branch Naming

```
feature/[story-id]-[short-description]
fix/[story-id]-[short-description]
```

Examples:
```
feature/s1-01-user-signup-screen
fix/s1-02-booking-confirmation-redirect
```

### PR Process

1. Developer opens PR to `main` when the story is In Review
2. PR title: `[Story ID] Short description`
3. PR description must include:
   - Story ID and full user story
   - AC checklist (mark each AC as passed or failed with evidence)
   - AI tool used and summary of review (or "No AI used")
   - Screenshots or GIF of the working feature in the deployed environment
4. One team member reviews and approves
5. PO confirms AC met (can be done in PR comments or at standup)
6. Reviewer merges -- not the original developer

### No direct pushes to main

Any commit pushed directly to `main` without a PR review is a process violation. The SM flags it in the next standup.

---

## Standup Format

**Cadence:** [Daily / Every 2 days -- specify]  
**Location:** [Slack channel name / GitHub Issues / other]  
**Time:** [HH:MM] every [day(s)]  
**Format:**

```
Yesterday: [What I completed -- be specific, include story ID]
Today: [What I am working on -- include story ID]
Blocker: [Anything stopping me -- or "none"]
AI note: [What AI generated yesterday. Accepted / modified / discarded percentage.]
```

**Who posts:** Every team member posts independently. The SM does not chase individuals after [time] -- if a member has not posted by [time], the SM flags it in the next standup as a process issue.

---

## Blocker Resolution

| Blocker Type | First Action | If Unresolved After 24h |
|-------------|-------------|------------------------|
| Technical (code, environment) | Post in standup with specific description | SM escalates to whole team in [channel] |
| Dependency on another story | Flag in PR or standup | SM reprioritises or re-assigns the blocking story |
| AI tool failure or hallucination | Note in ai-usage-log.md, try alternative tool | Bring to next standup for team decision |
| External dependency (API, third party) | Note in risk register | PO adjusts sprint scope if unresolved by Day 5 |

---

## Sprint Ceremonies: Who Does What

| Ceremony | Facilitator | Required Attendees | Output |
|----------|------------|-------------------|--------|
| Sprint Planning | Scrum Master | All team members | Committed sprint backlog with AC, assignees, AI tools |
| Daily Standup | Async -- no facilitator | All team members post | Blockers surfaced, coordination confirmed, AI output reviewed |
| Sprint Review | Product Owner | All team members | PO accepts or rejects each story. Backlog updated. |
| Retrospective | Scrum Master | All team members | 1 to 3 concrete process changes for next sprint |

---

## ai-usage-log.md Entry Format

All AI-assisted work is logged in `docs/ai-usage-log.md`. This is audited at Checkpoint 3.

```
---
Date: YYYY-MM-DD
Story: [Story ID] -- [Story summary]
Tool: [Google Stitch / Claude Code / GitHub Copilot / Google AI Studio]
Task: [What the AI was asked to generate or assist with]
Prompt summary: [Brief description of the prompt used]
Files changed: [List of files the AI output touched]
Result: Accepted / Modified / Discarded
Review notes: [What specifically was checked. What was changed from the AI output. Any errors or hallucinations found.]
Reviewer: [Name]
---
```

---

## Change Log

| Date | Version | Changes | Author |
|------|---------|---------|--------|
| [Date] | 1.0 | Initial process map | [Name] |

---

*Process Map | [Team Name] | CS-PD-2026 | Spring 2026*
