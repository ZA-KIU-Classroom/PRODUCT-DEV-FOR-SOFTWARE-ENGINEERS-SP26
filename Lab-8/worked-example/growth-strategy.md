# Growth Strategy -- StudySpace Finders

**Team:** StudySpace Finders
**Product:** A web app that helps KIU computer science students find available, quiet study spaces on campus in real time.
**Document version:** 1.0
**Last updated:** 7 May 2026

---

## 1. Target User (Reference)

Pulled from CP1 problem statement. Second and third year KIU computer science students who lose 15+ minutes per study session walking between library rooms and lab spaces looking for somewhere quiet to work. They currently rely on guessing or texting friends.

---

## 2. Activation Metric

**Aha moment:** A student opens the app and books a study space within 60 seconds of signup.

**Activation metric:** 70% of new signups complete a booking within 60 seconds.

**Why this is the aha moment:** From our 12 user interviews in CP1, the moment of relief was always the same: knowing where to go without thinking. If a student does not book within their first 60 seconds, they have likely opened the app, found it confusing or empty, and gone back to texting friends. We chose 60 seconds because that is faster than walking to the next library room.

---

## 3. Three Acquisition Channels

### Channel 1 -- KIU CS Discord and Reddit (r/KIU)

**Type:** Organic

**Why this channel:**
- **Fit:** Our entire target user base is on these two platforms. r/KIU has 1,247 members; the unofficial KIU CS Discord has 380 active members. From our interviews, 9 of 12 said they check Reddit or Discord daily.
- **Speed:** We can post today. Posts go live immediately. We can iterate every 48 hours based on response.
- **Cost:** Founder time only. Estimated 4 hours per week per channel for two weeks.

**What we will do in Sprint 2:**
1. Two posts per week in r/KIU during exam preparation peak times (Tuesday and Sunday evenings).
2. Pinned message in the KIU CS Discord study-help channel.
3. Reply to existing "where do you study?" threads with a non-spammy mention plus link.
4. Track signups by source via UTM parameters on every link.

**What success looks like in 4 weeks:** 80 to 120 signups, conversion rate from visit to signup of 8 to 12%, retention to D7 of 35%.

---

### Channel 2 -- Direct Outreach via University Faculty Mailing List

**Type:** Sales (founder-led)

**Why this channel:**
- **Fit:** The CS department head has agreed to forward one email per semester from student projects to all 312 enrolled CS students. This is the highest-trust, lowest-effort introduction we have access to.
- **Speed:** Email send pending department head approval. Realistic send date is Friday 15 May, two weeks from now.
- **Cost:** Founder time to draft. Approximately 6 hours total for drafting, approval cycles, and follow-up. No ad spend.

**What we will do in Sprint 2:**
1. Draft email by Tuesday 12 May. Subject: "30-second tool to find a quiet study space, built by your classmates."
2. Submit for department head approval.
3. Send Friday 15 May.
4. Track signups via a unique UTM source.

**What success looks like in 4 weeks:** 50 to 90 signups from a single send. 60% activation (higher than Channel 1 because of trust).

---

### Channel 3 -- Physical Posters in High-Traffic CS Building Locations

**Type:** Paid (low budget) plus organic

**Why this channel:**
- **Fit:** Students walking between buildings looking for somewhere to study are the literal target. A poster at the building entrance with a QR code catches them in the exact moment of need.
- **Speed:** Print today, post tomorrow.
- **Cost:** $25 for 20 A4 colour posters at the campus print shop. Plus 1 hour of founder time to put them up.

**What we will do in Sprint 2:**
1. Design poster: simple, large QR code, one sentence: "Find a quiet study space in 30 seconds."
2. Print 20 copies.
3. Post in: CS building entrance, library, three lab rooms, two student cafes near the building.
4. Refresh weekly. Track scans via UTM in the QR code.

**What success looks like in 4 weeks:** 30 to 50 scans per week. 60% scan-to-signup. 80% activation (these users have the highest intent because they are scanning at the exact moment of need).

---

## 4. Channel Ranking and Rationale

| Rank | Channel | One-sentence rationale |
|------|---------|------------------------|
| 1 | KIU CS Discord and Reddit | Largest reach, fastest to start, lowest cost, our user is already there |
| 2 | Faculty mailing list | Highest trust per signup but limited to one send per semester, so it is a one-shot |
| 3 | Physical posters | Lowest reach but highest activation rate; valuable for high-intent users in the moment |

---

## 5. Channels We Considered and Rejected

**Paid Meta or TikTok ads** -- Rejected. Our target audience is 312 students at one university. Targeting them via Meta requires ages, locations, and interests which would still surface the wrong people. The fit is poor and the budget would be wasted.

**Influencer / KOL partnerships** -- Rejected. We are not aware of any KIU CS-relevant influencers, and even if there were one, the audience would not be locked to KIU students. The local network effect of the product makes off-campus reach worthless.

**Word of mouth / referral programme** -- Not rejected, but deferred. We do not have enough activated users yet for a referral programme to make sense. We will revisit this in Sprint 3 once we have 100+ activated users.

---

## 6. Open Questions

What we do not yet know that we need to answer in Sprint 2:

1. What is the actual visit-to-signup conversion rate from r/KIU traffic? Our 8 to 12% range is from email signup industry benchmarks; Reddit traffic may convert differently.
2. How quickly does the faculty mailing list convert? We have no precedent for this kind of send and need real data.
3. Do poster QR codes drive signups or just scans that bounce? The friction of scanning, opening a browser, and signing up may be too much for the casual passer-by.

---

**Filed by:** Nino, David, Mariam, Luka
