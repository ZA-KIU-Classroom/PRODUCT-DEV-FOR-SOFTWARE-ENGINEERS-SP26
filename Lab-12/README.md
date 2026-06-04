# Lab 12: Pitch Deck Workshop

**Course:** CS-PD-2026 | Product Development for Software Engineers | Spring 2026
**Instructor:** Zeshan Ahmad | zeshan.ahmad@kiu.edu.ge
**Week:** 14

**Group A:** Thursday 4 June 2026 | 14:00 to 16:00 | Standard lab room
**Group B:** Friday 5 June 2026 | 13:00 to 15:00 | Standard lab room

**Checkpoint 4 deadline:** Thursday 11 June 2026 at 23:59

---

## What This Lab Is

This is the final lab of the semester. By the time you leave today you will have a complete 10-slide investor pitch deck, a one-page leave-behind, a plan for your 60-second launch video, and a full run-through of your 7-minute Demo Day pitch in front of the lab group.

Demo Day is Thursday 11 June. Every deliverable you produce today feeds directly into the 15 points that Checkpoint 4 is worth. This is not a draft session. Treat it as a dress rehearsal.

---

## Learning Objectives

By the end of this lab you will be able to:

1. Construct a 10-slide investor pitch deck that meets the standard required by external judges.
2. Write a one-page product brief that can stand alone without a presenter in the room.
3. Deliver a structured 7-minute pitch and handle Q&A from peers acting as judges.
4. Plan and script a 60-second TikTok-style launch video using the five-section structure from the Week 14 lecture.
5. Audit your GitHub repository against the Checkpoint 4 rubric and identify and close any gaps.

---

## Pre-Lab Requirements

Before arriving you must have:

- Your `06-strategy/competitive-analysis.md` from Lab 11 open and ready. Slide 9 of your pitch deck builds directly from this file. If it is incomplete, the first 20 minutes of lab are remediation.
- Your analytics dashboard open in a browser tab. Slide 6 (Traction) requires real numbers from your live dashboard.
- Your `04-gtm/financials/unit-economics.md` and `04-gtm/financials/12-month-model.xlsx` accessible. Slide 7 (Business Model) requires real CAC and LTV figures.
- At least one team member with the live deployed product open and working on a device. Slide 5 requires a screenshot of the real product, and the live demo requires the real product.
- Your repository cloned and writable. You will commit files during this session.

---

## Lab Schedule

| Time | Activity | Output |
|------|----------|--------|
| 0:00 to 0:15 | Repository audit and gap triage | Gap list with owner assigned |
| 0:15 to 1:00 | Build the 10-slide pitch deck | `05-fundraising/pitch-deck.pdf` draft |
| 1:00 to 1:15 | Build the one-pager | `05-fundraising/one-pager.pdf` draft |
| 1:15 to 1:45 | Team pitch run-through (7 minutes each) | Peer feedback notes |
| 1:45 to 2:00 | Launch video planning and repo commit | `09-final/demo-video.md` planned, all files committed |

Instructor checkpoints at 0:15, 0:45, 1:15, and 1:50.

---

## Part 1: Repository Audit (0:00 to 0:15)

Before building anything new, spend 15 minutes auditing your repository against the Checkpoint 4 requirements. Use the checklist in `templates/repo-audit-checklist.md`.

For each missing item, assign one team member as owner and set a deadline before 11 June at 23:59. Do not leave this audit until the night before Demo Day. Judges will check your repository.

The audit has three categories:

**Critical gaps** (will cost points if not resolved): missing pitch-deck.pdf, missing README live URL, private repository, broken deployment link, missing open-source licence.

**Important gaps** (expected to be present): missing one-pager.pdf, incomplete folder structure, missing case-study.md, no demo video link.

**Polish gaps** (improve score): README quality, PR history showing active development, documentation depth in 03-build.

---

## Part 2: The 10-Slide Pitch Deck (0:15 to 1:00)

### The brief

Build a 10-slide investor pitch deck using the template in `templates/pitch-deck-template.md`. Export it as a PDF and commit it to `05-fundraising/pitch-deck.pdf`.

Every slide has one job. Resist the temptation to add slides. A pitch deck with 14 slides tells judges you have not edited your thinking. The constraint is the discipline.

### Tools you may use

- Google Slides (export to PDF)
- Canva (export to PDF)
- Figma (export to PDF)
- PowerPoint (export to PDF)

The file must be a PDF named `pitch-deck.pdf` committed to `05-fundraising/`.

### Slide-by-slide requirements

**Slide 1: Problem**
One sentence stating the problem. Name your ICP. State the pain intensity with evidence. Include one verbatim quote from an interview. The quote must be from a real interview documented in `01-discovery/interview-logs/`.

**Slide 2: Solution**
One sentence. References the ICP named in Slide 1. No feature list. No bullet points of functionality. One sentence that names what changes for the user.

**Slide 3: Why Now**
One specific development in the last two years that makes this solvable today. This is not "technology has improved." It is a named change: a regulatory shift, a platform becoming available, a cost threshold crossed, a behaviour change documented by data.

**Slide 4: Market Size**
TAM, SAM, and SOM built bottom-up. Show the arithmetic explicitly. TAM is the global total serviceable market. SAM is the portion your product model can realistically address. SOM is your realistic target in the next 24 months. Do not reference a top-down industry report figure without showing your own bottom-up calculation beneath it.

**Slide 5: Product**
A screenshot of the deployed live product. Not a mockup. Not a Figma prototype. The real deployed product on a real device. Include the live URL in the presenter notes of this slide.

**Slide 6: Traction**
Your most honest slide. Pull real numbers from your analytics dashboard. MAU or WAU. Retention rate at 7 days and 30 days. Total sessions. Bookings completed. Revenue if applicable. If you have an MOU or design partner letter, state it. All numbers must be verifiable in your analytics dashboard.

**Slide 7: Business Model**
How you make money. Your price point. CAC from your unit-economics.md file. LTV from your unit-economics.md file. Payback period. A simple table is cleaner than prose.

**Slide 8: Go-to-Market**
Your first channel. Specific cost per acquisition in that channel from your experiments. Your plan to reach the first 500 users by name of tactic, not category. Example: "KIU student WhatsApp groups and library notice boards" is specific. "Social media and word of mouth" is not.

**Slide 9: Competition**
Reproduce your competitive matrix from `06-strategy/competitive-analysis.md`. Five or more competitors. Seven or more evaluation dimensions. Your moat statement from `06-strategy/moat-statement.md` placed beneath the matrix. One sentence naming the Helmer power you are building.

**Slide 10: Ask**
If you are presenting this to real investors: state a specific dollar amount, at what valuation, and what three milestones this funding enables. For Demo Day purposes: state what you would ask for and what it would fund. Be specific. Vague asks indicate vague thinking about the business.

---

## Part 3: The One-Pager (1:00 to 1:15)

### The brief

A one-pager is what a judge takes away after Demo Day ends. It must communicate your product, traction, team, and business model on a single A4 page without you present to explain it.

Build it using the template in `templates/one-pager-template.md`. Export as a PDF named `one-pager.pdf` and commit to `05-fundraising/`.

### Required sections

| Section | Content | Word limit |
|---------|---------|-----------|
| Header | Product name, tagline, live URL | 15 words |
| Problem | Specific user, specific pain, measurable consequence | 40 words |
| Solution | What it does, for whom | 30 words |
| Traction | Three real numbers from your analytics | 30 words |
| Business Model | Price, CAC, LTV in a table | 40 words |
| Market | SAM and SOM with bottom-up number | 30 words |
| Team | Photo, name, one-line credential per member | 20 words per person |
| Ask | Amount, stage, contact email if applicable | 25 words |

### Design requirements

- Fits on one A4 page when printed at 100%.
- Font no smaller than 10pt for body text, 8pt minimum for labels.
- Your live product URL is the most prominent element after the product name.
- White space is deliberate. Do not fill every pixel.
- Print two copies per team. Bring them to Demo Day.

---

## Part 4: Team Pitch Run-Through (1:15 to 1:45)

### The brief

Each team delivers their full 7-minute pitch to the lab group. The instructor runs a strict timer. At exactly 7 minutes, the room stops. This is identical to the Demo Day constraint.

All team members must speak at least once during the 7 minutes. Judges at Demo Day evaluate the whole team, not just the presenter. Practice handing control between speakers cleanly.

After each pitch, the lab group delivers 3 minutes of structured feedback using the feedback form in `templates/pitch-feedback-form.md`. One form per team per pitch.

### Pitch structure reminder

| Section | Time |
|---------|------|
| Problem and Solution | 60 seconds |
| Why Now and Market | 60 seconds |
| Product Demo | 90 seconds |
| Traction and Business Model | 90 seconds |
| Go-to-Market and Competition | 60 seconds |
| Ask and Close | 30 seconds |

### What the instructor is checking

The instructor circulates and scores each pitch using the rubric in `GRADING-RUBRIC.md`. This score is not the final Checkpoint 4 score, which is assessed at Demo Day. Today's run-through is formative feedback to help you improve before the real event.

---

## Part 5: Launch Video Planning and Final Commit (1:45 to 2:00)

### The 60-second launch video

Your launch video is a required deliverable for Checkpoint 4. It is shot on a phone. It is 60 seconds maximum. It is committed to your repository via `09-final/demo-video.md` as a link or file path.

Use the planning worksheet in `templates/video-script-template.md` to script and plan your video during this session. You may shoot it during or immediately after lab.

**The five-section structure:**

| Section | Seconds | Content |
|---------|---------|---------|
| Hook | 0 to 10 | State the problem in one sentence. The viewer must feel the pain. |
| Problem | 10 to 25 | Show the old painful way. Real location. Real footage. |
| Product | 25 to 45 | Open your real product on a real device. One core user flow. No cuts. |
| Proof | 45 to 55 | One number that shows it is working. From your analytics. |
| Call to Action | 55 to 60 | Your URL or QR code. Say it clearly. |

### Final commit before leaving

Before you leave the lab, every file produced today must be committed and pushed to your repository. Run this check:

```bash
git status
git add 05-fundraising/pitch-deck.pdf
git add 05-fundraising/one-pager.pdf
git add 09-final/demo-video.md
git commit -m "Lab 12: pitch deck, one-pager, and video plan committed"
git push
```

Verify the push succeeded. Verify your repository is public. If your repository is private, judges cannot review it.

---

## Deliverables

### Due at end of lab (committed before leaving)

| File | Location | Status |
|------|----------|--------|
| Pitch deck (PDF) | `05-fundraising/pitch-deck.pdf` | Draft committed |
| One-pager (PDF) | `05-fundraising/one-pager.pdf` | Draft committed |
| Video plan | `09-final/demo-video.md` | Plan committed |

### Due by Thursday 11 June at 23:59 (Checkpoint 4)

| File | Location |
|------|----------|
| Pitch deck (final PDF) | `05-fundraising/pitch-deck.pdf` |
| One-pager (final PDF) | `05-fundraising/one-pager.pdf` |
| Demo video (link or file) | `09-final/demo-video.md` |
| Case study | `09-final/case-study.md` |
| Complete repository | All folders 00-foundation through 09-final |
| Professional README | Root `README.md` with live URL |
| Open-source licence | Root `LICENSE` file |

---

## Templates in This Package

| File | Purpose |
|------|---------|
| `templates/repo-audit-checklist.md` | Systematic check of all Checkpoint 4 requirements |
| `templates/pitch-deck-template.md` | Slide-by-slide fill-in template for the 10-slide deck |
| `templates/one-pager-template.md` | Structured one-pager layout with word limits |
| `templates/pitch-feedback-form.md` | Peer feedback form used during run-throughs |
| `templates/video-script-template.md` | 60-second video planning worksheet |
| `examples/example-pitch-deck-outline.md` | StudySpace Finders worked example for the pitch deck |
| `examples/example-one-pager.md` | StudySpace Finders worked example for the one-pager |

---

## Getting Help

**During lab:** Raise your hand. The instructor circulates at 0:15, 0:45, 1:15, and 1:50.

**Outside lab:** Email zeshan.ahmad@kiu.edu.ge. Include your team name and repository URL in the subject line.

**Office hours:** By appointment via Google Meet. Book by email.

---

*Lab 12 | CS-PD-2026 | Kutaisi International University | Spring 2026*
