# beyond entry-level - Cloud & DevOps meow

> youre hired into a cloud/ops role.
> this is the next-few-years map.
> dont chase all of it. pick a direction once youve seen what u enjoy on the job.

[Hub](README.md) - [Job Hunt](05-job-hunt.md)

---

- [ ] **understand the growth path**
- [ ] **compare the major tracks**
- [ ] **use advanced certs only when they match the role**
- [ ] **compound the senior skills**
- [ ] **stay current without burning out**
- [ ] **check if youve leveled up**

## growth path

```text
Cloud Support / Cloud Ops
  -> Cloud Engineer / DevOps Engineer
  -> SRE / Platform / Cloud Architect / DevSecOps
  -> Senior / Staff / Principal / Engineering Management
```

theres no single ladder. most people zig-zag.
the throughline: u shift from **running things** to **building the systems other engineers run things on**.

## major tracks

### site reliability engineering

reliability as engineering: SLOs/SLIs, error budgets, incident command, postmortems, capacity planning, and code to eliminate toil.

- [ ] **learn:** Google SRE books, OpenTelemetry, Prometheus, Grafana, chaos engineering
- [ ] **signal:** define an SLO, run an incident, write a blameless postmortem

### platform engineering

build the internal developer platform so product teams can self-serve. this is the shift from "DevOps does everything" to "we build paved roads."

- [ ] **learn:** Backstage, golden-path templates, self-service provisioning, developer experience
- [ ] **signal:** developers ship without filing u a ticket

### cloud architecture

design the whole system: multi-account strategy, networking, cost, security, well-architected trade-offs.

- [ ] **learn:** professional-level cloud certs, well-architected frameworks, FinOps
- [ ] **signal:** justify cost, reliability, and security trade-offs to leadership

### DevSecOps / cloud security

shift security left: scanning in pipelines, supply-chain security, secrets, policy-as-code, runtime security.

- [ ] **learn:** Trivy/Snyk, OPA/Gatekeeper, Sigstore/SLSA, CKS, cloud-security certs
- [ ] **signal:** security is a pipeline stage, not a gate at the end

## certs that finally pay off

| Cert | Track | When |
|---|---|---|
| AWS DevOps Engineer **Pro** (DOP-C02) | DevOps/Cloud | 1-2 years in, after associate certs |
| AWS Solutions Architect **Pro** | Architecture | when designing systems |
| **CKA -> CKS** | K8s/Platform/Security | once u operate clusters daily |
| Azure **AZ-104 -> Solutions Architect Expert** | Azure shops | progression past support |
| FinOps Certified Practitioner | Cost/Architecture | when u own a cloud bill |

professional-tier certs that were premature for the first job become useful here. still: real systems > another badge.

## skills that compound

- [ ] **code, not clicks** - reusable IaC/automation modules
- [ ] **distributed systems thinking** - consensus, queues, idempotency, failure modes
- [ ] **cost ownership** - engineers who lower the bill get noticed
- [ ] **writing** - design docs, postmortems, runbooks
- [ ] **mentoring and on-call leadership** - senior path runs through making others better

## staying current without burning out

- [ ] follow CNCF project graduations
- [ ] track annual State of DevOps / DORA report
- [ ] build one small project on a new tool instead of bookmarking ten articles
- [ ] use AI for IaC generation, log summaries, incident summaries, and pipeline assist, but keep debugging judgment

## how to know youve leveled up

- [ ] trusted to own an incident end to end
- [ ] other engineers use infra/tooling u built
- [ ] can argue a design trade-off with cost + reliability + security numbers
- [ ] mentor the next junior through first on-call
- [ ] picked a track and are going deep

---

*Last reviewed: June 2026.*
