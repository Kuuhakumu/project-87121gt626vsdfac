# 🔀 Phase 3: Specialization Tracks

> **~100 hrs total** · your pace, no deadline
> The PM role branches. Pick the track that fits where you want to work — or where the jobs are.

[← Phase 2](02-core.md) · [Hub](README.md) · [Next: Phase 4 — Portfolio →](04-projects.md)

---

## Which track?

Most PM job families share the same Phase 1–2 foundation. Specialization is about depth — going deep enough in one area to be credibly hired into that flavor of PM work.

| Track | Best if you… | Entry difficulty |
|---|---|---|
| **Growth PM** | Like experiments, metrics, and acquisition/retention loops | 🟠 Moderate — needs analytics depth |
| **Technical PM** | Come from engineering or have strong eng literacy | 🟡 Accessible with the right background |
| **B2B / Enterprise PM** | Like complex stakeholder management, sales cycles, configurability | 🟢 Accessible — especially with sales/CS background |
| **AI PM** | Want to work on ML/LLM products; the emerging high-demand track | 🟠 Moderate — needs ML conceptual literacy |

> You don't have to pick one forever. Specializations are where you start, not where you stay. Many PMs cross over after their first role.

---

## Track A: Growth PM

### What it is

Growth PMs are responsible for the metrics that drive product adoption, activation, retention, and monetization. They run the experiment pipeline — generating hypotheses, designing tests, reading results, shipping winners.

Growth PM is different from marketing. A Growth PM works inside the product: improving onboarding flows, reducing friction at key steps, testing copy or UI changes that drive behavior. They partner with a growth engineer or full-stack engineer, often in a small "growth team" that operates semi-independently.

### What to go deep on

- **Growth accounting:** new users, retained users, resurrected users, churned users. Know the formulas.
- **Funnel analysis:** where do users drop off between acquisition and activation? Between activation and habit formation?
- **Experiment design:** power analysis (why small samples give misleading results), holdout groups, novelty effect, network effects that break A/B tests.
- **SQL and product analytics:** Growth PMs run their own queries. Fluency with Amplitude, Mixpanel, or a BI tool is expected. Basic SQL is required.
- **Growth loops vs funnels:** Sean Ellis / Andrew Chen's framework — viral loops, content loops, paid loops. Understanding which loop your product has (or needs) shapes what experiments you run.

### Signature deliverable

A structured **growth experiment backlog**: 20 growth hypotheses for a real product, each framed as "we believe [action] will increase [metric] by [expected lift] because [rationale]," prioritized by ICE score, with a measurement plan.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Amplitude funnel + retention analysis | Amplitude free tier | Build a funnel from signup to first key action; identify the top drop-off; write the hypothesis for fixing it | **Free** |
| SQL funnel query | DataLemur or Mode | Write a SQL query that shows step-by-step conversion through a multi-step funnel | **Free** |
| Growth experiment log | Notion | 20 growth hypotheses for your running product, ICE-scored and ranked | **Free** |
| Read "Reforge Growth Series" intros | reforge.com | Free articles on growth frameworks (full cohorts are paid, but the reading is useful) | **Free** tier |

### Resources

- *Hacking Growth* — Sean Ellis & Morgan Brown (the canonical growth playbook)
- Andrew Chen's essays at [andrewchen.com](https://andrewchen.com) — free and comprehensive
- Lenny's Newsletter has excellent growth PM content in the free tier

**Practice gate:** you can build a funnel analysis in Amplitude, identify the top drop-off step, write a growth hypothesis, and explain what sample size you'd need to detect a 5% lift with 95% confidence.

---

## Track B: Technical PM

### What it is

Technical PMs work on products with complex engineering surfaces: APIs, developer tools, infrastructure, platforms, data pipelines, or hardware. They're the bridge between engineering teams and product/business direction.

This doesn't mean writing code. It means you can read architecture diagrams, understand what's technically hard vs easy, speak credibly with engineers about tradeoffs, and write specs that don't need to be fully re-explained by a tech lead before they're actionable.

> Technical PM is the most credible on-ramp for software engineers who want to move into PM. If you have an engineering background, this is your natural track.

### What to go deep on

- **System design literacy:** HTTP, APIs (REST vs GraphQL), databases, caching, queues, microservices. Not building them — understanding them well enough to ask the right questions.
- **SQL:** a Technical PM who can query their own data has a real edge.
- **API product thinking:** if your product has a public API, what does developer experience mean? How do you version an API without breaking integrations? What does "ease of integration" mean concretely?
- **Platform thinking:** internal platforms (infra, data, auth) have internal customers. How do you discover their problems when they're inside your company?
- **Technical debt tradeoffs:** how do you make the case for investing in refactors alongside feature work? How do you measure the cost of not doing it?

### Signature deliverable

A **technical product spec** for a real API or developer-facing feature: background, API design considerations, backward compatibility requirements, error handling and edge cases, versioning strategy, and a rollout plan.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| SQL practice (PM-level) | DataLemur free tier | Solve 10 medium SQL problems; practice the queries you'd run to diagnose a metric drop | **Free** |
| Read an API reference | Any public API docs (Stripe, Twilio, GitHub) | Read the API docs as if you were the PM who owns it — identify what's missing or confusing | **Free** |
| System design intro | ByteByteGo YouTube / blog | Watch 5 system design explainer videos; identify 3 design decisions that a PM needs to understand | **Free** |
| Write a technical spec | Notion | One feature with: current system behavior, proposed change, edge cases, rollback plan | **Free** |

### Resources

- *Inspired* — Marty Cagan (chapters on technical leadership and working with engineering)
- ByteByteGo newsletter and YouTube: system design made accessible
- Stripe's API docs: the gold standard for developer-facing product — read them as a PM

**Practice gate:** you can read a basic system architecture diagram, identify 3 product-relevant tradeoffs in it, and write a technical spec that a senior engineer wouldn't have to substantially rewrite.

---

## Track C: B2B / Enterprise PM

### What it is

B2B PMs build products sold to businesses, not consumers. The differences from B2C are real:
- **Your buyer ≠ your user.** The VP of Sales buys the CRM; the sales rep uses it. You need to satisfy both.
- **Sales and CS are stakeholders.** What features do deals hinge on? What makes customers churn?
- **Configuration > personalization.** Enterprise customers want to customize workflows, roles, permissions, integrations. You build for flexibility.
- **Contracts and SLAs.** Enterprise customers have compliance requirements, security reviews, and uptime expectations baked into contracts.
- **Long sales cycles.** A feature might need to exist on a roadmap for 6 months before a deal closes on it.

### What to go deep on

- **The jobs-to-be-done of both the buyer and the user** — often in tension
- **Integrations and ecosystem:** enterprise products must plug into the customer's existing stack (SSO, SCIM, CRM, ERP)
- **Tiering and packaging:** how do you structure features across Free / Pro / Enterprise tiers without undermining upsell?
- **NPS and churn signals:** customer success data is your discovery input
- **Compliance basics:** SOC 2, GDPR, accessibility (WCAG) — a B2B PM needs to know what these mean for product decisions even if they don't own them

### Signature deliverable

A **B2B feature proposal** that addresses a real enterprise customer need: the buyer's problem, the user's problem (if different), the feature's impact on deal velocity or retention, the configuration requirements, and the rollout considerations for existing customers.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Enterprise feature teardown | Notion | Pick a B2B product (Salesforce, HubSpot, Notion for Teams, Jira Premium); document 5 features that exist specifically because of enterprise customers | **Free** |
| Tier and packaging analysis | Notion + Google Sheets | Map the pricing tiers of 2 competing B2B products; identify what features are gated at which tier and why | **Free** |
| Write a B2B PRD | Notion | For a hypothetical enterprise feature; include buyer vs user distinction and integration requirements | **Free** |
| Read "Building for Enterprise" (Lenny's) | lennysnewsletter.com | How B2B PM differs from consumer PM | **Free** tier |

**Practice gate:** you can write a B2B feature proposal that distinguishes the buyer's and user's jobs, identifies the integration requirements, and estimates the deal-velocity or retention impact.

---

## Track D: AI PM

### What it is

AI PM is an emerging specialization with genuine demand. You own products built on ML models, LLMs, or AI-powered features. The role is part traditional PM (discovery, prioritization, specs) and part ML literacy (understanding what models can and can't do, how they fail, how to evaluate them).

> The AI PM specialization is trending upward — most companies are now building AI features and need PMs who can navigate the ambiguity of non-deterministic systems. This is not a hype claim; it's directional. Verify the current state of specific job markets when you apply.

### What to go deep on

- **LLM product basics:** what prompting is, what RAG is (retrieval-augmented generation), what fine-tuning means and when it's warranted, what latency and cost tradeoffs look like.
- **Evaluation of non-deterministic systems:** how do you test a feature whose output varies? What does "good enough" mean for an LLM response? Hallucination, bias, and safety as product risks.
- **ML model lifecycle:** training, deployment, monitoring for drift. Not building it — understanding when to flag "the model needs retraining."
- **AI product ethics:** what does it mean to deploy a biased model? How do you build user trust in an AI feature? When do you *not* use AI?
- **Responsible AI frameworks:** most large companies have one. Know what's in it and how it affects product decisions.

### Signature deliverable

An **AI feature evaluation framework** for a real or hypothetical feature: the problem being solved, the model type (classification / generation / recommendation), the success metrics, the failure modes, the human review threshold, and the rollout strategy.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Use the Anthropic / OpenAI API | Anthropic or OpenAI playground | Build a simple prompt-based feature (summarizer, classifier, FAQ bot); document where it fails | **Free** tier |
| Evaluate an LLM feature | Notion | Define 5 evaluation criteria for a real AI product feature; score 10 sample outputs against them | **Free** |
| Read "AI PM Guide" (Lenny's) | lennysnewsletter.com | Practitioner breakdown of what AI PM requires vs regular PM | **Free** tier |
| DeepLearning.AI short courses (LLM intro) | deeplearning.ai/short-courses | 1–2 hour courses on LLM basics and prompt engineering — just enough ML literacy | **Free** |

### Resources

- DeepLearning.AI short courses (free): build the ML literacy without a math degree
- Hugging Face model cards — practice reading them to understand what a model does and doesn't do
- "AI and PM" content on Lenny's Newsletter and Reforge

**Practice gate:** you can explain what RAG is, why it matters for AI products, write an evaluation rubric for an LLM feature, and describe three failure modes that a PM (not an engineer) needs to own.

---

## Phase 3 exit checklist

- [ ] I have chosen one specialization track and can explain why it fits my background and target companies
- [ ] I completed the signature deliverable for my track
- [ ] I've done the core labs for my track
- [ ] I can answer a specialization-specific interview question (growth experiment design, technical architecture tradeoff, B2B buyer-vs-user distinction, or AI evaluation rubric)
- [ ] I have identified 3–5 target companies that hire my specialization

Next: [Phase 4 — Portfolio →](04-projects.md)
