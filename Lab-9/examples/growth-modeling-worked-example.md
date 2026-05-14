# Lab 9 Worked Example: StudySpace Finders

**This is an example only. Do not copy these numbers into your own documents.**
**Your documents must reflect your actual product, audience, and data.**

---

## Context

StudySpace Finders is a mobile-first web app that helps KIU students find and book available study spaces on and around campus. Students sign up with their university email, browse a real-time map of study spaces, and book a slot. Space hosts (campus facilities and local cafes) list their spaces and manage availability.

This is a two-sided marketplace at early stage. The team currently has a live Vercel deployment with 47 active users across two weeks of Sprint 1.

---

## Example: Growth Strategy Document

### Activation Metric

A user is activated when they find and complete a study space booking within 60 seconds of first opening the app after signup.

Activation number: one completed booking.
Time window: within 60 seconds of first app open post-signup.

Why this action indicates real value: In our interviews, 9 of 12 students said the primary reason they would stop using a study space app is if it took too long to find something useful. A student who books within 60 seconds has experienced the core value proposition end to end. Our event schema fires `booking_completed` with a `time_since_first_open_seconds` property. Our current data shows 31% of signups reach this activation event. Industry benchmark for marketplace activation is 25-40%, so we are within range.

---

### Acquisition Channels

**Primary channel:** Organic -- KIU student community channels (WhatsApp groups, Telegram study groups, KIU Discord server)

Type: Organic

Why: Our 12 discovery interviews showed that 10 of 12 KIU students find study-related tools through peer recommendation in existing student group chats, not through search or paid ads. Our ICP is highly concentrated in two or three group chats with 200 to 400 members each. A single well-timed post in the right channel has an estimated reach of 300 students at zero cost. Our early traction came entirely from this channel: all 47 current users arrived via two posts in the KIU Computer Science WhatsApp group.

How we will use it in Sprint 2: post two pieces of content per week in five targeted student group chats, rotating the message framing (exam period stress, group study coordination, quiet study availability). Track which channels convert via UTM parameters in the shared link.

Scale ceiling: Once we exhaust the active student group chats at KIU (estimated 15 to 20 groups with a total reachable audience of approximately 2,000 students), organic community growth will plateau. This channel gets us to approximately 400 to 600 users before we need to supplement with a second channel.

---

**Secondary channel:** Sales -- outreach to campus facility managers and local cafe owners to onboard supply-side listings

Type: Sales

Why: A study space app with zero listed spaces is useless. Our supply-side acquisition is a sales problem: we need to convince facility managers to create accounts and list their spaces. This is high-touch, high-conversion, and necessary. Without supply, demand acquisition from our primary channel produces users who open the app, see no spaces, and churn immediately.

How we will use it in Sprint 2: two team members will conduct five in-person facility manager conversations per week, targeting KIU library, student union, three campus cafes, and two local cafes within 500 metres of campus. Goal is 10 new listed spaces by end of Sprint 2.

Scale ceiling: This channel is limited by team headcount. Two people can conduct five meetings per week sustainably. This gets us to 20 to 30 listed spaces before we need to make the supply-side onboarding self-serve.

---

**Tertiary channel:** Viral -- shareable booking confirmation

Type: Viral

Status: In design. The loop exists conceptually but the sharing mechanic is not yet built. When a user books a space, they receive a confirmation that includes a shareable calendar event. The calendar event has StudySpace Finders branding and a link. A classmate who receives the calendar invite sees the link, clicks through, and can book an adjacent slot. We estimate K at approximately 0.2 if built. We will not include this in our Sprint 2 primary projection but will add it as a separate row in the growth model with K = 0.2 labelled as an assumption.

---

## Example: Unit Economics Analysis

### Channel 1: Organic Community

**CAC calculation:**

Total spend: We estimate 2 hours per week of team time on community posting at a notional rate of 10 GEL per hour (Georgian minimum wage approximate). Over 4 weeks: 2 hours x 4 weeks x 10 GEL = 80 GEL = approximately 30 USD.

Users acquired via this channel in Month 1: 47 (all current users came from this channel).

CAC = 30 USD / 47 users = 0.64 USD per acquired user.

Conversion funnel:
- Post view to link click: estimated 8% (assumption, will track with UTM in Sprint 2)
- Link click to signup: 22% (from our landing page analytics: 213 unique visitors, 47 signups)
- Signup to activation: 31% (from our event schema: 47 signups, 14.6 activations average over 2 weeks)

**LTV calculation:**

Our product is currently free. Monetisable value substitute: we interviewed 8 student users and asked willingness to pay. Median response was 5 GEL per month (approximately 1.85 USD). We will use 1.50 USD per month as a conservative estimate.

ARPU: 1.50 USD per month
Gross margin: 85% (hosting on Vercel free tier for now, costs near zero; assuming 15% for future infrastructure)
Average customer lifetime: estimated 6 months, based on a typical semester length. Students who find a useful study space app during exam period are likely to use it for the remainder of the academic year.

LTV = 1.50 x 0.85 x 6 = 7.65 USD

LTV:CAC = 7.65 / 0.64 = 11.9:1

This is a healthy ratio. The primary reason is that CAC is very low on this channel. As we scale beyond the initial group chats and the organic channel becomes harder to work, CAC will rise. We model CAC rising to 3.50 USD by Month 4 as we deplete the easiest audiences, which gives LTV:CAC of approximately 2.2:1 by Month 4. Still above 1:1 but below the ideal 3:1 floor.

Payback period: CAC / (ARPU x gross margin) = 0.64 / (1.50 x 0.85) = 0.64 / 1.275 = 0.5 months. At current CAC this is excellent. At Month 4 CAC of 3.50 USD: 3.50 / 1.275 = 2.7 months. Still acceptable.

---

### Channel 2: Sales (Facility Manager Outreach)

This channel acquires supply, not demand. CAC for the supply side is calculated differently.

Total spend: 5 meetings per week x 2 team members = 10 meetings per week. Each meeting is 30 minutes plus 30 minutes prep and follow-up. 20 hours per week x 10 GEL per hour x 4 weeks = 800 GEL = approximately 296 USD per month.

Supply-side users (listed spaces) acquired: we estimate 10 new listed spaces per month at this effort level based on our pilot (3 spaces onboarded from 6 meetings in our first two weeks of outreach).

CAC for supply: 296 USD / 10 spaces = 29.60 USD per listed space.

LTV of a listed space: A listed space that drives 5 bookings per week x 4 weeks = 20 bookings per month. If we eventually charge a 5% booking fee on a 2 GEL booking, that is 0.10 GEL per booking x 20 bookings = 2 GEL per space per month = approximately 0.74 USD. Over a 12-month facility contract: LTV = 0.74 x 12 = 8.88 USD.

LTV:CAC for supply = 8.88 / 29.60 = 0.30:1. This is below 1:1.

We acknowledge this. The sales channel for supply acquisition is currently loss-making at our current monetisation plan. This is acceptable at early stage because we need supply to make the demand side work. The path to improving this ratio: (1) make supply onboarding self-serve by Month 3, reducing CAC to near zero for organic supply signups; (2) increase the booking fee to 10% once we have proven booking volume. At 10% fee: LTV = 1.48 USD x 12 = 17.76 USD, giving LTV:CAC of 0.60:1 on sales-acquired supply, which improves further as self-serve supply grows.

---

## Example: Growth Projection Structure (text description, build in spreadsheet)

Month 1 expected case:
- Organic channel: 300 visitors, 66 signups (22% conversion), 20 activated (31%), 10 retained D30 (50% from activated), CAC 0.64 USD, LTV 7.65 USD, cumulative users 10
- Sales channel (supply): 10 listed spaces added, enables demand acquisition to continue functioning
- Cumulative activated users end of Month 1: 20

Month 2 expected case:
- Organic channel: 450 visitors (growth from 5 group chats vs 2), 99 signups, 31 activated, 18 retained D30, CAC 1.20 USD (more effort needed per signup as easy audiences saturate), LTV 7.65 USD, cumulative users 28
- Viral row added: K = 0.2, generates approximately 6 additional signups from existing 20 Month 1 users each generating 0.5 share events with 40% conversion, cumulative users 33

Best case Month 2: activation rate improves from 31% to 45% due to onboarding improvement from usability testing. All other variables same. Cumulative users: 42.

Worst case Month 2: WhatsApp group admin removes our posts as spam in two of five groups. Visitors drop to 220. Signups 48, activated 15, retained 9, cumulative users 18.

---

## Example: Loop and Moat Narrative

### Viral Loop

We have a loop in design, not yet built.

Designed loop:
Step 1: User books a study space and receives a confirmation email.
Step 2: The confirmation contains a calendar event download that includes a note: "Booked via StudySpace Finders -- find your own space at [link]."
Step 3: The user shares the calendar event with their study group.
Step 4: A study group member sees the link, clicks through, and books an adjacent slot.

K-factor estimate:
- Average calendar shares per booking: 0.8 (assumption -- most bookings are solo; some are group coordination)
- Conversion rate from shared link to signup: 25% (assumption based on our landing page conversion rate)
- K = 0.8 x 0.25 = 0.20

K = 0.20 means the loop reduces our blended CAC by approximately 25%. This is meaningful even though K is well below 1. At a blended CAC of 1.50 USD, a 25% reduction saves 0.37 USD per acquired user. Across 500 users, that is 185 USD saved -- more than a month of community posting effort.

We plan to build the shareable calendar confirmation in Sprint 2 as a 3-point story. If it does not improve activation rate by 10% within two weeks of launch, we will deprioritise it.

---

### Network Effects

Our primary network effect is local. StudySpace Finders becomes more valuable to each individual student as more students use it and more spaces are listed, because:

- More students listing availability preferences (future feature) means smarter recommendations
- More bookings means more social proof that a space is good
- More spaces listed means more choice per session

Type: Local network effect (within KIU campus ecosystem)

Critical mass threshold: The app becomes genuinely useful when there are at least 25 actively listed study spaces within a 10-minute walk of the main KIU building AND at least 100 active student users in the same week. Below either threshold, users open the app and find either no spaces or spaces with no recent booking history to validate quality.

Current position: 11 listed spaces, 47 active users. We are 44% of the way to the space threshold and 47% of the way to the user threshold.

---

### Moat Narrative

Our moat at current scale is weak. We have 47 users and 11 listed spaces. A competitor could rebuild what we have built in two weeks and undercut us on any dimension.

What we are building toward: a local data network effect. Every booking generates data about which spaces are popular at which times, which spaces have noise complaints (flagging in a future feature), and which spaces are underused. After 1,000 bookings, we will have a dataset that a new entrant cannot replicate without 1,000 bookings of their own. That dataset will power better recommendations and better pricing signals for space hosts.

At 1,000 bookings (we project this at approximately Month 4 in our expected case), our moat becomes moderate. A well-funded competitor could still enter but would face a 3 to 4 month data gap before their recommendations are as useful as ours.

At 10,000 bookings (projected Month 9 or 10, beyond our current model), the dataset moat becomes strong for the KIU context. A copycat would need to either acquire us or spend significant time building an equivalent dataset.

Threats we cannot defend against: a university administration decision to build their own booking system and mandate it for all students. This is a regulatory risk, not a competitive one. We are mitigating it by building a relationship with the KIU facilities team, who we have pitched as a potential design partner.
