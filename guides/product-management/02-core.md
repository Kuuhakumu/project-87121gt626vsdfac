# Goal 2: core PM skills - discovery, priority, PRDs, metrics meow

> **~160h total** - your pace, no deadline.
> goal: practice the skills PM interviews and real PM work both test: discovery, tradeoffs, writing, metrics, and stakeholders.

[Previous: Goal 1](01-foundations.md) - [Hub](README.md) - [Next: Goal 3](03-specialization.md)

---

- [ ] **product discovery vs delivery** (~40h)
- [ ] **prioritization frameworks** (~50h)
- [ ] **PRDs and user stories** (~30h)
- [ ] **metrics, North Star, OKRs** (~20h)
- [ ] **JTBD and stakeholder management** (~20h)
- [ ] **exit check** - discovery plan, RICE, PRD, metrics tree, JTBD, stakeholder update

## product discovery vs delivery (~40h)

this is the most important conceptual distinction in modern PM practice.
get it wrong and ull build the wrong things really well.

### what discovery is

**Discovery** is the work before building to determine:

- [ ] is this a real problem worth solving?
- [ ] do users experience it the way we think?
- [ ] is our proposed solution something theyd use?
- [ ] is it technically feasible without a huge lift?
- [ ] does it make business sense?

discovery outputs: interview findings, opportunity assessments, problem statements, solution prototypes tested with users.

**Delivery** is building and shipping a solution that has been validated.
delivery output: shipped features, deployed code, release notes.

common failure mode: treating every idea as ready for delivery, then discovering problems after it ships.
Marty Cagan calls this the build trap, and Melissa Perri's book uses the same idea.

### continuous discovery

Teresa Torres argues discovery should be a weekly habit, not a one-time stage.
the core practice: talk to at least one customer per week and connect what u learn to an opportunity solution tree.
it doesnt require a formal research budget.
it requires discipline and a habit of keeping 3-5 reachable users.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Map a discovery opportunity tree | Notion or paper | take your running product, identify the outcome, and map assumptions underneath it | **Free** |
| Write a user interview guide | Notion | write 5-7 questions that explore a problem space, not validate your solution | **Free** |
| Conduct 3 user interviews | video call or in person | talk to real users of your chosen product and synthesize what u heard | **Free** |
| Read "Dual-Track Agile" | SVPG article | understand discovery and delivery in parallel - ⚠️ TODO verify exact SVPG article link | **Free** |

**practice gate:** u can explain discovery vs delivery, name outputs for each, and identify one real product failure caused by skipping discovery.

## prioritization frameworks (~50h)

prioritization shows whether u can make real tradeoffs.
know the frameworks, but more importantly, explain why u chose one for a context.

### RICE

**R**each, **I**mpact, **C**onfidence, **E**ffort

```text
Score = (Reach x Impact x Confidence) / Effort
```

- [ ] **Reach:** users affected per time period, as a number.
- [ ] **Impact:** estimated impact per user. common scale: 0.5, 1, 2, 3.
- [ ] **Confidence:** how confident u are in the estimates: 100%, 80%, 50%.
- [ ] **Effort:** person-months across all functions.

use RICE when features have different audience sizes and effort levels.
weakness: estimated inputs can create false precision.

### MoSCoW

**M**ust have, **S**hould have, **C**ould have, **W**ont have this time.

best for release planning against a deadline.
weakness: everyone tries to mark their feature "Must" unless u are disciplined.

### Kano

classifies features by user satisfaction:

- [ ] **Basic / threshold:** users are angry if absent, indifferent if present.
- [ ] **Performance:** more equals more satisfaction.
- [ ] **Delighters:** unexpected features that disproportionately increase satisfaction.

use Kano to understand the kind of feature, not just rank a backlog.

### ICE

**I**mpact, **C**onfidence, **E**ase

```text
Score = (Impact x Confidence x Ease) / 3
```

simpler than RICE, with no Reach factor.
common in growth and experimentation.
weakness: subjective and missing volume signal.

### when to use which

| Framework | Best for |
|---|---|
| **RICE** | comparing features with different audience sizes and effort |
| **MoSCoW** | release scope against a fixed deadline |
| **Kano** | understanding hygiene vs growth vs delight |
| **ICE** | fast growth-experiment triage |

frameworks structure the conversation.
your research, stakeholder context, and judgment are still the answer.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| RICE score 5 features | Google Sheets | score 5 features for your running product and defend the estimates | **Free** |
| MoSCoW a release | Notion | sort a 12-item backlog into must/should/could/wont for a fixed 2-week sprint | **Free** |
| Kano analysis | Notion or paper | classify 10 features into Basic / Performance / Delighter and explain why | **Free** |
| Read "How to Prioritize" | Lenny's Newsletter | practitioner breakdown of PM prioritization - ⚠️ TODO verify exact article link | **Free** tier |

**practice gate:** u can score features with RICE, explain each input, and name one case where RICE might mislead u.

## writing PRDs and user stories (~30h)

Goal 1 introduced writing.
Goal 2 is where u get reps.

### PRD structure

there is no single canonical PRD format.
companies use different templates.
the consistent elements:

1. **Problem statement** - what problem exists, for whom, and why now.
2. **Goals and success metrics** - what numbers change if this works?
3. **Non-goals** - what u are explicitly not solving.
4. **User stories / requirements** - what the system should do from the user's perspective.
5. **Open questions** - things u dont know yet.
6. **Out of scope / future work** - related work intentionally deferred.
7. **Dependencies** - other teams, systems, or features needed.
8. **Timeline / milestones** - rough sequencing, not a fantasy Gantt chart.

beginners skip **non-goals**.
dont.
stating what u wont solve is the main tool for scope control.

### user story format

```text
As a [persona], I want [action] so that [benefit].
```

acceptance criteria are specific, testable conditions that must be true for the story to be done.

example:

> **Story:** As a returning customer, I want to see my last 5 orders on the account page so that I can quickly reorder or check status.
>
> **Acceptance criteria:**
> - last 5 orders shown in reverse chronological order
> - each shows order date, total, status, and "Reorder" CTA
> - status reflects real-time state
> - if fewer than 5 orders exist, show all of them
> - works on mobile and desktop

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Full PRD | Notion | write all core PRD sections for one feature of your running product | **Free** |
| Pressure-test PRD | friend or PM community | have someone ask "but what about X?" for 20 minutes, then revise | **Free** |
| 10 user stories | Jira | enter 10 stories with acceptance criteria and simulate sprint planning | **Free** |
| Read 3 real-world PRDs | public PM blogs / GitHub | find real PRDs and compare structure - ⚠️ TODO verify exact examples | **Free** |

**practice gate:** u can write a PRD a developer could begin scoping from: clear problem, success metrics, non-goals, and testable acceptance criteria.

## metrics, North Star, and OKRs (~20h)

### North Star metric

a North Star metric is the single metric that best captures whether users are getting value.
it should connect team work to product value.

examples:

- [ ] Spotify: time spent listening
- [ ] Airbnb: nights booked
- [ ] Slack: daily active users who sent a message
- [ ] Duolingo: days of streak, with the PM caveat that retention may not equal learning

the North Star is not the business metric like revenue or ARR.
its the leading indicator that precedes business outcome.

### supporting metrics tree

```text
North Star: Daily Active Users
  Acquisition: new users per day
  Activation: % of new users who complete onboarding
  Retention: % active day 7 and day 30
  Resurrection: % of churned users who return
```

when a metric drops, u navigate the tree to diagnose where.

### OKRs

**O**bjectives and **K**ey **R**esults

- [ ] **Objective:** qualitative direction. memorable, ambitious, not a number.
- [ ] **Key Results:** 2-4 measurable outcomes proving progress.

example:

> **Objective:** Make mobile onboarding fast and delightful
>
> **KR1:** Mobile Day-1 activation rate increases from 42% to 60%
> **KR2:** Onboarding completion time decreases from 4:20 to under 2:30
> **KR3:** Onboarding NPS increases from 32 to 50

### A/B testing literacy

u dont need to be a statistician.
u do need to know:

- [ ] control vs variant
- [ ] why sample size matters
- [ ] what p-value and 95% significance mean at a basic level
- [ ] novelty effect
- [ ] why success metrics must be defined before the experiment

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Define a North Star | Notion | choose the metric, justify it, and build a 3-level input tree | **Free** |
| Write OKRs | Notion | one objective with 3 key results for a product team | **Free** |
| Amplitude funnel analysis | Amplitude free tier | set up a funnel for your product or demo dataset and identify drop-off | **Free** |
| Read "Metrics for PMs" | Lenny's Newsletter | practitioner view on product metrics - ⚠️ TODO verify exact article link | **Free** tier |

**practice gate:** u can define a North Star metric, explain why its better than revenue as a daily signal, and sketch a 3-level input tree.

## JTBD and stakeholder management (~20h)

### Jobs-to-be-Done

JTBD explains why customers use a product, not just what they click.
people "hire" products to do a job.

Clayton Christensen's milkshake example: morning milkshake = long commute, one-handed, not messy.
afternoon milkshake = treat for a kid.
same product, different jobs.

PM takeaway: when u understand the job, u can prioritize features that make the product better at that job.

```text
When [situation], I want to [motivation / job], so I can [expected outcome].
```

JTBD is more specific than a user story bc it includes the situation that triggers the need.

### stakeholder management

stakeholders include:

- [ ] engineering lead / tech lead
- [ ] design lead
- [ ] data / analytics
- [ ] legal, compliance, security
- [ ] sales, customer success
- [ ] marketing
- [ ] executives
- [ ] customers, partners, regulators

the hard part: they have different goals, incentives, and information.
your job is to build enough shared context that everyone can move in the same direction, without authority over them.

what works:

- [ ] brief written updates every week
- [ ] involve stakeholders early in discovery, not just at spec review
- [ ] surface tradeoffs explicitly
- [ ] know what each stakeholder cares about and connect your work to it

what doesnt work:

- [ ] presenting a finished solution and asking for "buy-in"
- [ ] going around stakeholders when they slow u down
- [ ] promising timelines u dont control

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| 5 JTBD statements | Notion | for your running product, identify what users are hiring it for | **Free** |
| Stakeholder map | Notion | list 6 stakeholders, their goals, concerns, and alignment plan | **Free** |
| Stakeholder update | Notion | one-page weekly PM update: shipped, in progress, blocked, decisions needed | **Free** |

**practice gate:** u can write a JTBD statement for a real product feature and explain how the job changes the prioritization decision.

## exit check

- [ ] i can explain discovery vs delivery and name 2 discovery techniques
- [ ] i can score features using RICE and explain each input's limitation
- [ ] i can write a complete PRD with problem statement, success metrics, non-goals, and acceptance criteria
- [ ] i defined a North Star metric and input tree for my running product
- [ ] i can write specific, measurable OKRs
- [ ] i can write a JTBD statement and explain how it differs from a user story
- [ ] i understand stakeholder management and have a basic alignment strategy

[Next: Goal 3 - Specialization](03-specialization.md)
