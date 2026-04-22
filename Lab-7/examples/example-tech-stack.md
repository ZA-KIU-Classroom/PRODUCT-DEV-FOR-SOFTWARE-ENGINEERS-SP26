# Example Tech Stack Selection

**Team:** StudySpace Finders  
**Product:** StudySpace  
**Date:** 23 April 2026  
**Version:** 1.0

> Fictional example for structure only.

---

## 1. Decision Summary

The team is optimising for fast Sprint 1 execution with low setup overhead and easy public deployment. The product needs simple auth, relational data, event logging, and a search to booking flow on the web. Because the team already used a web prototype and wants one repo for frontend plus server logic, a Next.js based stack reduces context switching. The team is accepting some technical debt, especially around fallback geocoding and seeded availability data, in exchange for reliable delivery during the first sprint.

---

## 2. Stack by Layer

| Layer | Selected technology | Why this fits | Alternative considered | Why rejected | Owner |
|------|---------------------|--------------|------------------------|--------------|------|
| Frontend | Next.js | Same app supports UI and server actions, easy Vercel deploy | Plain React with separate API | More moving parts for a short sprint | Ana |
| Backend | Next.js server actions | Fast implementation path for CRUD logic | Express API | Extra setup and split deployment overhead | David |
| Database | Supabase Postgres | Relational model fits spaces, slots, bookings | Firebase | Team wanted SQL relationships and clearer booking logic | David |
| Authentication | Supabase Auth | Fast email auth with little custom work | Custom auth | Too risky for Sprint 1 | Ana |
| Analytics | Mixpanel | Event based product signals align with search and booking funnel | Google Analytics 4 | Team wanted product event focus over page analytics | Nino |
| Hosting | Vercel | Fast deploy path for Next.js | Render | Team already used Vercel in previous course work | Ana |
| Testing | Vitest plus manual flow test | Enough for Sprint 1 logic and verification | Cypress from day one | Too much setup for this sprint | David |
| Diagramming | Excalidraw | Fast team editing and easy export | Lucidchart | No strong added value for this sprint | Nino |

---

## 3. Approved AI Tools for Sprint 1

| Tool | Approved use | Not for | Review rule | Owner |
|------|--------------|---------|-------------|------|
| Stitch | UI scaffolding for auth, search, and detail screens | Backend logic, auth policy, database design | Acceptance criteria checked item by item before merge | Ana |
| Claude Code | Multi file search logic, booking flow, refactor, debug | Blind end to end generation without human reading | Human read, local test, PR review | David |
| AI Studio | Future AI feature experimentation only | General app coding | Prompts versioned, no runtime use yet | Nino |
| Copilot or Cursor | Inline completion, repetitive code, tests | Architecture decisions and feature design | Never accept unreviewed suggestions | Whole team |

---

## 4. Deployment Target

- Public deployment target: Vercel production URL
- Database region or environment: Supabase project in one shared environment
- How local and production differ: local uses `.env.local`, production uses hosted environment variables
- What gets deployed first: auth plus search shell and seeded data path
- What will stay local for now, if anything: experimental scripts and seed helpers

---

## 5. Rejected Architecture Paths

### Rejected Option 1
- Option: React frontend plus separate Express backend
- Why it was attractive: clearer separation of concerns
- Why it was rejected now: slower to ship and more files to coordinate during Sprint 1

### Rejected Option 2
- Option: Firebase for auth and data
- Why it was attractive: fast startup and generous free tier
- Why it was rejected now: booking logic fits relational data better and the team wanted SQL queries

---

## 6. Technical Debt You Are Accepting on Purpose

| Shortcut | Why accepted now | Risk created | When to revisit |
|----------|------------------|-------------|-----------------|
| Seeded study spaces | Faster demo and search flow build | Real data quality not proven | Sprint 2 |
| No full automated end to end suite yet | Saves setup time in Sprint 1 | Manual regression risk | Sprint 2 |
| One deployment environment only | Simpler team workflow | Less staging safety | Before external pilot |

---

## 7. Final Stack Lock

- Frontend: Next.js web app on Vercel
- Backend: Next.js server actions in same repo
- Database: Supabase Postgres
- Auth: Supabase Auth
- Analytics: Mixpanel
- Hosting: Vercel for app, Supabase for data and auth

No TBD entries remain.
