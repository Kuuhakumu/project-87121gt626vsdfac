# Interactive lab and tool inventory: IT Management (2026) meow

> every platform was verified June 2026.
> IT management practice means producing artifacts and running processes in real tools, not just reading.

Status labels: `live`, `bot-blocked but works in browser`, `dead`.

use this as your menu.
the portfolio in [Goal 4](04-projects.md) lives in these tools, so set up the free tiers early.

---

- [ ] **service management and ticketing**
- [ ] **project and work management**
- [ ] **templates and frameworks**
- [ ] **roadmapping**
- [ ] **governance, risk, frameworks**
- [ ] **case studies and simulations**
- [ ] **dead or changed resources**

## service management and ticketing

| Lab | Platform | What u do | Cost | Status |
|---|---|---|---|---|
| [Jira Free](https://www.atlassian.com/software/jira/free) | Atlassian | run backlog, sprints, tickets, velocity | **Free** up to 10 users | live |
| [Jira Service Management](https://www.atlassian.com/software/jira/service-management) | Atlassian | configure service desk, request types, SLA timers | **Free** tier | live |
| [ServiceNow Developer PDI](https://developer.servicenow.com/devdo) | ServiceNow | build incident workflow with categories, assignment rules, SLA timers | **Free** personal dev instance | live |
| [PagerDuty Free](https://www.pagerduty.com/pricing) | PagerDuty | on-call rotations, escalation policies, incident response | **Free** up to 5 users | live |
| [Confluence Free](https://www.atlassian.com/software/confluence/free) | Atlassian | service catalog, runbooks, team wiki | **Free** up to 10 users | live |

**practice gate:** provision ServiceNow PDI or Jira Service Management, configure one incident workflow with categories, an assignment rule, and an SLA timer. screenshot it and explain routing choices.

## project and work management

| Lab | Platform | What u do | Cost | Status |
|---|---|---|---|---|
| [Asana Free](https://asana.com/pricing) | Asana | project charter, timeline, risk register templates | **Free** tier | live |
| [Trello Free](https://trello.com/pricing) | Atlassian | lightweight kanban and action tracking | **Free** tier | live |
| [Monday.com Free](https://monday.com/pricing) | monday.com | work boards and dependency tracking | **Free** up to 2 seats | live |
| [Linear Free](https://linear.app/pricing) | Linear | issue tracking and roadmap | **Free** tier | live |
| [Notion Free](https://www.notion.com/pricing) | Notion | catalog, 90-day plan, OKRs, business cases, portfolio index | **Free** tier | live |

**practice gate:** build a project charter and RACI for "migrate team to SSO." every task has exactly one Accountable owner.

## templates and frameworks

| Lab | Platform | What u do | Cost | Status |
|---|---|---|---|---|
| [Atlassian Team Playbook](https://www.atlassian.com/team-playbook/plays) | Atlassian | health monitors, DACI, retrospectives | **Free** | live |
| [Asana Templates](https://asana.com/templates) | Asana | charter, risk register, roadmap, sprint planning, RACI | **Free** | live |
| [Miro Templates](https://miro.com/templates) | Miro | service blueprints, RACI, retrospectives, roadmaps | **Free** 3 boards | live |
| [OKR framework repo](https://github.com/joelparkerhenderson/objectives-and-key-results) | GitHub | OKR examples, templates, anti-patterns | **Free** | live |
| [Awesome SRE](https://github.com/dastergon/awesome-sre) | GitHub | post-mortems, runbooks, SLI/SLO resources | **Free** | live |
| [PagerDuty Incident Response](https://response.pagerduty.com) | PagerDuty | incident command process, roles, runbooks | **Free** | live |
| [PagerDuty Post-mortems](https://postmortems.pagerduty.com) | PagerDuty | blameless post-mortem guide and template | **Free** | live |

**practice gate:** simulate a P1 incident and complete a blameless post-mortem with timeline, contributing factors, and 5+ action items.

## roadmapping and visualization

| Lab | Platform | What u do | Cost | Status |
|---|---|---|---|---|
| [Miro Free](https://miro.com/pricing) | Miro | service blueprints, 12-month roadmap, retro boards | **Free** 3 boards | live |
| [Linear Free](https://linear.app/pricing) | Linear | visual roadmap by initiative/theme | **Free** tier | live |
| [Notion](https://www.notion.com/pricing) | Notion | roadmap tables, quarterly planning | **Free** tier | live |

**practice gate:** build a 12-month IT roadmap for a fictional startup with swimlanes by infrastructure, security, tooling, and team.

## governance, risk, and frameworks

| Lab | Platform | What u do | Cost | Status |
|---|---|---|---|---|
| [ITIL 4 overview](https://www.axelos.com/certifications/itil-service-management) | Axelos / PeopleCert | service value system and four dimensions | **Free** overview | live |
| [COBIT resources](https://www.isaca.org/resources/cobit) | ISACA | governance and IT risk intro content | **Free** intro | live |
| [TOGAF Standard](https://www.opengroup.org/togaf) | The Open Group | enterprise architecture overview | **Free** overview | live |
| [ISACA IT Risk Fundamentals](https://www.isaca.org/resources/it-risk) | ISACA | IT risk and governance intro content | **Free** | live |
| [SFIA 9 framework](https://sfia-online.org/en/sfia-9) | SFIA Foundation | self-assess skills Levels 1-7 | **Free** | live |

**practice gate:** self-assess against SFIA 9. pick 5 skills relevant to your target track and rate current level 1-7.

## case studies and simulations

| Lab | Platform | What u do | Cost | Status |
|---|---|---|---|---|
| [Atlassian Team Playbook](https://www.atlassian.com/team-playbook/plays) | Atlassian | facilitated exercises solo or group | **Free** | live |
| [PagerDuty Incident Response](https://response.pagerduty.com) | PagerDuty | role-play incident command | **Free** | live |
| [Google Project Management Certificate](https://www.coursera.org/professional-certificates/google-project-management) | Coursera | graded artifacts: stakeholders, project plans, risk registers | **Free** audit / ~$49/mo cert | live |
| [Harvard Business Publishing cases](https://hbsp.harvard.edu/cases) | HBP | IT strategy and org-change MBA cases | ~$4-9/case paywalled | bot-blocked/paywalled |
| [AXELOS ITIL practice guides](https://www.axelos.com/certifications/itil-service-management) | Axelos | ITIL scenario exercises and practice questions | **Free** overview; paid full guides | live |

## dead or changed since 2021

| Old resource | Status | Replacement |
|---|---|---|
| `projectmanagement.com/templates/` | 403 crawler-blocked | PMI.org with free account, or Asana/Miro templates |
| `notion.com/templates/category/project-management` | 404, URL changed | `notion.com/templates` root |
| Patrick Lencioni `tablegroup.com/topics/meetings/` | 404, restructured | Atlassian Team Playbook |
| Katacoda | shut down 2022 | ServiceNow PDI, Jira Free |

---

*URLs status-checked June 2026. Bot-blocked/paywalled means works in browser or with account. Confirm JS-rendered pricing on official sites before subscribing. Sources in [/research](../../research/).*
