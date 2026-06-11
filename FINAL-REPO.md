# Final Repository Requirements
## CS-PD-2026 | Checkpoint 4: Demo Day
**Due:** Sunday June 14, 2026 at 23:59  
**Worth:** 5 points (Repository Review component of CP4)  
**Submission:** Push all work and tag your final commit `cp4-submission` before the deadline

---

## Before You Submit: Critical Checks

Review repositories in this sequence. Fail any of these and points are deducted immediately before the detailed review begins.

1. Does the live product URL in the README load without error?
2. Is the `cp4-submission` tag pushed before 23:59 on June 14?
3. Are all required files present at the correct paths?
4. Is all content team-specific with no unfilled template placeholders?

---

## Repository Must Be Set to Public (unless instructor has already been made collaborator)

Your repository must be publicly visible at the time of judge review. A private repository cannot be graded.

---

## Root Level Requirements

### README.md
Your root README must include all of the following:

- Product name and tagline
- Problem statement (2 sentences)
- Live product URL (clickable, must load without a 404)
- Demo video link
- All team member names
- Tech stack listed
- Setup instructions (prerequisites, install, run)
- Architecture overview or link to diagram
- Open-source licence declaration

### LICENSE
An open-source licence file (MIT or Apache 2.0) must be present in the repository root.

---

## Required Folder Structure

All folders `00-foundation` through `09-final` must be present and non-empty.

---

### 00-foundation/
| File | Description |
|------|-------------|
| `team-contract.md` | Original team contract from Lab 1 |
| `team-problem-statement.md` | Final agreed problem statement |
| `team-icp.md` | Ideal Customer Profile definition |

---

### 01-discovery/synthesis/
| File | Description |
|------|-------------|
| `patterns-analysis.md` | Themes from affinity mapping across 10+ interviews |
| `final-problem-statement.md` | Evidence-based final problem statement |
| `competitive-landscape-seed.md` | Initial competitive landscape from Lab 4 |

Underlying interview logs must also be present: 10 or more interviews, each with verbatim quotes and an affinity map.

---

### 02-design/
| File | Description |
|------|-------------|
| `prototypes/high-fidelity/figma-link.md` | Link to high-fidelity prototype in Stitch or Figma |
| `user-testing/usability-findings.md` | Findings from minimum 5 real users, with at least one documented design change made in response |

---

### 03-build/architecture/
| File | Description |
|------|-------------|
| `system-design.md` | Architecture pattern, component breakdown, data flow, AI tool usage annotated |
| `tech-stack.md` | Every technology choice with justification |
| `architecture-diagram.png` | Architecture diagram (or equivalent format) |

### 03-build/analytics/
| File | Description |
|------|-------------|
| `dashboard-link.md` | Link to live analytics dashboard showing real event data |

### 03-build/experiments/
| File | Description |
|------|-------------|
| `experiment-results.md` | Hypothesis in standard format, method, real user data, pivot-or-persevere decision with reasoning |

For reference on what this file should contain, see the Lab 8 materials in your repository under `lab-8/`.

### 03-build/privacy-security/
| File | Description |
|------|-------------|
| `consent-form.md` | GDPR-compliant consent flow covering: freely given, specific, informed, unambiguous, withdrawable, and documented. Must include separate consent categories, withdrawal mechanism, and storage record. |
| `security-tabletop.md` | STRIDE threat model applied to your 5 highest-traffic user flows. Every threat must be mitigated or accepted with rationale. Must include dependency audit results (`npm audit` or `pip-audit`) with critical and high findings addressed, plus a secrets check result. |

### 03-build/reliability/
| File | Description |
|------|-------------|
| `slo-sheet.md` | Minimum 2 SLIs with measurement method, SLO targets with time window, severity definitions (SEV1/SEV2/SEV3) calibrated to your product |
| `error-budget.md` | Error budget calculated with arithmetic shown for each SLO, plus policy for what happens when the budget is exhausted |

---

### 04-gtm/
| File | Description |
|------|-------------|
| `growth-strategy.md` | 3 named acquisition channels with type, justification, priority ranking, and activation metric with specific number and time window |
| `financials/unit-economics.md` | CAC and LTV per channel with arithmetic shown, LTV:CAC ratio (per channel and blended), payback period |
| `financials/12-month-model.xlsx` | 12-month financial model with revenue projections and cost structure |
| `growth-projection.xlsx` | 6-month projection with all required columns, 3 scenarios (expected/best/worst), and sourced assumptions |
| `loops-and-moats.md` | Viral loop diagram, K-factor with arithmetic shown, network effect type identified, moat narrative |

### 04-gtm/traction/
At least ONE of the following must be present:

- A signed Design Partner MOU or Letter of Intent from a real external party
- A waitlist document (CSV or markdown table) with a minimum of 20 signups, including source and date for each
- Analytics data showing a positive trend in a retention metric over at least 2 consecutive weeks

---

### 05-fundraising/
| File | Description |
|------|-------------|
| `pitch-deck.pdf` | A real 10-slide investor deck. Must be a genuine PDF with actual slides, not a placeholder. Required slides: Problem (with ICP and verbatim quote), Solution, Why Now, Market Size (TAM/SAM/SOM bottom-up), Product (screenshot of live deployed product), Traction (real analytics numbers), Business Model (CAC/LTV/payback), Go-to-Market, Competition (competitive matrix and moat statement), Ask |
| `one-pager.pdf` | Single A4 page with: header, problem, solution, traction (3 real numbers), business model table, market (SAM/SOM), team, ask. Must fit on one printed page. |

---

### 06-strategy/
| File | Description |
|------|-------------|
| `competitive-analysis.md` | Matrix of 5 or more competitors across 7 or more dimensions (scored 0 to 5), plus a 200-word synthesis paragraph identifying Porter's Five Forces threat, defensible gaps, and what would close them |
| `strategy-canvas.md` | Industry factors curve, your curve, ERRC table (Eliminate/Reduce/Raise/Create), 150-word narrative |
| `ecosystem-map.md` | Complements, partners (with status: confirmed/in discussion/identified), threats (with likelihood rating and counter-strategy), complementors, and a 150-word Strategic Priorities section |
| `moat-statement.md` | Named Helmer power, mechanism, 3 pieces of repository evidence. If evidence is unavailable, clearly label as "Moat Hypothesis" with an evidence collection plan and 60-day path forward |
| `product-roadmap.md` | Product roadmap from Lab 6 |
| `prioritization-framework.md` | Prioritization framework from Lab 6 |

---

### 07-team/
| File | Description |
|------|-------------|
| `contribution-logs/` | Weekly contribution log entries for all team members. Used for individual grade adjustments. |

---

### 08-legal/
| File | Description |
|------|-------------|
| `privacy-notice.md` | Data inventory covering every category collected, lawful basis per category, all third-party processors named, and retention periods. User rights section covering GDPR rights (access, erasure, rectification, restriction, portability, objection) with contact method and response time. Data breach procedure with 72-hour notification requirement and named responsible person. Contact details. |

---

### 09-final/
| File | Description |
|------|-------------|
| `case-study.md` | Full case study of your product journey |
| `demo-video.md` | Link or file path to your 60-second launch video. Structure: Hook (problem) / Product demo / Proof (traction) / Call to Action |

---

### docs/
| File | Description |
|------|-------------|
| `ai-usage-log.md` | Entry for every AI tool usage including: date, story, tool, task, files changed, disposition (accepted/modified/discarded), reviewer name |
| `standup-log.md` | At least 3 standups documented during Sprint 1 (or standup history in GitHub Issues) |

---

## Repository Process Requirements

These affect your Repo Discipline score and are checked by judges.

- Commits must be distributed across the development period. A cluster of commits immediately before the deadline is a red flag.
- Every team member must have commits in the repository. A repo where one person made all commits will trigger individual grade review.
- Submission tag `cp4-submission` must be pushed before Sunday June 14 at 23:59.
- All links in the README must resolve correctly at the time of judge review.

---

## Grading Criteria (5 points)

| Dimension | Weight |
|-----------|--------|
| Completeness (all required files present at correct paths) | 30% |
| Documentation quality (team-specific content, no placeholders) | 25% |
| Professional presentation (clear writing, organised structure) | 25% |
| Technical execution (code quality, PR history, commit discipline) | 20% |

Full rubric: https://github.com/ZA-KIU-Classroom/PRODUCT-DEV-FOR-SOFTWARE-ENGINEERS-SP26/blob/main/Lab-12/GRADING-RUBRIC.md

---

## Quick Checklist Before Tagging

- [ ] Repository is set to Public (unless instructor is collaborator)
- [ ] Live product URL loads without error
- [ ] All folders 00-foundation through 09-final are present and non-empty
- [ ] Root README contains all required sections including clickable live URL
- [ ] LICENSE file is present in the root
- [ ] `pitch-deck.pdf` is a real PDF with actual slides
- [ ] At least one traction item is present in `04-gtm/traction/`
- [ ] All links resolve correctly
- [ ] Every team member has commits
- [ ] No unfilled template placeholders anywhere
- [ ] `cp4-submission` tag pushed before Sunday June 14 at 23:59

---

*CS-PD-2026 | Spring 2026 | Kutaisi International University | Instructor: Zeshan Ahmad*
