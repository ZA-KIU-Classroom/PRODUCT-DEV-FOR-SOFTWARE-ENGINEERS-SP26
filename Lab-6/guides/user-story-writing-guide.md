# User Story Writing Guide

**Course:** CS-PD-2026 | Spring 2026  
**For use in:** Lab 6 and all subsequent sprint planning sessions

---

## What a User Story Is

A user story is a value statement written from the user's perspective. It is not a task. It is not a technical specification. It is the smallest unit of work that delivers visible value to a real user.

**Format:**
```
As a [type of user],
I want [some goal]
so that [some reason].
```

Every part of this format is required. The So that clause is not optional. It tells every team member why the feature exists. When a developer is building and hits an ambiguity, the So that clause resolves it. If you cannot write it, you do not understand why you are building this feature. Do not put the story in the backlog until you can.

---

## INVEST Criteria

Every story must pass all six INVEST tests before it enters the backlog. Check each one explicitly.

### Independent

The story can be developed without depending on another story being Done first.

**Test:** Can a developer pull this story from the backlog and start work immediately, without waiting for another story to finish?

If the answer is no, either reorder the stories so the dependency is explicit, or merge them into one story.

**Example of a dependency problem:**
- S1-01: Build the booking screen
- S1-02: Build the booking confirmation (depends on S1-01)

S1-02 is not independent. Either merge it into S1-01 as a larger story or make the dependency explicit in the sprint plan so S1-02 is not started until S1-01 is Done.

### Negotiable

The implementation detail is flexible. The story states what the user wants, not how to build it.

**Test:** Does this story specify a technical approach? If so, remove it. The developer decides how to build; the PO decides what to build.

**Too prescriptive:** "As a user I want the booking form to use a PostgreSQL database with a REST API."
**Correct:** "As a user I want to submit a booking so that I receive a confirmation immediately."

### Valuable

Completing this story delivers visible value to a real user.

**Test:** If this story was the only thing shipped in the sprint, would a user notice the improvement? Would they care?

Technical stories (set up the database, configure the CI/CD pipeline) are not user stories. They are tasks. They belong in the sprint as technical tasks, not as user stories. They do not count toward your story point commitment the same way.

### Estimable

The team can put a Fibonacci number on it with confidence.

**Test:** After reading this story, can every team member give an estimate independently? If someone says "I have no idea," the story needs more definition. Mark it with a ? and run a spike to understand it before committing it to a sprint.

### Small

The story can be completed within a single sprint by one or two developers.

**Test:** Could a developer pick this up on Day 1 of the sprint and have it Done by Day 8?

If the story would take most of the sprint for most of the team, it is an epic. Split it.

**How to split a large story:**
- By user type (student version vs lecturer version)
- By workflow step (search only, then booking only, then confirmation only)
- By data complexity (simple case first, edge cases in Sprint 2)
- By platform (web only in Sprint 1, mobile in Sprint 2)

### Testable

You can write acceptance criteria that produce a clear pass or fail result.

**Test:** For every sentence in the AC, can you say "this either passes or it does not"? If any AC contains the words "should work well," "looks nice," or "is fast" without a specific threshold, it is not testable. Rewrite it.

---

## Writing Acceptance Criteria

### Format

Use Given-When-Then without exception:

```
Given [some context that must be true before the action],
When [some action the user or system takes],
Then [some observable outcome that can be verified].
```

### Rules

**Minimum 2 AC per story.** For any story touching the activation flow, aim for 3 to 4.

**Each AC must be falsifiable.** You can run a test that either passes or fails. No ambiguity.

**AC are about observable behaviour, not implementation.** "Given I submit the booking form, When the form submits successfully, Then I see a confirmation screen with a booking reference number" -- correct. "Given the database receives the insert, When the transaction commits, Then the booking_id is returned" -- this is implementation detail, not user-facing AC.

**AC are not feature descriptions.** "The booking form should be user-friendly" is not an AC. "Given I complete the booking form and tap Submit, When the form is invalid (missing required field), Then each invalid field displays a specific error message below the input" -- this is an AC.

### AC Checklist

Before marking AC as ready, confirm each item:

- [ ] Written in Given-When-Then format
- [ ] Each AC tests a single, specific behaviour
- [ ] Every AC is falsifiable (you could write a test that passes or fails)
- [ ] No AC contains the words "should," "nice," "good," or "fast" without a specific measurable threshold
- [ ] The PO can confirm or reject each AC independently by looking at the running product

---

## Story Points

### The Fibonacci Scale

| Points | What It Signals |
|--------|----------------|
| 1 | Trivially simple. One file. One change. No logic. |
| 2 | Simple but slightly more work. A couple of files. Obvious implementation. |
| 3 | A clear feature with a defined implementation path. Some edge cases to handle. |
| 5 | Non-trivial. Multiple components or files. Integration with another service or module. |
| 8 | Complex. Significant uncertainty in implementation. High review burden. Consider splitting. |
| 13 | Almost certainly too large for one sprint. Split before committing. |
| 21 | Epic. Split immediately. Do not estimate epics with story points. |
| ? | We do not understand this story well enough to estimate. Run a spike first. |

### With AI Tools

Estimate the full story cycle, not just the generation step.

A story that takes:
- 10 minutes to generate with Stitch or Claude Code
- 45 minutes to review, edit, and fix errors
- 30 minutes to write and run tests
- 15 minutes for PO to confirm AC

...is a 3-point story, not a 1-point story.

Never estimate based on how fast AI can produce output. Estimate based on how long the complete cycle takes: generate, review, edit, test, confirm AC, merge.

### Calibration Anchors

Before estimating your backlog, agree on three anchors as a team:

1. Name a story you all agree is 1 point.
2. Name a story you all agree is 3 points.
3. Name a story you all agree is 5 points.

Write these down at the top of your sprint plan. All subsequent estimates are relative to these anchors, not to hours.

### Planning Poker

Use Planning Poker for any story where team members might disagree.

1. PO reads the story and AC aloud.
2. Every team member picks a number privately (write it down, do not say it).
3. All reveal simultaneously on the count of three.
4. If all estimates are within one Fibonacci number of each other, average and record.
5. If there is a spread, the highest and lowest estimator each explain their thinking.
6. Re-estimate until convergence.

The discussion is the point. Planning Poker surfaces hidden complexity and shared assumptions before the sprint begins.

---

## Interview Evidence Requirement

Every story in the MVP backlog must trace to an interview. Not an assumption. Not a feature you think users would like. An actual thing a real user told you.

Reference format:
```
Source: Interview [#] ([participant description], [date]) -- "[verbatim quote or close paraphrase]"
```

Example:
```
Source: Interview 4 (KIU student, March 14 2026) -- "I always end up going to a space that's already full. There's no way to know in advance."
```

If you cannot cite an interview, move the story to the out-of-scope backlog or the future-phase list. Do not build features without discovery evidence.

---

## Common Mistakes

| Mistake | What It Looks Like | How to Fix It |
|---------|-------------------|---------------|
| Missing So that clause | "As a user I want to log in." | "As a university student I want to log in with my university account so that I do not need to create and remember a separate password." |
| Story is a technical task | "Set up PostgreSQL database." | This is a technical task. Put it in the sprint as a task item, not as a user story. |
| AC is a feature description | "The search results should be fast and easy to use." | "Given I submit a search, When the results return, Then all results are displayed within 2 seconds." |
| Story is too large | 13+ point stories in Sprint 1 | Split by user type, workflow step, or data complexity. See splitting patterns above. |
| No interview evidence | Story appears with no source citation | Find the interview or move the story to the future-phase backlog. |
| Estimating by hours | "This will take 2 days so it is 16 hours so it is... 16 points?" | Use calibration anchors. Points are relative, not time-based. |
| AI generation time only in estimate | "Stitch built it in 5 minutes so it is 1 point." | Estimate the full cycle including review, testing, and AC confirmation. |

---

## Quick Reference Card

```
User Story Format:
  As a [user type],
  I want [goal]
  so that [reason].

INVEST:
  I - Independent
  N - Negotiable
  V - Valuable
  E - Estimable
  S - Small
  T - Testable

AC Format:
  Given [context],
  When [action],
  Then [observable outcome].

Fibonacci Scale:
  1  2  3  5  8  13  21  ?

Evidence Format:
  Source: Interview [#] ([participant], [date]) -- "[quote]"
```

---

*User Story Writing Guide | CS-PD-2026 | Spring 2026 | Kutaisi International University*
