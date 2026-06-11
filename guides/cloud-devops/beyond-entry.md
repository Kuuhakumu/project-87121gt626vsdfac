# 🚀 Beyond Entry-Level — Cloud & DevOps (Years 2+)

> You're hired into a cloud/ops role. This is the map for the next few years.
> Don't chase all of it — pick a direction once you've seen what you enjoy on the job.

[← Hub](README.md) · [Job Hunt](05-job-hunt.md)

---

## The growth path (recap + forward)

```
Cloud Support / Cloud Ops  (your first job)
        ↓  1–2 yr: own IaC, pipelines, incidents
Cloud Engineer / DevOps Engineer
        ↓  pick a depth
   ┌────────────┬───────────────┬──────────────┐
   ↓            ↓               ↓              ↓
   SRE     Platform Eng     Cloud         DevSecOps
        (IDP/Backstage)   Architect
        ↓
Senior / Staff / Principal · Engineering Management
```

There's no single ladder — most people zig-zag. The throughline: **you shift from "running things" to "building the systems other engineers run things on."**

---

## The major tracks

### Site Reliability Engineering (SRE)
Reliability as an engineering discipline — SLOs/SLIs, error budgets, incident command, postmortems, capacity planning, and writing code to eliminate toil.
- **Learn:** the Google SRE books (free at sre.google/books), deep observability (OTel/Prometheus/Grafana), chaos engineering.
- **Signal:** you can define an SLO, run an incident, and write a blameless postmortem.

### Platform Engineering
Build the **internal developer platform (IDP)** so product teams can self-serve. It's the biggest framing shift in the field — "the DevOps team does everything" → "we build paved roads."
- **Learn:** Backstage, golden-path templates, self-service provisioning, developer-experience thinking.
- **Signal:** developers ship without filing you a ticket.

### Cloud Architecture
Design the whole system: multi-account/org strategy, networking, cost, security, well-architected trade-offs.
- **Learn:** AWS/Azure/GCP Professional-level certs (now they're worth it), well-architected frameworks, FinOps.
- **Signal:** you can justify a design's cost, reliability, and security trade-offs to leadership.

### DevSecOps / Cloud Security
Shift security left: scanning in pipelines, supply-chain security, secrets, policy-as-code, runtime security.
- **Learn:** Trivy/Snyk, OPA/Gatekeeper, Sigstore/SLSA, CKS, cloud-security certs.
- **Signal:** security is a pipeline stage, not a gate at the end.

---

## Certs that finally pay off (Years 2+)

| Cert | Track | When |
|---|---|---|
| AWS DevOps Engineer **Pro** (DOP-C02) | DevOps/Cloud | 1–2 yr in, after associate certs |
| AWS Solutions Architect **Pro** | Architecture | when designing systems |
| **CKA → CKS** | K8s/Platform/Security | once you operate clusters daily |
| Azure **AZ-104 → Solutions Architect Expert** | Azure shops | progression past support |
| FinOps Certified Practitioner | Cost/Architecture | when you own a cloud bill |

> Professional-tier certs that were *premature* for your first job become genuine differentiators here. (Still: a real system you built and operate > another cert.)

---

## Skills that compound

- **Code, not clicks** — your IaC/automation should be reusable modules, not one-offs.
- **Distributed systems thinking** — consensus, queues, idempotency, failure modes.
- **Cost ownership (FinOps)** — engineers who lower the bill get noticed fast.
- **Writing** — design docs, postmortems, runbooks. Senior is as much writing as YAML.
- **Mentoring & on-call leadership** — the path to senior/staff runs through making others better.

---

## Staying current without burning out

- Follow **CNCF** project graduations — they signal what's becoming standard.
- Track the **annual State of DevOps / DORA report** — the four key metrics (deploy frequency, lead time, change-fail rate, MTTR) are how teams measure you.
- One small project on a new tool beats ten bookmarked articles.
- **AIOps:** use AI for IaC generation, log/incident summarization, and pipeline assist — but keep your ability to read and debug what it produces. Judgment is the durable skill.

---

## How to know you've leveled up

- [ ] You're trusted to own an incident end to end
- [ ] Other engineers use infra/tooling you built
- [ ] You can argue a design trade-off with cost + reliability + security numbers
- [ ] You mentor the next junior through their first on-call
- [ ] You've picked a track (SRE / Platform / Architecture / Security) and are going deep

---

*The first job is the hard part — you've done it. From here, depth and ownership compound. Last reviewed: June 2026.*
