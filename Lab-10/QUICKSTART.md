# Lab 10 Quick Start

**2-Minute Setup | Compliance, Security, and Reliability Audit**

---

## Step 1: Check Your Readiness (2 minutes)

Answer all of these before the session starts:

- [ ] Have you reviewed the Week 11 lecture slides (Legal, IP, Privacy, Security, Reliability)?
- [ ] Is your live deployment URL working right now from outside your network?
- [ ] Do you have your event schema open? You need to know every data field you collect.
- [ ] Can you name every third-party service your product sends data to?

If any answer is no, resolve it in the first ten minutes of the session before touching the templates.

---

## Step 2: Create Your Folders (1 minute)

```bash
mkdir -p 08-legal
mkdir -p 03-build/privacy-security
mkdir -p 03-build/reliability
touch 08-legal/privacy-notice.md
touch 03-build/privacy-security/consent-form.md
touch 03-build/privacy-security/security-tabletop.md
touch 03-build/reliability/slo-sheet.md
touch 03-build/reliability/error-budget.md
```

---

## Step 3: Copy Templates (2 minutes)

From `Lab-10/templates/`, copy each template to the correct location:

| Template | Copy to |
|----------|---------|
| `privacy-notice-template.md` | `08-legal/privacy-notice.md` |
| `consent-form-template.md` | `03-build/privacy-security/consent-form.md` |
| `security-tabletop-template.md` | `03-build/privacy-security/security-tabletop.md` |
| `slo-sheet-template.md` | `03-build/reliability/slo-sheet.md` |
| `error-budget-template.md` | `03-build/reliability/error-budget.md` |

---

## Lab Flow (120 minutes)

```
0:00 to 0:10  |  Setup and folder check
0:10 to 0:40  |  Part 1: Privacy Notice
              |  Use: privacy-notice-template.md
              |
0:40 to 1:00  |  Part 2: Consent Flow Design
              |  Use: consent-form-template.md
              |
1:00 to 1:30  |  Part 3: Security Tabletop
              |  Use: security-tabletop-template.md
              |  Run npm audit or pip-audit during this part
              |
1:30 to 1:50  |  Part 4: SLO Sheet and Error Budget
              |  Use: slo-sheet-template.md and error-budget-template.md
              |
1:50 to 2:00  |  Commit everything and apply tag
```

---

## Commit at the End

```bash
git add 08-legal/ 03-build/privacy-security/ 03-build/reliability/
git commit -m "[LAB-10] Compliance, security, and reliability audit"
git push origin main
git tag lab-10-submission
git push origin lab-10-submission
```

---

## If You Are Stuck

**Cannot name your lawful basis for data collection?**
For most student products: data collected to provide the service = contract or legitimate interest. Analytics = legitimate interest if you have a notice. Marketing = consent only.

**Cannot find your third-party processors?**
Check your `package.json` or `requirements.txt`. Every analytics SDK, auth provider, and hosting service is a processor. List them all.

**STRIDE feels abstract?**
Start with: can someone pretend to be another user in this flow? That is Spoofing. Work through the six letters one at a time.

**SLO feels like a guess?**
It is at this stage. Write "assumption to be replaced with measured data" and set a realistic target. 99% availability on a Vercel hobby plan is achievable. 99.99% is not.

---

**Full instructions:** README.md in this folder
**Worked examples:** Lab-10/examples/
**Questions during lab:** Raise your hand or wait for the instructor checkpoint
