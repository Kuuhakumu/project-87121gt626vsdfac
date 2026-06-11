# 🧪 Lab Inventory — Cloud & DevOps (2026)

> Every platform here was **curl status-checked on 2026-06-13**.
> ✅ live · ⚠️ likely live (bot-blocked but reachable) · ❌ dead (do not use).
> Free-first. You can do ~90% of this roadmap without spending a cent.

[← Hub](README.md) · [Resources →](resources.md)

---

## How to use this page

Each phase of the guide tells you *what* to practice. This page tells you *where*.
Find the topic you're on, do it hands-on, then commit the result to GitHub. **A lab you didn't reproduce yourself doesn't count.**

---

## By topic

### Linux & CLI
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| Bandit wargame | OverTheWire | overthewire.org/wargames/bandit/ | SSH into real boxes, CLI puzzles level by level | Free | ✅ |
| Linux scenarios | KillerCoda | killercoda.com | Browser terminal, guided Linux tasks | Free | ✅ |

### Cloud provider free tiers
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| AWS Free Tier | AWS | aws.amazon.com/free/ | Build real infra (EC2, S3, IAM, VPC), 12-mo free | Free tier | ✅ |
| AWS Skill Builder | AWS | explore.skillbuilder.aws | Self-paced labs, some free | Freemium | ⚠️ |
| MS Learn sandboxes | Microsoft | learn.microsoft.com/training/ | Free Azure sandbox, **no credit card** | Free | ✅ |
| Google Cloud Skills Boost | Google | cloudskillsboost.google | Hands-on GCP labs (ex-Qwiklabs) | Freemium/credits | ⚠️ |

> 💡 **Set a billing alarm at $1 on day one.** The free tier is generous but not infinite — an unattended resource is the classic beginner mistake.

### Docker & containers
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| Play with Docker | Docker | labs.play-with-docker.com | Browser Docker host, 4-hr throwaway sessions | Free | ✅ |
| Docker scenarios | KillerCoda | killercoda.com | Guided container labs | Free | ✅ |

### Kubernetes
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| Play with Kubernetes | Docker | labs.play-with-k8s.com | Browser k8s cluster | Free | ✅ |
| K8s scenarios | KillerCoda | killercoda.com/kubernetes | Guided kubectl/cluster labs | Free | ✅ |
| Kube by Example | KodeKloud | kubebyexample.com | Structured k8s lessons | Free | ⚠️ |
| Official tutorials | Kubernetes | kubernetes.io/docs/tutorials/ | minikube / kind hands-on | Free | ✅ |
| killer.sh | killer.sh | killer.sh | CKA/CKAD exam simulator | Bundled w/ exam | ✅ |

> 🏠 **Run a cluster locally first.** Install **k3s**, **kind**, or **minikube** on your own machine before touching a managed cloud cluster (EKS/AKS/GKE) — local is free, fast, and forgiving.

### Terraform / IaC
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| Terraform tutorials | HashiCorp | developer.hashicorp.com/terraform/tutorials | Guided provisioning, real providers | Free | ✅ |
| Terraform/DevOps labs | KodeKloud | kodekloud.com | Browser labs, free community tier | Freemium | ⚠️ |

> HCL skills transfer 1:1 to **OpenTofu** (the open MPL-2 fork). Learn one, you know both — `terraform apply` ↔ `tofu apply`.

### CI/CD & GitOps
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| GitHub Skills | GitHub | skills.github.com | Build Actions pipelines in real repos | Free | ✅ |
| GitLab CI | GitLab | docs.gitlab.com/ee/ci/ | Pipeline YAML, free-tier minutes | Free tier | ⚠️ |

### Observability
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| Grafana scenarios | KillerCoda | killercoda.com/grafana-labs | Prometheus + Grafana hands-on | Free | ✅ |

### Git
| Lab | Platform | URL | What you do | Cost | Status |
|---|---|---|---|---|---|
| Learn Git Branching | — | learngitbranching.js.org | Visual git branch/merge puzzles | Free | ✅ |

---

## Platform quick reference

| Platform | Best for | Cost |
|---|---|---|
| **KillerCoda** | Browser scenarios: Linux, Docker, k8s, Grafana, Terraform | Free |
| **Play with Docker / K8s** | Throwaway Docker / k8s sandboxes | Free |
| **KodeKloud** | Structured DevOps labs + courses | Freemium |
| **killer.sh** | CKA/CKAD/CKS exam simulator | Bundled with LF exam |
| **AWS Free Tier** | Real AWS infra, 12 months | Free tier |
| **MS Learn** | Azure sandboxes, no card | Free |
| **Google Cloud Skills Boost** | GCP hands-on labs | Freemium/credits |
| **HashiCorp tutorials** | Terraform / Vault guided | Free |
| **GitHub Skills** | Actions / CI/CD in real repos | Free |

---

## ❌ Dead or paywalled since ~2021 (don't waste time)

| Old resource | What happened | Use instead |
|---|---|---|
| **Katacoda** | Shut down Jun 2023 (tombstone page only) | **KillerCoda** (same founders) |
| **A Cloud Guru** | Acquired → redirects to Pluralsight (paid) | AWS Skill Builder, KodeKloud free tier, freeCodeCamp |
| **Qwiklabs** | Rebranded | **Google Cloud Skills Boost** (same labs, new name) |
| **learn.hashicorp.com** | Moved | **developer.hashicorp.com/tutorials** |

---

## Suggested lab-to-portfolio pipeline

1. **Local k8s** (kind/k3s) → deploy a sample app → commit manifests.
2. **AWS Free Tier** → rebuild that app's infra in **Terraform/OpenTofu**, zero console clicks.
3. **GitHub Actions** → add a build → test → deploy pipeline to the repo.
4. **KillerCoda Grafana** → wire **OTel → Prometheus → Grafana** + one SLO alert.
5. Write the README with an architecture diagram. That makes it a portfolio project, not just a lab.

---

*Last verified: 2026-06-13. Platforms come and go — if a link 404s, check [resources.md](resources.md) for the current equivalent. Raw status checks in `research/lab-inventory/cloud-devops-2026.md`.*
