# 🎤 Interview Prep — Product Management

> Format guide + question bank. PM interviews are unlike any other technical field — you're being assessed on judgment, not correctness. Worth reading before your first mock.

[← Job Hunt](05-job-hunt.md) · [Hub](README.md)

---

## Interview formats by role

| Format | What's actually being tested |
|---|---|
| **Product sense / product design** | Can you frame a user problem, prioritize, and propose a measurable solution? |
| **Analytical / metrics** | Can you define the right metric, diagnose a drop, and design a fair experiment? |
| **Estimation / market sizing** | Can you reason from first principles to a defensible number? |
| **Technical** | Can you work credibly with engineers? Do you understand basic system concepts? |
| **Behavioral / leadership** | Have you demonstrated influence without authority, cross-functional collaboration, and recovery from failure? |
| **Strategy / roadmap** | Can you make and defend a prioritization call with incomplete information? |

> There's no universally "right" answer in PM interviews. Interviewers are evaluating **how you think**, not whether you landed on the "correct" feature or metric. Structure and honesty about tradeoffs matter more than matching whatever answer the interviewer had in mind.

---

## Format 1: Product sense / product design

The most common PM interview format. You'll get a prompt like:
- *"Design a product for elderly users who want to stay connected with family."*
- *"How would you improve Google Maps?"*
- *"Design an alarm clock for the blind."*

### The framework (CIRCLES-adjacent — adapt it, don't recite it)

1. **Clarify scope** — ask one or two scoping questions before diving in. Is this mobile or desktop? Are we optimizing an existing product or designing net-new?
2. **Define the user** — pick a specific user segment and describe them concretely. Don't say "all users." Say "working parents who want to share daily moments with grandparents."
3. **State user goals and pain points** — what are they trying to accomplish? Where does the current experience break down?
4. **Brainstorm solutions** — generate 3–5 possible solutions. Don't just pick one immediately; interviewers want to see breadth.
5. **Prioritize and justify** — pick your top 1–2 solutions and explain why: impact, feasibility, alignment with user need.
6. **Define success** — what metric would tell you this worked? What's your North Star for this feature?
7. **Acknowledge trade-offs** — what are the downsides of your recommendation? What would you watch for?

**Practice gate:** you can walk through a product design prompt for an unfamiliar product in under 8 minutes with clear structure, without being prompted by the interviewer.

---

## Format 2: Analytical / metrics

Prompts:
- *"DAU on our messaging feature dropped 15% last Tuesday. Walk me through how you'd investigate."*
- *"We're launching a new onboarding flow. What metric would you use to measure success?"*
- *"How would you define the North Star metric for Spotify?"*

### Diagnosing a metric drop — the structured approach

1. **Confirm the data** — is this a real drop or a logging/instrumentation issue? Check for code changes, tracking bugs, or A/B test misconfiguration deployed around that time.
2. **Segment the drop** — is it across all platforms/regions/user cohorts, or isolated? iOS vs Android, new users vs retained users, specific geography?
3. **Check for external events** — holiday, competitor launch, media event, app store policy change?
4. **Trace the funnel** — where exactly does the drop occur? Top of funnel (acquisition), activation, engagement, retention?
5. **Form hypotheses** — list 3–5 plausible root causes ranked by likelihood.
6. **Propose investigation steps** — which query or experiment would confirm/refute each hypothesis?
7. **Recommend a response** — once you know the cause, what do you do?

### Defining a good metric

A good PM metric is:
- **Measurable** — you can actually pull this number
- **Leading, not lagging** — it moves before the business outcome, not after
- **Sensitive to what you're building** — a feature that improves activation shouldn't be measured by LTV on day 1
- **Not gameable** — team shouldn't be able to hit the number by changing user behavior in harmful ways

**Practice gate:** you can take a "metric dropped X%" prompt and run a coherent structured investigation without prompting, ending with a prioritized hypothesis list and a recommended next step.

---

## Format 3: Estimation

Prompts:
- *"How many Uber rides happen in New York City on a Friday night?"*
- *"Estimate the market size for a subscription dog-food service."*
- *"How many iPhones are sold globally per year?"*

Estimation is not about the right number. It's about **structured decomposition** and **calibrated assumptions**.

### The approach

1. **State your approach** before calculating — "I'll estimate this by breaking the US adult population into relevant segments."
2. **Make assumptions explicit** — "I'm assuming X% of adults own a dog" — say the number and defend it briefly.
3. **Do the math out loud** — use round numbers, show your work.
4. **Sanity-check the result** — does it feel plausible? If the answer is "500 billion rides per day," something's wrong.
5. **Acknowledge uncertainty** — "my biggest assumption here is X; if that's off by 2x, the answer changes significantly."

**Practice gate:** you can estimate the number of "how many X" prompts end-to-end in under 5 minutes with explicit assumptions and a sanity check.

---

## Format 4: Technical

PM-level technical questions don't require you to write code. They test whether you can work credibly with engineers.

### Topics to be fluent in

- **APIs:** what is an API, what's a REST endpoint, what happens when a client calls an API and it fails? (PMs write PRDs with API specs regularly.)
- **Databases:** the difference between a relational DB (SQL) and a NoSQL store; when you'd use each.
- **Basic system architecture:** client → server → database; what a microservice is; what a CDN does.
- **Latency vs throughput:** what a p99 latency is; why it matters for user experience.
- **A/B testing infrastructure:** how an experiment is randomized; what a holdout group is.
- **SQL basics:** you should be able to write a basic SELECT/GROUP BY/JOIN — many PM jobs now require it.

### Common technical PM questions

- "Walk me through what happens when a user clicks 'Post' on Instagram."
- "We have a feature that works well for 99% of users but causes timeouts for 1%. How do you prioritize fixing it?"
- "What's the difference between synchronous and asynchronous processing? Why would you choose each?"
- "Our API is slow under load. What questions would you ask the engineering team to understand the problem?"

**Practice gate:** you can explain what happens between a user clicking a button and data appearing on screen without using the phrase "the computer just does it."

---

## Format 5: Behavioral / leadership (STAR)

PM behavioral questions probe for **influence without authority**, **cross-functional collaboration**, and **judgment under ambiguity**.

### The STAR structure

**S**ituation → **T**ask → **A**ction → **R**esult. Lead with the result if it's strong.

### Question bank with what interviewers want to hear

**Influence without authority:**
- *"Tell me about a time you got an engineering team to prioritize something they didn't want to build."*
  — Interviewers want: data you used to make the case, how you addressed their concerns, outcome.

**Prioritization under pressure:**
- *"Tell me about a time you had to cut scope. How did you decide what to cut?"*
  — Interviewers want: your prioritization framework, how you communicated the decision, what you shipped.

**Cross-functional conflict:**
- *"Tell me about a time you disagreed with a designer/engineer/stakeholder about the direction."*
  — Interviewers want: how you gathered data or user evidence, whether you updated your view, outcome.

**User advocacy:**
- *"Tell me about a time you pushed back on something leadership wanted because you believed it was wrong for users."*
  — Interviewers want: what evidence you used, how you framed it, what happened.

**Failure and learning:**
- *"Tell me about a product decision that didn't work out. What did you do and what did you learn?"*
  — Interviewers want: honest acknowledgment of what went wrong, specific learning, what you'd change.

**Ambiguity:**
- *"Tell me about a time you had to make a decision with incomplete information."*
  — Interviewers want: how you reduced uncertainty, what you did to move forward, how you monitored.

---

## Format 6: Strategy and roadmap

Prompts:
- *"You're the PM for Gmail. What would you work on next quarter and why?"*
- *"We have 20 feature requests from enterprise customers and 6 weeks of engineering time. How do you decide what to build?"*

### How to approach a roadmap question

1. **Frame the strategy first** — what is this product trying to accomplish in this time horizon? What's the company's North Star?
2. **Segment the ideas** — growth/acquisition, activation, retention, monetization, infrastructure/debt
3. **Apply a framework** — RICE (Reach × Impact × Confidence ÷ Effort) or ICE is useful here; state what you'd score and why
4. **Show trade-offs** — what are you deprioritizing, and why? Interviewers want to see that you can say no.
5. **Define success** — what metric moves if you're right?

---

## The AI / LLM question (all PM roles, 2026)

You will be asked: *"How do you see AI changing product management?"* or *"How do you use AI in your daily PM work?"*

Strong answer signals:
- You use AI tools in your workflow now (drafting PRDs, summarizing user research, generating acceptance criteria drafts) — but you own and verify the output
- You understand that tactical Product Owner work (ticket-writing, story grooming) is most exposed to automation
- You understand the differentiated value PMs bring: discovery, user empathy, prioritization judgment, stakeholder influence — things AI amplifies but doesn't replace
- If you're interested in AI PM as a specialization: you understand the unique challenges (non-deterministic outputs, evaluation, responsible AI requirements, model drift)

**Don't overclaim.** "I use Claude to help draft user stories and then review them carefully" is a better answer than "I've built a full LLM pipeline for PM work."

---

## APM-specific prep

APM program interviews differ from standard PM loops. Expect:

- **Product design questions** — same format as above; you're assessed on structured thinking, not domain knowledge
- **Analytical thinking cases** — "here's a chart showing user drop-off; what do you think is happening?" — they want to see systematic decomposition
- **Why PM / why this company** — they're building a pipeline; they want to know your commitment and your reasoning are genuine
- **Estimation** — common in APM screens to assess quantitative reasoning
- **Behavioral** — emphasize experiences that demonstrate cross-functional influence, user empathy, and intellectual curiosity

**APM prep resource:** Exponent (tryexponent.com) has an APM-specific question bank — worth the free tier at minimum.

---

## Quick-drill question list

Bookmark this and run through 2–3 per day:

**Product sense:**
- How would you improve the YouTube home feed?
- Design a product that helps people manage chronic illness.
- What metric would you use to measure the health of Slack?

**Metrics:**
- How do you define "active user" for a B2B SaaS product?
- Retention for our mobile app dropped 8% month-over-month. Walk me through your investigation.
- We A/B tested a new onboarding flow and sign-ups went up 12% but day-7 retention dropped 5%. What do you do?

**Estimation:**
- How many pizzas are ordered in the US on Super Bowl Sunday?
- Estimate the total addressable market for a grocery delivery service.

**Technical:**
- What happens when a user searches on Google? (Walk through the full system.)
- What's a webhook and when would you use it instead of polling?

**Behavioral:**
- A time you had to say no to a customer request.
- A time you changed your mind based on data.
- A feature you shipped that you're proud of and one you'd do differently.

---

[← Job Hunt](05-job-hunt.md) · [Hub](README.md) · [Certifications](certifications.md)
