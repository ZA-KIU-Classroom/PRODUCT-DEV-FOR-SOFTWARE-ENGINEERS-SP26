# Lab 5 Quick Start
## 2-Minute Setup | Read Before the Lab Begins

---

## Step 1: Confirm Access (Do Before Lab Starts)

Open both of these on your laptop right now:

- **Google Stitch:** https://stitch.withgoogle.com
- **Google AI Studio:** https://aistudio.google.com

Sign in with your Google account. If either does not load, tell the instructor immediately. Do not wait until Part 2 begins.

---

## Step 2: Open Your Synthesis Documents (2 minutes)

Have these open and visible before Part 1 starts:

- `01-discovery/synthesis/patterns-analysis.md`
- `01-discovery/synthesis/final-problem-statement.md` (or equivalent)
- `00-foundation/team-icp.md`

Your North Star Metric and your Stitch brief both come directly from these documents. If you have not read your own synthesis before arriving, you will waste 20 minutes of lab time.

---

## Step 3: Split Your Team (1 minute)

Decide now who does what during Parts 2 and 3:

**2 people on Stitch** (prototype builders)
**2 people on Event Schema** (measurement designers)

If you have 3 people: 1 leads Stitch, 2 lead schema, then swap for review at 1:05.

Write the names down. Do not leave this to chance.

| Role | Team Members |
|------|-------------|
| Stitch prototype | |
| Event schema | |

---

## Step 4: Create the Folder Structure (2 minutes)

Run these commands in your team repo before Part 1 ends:

```bash
mkdir -p 02-design/prototypes/high-fidelity
mkdir -p 03-build/analytics
```

---

## The Lab in 5 Bullet Points

- **0:00 to 0:20** -- North Star Metric. One number. Team consensus. Document and commit.
- **0:20 to 1:20** -- Stitch builds the prototype. Schema team designs 6 to 10 events. Both run in parallel.
- **1:20 to 1:45** -- Cross-team critique. Demo your prototype. Read your activation event aloud.
- **1:45 to 2:00** -- Commit three files to GitHub. Tag the commit `lab-5-draft`.
- **April 23 at 23:59** -- Final combined deadline for all Lab 5 and Lab 6 deliverables.

---

## Files You Will Commit Today

```
03-build/analytics/north-star-metric.md
03-build/analytics/event-schema.md
02-design/prototypes/high-fidelity/stitch-prototype-link.md
```

---

## If Something Goes Wrong

| Problem | Solution |
|---------|----------|
| Stitch will not load | Use backup prompting guide. Document what you would have built. |
| Team cannot agree on NSM | Apply the test: does this number change when we ship a bad release? If no, it is the wrong metric. |
| Event schema has more than 10 events | Cut everything marked "nice to have." Start with must-haves only. |
| Cannot agree on event name | Use object_action snake_case past tense. First team member to write it wins. |

---

*Lab 5 | CS-PD-2026 | Spring 2026 | Kutaisi International University*
