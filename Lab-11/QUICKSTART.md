# Lab 11 QUICKSTART

**If you missed the session or need a fast reference, this document is self-contained.**

---

## What you are building

Four documents in `06-strategy/` of your team repository:

| File | What it is | Time |
|------|------------|------|
| `competitive-analysis.md` | Matrix: 5+ competitors x 7+ dimensions, scored 0-5 | 35 min |
| `strategy-canvas.md` | Blue Ocean canvas with ERRC table | 25 min |
| `ecosystem-map.md` | Complements, partners, threats, complementors | 25 min |
| `moat-statement.md` | One named power, three pieces of evidence | 15 min |

**Deadline:** Saturday 31 May 2026 at 23:59
**Tag:** `lab-11-submission`

---

## Step 1: Open your seed document (do this first)

Find `01-discovery/synthesis/competitive-landscape-seed.md` in your repo. This is the preliminary list of competitors and alternatives you compiled in Lab 4. It is your starting point.

If it is missing, spend 20 minutes reconstructing it from your interview logs. Look for every time a user mentioned an existing solution, a workaround, or an alternative they had tried.

---

## Step 2: Competitive matrix (use the template)

Copy `Lab-11/templates/competitive-analysis-template.md` to `06-strategy/competitive-analysis.md`.

Required competitors: 5 or more. Must include:
- At least 2 direct competitors (same product category)
- At least 1 indirect competitor (different product, same user job)
- At least 1 substitute (the zero-tech alternative, e.g. "walking around", "asking a friend", "doing nothing")

Required dimensions: 7 or more. Must include core feature coverage, pricing model, target segment, and switching cost. Add dimensions specific to your market.

Score every competitor on every dimension from 0 to 5. Score your own product too. Score it honestly.

Write a 200-word synthesis paragraph at the bottom identifying your two strongest gap dimensions and your biggest Porter force threat.

---

## Step 3: Strategy Canvas (use the template)

Copy `Lab-11/templates/strategy-canvas-template.md` to `06-strategy/strategy-canvas.md`.

List the 8-10 factors your market competes on. For each factor:
- Calculate the industry average score from your matrix (add up all competitor scores for that dimension and divide by the number of competitors)
- Note your own score

Fill in the ERRC table:

| Factor | Action | Rationale |
|--------|--------|-----------|
| [Factor] | Eliminate / Reduce / Raise / Create | [One sentence] |

Every factor must be assigned to exactly one category. Write a 150-word narrative below the table.

---

## Step 4: Ecosystem map (use the template)

Copy `Lab-11/templates/ecosystem-map-template.md` to `06-strategy/ecosystem-map.md`.

Fill in all four sections:

**Complements:** Name specific products. Explain the relationship in one sentence each.

**Partners:** Name specific organisations. Mark each as: Confirmed / In discussion / Identified. Note what they give you (data, distribution, credibility, access).

**Threats:** Name each threat. Rate likelihood: Low / Medium / High. State your counter-strategy in one sentence.

**Complementors:** Name parties whose product increases demand for yours. These often include EdTech tools, productivity apps, or institutional services in adjacent spaces.

Write the 150-word Strategic Priorities section at the bottom.

---

## Step 5: Moat statement (use the template)

Copy `Lab-11/templates/moat-statement-template.md` to `06-strategy/moat-statement.md`.

Pick one of Helmer's Seven Powers:

1. Scale Economies
2. Network Effects
3. Counter-Positioning
4. Switching Costs
5. Branding
6. Cornered Resource
7. Process Power

The three most accessible at your stage: Network Effects, Switching Costs, Cornered Resource.

Write:
- The power named (one line)
- The mechanism in your product (2-3 sentences)
- Three pieces of evidence from your repo (links, screenshots, metric quotes)
- Your 60-day path to strengthening it (2-3 sentences)

If you do not have three pieces of evidence, label it "Moat Hypothesis" and state what evidence you will collect and how.

---

## Step 6: Commit and tag

```bash
git add 06-strategy/
git commit -m "[LAB-11] Strategic analysis: competitive matrix, canvas, ecosystem map, moat statement"
git tag lab-11-submission
git push origin main --tags
```

Verify all four files are visible in your GitHub repository before Saturday 31 May at 23:59.

---

## Common mistakes that cost marks

- Scoring your own product 5/5 on every dimension
- Listing competitors without naming them specifically (no "other apps" or "various tools")
- Claiming a moat without repo evidence
- Writing a moat statement for branding, scale economies, or process power without evidence
- Ecosystem map with generic categories and no named organisations
- Missing the synthesis paragraph in the competitive analysis
- Forgetting to tag the commit

---

## Questions

Email zeshan.ahmad@kiu.edu.ge with subject `[LAB-11] your question here`
