# Technical Risk Guide

Use this guide while filling `risk-register.md`.

---

## What Counts as a Technical Risk

A technical risk is a concrete system level uncertainty that could block, degrade, or distort Sprint 1.

Examples:

- Search response may be too slow once multiple filters are applied
- Auth email flow may break first session activation
- Third party API quota may block the main workflow
- Data model may not support real time availability updates cleanly

These are technical risks.

The following are not the focus here:

- We are busy
- We are stressed
- Communication may be hard

Those are real, but they belong in team management, not this document.

---

## How to Write a Strong Risk

A strong risk statement has three parts:

1. what could fail
2. why it matters
3. where it would surface

Weak:

- Database risk

Strong:

- Concurrent booking writes may create double booking because the current write path lacks a locking or validation rule

---

## Spikes

A spike is a short, timeboxed investigation to answer one technical question.

Good spike:

- Can Supabase row level security handle our booking access rules without custom backend logic?

Weak spike:

- Research backend options

The spike should produce a decision, not endless notes.

---

## Prioritise Like This

Rank higher if the risk is:

- close to the core request
- hard to detect late
- expensive to fix once the sprint is underway
- likely to damage the live demo or experiment

---

## Minimum Standard

Your top three risks should each have:

- owner
- likelihood
- impact
- mitigation or spike
- earliest detection point
