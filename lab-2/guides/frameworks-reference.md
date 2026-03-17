# Frameworks Reference: Mom Test, Five Whys, and Jobs to Be Done

**Course:** CS-PD-2026 Product Development for Software Engineers
**Relevant to:** Lab 2 and all subsequent discovery and interview work

This document is a working reference. Keep it open during lab and while writing your homework. These three frameworks are the core tools of customer discovery. You will use all three in every interview you conduct this semester.

---

## 1. The Mom Test

### What It Is

The Mom Test is a set of rules for asking questions that produce honest, useful answers — even from people who want to be supportive or polite. It was developed by Rob Fitzpatrick and named after the observation that even your mum will tell you your idea is great if you ask the wrong questions.

The core problem it solves: people lie in interviews. Not maliciously — they do it to be kind, to seem helpful, or to avoid conflict. If you ask "do you think this is a good idea?", almost everyone will say yes. That yes is worthless. The Mom Test gives you questions that are almost impossible to answer politely if the answer is actually no.

### The Three Rules

**Rule 1: Talk about their life, not your idea.**

Every question should be about the interviewee's experience, not about your product or concept. The moment you describe what you are building, the interview becomes a product review. People start evaluating your idea instead of describing their reality. That data is corrupted.

Wrong: "We're building an app that shows real-time seat availability in the library. Do you think that would be useful?"
Right: "Walk me through what you do when you have a gap between classes and want to find somewhere to work."

**Rule 2: Ask about specifics in the past, not generalities or opinions about the future.**

Past behaviour is real data. Future intentions are fiction. When people describe what they have actually done, they are constrained by reality. When they describe what they would do, they are imagining a best version of themselves in a hypothetical situation — and that person is always more rational, more motivated, and more organised than the real person.

Wrong: "Would you use a tool like this regularly?"
Right: "Tell me about the last time you had a problem finding somewhere to work on campus. What did you do?"

Wrong: "How often do you think you'd encounter this problem?"
Right: "How many times in the past two weeks has this come up for you?"

**Rule 3: Listen more than you talk.**

Your ratio in a customer discovery interview should be roughly 20% talking, 80% listening. If you are explaining, defending, or filling silence with your own words, you are not learning. Silence after a question is not a problem — it usually means the person is thinking, and what comes after the pause is often the most honest thing they say.

### What a Mom Test-Compliant Question Looks Like

| Non-compliant | Compliant | Why |
|---------------|-----------|-----|
| "Would you pay for something that solved this?" | "Have you ever paid for anything to help with this? What did you pay for?" | Past behaviour vs future intention |
| "Don't you find the current system frustrating?" | "What do you think of the current system?" | Leading vs neutral |
| "Is this a big problem for you?" | "How much time do you lose when this happens?" | Vague vs specific |
| "Would you use this feature?" | "When this problem comes up, what do you do?" | Future hypothetical vs past behaviour |
| "Do you struggle with X?" | "Tell me about the last time X happened." | Yes/No vs open narrative |

### What the Mom Test Does Not Fix

The Mom Test improves the quality of individual questions. It does not fix a bad ICP (you are still talking to the wrong person), a bad problem hypothesis (you are still investigating the wrong thing), or confirmation bias in how you interpret answers. It is a tool for getting honest data — what you do with that data is a separate skill.

---

## 2. The Five Whys

### What It Is

The Five Whys is a root cause analysis technique developed by Taiichi Ohno at Toyota. The principle is simple: when you encounter a problem or a behaviour, ask "why" repeatedly — typically five times — until you reach the underlying cause rather than the surface symptom.

In customer discovery, it is used during the problem deep dive phase of interviews to move from surface-level complaints to genuine root causes. Surface-level complaints produce surface-level solutions. Root causes produce solutions that actually address why the problem exists.

### Why It Matters

Most interviewees will give you their first-level explanation of a problem, which is usually a symptom. If you take that at face value and build a solution for it, you are treating the symptom. The root cause — which might be structurally different — will remain, and your product will not solve it.

Example of stopping too early:

"I can't find a study space." → Build a room finder app.

Example of going to root cause:

"I can't find a study space." → Why? "Because I don't know which spaces are available before I walk to them." → Why don't you know? "Because there's no real-time information anywhere." → Why is there no real-time information? "Because the booking system only tracks formal reservations, not actual occupancy." → Why does that gap exist? "Because no one is measuring occupancy — it would require sensors or check-in behaviour that doesn't exist."

Now you understand the structural problem: the absence of occupancy data. Your solution space is completely different. You might build a crowdsourced check-in system, a sensor integration, or a social coordination tool — not just a room finder that queries the same broken booking system.

### How to Use It in an Interview

You do not ask "why" five times in rapid succession — that feels like an interrogation. Instead, embed it naturally into the conversation using the following phrases:

- "Why do you do it that way?"
- "What makes that the approach you take?"
- "What's behind that?"
- "Help me understand why that matters."
- "And why is that?"

Each time the interviewee answers, pause, consider whether they have reached a root cause or described another symptom, and probe again if needed.

### Knowing When to Stop

You have reached a root cause when:

- The answer is structural or systemic, not behavioural ("the system doesn't capture that data" rather than "I don't check it")
- Further "why" questions would go outside the problem space into human psychology or organisational politics that you cannot address with a product
- The interviewee says something that surprises you — unexpected answers are often signs you have gone deep enough

You have not yet reached a root cause when:

- The answer is still a behaviour you can ask "why" about
- The answer restates the original problem in different words
- You feel like you still do not understand why the problem exists

### A Worked Example

**Surface complaint:** "I always end up doing my coursework in the noisy cafeteria."

Why?
"Because I can't find anywhere quiet."

Why can't you find anywhere quiet?
"Because I don't know which rooms are free until I physically walk there."

Why don't you know which rooms are free?
"Because there's no way to check from my phone. The booking portal only shows which rooms are formally reserved."

Why does the portal only show formal reservations?
"I think it only tracks bookings made through the system — it has no idea whether a room is actually occupied or just unlocked and empty."

Why is that a problem specifically?
"Because half the quiet rooms on campus are usable but not bookable — they're just open access. And I have no way of knowing if anyone's in them."

Root cause: There is no data layer for non-bookable, open-access spaces. The user's problem is not just "no room finder" — it is that the occupancy data for the most relevant spaces does not exist anywhere.

---

## 3. Jobs to Be Done

### What It Is

Jobs to Be Done (JTBD) is a framework for understanding why people use products. It was developed primarily by Clayton Christensen and further refined by Bob Moesta. The central insight is that people do not buy products — they hire them to do a job. Understanding the job clarifies what your product must actually accomplish, and who your real competition is.

The classic example: people do not buy a quarter-inch drill. They buy a quarter-inch hole. If a better way to make holes without a drill existed, they would switch immediately. The drill is hired for the job of hole-making.

### Why It Matters for Your ICP and Problem Statement

JTBD gives you a precise way to describe what your target user is actually trying to accomplish. This is different from describing the problem. The problem is what goes wrong. The job is what the user is trying to do despite the problem going wrong.

Distinguishing the two matters because solutions to the problem and solutions to the job are often different things. A solution that eliminates the problem but does not help the user complete the job will not be adopted. A solution that helps the user complete the job — even if it does not fully eliminate the problem — will.

### The JTBD Format

The standard format for writing a JTBD statement is:

**"When [situation], I want to [motivation], so I can [desired outcome]."**

- **Situation:** The specific context in which the job arises. Not "when I'm at university" but "when I have a two-hour gap between classes and need to do focused work."
- **Motivation:** What the person is trying to do in that moment. Not "find a room" but "immediately know where I can go to work without searching."
- **Desired outcome:** The final state they are trying to reach. Not "be in a room" but "use that time productively and leave campus feeling the day was worthwhile."

### Functional, Emotional, and Social Jobs

Every job has three dimensions. Strong JTBD statements acknowledge all three.

**Functional job:** The practical task the person is trying to accomplish.
"I want to find a quiet workspace within five minutes."

**Emotional job:** How the person wants to feel during or after the task.
"I want to feel that my time on campus is under my control, not wasted by circumstances."

**Social job:** How the person wants to be perceived by others, or how they perceive themselves.
"I want to be the kind of student who uses their time well — not someone who kills two hours scrolling in the cafeteria."

In your ICP and interview work, the emotional and social jobs are often the ones that determine whether someone will actually change their behaviour to adopt a new solution. Functional jobs tell you what to build. Emotional and social jobs tell you whether people will use it.

### JTBD in Practice: What to Listen For in Interviews

When an interviewee describes their workaround, ask:

- "What were you trying to accomplish when you did that?"
- "What does a good outcome look like for you in that situation?"
- "How do you feel when you manage to do that successfully? And when you don't?"

The answers to these questions reveal the job. Once you know the job, you can evaluate your proposed solution against it: does it actually help the person complete the job, or does it only address one symptom of the problem?

### A Worked Example

**Surface behaviour:** Student messages WhatsApp groups to find a study space.

**Obvious interpretation:** The job is "find a study space."

**JTBD analysis:**

Functional job: "When I have a class gap, I want to immediately know where I can go to do focused work, so I can sit down and start working without a search process."

Emotional job: "When I have a class gap, I want to feel like I have a plan for the next two hours, so I don't experience that low-level anxiety of not knowing where I'll end up."

Social job: "When I have a class gap, I want to use my time the way a serious student would, so I can maintain my own self-image as someone who works hard and does not waste time."

**Implication for your solution:** A product that shows available rooms solves the functional job. But a product that also removes the uncertainty anxiety and makes it feel effortless to be productive addresses all three dimensions — and is much harder to compete with.

---

## Using All Three Together

These frameworks are not independent tools. In a well-executed customer discovery interview, all three operate simultaneously:

1. **Mom Test** governs how you ask questions — past-tense, about behaviour, non-leading, open-ended.
2. **Five Whys** governs how deep you go once an interesting thread emerges — you keep asking "why" until you reach a structural root cause, not just a surface complaint.
3. **JTBD** governs how you interpret what you hear — you are always listening for the functional, emotional, and social job beneath the stated behaviour, because that is what your product ultimately needs to serve.

A question that applies all three at once: "Tell me about the last time you were looking for somewhere to work on campus and couldn't find it. Walk me through exactly what you did." (Mom Test: past-tense, specific, non-leading.) Then: "Why did you try it that way?" repeated until root cause. (Five Whys.) Then: "What were you ultimately trying to accomplish that afternoon?" (JTBD.)

The combination is what separates a productive discovery interview from a pleasant conversation that produces nothing actionable.
