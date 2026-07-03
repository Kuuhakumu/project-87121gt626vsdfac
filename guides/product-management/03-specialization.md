# Goal 3: pick your PM track meow

> **~100h total** - your pace, no deadline.
> goal: choose the flavor of PM that fits your background, target companies, and skill gaps.

[Previous: Goal 2](02-core.md) - [Hub](README.md) - [Next: Goal 4](04-projects.md)

---

- [ ] **choose a track**
- [ ] **Track A: Growth PM**
- [ ] **Track B: Technical PM**
- [ ] **Track C: B2B / Enterprise PM**
- [ ] **Track D: AI PM**
- [ ] **exit check** - track chosen, signature deliverable done, target companies identified

## choose a track

most PM job families share the same Goal 1-2 foundation.
specialization is depth: enough evidence that u can be hired into that flavor of PM work.

| Track | Best if u... | Entry difficulty |
|---|---|---|
| **Growth PM** | like experiments, metrics, acquisition, retention | moderate, needs analytics depth |
| **Technical PM** | come from engineering or have strong engineering literacy | accessible with the right background |
| **B2B / Enterprise PM** | like stakeholders, sales cycles, configurability | accessible, especially with sales/CS background |
| **AI PM** | want ML/LLM products and emerging demand | moderate, needs ML conceptual literacy |

u dont have to pick one forever.
specializations are where u start, not where u stay.

## track A: growth PM

### what it is

Growth PMs own metrics that drive adoption, activation, retention, and monetization.
they run the experiment pipeline: hypotheses, tests, results, winners.

Growth PM is not marketing.
a Growth PM works inside the product: onboarding flows, friction reduction, copy/UI tests, behavior change.
they often partner with a growth engineer in a semi-independent growth team.

### go deep on this

- [ ] **Growth accounting:** new users, retained users, resurrected users, churned users.
- [ ] **Funnel analysis:** where users drop from acquisition to activation to habit.
- [ ] **Experiment design:** sample size, holdouts, novelty effect, network effects.
- [ ] **SQL and analytics:** Amplitude, Mixpanel, BI tools, basic SQL.
- [ ] **Growth loops vs funnels:** viral loops, content loops, paid loops.

**signature deliverable:** a growth experiment backlog with 20 hypotheses for a real product.
each should say: "we believe [action] will increase [metric] by [expected lift] because [rationale]."
prioritize by ICE and include a measurement plan.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Amplitude funnel + retention analysis | Amplitude free tier | build signup -> first key action funnel, identify drop-off, write a hypothesis | **Free** |
| SQL funnel query | DataLemur or Mode | write a SQL query showing step-by-step conversion through a funnel | **Free** |
| Growth experiment log | Notion | write 20 ICE-scored hypotheses for your running product | **Free** |
| Reforge Growth Series intros | Reforge | read free growth framework intros - ⚠️ TODO verify exact article links | **Free** tier |

### resources

- *Hacking Growth* by Sean Ellis and Morgan Brown
- [Andrew Chen essays](https://andrewchen.com) - ⚠️ TODO verify exact starter essays
- Lenny's Newsletter growth PM content - ⚠️ TODO verify exact starter articles

**practice gate:** u can build a funnel in Amplitude, identify top drop-off, write a growth hypothesis, and explain what sample size u need to detect a 5% lift with 95% confidence.

## track B: technical PM

### what it is

Technical PMs work on products with complex engineering surfaces: APIs, developer tools, infrastructure, platforms, data pipelines, or hardware.
they bridge engineering teams and product/business direction.

this doesnt mean writing code.
it means u can read architecture diagrams, understand hard vs easy tradeoffs, speak credibly with engineers, and write specs that dont need a tech lead to rewrite them.

Technical PM is the most credible on-ramp for software engineers moving into PM.
if u have engineering background, this is your natural track.

### go deep on this

- [ ] **System design literacy:** HTTP, APIs, REST vs GraphQL, databases, caching, queues, microservices.
- [ ] **SQL:** query your own data and diagnose metric drops.
- [ ] **API product thinking:** developer experience, versioning, integration friction.
- [ ] **Platform thinking:** internal platforms have internal customers too.
- [ ] **Technical debt tradeoffs:** make the case for refactors alongside feature work.

**signature deliverable:** a technical product spec for a real API or developer-facing feature: background, API design considerations, backwards compatibility, error handling, edge cases, versioning, rollout.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| SQL practice | DataLemur free tier | solve 10 medium SQL problems and practice metric-drop queries | **Free** |
| Read an API reference | public API docs | read Stripe, Twilio, or GitHub docs as the PM owner and identify confusing gaps | **Free** |
| System design intro | ByteByteGo YouTube / blog | watch 5 system design explainers and identify 3 PM-relevant decisions - ⚠️ TODO verify exact videos/articles | **Free** |
| Technical spec | Notion | write one feature spec with current behavior, proposed change, edge cases, rollback plan | **Free** |

### resources

- *Inspired* by Marty Cagan, especially engineering partnership sections
- ByteByteGo newsletter and YouTube - ⚠️ TODO verify exact starter resources
- Stripe API docs as a developer-facing product reference

**practice gate:** u can read a basic architecture diagram, identify 3 product-relevant tradeoffs, and write a technical spec a senior engineer would not need to rewrite.

## track C: B2B / enterprise PM

### what it is

B2B PMs build products sold to businesses.
the differences from B2C are real:

- [ ] **buyer != user** - VP buys the CRM, sales rep uses it.
- [ ] **sales and CS are stakeholders** - deals and churn create product signal.
- [ ] **configuration beats personalization** - workflows, roles, permissions, integrations.
- [ ] **contracts and SLAs** - compliance, security, uptime expectations.
- [ ] **long sales cycles** - a roadmap item may affect a deal months before it ships.

### go deep on this

- [ ] buyer and user JTBD, often in tension
- [ ] integrations and ecosystem: SSO, SCIM, CRM, ERP
- [ ] tiering and packaging across Free / Pro / Enterprise
- [ ] NPS and churn signals from customer success
- [ ] compliance basics: SOC 2, GDPR, WCAG

**signature deliverable:** a B2B feature proposal for a real enterprise need: buyer problem, user problem, deal velocity or retention impact, configuration requirements, rollout considerations.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Enterprise feature teardown | Notion | pick Salesforce, HubSpot, Notion for Teams, or Jira Premium; document 5 enterprise-specific features | **Free** |
| Tier and packaging analysis | Notion + Sheets | compare pricing tiers of 2 B2B products and explain feature gating | **Free** |
| B2B PRD | Notion | write a PRD with buyer/user distinction and integration requirements | **Free** |
| "Building for Enterprise" | Lenny's Newsletter | read how B2B PM differs from consumer PM - ⚠️ TODO verify exact article link | **Free** tier |

**practice gate:** u can write a B2B proposal that distinguishes buyer and user jobs, identifies integrations, and estimates deal-velocity or retention impact.

## Track D: AI PM

### what it is

AI PM is an emerging specialization with real demand.
u own products built on ML models, LLMs, or AI-powered features.
the role is traditional PM plus ML literacy: what models can and cant do, how they fail, and how to evaluate them.

this is directional, not a hype guarantee.
verify specific job markets when u apply.

### go deep on this

- [ ] **LLM basics:** prompting, RAG, fine-tuning, latency, cost.
- [ ] **Non-deterministic evaluation:** outputs vary. define "good enough."
- [ ] **Failure risks:** hallucination, bias, safety, trust.
- [ ] **ML lifecycle:** training, deployment, drift monitoring.
- [ ] **Responsible AI frameworks:** know how they affect product decisions.

**signature deliverable:** an AI feature evaluation framework: problem, model type, success metrics, failure modes, human review threshold, rollout strategy.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Use Anthropic / OpenAI API | Anthropic or OpenAI playground | build a simple prompt feature, like summarizer/classifier/FAQ bot, and document failures | **Free** tier |
| Evaluate an LLM feature | Notion | define 5 criteria and score 10 sample outputs | **Free** |
| "AI PM Guide" | Lenny's Newsletter | read what AI PM requires vs regular PM - ⚠️ TODO verify exact article link | **Free** tier |
| DeepLearning.AI short courses | [deeplearning.ai/short-courses](https://www.deeplearning.ai/short-courses/) | take 1-2 hour LLM intro courses - ⚠️ TODO verify exact course names | **Free** |

### resources

- DeepLearning.AI short courses for ML literacy
- Hugging Face model cards to practice reading model capabilities and limits
- AI + PM content on Lenny's Newsletter and Reforge - ⚠️ TODO verify exact starter links

**practice gate:** u can explain RAG, why it matters for AI products, write an LLM evaluation rubric, and describe 3 PM-owned failure modes.

## exit check

- [ ] i chose one specialization track and can explain why it fits my background and target companies
- [ ] i completed the signature deliverable for my track
- [ ] i did the core labs for my track
- [ ] i can answer one specialization-specific interview question
- [ ] i identified 3-5 target companies that hire my specialization

[Next: Goal 4 - PM Portfolio](04-projects.md)
