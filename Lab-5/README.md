# Lab 5: From Synthesis to High-Fidelity Prototype and Event Schema

**Course:** CS-PD-2026 | Product Development for Software Engineers  
**Instructor:** Zeshan Ahmad | zeshan.ahmad@kiu.edu.ge  
**Group A:** Thursday 9 April 2026 | 14:00 to 16:00  
**Group B:** Friday 10 April 2026 | 13:00 to 15:00  
**Combined Lab 5 and Lab 6 Deadline:** Wednesday 23 April 2026 at 23:59

---

## What This Lab Is About

You have completed discovery. You have 10 or more interviews. You have a final problem statement, a patterns analysis, and a competitive landscape seed. You understand your user's job to be done and you have a value proposition.

Now you build.

Lab 5 has two parallel workstreams that run simultaneously within your team:

**Workstream A: High-Fidelity Prototype in Google Stitch**
Take your synthesis directly into Google Stitch and build a working high-fidelity prototype of your product. This is not a wireframe. Stitch generates real, interactive UI from natural language prompts. You will leave today with a clickable prototype that represents your core user flow.

**Workstream B: Event Schema Design**
Separately, design the complete event schema blueprint for your product. This is the measurement plan for everything your users will do. It is a markdown document only today. The actual instrumentation code gets written in Lab 6 when you integrate it into your AI Studio app.

By the end of Lab 5, your team has a real prototype and a complete measurement blueprint. Lab 6 turns both into a deployed, instrumented application.

---

## Learning Objectives

By the end of this lab, your team will:

1. Define and commit your North Star Metric with team consensus
2. Build a high-fidelity prototype of your core user flow using Google Stitch
3. Design a complete event schema covering all five AARRR stages
4. Understand how the prototype and event schema connect to each other before a single line of code is written

---

## What You Need Before You Arrive

- [ ] Your team's final problem statement (committed to repo)
- [ ] Your patterns analysis document (committed to repo)
- [ ] Your JTBD statement and value proposition canvas (from Checkpoint 1)
- [ ] Access to Google Stitch: https://stitch.withgoogle.com (sign in with your Google account)
- [ ] Access to Google AI Studio: https://aistudio.google.com (for Lab 6, but sign in today to confirm access)
- [ ] Your team's GitHub repo open and ready to commit
- [ ] Every team member on a laptop with a working internet connection

---

## Lab Timeline (120 minutes)

| Time | Activity | Output |
|------|----------|--------|
| 0:00 to 0:20 | Part 1: North Star Metric definition | `north-star-metric.md` drafted |
| 0:20 to 1:20 | Part 2: Stitch prototype build (parallel with Part 3) | Working Stitch prototype |
| 0:20 to 1:20 | Part 3: Event schema design (parallel with Part 2) | `event-schema.md` drafted |
| 1:20 to 1:45 | Part 4: Cross-team critique | Schema and prototype review |
| 1:45 to 2:00 | Part 5: Commit and close | Files committed to GitHub |

**Note on parallel workstreams:** Parts 2 and 3 run at the same time. Split your team. If you have 4 members, 2 work on Stitch and 2 work on the event schema. If you have 3 members, 1 leads Stitch and 2 lead the schema, then swap for review. Coordinate every 20 minutes.

---

## Part 1: North Star Metric (0:00 to 0:20)

### Why First

Your North Star Metric (NSM) is the single number that best captures the value your product delivers to users. It is not a business metric. It is a user value metric. Everything you build in Stitch and everything you measure in your event schema must connect back to this number.

Defining it first means every subsequent decision in today's lab has a clear north star. Literally.

### How to Define Your NSM

Answer these three questions as a team. Write your answers before you write the metric.

**Question 1: What is the core action a user takes that proves they got value from our product?**
Not signing up. Not logging in. The moment they say "yes, this works for me."

Example: For StudySpace Finders, it is not "searched for a space." It is "completed a study session booking at a verified space."

**Question 2: Can we measure it? Is it a discrete, countable event?**
"User satisfaction" is not an NSM. "Bookings completed per user per week" is an NSM.

**Question 3: Does it change when our product gets better or worse?**
If your NSM stays flat when you ship a bad release, it is not measuring the right thing.

### NSM Format

Write it in this exact format:

```
[Number] of [action] per [user/team] per [time period]
```

Examples:
- Weekly study sessions booked per active user
- Documents reviewed per team per sprint
- Meals planned per household per week

### Common NSM Mistakes

| Mistake | Why It Is Wrong |
|---------|----------------|
| Total signups | Vanity. Does not measure value delivered. |
| Page views | Activity, not outcome. |
| App downloads | Acquisition, not activation. |
| Revenue | Lagging indicator for an MVP with no paying users yet. |
| Daily active users | Too broad. Active doing what? |

### Deliverable

Complete the North Star Metric template at `templates/north-star-metric-template.md` and save your output to `03-build/analytics/north-star-metric.md`.

---

## Part 2: Google Stitch Prototype (0:20 to 1:20)

### What Is Google Stitch

Google Stitch (https://stitch.withgoogle.com) is an AI-powered tool that generates high-fidelity, interactive web application UI from natural language prompts. You describe your product, your users, and the screens you need, and Stitch builds a working interface you can click through and iterate on in real time.

This is not a mockup tool. The output is real HTML and CSS that you can export. In Lab 6, you will bring this into Google AI Studio Apps to add backend logic and your event schema instrumentation, then deploy to Vercel.

### Before You Open Stitch

Spend 5 minutes as a team writing your Stitch brief. Do not skip this. Teams that open Stitch without a brief waste 20 minutes prompting randomly.

Your brief must answer:
1. What is the product called? (Use your actual product name)
2. Who is the primary user? (One sentence from your ICP)
3. What is the single most important user flow we need to prototype today?
4. What are the 3 to 5 screens that flow requires?
5. What does the activation moment look like on screen?

See `guides/stitch-prompting-guide.md` for prompt templates and worked examples.

### Core User Flow First

Do not build every screen. Build the one flow that leads to your activation moment. For most products this is:

**Landing or Home screen → Core action screen → Confirmation or success screen**

For StudySpace Finders:
- Search screen (enter location, date, time)
- Results screen (list of available spaces with details)
- Booking confirmation screen (booking complete, session logged)

That is the activation moment: `booking_completed`. Everything else is secondary.

### Stitch Prompting Strategy

Stitch responds best to specific, structured prompts. Vague prompts produce generic output.

**Weak prompt:**
"Build me a study space finder app"

**Strong prompt:**
"Build a mobile-first web app called StudySpace. The primary user is a university student who needs to find a verified quiet study space on short notice. Screen 1: a search screen with a location input, a date picker, a time slot selector (morning, afternoon, evening), and a search button. Screen 2: results list showing space name, distance, availability badge (Available or Full), noise level (Quiet, Moderate, Lively), and a Book Now button. Screen 3: booking confirmation with space name, time slot, a booking reference number, and a button to add to calendar. Use a clean, minimal design with a blue and white colour scheme."

### Iteration During Lab

You have 60 minutes in Stitch. Use them in three rounds:

**Round 1 (0:20 to 0:45):** Build the core flow. Get all three screens working. Do not perfect anything.

**Round 2 (0:45 to 1:05):** Iterate on the activation screen specifically. This is the screen that drives your NSM. It must be clear, simple, and require no explanation.

**Round 3 (1:05 to 1:20):** Add one additional screen that your event schema requires. For example, if your schema tracks `profile_completed`, you need a profile screen.

### Saving Your Stitch Output

1. In Stitch, click Share and copy the shareable link
2. Also export the code if Stitch offers that option
3. Save both to your Stitch prototype doc (template provided)

### Deliverable

Complete `templates/stitch-prototype-template.md` and save your output to `02-design/prototypes/high-fidelity/stitch-prototype-link.md`.

---

## Part 3: Event Schema Design (0:20 to 1:20)

### Why Design Before You Code

Your event schema is the blueprint for everything you will measure. Changing event names after you have data means losing all historical data for that event. Designing it carefully now, before Lab 6 instrumentation, means you never have to break backwards compatibility.

A good event schema answers three questions for every user action:
1. What did the user do? (event name)
2. What context matters for understanding why? (properties)
3. Which stage of the AARRR funnel does this belong to? (stage mapping)

### Event Naming Convention

Follow this rule without exception:

```
object_action (snake_case, past tense)
```

| Correct | Wrong | Why Wrong |
|---------|-------|-----------|
| `user_signup_completed` | `UserSignupCompleted` | camelCase not permitted |
| `booking_created` | `create_booking` | verb first not permitted |
| `space_search_started` | `search` | no action verb |
| `profile_photo_uploaded` | `click_button_3` | meaningless |

### How Many Events

For an MVP, 6 to 10 events is enough. You can always add more. You cannot easily rename what you already have in production.

**Must have (cover these first):**
- One Acquisition event (user enters your product)
- One Activation event (user reaches the aha moment -- this drives your NSM)
- One Retention event (user returns and does the core action again)

**Should have:**
- One Referral event (user invites or shares)
- Key feature usage events (the features that distinguish your product)

**Nice to have:**
- Revenue event (if your MVP has any payment flow)
- Error or failure events (useful for debugging early users)

### Event Properties

Each event needs properties that give you context. Without properties, you know something happened but not why.

**For every event, include:**
- `user_id` (string, UUID) -- who did it
- `timestamp` (ISO 8601) -- when did it happen
- `session_id` (string, UUID) -- which session it happened in

**Then add event-specific properties that help you understand the action:**

Example for `space_search_started`:
```
user_id: "user_12345"
timestamp: "2026-04-09T14:23:45Z"
session_id: "sess_67890"
search_location: "Kutaisi City Centre"
search_date: "2026-04-10"
search_time_slot: "afternoon"
```

### Privacy Rules (Non-Negotiable)

- Never include names, email addresses, or phone numbers in event properties
- `user_id` is a UUID generated by your system, never the user's email
- Never log the contents of messages, notes, or any user-generated content
- If you are unsure whether something is PII, leave it out

### Mapping Events to AARRR

Every event must serve a specific stage of the funnel. If you cannot explain which stage an event serves, do not track it.

| Stage | Question It Answers | Example Event |
|-------|-------------------|---------------|
| Acquisition | How did users find and enter the product? | `user_signup_completed` |
| Activation | Did the user reach the aha moment? | `booking_completed` |
| Retention | Did the user come back and do it again? | `user_session_started` |
| Referral | Did the user tell someone else? | `invite_sent` |
| Revenue | Did the user pay? | `subscription_started` |

### Deliverable

Complete `templates/event-schema-template.md` and save your output to `03-build/analytics/event-schema.md`.

---

## Part 4: Cross-Team Critique (1:20 to 1:45)

Each team presents two things in 5 minutes:

1. **Demo your Stitch prototype.** Click through the core user flow. Point to the activation moment screen. Explain: what is the NSM and how does this screen drive it?

2. **Read your activation event aloud.** State the event name, its AARRR stage, and its three most important properties. The room will check: does the event name follow the naming convention? Does it actually measure the activation moment you just showed in the prototype?

The instructor will facilitate. Every team presents. Critique is direct and specific.

**Questions the room will ask:**
- What is your NSM? Does the activation screen make that moment obvious?
- What is your activation event? Is it named correctly?
- Are there any events you are tracking that you do not need?
- Are there any events missing that your NSM requires?

---

## Part 5: Commit and Close (1:45 to 2:00)

Before you leave, commit the following to your team repo:

```
03-build/analytics/north-star-metric.md     (required)
03-build/analytics/event-schema.md          (required)
02-design/prototypes/high-fidelity/stitch-prototype-link.md  (required)
```

Use this commit message format:
```
[LAB-5] north star metric, event schema v1, stitch prototype link
```

Tag the commit:
```
git tag lab-5-draft
git push origin lab-5-draft
```

**This is a draft commit.** You will refine all three documents after Lab 6 and before the combined deadline of Wednesday 23 April at 23:59.

---

## What Comes Next: Lab 6

In Lab 6 (Group A Thursday 16 April at 14:00, Group B Friday 17 April at 13:00) you will:

1. Open your Stitch prototype and bring it into Google AI Studio Apps (https://aistudio.google.com/apps)
2. Use AI Studio to add backend logic, user flows, and data persistence to your prototype
3. Integrate your event schema -- write the actual instrumentation code that fires events on user actions
4. Deploy the complete app to Vercel (https://vercel.com)
5. Get the live URL and begin collecting real data

By the end of Lab 6 you will have a publicly accessible URL that real users can visit. That is when user testing begins.

**Combined deadline: Wednesday 23 April at 23:59** for all Lab 5 and Lab 6 deliverables.

---

## Deliverables Summary

| File | Path | Due |
|------|------|-----|
| North Star Metric | `03-build/analytics/north-star-metric.md` | Draft by end of Lab 5, final by April 23 |
| Event Schema | `03-build/analytics/event-schema.md` | Draft by end of Lab 5, final by April 23 |
| Stitch Prototype Link | `02-design/prototypes/high-fidelity/stitch-prototype-link.md` | Draft by end of Lab 5, final by April 23 |
| Deployed App URL | `03-build/analytics/analytics-plan.md` | After Lab 6, by April 23 |
| Usability Findings | `02-design/user-testing/usability-findings.md` | After real user testing, by April 23 |

---

## Grading

Lab 5 participation is assessed on the quality of your in-lab output, not just completion.

| Component | What We Look For |
|-----------|-----------------|
| North Star Metric | Measures user value not activity. Follows the format. Team can defend the choice. |
| Event Schema | 6 to 10 events. Correct naming convention throughout. Every AARRR stage covered. Properties include context without PII. |
| Stitch Prototype | Core user flow is clickable end to end. Activation moment is clear on screen. At least 3 screens. |
| Cross-team critique | Team presented both deliverables. Engaged with feedback. |
| GitHub commit | All three files committed before leaving lab. Correct paths. |

---

## Getting Help

**During lab:** Raise your hand. The instructor circulates every 15 minutes.

**Stitch issues:** If Stitch is slow or unavailable, use the backup prompting guide in `guides/stitch-prompting-guide.md` and document what you would have built. Stitch access issues do not excuse missing the deliverable.

**Schema debates:** If your team cannot agree on an event name or whether to track something, apply this rule: track it if you would make a product decision differently based on that data. If you would not, do not track it.

**After lab:** Email zeshan.ahmad@kiu.edu.ge with subject line `[LAB-5] [Your Team Name] question`. Office hours available via Google Meet booked by email.

---

*Lab 5 | CS-PD-2026 | Spring 2026 | Kutaisi International University*
