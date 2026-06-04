# Pitch Deck Template

**Team name:** [Your team name]
**Product name:** [Your product name]
**Date:** Thursday 4 June 2026 or Friday 5 June 2026
**Version:** Draft 1 (complete during Lab 12)

When you are done, export this as a PDF using your presentation tool of choice. Commit the PDF to `05-fundraising/pitch-deck.pdf`. Do not commit this markdown file as your pitch deck. The PDF is what judges receive.

---

## How to use this template

Each slide section below contains:

- The **one job** that slide must accomplish
- A **content prompt** telling you exactly what to write
- A **StudySpace Finders example** showing what a filled version looks like
- A **quality check** you must pass before moving to the next slide

Work through all 10 slides in order. Draft all 10 with real content before polishing any of them.

---

## Slide 1: Problem

**One job:** Make the judge feel the pain of one specific person before you say a single word about your product.

**Content prompt:**

Write one sentence that names your ICP and the pain they experience. Then answer: how often does this happen? How bad is it? What does it cost them (time, money, stress, opportunity)?

Support your problem statement with one verbatim quote from a real interview in your `01-discovery/interview-logs/` folder. The quote must be from a real documented interview. If you cannot cite the interview log file and quote number, you cannot use the quote.

---

**Your ICP:**

[Who specifically is this person? Name their role, context, and the moment they experience the pain.]

**Your problem statement (one sentence):**

[Write it here. If it is longer than 25 words, cut it.]

**Pain intensity evidence:**

[How frequently does this happen? What measurable consequence does it cause?]

**Real interview quote (with source):**

Quote: "[Verbatim quote from a real interview]"
Source: Interview log file name, interview number, date of interview.

---

**StudySpace Finders example:**

ICP: KIU students studying for exams who cannot find a quiet space with available seating and power sockets on short notice.

Problem statement: KIU students waste an average of 18 minutes per study session searching for available workspace, with no real-time visibility into which spaces are free.

Pain intensity: Happens 3 to 4 times per week during exam season. Causes late arrivals to study groups and reduced effective study time.

Quote: "I walked through four floors of the library last Tuesday and every seat was taken. I ended up studying on the floor of a corridor."
Source: interview-logs/interview-007.md, Quote 2, collected 14 March 2026.

---

**Quality check before moving on:**

- [ ] ICP is named and specific (not "students" or "users")
- [ ] Problem is one sentence, 25 words or fewer
- [ ] Pain is quantified or evidenced, not just described
- [ ] Interview quote is real and the source file is cited

---

## Slide 2: Solution

**One job:** State in one sentence what changes for the ICP named in Slide 1 when they use your product.

**Content prompt:**

Write one sentence. No bullet points. No feature list. No technical description. The sentence must reference the same ICP from Slide 1 and name the outcome they get, not the mechanism by which they get it.

---

**Your solution statement (one sentence):**

[Write it here.]

**The core user action (one sentence describing what the user actually does):**

[What does the user do in your product to achieve the outcome above?]

---

**StudySpace Finders example:**

Solution statement: StudySpace Finders lets KIU students find and book an available study space with the right amenities in under 60 seconds from their phone.

Core user action: The user opens the app, enters their preferred noise level and required amenities, sees real-time availability across campus, and books a space in three taps.

---

**Quality check before moving on:**

- [ ] Solution is one sentence
- [ ] Solution references the ICP from Slide 1 by name
- [ ] Solution names an outcome, not a feature list
- [ ] No technical jargon

---

## Slide 3: Why Now

**One job:** Name one specific development in the last two years that makes this problem solvable today when it was not before.

**Content prompt:**

This is not "technology has improved." Name the specific change. It could be a platform that became available (a specific API, a tool, a regulatory ruling), a behaviour change you can evidence (data showing students using mobile for X), a cost that dropped to a threshold, or a competitor that proved the market exists and left a gap.

---

**The specific change (one sentence):**

[Name it. Date it if possible.]

**Why this change matters for your product specifically:**

[Two to three sentences explaining the causal link between the change and your product's viability.]

---

**StudySpace Finders example:**

Specific change: The KIU library system introduced an API for room availability data in September 2025, making real-time occupancy data accessible to third-party applications for the first time.

Why it matters: Before this API existed, any attempt to show real-time space availability required manual data entry or sensor hardware costing tens of thousands of euros. The API removes that barrier entirely, making a real-time booking layer viable at zero infrastructure cost.

---

**Quality check before moving on:**

- [ ] A specific named change is stated, not a general trend
- [ ] The change is dated or can be verified
- [ ] The causal link to your product's viability is explicit

---

## Slide 4: Market Size

**One job:** Show the size of the opportunity using numbers you built yourself, not borrowed from an industry report.

**Content prompt:**

Build your market size bottom-up. Start with the smallest defensible number (your SOM: how many users can you realistically reach in 24 months?). Build up to SAM and then TAM. Show the arithmetic on the slide or in presenter notes.

Do not open with "the global EdTech market is $350 billion." Open with your own numbers and let judges extrapolate upward.

---

**SOM (Serviceable Obtainable Market): your realistic 24-month target**

Number of users: [X]
At what price per user per period: [Y]
Frequency of payment or interaction: [Z times per year]
SOM calculation: X times Y times Z = [your SOM in currency]

**SAM (Serviceable Addressable Market): the portion of the total market your model can address**

Describe the boundary: [What defines your SAM? Geography? User type? Platform constraint?]
SAM estimate: [Number of potential users] times [price] = [SAM in currency]

**TAM (Total Addressable Market): the full global market if you had 100% penetration**

TAM estimate: [Total market users globally] times [price] = [TAM in currency]
Source or rationale for total user count: [How did you arrive at the total?]

---

**StudySpace Finders example:**

SOM: 2,400 KIU students times 8 GEL per month times 12 months = 230,400 GEL per year. Achievable in 24 months based on current 230-user base and word-of-mouth growth rate.

SAM: 120,000 students across Georgian universities with comparable campus infrastructure. 120,000 times 8 GEL times 12 months = 11.5 million GEL per year.

TAM: 50 million university students in Europe with campus space scarcity as a documented problem. 50 million times 8 GEL times 12 months = 4.8 billion GEL per year (approximately 1.6 billion EUR).

---

**Quality check before moving on:**

- [ ] SOM is the smallest number and is based on users you could realistically reach
- [ ] All three numbers are calculated from first principles, not borrowed from a report
- [ ] The arithmetic is visible either on the slide or in presenter notes
- [ ] The progression from SOM to TAM is coherent (SOM is a subset of SAM which is a subset of TAM)

---

## Slide 5: Product

**One job:** Show the real deployed product on a real device. Nothing else.

**Content prompt:**

Take a screenshot of your live deployed product. Not Figma. Not a mockup. Not a demo environment with fake data. The live URL, loaded in a browser or on a device, showing real content.

If your product requires login, show the logged-in state. If your product shows user data, show real anonymised data from a real user session. If your core value is visible on first load (a map, a search result, a dashboard), make sure that is what is in the screenshot.

Include your live URL beneath the screenshot. Place the full URL in the presenter notes of this slide.

---

**Screenshot:** [Insert screenshot of live product here]

**Caption (one sentence describing what the user is seeing in the screenshot):**

[Write it here.]

**Live URL:** [Paste your full live URL here]

**Presenter notes (URL and any demo talking points):**

[Write your presenter notes here. Include the URL. Include what you will say while showing the product for 90 seconds during the live demo portion of the pitch.]

---

**StudySpace Finders example:**

Caption: A student has searched for a quiet space with power sockets available right now, and the app is showing three results on the KIU campus with real-time occupancy indicators.

Live URL: https://studyspace-finders.vercel.app

Presenter notes: "This is the live product, logged in as a student account. What you can see is a real-time availability view. These green indicators are live. I am going to tap on Room 304 in the Engineering block, which shows 3 of 8 seats available. I book it in three taps. Confirmation goes to my phone. This booking is now in the database."

---

**Quality check before moving on:**

- [ ] Screenshot is of the live deployed product, not a mockup or prototype
- [ ] Live URL is on the slide and in presenter notes
- [ ] Screenshot shows something that communicates value instantly, not a login screen
- [ ] Presenter notes contain a scripted 90-second talking track for the live demo

---

## Slide 6: Traction

**One job:** Show your most honest numbers. Real data from real users. Nothing projected.

**Content prompt:**

Open your analytics dashboard right now. Pull the exact numbers. Do not round up. Do not use numbers you remember from last month. The number on this slide and the number in your dashboard must match.

If your numbers are small, be honest about what they are and frame them accurately. Three active users with 80% weekly retention is a better story than claiming 200 "signups" who never returned.

---

**Primary traction metric (your most important number):**

Metric name: [e.g. Weekly Active Users]
Current value: [Pull from your dashboard right now]
Source: [Your analytics dashboard name and URL]
Date of data pull: [Today's date]

**Secondary metrics (2 to 3 supporting numbers):**

| Metric | Value | Source |
|--------|-------|--------|
| [Metric 1, e.g. Day-7 retention rate] | [Value] | [Source] |
| [Metric 2, e.g. Sessions per active user per week] | [Value] | [Source] |
| [Metric 3, e.g. Total bookings completed] | [Value] | [Source] |

**Qualitative traction (if applicable):**

MOUs signed: [Number and with whom]
Design partners: [Names of organisations if applicable]
Waitlist: [Number if applicable]
User testimonials: [One short quote if you have one]

**Growth trend (if your data shows it):**

[Describe the trend line. If you have been live for 6 weeks, show week-by-week user counts. Growth is more compelling than a single data point.]

---

**StudySpace Finders example:**

Primary metric: 230 Weekly Active Users as of 3 June 2026.
Source: Mixpanel dashboard, event "session_start" unique users over last 7 days.

Secondary metrics:
- Day-7 retention rate: 61%
- Average sessions per active user per week: 3.2
- Total bookings completed: 847

Qualitative: MOU signed with KIU Library Services for data access. Shortlisted for KIU Innovation Fund.

Growth trend: Week 1 launch: 12 WAU. Week 4: 89 WAU. Week 8: 230 WAU. Doubling approximately every 3 weeks.

---

**Quality check before moving on:**

- [ ] Every number was pulled from your live analytics dashboard today
- [ ] The primary metric is clearly named (WAU, MAU, bookings, revenue, etc.)
- [ ] Numbers are internally consistent (e.g. WAU does not exceed total signups)
- [ ] No projected numbers appear on this slide. Projections belong in the financial model, not the traction slide.

---

## Slide 7: Business Model

**One job:** Show how you make money and whether the unit economics make sense.

**Content prompt:**

Pull your CAC and LTV numbers from `04-gtm/financials/unit-economics.md`. If that file has template text rather than real numbers, stop and calculate them now before filling in this slide.

---

**Pricing:**

How do users pay? [Subscription / transactional / freemium with premium tier / institutional licence / other]
Price per user per period: [Amount and currency]
Free tier (if applicable): [What is free and what is paid?]

**Unit Economics:**

| Metric | Value | Source file |
|--------|-------|-------------|
| Customer Acquisition Cost (CAC) | [Amount] | unit-economics.md |
| Customer Lifetime Value (LTV) | [Amount] | unit-economics.md |
| LTV to CAC ratio | [Ratio] | Calculated |
| Payback period | [Months] | Calculated |
| Gross margin | [Percentage] | unit-economics.md |

**Revenue to date (if applicable):**

[Amount and currency. If zero, state "pre-revenue" and explain what milestone triggers first revenue.]

---

**StudySpace Finders example:**

Pricing: Freemium. Free tier: 3 bookings per month. Premium: 8 GEL per month for unlimited bookings and noise level filters. Institutional licence: 150 GEL per month for universities to access occupancy analytics.

Unit Economics:
- CAC (student channel): 3.20 GEL via WhatsApp group referrals
- CAC (institutional channel): 0 GEL (inbound from library administration)
- LTV (student, 8-month academic year): 64 GEL
- LTV to CAC ratio: 20:1
- Payback period: 0.4 months
- Gross margin: 91% (cloud infrastructure only variable cost)

Revenue to date: Pre-revenue. Institutional licensing pilot begins September 2026.

---

**Quality check before moving on:**

- [ ] CAC and LTV are sourced from unit-economics.md, not estimated on the spot
- [ ] LTV to CAC ratio is at least 3:1 (if it is not, note it and explain your path to improving it)
- [ ] Pricing is stated in specific numbers, not "we are exploring monetisation"
- [ ] Gross margin is calculated and shown

---

## Slide 8: Go-to-Market

**One job:** Name your first channel and show that you have tested it.

**Content prompt:**

This is not a list of every channel you might use. It is a specific plan for reaching your first 500 users via one primary channel, with evidence that you have already tested it. Pull your channel experiment results from `04-gtm/experiments/`.

---

**Primary acquisition channel:**

Channel name: [Be specific. "Social media" is not specific. "KIU student WhatsApp groups" is specific.]
CAC in this channel (from your experiments): [Amount]
Conversion rate from reach to activation: [Percentage]
Current users acquired via this channel: [Number]

**First 500 users plan:**

Starting from [current user count], reaching 500 users requires acquiring [X] more users.

At a CAC of [amount] in the primary channel, this costs [total cost].

Timeline: [Number of weeks] weeks at current growth rate, or [weeks] with [specific tactic] acceleration.

**Secondary channel (if applicable):**

[Name the second channel, its CAC, and why you are not leading with it.]

---

**StudySpace Finders example:**

Primary channel: KIU student WhatsApp groups and course announcement channels.
CAC: 3.20 GEL (cost of printed QR code cards distributed to 3 group administrators).
Conversion rate: 18% from link click to completed first booking.
Current users acquired via this channel: 187 of 230 total WAU.

First 500 users plan: Need 270 more users. At 3.20 GEL CAC, total acquisition cost is 864 GEL. At current weekly growth rate of 28 new users per week, reach 500 in 10 weeks. With a coordinated push during September exam registration, can reach 500 in 4 weeks.

Secondary channel: KIU library notice boards with QR codes. CAC unknown (in test). Not leading with this because it cannot be measured as precisely as the WhatsApp channel.

---

**Quality check before moving on:**

- [ ] One primary channel is named specifically, not categorically
- [ ] CAC for that channel is sourced from a real experiment in your repository
- [ ] The first 500 users plan is arithmetic, not aspiration
- [ ] You are not claiming "viral growth" or "word of mouth" without data showing it is happening

---

## Slide 9: Competition

**One job:** Show that you understand your market better than any competitor does, and name the structural advantage that makes you hard to copy.

**Content prompt:**

Reproduce your competitive matrix from `06-strategy/competitive-analysis.md`. It must have 5 or more named competitors and 7 or more evaluation dimensions. Choose dimensions where your product leads or where competitors have a genuine gap.

Place your moat statement from `06-strategy/moat-statement.md` beneath the matrix. Name the Helmer power explicitly.

---

**Competitive Matrix:**

Copy your matrix from `06-strategy/competitive-analysis.md` here. If it is not complete, stop and complete it now before continuing.

| Competitor | [Dimension 1] | [Dimension 2] | [Dimension 3] | [Dimension 4] | [Dimension 5] | [Dimension 6] | [Dimension 7] |
|------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| [Competitor 1] | | | | | | | |
| [Competitor 2] | | | | | | | |
| [Competitor 3] | | | | | | | |
| [Competitor 4] | | | | | | | |
| [Competitor 5] | | | | | | | |
| **[Your product]** | | | | | | | |

**Moat statement (one paragraph, sourced from moat-statement.md):**

[Copy your moat statement here. It must name the Helmer power and cite at least two pieces of evidence from your repository.]

---

**StudySpace Finders example:**

Moat statement: StudySpace Finders is building a Cornered Resource moat through exclusive data partnerships with KIU Library Services and the Engineering block facilities team. Our real-time occupancy dataset, now spanning 847 completed bookings and 8 weeks of continuous sensor data from 3 buildings, cannot be replicated by a new entrant without negotiating separate institutional agreements with each building administrator. This is evidenced by our signed MOU with KIU Library Services (01-discovery/synthesis/competitive-landscape-seed.md) and the occupancy data pipeline in our repository (03-build/architecture/data-pipeline.md). The data advantage compounds with every booking: each session improves our availability prediction model, raising switching costs for institutions already using our analytics dashboard.

---

**Quality check before moving on:**

- [ ] 5 or more named competitors in the matrix (not "other apps" or "manual processes" without a name)
- [ ] 7 or more evaluation dimensions
- [ ] Your product does not score highest on every dimension (that signals the matrix is not honest)
- [ ] Moat statement names a specific Helmer power
- [ ] Moat statement cites at least two pieces of evidence from actual repository files
- [ ] "There is no real competition" does not appear anywhere on this slide

---

## Slide 10: Ask

**One job:** State exactly what you want and what it enables.

**Content prompt:**

Name a specific amount. Name a valuation method. Name three line items that the capital funds. Name the milestone that reaching this funding enables.

For Demo Day purposes, this slide demonstrates that you have thought rigorously about the economics of your business. Even if you are not actually fundraising right now, judges evaluate whether you understand what your business needs to reach the next stage.

---

**The ask:**

We are raising: [Amount and currency]
At a pre-money valuation of: [Amount] implied by: [VC method / comps / other, with one-line explanation of your method]
This represents: [Percentage] dilution

**Use of funds (three line items only):**

| Line item | Amount | Purpose |
|-----------|--------|---------|
| [Item 1, e.g. Engineering hire] | [Amount] | [What specifically this funds and for how long] |
| [Item 2, e.g. Institutional sales] | [Amount] | [What specifically this funds and for how long] |
| [Item 3, e.g. Infrastructure and compliance] | [Amount] | [What specifically this funds and for how long] |

**The milestone this capital funds:**

By [Date], with this capital, we will: [Specific, measurable outcome. Users, revenue, partnerships, or market expansion. Not "scale the product."]

**Contact:**

Team name: [Your team name]
Email: [Team contact email]
Repository: [Your GitHub repository URL]
Live product: [Your live URL]

---

**StudySpace Finders example:**

We are raising 75,000 GEL at a pre-money valuation of 300,000 GEL, implying 20% dilution. Valuation derived by VC method: projected exit at 2.4 million GEL in year 5 (20x current institutional contract value if scaled to 8 universities), discounted 75% for early-stage risk.

Use of funds:
- Engineering (part-time backend engineer, 12 months): 36,000 GEL. Funds real-time sensor integration and the institutional analytics dashboard.
- Institutional sales (3 university partnership campaigns): 24,000 GEL. Funds partnership negotiation, onboarding, and 90-day free trials for 3 new institutions.
- Infrastructure and legal (cloud hosting, GDPR compliance audit): 15,000 GEL. Funds 12 months of Vercel Pro and a legal review of our data handling agreements.

Milestone: By March 2027, with this capital, we will have 3 signed institutional licence agreements generating 5,400 GEL per month in recurring revenue and 2,000 monthly active student users across 4 university campuses.

---

**Quality check before moving on:**

- [ ] A specific amount is named (not "we are raising a seed round")
- [ ] A valuation method is named and briefly explained
- [ ] Exactly three use-of-funds line items are present
- [ ] The milestone is specific and measurable, not directional
- [ ] Contact information is present and accurate

---

## Final export checklist

Before exporting to PDF:

- [ ] All 10 slides have real content. No placeholder brackets remain.
- [ ] Every number on every slide has been verified against its source today
- [ ] Slide 5 shows the live product (not a mockup)
- [ ] Slide 9 matrix has 5 or more competitors and 7 or more dimensions
- [ ] The file is exported as PDF
- [ ] PDF is named exactly `pitch-deck.pdf`
- [ ] PDF is committed to `05-fundraising/pitch-deck.pdf`

---

*Pitch Deck Template | Lab 12 | CS-PD-2026 | Spring 2026*
