# Tech Stack Selection Guide

Use this guide while filling `tech-stack.md`.

---

## The Rule

Every selected tool needs a reason.

Good reason:

- We chose Supabase because Sprint 1 needs auth and database setup fast, and the team already knows the basics.

Weak reason:

- We chose Supabase because everyone uses it.

Your stack should reflect product need, team ability, and sprint constraints.

---

## What to Cover

At minimum, decide these layers:

- frontend
- backend
- database
- auth
- analytics
- hosting
- testing
- approved AI tooling

If a layer is intentionally absent, say why.

---

## How to Reject Alternatives Properly

Do not reject alternatives with vague phrases.

Weak:

- Firebase rejected because not good

Strong:

- Firebase rejected because the team wants relational queries for booking logic and already planned SQL based data design

A good rejection shows that the team understood the option before saying no.

---

## What Instructors Want to See

- no TBD entries
- no contradiction between system design and stack file
- deployment target named clearly
- AI tool policy aligned with the Week 7 lecture
- shortcuts accepted on purpose, not by accident

---

## AI Tool Guidance for Sprint 1

Use the Week 7 logic:

- Stitch for UI scaffolding and screens
- Claude Code for substantial multi-file logic, debugging, and architectural work
- AI Studio for building or testing AI product features before integration
- Copilot or Cursor for inline completion and repetitive patterns

Do not say "AI" as a generic tool choice. Name the tool and the reason.
