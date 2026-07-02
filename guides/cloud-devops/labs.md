# Lab inventory - Cloud & DevOps meow

> platform status was curl-checked on 2026-06-13.
> free-first. u can do most of this roadmap without spending money.

[Hub](README.md) - [Resources](resources.md)

---

- [ ] **use this page by topic**
- [ ] **build labs into portfolio proof**
- [ ] **avoid dead old resources**

## how to use this page

each goal tells u *what* to practice. this page tells u *where*.
find the topic, do it hands-on, then commit the result to GitHub.

a lab u didnt reproduce yourself doesnt count, meow.

## by topic

### Linux and CLI

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| Bandit wargame | OverTheWire | overthewire.org/wargames/bandit/ | SSH into real boxes, CLI puzzles | Free | live |
| Linux scenarios | KillerCoda | killercoda.com | browser terminal, guided Linux tasks | Free | live |

### cloud provider free tiers

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| AWS Free Tier | AWS | aws.amazon.com/free/ | EC2, S3, IAM, VPC | Free tier | live |
| AWS Skill Builder | AWS | explore.skillbuilder.aws | self-paced labs, some free | Freemium | likely live |
| MS Learn sandboxes | Microsoft | learn.microsoft.com/training/ | Azure sandbox, no card | Free | live |
| Google Cloud Skills Boost | Google | cloudskillsboost.google | GCP hands-on labs | Freemium/credits | likely live |

set a billing alarm at $1 on day one. free tier is generous, not infinite.

### Docker and containers

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| Play with Docker | Docker | labs.play-with-docker.com | browser Docker host | Free | live |
| Docker scenarios | KillerCoda | killercoda.com | guided container labs | Free | live |

### Kubernetes

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| Play with Kubernetes | Docker | labs.play-with-k8s.com | browser k8s cluster | Free | live |
| K8s scenarios | KillerCoda | killercoda.com/kubernetes | kubectl/cluster labs | Free | live |
| Kube by Example | KodeKloud | kubebyexample.com | structured k8s lessons | Free | likely live |
| Official tutorials | Kubernetes | kubernetes.io/docs/tutorials/ | minikube/kind hands-on | Free | live |
| killer.sh | killer.sh | killer.sh | CKA/CKAD simulator | bundled w/ exam | live |

run a local cluster first: **k3s**, **kind**, or **minikube** before managed EKS/AKS/GKE.

### Terraform / IaC

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| Terraform tutorials | HashiCorp | developer.hashicorp.com/terraform/tutorials | provisioning, real providers | Free | live |
| Terraform/DevOps labs | KodeKloud | kodekloud.com | browser labs | Freemium | likely live |

HCL skills transfer 1:1 to **OpenTofu**.

### CI/CD and GitOps

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| GitHub Skills | GitHub | skills.github.com | Actions pipelines in repos | Free | live |
| GitLab CI | GitLab | docs.gitlab.com/ee/ci/ | pipeline YAML | Free tier | likely live |

### Observability

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| Grafana scenarios | KillerCoda | killercoda.com/grafana-labs | Prometheus + Grafana hands-on | Free | live |

### Git

| Lab | Platform | URL | What u do | Cost | Status |
|---|---|---|---|---|---|
| Learn Git Branching | - | learngitbranching.js.org | branch/merge puzzles | Free | live |

## platform quick reference

| Platform | Best for | Cost |
|---|---|---|
| **KillerCoda** | Linux, Docker, k8s, Grafana, Terraform | Free |
| **Play with Docker / K8s** | throwaway Docker/k8s sandboxes | Free |
| **KodeKloud** | structured DevOps labs | Freemium |
| **killer.sh** | CKA/CKAD/CKS simulator | bundled |
| **AWS Free Tier** | real AWS infra | Free tier |
| **MS Learn** | Azure sandboxes | Free |
| **Google Cloud Skills Boost** | GCP hands-on labs | Freemium |
| **HashiCorp tutorials** | Terraform/Vault guided | Free |
| **GitHub Skills** | Actions / CI/CD | Free |

## dead or paywalled old picks

| Old resource | What happened | Use instead |
|---|---|---|
| **Katacoda** | shut down Jun 2023 | **KillerCoda** |
| **A Cloud Guru** | acquired -> Pluralsight paid | AWS Skill Builder, KodeKloud free tier, freeCodeCamp **⚠️ TODO verify exact current course** |
| **Qwiklabs** | rebranded | Google Cloud Skills Boost |
| **learn.hashicorp.com** | moved | developer.hashicorp.com/tutorials |

## lab-to-portfolio pipeline

- [ ] local k8s with kind/k3s -> deploy sample app -> commit manifests
- [ ] AWS Free Tier -> rebuild infra in Terraform/OpenTofu
- [ ] GitHub Actions -> build -> test -> deploy pipeline
- [ ] KillerCoda Grafana -> OTel -> Prometheus -> Grafana + one SLO alert
- [ ] README with architecture diagram

---

*Last verified: 2026-06-13. Raw status checks in `research/lab-inventory/cloud-devops-2026.md`.*
