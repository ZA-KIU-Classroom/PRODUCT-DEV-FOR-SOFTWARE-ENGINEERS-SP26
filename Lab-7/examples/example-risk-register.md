# Example Risk Register

**Team:** StudySpace Finders  
**Product:** StudySpace  
**Date:** 23 April 2026

> Fictional example for structure only.

---

## Top Technical Risks

| Risk ID | Risk statement | Likelihood, Low Medium High | Impact, Low Medium High | Earliest detection point | Mitigation or spike | Owner | Status |
|--------|----------------|-----------------------------|-------------------------|--------------------------|--------------------|-------|--------|
| R1 | Booking write path may allow the same slot to be reserved twice | Medium | High | First concurrent booking test | Add server side availability check and write test | David | Open |
| R2 | Email auth confirmation may block first session activation | Medium | High | First signup walkthrough | Instrument drop off and keep demo accounts ready | Ana | Open |
| R3 | Search may feel slow if geocoding runs on every request | Medium | Medium | First integrated search test | Cache seeded coordinates and allow fallback | Nino | Open |
| R4 | Analytics events may not fire reliably from all critical states | Medium | Medium | First end to end demo rehearsal | Validate each event manually and log test cases | Ana | Open |

---

## Notes on the Top 3

### R1
- Why this matters to Sprint 1: double booking breaks the main trust promise
- What evidence would show the risk is real: two users reserve one slot successfully
- What you will do first: write a targeted booking validation test

### R2
- Why this matters to Sprint 1: users may never reach search and booking
- What evidence would show the risk is real: signup completion rate collapses at email step
- What you will do first: test seeded accounts and track signup drop off

### R3
- Why this matters to Sprint 1: slow search damages first use experience
- What evidence would show the risk is real: search latency spikes when geocoding is called
- What you will do first: pre seed coordinates for initial venue list

---

## Spike Plan

| Spike | Question to answer | Timebox | Owner | Output |
|------|--------------------|---------|-------|--------|
| Spike 1 | Can one slot be locked or validated safely before booking write? | 90 minutes | David | Decision note plus one tested implementation path |
| Spike 2 | Do we need live geocoding in Sprint 1, or will seeded coordinates be enough? | 45 minutes | Nino | Keep or remove external dependency |
