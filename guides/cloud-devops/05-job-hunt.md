# 💼 Phase 5: Portfolio, Resume & Job Hunt

> **~80 hrs total** · your pace, no deadline
> Build the portfolio *as you learn* — don't wait until the end.

[← Phase 4](04-kubernetes-specialization.md) · [Hub](README.md) · [Beyond Entry-Level →](beyond-entry.md)

---

## The honest entry reality (read this first)

**"DevOps Engineer" is rarely a true entry-level role.** It bridges development and operations — which means it assumes you already know one of them. Postings titled just "DevOps Engineer" almost always want 2+ years.

The realistic on-ramp:

```
Cloud Support Associate / Cloud Ops Analyst / IT role with cloud exposure
   (6–18 mo: learn cloud in production, scripting, tickets, incident response)
        ↓
Junior Cloud Engineer / Junior DevOps Engineer / Associate Cloud Engineer
   (1–2 yr: IaC, CI/CD, containers, automation projects)
        ↓
Cloud Engineer / DevOps Engineer / Platform Engineer  (2–4 yr)
        ↓
SRE / Senior Platform Engineer / Cloud Architect  (4+ yr)
```

Target the **first row** for your first job. A "Cloud Support" role isn't a consolation prize — it's the standard, employer-built entry door into this field.

---

## GitHub portfolio

In cloud/DevOps, **a deployed, reproducible project beats a pile of certs**. Each repo needs:
- A clear `README`: what it does, an architecture diagram, how to run it, what you'd improve
- **All infrastructure as code** — if someone can't `terraform apply` (or `tofu apply`) and reproduce it, it doesn't count
- A pipeline file (GitHub Actions YAML) showing build → test → deploy
- Screenshots or a short walkthrough

### Project ideas by track

| Track | Signature portfolio project |
|---|---|
| Cloud | Multi-tier app deployed via console, then fully rebuilt in Terraform/OpenTofu |
| Platform/IaC | Entire K8s cluster + app provisioned with IaC only, reusable modules |
| CI/CD | Full pipeline: lint → test → build → push → deploy to staging → promote to prod, GitOps with ArgoCD |
| SRE | OTel → Prometheus → Grafana observability stack with a working SLO + alert |
| DevSecOps | Pipeline with Trivy image scanning, secret scanning, SAST, and managed secrets |

> **Quality > quantity.** One reproducible, observable, IaC-provisioned app with a real pipeline beats ten console-clicked screenshots.

---

## Resume & profiles

- **Lead with projects + certs**, then skills, then any experience
- **Quantify:** "Provisioned a 3-node K8s cluster via Terraform", "Built a CI/CD pipeline cutting deploy time from X to Y"
- **Mirror posting keywords** for ATS — if it says "Terraform, AWS, CI/CD, Kubernetes", those exact words must appear (truthfully)
- Link your GitHub; pin the IaC/pipeline repos
- **Headline example:** `Aspiring Cloud Engineer | AWS SAA | Terraform & Kubernetes labs`

---

## Job titles to search for

True-entry (target these):
- Cloud Support Associate / Cloud Support Engineer
- Junior Cloud Engineer · Associate Cloud Engineer
- Cloud Operations Analyst

Borderline (achievable after the above, or with strong projects):
- Junior DevOps Engineer / DevOps Engineer I
- Infrastructure Engineer

> Avoid anchoring on unleveled "DevOps Engineer", "Platform Engineer", or "SRE" for a *first* job — those almost always want experience.

---

## How to find and target roles (region-agnostic)

Job boards are mostly local, so use a strategy that travels:

1. **The cloud providers themselves hire entry-level.** AWS, Microsoft, and Google all run structured Cloud Support programs that hire from near-zero experience — and MSPs/consultancies hire in volume.
2. **Company-direct.** Build a list of 20–40 target employers (cloud-native startups, MSPs, consultancies, any enterprise with a cloud team) and check their careers pages directly.
3. **Referrals beat cold applications.** Engage in communities (see [resources.md](resources.md)), contribute to open-source infra tools, connect with people doing the work.
4. **Filter for remote** if your local market is thin — cloud/DevOps is one of the more remote-friendly fields.
5. **Tailor every application** — lead with the one project most relevant to that stack.

---

## Interview prep

See the full **[Interview Prep Q&A bank →](interview-prep.md)** — ~25 technical questions (Linux, networking, cloud, Docker, K8s, CI/CD, IaC) + behavioral prompts.

### Quick hits — questions you *will* be asked
- A pod is in `CrashLoopBackOff` — walk me through diagnosing it
- IAM roles vs IAM users — when do you use each?
- `terraform plan` vs `apply` — why always plan first? What is state and what breaks it?
- A broken Dockerfile / a container that exits immediately — debug it
- Describe a CI/CD pipeline from `git push` to production
- Reverse proxy vs load balancer — real use case for each

### Behavioral (STAR)
- "Something you deployed broke in production — what did you do?"
- "A manual process you automated — what was the impact?"
- "A new technology you had to learn fast"

Next: [Beyond Entry-Level — Years 2+ →](beyond-entry.md)
