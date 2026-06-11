# ⚙️ Phase 2: Core IT Management Skills

> **~160 hrs total** · your pace, no deadline
> Service management, project delivery, metrics and SLAs, budgeting, vendor management, risk, and stakeholder management — the operational toolkit every IT manager uses weekly.

[← Phase 1](01-foundations.md) · [Hub](README.md) · [Next: Phase 3 — Specialization →](03-specialization.md)

---

This is the longest phase, deliberately. Phase 1 gave you the vocabulary and the map. Phase 2 is where you learn to actually *run* things: keep services healthy, deliver projects, manage money, hold vendors accountable, quantify risk, and keep stakeholders aligned. These are the skills that show up in every IT management job description and every interview scenario.

Work through the blocks in order — each builds on the last. Do the labs. Reading about incident management without ever running a mock incident is the fastest way to interview poorly.

---

## Service Management in Practice (~45 hrs)

In Phase 1 you learned what ITIL 4 is. Here you learn to operate its three most-used practices: **incident**, **problem**, and **change** management. These three make up the bulk of an IT manager's day-to-day process work.

### Incident management

An **incident** is an unplanned interruption or degradation of a service. Incident management has one goal: **restore service as fast as possible**, even with a workaround. Root cause comes later (that's problem management).

The flow:
1. **Detect & log** — monitoring alert or user report; create a ticket
2. **Categorize & prioritize** — by impact (how many users) × urgency (how time-sensitive)
3. **Investigate & diagnose** — what's broken?
4. **Resolve & recover** — restore service, even via workaround
5. **Close** — confirm with the user, document

**Priority** is impact × urgency. A standard matrix:

| | Urgency High | Urgency Medium | Urgency Low |
|---|---|---|---|
| **Impact High** | P1 | P2 | P3 |
| **Impact Medium** | P2 | P3 | P4 |
| **Impact Low** | P3 | P4 | P4 |

A **P1 (major incident)** — company-wide outage, revenue-affecting — triggers a separate major-incident process: an incident commander, a comms lead, a dedicated bridge call, and stakeholder updates at fixed intervals.

### Problem management

A **problem** is the underlying cause of one or more incidents. Where incident management asks *"how do we restore service now?"*, problem management asks *"how do we stop this recurring?"* Outputs: root-cause analysis, known-error records, and permanent fixes. The blameless post-mortem (you'll write one in Phase 4) is the signature problem-management artifact.

### Change management (change enablement)

A **change** is any addition, modification, or removal of something that could affect services. Change management balances **speed of delivery** against **risk of breakage**.

Three change types:
- **Standard** — pre-approved, low-risk, routine (e.g., a documented password reset). No approval needed each time.
- **Normal** — assessed and authorized via a process, often a **Change Advisory Board (CAB)**. Most planned changes.
- **Emergency** — must happen fast (e.g., a security patch for an active exploit). Expedited approval, reviewed after the fact.

> The CAB is where many new IT managers first sit at a decision-making table. Your job there: assess risk, check the rollback plan, confirm the change window, and either authorize or send it back. Approving a change with no rollback plan is the classic rookie mistake.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Configure an incident workflow | ServiceNow Developer Instance (free PDI) | Provision a free personal dev instance; set up incident categories, assignment rules, and SLA timers | **Free** |
| Build a priority matrix | Notion or Google Sheets | Create an impact × urgency matrix; classify 10 sample incidents and justify each priority | **Free** |
| Read the incident response guide | PagerDuty (response.pagerduty.com) | Study the full incident command process: roles, comms, escalation | **Free** |
| Map a change process | Miro (free, 3 boards) | Diagram a normal-change flow from request → CAB → implementation → review | **Free** |

**Practice gate:** you can classify an incident's priority from impact × urgency, explain the difference between an incident and a problem, and describe when a change goes to a CAB vs. when it's pre-approved as standard.

---

## Project & Delivery Basics (~40 hrs)

IT managers either run projects directly or govern people who do. You don't need a PM cert to manage IT, but you do need to speak the language of delivery fluently.

### The project lifecycle

Every project framework — PMBOK, PRINCE2, or a lightweight in-house process — covers the same arc:

1. **Initiation** — why are we doing this? (business case, sponsor, high-level scope)
2. **Planning** — scope, schedule, budget, resources, risks
3. **Execution** — build and deliver the work
4. **Monitoring & controlling** — track progress vs. plan; manage change requests
5. **Closure** — handover, retrospective, benefits review

### The triple constraint

**Scope, time, and cost** form the classic project triangle, with **quality** in the middle. Change one and at least one other has to move. When a stakeholder asks for more scope with no schedule or budget change, your job is to make the tradeoff explicit — not to silently absorb it (that's how projects fail).

### Core project artifacts

- **Project charter** — the one-pager that authorizes the project (objective, scope, sponsor, success criteria). You'll write one in Phase 4.
- **Work breakdown structure (WBS)** — the deliverables broken into manageable tasks.
- **RACI matrix** — who's **R**esponsible, **A**ccountable, **C**onsulted, **I**nformed for each task. Exactly one A per task.
- **Risk register** — covered below; projects own their risks formally.
- **Status report** — the recurring artifact that keeps sponsors informed: progress, risks, decisions needed.

### Waterfall vs. Agile delivery

- **Waterfall / stage-gate (PRINCE2-style):** sequential phases with approval gates. Suits projects with fixed, well-understood scope — a data-center migration, a compliance rollout.
- **Agile:** iterative delivery in sprints, adapting as you learn. Suits projects with evolving requirements — internal tooling, product-adjacent work.

Most real IT delivery is **hybrid**: agile execution inside a stage-gated governance wrapper that finance and the steering committee understand.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Build a project charter | Asana template (free) | Draft a charter for a fictional "migrate team to SSO" project: objective, scope, success criteria, milestones | **Free** |
| Create a RACI matrix | Miro (free) | Map 6–8 tasks × 5–6 roles; ensure exactly one Accountable per task | **Free** |
| Run a status report | Google Docs | Write a 1-page project status: % complete, top risks, decisions needed, next milestone | **Free** |
| Audit Google PM concepts | Coursera (audit free) | Audit the Google Project Management Certificate modules on planning and execution | **Free** (audit) |

**Practice gate:** you can explain the triple constraint with a concrete tradeoff example, build a RACI matrix with correct A/R separation, and describe when you'd choose waterfall vs. agile delivery for a given IT project.

---

## Metrics, KPIs & SLAs (~30 hrs)

"You can't manage what you can't measure" is a cliché because it's true for IT operations. This block teaches you the metrics that matter and how to set service targets people can actually hit.

### SLAs, OLAs, and underpinning contracts

- **SLA (Service Level Agreement)** — the commitment to your customer (the business or end users). E.g., "P1 incidents responded to within 15 minutes, resolved within 4 hours."
- **OLA (Operational Level Agreement)** — internal commitments *between teams* that make the SLA achievable. E.g., "the network team responds to escalations from the service desk within 30 minutes."
- **Underpinning contract** — the SLA-equivalent with an external vendor.

> The rookie error is promising an SLA to the business without the OLAs and vendor contracts to back it. If your customer SLA is 4-hour resolution but your hardware vendor's contract allows 48-hour part replacement, your SLA is fiction. Chain the commitments.

### The operational metrics that matter

| Metric | What it measures | Why it matters |
|---|---|---|
| **MTTR** (Mean Time to Restore/Resolve) | Average time to restore service after an incident | The headline incident-management metric |
| **MTBF** (Mean Time Between Failures) | Average uptime between failures | Reliability of a service or component |
| **MTTA** (Mean Time to Acknowledge) | Time from alert to someone owning it | On-call responsiveness |
| **SLA breach rate** | % of incidents that missed their SLA | Direct measure of service-desk health |
| **First-contact resolution** | % resolved without escalation | Service-desk efficiency and skill |
| **Ticket volume by category** | Where the work actually comes from | Tells you what to automate or fix at the root |
| **Uptime / availability** | % of time a service is usable (e.g., 99.9%) | The number executives quote |

### Reading availability targets

"Three nines" (99.9%) sounds great until you do the math: it allows **~8.7 hours of downtime per year**. "Four nines" (99.99%) allows ~52 minutes. The more nines, the exponentially more expensive to deliver. Part of the IT manager's job is telling the business what a given availability target actually costs — and whether they really need it.

### SLIs and SLOs (the SRE vocabulary)

Modern ops borrows from Google's SRE practice:
- **SLI (Service Level Indicator)** — the actual measured value (e.g., current request success rate)
- **SLO (Service Level Objective)** — the internal target for that SLI (e.g., 99.5%)
- **Error budget** — the allowed amount of failure (100% − SLO). When you've burned the budget, you stop shipping risky changes and focus on reliability.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Build an SLA dashboard mock | Google Sheets or Miro | Define SLAs for P1–P4; build a mock weekly dashboard with ticket volumes, breach rates, and a trend chart | **Free** |
| Calculate availability budgets | Paper or Sheets | Compute allowed downtime for 99%, 99.9%, 99.99%; explain the cost implication of each | **Free** |
| Read the SRE workbook intro | Google SRE (sre.google/books) | Read the chapters on SLIs, SLOs, and error budgets | **Free** |

**Practice gate:** you can define SLA/OLA/SLI/SLO without confusing them, calculate the annual downtime allowed by a "number of nines" target, and explain why an SLA needs OLAs and vendor contracts to be real.

---

## IT Budgeting & Financial Management (~25 hrs)

Financial fluency is the single biggest skill gap that stalls technical managers. The ones who plateau can run a flawless service desk but can't build a budget or defend a spend to finance. Don't be one of them.

### CapEx vs. OpEx

- **CapEx (Capital Expenditure)** — large up-front purchases of assets used over years (servers, network hardware, perpetual software licenses). Depreciated over time on the books.
- **OpEx (Operating Expenditure)** — ongoing running costs (cloud subscriptions, SaaS licenses, support contracts, salaries). Expensed in the period they occur.

> The cloud shift is fundamentally a CapEx→OpEx shift: instead of buying servers (CapEx), you rent compute monthly (OpEx). Finance teams care deeply about this distinction because it changes the company's tax and cash-flow profile. An IT manager who understands it earns instant credibility in budget meetings.

### TCO and ROI

- **TCO (Total Cost of Ownership)** — the full lifetime cost of something, not just the sticker price: license + implementation + training + support + maintenance + eventual decommissioning. The cheap tool with high integration and support costs often has a higher TCO than the "expensive" one.
- **ROI (Return on Investment)** — `(gain − cost) / cost`. For IT, "gain" is often cost *avoided* (staff hours saved, downtime prevented) rather than revenue earned. Quantifying avoided cost is the heart of every IT business case.

### Chargeback and showback

- **Showback** — reporting to each department what its IT consumption *would* cost, for visibility (no actual billing).
- **Chargeback** — actually billing departments for their IT consumption. Drives accountability but adds administrative overhead.

### The budget cycle

Most organizations run an annual budget cycle: you forecast next year's IT spend (broken into CapEx/OpEx, by category), defend it, then track **actuals vs. forecast** monthly and explain variance. "We're 8% over on cloud spend because of the unplanned data-migration egress costs" is the kind of sentence you'll say often.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Build a TCO comparison | Google Sheets | Compare 3-year TCO of two ITSM tools (license + setup + training + support); identify the break-even point | **Free** |
| Classify CapEx vs OpEx | Paper or Sheets | Sort 15 IT expenses into CapEx/OpEx and justify each | **Free** |
| Draft an IT investment memo | Google Docs | Write a 1-page business case for a tool purchase with a quantified ROI (cost-avoided basis) | **Free** |

**Practice gate:** you can classify an expense as CapEx or OpEx and explain why finance cares, calculate a simple ROI on a cost-avoidance basis, and articulate why the cheapest tool isn't always the lowest TCO.

---

## Vendor, Risk & Stakeholder Management (~20 hrs)

The final core block covers three relationship-and-judgment skills that don't fit neatly into a framework but define whether you're trusted with bigger scope.

### Vendor & contract management

IT runs on third parties — SaaS providers, hardware suppliers, MSPs, consultants. Managing them well is a core skill:

- **Selection:** run a structured evaluation (RFP/RFI). Score vendors against weighted criteria (cost, integrations, security posture, support quality, SLAs) — don't pick on vibes or the slickest demo.
- **Negotiation:** SLAs, pricing tiers, exit clauses, data ownership. Always know your **exit cost** before you sign.
- **Ongoing governance:** quarterly business reviews (QBRs), SLA performance tracking, renewal management. A vendor who hit their SLAs in year one and coasts in year two is common — governance catches it.
- **Third-party risk:** a vendor's security posture is now *your* risk. Vendor breaches are a leading cause of incidents.

### Risk management

Risk management is identifying what could go wrong, how likely it is, how bad it would be, and what you'll do about it.

The core tool is the **risk register** (you'll build one in Phase 4). Each risk gets:
- A specific description (not "data loss" but "users save to local drives during cutover, losing data")
- **Likelihood × Impact** scoring (usually 1–5 each)
- A **risk score** (the product) to rank by
- A **mitigation** (concrete action) and an **owner**
- A **residual risk** rating after mitigation

The four standard risk responses: **avoid** (don't do the risky thing), **mitigate** (reduce likelihood/impact), **transfer** (insurance, or push it to a vendor contract), **accept** (it's cheap enough to just live with). Knowing which response fits is the judgment part.

### Stakeholder management

You deliver everything through other people, most of whom you don't control. Stakeholder management is the skill of keeping the right people informed and aligned.

The classic tool is the **power/interest grid**:

| | Low Interest | High Interest |
|---|---|---|
| **High Power** | Keep satisfied | Manage closely |
| **Low Power** | Monitor | Keep informed |

Map your stakeholders, then set a communication cadence for each quadrant. The CFO (high power, periodic interest) gets a concise monthly summary; the engineering lead you depend on daily (high interest) gets continuous contact. Getting this wrong — over-communicating to executives, under-communicating to key collaborators — is a common, avoidable failure.

> **Managing up** is the sub-skill that accelerates careers: giving your own manager and skip-level the right information at the right altitude, flagging risks early, and never letting them be surprised. "No surprises" is the entire job in three words.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Build a vendor evaluation matrix | Google Sheets or Notion | Score 3 fictional vendors across 8 weighted criteria for an ITSM purchase; document the decision rationale | **Free** |
| Create a risk register | Asana template or Sheets | Build 10+ risks for a cloud migration, scored by likelihood × impact, with mitigations and owners | **Free** |
| Map stakeholders | Miro (free) | Plot 8 stakeholders for an IT program on a power/interest grid; define a comms cadence per quadrant | **Free** |

**Practice gate:** you can run a weighted vendor evaluation, build a risk register with likelihood × impact scoring and name the four risk responses, and place stakeholders on a power/interest grid with an appropriate communication cadence for each.

---

## Phase 2 checkpoint

You've now covered the operational core of IT management. Before moving to specialization, confirm you can:

- [ ] Classify incident priority and distinguish incident / problem / change management
- [ ] Explain the triple constraint and build a correct RACI matrix
- [ ] Define SLA/OLA/SLI/SLO and calculate availability budgets
- [ ] Classify CapEx vs OpEx and build a simple TCO/ROI case
- [ ] Run a vendor evaluation, build a risk register, and map stakeholders

If any box is empty, revisit that block — Phase 3 and the portfolio in Phase 4 assume all of this is solid.

---

Next: [Phase 3 — Pick a Track →](03-specialization.md)
