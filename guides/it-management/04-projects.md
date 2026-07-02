# Goal 4: the IT management portfolio meow

> **~70h total** - your pace, no deadline.
> goal: build thinking artifacts that show u can manage services, risk, vendors, budgets, and people.
> no code, no visual design. what u write reveals whether u can manage.

[Previous: Goal 3](03-specialization.md) - [Hub](README.md) - [Next: Goal 5](05-job-hunt.md)

---

- [ ] **understand what the portfolio proves**
- [ ] **build the 8 artifacts**
- [ ] **package them in Notion or Confluence**
- [ ] **exit check** - 4+ artifacts published, including post-mortem and business case

## what an IT management portfolio is

IT management portfolios are not coding portfolios.
u produce artifacts that demonstrate:

1. **u can assess operational reality** - not just recite ITIL definitions.
2. **u can manage risk and explain it to non-technical stakeholders**.
3. **u can run process** - incidents, sprints, vendors, budgets.
4. **u can set direction and measure it** - OKRs, 30/60/90 plans, roadmaps.
5. **u understand accountability** - problem -> decision -> owner -> outcome.

hiring bar: would i trust this person to own IT operations?
that means judgment about priorities, risk, and communication.
anyone can define an SLA.
fewer can write a service catalog where the SLA is achievable and costs are visible.

host everything in a **Notion or Confluence "IT Manager Portfolio" site**.
export 2-3 strongest pieces as PDFs for applications or interviews.

## what strong pieces look like

| Weak | Strong |
|---|---|
| copied ITIL template | filled-in artifact for a specific fictional company |
| "Risks: TBD" | 10 risks rated likelihood x impact with owners |
| incident timeline with no cause | blameless post-mortem with contributing factors and action items |
| unmeasurable OKRs | each KR has baseline, metric, and measurement method |
| business case with no numbers | TCO, cost/benefit, recommendation, payback rationale |

## artifact 1: mock IT service catalog

**scenario:** 200-person company is scaling fast.
IT is reactive.
employees dont know what to request, how long it takes, or who owns what.

**produce:** Notion, Confluence, or Google Sheet covering 8-10 IT services.

for each service:

- [ ] service name and plain-language description
- [ ] service owner by role
- [ ] who can request it
- [ ] how to request it
- [ ] SLA: response time + resolution target
- [ ] fully loaded cost estimate
- [ ] linked runbook or how-to stub

example services: laptop provisioning, new-hire onboarding, software access, password reset, VPN, printer support, security incident reporting, offboarding, application support triage, mobile device enrollment.

**demonstrates:** service ownership, SLA setting, cost visibility.

## artifact 2: blameless incident post-mortem

**scenario:** Tuesday 9:14 AM, employees across three offices lose SSO.
no email, Slack, or ERP login.
resolved at 11:47 AM.
u are incident commander.

**produce:** Google Doc or Notion page using PagerDuty post-mortem structure:

- [ ] incident summary: severity, duration, impact, affected services
- [ ] timeline: minute-by-minute from alert to resolution
- [ ] contributing factors: monitoring gap, on-call gap, outdated runbook
- [ ] what went well
- [ ] action items: at least 5, each with owner role and due date
- [ ] lessons learned in blameless language

length: 600-900 words.
tone: factual and forward-looking.

**demonstrates:** incident process, calm communication, systemic improvement without blame.

## artifact 3: project charter + RACI

**scenario:** migrate 120 employees from individual app logins to centralized SSO over 12 weeks.
u are project lead.

**produce:** 1-2 page charter plus RACI.

include:

- [ ] project title and sponsor
- [ ] business objective
- [ ] scope: whats in and out
- [ ] success criteria, like Tier-1 apps integrated and password-reset tickets reduced
- [ ] 4-6 milestones
- [ ] top 3 risks
- [ ] RACI with 6-8 tasks x 5-6 roles, exactly one Accountable per task

**demonstrates:** delivery structure and accountability.

## artifact 4: Agile IT sprint simulation

**scenario:** IT team uses two-week sprints for operations plus project work.

**produce:**

- [ ] Jira backlog with 15-20 tickets across infra, security, vendor, service request, project work
- [ ] sprint plan with 8-10 tickets, points, roles, acceptance criteria
- [ ] board states: To Do -> In Progress -> In Review -> Done
- [ ] simulate 2-3 blockers
- [ ] retrospective doc: went well, needs improvement, action item
- [ ] velocity note: planned vs completed points

**demonstrates:** agile operations, capacity planning, retrospectives.

## artifact 5: 90-day IT ops improvement plan

**scenario:** u are hired as IT Manager at a 300-person company.
documentation is thin, helpdesk is reactive, no service catalog, security enforcement inconsistent, morale low.

**produce:** Notion page or 3-5 slide deck.

**Days 1-30: listen and assess**

- [ ] shadow each IT team member
- [ ] audit ticket backlog
- [ ] identify top recurring ticket types
- [ ] meet department heads
- [ ] deliver 1-page current-state assessment

**Days 31-60: quick wins and process fixes**

- [ ] publish first-draft service catalog
- [ ] reduce P1 MTTR through on-call and clearer escalation
- [ ] standardize onboarding/offboarding checklist
- [ ] track ticket category, MTTR, SLA breach, utilization

**Days 61-90: strategic foundation**

- [ ] present 12-month IT roadmap
- [ ] launch quarterly team health check
- [ ] propose budget for one deferred security initiative
- [ ] track satisfaction, policy compliance, backlog trend

**demonstrates:** strategic thinking, operational awareness, prioritization under uncertainty.

## artifact 6: risk register

**scenario:** migrate 8 TB of file storage from on-prem NAS to cloud storage for 280 users.

**produce:** Google Sheet or Asana item with 10-12 risks.

each risk needs:

- [ ] risk ID
- [ ] specific description
- [ ] category: data, security, vendor, people, timeline
- [ ] likelihood 1-5
- [ ] impact 1-5
- [ ] risk score = likelihood x impact
- [ ] mitigation
- [ ] owner role
- [ ] status
- [ ] residual risk score

include risks like data corruption, shadow IT, vendor SLA failure, egress cost overrun, data residency gap, downtime during cutover.

**demonstrates:** quantified risk and defensible prioritization.

## artifact 7: OKR set for IT department

**scenario:** Q4 planning for Q1.
company theme: operational resilience and security posture.

**produce:** Notion page with objectives and KRs.
for each KR include baseline, target, measurement method, cadence.

example:

**Objective 1: Improve IT service reliability**

- [ ] KR 1: reduce P1/P2 MTTR from 4.2 hours to under 2.5 hours
- [ ] KR 2: achieve 99.5% uptime on Tier-1 systems
- [ ] KR 3: publish runbooks for top 5 recurring incident types by Week 6

**Objective 2: Strengthen security baseline**

- [ ] KR 1: reach 100% MFA enrollment from current 74%
- [ ] KR 2: remediate all critical/high Q4 scan findings by Week 8
- [ ] KR 3: deliver security awareness training to 90% of staff

**Objective 3: Increase capacity through process efficiency**

- [ ] KR 1: reduce Tier-1 request resolution time by 40% via self-service
- [ ] KR 2: onboard 2 IT team members to full productivity by Week 6
- [ ] KR 3: automate weekly vulnerability scan reporting

reference: [OKR framework repo](https://github.com/joelparkerhenderson/objectives-and-key-results).

**demonstrates:** translating reactive IT work into measurable outcomes.

## artifact 8: business case / IT investment memo

**scenario:** legacy helpdesk system is 5 years old, no integrations, poor mobile support, no SLA tracking.
CFO wants a 2-page business case before budget approval.

**produce:** Google Doc executive memo.

include:

- [ ] problem statement with evidence: manual hours lost, SLA compliance unmeasurable, HRIS integration missing
- [ ] business impact: slower incident response, labor cost, audit risk
- [ ] options analysis table
- [ ] recommendation with 3-year TCO and payback
- [ ] 8-week migration plan with phased rollout and hypercare

example options:

| Option | Description | Year-1 Cost | Pros | Cons |
|---|---|---|---|---|
| Status quo | keep current system | ~$8K | no disruption | problem persists |
| Option A | mid-market ITSM | ~$18K | modern UX, integrations, SLA tracking | migration effort |
| Option B | enterprise ITSM | ~$65K+ | full ITIL suite | overkill and admin burden |
| Option C | Jira Service Management | ~$12K | existing Jira familiarity | limited native ITSM features |

**demonstrates:** selling an investment to finance with numbers and a recommendation.

## packaging

**Notion/Confluence portfolio site:**
create an index page titled `IT Management Portfolio - [Your Name]`.
add 2-3 sentence intro.
group artifacts:

- [ ] Operations & Incidents
- [ ] Planning & Strategy
- [ ] Projects & Investment

**PDF one-pagers to export:**

- [ ] Project Charter + RACI
- [ ] Business Case memo
- [ ] 90-Day IT Ops Plan

**optional extras:**

- [ ] Vendor Evaluation Matrix
- [ ] Change Management Communication Plan
- [ ] 12-month IT Roadmap

publish the workspace as one public URL and add it to your resume under Portfolio.
in interviews, open the index before the call starts.

## exit check

- [ ] at least 4 artifacts published to one portfolio site
- [ ] one artifact is an incident post-mortem
- [ ] one artifact is a business case
- [ ] each artifact uses a specific fictional scenario, not generic placeholders
- [ ] artifacts have named owners where appropriate
- [ ] each artifact includes at least one measurable outcome or KPI
- [ ] portfolio is accessible via one public URL

[Next: Goal 5 - Job Hunt](05-job-hunt.md)
