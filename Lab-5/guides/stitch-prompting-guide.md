# Google Stitch Prompting Guide

**Lab 5 | CS-PD-2026 | Spring 2026**

---

## What Is Stitch

Google Stitch (https://stitch.withgoogle.com) generates high-fidelity, interactive web application UI from natural language prompts. You describe what you need and Stitch builds a clickable prototype with real UI components, navigation, and visual design.

The output is real code (HTML, CSS, JavaScript) that you will bring into Google AI Studio in Lab 6 to add backend logic and event instrumentation, then deploy to Vercel.

---

## The Brief: Write This Before You Open Stitch

Do not open Stitch until you have answered all five questions below. Teams that skip the brief waste 20 minutes.

**Brief template:**

```
Product name: [Your product name]

Primary user: [One sentence description of your ICP from team-icp.md]

The most important user flow to prototype today:
[Describe the flow in one sentence: what does the user want to accomplish?]

Screens required (list 3 to 5):
1. [Screen name and its purpose]
2. [Screen name and its purpose]
3. [Screen name and its purpose]

The activation moment: [What specific action on which screen proves the user got value?]

Visual style: [e.g. clean and minimal, dark and technical, warm and friendly, professional and corporate]
```

---

## Prompt Structure

A strong Stitch prompt has four parts in this order:

1. **Product identity** -- what it is and who it is for
2. **Screen specification** -- exactly what each screen contains
3. **Interaction description** -- what happens when the user takes the main action
4. **Visual direction** -- colour, tone, density

---

## Worked Example: StudySpace Finders

**Brief:**
```
Product name: StudySpace

Primary user: A KIU student who needs to find a quiet verified study space 
on short notice, usually within 2 hours of when they need it.

Most important flow: Student searches for a space, sees results, and completes 
a booking.

Screens:
1. Search screen -- location input, date, time slot selector, search button
2. Results screen -- list of spaces with availability, noise level, distance
3. Booking confirmation screen -- booking details and reference number

Activation moment: User taps "Confirm Booking" on screen 3. This fires 
booking_completed.

Visual style: Clean and minimal, blue and white, mobile-first.
```

**Weak prompt (do not write this):**
```
Build a study space finder app for university students.
```

**Strong prompt (based on the brief above):**
```
Build a mobile-first web app called StudySpace for university students who 
need to find quiet study spaces on short notice.

Screen 1 -- Search: 
A clean search screen with a page title "Find a Study Space", a location 
text input labelled "Where are you?", a date picker labelled "When?", a 
segmented control for time slot with three options (Morning, Afternoon, 
Evening), and a large primary button labelled "Search Spaces". Use a white 
background with a blue (#1d4ed8) primary colour.

Screen 2 -- Results: 
A list of study space cards. Each card shows: space name in bold, distance 
from search location (e.g. "0.3 km away"), a green "Available" badge or red 
"Full" badge, a noise level indicator (Quiet / Moderate / Lively), a star 
rating, and a "Book Now" button. Show 4 cards. The first two are Available, 
the third is Full, the fourth is Available.

Screen 3 -- Booking Confirmation: 
A confirmation screen with a green checkmark icon at the top, the heading 
"Booking Confirmed", the space name, the selected time slot, a booking 
reference number in monospace font (e.g. BK-20260409-001), an "Add to 
Calendar" button, and a "Find Another Space" button. This screen appears 
after the user taps "Book Now" on a result card.

Navigation: Screen 1 leads to Screen 2 on search button tap. Screen 2 leads 
to Screen 3 on "Book Now" tap.

Style: Clean, minimal, mobile-first (375px wide). Blue (#1d4ed8) and white. 
Body text in Inter or system sans-serif.
```

---

## Iteration Strategy

### Round 1 (0:20 to 0:45): Get All Screens Working

Goal: 3 screens exist and are navigable.

Do not perfect anything in Round 1. Focus on getting the structure right. If a button does not work or a screen looks wrong, note it and move on.

### Round 2 (0:45 to 1:05): Perfect the Activation Screen

Goal: The activation screen is visually clear and complete.

Your activation screen is the most important screen in the prototype. A first-time user should understand exactly what to do without any explanation. Spend most of Round 2 here.

Prompts to improve a specific screen:
- "Make the confirmation screen cleaner. The booking reference number should be larger and the checkmark icon should be bigger."
- "Add a progress indicator at the top of the search screen showing Step 1 of 3."
- "Replace the star rating with a specific label like Verified Quiet Space and add a small verified badge icon."

### Round 3 (1:05 to 1:20): Add One Schema-Driven Screen

Look at your event schema. Is there a screen missing that your schema requires?

Example: If your schema includes `profile_completed` as an activation event but you have no profile screen, add it now.

Keep this screen simple. One round of prompting. Do not let it eat into commit time.

---

## Common Stitch Problems and Fixes

| Problem | Fix |
|---------|-----|
| Output is too generic, looks like a template | Add more specific labels, field names, and button text to your prompt. Stitch follows instructions literally. |
| Screens are not connected | Add explicit navigation instructions: "Screen 2 appears when the user taps the Search button on Screen 1." |
| Layout looks broken on mobile | Add "mobile-first, 375px viewport width" to your prompt. |
| Colours are wrong | Specify exact hex codes in your prompt. |
| Text is placeholder lorem ipsum | Specify the exact text for all headings, labels, and body content. |
| Stitch keeps regenerating in a style you do not want | Add "Do not change the overall layout or colour scheme" to your iteration prompt. |

---

## Saving and Sharing Your Output

When your prototype is ready:

1. In Stitch, click the **Share** button (top right)
2. Set sharing to **Anyone with the link can view**
3. Copy the link
4. If Stitch offers a **Download code** or **Export** option, download it and save it to your repo as a zip or in a `stitch-export/` folder
5. Paste the link into your `stitch-prototype-link.md` document

**Critical:** Test the link in an incognito window before committing it. If the link does not work in incognito, your teammates and instructor cannot open it.

---

## Backup: If Stitch Is Unavailable

If Stitch does not load or is unavailable during lab:

1. Complete your brief document in full
2. Write out the 3 screen descriptions exactly as you would have prompted them
3. Sketch each screen on paper and photograph it
4. Commit the brief, screen descriptions, and photos to your repo as `02-design/prototypes/high-fidelity/stitch-backup/`
5. Notify the instructor immediately

You will still receive participation credit for completing this work. You must complete the actual Stitch prototype before the combined deadline of Wednesday 23 April at 23:59.

---

*Google Stitch Prompting Guide | Lab 5 | CS-PD-2026 | Spring 2026 | Kutaisi International University*
