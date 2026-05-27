# Lab 11: Strategic Analysis

**Course:** CS-PD-2026 Product Development for Software Engineers
**Week:** 13
**Group A:** Thursday 28 May 2026, 14:00 to 16:00
**Group B:** Friday 29 May 2026, 16:00 to 18:00
**Location:** Standard lab room, in person
**Submission deadline:** Saturday 31 May 2026 at 23:59
**Commit tag:** `lab-11-submission`

---

## Overview

You have been building a product for thirteen weeks. Today you answer the question that every investor, every judge, and every serious customer will ask you: why can't someone just copy this?

This lab takes the competitive strategy frameworks from the Week 13 lecture and turns them into four concrete documents that will live in your repository and feed directly into your Demo Day pitch and Checkpoint 4 submission.

You are not starting from scratch. Every team produced a competitive landscape seed document in Lab 4 (`01-discovery/synthesis/competitive-landscape-seed.md`). That document is your foundation. The first thing you do when you sit down is open it.

---

## Learning Outcomes

By the end of this lab you will be able to:

- Map the competitive forces operating on your product using Porter's Five Forces
- Construct a rigorous competitive matrix with five or more named competitors evaluated across seven or more dimensions
- Draw a Blue Ocean Strategy Canvas identifying which dimensions you are eliminating, reducing, raising, and creating
- Produce an ecosystem map naming actual organisations across four categories: complements, partners, threats, and complementors
- Write a moat statement that names a specific Helmer power, provides evidence from your repository, and articulates a path to strengthening it
- Articulate at least two counter-strategies for your most significant competitive threats

---

## Pre-Lab Requirements

Before you arrive, every team member must:

1. **Open your repository** and locate `01-discovery/synthesis/competitive-landscape-seed.md`
2. **Review the Week 13 lecture slides** for the definitions of Porter's Five Forces, Helmer's Seven Powers, and the Blue Ocean ERRC framework
3. **Identify at least three competitors or alternatives** that your users mentioned during interviews. These go into the competitive matrix
4. **Think individually** about which of Helmer's Seven Powers you believe your product could honestly claim, and what evidence from your repository would support that claim

If your competitive landscape seed document is missing or incomplete, use the first 30 minutes of the lab to reconstruct it from your interview logs before beginning Activity 1.

---

## Activities

### Activity 1: Competitive Matrix (35 minutes)

**Output file:** `06-strategy/competitive-analysis.md`
**Template:** `Lab-11/templates/competitive-analysis-template.md`
**Worked example:** `Lab-11/examples/competitive-analysis-example.md`

Evaluate five or more competitors or alternatives across seven or more dimensions. Your competitors must include both direct competitors (products doing the same thing) and indirect competitors and substitutes (products satisfying the same user job in a different way).

**Dimensions to evaluate must include at minimum:**

- Core feature coverage (does it solve the primary job?)
- Pricing model
- Target user segment
- Geographic or institutional reach
- Quality of mobile experience
- Data or personalisation depth
- Switching cost or lock-in

You may add dimensions specific to your market. The worked example shows how StudySpace Finders does this for the campus space-finding market.

**Scoring:** Use a 0 to 5 scale for each dimension. Score each competitor honestly, including your own product. A matrix where your product scores five on every dimension is not an honest analysis and will not earn marks.

**The gap is the point.** After scoring, identify the two or three dimensions where your product scores highest and every incumbent scores lowest. Those gaps define your Blue Ocean position and anchor your pitch.

After completing the matrix, write a 200-word synthesis paragraph below it that explains:
- Which force from Porter's Five Forces represents your greatest external threat and why
- Which two dimensions create the most defensible gap for your product
- What would have to change in the market for that gap to close

---

### Activity 2: Strategy Canvas (25 minutes)

**Output file:** `06-strategy/strategy-canvas.md`
**Template:** `Lab-11/templates/strategy-canvas-template.md`
**Worked example:** `Lab-11/examples/strategy-canvas-example.md`

The Strategy Canvas is a single visual representation of how your product and your key competitors invest in each competitive dimension. It makes your Blue Ocean move explicit and communicable.

**Step 1:** List the eight to ten factors your industry currently competes on across the horizontal axis. Draw from your competitive matrix dimensions, but focus on the ones that matter most in your market.

**Step 2:** For each factor, draw a curve showing the current industry standard. Average your competitors' scores from Activity 1 to get this.

**Step 3:** Draw your own curve. Where does it diverge from the industry standard?

**Step 4:** Apply the ERRC framework explicitly. For each factor, assign it to one of four categories:

- **Eliminate:** Reduce this factor below industry standard because your users do not value it
- **Reduce:** Offer this below the standard competitor level to reduce cost or complexity
- **Raise:** Elevate this significantly above what the industry currently offers
- **Create:** Introduce something entirely new that no competitor currently provides

Write the ERRC table in your markdown file. Below it, write a 150-word narrative that explains your Blue Ocean move in plain language: what you stopped competing on, what you introduced, and why that combination is appropriate for your specific user segment.

---

### Activity 3: Ecosystem Map (25 minutes)

**Output file:** `06-strategy/ecosystem-map.md`
**Template:** `Lab-11/templates/ecosystem-map-template.md`
**Worked example:** `Lab-11/examples/ecosystem-map-example.md`

Map every relevant party in your product's surrounding environment across four categories.

**Complements:** Products or services that make your product more valuable when used together. Name specific applications, tools, or services. Explain the relationship.

**Partners:** Organisations that give you access, distribution, data, or credibility. Name the actual organisations. Note whether each partnership is confirmed, in discussion, or identified but not yet approached.

**Threats:** Parties who could decide to enter your market and compete with you. Include not just obvious competitors but also platform threats (a larger platform adding your functionality), institutional threats (a university building their own system), and technology shifts (a capability that could make your product redundant). For each threat, rate the likelihood as low, medium, or high, and note your counter-strategy.

**Complementors:** Parties whose product or service increases demand for yours, even without a formal relationship. These are often overlooked but strategically valuable. If a student productivity tool drives students to spend more time studying, they create demand for better study spaces. That makes them your complementor even if they have never heard of you.

After mapping all four categories, write a 150-word section called **Strategic Priorities** that answers:
- Which partner relationship would most accelerate your growth if formalised in the next 90 days?
- Which threat is most likely to materialise and what is your specific counter-strategy?
- Which complementor could you approach for a lightweight co-promotion arrangement?

---

### Activity 4: Moat Statement (15 minutes)

**Output file:** `06-strategy/moat-statement.md`
**Template:** `Lab-11/templates/moat-statement-template.md`
**Worked example:** `Lab-11/examples/moat-statement-example.md`

A moat is a structural advantage that compounds over time and requires increasing effort for a competitor to overcome. This document makes that advantage explicit and evidenced.

**The moat statement has four required components:**

**1. The power named.** State which of Helmer's Seven Powers your moat maps to. You may claim only one primary power. If you have a secondary power emerging, you may note it, but the primary claim must be specific and evidenced.

**2. The mechanism explained.** In two to three sentences, explain how this power operates for your product. Not what it is in general. How it works specifically for your users, your data, your market.

**3. The evidence provided.** Minimum three pieces of evidence from your repository that demonstrate this power is real today, not aspirational. Acceptable evidence includes: analytics dashboard screenshots showing retention curves, signed MOUs or partnership agreements committed to your repo, word-of-mouth growth metrics, data showing increasing engagement per user over time, screenshots of a proprietary data source others cannot access, or user quotes from your interview logs that demonstrate lock-in or switching cost.

**4. The path forward.** Two to three sentences explaining what specific actions over the next 60 days would strengthen this moat. Be concrete: not "we will grow our user base" but "we will approach three additional universities for data sharing agreements before Demo Day, which would triple the geographic reach of our occupancy dataset."

**If you cannot provide three pieces of repository evidence,** write the moat statement as a hypothesis. Label it clearly as "Moat Hypothesis" rather than "Moat Statement." Name the evidence you would need to collect to confirm it, and state your plan for collecting it before Checkpoint 4. A well-written hypothesis earns partial marks. An overclaimed moat earns none.

---

## Deliverables Summary

| File | Activity | Required by |
|------|----------|-------------|
| `06-strategy/competitive-analysis.md` | Activity 1 | Sat 31 May 23:59 |
| `06-strategy/strategy-canvas.md` | Activity 2 | Sat 31 May 23:59 |
| `06-strategy/ecosystem-map.md` | Activity 3 | Sat 31 May 23:59 |
| `06-strategy/moat-statement.md` | Activity 4 | Sat 31 May 23:59 |

All four files must be committed and pushed to your team repository. Tag the commit `lab-11-submission`.

---

## Repository Structure

Your `06-strategy/` folder should look like this after Lab 11:

```
06-strategy/
├── competitive-analysis.md       (Activity 1)
├── strategy-canvas.md            (Activity 2)
├── ecosystem-map.md              (Activity 3)
├── moat-statement.md             (Activity 4)
├── product-roadmap.md            (from Lab 6)
└── prioritization-framework.md   (from Lab 6)
```

---

## Submission Instructions

1. Complete all four activity files and commit them to `06-strategy/`
2. Run `git tag lab-11-submission` on your final commit
3. Push both the commits and the tag: `git push origin main --tags`
4. Verify all four files are visible in your GitHub repository before the deadline

If you encounter a merge conflict during the lab, resolve it before pushing. Do not submit with unresolved conflicts.

---

## Connection to Checkpoint 4 and Demo Day

Every document you produce today feeds directly into your Demo Day pitch and your Checkpoint 4 repository review.

Your **moat statement** answers the question judges ask most: why can't someone just copy this?

Your **ecosystem map** and **competitive matrix** answer the question investors ask second: why are you the team to build this in this market right now?

In your Demo Day pitch you have approximately 90 seconds to address competitive positioning. Judges have seen hundreds of pitches. The ones that stand out name specific competitors, acknowledge what those competitors do well, and explain with precision why their position is defensible. Your Lab 11 documents are the research behind those 90 seconds.

---

## Questions

Raise your hand during the lab session. For questions after the session, email zeshan.ahmad@kiu.edu.ge with the subject line `[LAB-11] your question here`.
