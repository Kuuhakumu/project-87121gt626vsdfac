# Goal 5: portfolio, resume, and job hunt meow

> **~80h total** - your pace, no deadline.
> build the portfolio *as u learn*. dont wait until the end.

[Previous: Goal 4](04-kubernetes-specialization.md) - [Hub](README.md) - [Beyond Entry-Level](beyond-entry.md)

---

- [ ] **understand the entry reality**
- [ ] **build a cloud/DevOps GitHub portfolio**
- [ ] **write resume and profiles**
- [ ] **target realistic titles**
- [ ] **find roles without relying on local job-board lists**
- [ ] **prep interviews**

## understand the entry reality

**"DevOps Engineer" is rarely a true entry-level role.**
it bridges development and operations, so it assumes u already know one side.

```text
Cloud Support Associate / Cloud Ops Analyst / IT role with cloud exposure
  -> Junior Cloud Engineer / Junior DevOps Engineer / Associate Cloud Engineer
  -> Cloud Engineer / DevOps Engineer / Platform Engineer
  -> SRE / Senior Platform Engineer / Cloud Architect
```

target the first row for your first job. Cloud Support is the standard employer-built entry door into this field.

## GitHub portfolio

in cloud/DevOps, a deployed, reproducible project beats a pile of certs.

each repo needs:

- [ ] clear `README`: what it does, architecture diagram, how to run it, what youd improve
- [ ] all infrastructure as code
- [ ] reproducible `terraform apply` or `tofu apply` path where relevant
- [ ] pipeline file: GitHub Actions YAML showing build -> test -> deploy
- [ ] screenshots or short walkthrough

| Track | Signature portfolio project |
|---|---|
| Cloud | multi-tier app deployed via console, then fully rebuilt in Terraform/OpenTofu |
| Platform/IaC | entire K8s cluster + app provisioned with IaC only |
| CI/CD | full pipeline with GitOps via ArgoCD |
| SRE | OTel -> Prometheus -> Grafana observability stack with SLO + alert |
| DevSecOps | pipeline with Trivy, secret scanning, SAST, and managed secrets |

quality > quantity. one reproducible, observable, IaC-provisioned app with a real pipeline beats ten console-clicked screenshots.

## resume and profiles

- [ ] lead with projects + certs, then skills, then any experience
- [ ] quantify: "Provisioned a 3-node K8s cluster via Terraform"
- [ ] mirror posting keywords truthfully: Terraform, AWS, CI/CD, Kubernetes
- [ ] link GitHub and pin IaC/pipeline repos
- [ ] headline example: `Aspiring Cloud Engineer | AWS SAA | Terraform & Kubernetes labs`

## job titles to search for

true-entry targets:

- Cloud Support Associate / Cloud Support Engineer
- Junior Cloud Engineer / Associate Cloud Engineer
- Cloud Operations Analyst

borderline after strong projects or some experience:

- Junior DevOps Engineer / DevOps Engineer I
- Infrastructure Engineer

avoid anchoring on unleveled "DevOps Engineer", "Platform Engineer", or "SRE" for a first job.

## find and target roles

job boards are local, so use a strategy that travels:

- [ ] cloud providers hire entry-level support programs
- [ ] MSPs and consultancies hire cloud support in volume
- [ ] build a list of 20-40 target employers
- [ ] check careers pages directly
- [ ] use referrals through communities and open-source infra tools
- [ ] filter remote/timezone if local market is thin
- [ ] tailor every application to the stack

## interview prep

see [interview-prep.md](interview-prep.md) for the full Q&A bank.

questions u will be asked:

- [ ] pod in `CrashLoopBackOff` - diagnose it
- [ ] IAM roles vs IAM users
- [ ] `terraform plan` vs `apply`; what state is and what breaks it
- [ ] broken Dockerfile or container exits immediately
- [ ] CI/CD from `git push` to production
- [ ] reverse proxy vs load balancer

behavioral prompts:

- [ ] something u deployed broke in production - what did u do?
- [ ] manual process u automated - what was the impact?
- [ ] new technology u had to learn fast

## exit check

- [ ] 2-3 cloud/DevOps projects are reproducible from GitHub
- [ ] at least one project uses IaC
- [ ] at least one project has CI/CD
- [ ] resume points to proof, not vague tool lists
- [ ] target role list focuses on cloud support/ops and junior cloud roles
- [ ] u can explain one broken-deploy story out loud

[Beyond Entry-Level - Years 2+](beyond-entry.md)
