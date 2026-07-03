# goal 1: foundations - IT management map, ITIL, Agile, communication meow

> **~120h total** - your pace, no deadline.
> goal: understand what IT management is, which track fits u, and why communication is the real core skill.

[Previous: Goal 0](00-prep.md) - [Hub](README.md) - [Next: Goal 2](02-core.md)

---

- [ ] **what IT management and strategy actually is** (~25h)
- [ ] **ITIL 4 service-management foundation** (~40h)
- [ ] **Agile, Scrum, and Kanban** (~30h)
- [ ] **communication** (~25h)
- [ ] **exit check** - five tracks, ITIL basics, sprint vocabulary, executive comms

## what IT management & strategy actually is (~25h)

IT Management & Strategy is an umbrella over five related disciplines.
understanding the split matters because it determines your on-ramp, certs, and [Goal 3](03-specialization.md) specialization.

### the five sub-tracks

**1. IT Service Management (ITSM)**
delivering and supporting IT services to the business.
rooted in ITIL 4.
daily work: incident, change, problem, SLAs, service desks, continual improvement.
senior destination: Service Delivery Manager, IT Operations Manager.
question: **are our services running well and improving?**

**2. IT Project & Program Management**
delivering defined outcomes on time and budget: implementations, migrations, rollouts.
governed by PMI and PRINCE2.
projects end; u dont necessarily own the service after go-live.
senior destination: Program Manager, PMO Director.
question: **are we delivering this change successfully?**

**3. IT Governance & Strategy**
making sure IT decisions align with org goals, manage risk, and generate value.
COBIT 2019 is the main governance framework.
TOGAF addresses enterprise architecture.
senior destination: CIO, IT Director, Enterprise Architect.
question: **is IT serving long-term interests and managing risk?**

**4. People & Team Management**
hiring, reviews, team structure, budget ownership, 1:1s, career growth.
less framework-driven, more leadership-craft driven.
overlaps with every track.
question: **is my team healthy, growing, and delivering?**

**5. IT Operations**
running infrastructure, platforms, systems, networks, cloud, monitoring, incident response.
adjacent to ITSM but more technical.
senior destination: Infrastructure Manager, Head of Platform.
question: **is everything up, performing, and secure?**

### overlap and divergence

| Dimension | ITSM | Project Mgmt | Governance/Strategy | People Mgmt | IT Ops |
|---|---|---|---|---|---|
| Time horizon | ongoing | fixed end-date | multi-year | ongoing | ongoing |
| Primary output | service quality | delivered change | risk/value alignment | team performance | system uptime |
| Key framework | ITIL 4 | PMP / PRINCE2 | COBIT / TOGAF | leadership craft | ITIL / SRE |
| Typical entry | service desk | junior PM / BA | audit / architecture | tech lead | sysadmin / NOC |

- [ ] ITSM and IT Ops share incident and problem management.
- [ ] Governance uses ITSM metrics as audit evidence.
- [ ] Project Management executes changes that IT Strategy defines.
- [ ] People Management sits on top of every track.

dont try to master all five rn.
Goals 1-2 are shared.
Goal 3 is where u pick one to go deep.

### scope boundary

this guide covers **managing and governing IT**.
it is not building products, writing code, or doing hands-on support.

- [ ] **Not Product Management**: PM manages a product; IT manager manages an internal IT function.
- [ ] **Not IT Support**: support troubleshoots; IT management leads the function that does it.

one sentence: this guide takes u from team lead toward CIO, leading people, processes, and governance of IT.

**practice gate:** u can name the five sub-tracks, state the question each answers, and explain how IT Management differs from Product Management and IT Support.

## ITIL 4 service-management foundation (~40h)

ITIL 4 is the most recognized framework in IT service management.
even if u never sit the exam, its vocabulary is the language of IT operations.

2026 note: PeopleCert has begun rolling out ITIL Version 5 around five streams: Product, Service, Experience, Strategy, Transformation.
**ITIL 4 Foundation is still actively offered and recognized** as of mid-2026.
see [certifications.md](certifications.md) and confirm the live exam version before booking.

### core concepts

- [ ] **Services and value:** IT is a service provider to the business. email is a service; staff get communication without managing mail servers.
- [ ] **Four dimensions:** organizations and people, information and technology, partners and suppliers, value streams and processes.
- [ ] **Service value chain:** Plan, Improve, Engage, Design & Transition, Obtain/Build, Deliver & Support.

entry-level manager practices:

| Practice | What it is |
|---|---|
| **Incident Management** | restore normal service fast after disruption |
| **Problem Management** | find and fix root causes behind recurring incidents |
| **Change Enablement** | assess, authorize, and schedule changes to reduce risk |
| **Service Request Management** | handle routine pre-approved requests |
| **Service Level Management** | define, monitor, and report SLAs |
| **Continual Improvement** | make services measurably better over time |

the interview distinction: **incident vs problem**.
incident = website is down, restore it now.
problem = website went down four times, why and how do we stop it?

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| ITIL 4 overview | [Axelos ITIL page](https://www.axelos.com/certifications/itil-service-management) | get official framing of services, value, four dimensions | **Free** |
| Incident workflow | [ServiceNow Developer Instance](https://developer.servicenow.com/devdo) | provision PDI and set incident categories, assignment rules, SLA timers | **Free** |
| Incident vs problem map | Notion or paper | take a recurring outage and write incident response + problem investigation separately | **Free** |
| Atlassian Team Playbook | [Team Playbook](https://www.atlassian.com/team-playbook/plays) | run a health monitor or incident response play | **Free** |

**practice gate:** u can explain incident vs problem vs change with concrete examples, and u configured one basic incident workflow in ServiceNow.

## Agile, Scrum, and how IT teams work (~30h)

modern IT teams often run on Agile rhythms.
u dont need to be a Scrum Master, but u need the vocabulary and the why.

Agile is a mindset: iterative delivery, short feedback loops, responding to change.
Scrum is a framework that implements it.

### Scrum in 90 seconds

- [ ] work is organized into **sprints**, usually 2 weeks.
- [ ] a prioritized **product backlog** holds possible work.
- [ ] **sprint planning** pulls work into the sprint backlog.
- [ ] **daily standup** surfaces progress and blockers.
- [ ] **review** shows completed work.
- [ ] **retrospective** improves how the team works.
- [ ] roles: Product Owner, Scrum Master, Developers.

Kanban is lighter: continuous flow, WIP limits, no fixed sprints.
IT operations teams often prefer Kanban because incidents and requests arrive unpredictably.

as an IT manager, u may act like a Product-Owner-style prioritizer and Scrum-Master-style blocker remover, even if nobody uses those titles.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Scrum Guide | [scrumguides.org](https://scrumguides.org) | read the authoritative reference end to end | **Free** |
| Backlog and sprint | [Jira Free](https://www.atlassian.com/software/jira/free) | create 10+ IT tickets, acceptance criteria, run a 2-week sprint | **Free** |
| Retrospective | [Miro Free](https://miro.com) | use Start/Stop/Continue, capture action items | **Free** |

**practice gate:** u can run a sprint in Jira from planning to retro, explain when Kanban beats Scrum for ops work, and define the three Scrum roles.

## communication: the real core skill (~25h)

the day-to-day work of an IT manager is overwhelmingly communication.
u translate technical reality for executives, explain outages to departments, write business cases, give feedback, and say no without burning trust.

technical managers who cant do this plateau.

### skills to build now

- [ ] **Translating up:** lead with business impact, not technical trivia.
- [ ] **Writing for decisions:** recommendation first, reasoning second, detail in appendix.
- [ ] **Managing up and across:** influence people who dont report to u.
- [ ] **Hard messages:** outages, delays, budget cuts, performance feedback. direct and respectful.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Outage comms note | Google Docs or Notion | use the SSO outage from [Goal 4](04-projects.md); write staff update + executive summary | **Free** |
| Rewrite jargon for executives | Notion | take a technical incident and rewrite it with business impact, no unexplained acronyms | **Free** |
| *The Manager's Path* intro chapters | Library / [O'Reilly](https://www.oreilly.com/library/view/the-managers-path/9781491973882/) | read Camille Fournier on management transition and communication | Varies |

**practice gate:** u can produce engineer and executive versions of the same incident message, where the executive version leads with business impact and has no unexplained jargon.

## exit check

- [ ] i can name the five IT management sub-tracks and the question each answers
- [ ] i can explain IT Management vs Product Management vs IT Support
- [ ] i can explain incident, problem, and change management with examples
- [ ] i configured a basic incident workflow in ServiceNow or equivalent
- [ ] i can explain Scrum roles and when Kanban fits operations better
- [ ] i wrote an outage message for engineers and an executive summary for leadership

[Next: Goal 2 - Core Skills](02-core.md)
