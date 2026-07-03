# goal 1: foundations - role, lifecycle, Agile, writing meow

> **~120h total** - your pace, no deadline.
> goal: understand what PM actually is, how products get built, and why writing is the job.

[Previous: Goal 0](00-prep.md) - [Hub](README.md) - [Next: Goal 2](02-core.md)

---

- [ ] **what PM actually is** (~40h)
- [ ] **product development lifecycle** (~30h)
- [ ] **Agile and Scrum fundamentals** (~30h)
- [ ] **communication and writing** (~20h)
- [ ] **exit check** - PM role, lifecycle, Scrum, PRD draft, writing fluency

## what PM actually is (~40h)

before frameworks, u need an accurate model of what PMs do and dont do.

### the PM job in plain language

a Product Manager is responsible for:

1. **Discovery** - figure out what problems are worth solving through users, data, and market context.
2. **Definition** - state the problem and proposed solution clearly enough that a team can build.
3. **Delivery** - work with engineering and design to ship.
4. **Learning** - measure whether it worked and decide what to do next.

what PMs are not responsible for in well-run teams:

- [ ] writing code or designing UI
- [ ] making unilateral product decisions
- [ ] managing engineers
- [ ] guaranteeing project timelines they dont control

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [SVPG "The Kind of Product Manager We're Looking For"](https://www.svpg.com/the-kind-of-product-manager-we-are-looking-for/) | SVPG | absorb the canonical empowered-PM definition | **Free** |
| [Marty Cagan "Product vs Feature Teams"](https://www.svpg.com/product-vs-feature-teams/) | SVPG | understand feature-team vs product-team reality | **Free** |
| [Lenny's Newsletter](https://www.lennysnewsletter.com) | Newsletter | read the "What is a PM" practitioner take - ⚠️ TODO verify exact article link | **Free** tier |
| [Lenny's Podcast](https://www.lennysnewsletter.com/podcast) | Podcast | listen to 3 working PM episodes - ⚠️ TODO verify exact starter episodes | **Free** |

**practice gate:** u can explain in two sentences what a PM does, what they dont do, and how that differs from a Product Owner, without saying "CEO of the product."

## product development lifecycle (~30h)

the product lifecycle is the loop from idea to data.
everything else hangs on this frame.

```text
Discover -> Define -> Design -> Build -> Measure -> Learn -> repeat
```

- [ ] **Discover:** user research, competitive analysis, data analysis, stakeholder conversations.
- [ ] **Define:** problem framing, opportunity sizing, success metrics, PRD writing.
- [ ] **Design:** wireframes, prototypes, design reviews. PMs participate, designers own.
- [ ] **Build:** sprint planning, backlog grooming, stand-ups, unblocking engineers.
- [ ] **Measure:** instrumentation, dashboards, qualitative feedback, A/B test results.
- [ ] **Learn:** did it work, why or why not, whats next?

### what makes the loop break

- [ ] **Discovery skipped** - building features that dont solve real user problems.
- [ ] **Definition vague** - engineers build different things than intended.
- [ ] **Measurement absent** - no metrics defined upfront, so nobody knows if it worked.

when u read product postmortems, many failures trace to one of those three.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Map one app's lifecycle | paper + Notion | sketch the discover -> measure loop for one feature u know well | **Free** |
| Read 2-3 product postmortems | [First Round Review](https://review.firstround.com) | identify which part of the loop broke - ⚠️ TODO verify exact starter postmortems | **Free** |
| Notion product lifecycle template | Notion | clone a lifecycle doc and fill it for your chosen product - ⚠️ TODO verify exact template link | **Free** |

**practice gate:** u can walk through the lifecycle loop for a real product and identify where discovery, definition, or measurement looks weak.

## Agile and Scrum fundamentals (~30h)

most PM jobs operate inside some flavor of Agile.
u dont need to become a Scrum Master, but u do need the vocabulary and ceremonies.

### core vocabulary

- [ ] **Sprint:** time-boxed work period, usually 1-2 weeks.
- [ ] **Backlog:** prioritized list of possible work. product backlog belongs to the PM/PO. sprint backlog belongs to the sprint.
- [ ] **User story:** requirement from the user's perspective. `As a [user], I want [action] so that [benefit].`
- [ ] **Acceptance criteria:** testable conditions that define done.
- [ ] **Sprint planning:** team selects and sizes work for the sprint.
- [ ] **Daily stand-up / daily scrum:** 15-minute sync on progress and blockers.
- [ ] **Sprint review / demo:** built work is shown to stakeholders.
- [ ] **Sprint retrospective:** team reflects on process.
- [ ] **Definition of Done (DoD):** agreed criteria for what "done" means.
- [ ] **Velocity:** work completed per sprint, used for forecasting, not judging individuals.

### PM's role in Scrum

- [ ] own and prioritize the product backlog
- [ ] write clear stories with acceptance criteria before sprint planning
- [ ] answer clarifying questions quickly during the sprint
- [ ] participate in reviews and retrospectives
- [ ] shield the team from mid-sprint scope changes where possible

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Jira free workspace: create a backlog | [Atlassian Jira](https://www.atlassian.com/software/jira) | set up a project, write 10 user stories, prioritize them | **Free** |
| [Scrum Guide](https://www.scrum.org/resources/scrum-guide) | Scrum.org | read the canonical Scrum Guide | **Free** |
| Simulated sprint planning | Jira + Notion | plan a 2-week sprint by selecting and sizing stories | **Free** |
| 5 user stories with acceptance criteria | Notion | write 5 stories for your chosen product until the format feels fluent | **Free** |

Kanban exists too, especially in startups.
continuous flow vs sprint cadence matters less than knowing the team's actual process.

**practice gate:** u can explain product backlog vs sprint backlog, write a user story with acceptance criteria, and describe the four main Scrum ceremonies.

## communication and writing (~20h)

this gets less glamorous billing than discovery frameworks or prioritization.
but its the most important part of Goal 1, maybe the whole guide.

### why writing is the PM job

every PM output is a document:

- [ ] PRDs and specs explain what to build
- [ ] roadmaps explain whats coming and why
- [ ] strategy memos align leadership
- [ ] stakeholder updates reduce meetings
- [ ] interview answers reveal written-quality thinking

PMs who write clearly make teams faster.
vague specs create rework.
unclear reasoning creates endless alignment meetings.
the quality of your writing is a proxy for the quality of your thinking.

### what good PM writing looks like

- [ ] starts with the problem, not the solution
- [ ] states assumptions explicitly
- [ ] separates what from why
- [ ] has a clear "so what": decision, next step, or recommendation
- [ ] is shorter than u think. a one-page problem statement beats a 10-page unread spec

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| One-page problem statement | Notion | state the problem, who has it, why it matters, and success criteria | **Free** |
| Read 3 real PRD examples | GitHub / product blogs | analyze structure, not content - ⚠️ TODO verify exact examples | **Free** |
| First draft PRD | Notion | write a full PRD for one feature of your chosen product | **Free** |
| Rewrite a vague requirement | Notion | turn "improve search" into something specific and measurable | **Free** |

**practice gate:** u can write a one-page problem statement that starts with the user problem, states success metric, and makes assumptions explicit in under 30 minutes.

## exit check

- [ ] i can explain what a PM does and doesnt do, and distinguish PM from Product Owner
- [ ] i can map the product lifecycle loop for a real product
- [ ] i know Scrum ceremonies, artifacts, and vocabulary well enough to participate on day one
- [ ] i wrote 5+ user stories with acceptance criteria in Jira
- [ ] i drafted a one-page problem statement and first PRD for my chosen product
- [ ] i can explain why communication/writing is the core PM skill

[Next: Goal 2 - Core PM Skills](02-core.md)
