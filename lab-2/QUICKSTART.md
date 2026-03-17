# QUICKSTART — Lab 2

You have 120 minutes. Here is what to do, in order.

---

## Before You Start (5 minutes)

1. Open your team GitHub repository
2. Confirm `00-foundation/all-problem-statements.md` is there with every member's three problems
3. Count your total problem candidates: you should have between 9 and 16 depending on team size
4. Open the `templates/` folder in this repo — you will need it throughout lab

If your team was assigned by the professor (you missed the 18 March deadline), spend your first 10 minutes on quick introductions and agreeing on a team name before starting Step 1.

---

## Step 1: List Your Candidates (0:00 - 0:15)

Pull all individual problem statements into a shared view. Use one of:
- A shared Google Doc
- A Miro board
- Sticky notes on a whiteboard

Do not discuss which problems are good yet. Just get them visible. List every single one.

---

## Step 2: Run the Four Filters (0:15 - 0:50)

For each problem candidate, score it on the Four Filters using `templates/four-filters-evaluation-template.md`.

The Four Filters are:

| Filter | The question you are asking |
|--------|----------------------------|
| **Real and Recurring** | Does this happen to real people often enough to matter? |
| **Painful Enough to Act** | Are people already trying to solve it, even badly? |
| **Underserved Today** | Are current solutions genuinely inadequate? |
| **Accessible to You** | Can you reach people with this problem and build something for them? |

Score each filter 1-3. Total score out of 12. Problems scoring below 7 are usually not worth pursuing. Problems scoring 10+ are your shortlist.

Use `guides/four-filters-guide.md` for detailed scoring criteria.

---

## Step 3: Commit to One Problem (0:50 - 1:05)

Your top-scoring problem from the Four Filters is your starting point. Discuss as a team:

- Does this feel real to us?
- Can we reach people who have this problem this week?
- Does at least one team member have personal proximity to this problem?

Then commit. Fill in `templates/team-problem-statement-template.md`. Every member must agree before you move on.

> **This is not reversible today.** You are committing for the next several weeks. If you feel genuine uncertainty, raise it with the instructor before moving past this step.

---

## Step 4: Build Your Ideal Customer Profile (1:05 - 1:25)

Using `templates/icp-template.md`, build your primary ICP. This is a precise description of the person most likely to experience your problem most acutely.

Be specific. "University students" is not an ICP. "Second-year Computer Science students at KIU who commute from outside Kutaisi and have no consistent study space between classes" is an ICP.

---

## Step 5: Write Your Interview Questions (1:25 - 1:50)

Using `templates/interview-script-v1-template.md`, write your first 10 interview questions.

Every question must pass the Mom Test:
- Ask about past behaviour, not future intentions
- Ask about the problem, not your solution
- No leading questions
- No hypotheticals ("would you use...?")

Use `guides/interview-script-guide.md` for question-writing rules and common mistakes.

---

## Step 6: Plan Your Outreach (1:50 - 2:00)

Open `templates/interview-tracker-template.md` and identify at least 5 real people you could interview this week. These should be people who match your ICP. Write down:

- Who they are
- Why they fit your ICP
- How you will contact them
- Target date for the interview

---

## Commit Before You Leave

```bash
git add .
git commit -m "[LAB-2] In-lab: Four Filters, problem statement, ICP draft"
git push origin main
```

Full homework is due **Wednesday 25 March at 23:59**. Tag your final submission:

```bash
git tag lab-2-submission
git push origin main --tags
```

---

## If You Finish Early

Start your second ICP (the secondary candidate from your Four Filters shortlist). You need two ICPs in your homework submission.
