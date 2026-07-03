# cloud & DevOps career roadmap: zero to first cloud role meow

> [!IMPORTANT]
> **read this first: "DevOps" is rarely a true entry-level job.**
> the honest on-ramp is **Cloud Support / Cloud Ops -> Junior Cloud Engineer -> DevOps Engineer**.
> this guide gets u hired into that first cloud role, then sets u up to grow into DevOps/SRE.

## how to track your progress meow

oki so u might notice all the `- [ ]` checkboxes in this guide... heres the thing: **these boxes are display-only in this public repo** - u cant actually tick them here.

**so use your own copy:**
- **fork this repo** and tick boxes in your fork, or
- **copy the checklist into Obsidian/OneNote/Notion**, or
- **download/print it** if paper works better.

the real progress signal is not the checkbox anyway. its whether the lab works, the project is reproducible, and u can explain what broke when cloud does cloud things qwq.

## todo map at a glance

- [ ] **Goal 0 - prep** - [00-prep.md](00-prep.md) (Day 1): honest path, accounts, free-tier setup.
- [ ] **Goal 1 - foundations** - [01-foundations.md](01-foundations.md) (~140h): Linux, networking, Git, scripting.
- [ ] **Goal 2 - cloud core + Docker** - [02-core.md](02-core.md) (~180h): one provider, IAM, VPC, compute, storage, containers.
- [ ] **Goal 3 - IaC + CI/CD** - [03-iac-cicd.md](03-iac-cicd.md) (~120h): Terraform/OpenTofu, pipelines, GitHub Actions.
- [ ] **Goal 4 - Kubernetes + specialization** - [04-kubernetes-specialization.md](04-kubernetes-specialization.md) (~160h): K8s, observability, one depth track.
- [ ] **Goal 5 - portfolio + job hunt** - [05-job-hunt.md](05-job-hunt.md) (~80h): proof projects, resume, role targeting.
- [ ] **After entry-level** - [beyond-entry.md](beyond-entry.md): SRE, platform, architecture, DevSecOps.

## how the hour system works

timelines are in **study hours**, not weeks.

| Your pace | 600 hours takes |
|---|---|
| 1 hr/day | ~20 months |
| 2 hrs/day | ~10 months |
| 4 hrs/day | ~5 months |
| 6 hrs/day (full-time) | ~3.5 months |

each goal is a budget, not a deadline. at **2 h/day**, this is roughly **10 months**. thats normal for cloud; the stack is wide.

## guide contents

| File | whats inside |
|---|---|
| [00-prep.md](00-prep.md) | mindset, honest career path, accounts, free-tier setup |
| [01-foundations.md](01-foundations.md) | Linux, networking, Git, Bash/Python scripting |
| [02-core.md](02-core.md) | one cloud provider deep, AWS-led: compute, storage, networking, IAM |
| [03-iac-cicd.md](03-iac-cicd.md) | Docker, Terraform/OpenTofu, CI/CD, GitHub Actions, GitOps |
| [04-kubernetes-specialization.md](04-kubernetes-specialization.md) | Kubernetes, observability, specialization tracks |
| [05-job-hunt.md](05-job-hunt.md) | portfolio projects, resume, finding and targeting roles |
| [beyond-entry.md](beyond-entry.md) | SRE, platform engineering, advanced tracks |
| [certifications.md](certifications.md) | cert matrix, ROI tiers, recommended paths |
| [labs.md](labs.md) | interactive lab inventory |
| [resources.md](resources.md) | channels, books, communities, roadmaps |
| [interview-prep.md](interview-prep.md) | technical + behavioral question bank |

## certification ladder

```text
[Foundation]      AWS Cloud Practitioner (CLF-C02) - or AZ-900 / GCP CDL
[Baseline]        AWS Solutions Architect Associate (SAA-C03) - the real hiring filter
[Differentiator]  Terraform Associate (TA-004) + CKA
[Later]           AWS DevOps Pro / specialty certs - after youre in-role
```

> **do not pursue AZ-204** (retiring July 2026) or **Docker DCA** (discontinued). see [certifications.md](certifications.md).

## what makes this guide different

- **honest on-ramp** - cloud support/ops first, DevOps later.
- **hour-based** - fits any schedule.
- **verified June 2026** - exam codes, prices, and tool versions checked against official sources.
- **region-agnostic** - no salary tables, no local job-board lists.
- **free-first** - AWS Free Tier, KillerCoda, Play with Docker, KodeKloud free tier, k3s/kind local labs.
- **current stack** - Kubernetes v1.36, Terraform v1.15 + OpenTofu, Helm v4, ArgoCD v3, OpenTelemetry.

---

*Last verified: June 2026. Prices, exam codes, and tool versions change - confirm with the provider before booking. Sources in [/research](../../research/).*
