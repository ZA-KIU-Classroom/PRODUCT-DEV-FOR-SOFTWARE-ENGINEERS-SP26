# Sprint 1 Plan — Example

**Team:** StudySpace Finders  
**Product:** StudySpace  
**Sprint:** 1 of 4  
**Dates:** April 24 to May 7 2026  
**Product Owner:** Ana  
**Scrum Master:** David  
**Version:** 1.0

> **Note to students:** This is a worked example using the fictional StudySpace Finders team. It shows the expected level of detail for user stories, acceptance criteria, and AI tool assignments. Do not copy it. Your sprint plan must reflect your actual product and your actual stories.

---

## Sprint Goal

A real user can sign up, search for a study space by location and time slot, and complete a booking -- from a publicly accessible URL -- by the end of Sprint 1.

---

## Sprint Ceremonies

| Ceremony | When | Where | Who Facilitates |
|----------|------|-------|----------------|
| Sprint Planning | Lab 8, Apr 24 (Group A) | In person | David (SM) |
| Daily Standup | 09:00 every day | #standup Slack channel | Async -- all post independently |
| Sprint Review | May 7, 12:00 (Google Meet) | Google Meet | Ana (PO) |
| Retrospective | May 8, 18:00 | Google Meet | David (SM) |

**Async standup format:**
```
Yesterday: [completed -- include story ID]
Today: [working on -- include story ID]
Blocker: [specific blocker or "none"]
AI note: [what AI generated yesterday, accepted/modified/discarded]
```

**Blocker escalation:** If a blocker is not resolved within 24 hours, David posts in #blockers and tags affected team members.

---

## Definition of Done

A story is Done when all of the following are true:

- [ ] Code reviewed by at least one team member who is not the original author
- [ ] Pull request merged to `main` via GitHub PR
- [ ] Acceptance criteria confirmed as met by Ana (PO) -- not by the developer who built it
- [ ] If AI-generated: code annotated with inline comments explaining the logic
- [ ] If AI-generated: entry added to `docs/ai-usage-log.md`
- [ ] Feature works at the deployed Vercel URL, not just locally
- [ ] No new known bugs introduced to the main branch

---

## Calibration Anchors

| Points | StudySpace Example |
|--------|-------------------|
| 1 | Change the "Book Now" button label to "Reserve Space" |
| 3 | Add an email validation check to the signup form with error display |
| 5 | Build the space search API endpoint with location and time-slot filtering |

---

## Sprint 1 Backlog

### Story S1-01: User Signup

**User Story:**  
As a university student, I want to sign up for StudySpace with my email address so that I can access the platform and book study spaces without creating a new password I will forget.

**Interview Evidence:**  
Source: Interview 2 (KIU CS student, March 12 2026) -- "I'm not going to make another account. I already have 15 passwords I can't remember."  
Source: Interview 5 (KIU Business student, March 14 2026) -- "If it needs a separate login, I probably won't use it after the first week."

**Story Points:** 3  
**Assignee:** Ana  
**AI Tool:** Google Stitch (signup UI screens), Claude Code (email verification backend logic)  
**AI Tool Rationale:** Stitch generates the signup form UI from AC prompt. Claude Code handles the multi-step email verification logic which requires understanding the full auth flow.

**Acceptance Criteria:**

```
AC1:
Given I am on the signup screen,
When I enter a valid email address and tap "Create Account",
Then I receive a verification email within 60 seconds and the screen shows
"Check your email to confirm your account."

AC2:
Given I have received the verification email,
When I click the confirmation link,
Then I am redirected to the StudySpace app and logged in automatically.

AC3:
Given I am on the signup screen,
When I enter an email address that is already registered,
Then the form displays the error "An account with this email already exists.
Log in instead?" with a link to the login screen.

AC4:
Given I am on the signup screen,
When I enter a malformed email address (missing @ or domain),
Then the form displays "Please enter a valid email address" before I can submit.
```

**Notes:** Use Supabase Auth for email verification -- David has prior experience. Do not build custom auth. Stitch prompt should include all four error states from the AC.

---

### Story S1-02: User Login

**User Story:**  
As a returning user, I want to log in to StudySpace with my email and password so that I can access my account and bookings without signing up again.

**Interview Evidence:**  
Source: Interview 2 (KIU CS student, March 12 2026) -- "Once I've made an account somewhere I want to just get back in quickly."

**Story Points:** 2  
**Assignee:** Ana  
**AI Tool:** GitHub Copilot  
**AI Tool Rationale:** Login form is straightforward boilerplate once auth is set up. Copilot handles the implementation efficiently. No architectural decisions required.

**Acceptance Criteria:**

```
AC1:
Given I am on the login screen,
When I enter my registered email and correct password and tap "Log In",
Then I am taken to the search screen and my session is maintained for 7 days
without re-authentication.

AC2:
Given I am on the login screen,
When I enter a registered email with an incorrect password,
Then the form displays "Incorrect email or password" without specifying
which is wrong, and I remain on the login screen.

AC3:
Given I am logged in on Device A,
When I open the app on Device B with the same account,
Then I am logged in on both devices simultaneously.
```

**Notes:** Depends on S1-01 (auth must be set up). Do not start S1-02 until S1-01 is Done. Mark this dependency explicitly in the sprint tracker.

---

### Story S1-03: Space Search

**User Story:**  
As a student who needs to study, I want to search for available study spaces by location and time slot so that I can find a space that is actually free before I travel there.

**Interview Evidence:**  
Source: Interview 1 (KIU Architecture student, March 11 2026) -- "I walked 20 minutes to the library last Tuesday and it was completely full. I had to go home."  
Source: Interview 4 (KIU Law student, March 13 2026) -- "I just need to know: is it quiet, is it free, and how far is it?"  
Source: Interview 7 (KIU Engineering student, March 15 2026) -- "The main thing is real-time availability. Otherwise it's useless."

**Story Points:** 5  
**Assignee:** David  
**AI Tool:** Claude Code  
**AI Tool Rationale:** The search logic requires filtering across multiple dimensions (location, date, time slot, availability status) and will touch multiple files (API endpoint, database query, search state management). Claude Code is better suited than Copilot for this level of complexity.

**Acceptance Criteria:**

```
AC1:
Given I am on the search screen,
When I enter "Kutaisi city centre" in the location field, select today's date,
and choose the "Afternoon" time slot, then tap "Search",
Then I see a list of available spaces sorted by distance from the search location.

AC2:
Given search results are displayed,
When there are no available spaces matching my search,
Then I see the message "No spaces available for this time slot. Try a different
time or location." with a button to clear filters.

AC3:
Given search results are displayed,
When I view a space in the results list,
Then I can see: space name, distance from my location (in km), availability
status (Available / Full), noise level (Quiet / Moderate / Lively), and a
"View Space" button.

AC4:
Given I am on the search screen,
When I do not enter a location and tap "Search",
Then the location field displays the error "Please enter a location to search."
```

**Notes:** Use seeded database with 5 to 10 fictional spaces for Sprint 1 demo. Real space data is a Sprint 2 concern. Distance calculation: Haversine formula is sufficient for MVP, no need for routing API in Sprint 1.

---

### Story S1-04: Space Detail View

**User Story:**  
As a student viewing search results, I want to see more detail about a specific space so that I can decide whether it meets my needs before committing to a booking.

**Interview Evidence:**  
Source: Interview 3 (KIU Medicine student, March 12 2026) -- "I need to know if it's actually quiet, not just what they claim. And I need to know the exact address."  
Source: Interview 6 (KIU Economics student, March 14 2026) -- "Just show me: quiet or not, desk and chair or not, how far. That's enough."

**Story Points:** 3  
**Assignee:** Nino  
**AI Tool:** Google Stitch  
**AI Tool Rationale:** The detail view is a display screen with no complex logic. Stitch generates the layout from a detailed AC prompt efficiently.

**Acceptance Criteria:**

```
AC1:
Given I tap "View Space" on a search result,
When the space detail screen loads,
Then I see: space name, full address, noise level label (Quiet / Moderate / Lively),
available time slots for today, a photo or placeholder image, and a "Book This Space" button.

AC2:
Given I am on the space detail screen,
When the space has no available slots remaining for my searched time,
Then the "Book This Space" button is replaced with "Fully Booked" (greyed out)
and I see "Next available: [time slot]" below it.

AC3:
Given I am on the space detail screen,
When I tap the back button or swipe back,
Then I return to my search results with my previous search filters preserved.
```

**Notes:** Depends on S1-03 (search must return a space ID for the detail view to load). Do not begin until S1-03 API returns space objects with the required fields.

---

### Story S1-05: Booking Creation and Confirmation

**User Story:**  
As a student who has found a suitable space, I want to complete a booking and receive an immediate confirmation so that I know my spot is secured and I have a record to refer back to.

**Interview Evidence:**  
Source: Interview 1 (KIU Architecture student, March 11 2026) -- "The confirmation needs to feel definitive. I want to know it's actually mine."  
Source: Interview 9 (KIU CS student, March 17 2026) -- "Give me a reference number or something. Otherwise I don't trust it."  
Source: Interview 4 (KIU Law student, March 13 2026) -- "If I book it I need to be sure no one else can take it."

**Story Points:** 3  
**Assignee:** David  
**AI Tool:** Claude Code (booking logic), GitHub Copilot (confirmation UI boilerplate)  
**AI Tool Rationale:** The booking logic (availability lock, concurrency handling, reference number generation) requires careful multi-file implementation -- Claude Code. The confirmation screen is simpler UI -- Copilot handles that efficiently.

**Acceptance Criteria:**

```
AC1:
Given I am on the space detail screen and the space has an available slot,
When I tap "Book This Space" and confirm on the booking summary screen,
Then a booking record is created, the slot is marked unavailable to other users,
and I see the confirmation screen within 3 seconds.

AC2:
Given I am on the confirmation screen,
When the booking is successful,
Then I see: space name, address, time slot booked, a unique booking reference number
(8 characters, alphanumeric), and a "Done" button that returns me to the search screen.

AC3:
Given two users attempt to book the same last available slot simultaneously,
When both submit the booking at the same time,
Then exactly one booking succeeds and shows a confirmation. The other user sees
"Sorry, this slot was just taken. Please choose another slot." with a link
back to the detail view.

AC4:
Given I have completed a booking,
When I tap "Done" on the confirmation screen,
Then my completed booking appears in my booking history (S2-03, future sprint)
and the search results no longer show this slot as available.
```

**Notes:** AC3 (concurrency) is critical for correctness but hard to test manually. David to write an automated test that fires two simultaneous booking requests and confirms only one succeeds. This test counts toward the DoD for S1-05.

---

## Sprint 1 Summary

| Story ID | Summary | Points | Assignee | AI Tool | Status |
|----------|---------|--------|----------|---------|--------|
| S1-01 | User signup | 3 | Ana | Stitch + Claude Code | Not started |
| S1-02 | User login | 2 | Ana | Copilot | Not started |
| S1-03 | Space search | 5 | David | Claude Code | Not started |
| S1-04 | Space detail view | 3 | Nino | Stitch | Not started |
| S1-05 | Booking and confirmation | 3 | David | Claude Code + Copilot | Not started |
| **Total** | | **16** | | | |

**Capacity check:** 16 points committed out of approximately 29 maximum (55% -- target 60% or below) ✓

---

## Sprint Review Criteria

At Sprint Review (May 7, Google Meet), Ana will demo:

1. Sign up as a new user (S1-01) -- live, using a real email address
2. Search for a space in Kutaisi city centre for the afternoon slot (S1-03, S1-04)
3. Complete a booking and show the confirmation screen with the reference number (S1-05)

The entire flow runs live. No screenshots. No recording. The deployed Vercel URL is used. If anything fails to load, the Sprint Review pauses until it is resolved.

---

## Change Log

| Date | Changes | Author |
|------|---------|--------|
| 16 Apr 2026 | Sprint 1 plan created in Lab 6 | Ana |

---

*Sprint 1 Plan Example | StudySpace Finders | CS-PD-2026 | Spring 2026*  
*This is a worked example for instructional purposes. Not a real student submission.*
