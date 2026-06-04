# Example: Pitch Deck Outline

**Product:** StudySpace Finders
**Team:** Team Sigma (Ana Beridze, Nino Kvaratskhelia, David Chikvanaia)
**Date:** 4 June 2026

This is a worked example for instructional purposes only. It shows what a complete, honest, and well-evidenced pitch deck outline looks like for the StudySpace Finders reference product. Use it to calibrate the standard expected for your own deck. Do not copy it. Your deck must reflect your actual product and your actual data.

---

## Slide 1: Problem

**ICP:** KIU postgraduate and final-year undergraduate students studying during exam season, especially between 18:00 and 23:00 on weekdays.

**Problem statement:** KIU students waste an average of 18 minutes per study session searching for available workspace because no real-time visibility into campus space occupancy exists.

**Pain intensity evidence:** In 25 interviews, 21 students described arriving at the library during peak hours only to find no available seats. 14 described leaving campus entirely and studying at home as a result. Average reported time lost per session: 18 minutes. Reported frequency: 3 to 4 times per week during exam season.

**Interview quote:** "I walked through four floors last Tuesday and every seat was taken. I ended up studying on the floor of a corridor for two hours." Source: interview-logs/interview-007.md, Quote 2, 14 March 2026.

---

## Slide 2: Solution

**Solution statement:** StudySpace Finders lets KIU students find and book an available study space with the right amenities in under 60 seconds from their phone.

**Core user action:** The user opens the app, filters by noise level and required amenities (power sockets, whiteboard, group or solo), sees real-time availability across campus, and books a space in three taps.

---

## Slide 3: Why Now

**Specific change:** KIU Library Services introduced a room availability API in September 2025, making real-time occupancy data accessible to third-party applications for the first time.

**Why it matters for this product:** Before this API, any real-time availability layer required either manual data entry (infeasible at scale) or physical sensor hardware costing 15,000 to 40,000 EUR per building. The API reduces the infrastructure cost of a real-time layer to zero. The gap between when the problem has existed (years) and when a solution became viable (September 2025) is the "why now" that no earlier product could answer.

---

## Slide 4: Market Size

**SOM calculation:**
- KIU students who study on campus regularly: approximately 2,400
- Premium subscription price: 8 GEL per month
- Academic year: 10 months
- SOM: 2,400 x 8 x 10 = 192,000 GEL per year
- Realistic 24-month penetration at current growth rate: 40%, giving 76,800 GEL ARR

**SAM calculation:**
- Georgian university students with comparable campus infrastructure: approximately 120,000
- SAM: 120,000 x 8 x 10 = 9,600,000 GEL per year

**TAM calculation:**
- European university students with campus space scarcity: approximately 50 million (source: Eurostat 2024 tertiary enrolment data)
- TAM: 50,000,000 x 8 x 10 = 4,000,000,000 GEL per year (approximately 1.35 billion EUR)

---

## Slide 5: Product

**Screenshot description:** The main discovery screen showing three available study spaces in the KIU Engineering block. Each result shows a space name, current occupancy as a percentage, noise level rating, available amenities as icons, and a Book button. A real booking confirmation screen follows.

**Live URL:** https://studyspace-finders.vercel.app

**Presenter notes for live demo:** Open the app on the Android device. Logged in as student account. Say: "This is the live product, running right now, with real availability data from the KIU library API. I am going to filter for a quiet space with power sockets available in the next hour." Tap the filter. Three results appear. Say: "Room 304, Engineering block, three of eight seats available. I will book it." Tap Book. Confirmation appears with a booking reference. Say: "That took eight seconds. The space is now reserved in the database."

---

## Slide 6: Traction

**Primary metric:** 230 Weekly Active Users as of 3 June 2026. Source: Mixpanel, event "session_start" unique users, rolling 7-day window.

**Supporting metrics:**

| Metric | Value | Source | Date |
|--------|-------|--------|------|
| Day-7 retention rate | 61% | Mixpanel cohort analysis | 3 Jun 2026 |
| Sessions per WAU per week | 3.2 | Mixpanel | 3 Jun 2026 |
| Total bookings completed | 847 | Supabase bookings table | 3 Jun 2026 |
| Day-30 retention rate | 44% | Mixpanel cohort analysis | 3 Jun 2026 |

**Growth trend:** Week 1 post-launch (8 Apr 2026): 12 WAU. Week 4: 89 WAU. Week 8: 230 WAU. Compound weekly growth rate: approximately 28%.

**Qualitative traction:** Signed MOU with KIU Library Services for continued API access and co-marketing. Shortlisted (not yet awarded) for the KIU Innovation Fund 2026.

---

## Slide 7: Business Model

**Pricing:** Freemium. Free tier: 3 space bookings per month. Premium: 8 GEL per month, unlimited bookings and advanced filters. Institutional licence: 150 GEL per month, gives the institution access to occupancy analytics and usage reports.

**Unit economics (from unit-economics.md):**

| Metric | Student channel | Institutional channel |
|--------|----------------|----------------------|
| CAC | 3.20 GEL | 0 GEL (inbound) |
| LTV | 64 GEL (8-month academic year, 0% churn modelled for first year) | 1,800 GEL (12-month contract) |
| LTV:CAC | 20:1 | Not applicable |
| Payback period | 0.4 months | Immediate |
| Gross margin | 91% | 91% |

**Revenue to date:** Pre-revenue. Institutional pilot begins September 2026 with KIU Library Services as first paying institutional customer.

---

## Slide 8: Go-to-Market

**Primary channel:** KIU student WhatsApp groups and course announcement channels administered by faculty.

- CAC in this channel: 3.20 GEL (cost of QR code card stock and printing, distributed to 3 group administrators)
- Conversion rate from link click to first completed booking: 18%
- Users acquired via this channel: 187 of 230 total WAU

**First 500 users plan:**
- Remaining users needed: 270
- At 3.20 GEL CAC and 18% conversion: 270 users require 1,500 link clicks, requiring distribution to approximately 8,333 people
- KIU has approximately 6,000 students reachable via WhatsApp groups
- Strategy: coordinate with 8 faculty members to distribute the link in their course groups at the start of October exam preparation period
- Timeline: 500 users within 4 weeks of coordinated push

**Secondary channel (not primary):** KIU library notice boards with printed QR codes. Under test. CAC not yet established. Not leading with this channel because it cannot be tracked as precisely.

---

## Slide 9: Competition

**Competitive matrix (from competitive-analysis.md):**

| Competitor | Real-time availability | Reservations | Noise level data | Cross-campus | Mobile UX | Personalisation | Institutional integration |
|------------|----------------------|-------------|-----------------|--------------|-----------|----------------|--------------------------|
| Google Maps | 1/5 | 1/5 | 0/5 | 1/5 | 5/5 | 2/5 | 1/5 |
| KIU Library booking | 3/5 | 5/5 | 0/5 | 1/5 | 2/5 | 0/5 | 3/5 |
| University mobile app | 2/5 | 3/5 | 0/5 | 2/5 | 3/5 | 1/5 | 5/5 |
| Walking around campus | 0/5 | 0/5 | 5/5 | 1/5 | 0/5 | 0/5 | 0/5 |
| Notion / calendar blocking | 0/5 | 3/5 | 0/5 | 0/5 | 4/5 | 2/5 | 0/5 |
| **StudySpace Finders** | **5/5** | **5/5** | **5/5** | **4/5** | **5/5** | **5/5** | **4/5** |

**Moat statement (from moat-statement.md):**

StudySpace Finders is building a Cornered Resource moat through exclusive data partnerships with KIU Library Services. Our real-time occupancy dataset, accumulated over 847 completed bookings and 8 weeks of continuous API access, cannot be replicated by a new entrant without negotiating separate institutional access agreements. Each building partnership we secure raises the cost of entry for the next competitor by exactly the effort it took us to secure that partnership. This maps to Hamilton Helmer's Cornered Resource power: exclusive access to an asset (institutional occupancy data) that others cannot easily replicate. Evidence: signed MOU with KIU Library Services (01-discovery/synthesis/competitive-landscape-seed.md) and the data pipeline committed to 03-build/architecture/.

---

## Slide 10: Ask

**The ask:** We are raising 75,000 GEL at a pre-money valuation of 300,000 GEL, representing 20% dilution.

**Valuation method:** VC method. Projected exit in year 5 at 2,400,000 GEL (16x current institutional contract value if scaled to 8 universities). Applied 75% discount for early-stage risk. Implied pre-money: 2,400,000 / 10 target multiple x 0.25 = 60,000 GEL. Rounded to 75,000 GEL to account for 12-month runway requirement.

**Use of funds:**

| Line item | Amount | Purpose |
|-----------|--------|---------|
| Engineering (part-time backend engineer, 12 months) | 36,000 GEL | Sensor integration, institutional analytics dashboard, and iOS app |
| Institutional sales (3 university partnership campaigns) | 24,000 GEL | Partnership negotiation, onboarding, and 90-day free trial costs for 3 new institutions |
| Infrastructure and legal (cloud hosting, GDPR audit) | 15,000 GEL | 12 months Vercel Pro plus a legal review of data handling agreements |

**Milestone this capital funds:** By March 2027, 3 signed institutional licences generating 5,400 GEL per month in recurring revenue and 2,000 monthly active student users across 4 university campuses.

**Contact:**
Team: Team Sigma
Email: studyspace@kiu.edu.ge
Repository: github.com/ZA-KIU-Classroom/team-sigma-sp26
Live product: studyspace-finders.vercel.app

---

*Pitch Deck Worked Example | StudySpace Finders | Lab 12 | CS-PD-2026 | Spring 2026*
*This is an instructional example. Not a real student submission.*
