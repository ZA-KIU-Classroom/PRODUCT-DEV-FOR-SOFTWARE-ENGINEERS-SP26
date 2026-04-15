# Lab 5 Grading Rubric

**Course:** CS-PD-2026 | Spring 2026  
**Instructor:** Zeshan Ahmad  
**Combined Lab 5 and Lab 6 Deadline:** Wednesday 22 April 2026 at 23:59

---

## Overview

Lab 5 is assessed as part of the combined Lab 5 and Lab 6 deliverable package due Wednesday 23 April at 23:59. Participation points are awarded based on in-lab output quality observed during the session itself.

---

## Participation (In-Lab, Observed by Instructor)

Instructor circulates and checks progress at 0:20, 0:45, 1:20, and 1:50.

| Checkpoint | What Is Checked | Full Credit | Partial Credit | No Credit |
|------------|----------------|-------------|---------------|-----------|
| 0:20 | NSM defined and documented | Clear metric in correct format with team rationale | Metric defined but format incorrect or team cannot explain it | Not started |
| 0:45 | Stitch progress and schema progress | 3 screens in progress in Stitch AND at least 4 events drafted | Only one workstream active | Neither started |
| 1:20 | Cross-team critique participation | Team presented prototype and activation event. Engaged with peer feedback. | Presented but did not engage with feedback | Did not present |
| 1:50 | GitHub commit | All three required files committed with correct paths | Files committed but wrong paths or missing one | Nothing committed |

---

## Deliverable Quality (Assessed After Deadline)

### North Star Metric (20% of Lab 5 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Format | Follows exact format: [Number] of [action] per [user/team] per [time period] | Close to format but missing one element | Does not follow format |
| Measures value | Captures the moment a user gets value, not activity | Partially measures value but includes vanity elements | Measures activity only (signups, page views, downloads) |
| Defensible | Team can explain why this specific metric and not an alternative | Some justification provided | No rationale given |
| Connects to prototype | The activation screen in the Stitch prototype directly drives this metric | Partial connection | No visible connection |

### Event Schema (40% of Lab 5 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Quantity | 6 to 10 events, no more, no fewer | 4 to 5 events or 11 to 12 events | Fewer than 4 or more than 12 |
| Naming convention | All events follow object_action snake_case past tense without exception | Most events correct, 1 to 2 violations | More than 2 naming violations |
| AARRR coverage | Acquisition, Activation, and Retention each have at least one event | Two of three core stages covered | Only one stage covered |
| Properties | Each event has user_id, timestamp, session_id, and at least 2 event-specific properties | Some events missing context properties | Properties missing entirely |
| Privacy | No PII in any event properties | One accidental PII field | Multiple PII fields present |
| Activation event | The activation event directly maps to the NSM | Partial connection to NSM | Activation event does not relate to NSM |
| Schema rationale | Brief explanation for why each event is included | Some events explained | No rationale provided |

### Stitch Prototype (30% of Lab 5 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| Clickable flow | Core user flow is clickable end to end from first screen to activation moment | Flow partially clickable, stops before activation | Not clickable or only one static screen |
| Screen count | At least 3 screens covering the core flow | 2 screens | 1 screen or Stitch link broken |
| Activation clarity | The activation moment screen is visually clear. A first-time user would understand what to do. | Activation screen present but unclear | No screen representing activation |
| Fidelity | High-fidelity: real UI elements, readable labels, coherent layout | Medium fidelity: some elements unclear | Low fidelity: placeholder text throughout |
| Link committed | Stitch shareable link is in the correct file at the correct path | Link present but wrong path | No link committed |

### GitHub Commit Quality (10% of Lab 5 grade)

| Criterion | Full Marks | Partial Marks | No Marks |
|-----------|-----------|--------------|---------|
| File paths | All files at exact required paths | 1 file at wrong path | 2 or more files missing or wrong path |
| Commit message | Follows format: `[LAB-5] description` | Descriptive but wrong format | No meaningful commit message |
| Draft tag | `lab-5-draft` tag pushed | Tag present but not pushed to remote | No tag |

---

## Late Submission Policy

The combined Lab 5 and Lab 6 deadline is Wednesday 23 April at 23:59.

One resubmission is permitted within one week of the deadline (by Wednesday 30 April at 23:59) for up to 80% of lost marks. After that window closes, the marks are gone.

---

## What Instructors Are Looking For

The most common failures in Lab 5 are:

**NSM failures:**
- Choosing signups or page views as the NSM (vanity metrics)
- Writing the NSM in free text instead of the required format
- Having an NSM that does not connect to the activation screen in the prototype

**Schema failures:**
- Using camelCase or verb-first naming (UserSignupCompleted, create_booking)
- Tracking more than 10 events for an MVP (scope creep)
- Missing the Retention stage entirely (teams forget to track returning users)
- Including email or name in event properties (PII violation)

**Prototype failures:**
- Building too many screens instead of focusing on the core activation flow
- Vague Stitch prompts that produce generic UI unrelated to the product
- Not saving the Stitch link before the lab ends

---

*Lab 5 Rubric | CS-PD-2026 | Spring 2026 | Kutaisi International University*
