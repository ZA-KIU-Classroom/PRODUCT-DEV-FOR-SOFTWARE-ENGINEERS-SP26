# Lab 9 QUICKSTART

**Read this before the session starts. It takes two minutes.**

---

## What is happening today

You are building four documents that form the go-to-market foundation of your checkpoint submission. Every number needs a source. Every assumption needs a label.

---

## Step 1: Folder setup (do this before lab starts)

In your team repo:

```bash
mkdir -p 04-gtm/financials
mkdir -p 04-gtm/traction
touch 04-gtm/growth-strategy.md
touch 04-gtm/financials/unit-economics.md
touch 04-gtm/loops-and-moats.md
```

The growth projection is a spreadsheet. Open Google Sheets now and create a new file called `growth-projection`.

---

## Step 2: Have these open in browser tabs before 14:00 / 13:00

- [ ] Your live deployment URL
- [ ] Your analytics dashboard (Mixpanel, Amplitude, GA4, or equivalent)
- [ ] Your event schema document from Lab 6
- [ ] Your experiment results from Sprint 1 (partial is fine)
- [ ] Google Sheets with your growth projection file open
- [ ] The Lab 9 README for reference

---

## Step 3: Know the answer to these questions before the session

Your team should be able to answer all of these without a document:

1. What is your activation metric? State it as a specific action, a specific number, and a specific time window.
2. What are your two or three main acquisition channels? What type is each: paid, organic, viral, or sales?
3. What does a user pay, or what is the monetisable value per user if free?
4. Does your product create a situation where one user's presence causes another user to sign up?

If your team cannot answer question 1 before the session, spend five minutes before 14:00 agreeing on it. Everything else in the lab depends on it.

---

## Step 4: The four deliverables and their time slots

| Time | What you are building | File |
|------|-----------------------|------|
| 0:10 to 0:40 | Growth Strategy Document | `04-gtm/growth-strategy.md` |
| 0:40 to 1:00 | Unit Economics Analysis | `04-gtm/financials/unit-economics.md` |
| 1:00 to 1:30 | Six-Month Growth Projection | `04-gtm/growth-projection.xlsx` |
| 1:30 to 1:50 | Loop and Moat Narrative | `04-gtm/loops-and-moats.md` |
| 1:50 to 2:00 | Commit and tag | All files pushed |

---

## Step 5: Commit at the end

```bash
git add 04-gtm/
git commit -m "[LAB-9] Growth modeling: strategy, unit economics, projection, loops"
git push origin main
git tag lab-9-submission
git push origin lab-9-submission
```

Every team member commits at least one file. The instructor checks the commit log.

---

## If you are stuck on a number

Label it clearly: `[TBD - benchmark needed]` or `[Assumption: will replace with data from live experiment]`. Do not leave cells blank. A labelled assumption is gradeable. A blank cell is not.

---

## Full instructions

See `Lab-9/README.md` for complete activity descriptions, grading criteria, and coaching notes.
