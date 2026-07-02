# Goal 2: core IT management skills meow

> **~160h total** - your pace, no deadline.
> goal: learn to run services, deliver projects, manage money, hold vendors accountable, quantify risk, and keep stakeholders aligned.

[Previous: Goal 1](01-foundations.md) - [Hub](README.md) - [Next: Goal 3](03-specialization.md)

---

- [ ] **service management in practice** (~45h)
- [ ] **project and delivery basics** (~40h)
- [ ] **metrics, KPIs, and SLAs** (~30h)
- [ ] **IT budgeting and finance** (~25h)
- [ ] **vendor, risk, and stakeholder management** (~20h)
- [ ] **exit check** - incident priority, RACI, SLA math, budget case, vendor/risk/stakeholder artifacts

## service management in practice (~45h)

Goal 1 introduced ITIL 4.
now u operate the three most-used practices: **incident**, **problem**, and **change** management.

### incident management

an **incident** is an unplanned interruption or degradation of service.
goal: **restore service as fast as possible**, even with a workaround.
root cause comes later.

flow:

1. detect and log
2. categorize and prioritize
3. investigate and diagnose
4. resolve and recover
5. close and document

priority = impact x urgency.

| | Urgency High | Urgency Medium | Urgency Low |
|---|---|---|---|
| **Impact High** | P1 | P2 | P3 |
| **Impact Medium** | P2 | P3 | P4 |
| **Impact Low** | P3 | P4 | P4 |

a **P1 major incident** triggers a major-incident process: incident commander, comms lead, bridge call, stakeholder updates at fixed intervals.

### problem management

a **problem** is the underlying cause of incidents.
incident asks: how do we restore service now?
problem asks: how do we stop this recurring?
outputs: root-cause analysis, known-error records, permanent fixes.
the blameless post-mortem in [Goal 4](04-projects.md) is the signature artifact.

### change management

a **change** is an addition, modification, or removal that could affect services.
change management balances speed against risk.

- [ ] **Standard:** pre-approved, low-risk, routine.
- [ ] **Normal:** assessed and authorized, often by a Change Advisory Board (CAB).
- [ ] **Emergency:** expedited because waiting is riskier, then reviewed after.

CAB is where many IT managers first sit at a decision table.
check risk, rollback plan, change window, and communication.
approving a change with no rollback plan is the rookie mistake.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Incident workflow | ServiceNow Developer Instance | set up categories, assignment rules, SLA timers | **Free** |
| Priority matrix | Notion or Sheets | classify 10 sample incidents by impact x urgency | **Free** |
| Incident response guide | [PagerDuty Incident Response](https://response.pagerduty.com) | study incident command roles, comms, escalation | **Free** |
| Change process map | Miro free | diagram request -> CAB -> implementation -> review | **Free** |

**practice gate:** u can classify incident priority, explain incident vs problem, and describe when a change needs CAB vs standard pre-approval.

## project and delivery basics (~40h)

IT managers run projects or govern people who do.
u dont need a PM cert immediately, but u need delivery vocabulary.

### project lifecycle

1. **Initiation:** business case, sponsor, high-level scope.
2. **Planning:** scope, schedule, budget, resources, risks.
3. **Execution:** build and deliver.
4. **Monitoring and controlling:** track vs plan, manage changes.
5. **Closure:** handover, retrospective, benefits review.

### triple constraint

scope, time, and cost form the project triangle, with quality in the middle.
change one and another moves.
when a stakeholder asks for more scope with no schedule or budget change, make the tradeoff explicit.
dont silently absorb it.

### core artifacts

- [ ] **Project charter:** one-pager authorizing the project. u write one in Goal 4.
- [ ] **Work breakdown structure:** deliverables broken into tasks.
- [ ] **RACI matrix:** Responsible, Accountable, Consulted, Informed. exactly one Accountable per task.
- [ ] **Risk register:** formal risk list with owners and mitigations.
- [ ] **Status report:** progress, risks, decisions needed.

### waterfall vs Agile

- [ ] **Waterfall / stage-gate:** fixed, understood scope, approval gates.
- [ ] **Agile:** iterative delivery when requirements evolve.

most IT delivery is hybrid: agile execution inside governance that finance and steering committees understand.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Project charter | Asana template | draft charter for "migrate team to SSO" | **Free** |
| RACI matrix | Miro free | map 6-8 tasks x 5-6 roles, exactly one Accountable per task | **Free** |
| Status report | Google Docs | write 1-page status: % complete, risks, decisions needed, next milestone | **Free** |
| Google PM concepts | Coursera audit | audit planning, execution, Agile modules | **Free** audit |

**practice gate:** u can explain the triple constraint, build a correct RACI, and choose waterfall vs Agile for a given IT project.

## metrics, KPIs, and SLAs (~30h)

"u cant manage what u cant measure" is overused because its true for IT ops.

### SLA, OLA, underpinning contract

- [ ] **SLA:** customer commitment, like P1 response within 15 min and resolution within 4 hrs.
- [ ] **OLA:** internal team commitment that makes the SLA achievable.
- [ ] **Underpinning contract:** vendor commitment supporting your SLA.

rookie error: promising SLA without OLAs and vendor contracts behind it.
if hardware vendor allows 48-hour part replacement, a 4-hour resolution SLA is fiction.

### operational metrics

| Metric | Measures | Why it matters |
|---|---|---|
| **MTTR** | time to restore/resolve | headline incident metric |
| **MTBF** | uptime between failures | reliability |
| **MTTA** | alert to owner | on-call responsiveness |
| **SLA breach rate** | missed commitments | service-desk health |
| **First-contact resolution** | resolved without escalation | efficiency and skill |
| **Ticket volume by category** | where work comes from | what to automate or fix |
| **Uptime / availability** | service usable % | number executives quote |

### availability targets

99.9% allows about 8.7 hours downtime per year.
99.99% allows about 52 minutes.
more nines gets exponentially more expensive.
part of the IT manager job is explaining what the target costs and whether the business truly needs it.

### SLI, SLO, error budget

- [ ] **SLI:** actual measured value.
- [ ] **SLO:** internal target for that value.
- [ ] **Error budget:** allowed failure. if burned, stop risky changes and focus reliability.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| SLA dashboard mock | Sheets or Miro | define SLAs for P1-P4 and mock weekly dashboard | **Free** |
| Availability budgets | Paper or Sheets | compute downtime for 99%, 99.9%, 99.99% | **Free** |
| SRE workbook intro | [Google SRE books](https://sre.google/books/) | read SLI/SLO/error budget chapters - ⚠️ TODO verify exact chapter links | **Free** |

**practice gate:** u can define SLA/OLA/SLI/SLO, calculate annual downtime for nines targets, and explain why SLAs need OLAs and vendor contracts.

## IT budgeting and finance (~25h)

financial fluency is the gap that stalls technical managers.
u can run a flawless service desk, but if u cant defend spend to finance, u plateau.

### CapEx vs OpEx

- [ ] **CapEx:** large upfront assets used over years, like servers or perpetual licenses. depreciated over time.
- [ ] **OpEx:** ongoing running costs, like SaaS subscriptions, cloud, support contracts, salaries.

cloud shifts CapEx to OpEx: renting compute instead of buying servers.
finance cares because it changes taxes and cash flow.

### TCO and ROI

- [ ] **TCO:** total lifetime cost, not sticker price: license + implementation + training + support + maintenance + decommissioning.
- [ ] **ROI:** `(gain - cost) / cost`. in IT, gain is often avoided cost: staff hours saved, downtime prevented.

### chargeback and showback

- [ ] **Showback:** show departments what IT consumption would cost.
- [ ] **Chargeback:** actually bill departments for their IT usage.

### budget cycle

annual budget cycle: forecast next year's IT spend, defend it, track actuals vs forecast monthly, explain variance.
"we are 8% over cloud spend because of unplanned data-migration egress costs" is a normal sentence here.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| TCO comparison | Google Sheets | compare 3-year TCO of two ITSM tools | **Free** |
| CapEx vs OpEx sort | Paper or Sheets | classify 15 IT expenses and justify each | **Free** |
| IT investment memo | Google Docs | 1-page business case for tool purchase with cost-avoidance ROI | **Free** |

**practice gate:** u can classify CapEx vs OpEx, calculate simple cost-avoidance ROI, and explain why cheapest sticker price may not be lowest TCO.

## vendor, risk, and stakeholder management (~20h)

these judgment skills define whether u get trusted with bigger scope.

### vendor and contract management

- [ ] **Selection:** RFP/RFI, weighted criteria, not vibes.
- [ ] **Negotiation:** SLAs, pricing tiers, exit clauses, data ownership.
- [ ] **Governance:** QBRs, SLA tracking, renewal management.
- [ ] **Third-party risk:** vendor security posture becomes your risk.

### risk management

risk management asks what could go wrong, how likely, how bad, and what ull do.

the core tool is the **risk register** in Goal 4.
each risk gets:

- [ ] specific description
- [ ] likelihood x impact score
- [ ] mitigation and owner
- [ ] residual risk after mitigation

four risk responses:

- [ ] **avoid:** dont do the risky thing
- [ ] **mitigate:** reduce likelihood or impact
- [ ] **transfer:** insurance or vendor contract
- [ ] **accept:** cheap enough to live with

### stakeholder management

classic tool: power/interest grid.

| | Low Interest | High Interest |
|---|---|---|
| **High Power** | keep satisfied | manage closely |
| **Low Power** | monitor | keep informed |

map stakeholders and set communication cadence.
CFO gets concise monthly summary.
engineering lead may need continuous contact.
getting this wrong is avoidable pain.

managing up = no surprises.
flag risks early and at the right altitude.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Vendor matrix | Sheets or Notion | score 3 vendors across 8 weighted criteria | **Free** |
| Risk register | Asana template or Sheets | 10+ cloud-migration risks, likelihood x impact, mitigations, owners | **Free** |
| Stakeholder map | Miro free | plot 8 stakeholders on power/interest grid with comms cadence | **Free** |

**practice gate:** u can run weighted vendor evaluation, build a risk register, name the four risk responses, and map stakeholders with appropriate communication cadence.

## exit check

- [ ] classify incident priority and distinguish incident / problem / change
- [ ] explain triple constraint and build a correct RACI matrix
- [ ] define SLA/OLA/SLI/SLO and calculate availability budgets
- [ ] classify CapEx vs OpEx and build a simple TCO/ROI case
- [ ] run a vendor evaluation, build a risk register, and map stakeholders

[Next: Goal 3 - Pick a Track](03-specialization.md)
