# Architecture Diagram Guide

Use this guide before exporting `architecture-diagram.png`.

---

## The Test

A good architecture diagram passes one test:

**A teammate who did not draw it should be able to narrate the Sprint 1 request from left to right.**

If they cannot, the diagram is not finished.

---

## What to Show

Most Sprint 1 diagrams in this course should include:

- the user
- the client or browser
- the frontend application
- auth
- backend or server logic
- database
- analytics or event tracking
- external service, if used

Show only the boxes that matter to the current sprint.

---

## Label the Arrows

Boxes without labeled arrows create confusion.

Use action labels such as:

- signs in
- submits search
- validates session
- queries database
- stores booking
- emits event
- returns confirmation

This is the difference between a meaningful diagram and a decorative one.

---

## Common Mistakes

### 1. Diagram does not match the written document
The PNG and `system-design.md` should describe the same system.

### 2. Analytics missing
If the team says instrumentation matters, the diagram should show where events fire.

### 3. Auth missing
If the user logs in, auth belongs in the picture.

### 4. AI shown as magic
If AI exists in the system, show where it is called and what inputs or outputs it touches.

### 5. Too much future state
Do not diagram a Phase 3 platform when the team has not built Phase 1.

---

## Practical Advice

- keep layout left to right
- keep labels short
- group components by layer
- use different shapes or styling for data stores
- export the final as PNG and test readability at normal zoom
