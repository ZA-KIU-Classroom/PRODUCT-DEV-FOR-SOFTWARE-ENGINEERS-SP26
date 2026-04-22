# System Design Template

**File path:** `03-build/architecture/system-design.md`

**Team:**  
**Product:**  
**Date:**  
**Version:**  
**Primary author:**

---

## 1. Core Sprint 1 Request

Write one sentence.

```text
A [target user] does [core action] and receives [observable result].
```

**Current Sprint 1 boundary:**
- In scope:
- Out of scope:

---

## 2. System Goal

Explain in 3 to 5 sentences what this system must do by Sprint 1 review.

---

## 3. Component Breakdown

| Component | Layer | Responsibility | Owner | Technology | AI touchpoint, if any |
|-----------|-------|----------------|-------|------------|-----------------------|
| Frontend web app | Client | | | | |
| Application logic | Server | | | | |
| Database | Data | | | | |
| Authentication | Auth | | | | |
| Analytics | Measurement | | | | |
| External services | Integration | | | | |

Add rows as needed.

---

## 4. Key Data Objects

List the core entities the system must store or move.

| Entity | What it represents | Created by | Read by | Stored where |
|--------|--------------------|-----------|---------|-------------|
| | | | | |
| | | | | |
| | | | | |

---

## 5. User Request Lifecycle

Describe the exact sequence for the core Sprint 1 request.

1. User opens:
2. Frontend sends:
3. Backend validates:
4. Database reads or writes:
5. External service, if any:
6. Analytics event fired:
7. User sees:

Write this as a real sequence, not vague bullets.

---

## 6. Data Flow Notes

Answer these:

- What data enters from the user?
- What data is validated?
- What data is stored permanently?
- What data is temporary or computed?
- What data should never be stored?

---

## 7. APIs and Integrations

| Service or API | Why it exists | Request direction | Risk | Fallback plan |
|----------------|---------------|------------------|------|---------------|
| | | | | |
| | | | | |

---

## 8. Deployment Topology

Fill this in directly.

- Frontend hosted on:
- Backend hosted on:
- Database hosted on:
- Domain or public URL:
- Analytics platform:
- Auth provider:
- File storage, if any:

---

## 9. AI in the Build and AI in the Product

### AI in the build workflow

| Tool | Used for what | Owner | Review rule |
|------|---------------|-------|-------------|
| Stitch | | | |
| Claude Code | | | |
| AI Studio | | | |
| Copilot or Cursor | | | |

### AI in the product, if applicable

Describe whether the product itself has an AI feature in Sprint 1. If not, say so clearly.

---

## 10. Security, Privacy, and Reliability Basics

Answer briefly.

- Auth risks:
- Sensitive data handled:
- Failure mode if main service goes down:
- Logging and monitoring plan for Sprint 1:
- One thing you will not promise yet:

---

## 11. Technical Risks and Spikes

Name the top 3 technical risks.

1. Risk:
   - Why it matters:
   - Mitigation or spike:
   - Owner:

2. Risk:
   - Why it matters:
   - Mitigation or spike:
   - Owner:

3. Risk:
   - Why it matters:
   - Mitigation or spike:
   - Owner:

---

## 12. Open Questions

List only questions that must be resolved during Sprint 1.

- 
- 
- 

---

## 13. Final Readiness Check

- [ ] Every component has one clear job
- [ ] Core request lifecycle is written end to end
- [ ] Stack in this file matches `tech-stack.md`
- [ ] Top technical risks are named
- [ ] Out of scope items are explicit
- [ ] Another developer could start work from this document
