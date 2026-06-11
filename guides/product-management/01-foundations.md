# 🧱 Phase 1: Foundations

> **~120 hrs total** · your pace, no deadline
> What PM actually is, how products are built, core Agile/Scrum mechanics, and why writing is the job.

[← Phase 0](00-prep.md) · [Hub](README.md) · [Next: Phase 2 — Core Skills →](02-core.md)

---

## What PM Actually Is (~40 hrs)

Before diving into any framework, you need an accurate model of what PMs do — and what they don't.

### The PM job in plain language

A Product Manager is responsible for:
1. **Discovery** — figuring out what problems are worth solving (talking to users, analyzing data, understanding the market)
2. **Definition** — articulating the problem and proposed solution clearly enough that a team can build it
3. **Delivery** — working with engineering and design to ship it
4. **Learning** — measuring whether it actually worked and deciding what to do next

What PMs are not responsible for (in well-run teams):
- Writing code or designing UI
- Making unilateral product decisions
- Managing engineers (PMs have no direct reports on the product team)
- Guaranteeing a project timeline

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Read SVPG "The Kind of PM We're Looking For" | [svpg.com](https://www.svpg.com/the-kind-of-product-manager-we-are-looking-for/) | Absorb the canonical definition of the empowered PM role | **Free** |
| Read Marty Cagan's "Product vs Feature Teams" | [svpg.com](https://www.svpg.com/product-vs-feature-teams/) | Understand the feature-team vs product-team distinction that shapes most job realities | **Free** |
| Lenny's Newsletter "What is a PM" | [lennysnewsletter.com](https://www.lennysnewsletter.com) | Modern practitioner take on the role | **Free** tier |
| Watch 3 episodes of Lenny's Podcast | [lennyspodcast.com](https://www.lennyspodcast.com) | Listen to working PMs describe their actual day | **Free** |

**Practice gate:** you can explain in two sentences what a PM does, what they don't do, and how that differs from a Product Owner — without using the phrase "CEO of the product."

---

## The Product Development Lifecycle (~30 hrs)

Understanding how products actually get built — the full loop from idea to data — is the frame everything else hangs on.

### The loop

```
Discover → Define → Design → Build → Measure → Learn → (repeat)
```

**Discover:** user research, competitive analysis, data analysis, stakeholder conversations.
**Define:** problem framing, opportunity sizing, success metrics, PRD writing.
**Design:** wireframes, prototypes, design reviews (PMs participate, don't own).
**Build:** sprint planning, backlog grooming, stand-ups, unblocking engineers.
**Measure:** instrumentation, dashboards, qualitative feedback, A/B test results.
**Learn:** did it work? Why or why not? What's next?

### What makes this loop break

Most of the PM failures you'll encounter come from one of three places:
- **Discovery skipped** — building features that don't solve real user problems because no one asked users
- **Definition vague** — engineers building different things than what was intended because the spec was ambiguous
- **Measurement absent** — no metrics defined upfront, so there's no way to know if it worked

These aren't abstract concepts. When you read product postmortems (Reforge has good ones; so does FirstRound Review), almost every failure traces back to one of these three.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Pick one app you use and map its lifecycle | Paper + Notion | Sketch the discover → measure loop for one feature you know well | **Free** |
| Read 2–3 product postmortems | [firstround.com/review](https://review.firstround.com) | Identify which part of the loop broke | **Free** |
| Notion product lifecycle template | Notion | Clone a product lifecycle doc, fill it in for your chosen product | **Free** |

**Practice gate:** you can walk through the full product lifecycle loop for a real product you know, identifying where discovery, definition, or measurement looks weak.

---

## Agile and Scrum Fundamentals (~30 hrs)

Most PM jobs operate inside some flavor of Agile. You don't need to become a Scrum Master, but you do need to know the vocabulary and ceremonies well enough to participate on day one.

### Core vocabulary

**Sprint:** a time-boxed work period, typically 1–2 weeks, in which a team commits to completing a set of work items.

**Backlog:** the prioritized list of everything the team might work on. The **product backlog** is the PM's responsibility. The **sprint backlog** is what the team commits to for a given sprint.

**User story:** a requirement written from the user's perspective. Format: *"As a [user type], I want [action] so that [benefit]."* Acceptance criteria define when it's done.

**Sprint planning:** the ceremony at the start of a sprint where the team pulls stories from the backlog and commits to what they'll complete.

**Daily stand-up (daily scrum):** 15-minute daily sync. What did I do yesterday? What am I doing today? Any blockers?

**Sprint review / demo:** end of sprint, team demos what was built, stakeholders give feedback.

**Sprint retrospective:** team-only, reflects on process — what went well, what to improve.

**Definition of Done (DoD):** agreed criteria for what "done" means (coded, tested, deployed, accessible, documented?).

**Velocity:** the amount of work a team completes per sprint, measured in story points or items. Used for forecasting, not judging individuals.

### PM's role in Scrum

You are not the Scrum Master (that's a different role). Your Scrum responsibilities are:
- Own and prioritize the product backlog
- Write clear user stories with acceptance criteria before sprint planning
- Be available during the sprint to answer clarifying questions quickly
- Participate in reviews and retrospectives
- Shield the team from scope changes mid-sprint (mostly)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Jira free workspace: create a backlog | [atlassian.com/jira](https://www.atlassian.com/software/jira) | Set up a project, write 10 user stories for your chosen product, prioritize them | **Free** |
| Scrum.org Scrum Guide (read) | [scrum.org/resources/scrum-guide](https://www.scrum.org/resources/scrum-guide) | Read the canonical 13-page Scrum Guide | **Free** |
| Run a simulated sprint planning | Jira + Notion | Take your backlog, "plan" a 2-week sprint by selecting and sizing stories | **Free** |
| Write 5 user stories with acceptance criteria | Notion | For your chosen product — practice the format until it's fluent | **Free** |

> **Kanban vs Scrum:** many teams (especially in startups) use Kanban (continuous flow, no sprints) rather than Scrum. The difference matters less than you think. Know both exist; know your team's process.

**Practice gate:** you can explain the difference between a product backlog and a sprint backlog, write a user story with acceptance criteria, and describe what happens in each of the four main Scrum ceremonies.

---

## Communication and Writing as the Core Skill (~20 hrs)

This section gets less glamorous billing than "discovery frameworks" or "prioritization techniques," but it's the most important section in Phase 1. Possibly in the entire guide.

### Why writing is the PM job

Every PM output is a document:
- PRDs and specs communicate what to build
- Roadmaps communicate what's coming and why
- Strategy memos communicate direction to leadership
- Stakeholder updates build alignment without meetings
- Interview answers that are written-quality thinking get offers

PMs who write clearly make their teams faster. Vague specs create rework. Unclear reasoning creates endless alignment meetings. The quality of your writing is a direct proxy for the quality of your thinking, and every PM interview knows this.

### What good PM writing looks like

- **Starts with the problem, not the solution.** "Users can't find their recent orders on mobile" before "add a recent orders widget to the mobile homepage."
- **States assumptions explicitly.** "This assumes our primary persona is a mobile-first user making repeat purchases."
- **Separates what from why.** The "why" (the problem and its importance) should be clear before any "what" (the solution) appears.
- **Has a clear "so what."** Every document should end with a decision, a next step, or a recommendation.
- **Is shorter than you think.** A one-page problem statement beats a 10-page spec nobody reads.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Write a one-page problem statement | Notion | For your chosen product: state the problem, who has it, why it matters, what success looks like | **Free** |
| Read 3 real PRD examples | Public PRDs on GitHub or product blogs | Search GitHub/product blogs for public PRDs; analyze structure, not content | **Free** |
| First draft PRD | Notion | Write a full PRD for one feature of your chosen product — it will be rough, that's fine | **Free** |
| Rewrite a vague requirement | Notion | Take a vague spec ("improve search") and rewrite it to be specific and measurable | **Free** |

**Practice gate:** you can write a one-page problem statement that starts with the user problem (not the solution), states the success metric, and makes its assumptions explicit — in under 30 minutes.

---

## Phase 1 exit checklist

- [ ] I can explain what a PM does and doesn't do, and distinguish PM from Product Owner
- [ ] I can map the full product lifecycle loop (discover → define → design → build → measure → learn) for a real product
- [ ] I know Scrum ceremonies, artifacts, and vocabulary well enough to participate on day one
- [ ] I've written 5+ user stories with acceptance criteria in Jira
- [ ] I've drafted a one-page problem statement and a first PRD for my chosen product
- [ ] I can explain why communication/writing is the core PM skill

Next: [Phase 2 — Core PM Skills →](02-core.md)
