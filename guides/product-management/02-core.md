# ⚙️ Phase 2: Core PM Skills

> **~160 hrs total** · your pace, no deadline
> Discovery vs delivery, prioritization frameworks, PRDs, metrics, OKRs, and stakeholder management.

[← Phase 1](01-foundations.md) · [Hub](README.md) · [Next: Phase 3 — Specialization →](03-specialization.md)

---

## Product Discovery vs Delivery (~40 hrs)

This is the most important conceptual distinction in modern PM practice. Get it wrong and you'll spend your career building the wrong things really well.

### What discovery is

**Discovery** is the work you do *before* building to determine:
- Is this actually a problem worth solving?
- Do users experience this problem the way we think they do?
- Is our proposed solution actually something they'd use?
- Is it technically feasible without a huge lift?
- Does it make business sense?

Discovery outputs: user interview findings, opportunity assessments, problem statements, solution prototypes tested with users.

**Delivery** is the work of building and shipping a solution that's already been validated. Delivery output: shipped features, deployed code, release notes.

> The failure mode most PM teams fall into: treating every idea as ready for delivery, and only discovering the problems *after* it's built. Marty Cagan calls this the "build trap" — Melissa Perri's book of the same name is required reading.

### Continuous discovery (Teresa Torres)

Teresa Torres's *Continuous Discovery Habits* framework argues that discovery should not be a phase — it should be a weekly habit. The core practice: talk to at least one customer per week, consistently, and connect what you learn to a structured opportunity solution tree.

This doesn't require a formal research budget. It just takes discipline and a habit of keeping 3–5 users you can reach out to.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Map a discovery opportunity tree | Notion or paper | Take your running-example product, identify the outcome you want, and map the assumptions underneath it | **Free** |
| Write a user interview guide | Notion | 5–7 questions that explore a problem space (not validate your solution) | **Free** |
| Conduct 3 user interviews | Video call or in person | Talk to real users of your chosen product; synthesize what you heard | **Free** |
| Read "Dual-Track Agile" | SVPG article | Understand how discovery and delivery run in parallel on empowered teams | **Free** |

**Practice gate:** you can explain the difference between discovery and delivery, describe what outputs belong to each, and identify one example where skipping discovery caused a real product failure.

---

## Prioritization Frameworks (~50 hrs)

Prioritization is the skill interviewers dig into hardest because it reveals whether you can make real tradeoffs. You need fluency with the major frameworks — but more importantly, you need to be able to explain *why* you chose one over another for a given context.

### RICE

**R**each · **I**mpact · **C**onfidence · **E**ffort

Score = (Reach × Impact × Confidence) / Effort

- **Reach:** how many users affected per time period (number, not percentage)
- **Impact:** estimated impact per user (1 = low, 2 = medium, 3 = high, 0.5 = minimal — use a multiplier scale)
- **Confidence:** how confident are you in your estimates? (100% = high, 80% = medium, 50% = low)
- **Effort:** person-months of work across all functions

Use RICE when you have multiple features to compare and need a defensible ranking to bring to stakeholders. Weakness: the inputs are estimates, so RICE can give you false precision if you're not careful about it.

### MoSCoW

**M**ust have · **S**hould have · **C**ould have · **W**on't have (this time)

Used primarily for **release planning** — deciding what goes into a specific launch or sprint. Works best when paired with a deadline and a constrained scope. Weakness: everything gets labeled "Must" if you're not disciplined.

### Kano Model

Classifies features into three buckets based on how they affect user satisfaction:
- **Basic/threshold features:** users are angry if absent, indifferent if present (expected)
- **Performance features:** more = more satisfaction (linear)
- **Delighters:** unexpected features that disproportionately increase satisfaction

Use Kano for **deciding what kind of features to invest in**, not for ranking a backlog. Especially useful when you're trying to understand whether you're working on hygiene vs growth vs delight.

### ICE

**I**mpact · **C**onfidence · **E**ase

Score = (Impact × Confidence × Ease) / 3 (or averaged)

Simpler than RICE — no Reach factor. Used in growth/experimentation contexts. Fast to apply across many ideas. Weakness: more subjective, no volume signal.

### When to use which

| Framework | Best for |
|---|---|
| **RICE** | Comparing features with different audience sizes and effort levels |
| **MoSCoW** | Release scope decisions against a fixed deadline |
| **Kano** | Understanding the nature of what you're building, not just ranking it |
| **ICE** | Quick growth-experiment triage; many ideas, fast scoring |

The framework isn't the answer — your research, stakeholder context, and judgment are. Frameworks structure the conversation.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| RICE score 5 features | Google Sheets | Take 5 hypothetical features for your running product; score each with RICE; defend your estimates | **Free** |
| MoSCoW a release | Notion | Given a fixed 2-week sprint, sort a 12-item backlog into must/should/could/won't | **Free** |
| Kano analysis exercise | Notion or paper | For your product, classify 10 features into Basic / Performance / Delighter and explain why | **Free** |
| Read "How to Prioritize" (Lenny's) | lennysnewsletter.com | Practitioner breakdown of how real PMs prioritize | **Free** tier |

**Practice gate:** you can score a set of features using RICE, explain each input, and articulate why RICE might mislead you on a specific item.

---

## Writing PRDs and User Stories (~30 hrs)

Phase 1 introduced writing. Phase 2 is where you get the reps in.

### PRD structure

There's no single canonical PRD format. Different companies use different templates. The consistent elements:

1. **Problem statement** — what problem exists, for whom, and why it matters now
2. **Goals and success metrics** — what does success look like? What numbers change?
3. **Non-goals** — what you are explicitly *not* solving (important to prevent scope creep)
4. **User stories / requirements** — what the system should do, from the user's perspective
5. **Open questions** — things you don't yet know that could affect the solution
6. **Out of scope / future work** — related work intentionally deferred
7. **Dependencies** — other teams, systems, or features this depends on
8. **Timeline / phasing** — rough phases or milestones (not a Gantt chart)

> The most important PRD element that beginners skip: **Non-goals.** Stating what you won't solve is as important as stating what you will. It's the primary tool for scope management.

### User story format

**Template:** As a [persona], I want [action] so that [benefit].

**Acceptance criteria:** A list of specific, testable conditions that must be true for the story to be "done."

Example:
> **Story:** As a returning customer, I want to see my last 5 orders on the account page so that I can quickly reorder or check status.
>
> **Acceptance criteria:**
> - Last 5 orders shown in reverse chronological order
> - Each shows: order date, total, status, and a "Reorder" CTA
> - Status reflects real-time state (pending / shipped / delivered)
> - If fewer than 5 orders exist, show all of them
> - Works on mobile and desktop

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Write a full PRD | Notion | PRD for one feature of your running product — all 7 sections | **Free** |
| Pressure-test your PRD | With a friend or online PM community | Have someone ask "but what about X?" for 20 minutes; revise accordingly | **Free** |
| Write 10 user stories with acceptance criteria | Jira | Enter them in Jira and simulate sprint planning | **Free** |
| Read 3 real-world PRDs | Public PM blogs / GitHub | Find and analyze real PRDs — what does this company care about that yours doesn't cover? | **Free** |

**Practice gate:** you can write a PRD that a developer could begin scoping from — problem stated clearly, success metrics defined, non-goals listed, and acceptance criteria specific enough to be testable.

---

## Metrics, North Star, and OKRs (~20 hrs)

### North Star metric

A North Star metric is the single metric that best captures whether users are getting value from your product. Every team in the company should be able to see how their work connects to it.

Examples:
- Spotify: time spent listening
- Airbnb: nights booked
- Slack: daily active users who sent a message
- Duolingo: days of streak (debatable — a good PM question: is retention the right proxy for learning?)

The North Star is not the business metric (revenue, ARR). It's the leading indicator that *precedes* the business outcome.

### Supporting metrics tree

Every North Star breaks down into inputs:
```
North Star: Daily Active Users
  ├── Acquisition: new users per day
  ├── Activation: % of new users who complete onboarding
  ├── Retention: % of users active day 7, day 30
  └── Resurrection: % of churned users who return
```

Understanding this tree is what makes PM analytics work. When a metric drops, you navigate the tree to diagnose where.

### OKRs

**O**bjectives and **K**ey **R**esults

- **Objective:** qualitative direction. Ambitious, memorable, motivating. Not a number.
- **Key Results:** 2–4 specific, measurable outcomes that indicate you hit the objective.

Example:
> **Objective:** Make the mobile onboarding experience fast and delightful
>
> **KR1:** Mobile Day-1 activation rate increases from 42% to 60%
> **KR2:** Onboarding completion time decreases from 4:20 to under 2:30
> **KR3:** Onboarding NPS increases from 32 to 50

OKRs set at the team level should connect to company-level OKRs. A PM's job is to translate company objectives into product team outcomes.

### A/B testing literacy

You don't need to be a statistician. You need to know:
- What a control and variant are
- Why you need a sufficient sample size before reading results
- What p-value means (probability the result is due to chance) and what 95% significance means
- What novelty effect is and why it can mislead early results
- Why you should define success metrics *before* running the experiment

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Define a North Star for your product | Notion | Choose the metric, justify it, and build a 3-level input tree | **Free** |
| Write a set of OKRs | Notion | One objective with 3 key results for a hypothetical product team | **Free** |
| Amplitude funnel analysis | Amplitude free tier | Set up a funnel for your product or a demo dataset; identify the biggest drop-off | **Free** |
| Read "Metrics for PMs" (Lenny's) | lennysnewsletter.com | Current practitioner view on product metrics | **Free** tier |

**Practice gate:** you can define a North Star metric for a given product, explain why it's better than revenue as a daily signal, and sketch a 3-level input tree underneath it.

---

## Jobs-to-be-Done and Stakeholder Management (~20 hrs)

### Jobs-to-be-Done (JTBD)

JTBD is a framework for understanding why customers use a product, not just what they do with it. The core insight: people don't buy products — they "hire" products to do a job.

Clayton Christensen's original framing: a milkshake sold in the morning is being hired for a different job (a long commute, one-handed, not messy) than one sold in the afternoon (something fun for my kid). Same product, completely different jobs.

For PM: when you understand the job a user is hiring your product for, you can prioritize features that make the product *better at that job*, rather than features that look interesting in isolation.

**JTBD format:** When [situation], I want to [motivation / job], so I can [expected outcome].

This is more specific than a user story because it focuses on the *situation* that triggers the need, not just the action.

### Stakeholder management

This is the skill most PM frameworks don't teach explicitly. It's also the one that breaks most PMs.

**Who stakeholders are:**
- Engineering lead / tech lead
- Design lead
- Data / analytics
- Legal, compliance, security
- Sales, customer success
- Marketing
- Executives (your manager, their manager, sometimes CEO)
- External: customers, partners, regulators

**The core problem:** stakeholders have different goals, different incentives, and different information. Your job is to build enough shared context that everyone is pulling in the same direction — without having authority over any of them.

**What works:**
- Regular, brief written updates (a weekly PM update that goes to all stakeholders saves 3 alignment meetings)
- Involve stakeholders early in discovery, not just at spec review (so they don't feel ambushed)
- Surface tradeoffs explicitly: "We can ship X by Q2 or Y by Q2, not both — here's my recommendation"
- Know what each stakeholder cares about and connect your work to it

**What doesn't work:**
- Presenting a fully-formed solution and asking for "buy-in" (they'll add requirements or block it)
- Going around a stakeholder when they slow you down (it will come back)
- Promising timelines you don't control

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Write 5 JTBD statements | Notion | For your running product; for each, identify what the user is *actually* hiring it for | **Free** |
| Map your stakeholders | Notion | List 6 hypothetical stakeholders for your product team; for each: their goal, their concern, and how you'd keep them aligned | **Free** |
| Write a stakeholder update | Notion | One-page weekly PM update covering: what shipped, what's in progress, what's blocked, key decisions needed | **Free** |

**Practice gate:** you can write a JTBD statement for a real product feature and explain how understanding the "job" changes the prioritization decision.

---

## Phase 2 exit checklist

- [ ] I can explain the difference between discovery and delivery, and name 2 discovery techniques
- [ ] I can score features using RICE and explain each input's limitations
- [ ] I can write a complete PRD with problem statement, success metrics, non-goals, and acceptance criteria
- [ ] I have defined a North Star metric and input tree for my running product
- [ ] I can write a set of OKRs that are specific and measurable
- [ ] I can write a JTBD statement and explain how it differs from a user story
- [ ] I understand what makes stakeholder management hard and have a basic alignment strategy

Next: [Phase 3 — Specialization →](03-specialization.md)
