# interview prep: IT management & strategy (2026) meow

> IT management interviews are behavioral-heavy and scenario-driven.
> they probe judgment, communication, people leadership, and pressure handling, because thats the job.

[Previous: Goal 5](05-job-hunt.md) - [Hub](README.md)

---

- [ ] **understand what interviews test**
- [ ] **prepare STAR stories**
- [ ] **practice incident scenarios**
- [ ] **answer "why management?"**
- [ ] **refresh track-specific vocabulary**
- [ ] **prepare questions for them**

## what interviews test

u are not being tested on whether u can configure a server.
u are being tested on:

1. **Judgment under ambiguity** - can u decide with incomplete information?
2. **Communication** - can u explain technical reality to executives and business constraints to engineers?
3. **People leadership** - conflict, underperformance, motivation.
4. **Prioritization** - when everything is urgent, what comes first?
5. **Ownership** - do u take accountability for outcomes and failures?

big tell: do u talk only about **i fixed it**, or do u talk about **the team, the process, and what u enabled**?
first-time manager candidates who still describe themselves doing all technical work sound like they havent crossed the IC -> manager bridge yet.

## formats youll face

| Format | What it looks like | What they assess |
|---|---|---|
| **Behavioral** | "Tell me about a time..." | leadership, conflict, ownership |
| **Scenario / situational** | outage at 9 AM, teams blaming each other | incident handling, calm, process |
| **Prioritization case** | security patch, CEO laptop, project deadline | business-risk weighting |
| **Budget / business case** | justify tooling spend | financial literacy |
| **People management** | underperformer, burned-out team | coaching, standards, empathy |
| **Strategy / vision** | first 90 days, align IT to business | strategic thinking |

small companies lean scenario + behavioral.
enterprise/government adds governance, compliance, and project questions.

## STAR for management answers

STAR = **Situation -> Task -> Action -> Result**.
for management interviews, weight Action and Result.

in Action, include the people dimension:
who u talked to, how u communicated, how u brought the team along.
a technically correct decision delivered badly is still a management failure.

weak:
> "we had an outage so i fixed the server and it came back up."

strong:
> "SSO went down at 9 AM. as the lead, i owned response. i assigned one engineer to diagnose while i ran comms: all-staff status within 15 minutes and updates every 30. we restored in 2.5 hours. post-mortem found unmonitored cert expiry, so i added expiry alerting and a runbook. P1 cert incidents went to zero after that."

## behavioral question bank

prepare 6-8 distinct stories u can flex.

### leadership and people

- [ ] led a team through difficult change
- [ ] handled conflict between team members
- [ ] managed an underperformer
- [ ] developed someone on your team
- [ ] delivered hard feedback
- [ ] motivated a team through stress

### ownership and failure

- [ ] project failed or went badly
- [ ] decision turned out wrong
- [ ] took accountability for a team member's mistake

### stakeholders and communication

- [ ] said no to an executive or important stakeholder
- [ ] explained technical issue to non-technical audience
- [ ] influenced without authority

### prioritization and pressure

- [ ] everything was urgent, what came first
- [ ] managed a major incident
- [ ] cut scope or pushed back on deadline

### strategy and judgment

- [ ] improved a process
- [ ] made a data-driven decision
- [ ] owned vendor or tool decision

one incident story, one conflict story, one failure story, one stakeholder-pushback story, one process-improvement story, and one cross-functional influence story cover most prompts.

## scenario questions

when given an outage or blame scenario, dont jump to a fix.
show a visible process:

1. **Stabilize first** - restore service before root cause. assign incident commander, stop blame, focus on impact.
2. **Communicate** - update affected users fast, set cadence, keep leadership informed.
3. **Resolve, then learn** - after restoration, run blameless post-mortem.
4. **Prevent** - action items with owners/dates, monitoring/runbook checks.

this shows ITIL instinct plus people/comms, without reciting definitions.

### prioritization scenario

for "security patch vs CEO laptop vs project deadline," weigh **business risk and blast radius**, not who shouts loudest.

good structure:

- [ ] assess blast radius and reversibility first
- [ ] critical active-exploit patch likely wins because it affects everyone
- [ ] CEO laptop affects one person, delegate in parallel if possible
- [ ] project deadline: decide whether fixed or negotiable
- [ ] communicate tradeoff to everyone affected

decision content matters less than structured reasoning + communication.

## the "why management?" question

if moving from IC role, u will be asked why u want to manage.

bad answers:

- [ ] "its the next step"
- [ ] "more money"
- [ ] "im tired of coding"

strong framing:
u get more leverage and satisfaction from multiplying a team's output than from your own.
ground it in proof: mentoring, leading a project, improving a process.

interviewers know IC -> manager is where people fail.
they want evidence u understand that your output becomes the team's output.

## track-specific angles

| Target | Extra questions |
|---|---|
| **ITSM / Service Delivery** | incident/change/problem, SLA management, CAB, continual improvement |
| **Project/Program** | Agile vs waterfall vs PRINCE2, scope/risk, governance, earned value |
| **Governance/Strategy** | COBIT, audit readiness, IT spend alignment, board communication |
| **People/Eng Management** | hiring, performance, team topology, career development, retention |
| **IT Operations** | uptime, on-call, incident command, capacity planning, infra cost |

## questions to ask them

asking sharp questions signals seniority.

- [ ] "How is IT perceived here: cost center or strategic partner? what would change that?"
- [ ] "What does success look like at 90 days and one year?"
- [ ] "How does the team handle incidents and post-mortems today?"
- [ ] "Whats the biggest friction between IT and the business rn?"
- [ ] "How are IT priorities and budgets set, and who is at the table?"
- [ ] "Whats the tenure and morale of the team id inherit?"

## practice resources

| Resource | What u do | Cost | Status |
|---|---|---|---|
| [ADPList](https://adplist.org) | mock interviews / mentorship with IT and engineering managers | **Free** | live |
| [Atlassian Team Playbook](https://www.atlassian.com/team-playbook/plays) | exercises for management vocabulary | **Free** | live |
| [PagerDuty Incident Response](https://response.pagerduty.com) | incident-command language for scenarios | **Free** | live |
| [r/ITManagers](https://www.reddit.com/r/ITManagers/) | real debriefs and interview threads | **Free** | live |

## final prep checklist

- [ ] 6-8 STAR stories written with measurable result and lesson learned
- [ ] one incident/outage story in 90 seconds
- [ ] one failure story where u took accountability and changed something
- [ ] crisp 60-second "why management?" answer with real example
- [ ] 90-day plan artifact from [Goal 4](04-projects.md) ready
- [ ] 4-5 sharp questions to ask them
- [ ] track-specific vocabulary refreshed
- [ ] answers frame the team's outcomes, not individual heroics

---

*Last verified: June 2026. Practice-platform availability changes, so confirm before relying on a tool. Sources in [/research](../../research/).*
