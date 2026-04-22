# Example System Design

**Team:** StudySpace Finders  
**Product:** StudySpace  
**Date:** 23 April 2026  
**Version:** 1.0

> This is a fictional worked example. Use it as a model for structure and detail, not as content to copy.

---

## 1. Core Sprint 1 Request

A university student signs in, searches for a study space, books one available slot, and sees a confirmation screen.

**Current Sprint 1 boundary:**
- In scope: signup, login, search, detail view, booking create, confirmation, event logging
- Out of scope: real campus occupancy integrations, notifications, payment, owner dashboard, referral loop

---

## 2. System Goal

By Sprint 1 review, StudySpace must support one end to end booking flow on a public URL. A user should be able to create an account, search seeded study spaces, select one option, and create a booking record that appears as confirmed. The system also needs event logging so the team can observe whether users reach search, detail, and booking confirmation. The design prioritises speed, clarity, and demo reliability over full real world completeness.

---

## 3. Component Breakdown

| Component | Layer | Responsibility | Owner | Technology | AI touchpoint, if any |
|-----------|-------|----------------|-------|------------|-----------------------|
| Web app | Client | Renders auth, search, detail, booking, confirmation screens | Ana | Next.js | Stitch used to scaffold UI screens |
| App routes and server actions | Server | Validates requests and coordinates reads and writes | David | Next.js server actions | Claude Code used for substantial multi file logic review |
| Auth | Auth | Account creation, login, session handling | Ana | Supabase Auth | No runtime AI |
| Booking data store | Data | Stores users, spaces, slots, bookings | David | Supabase Postgres | No runtime AI |
| Analytics | Measurement | Records search, view, booking created events | Nino | Mixpanel | No runtime AI |
| Map helper | Integration | Converts location string into coordinates for simple distance sort | Nino | Mapbox Geocoding API | No runtime AI |

---

## 4. Key Data Objects

| Entity | What it represents | Created by | Read by | Stored where |
|--------|--------------------|-----------|---------|-------------|
| User | Student account and session identity | Signup flow | Auth check, booking flow | Supabase Auth and profile table |
| Space | Study location available for booking | Seed script | Search and detail view | Postgres |
| Slot | Time bound availability block | Seed script | Search, detail, booking validation | Postgres |
| Booking | User reservation of one slot | Booking action | Confirmation view, future history view | Postgres |
| Event | Product usage signal such as search or booking | Frontend and server action | Team dashboard | Mixpanel |

---

## 5. User Request Lifecycle

1. Student opens the public StudySpace URL.
2. Frontend checks whether a session exists.
3. If not authenticated, the student signs up or logs in through Supabase Auth.
4. Student enters location and time filter on the search screen.
5. Frontend sends search filters to a server action.
6. Server action validates inputs and reads matching spaces and slots from Postgres.
7. Server action optionally enriches location results through the geocoding helper.
8. Matching spaces are returned to the frontend and rendered.
9. Student opens one detail view and selects a slot.
10. Frontend sends booking create request.
11. Server action validates slot availability and writes booking row.
12. Booking confirmation is returned.
13. Search viewed, detail viewed, and booking created events are sent to Mixpanel.
14. Student sees confirmation screen with booking reference.

---

## 6. Data Flow Notes

- User inputs: email, password, location string, selected slot
- Validated data: auth credentials, filter values, slot availability, existing booking conflict
- Stored permanently: users, spaces, slots, bookings
- Temporary or computed: distance sort result, session state, rendered result cards
- Data not stored: raw passwords, unnecessary precise location history beyond the requested search

---

## 7. APIs and Integrations

| Service or API | Why it exists | Request direction | Risk | Fallback plan |
|----------------|---------------|------------------|------|---------------|
| Supabase Auth | Fast account and session setup | Frontend to auth service | Email confirmation friction | Allow seeded test accounts for demo |
| Mapbox Geocoding | Simple coordinate lookup | Server to external API | Quota or latency | Fallback to seeded coordinates and manual distance sort |
| Mixpanel | Real event visibility | Frontend and server to analytics | Misfired events | Log locally and verify with manual event tests |

---

## 8. Deployment Topology

- Frontend hosted on: Vercel
- Backend hosted on: Next.js server actions on Vercel
- Database hosted on: Supabase managed Postgres
- Domain or public URL: Vercel preview or production URL
- Analytics platform: Mixpanel
- Auth provider: Supabase Auth
- File storage, if any: not needed in Sprint 1

---

## 9. AI in the Build and AI in the Product

### AI in the build workflow

| Tool | Used for what | Owner | Review rule |
|------|---------------|-------|-------------|
| Stitch | Generate auth and search screen scaffolds | Ana | Review every acceptance criterion against the generated UI |
| Claude Code | Search and booking logic, refactor, debug | David | Human read before merge, test locally, then PR review |
| AI Studio | Not used in Sprint 1 runtime | Nino | Reserved for future summarisation feature experiments |
| Copilot or Cursor | Inline completions and boilerplate | Whole team | Suggestion accepted only after line by line review |

### AI in the product, if applicable

No runtime AI feature exists in Sprint 1. AI is used in the build workflow only.

---

## 10. Security, Privacy, and Reliability Basics

- Auth risks: confirmation email friction could block first session activation
- Sensitive data handled: user identity and booking records
- Failure mode if main service goes down: search and booking unavailable, seeded fallback demo path retained
- Logging and monitoring plan for Sprint 1: Mixpanel event verification plus server error logs on host
- One thing we will not promise yet: real time occupancy truth from live venues

---

## 11. Technical Risks and Spikes

1. Risk: slot availability logic may allow double booking
   - Why it matters: breaks trust in the core booking flow
   - Mitigation or spike: add server side validation on slot status before write and test with concurrent requests
   - Owner: David

2. Risk: auth flow may add too much friction to activation
   - Why it matters: users may never reach search
   - Mitigation or spike: keep seeded test accounts ready and instrument signup drop off
   - Owner: Ana

3. Risk: geocoding dependency may slow or fail search
   - Why it matters: search is the core request entry point
   - Mitigation or spike: seed fixed coordinates and allow fallback sort without live API
   - Owner: Nino

---

## 12. Open Questions

- Should demo mode bypass email confirmation for instructor review accounts?
- Do we need a booking history view in Sprint 1, or is confirmation enough?
- Will event logging happen only client side, or also server side for booking create?

---

## 13. Final Readiness Check

- [x] Every component has one clear job
- [x] Core request lifecycle is written end to end
- [x] Stack in this file matches `tech-stack.md`
- [x] Top technical risks are named
- [x] Out of scope items are explicit
- [x] Another developer could start work from this document
