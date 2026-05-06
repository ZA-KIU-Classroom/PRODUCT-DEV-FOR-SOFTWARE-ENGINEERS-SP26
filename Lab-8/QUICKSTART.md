# Lab 10 QUICKSTART

If you missed the lab session or arrived late, this is the absolute minimum to produce passable deliverables. This is not a substitute for the full lab. It is a recovery path.

---

## You Have 90 Minutes

Set a timer. Work in this order. Do not skip ahead.

---

## Step 1 (15 min) -- Pick Three Channels

Open `templates/growth-strategy-template.md`. Copy to `04-gtm/growth-strategy.md`.

Answer in writing:

1. Where does your target user already spend time online?
2. Who do they trust for product recommendations in your category?
3. What is the cheapest way to put your product in front of them?

The answers to those three questions are your three channels. Classify each as paid, organic, viral, or sales. Write one paragraph per channel covering fit, speed, and cost. Done.

---

## Step 2 (25 min) -- Calculate CAC and LTV

Open `templates/unit-economics-template.md`. Copy to `04-gtm/financials/unit-economics.md`.

For each channel, fill in:

```
Channel: [name]
Total spend: $[amount]
Customers acquired: [number]
CAC = total spend / customers = $[amount]
```

For your product:

```
ARPU (monthly): $[amount]
Gross margin: [%]
Average lifetime: [months]
LTV = ARPU × margin × lifetime = $[amount]
```

Compute:

```
LTV:CAC ratio per channel = [LTV] / [CAC]
Payback period = CAC / (ARPU × margin) = [months]
```

If you do not have real numbers yet, use industry benchmarks but cite them and mark them as placeholders.

---

## Step 3 (35 min) -- Build the Spreadsheet

Open `templates/growth-projection-template.xlsx`. Copy to `04-gtm/financials/growth-projection.xlsx`.

Fill in months 1 through 6 for each channel. Columns are pre-built. The minimum to pass:

- Conversion rates as formulas, not hardcoded numbers.
- Three scenarios: best, expected, worst (use the toggle cell).
- Cumulative user count chart on the Output tab.
- No errors on submission.

If you have under 30 minutes left, fill expected case only and acknowledge in the document that best and worst cases are pending.

---

## Step 4 (15 min) -- Loops and Moats

Open `templates/loops-and-moats-template.md`. Copy to `04-gtm/loops-and-moats.md`.

Answer four questions in writing, three sentences each:

1. Does the product have a viral loop? If yes, what is K? If no, why not?
2. Does the product have network effects? Which type?
3. What protects you against a copycat at 10x your size?
4. What is the riskiest assumption in your growth model?

Done.

---

## Submit

```bash
git add 04-gtm/
git commit -m "[LAB-10] Growth modeling deliverables"
git push
git tag lab-10-submission
git push --tags
```

Paste the commit URL in the Lab 10 Teams thread.

---

## If You Fall Short

Commit what you have. Open an issue titled "Lab 10 incomplete -- planned completion by [date]" with what is missing. Finish before the Sprint 1 close-out at Wednesday 13 May 23:59. One resubmission allowed for up to 80% of lost participation marks.

---

## Common Mistakes to Avoid

- Skipping the rejected channel. Knowing what you said no to matters.
- Picking three channels of the same type.
- Using "we think it is around 5%" without a source.
- Hardcoding spreadsheet numbers instead of formulas.
- Forgetting to push the tag.

---

**Last updated:** 5 May 2026
