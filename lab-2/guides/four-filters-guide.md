# Guide: The Four Filters Framework

## What This Is

The Four Filters is a structured evaluation method for deciding which problem is worth committing to. You run every candidate problem through four tests. Problems that fail multiple filters should be dropped. Problems that pass all four filters are worth pursuing.

This is not a vague gut-feel exercise. Each filter has specific evidence signals that indicate a pass or a fail.

---

## Why This Matters

Most student teams fail at product development because they fall in love with a problem before checking whether it is real, painful, solvable, and accessible. The Four Filters forces you to separate your emotional attachment from the evidence.

A problem that scores highly on all four filters is not necessarily the most interesting problem. It is the problem you can actually make progress on in 13 weeks.

---

## The Four Filters in Detail

### Filter 1: Real and Recurring

**The question:** Does this problem actually happen to real people, and often enough that a solution is worth building?

**What you are looking for:** A problem that occurs at a frequency where the user would notice its absence. If someone experiences this problem once a year, they will not change their behaviour to adopt your solution. If they experience it weekly or daily, they will.

**Scoring:**
- **3 — Strong pass:** The problem is frequent (at least weekly for the target user) and you can name specific people who experience it
- **2 — Weak pass:** The problem exists but you are unsure of frequency, or it is monthly/occasional
- **1 — Fail:** The problem is rare, hypothetical, or you cannot name anyone who actually has it

**Common failure mode:** Teams confuse "this would be annoying if it happened" with "this happens regularly." Do not score based on imagination. Score based on what you know.

**Evidence signals that indicate a 3:**
- You have personally experienced this problem
- Multiple team members have independently experienced it
- People bring it up unprompted when you describe the space
- You can identify a community (subreddit, WhatsApp group, forum) where people complain about it

---

### Filter 2: Painful Enough to Act

**The question:** Is the pain acute enough that people are already doing something about it, even if that something is a bad solution?

**What you are looking for:** Evidence of active workarounds. If people are not currently trying to solve this problem in some way, it is probably not painful enough to adopt a new product. The existence of a workaround is the strongest possible signal that the problem is real.

**Scoring:**
- **3 — Strong pass:** People have a clear current workaround you can describe precisely (spreadsheet, WhatsApp group, manual process, paying someone)
- **2 — Weak pass:** People complain about the problem but have no workaround; they just tolerate it
- **1 — Fail:** People do not seem to care much; they accept the situation without friction

**Common failure mode:** Teams assume that "there is no solution currently" means the problem is a great opportunity. Sometimes it means nobody cares enough to even try. A missing solution is not evidence of pain. A bad existing solution is.

**Evidence signals that indicate a 3:**
- You can describe the workaround precisely: "They use a shared Google Sheet with 15 tabs and update it manually every Monday"
- People express frustration about the workaround, not the problem
- People have tried multiple workarounds and abandoned them
- Someone is paying money (even a small amount) to partially address this

---

### Filter 3: Underserved Today

**The question:** Are the existing solutions genuinely inadequate, or are people actually fine with what exists?

**What you are looking for:** A real gap between what users need and what existing tools provide. If Google Docs, WhatsApp, or a simple spreadsheet actually solves the problem adequately, you do not have an opportunity.

**Scoring:**
- **3 — Strong pass:** Existing solutions are clearly inadequate — too expensive, too complex, too slow, missing a critical feature, or unavailable in this context
- **2 — Weak pass:** Existing solutions are imperfect but users have adapted; the gap is real but small
- **1 — Fail:** Existing solutions work fine; users are satisfied with what exists

**Common failure mode:** Teams build features that already exist in tools users simply have not discovered yet. Before scoring a 3, spend 30 minutes genuinely trying to solve the problem with existing free tools. If you can solve it in 30 minutes with Google Forms, your problem fails this filter.

**Questions to stress-test your score:**
- Have you actually tried the existing solutions?
- What specifically is missing or broken?
- Would a user switch from their current solution to yours? What would make them switch?

---

### Filter 4: Accessible to You

**The question:** Can you reach and interview people who have this problem this week? Can your team actually build something for this problem given your skills and the 13-week timeline?

**What you are looking for:** Practical access to potential users for discovery interviews, and a realistic assessment of whether your team can build an MVP in this space.

**Scoring:**
- **3 — Strong pass:** You can name 5+ people you could interview this week. At least one team member has domain knowledge. The technical scope is within reach.
- **2 — Weak pass:** You can reach users but it will take significant time. Or the technical scope is ambitious but feasible.
- **1 — Fail:** You cannot name a single person to interview. Or the problem requires expertise your team does not have. Or it requires data, infrastructure, or partnerships that will take months to acquire.

**Common failure mode:** Teams choose problems in industries they find exciting (fintech, healthcare, AI) but have no contacts, no domain knowledge, and no ability to prototype in the space within the semester. Access is not optional.

**Be honest about this filter.** A problem that scores 3+3+3+1 is worse than a problem that scores 2+3+2+3. You cannot make progress if you cannot talk to users.

---

## Scoring and Decision Rules

| Total Score | Recommendation |
|-------------|---------------|
| 10-12 | Strong candidate. Pursue this problem. |
| 7-9 | Possible candidate. Discuss what would need to be true for it to become a 10+. |
| 4-6 | Weak candidate. Only pursue if your entire shortlist is in this range. |
| Below 4 | Drop this problem. |

### Tie-breaking

If two problems score equally, use this tie-breaker in order:

1. Which problem do team members have more personal proximity to?
2. Which problem has the more accessible user pool for interviews?
3. Which problem gives your team a more realistic chance of building something demonstrable by Week 15?

### Do Not Average

Do not average your scores and commit to a problem that scored 1 on Filter 4 because its total was high. A 1 on any single filter is a red flag that needs a deliberate answer before you commit.

---

## What to Do After Scoring

1. Fill in `templates/four-filters-evaluation-template.md` with your scores and written justifications
2. Identify your top 2-3 candidates
3. Use your top candidate as the basis for your problem commitment decision in the next activity
4. Keep your second candidate documented — it becomes your secondary ICP

---

## A Note on Honesty

The Four Filters only work if you score honestly. It is tempting to inflate scores for the problem you are already excited about. Resist this. The filter is a forcing function, not a rubber stamp.

If your favourite problem scores poorly, that is important information. Either abandon it or go and gather evidence that would change the score. Do not manufacture a score you cannot justify with real observations.
