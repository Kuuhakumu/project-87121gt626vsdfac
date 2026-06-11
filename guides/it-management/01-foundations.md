# 📁 Phase 1: Foundations

> **~120 hrs total** · your pace, no deadline
> What IT management actually is, the five sub-tracks and how they diverge, ITIL 4 service-management basics, Agile/Scrum vocabulary, and the core skill nobody warns you about: communication.

[← Phase 0](00-prep.md) · [Hub](README.md) · [Next: Phase 2 — Core Skills →](02-core.md)

---

## What IT Management & Strategy actually is (~25 hrs)

"IT Management & Strategy" is an umbrella over five distinct but overlapping disciplines. Understanding how they diverge is the most important framing decision you'll make — it determines which on-ramp, which certs, and which specialization in [Phase 3](03-specialization.md) are right for you.

### The five sub-tracks

**1. IT Service Management (ITSM)**
Delivering and supporting IT services to the business. Rooted in ITIL 4. The work is operational and process-driven: incident management, change management, problem management, SLAs, service desks, continual improvement. Senior destination: Service Delivery Manager, IT Operations Manager.
*The question ITSM answers: "Are our services running well and improving?"*

**2. IT Project & Program Management**
Delivering defined outcomes on time and budget — system implementations, migrations, infrastructure rollouts, transformation initiatives. Governed by PMI (PMP, CAPM) and PRINCE2. Distinct from ITSM because projects *end* — you don't own the service after go-live. Senior destination: Program Manager, PMO Director.
*The question: "Are we delivering this change successfully?"*

**3. IT Governance & Strategy**
Ensuring IT decisions align with organizational goals, risk is managed, and IT investment generates value. COBIT 2019 is the dominant framework; TOGAF addresses enterprise architecture. Senior destination: CIO, IT Director, Enterprise Architect, Governance Lead.
*The question: "Is IT serving the organization's long-term interests and managing its risks?"*

**4. People & Team Management**
The line-management track: hiring, performance reviews, team structure, budget ownership, 1:1s, career development. Less framework-driven, more leadership-competency-driven. This is the track a senior engineer or sysadmin enters when they move into management. It overlaps with all the others — every IT manager does some of this.
*The question: "Is my team healthy, growing, and delivering?"*

**5. IT Operations**
The day-to-day running of infrastructure, platforms, and systems — networks, servers, cloud, monitoring, incident response. Operationally adjacent to ITSM but more technically focused. Senior destination: Infrastructure Manager, Head of Platform.
*The question: "Is everything up, performing, and secure?"*

### Where they overlap and diverge

| Dimension | ITSM | Project Mgmt | Governance/Strategy | People Mgmt | IT Ops |
|---|---|---|---|---|---|
| Time horizon | Ongoing | Fixed end-date | Multi-year | Ongoing | Ongoing |
| Primary output | Service quality | Delivered change | Risk/value alignment | Team performance | System uptime |
| Key framework | ITIL 4 | PMP / PRINCE2 | COBIT / TOGAF | None (leadership) | ITIL / SRE |
| Typical entry | Service desk | Junior PM / BA | Audit / architecture | Tech lead | Sysadmin / NOC |

- ITSM and IT Operations share incident and problem management heavily; in a small org, one person covers both.
- Governance uses ITSM's process metrics as evidence for audit and compliance.
- Project Management *executes* the changes that IT Strategy *defines*.
- People Management is a layer on top of every track.

> **Don't try to master all five.** Foundations and core skills (Phases 1–2) are shared across all of them. In [Phase 3](03-specialization.md) you'll pick one to go deep. For now, just learn the map.

### The scope boundary (what this guide is *not*)

This guide covers **managing and governing IT** — not building products, not writing code, not doing hands-on technical support.

- **Not Product Management** ([that guide](../product-management/)): a PM manages *a product* (its features, market position, users). An IT manager manages *an IT function* (services, teams, budgets, risk) for the whole organization internally.
- **Not IT Support** ([that guide](../it-support-networking/)): IT Support does the hands-on troubleshooting. IT Management *leads the function* that does it — setting process, owning the budget, reporting to leadership.

> In one sentence: **this guide takes you from team lead to CIO — leading the people, processes, and governance of IT, not doing the technical work yourself.**

**Practice gate:** you can name the five sub-tracks, state the question each one answers, and explain in your own words how IT Management differs from both Product Management and IT Support.

---

## ITIL 4 — the service-management foundation (~40 hrs)

ITIL 4 is the most widely recognized framework in IT service management worldwide. Even if you never sit the exam, its vocabulary is the lingua franca of IT operations — you need fluency.

> **2026 note:** PeopleCert (which owns the ITIL IP) has begun rolling out a newer ITIL version restructured around five streams (Product, Service, Experience, Strategy, Transformation). **ITIL 4 Foundation is still actively offered and recognized** as of mid-2026, and its concepts below remain the core. See [certifications.md](certifications.md) for the current exam picture and confidence tags — and confirm the live exam version on the official site before booking.

### The core concepts

**Services and value.** ITIL frames IT as a *service provider* to the business. A service delivers value by enabling outcomes the customer wants, without the customer owning the specific costs and risks. (Example: "email" is a service — staff get reliable communication without managing mail servers themselves.)

**The four dimensions of service management:**
1. Organizations and people
2. Information and technology
3. Partners and suppliers
4. Value streams and processes

A healthy service balances all four. Ignore "organizations and people" and the best tooling still fails.

**The service value chain** — six activities that turn demand into value: Plan · Improve · Engage · Design & Transition · Obtain/Build · Deliver & Support.

**The key practices an entry-level manager must know cold:**

| Practice | What it is |
|---|---|
| **Incident Management** | Restore normal service as fast as possible after an unplanned disruption |
| **Problem Management** | Find and fix the *root cause* behind recurring incidents (incident = symptom, problem = cause) |
| **Change Enablement** | Assess, authorize, and schedule changes to minimize risk (the Change Advisory Board lives here) |
| **Service Request Management** | Handle routine, pre-approved requests (new laptop, access grant) — distinct from incidents |
| **Service Level Management** | Define, monitor, and report on SLAs |
| **Continual Improvement** | The ongoing discipline of making services measurably better over time |

> The distinction interviewers probe most: **incident vs. problem.** An incident is "the website is down — restore it now." A problem is "the website has gone down four times this month — why, and how do we stop it permanently?" Incident management is reactive and speed-focused; problem management is investigative and prevention-focused.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Read the ITIL 4 overview | [Axelos ITIL page](https://www.axelos.com/certifications/itil-service-management) | Get the official framing of services, value, and the four dimensions | **Free** |
| Configure an incident workflow | [ServiceNow Developer Instance](https://developer.servicenow.com/devdo) | Provision a free PDI; set up incident categories, assignment rules, and SLA timers | **Free** |
| Map incident vs. problem | Notion or paper | Take a recurring outage scenario; write the incident response *and* the problem investigation separately | **Free** |
| Explore the Atlassian Team Playbook | [Team Playbook](https://www.atlassian.com/team-playbook/plays) | Run a "health monitor" or "incident response" play to see ITSM practices in action | **Free** |

**Practice gate:** you can explain incident vs. problem vs. change with a concrete example of each, and you've configured one incident workflow (even a basic one) in a ServiceNow developer instance.

---

## Agile, Scrum, and how IT teams actually work (~30 hrs)

Modern IT teams — even operations teams — increasingly run on Agile rhythms. You don't need to be a certified Scrum Master, but you need the vocabulary and the *why*.

### The essentials

**Agile** is a mindset (iterative delivery, responding to change, working in short feedback loops) — not a process. **Scrum** is the most common *framework* that implements it.

**Scrum in 90 seconds:**
- Work is organized into **sprints** (usually 2 weeks).
- A prioritized **product backlog** holds everything that might get done.
- At **sprint planning**, the team pulls a slice of the backlog into the **sprint backlog**.
- A short **daily standup** keeps everyone aligned and surfaces blockers.
- At sprint end, a **review** shows what was completed and a **retrospective** improves how the team works.
- Three roles: **Product Owner** (owns the backlog/priorities), **Scrum Master** (facilitates the process, removes blockers), **Developers** (do the work).

**Kanban** is the lighter alternative — continuous flow, work-in-progress limits, no fixed sprints. Many IT operations teams prefer Kanban because operational work (incidents, requests) arrives unpredictably and doesn't fit neat two-week boxes.

> As an IT manager, you'll often act as a Product-Owner-like prioritizer for your team's work *and* a Scrum-Master-like blocker-remover — even if no one has those titles. Knowing both lenses lets you choose the right rhythm for the work in front of you.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Read the Scrum Guide | [scrumguides.org](https://scrumguides.org) | The authoritative ~13-page reference — read it end to end | **Free** |
| Build a backlog and sprint | [Jira Free](https://www.atlassian.com/software/jira/free) | Create 10+ IT tickets, write acceptance criteria, run a 2-week sprint, move cards to Done | **Free** |
| Run a retrospective | [Miro Free](https://miro.com) | Use a Start/Stop/Continue template; capture action items | **Free** |

**Practice gate:** you can run a sprint in Jira from planning to retrospective, explain when Kanban beats Scrum for operational work, and define the three Scrum roles without notes.

---

## Communication — the real core skill (~25 hrs)

Here's what no framework tells you: **the day-to-day work of an IT manager is overwhelmingly communication.** Translating technical reality for non-technical executives. Explaining an outage to frustrated department heads. Writing a business case that gets budget approved. Giving feedback that lands. Saying "no" to a stakeholder without burning the relationship.

Technical managers who can't do this plateau — usually right at the point where they need to influence people who don't report to them ("influence without authority").

### The communication skills to start building now

**Translating up.** Executives don't care about the certificate that expired; they care that "all staff lost access to email for two hours, here's the business impact, and here's what we're changing so it can't recur." Practice stripping jargon and leading with impact.

**Writing for decisions.** A good IT manager's writing is structured for a busy reader: the recommendation first, the reasoning second, the detail in an appendix. The business case and post-mortem you'll write in [Phase 4](04-projects.md) are exactly this skill.

**Managing up and across.** You'll spend enormous energy on stakeholders who don't report to you — other department heads, vendors, your own boss. Influence comes from credibility, clarity, and reliability, not authority.

**Delivering hard messages.** Outage notifications, project delays, budget cuts, performance feedback. The skill is being direct *and* respectful — stating the reality plainly while preserving the relationship.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Write an outage comms note | Google Docs or Notion | Take the SSO-outage scenario from [Phase 4](04-projects.md); write the all-staff update *and* the executive summary | **Free** |
| Rewrite jargon for executives | Notion | Take a technical incident description; rewrite it leading with business impact, zero acronyms | **Free** |
| Read *The Manager's Path* (intro chapters) | Library / [O'Reilly](https://www.oreilly.com/library/view/the-managers-path/9781491973882/) | Camille Fournier on the management transition and communication — see [resources.md](resources.md) | Varies |

**Practice gate:** you can take a purely technical incident and produce two versions of the same message — one for engineers, one for executives — where the executive version leads with business impact and contains no unexplained jargon.

---

## Phase 1 complete

You now have the map (five sub-tracks), the service-management foundation (ITIL 4), the team-rhythm vocabulary (Agile/Scrum/Kanban), and an honest appreciation that communication is the core skill. Next, the heavier core skills: running service management for real, project delivery, metrics, budgeting, vendors, and risk.

Next: [Phase 2 — Core Skills →](02-core.md)
