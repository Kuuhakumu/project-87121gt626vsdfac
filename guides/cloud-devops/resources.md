# resources - Cloud & DevOps meow

> free-first, current as of June 2026.
> no paid course is required to get hired; the free path covers the roadmap.

[Hub](README.md) - [Labs](labs.md) - [Interview Prep](interview-prep.md)

---

- [ ] **use official docs as truth**
- [ ] **use broad courses as backup**
- [ ] **read optional books when useful**
- [ ] **join communities carefully**
- [ ] **stay current without chasing everything**
- [ ] **skip dated advice**

## broad free courses and learning paths

these are broad resources. use them as backup or extra explanation, not as vague primary instructions unless a goal names an exact lesson.

| Resource | Covers | Why |
|---|---|---|
| **freeCodeCamp YouTube** | AWS, Docker, K8s, Terraform, Linux | full free courses; **⚠️ TODO verify exact video before primary use** |
| **MS Learn** | Azure fundamentals -> associate | official, free, sandboxed |
| **AWS Skill Builder** | AWS services | source-of-truth AWS courses |
| **Google Cloud Skills Boost** | GCP hands-on | official GCP labs |
| **KodeKloud free tier** | Docker, K8s, Terraform, CI/CD | lab-driven |
| **The Net Ninja / TechWorld with Nana YouTube** | DevOps, K8s, Docker, CI/CD | useful explainers; **⚠️ TODO verify exact playlist/video before primary use** |
| **Roadmap.sh** | DevOps / Cloud / K8s maps | sanity-check whats next |

## official docs

- [ ] **AWS:** docs.aws.amazon.com
- [ ] **Azure:** learn.microsoft.com
- [ ] **GCP:** cloud.google.com/docs
- [ ] **Kubernetes:** kubernetes.io/docs
- [ ] **Docker:** docs.docker.com
- [ ] **Terraform:** developer.hashicorp.com/terraform
- [ ] **OpenTofu:** opentofu.org
- [ ] **Prometheus:** prometheus.io
- [ ] **Grafana:** grafana.com/docs
- [ ] **OpenTelemetry:** opentelemetry.io
- [ ] **ArgoCD:** argo-cd.readthedocs.io

when YouTube and docs disagree, trust docs. videos go stale fast in cloud.

## books

| Book | For |
|---|---|
| *The Phoenix Project* | why DevOps exists |
| *The DevOps Handbook* | practices behind the story |
| *Site Reliability Engineering* | free Google SRE mindset book |
| *Terraform: Up & Running* | IaC depth after basics |
| *Kubernetes Up & Running* | K8s mental model |

## communities

- [ ] **r/devops**, **r/aws**, **r/kubernetes**
- [ ] **CNCF Slack**
- [ ] **HashiCorp Discuss**
- [ ] **DevOps / Platform Engineering Discords**
- [ ] **Dev.to / Hashnode** for project writeups

referrals beat cold applications. answer questions, share labs, and be specific.

## stay current

| Topic | What changed recently |
|---|---|
| **IaC** | OpenTofu is real alongside Terraform |
| **Helm** | v4 has breaking changes |
| **Observability** | OpenTelemetry is standard now |
| **Secrets** | cloud-native first; Vault v2.0 for self-hosted |
| **Platform Engineering** | internal developer platforms replacing ticket-driven DevOps |
| **AIOps** | use AI for config/log help, but keep debugging judgment |

## skip dated advice

- [ ] Jenkins-first -> start with GitHub Actions
- [ ] raw CloudFormation first -> Terraform/OpenTofu transfers better
- [ ] ELK as default observability -> OTel -> Prometheus -> Grafana
- [ ] Nagios first -> Prometheus + Grafana
- [ ] Chef/Puppet primary -> Ansible + IaC
- [ ] full cloud K8s before local -> kind/k3s/minikube first

---

*Last verified: June 2026. Links and versions drift - confirm on the official site. Sources in [/research](../../research/).*
