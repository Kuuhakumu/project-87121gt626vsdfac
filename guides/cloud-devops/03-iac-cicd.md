# 🔧 Phase 3: Infrastructure as Code & CI/CD

> **~120 hrs total** · your pace, no deadline
> This is the heart of DevOps: stop clicking in consoles, start defining everything as code. IaC + CI/CD is the #1 hireable DevOps skill combination.

[← Phase 2: Cloud Core](02-core.md) · [Hub](README.md) · [Next: Phase 4 →](04-kubernetes-specialization.md)

---

## Infrastructure as Code (Terraform / OpenTofu) (~70 hrs)

IaC means your infrastructure (servers, networks, databases) is defined in version-controlled files — not hand-built by clicking through a console. It's reproducible, reviewable, and the backbone of every DevOps role.

### Terraform vs OpenTofu — what to know in 2026
- **Terraform** (HashiCorp, now IBM) is the dominant tool in enterprise. Current v1.15. Uses the BSL license since 2023.
- **OpenTofu** is the fully open-source (MPL-2) fork, now CNCF-adopted and at feature parity (v1.12). It's a drop-in replacement — the language (HCL) is identical.
- **For learning, they're interchangeable.** Learn the concepts on either; most tutorials work for both. OpenTofu is the safe open default; Terraform is what most job postings still name.

### What to cover
- HCL syntax: providers, resources, variables, outputs, data sources
- **State**: what `terraform.tfstate` is, why it matters, remote state (S3 + DynamoDB lock), never commit state to Git
- The core workflow: `init` → `plan` → `apply` → `destroy` (**always `plan` before `apply`**)
- **Modules**: reusable infrastructure components
- Provisioners, `count`/`for_each`, dependencies
- Secrets handling (don't hardcode — use variables + a secrets manager)

> **Also know configuration management exists:** **Ansible** (the top tool — agentless, YAML playbooks) configures servers *after* they exist, where Terraform *provisions* them. Learn Ansible basics after Terraform.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [HashiCorp Tutorials](https://developer.hashicorp.com/terraform/tutorials) | Official | Guided Terraform from zero to modules + remote state | **Free** |
| Terraform labs | [KodeKloud](https://kodekloud.com/) | Hands-on HCL, state, modules (free tier) | Freemium |
| [KillerCoda Terraform](https://killercoda.com/) | Web | Live-terminal Terraform scenarios | **Free** |

**Cert:** **HashiCorp Terraform Associate (TA-004, ~$70)** — cheap, high-signal, IaC fluency proof. Strongly recommended.

**Project:** provision a complete environment with Terraform — VPC + subnets + an EC2 instance (or equivalent) + security groups — using **modules** and **remote state**. Zero console clicks. Put it on GitHub.

---

## CI/CD pipelines (~50 hrs)

CI/CD automates the path from `git push` to running software — build → test → deploy — so humans aren't in the loop for every release.

### What to cover
- **CI (Continuous Integration):** on every push, automatically lint, build, and run tests
- **CD (Continuous Delivery/Deployment):** automatically ship to staging/prod (with gates)
- Pipeline stages, jobs, runners, artifacts, caching, secrets in pipelines
- **GitHub Actions** (the entry-level standard — learn this first): workflow YAML, triggers, jobs, marketplace actions
- GitLab CI as the main alternative; Jenkins exists in enterprise (legacy but common)
- Deployment strategies: blue-green, canary, rolling
- Integrating it all: pipeline builds a Docker image → pushes to registry → deploys

> **2026 note:** GitHub Actions is the default for new projects and the best first thing to learn. Jenkins is worth recognizing (lots of enterprise uses it) but don't start there.

### Labs / theory

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [GitHub Skills](https://skills.github.com/) | GitHub | Guided Actions courses inside real repos | **Free** |
| [GitHub Actions docs](https://docs.github.com/actions) | Official | Build your first workflow step by step | **Free** |
| GitLab CI/CD tutorials | [GitLab Docs](https://docs.gitlab.com/ee/ci/) | Build a `.gitlab-ci.yml` pipeline | **Free** |

**Project (portfolio centerpiece):** build a full pipeline for your containerized app from Phase 2:
`push → lint → test → build Docker image → push to registry → deploy to a cloud service or k8s namespace → smoke test`. Document it with a diagram in the README.

---

## Phase 3 exit checklist
- [ ] Can write Terraform/OpenTofu to provision real infrastructure using modules + remote state
- [ ] Terraform Associate cert passed (recommended)
- [ ] Understand the difference between provisioning (Terraform) and config management (Ansible)
- [ ] Can write a working GitHub Actions pipeline from scratch
- [ ] Built an end-to-end pipeline: push → test → build image → deploy
- [ ] Both projects on GitHub with architecture diagrams

Next: [Phase 4 — Specialization (Kubernetes & beyond) →](04-kubernetes-specialization.md)
