# System Design Guide

Use this guide while filling `system-design.md`.

---

## What This Document Must Do

A strong system design document answers one practical question:

**If a developer opens this file tonight, do they know what to build first and how the system is supposed to behave?**

If the answer is no, the document is too vague.

---

## Start From One User Request

Do not start from tools. Start from one user request.

Bad starting point:

- We use Next.js, Supabase, and Mixpanel

Good starting point:

- A student signs in, searches for a space, books it, and sees confirmation

Architecture exists to support a request. The request comes first.

---

## What Good Component Design Looks Like

Each component should have one job.

Examples:

- Frontend app renders UI, collects user input, shows results
- Auth service handles identity and session logic
- Backend service validates requests and coordinates business logic
- Database stores users, resources, actions, and state
- Analytics platform records event signals for measurement

If one component does everything, the design is still muddy.

---

## How Detailed the Request Lifecycle Should Be

A request lifecycle should read like a walkthrough.

Example skeleton:

1. User opens search screen
2. Frontend checks session state
3. User enters filters and submits
4. Frontend sends request to backend endpoint
5. Backend validates auth and inputs
6. Backend queries database
7. Backend returns matching results
8. Frontend renders result cards
9. Search event fires to analytics

That level is enough for Sprint 1. You do not need distributed systems depth here. You do need clarity.

---

## Where Teams Usually Go Wrong

### 1. Mixing present architecture with future architecture
If a feature is not needed for Sprint 1, do not architect it deeply now.

### 2. Writing a tool list instead of a design
Tool names are not architecture. Responsibilities and flow are architecture.

### 3. Forgetting analytics and auth
Students often design the happy path but forget measurement and identity. If the user must sign in or if the team wants evidence, these belong in the design.

### 4. Forgetting what AI is doing
If AI is used in the product or the build workflow, document where it sits and how the team reviews it.

---

## Minimum Standard for a Good Submission

A good submission has:

- a narrow Sprint 1 boundary
- a readable component table
- a request lifecycle with steps in order
- a clear statement of stored data
- top risks named without hand waving

If your document still reads like a brainstorm, it is not ready.
