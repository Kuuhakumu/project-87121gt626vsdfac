# 🎤 Interview Prep — IT Management & Strategy (2026)

> IT management interviews are **behavioral-heavy and scenario-driven**, not technical trivia. They probe judgment, communication, and how you handle people and pressure — because that's the actual job. This file gives you the formats, a question bank, and a way to structure answers.

[← Job Hunt](05-job-hunt.md) · [Hub](README.md)

---

## What IT management interviews actually test

You're not being tested on whether you can configure a server. You're being tested on:

1. **Judgment under ambiguity** — can you make a defensible decision with incomplete information?
2. **Communication** — can you explain a technical situation to a non-technical executive, and a business constraint to an engineer?
3. **People leadership** — how do you handle conflict, underperformance, and motivation?
4. **Prioritization** — when everything is on fire, what do you do first, and why?
5. **Ownership** — do you take accountability for outcomes, including failures?

> The single biggest tell interviewers listen for: do you talk about **"I"** (individual contributor mindset) or **"we / the team / I enabled them to…"** (manager mindset)? First-time-manager candidates who still describe themselves doing all the technical work signal they haven't made the transition. Frame your answers around enabling outcomes, not doing the tasks.

---

## The interview formats you'll face

| Format | What it looks like | What they're assessing |
|---|---|---|
| **Behavioral** | "Tell me about a time you…" | Past behavior as predictor; leadership, conflict, ownership |
| **Scenario / situational** | "An outage hits at 9 AM and three teams are blaming each other. What do you do?" | Incident handling, calm under pressure, process instinct |
| **Prioritization case** | "You have a security patch, a CEO laptop issue, and a project deadline — all urgent. Walk me through it." | Tradeoff reasoning, business-risk weighting |
| **Budget / business case** | "Walk us through a business case you've built" or "How would you justify a tooling spend?" | Financial literacy, executive communication |
| **People-management** | "How do you handle an underperformer?" / "How do you motivate a burned-out team?" | Coaching, accountability, empathy + standards |
| **Strategy / vision** | "What would your first 90 days look like?" / "How do you align IT with business goals?" | Strategic thinking, governance awareness |

Most loops mix several of these. Smaller companies lean toward scenario + behavioral; enterprise/government adds governance, compliance, and PMP-style project questions.

---

## STAR: the structure for every behavioral answer

**S**ituation → **T**ask → **A**ction → **R**esult. For management interviews, weight **Action** (what *you* decided and why) and **Result** (measurable outcome + what you learned).

> The management upgrade to STAR: in the Action step, always include the *people* dimension — who you talked to, how you communicated the decision, how you brought the team along. A technically correct decision delivered badly is a management failure.

**Weak:** "We had an outage so I fixed the server and it came back up."
**Strong:** "SSO went down at 9 AM (S). As the lead, I owned the response (T). I assigned one engineer to diagnose while I ran comms — a status note to all staff within 15 minutes and updates every 30 (A). We restored in 2.5 hours, and in the post-mortem we found the root cause was an unmonitored cert expiry, so I added expiry alerting and a runbook. P1 cert incidents went to zero after that (R)."

---

## Behavioral question bank (prep a STAR story for each)

**Leadership & people**
- Tell me about a time you led a team through a difficult change.
- Describe a conflict between two team members. How did you handle it?
- Tell me about a time you had to manage an underperformer.
- How have you developed someone on your team?
- Tell me about a time you had to deliver hard feedback.
- Describe a time you motivated a team through a stressful period.

**Ownership & failure**
- Tell me about a project that failed or went badly. What did you do?
- Describe a decision you made that turned out to be wrong.
- Tell me about a time you took accountability for a team member's mistake.

**Stakeholders & communication**
- Tell me about a time you had to say no to an executive or important stakeholder.
- Describe explaining a complex technical issue to a non-technical audience.
- Tell me about a time you had to influence without authority.

**Prioritization & pressure**
- Tell me about a time everything was urgent. How did you decide what to do first?
- Describe a major incident you managed.
- Tell me about a time you had to cut scope or push back on a deadline.

**Strategy & judgment**
- Tell me about a process you improved.
- Describe a time you made a data-driven decision.
- Tell me about a vendor or tool decision you owned.

> Prepare **6–8 distinct stories** that you can flex across these questions. One strong incident story, one conflict story, one failure story, one stakeholder-pushback story, one process-improvement story, and one cross-functional-influence story will cover the majority of behavioral prompts.

---

## Scenario questions — how to structure the answer

When given a scenario ("an outage hits, teams are blaming each other"), don't jump to a fix. Follow a visible process:

1. **Stabilize first** — "My first priority is service restoration, not root cause. I'd establish an incident commander (me, if no one's assigned), get one person diagnosing, and stop the cross-team blame by focusing everyone on impact."
2. **Communicate** — "I'd send a status update to affected users within minutes, set an update cadence, and keep leadership informed so they're not surprised."
3. **Resolve, then learn** — "Once restored, I'd run a blameless post-mortem — the blaming you described is exactly the culture problem a good post-mortem process fixes."
4. **Prevent** — "Action items with owners and due dates, and a check on whether monitoring should have caught this earlier."

This shows you know ITIL incident-management instinct *and* the people/comms dimension without reciting definitions.

### The prioritization scenario

For "security patch vs. CEO laptop vs. project deadline," show you weigh by **business risk and blast radius**, not by who's shouting loudest:

- "I'd assess blast radius and reversibility first. A critical security patch with an active exploit affects everyone and is hard to undo if breached — that usually wins. The CEO's laptop affects one person; I'd delegate it to a team member in parallel rather than drop everything myself. The project deadline I'd assess: is it truly fixed, or can I negotiate a short slip with the stakeholder? I'd communicate the tradeoff to everyone affected rather than silently deprioritize."

The content of the decision matters less than showing structured reasoning + communication.

---

## The "why management?" question (critical for first-timers)

If you're moving from an IC role (sysadmin, engineer, support lead), you *will* get asked why you want to manage. Bad answers: "it's the next step," "more money," "I'm tired of coding." These signal you're escaping, not choosing.

**Strong framing:** you get more leverage and satisfaction from multiplying a team's output than from your own — and you have evidence (you mentored, you led a project, you improved a process). Make it about impact through others, grounded in a concrete example of you already doing management-shaped work.

> Interviewers know the IC→manager transition is where people fail. They want to see you understand the job changes fundamentally — your output becomes your team's output — and that you're running *toward* that, with proof you've started already.

---

## Track-specific angles

| If you're targeting… | Expect extra questions on… |
|---|---|
| **ITSM / Service Delivery** | ITIL processes (incident/change/problem), SLA management, CAB, continual improvement |
| **Project/Program Mgmt** | Methodology choice (Agile vs. waterfall vs. PRINCE2), scope/risk management, stakeholder governance, earned value |
| **Governance/Strategy** | COBIT/risk frameworks, audit readiness, aligning IT spend to business strategy, board communication |
| **People/Eng Management** | Hiring, performance management, team topology, career development, retention |
| **IT Operations** | Uptime/reliability, on-call and incident command, capacity planning, infra cost management |

---

## Questions to ask them (you're interviewing them too)

Asking sharp questions signals seniority. Pick a few:

- "How is IT perceived here — as a cost center or a strategic partner? What would change that?"
- "What does success in this role look like at 90 days? At one year?"
- "How does the team currently handle incidents and post-mortems?"
- "What's the biggest source of friction between IT and the rest of the business right now?"
- "How are IT priorities and budgets set — and who's at the table when they are?"
- "What's the tenure and morale of the team I'd be inheriting?"

---

## Practice resources

| Resource | What you do | Cost | Status |
|---|---|---|---|
| [ADPList](https://adplist.org) | Free 1:1 mock interviews / mentorship with IT & eng managers | **Free** | ✅ |
| [Atlassian Team Playbook](https://www.atlassian.com/team-playbook/plays) | Run the exercises to build real management vocabulary | **Free** | ✅ |
| [PagerDuty Incident Response](https://response.pagerduty.com) | Internalize incident-command language for scenario questions | **Free** | ✅ |
| [r/ITManagers](https://www.reddit.com/r/ITManagers/) | Real interview debriefs and "what they asked me" threads | **Free** | ✅ |

---

## Final prep checklist

- [ ] 6–8 STAR stories written out, each with a measurable result and a lesson learned
- [ ] One strong **incident / outage** story you can tell in 90 seconds
- [ ] One **failure** story where you took accountability and changed something
- [ ] A crisp 60-second answer to **"why management?"** backed by a real example
- [ ] Your **90-day plan** artifact (from [04-projects.md](04-projects.md)) ready to reference
- [ ] 4–5 sharp questions to ask them
- [ ] Track-specific framework vocabulary refreshed (ITIL / PMBOK / COBIT as relevant)
- [ ] You consistently frame answers around **the team's outcomes**, not your individual heroics

---

*Last verified: June 2026. Practice-platform availability changes — confirm before relying on a tool. Sources in [/research](../../research/).*
