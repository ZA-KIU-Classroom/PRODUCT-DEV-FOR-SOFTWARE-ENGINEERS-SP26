# Experiment Design Guide

Use this guide while filling `experiment-plan.md`.

---

## The Point of the Experiment

The experiment exists to test the riskiest assumption fast and cheaply.

You are not trying to prove you are right. You are trying to find out if you are wrong before you spend more build time.

---

## A Hypothesis Needs Four Parts

Your hypothesis should name:

1. target user
2. specific problem
3. measurable behavior
4. underlying reason

Example:

> We believe KIU students who lose study time to space hunting will sign up for occupancy alerts at 20% or more because they want a reliable signal before they leave home.

This works because it has a user, a pain, a measurable action, and a reason.

---

## Experiment Methods

### Smoke Test
Use when you want to test demand before the product exists.

Typical setup:
- landing page
- short explanation of value
- real call to action such as signup, join waitlist, or request access

### Wizard of Oz
Use when you want the user to believe the feature works automatically, but a human is handling the work behind the scenes.

### Concierge MVP
Use when you want to deliver the value manually and learn from close contact with a small number of users.

### Prototype Test
Use when you need to test usability or comprehension before build, not market demand.

Pick the cheapest method that could kill the assumption.

---

## Success and Failure Thresholds

Set both before launch.

Good:

- success at 20% or more signup conversion
- failure below 10%
- gray zone between 10% and 19%

Bad:

- we will know it when we see it

If the threshold changes after results come in, the team is rationalising.

---

## What Counts as Signal

Good signals are behaviors:

- click
- signup
- booking
- payment
- reply from real target user
- repeat action

Weak signals are opinions:

- likes
- compliments
- survey scores by people who know you

---

## Common Mistakes

- testing on teammates
- hypothesis with no number
- measuring opinions instead of actions
- building during the experiment window instead of measuring
- choosing a big launch when a small test would work better

---

## Minimum Standard for This Course

A good experiment plan in this course has:

- one primary assumption
- one method
- clear thresholds
- real target users
- time window and sample goal
- clear decision rule
