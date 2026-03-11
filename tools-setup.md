# Tools Setup Guide

**Course:** CS-PD-2026 Product Development for Software Engineers  
**Kutaisi International University | Spring 2026**  

---

## Before You Read This

Set everything up in **Week 1 and Week 2**, not when you need it. A team that discovers a broken Figma account the night before a prototype is due has created a problem that did not need to exist.

Every tool in this document has a free tier that is sufficient for this course. You will not need to pay for anything. If a tool asks you to upgrade, you are on the wrong plan.

This guide tells you: what the tool is, when you need it, which plan to use, and exactly how to set it up.

---

## Quick Reference: What You Need and When

| Tool | Phase | First Used | Required |
|------|-------|-----------|----------|
| GitHub | All semester | Week 1 | Yes |
| Google Meet | All semester | Week 1 | Yes |
| Miro | Discovery and Design | Week 4 | Yes |
| Figma | Design | Week 6 | Yes |
| Mixpanel | Build and GTM | Week 7 | Yes (pick one) |
| Amplitude | Build and GTM | Week 7 | Yes (pick one) |
| Excalidraw | Build | Week 8 | Yes |
| Carrd | GTM | Week 10 | Yes (pick one) |
| Google Forms | Discovery and GTM | Week 3 | Yes |
| Google Sheets | GTM and Finance | Week 11 | Yes |
| Canva or Google Slides | Launch | Week 13 | Yes (pick one) |
| Loom | Launch | Week 14 | Yes |
| Notion | Optional | Any | No |
| Microsoft Clarity | Optional | Week 10 | No |

---

## Category 1: Foundation (Set Up in Week 1)

These tools are active from day one. Do not start the course without them.

---

### GitHub

**What it is:** Your team's version-controlled repository for all capstone work. Every document, interview log, piece of code, and decision record lives here.

**Why it matters:** GitHub is not a submission portal. It is the evidence base for your entire venture. Investors, graders, and future employers can read your commit history and understand how your product evolved. A well-maintained repo tells a story. A chaotic one with 11 commits all named "update" tells a different story.

**Plan:** Free personal account. All team repos live in the course organisation: `ZA-KIU-Classroom`.

**Setup steps:**
1. Go to [github.com](https://github.com) and create an account if you do not have one. Use a professional username -- this will be in your portfolio.
2. Set a profile photo and fill in your name in Settings. Anonymous contributors are hard to grade.
3. Enable two-factor authentication in Settings > Password and Authentication. This is required, not optional.
4. Accept the collaborator invitation to the course organisation when it arrives in your email. Without this you cannot access course materials.
5. In Week 2 Lab 1, your Tech Lead creates the team repo following the instructions in `Lab 1/resources/github-setup-guide.md`.

**Git client:** You can use the GitHub web interface for simple edits but you need a local Git installation for Lab 1 onwards.
- macOS: Git is pre-installed. Run `git --version` in Terminal to confirm.
- Windows: Install [Git for Windows](https://git-scm.com/download/win). During installation, choose "Use Git from the command line and also from 3rd-party software."
- Linux: `sudo apt install git` or equivalent.

Configure your identity after installing:
```bash
git config --global user.name "Your Full Name"
git config --global user.email "your.email@kiu.edu.ge"
```

**Recommended Git client (optional):** [GitHub Desktop](https://desktop.github.com) is a free GUI client that simplifies the commit-push workflow for students who are not comfortable with the command line. It is not a crutch -- use it if it helps you move faster.

---

### Google Meet

**What it is:** Video calling for office hours with the instructor and for team standups.

**Plan:** Free with any Google account.

**Setup steps:**
1. You need a Google account. Your KIU email may provide Google Workspace access -- confirm this in Week 1.
2. If your KIU email does not work with Google Meet, create a personal Gmail account.
3. Test a call with a teammate before Week 2 to confirm audio and video work.

**For office hours:** Email zeshan.ahmad@kiu.edu.ge with your availability and you will receive a Google Meet link. Do not show up without booking.

---

## Category 2: Discovery and Research (Set Up by Week 3)

These tools support the customer discovery phase, which begins in Lab 2 (Week 3). Have them ready before then.

---

### Google Forms

**What it is:** Free survey and data collection tool. Used in the discovery phase for screener surveys to recruit interview subjects, and later in the GTM phase for waitlist signups and experiment data collection.

**Plan:** Free with any Google account.

**Setup steps:**
1. Go to [forms.google.com](https://forms.google.com).
2. Sign in with your Google account.
3. Your first use will be in Lab 2 when you draft outreach messages. You may need a short screener survey to qualify interview candidates.

**Key tip:** Link your form responses to a Google Sheet automatically by clicking the Responses tab > Spreadsheet icon in any form. This makes tracking and sharing much easier.

**Alternative:** [Tally.so](https://tally.so) is a cleaner form builder with a generous free tier. Use it if you find Google Forms limiting.

---

### Miro

**What it is:** A collaborative online whiteboard. Used in Lab 4 for affinity mapping and synthesis workshops, and throughout the design phase for brainstorming and user journey mapping.

**Plan:** Free Starter plan. Supports unlimited team members on 3 boards. 3 boards is sufficient -- you will not need more unless you are very inefficient with board space.

**Setup steps:**
1. Go to [miro.com](https://miro.com) and click "Sign up free."
2. Use your email to create an account. Each team member needs their own account.
3. One team member creates a team workspace and invites the others. In Miro, click "Create a team" and send invitations via email.
4. Create your first board and name it `[Team Name] -- CS-PD-2026`.

**Education discount:** Miro offers a free Education plan with unlimited boards for verified students. Go to [miro.com/education](https://miro.com/education) and apply with your KIU email. If approved, you have unlimited boards. Apply in Week 1 -- verification can take a few days.

**Boards you will create across the semester:**
- Discovery board: affinity mapping, pattern clusters, Five Whys diagrams
- Design board: How Might We exercises, solution sketches, user flows
- Planning board: sprint planning, retrospective sticky notes

**Key Miro features to learn before Lab 4:**
- Sticky notes (N key)
- Frames (F key) -- used to organise sections of a board
- Voting (timer + dot voting for prioritisation exercises)
- Templates: search "Affinity Map" in the template library -- Miro has a built-in template that works well for Lab 4

---

## Category 3: Design and Prototyping (Set Up by Week 6)

---

### Figma

**What it is:** The industry-standard interface design and prototyping tool. You will use it to create wireframes (Lab 5), hi-fi prototypes (Lab 6), and your final pitch deck visuals.

**Plan:** Free Starter plan. Supports 3 projects, unlimited personal files, and 1 team with unlimited files in draft mode. This is sufficient.

**Education plan:** Figma offers a free verified Education plan that unlocks unlimited projects and team features. Go to [figma.com/education](https://www.figma.com/education/) and apply with your KIU email. Strongly recommended -- apply in Week 1.

**Setup steps:**
1. Go to [figma.com](https://figma.com) and sign up. Use the same email across your team.
2. Download the Figma desktop app from [figma.com/downloads](https://www.figma.com/downloads/). The browser version works but the desktop app is faster.
3. One team member creates a team and shares the project URL with teammates.
4. All team members must accept the invite and confirm they can open and edit a shared file before Lab 5.

**If you have never used Figma before:** Complete the official [Figma Basics tutorial](https://help.figma.com/hc/en-us/articles/360038006834) before Lab 5. It takes about 45 minutes and covers everything you need. Do not arrive at Lab 5 having never opened the tool.

**Key features you will use:**
- Frames: the container for each screen
- Auto Layout: for building responsive components
- Components: for reusing elements (buttons, nav bars) consistently
- Prototype tab: for linking frames into a clickable flow
- Comment mode: for async feedback from teammates

**Lo-fi vs hi-fi:** In Lab 5 you will start with lo-fi wireframes. These are intentionally low-detail -- black, white, and grey with placeholder text. The purpose is to test structure, not aesthetics. Resist the urge to add colour and style in the first round. Figma makes this easy: create a frame, draw rectangles, label them, link them. That is enough for a lo-fi prototype.

---

### Excalidraw

**What it is:** A free, lightweight diagramming tool with a hand-drawn aesthetic. Used in Lab 7 for system architecture diagrams and technical diagrams throughout the build phase.

**Plan:** Fully free, no account required. Optional account to save files.

**Why Excalidraw and not draw.io or Lucidchart:** Excalidraw's hand-drawn style signals to reviewers that diagrams are conceptual, not final specifications. This is appropriate at the architecture sketching stage. It also requires zero setup and runs entirely in the browser.

**Setup steps:**
1. Go to [excalidraw.com](https://excalidraw.com). No signup required.
2. Create an account at [excalidraw.com](https://excalidraw.com) if you want to save files to the cloud and collaborate in real time. Free accounts get this.
3. Use the "Share link" feature to share a live board with your team for collaborative diagramming.

**Export:** Export diagrams as PNG and commit them to your repository as `03-build/architecture/architecture-diagram.png`. Excalidraw also exports its native `.excalidraw` file format -- commit this too so diagrams can be edited later.

**Alternative:** [draw.io](https://app.diagrams.net) (also called diagrams.net) is a more formal diagramming tool. Use it if you prefer precise UML-style diagrams.

---

## Category 4: Analytics (Set Up by Week 7)

Your team will pick one analytics platform and use it throughout the build phase. Both options below are free for the usage levels you will reach in this course.

---

### Mixpanel

**What it is:** A product analytics platform that tracks user behaviour through custom events. You will define your event schema in Lab 5, implement tracking in Weeks 8-12, and analyse real user behaviour in the GTM phase.

**Plan:** Free plan includes 20 million monthly events, 90-day data history, unlimited users and reports. This is more than sufficient.

**Setup steps:**
1. Go to [mixpanel.com](https://mixpanel.com) and sign up.
2. Create a new project named `[Team Name] CS-PD-2026`.
3. In your project settings, invite all team members as editors.
4. Copy your Project Token from Settings > Project Details. You will need this when integrating the SDK into your codebase.
5. Select the appropriate SDK for your tech stack: JavaScript, Python, Node.js, iOS, Android, and others are available at [developer.mixpanel.com](https://developer.mixpanel.com).

**Recommended:** Create both a Development and Production project in Mixpanel. Track test events in Development and keep your Production data clean from the start. This is standard practice and takes two minutes to set up.

---

### Amplitude

**What it is:** Mixpanel's main competitor. Slightly stronger in funnel analysis and retention cohorts; Mixpanel is slightly stronger in event flexibility. Both are appropriate for this course.

**Plan:** Free Starter plan includes unlimited events, unlimited users, and unlimited charts.

**Setup steps:**
1. Go to [amplitude.com](https://amplitude.com) and sign up.
2. Create a project named `[Team Name] CS-PD-2026`.
3. Invite team members under Settings > Members.
4. Copy your API Key from Settings > Projects. You will need this for SDK integration.
5. SDK documentation at [www.docs.developers.amplitude.com](https://www.docs.developers.amplitude.com).

**Which should you pick?** If your team is building a web app, either is fine -- both have strong JavaScript SDKs. If you are building a mobile app, Amplitude's mobile SDKs are marginally more mature. If half your team has already used one or the other, use the one they know.

---

### Google Analytics 4 (GA4)

**What it is:** Google's free web analytics platform. Less powerful than Mixpanel or Amplitude for product analytics specifically, but completely free and widely known.

**Use case:** Suitable if you are building a content site or a product where pageviews and acquisition source are more important than specific user actions. Not recommended if your product has complex in-app behaviour you need to track.

**Plan:** Free, unlimited.

**Setup steps:**
1. Go to [analytics.google.com](https://analytics.google.com).
2. Create an account and a property for your project.
3. Add the GA4 tag to your web app via Google Tag Manager (recommended) or by pasting the snippet directly into your HTML.

---

## Category 5: Go-to-Market (Set Up by Week 10)

---

### Landing Page Builder

You will build a GTM experiment landing page in Lab 8. Pick one of the following and set it up before then.

**Option A: Carrd**  
Best for: simple, single-section landing pages. Fast to build, clean output.  
Plan: Free tier supports 3 sites. Sufficient.  
Setup: [carrd.co](https://carrd.co) > Sign up > Create site.  
Limitation: Very limited layout flexibility on the free tier.

**Option B: Typedream**  
Best for: slightly richer landing pages with more layout options than Carrd.  
Plan: Free tier supports 1 published site.  
Setup: [typedream.com](https://typedream.com) > Sign up > New site.

**Option C: Webflow**  
Best for: teams who want full design control and a professional-grade output.  
Plan: Free Starter plan supports 2 projects with a `.webflow.io` subdomain.  
Setup: [webflow.com](https://webflow.com) > Sign up > New project.  
Limitation: Steeper learning curve. Do not choose Webflow if your team has never used it and you are under time pressure.

**Option D: GitHub Pages with plain HTML**  
Best for: teams with frontend development skills who want complete control.  
Plan: Fully free.  
Setup: Create an `index.html` in your repo, go to Settings > Pages, and enable GitHub Pages on the main branch.  
Limitation: You are writing HTML. If your team is comfortable with this, it is the most flexible option.

**Which to pick:** If you are unsure, choose Carrd. It takes 30 minutes to build a functional landing page and the output is clean enough for a GTM experiment.

---

### Typeform

**What it is:** A more polished form and survey tool than Google Forms. Used for waitlist signups on landing pages and for interview screening when you want a better user experience.

**Plan:** Free Basic plan. Supports 10 questions per form and 10 responses per month. This is tight -- consider upgrading to the Plus plan if you are running a GTM experiment with significant traffic.

**Alternative:** [Tally.so](https://tally.so) has no response limit on the free plan and is cleaner than Google Forms. Recommended over Typeform for most use cases in this course.

**Setup steps:**
1. Go to [tally.so](https://tally.so) or [typeform.com](https://typeform.com) and sign up.
2. Create a form for your waitlist. Keep it to 3 fields or fewer: name, email, and optionally one qualifying question.
3. Copy the embed link and paste it into your landing page.

---

## Category 6: Financial Modelling (Set Up by Week 11)

---

### Google Sheets

**What it is:** Collaborative spreadsheet tool. Used in Lab 11 for unit economics and the 12-month financial model.

**Plan:** Free with any Google account.

**Setup steps:**
1. You already have this from your Google account setup in Week 1.
2. In Week 11, one team member creates the financial model spreadsheet and shares it with editor access to all teammates.
3. Commit a link to the spreadsheet as `04-gtm/financials/12-month-model-link.md` in your repo. Do not commit the spreadsheet file -- link to it.

**A note on financial modelling:** The 12-month model you produce in Lab 11 does not need to be complex. It needs to be honest. A model with three tabs -- revenue assumptions, cost assumptions, and a monthly P&L -- that is clearly tied to your real pricing and unit economics is worth more than a sophisticated model built on numbers you invented.

---

## Category 7: Pitch and Demo Day (Set Up by Week 13)

---

### Pitch Deck Tool

You will present a 5-minute investor pitch on Demo Day in Week 15. Your pitch deck must be visually professional. Pick one tool and commit to it.

**Option A: Figma (recommended)**  
If your team is already using Figma for prototyping, building the pitch deck there keeps everything in one tool. Figma's presentation mode (View > Present) renders slides full-screen and handles slide navigation cleanly.  
Use the free Presentation template in Figma's community ([figma.com/community](https://www.figma.com/community)) as a starting point. Search "pitch deck."

**Option B: Canva**  
Canva is the fastest way to produce a visually polished deck with no prior design experience.  
Plan: Free tier has hundreds of pitch deck templates and is fully sufficient.  
Setup: [canva.com](https://canva.com) > Sign up > search "pitch deck" in templates.  
Education plan: [canva.com/education](https://canva.com/education) gives free Canva Pro to verified students and teachers.

**Option C: Google Slides**  
Reliable, collaborative, free, and produces decent output if you use a clean template.  
Avoid the default Google Slides themes -- they are visually dated and signal low effort. Download a free professional template from [slidesgo.com](https://slidesgo.com) or [slidescarnival.com](https://www.slidescarnival.com).

**What the deck must contain (regardless of tool):**
- Cover: team name, product name, one-sentence value proposition
- Problem: the specific problem with evidence from your discovery
- Solution: your product, shown live or in prototype
- Traction: your best real metric (users, signups, interviews, anything real)
- Business model: how you make money
- Ask: what you need next (even if hypothetical for this course)

8 to 12 slides. No more. Investors stop listening after slide 12.

---

### Loom

**What it is:** Screen and webcam recording tool. Used in Week 14-15 to record your demo video, which forms part of the venture packet submitted via GitHub.

**Plan:** Free Starter plan includes 25 videos with a 5-minute limit per video. The demo video should be under 3 minutes, so this is sufficient.

**Setup steps:**
1. Go to [loom.com](https://loom.com) and sign up.
2. Install the Loom desktop app or Chrome extension.
3. Test a recording before Week 14: open your product, hit record, narrate a 2-minute walkthrough of the core user flow.
4. Once recorded, Loom generates a shareable link immediately. Commit the link as `09-final/demo-video.md` in your capstone repo.

**Education plan:** Loom offers free Education accounts with unlimited video and no time limit. Go to [loom.com/education](https://www.loom.com/education) and apply with your KIU email. Apply in Week 1 -- do not discover this option the night before the demo video is due.

---

## Category 8: Optional but Useful

These tools are not required but will improve your work if you use them.

---

### Microsoft Clarity

**What it is:** Free heatmap and session recording tool from Microsoft. Adds to your site in 5 minutes and records real user sessions, showing where people click, scroll, and get confused.

**Plan:** Completely free, no limits.

**When to use it:** Install it on your GTM landing page and your live MVP. The session recordings in Week 11 and 12 will often reveal usability issues that analytics events do not surface.

**Setup:** [clarity.microsoft.com](https://clarity.microsoft.com) > Sign up > Add project > Copy the snippet into your site's `<head>`.

---

### Notion

**What it is:** An all-in-one note-taking and documentation tool. Some teams use it for meeting notes, sprint planning, and personal organisation.

**Plan:** Free personal plan is unlimited for individuals.

**Note:** Your capstone work lives in GitHub, not Notion. If your team uses Notion for planning, ensure all formal deliverables are also committed to your GitHub repo. Notion content is not gradeable.

---

### Hotjar

**What it is:** A heatmap, session recording, and user feedback tool. Similar to Microsoft Clarity but with more features on the free tier.

**Plan:** Free Basic plan includes 35 daily sessions.

**When to use it:** An alternative to Microsoft Clarity. Pick one, not both.

---

## Team Setup Checklist

Complete this together in Week 1 and Week 2. Every person on the team should complete their own row.

**All members -- required before Lab 1:**
- [ ] GitHub account created with professional username and profile photo
- [ ] Two-factor authentication enabled on GitHub
- [ ] Course organisation invitation accepted
- [ ] Git installed and configured locally (`git config --global user.name` and `user.email`)
- [ ] Google account confirmed for Google Meet
- [ ] Miro account created

**All members -- required before Lab 5:**
- [ ] Figma account created
- [ ] Figma Education plan applied for (do this in Week 1, not Week 5)
- [ ] Figma desktop app installed
- [ ] Test file opened and edited in Figma

**One member (Tech Lead) -- required before Lab 7:**
- [ ] Mixpanel or Amplitude project created with team invited
- [ ] Development project created separately from Production project
- [ ] API key or Project Token recorded and shared with team securely

**All members -- required before Lab 8:**
- [ ] Carrd (or chosen landing page tool) account created
- [ ] Tally.so or Typeform account created
- [ ] Excalidraw tested (no account needed)

**All members -- required before Lab 12:**
- [ ] Loom account created
- [ ] Loom Education plan applied for
- [ ] Test recording completed and link confirmed working

---

## A Note on Tool Sprawl

The list above can feel overwhelming. The principle is simple: use the minimum number of tools that lets your team do quality work. If your team is already comfortable with a different diagramming tool than Excalidraw, use that. If your team prefers a different landing page builder than Carrd, use that.

The only tools where there is no flexibility are GitHub (non-negotiable), a prototyping tool (Figma is strongly recommended), and an analytics platform (pick one and implement it properly -- a half-integrated analytics setup produces meaningless data).

Everything else is a means to an end. The end is a working product with real users and real data, presented with confidence on Demo Day.

---

## Getting Help with Tools

If a tool is blocking you, contact zeshan.ahmad@kiu.edu.ge before the deadline, not at it. Most tool issues are resolved in 10 minutes if caught early.

For GitHub-specific issues, the Lab 1 `resources/github-setup-guide.md` covers the most common problems including merge conflicts, permission errors, and tag creation.

---

*CS-PD-2026 | Kutaisi International University | Spring 2026*
