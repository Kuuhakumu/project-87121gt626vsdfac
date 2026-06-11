# 📚 Resources — Cloud & DevOps (2026)

> Free-first, current as of June 2026. Channels, courses, books, communities, and roadmaps.
> No paid course is *required* to get hired — the free column covers the whole roadmap.

[← Hub](README.md) · [Labs](labs.md) · [Interview Prep →](interview-prep.md)

---

## Free courses & learning paths

| Resource | Covers | Why |
|---|---|---|
| **freeCodeCamp (YouTube)** | AWS, Docker, K8s, Terraform, Linux — full multi-hour courses | The single best free firehose; full cert-prep courses |
| **MS Learn** | Azure, fundamentals → associate | Official, free, with built-in sandboxes |
| **AWS Skill Builder** | AWS services, some free digital courses | Straight from the source |
| **Google Cloud Skills Boost** | GCP hands-on | Official GCP labs |
| **KodeKloud (free tier)** | Docker, K8s, Terraform, CI/CD with browser labs | Lab-driven, beginner-friendly |
| **The Net Ninja / TechWorld with Nana (YouTube)** | DevOps end-to-end, K8s, Docker, CI/CD | Nana's DevOps bootcamp video is a classic starting point |
| **Roadmap.sh** | DevOps / Cloud / K8s visual roadmaps | Sanity-check what to learn next |

---

## Official docs (your real source of truth)

- **AWS** — docs.aws.amazon.com · **Azure** — learn.microsoft.com · **GCP** — cloud.google.com/docs
- **Kubernetes** — kubernetes.io/docs (the tutorials are excellent)
- **Docker** — docs.docker.com
- **Terraform** — developer.hashicorp.com/terraform · **OpenTofu** — opentofu.org
- **Prometheus** — prometheus.io · **Grafana** — grafana.com/docs · **OpenTelemetry** — opentelemetry.io
- **ArgoCD** — argo-cd.readthedocs.io

> When a YouTube tutorial and the official docs disagree, trust the docs — videos go stale, especially on fast-moving tools (Helm v3→v4, Vault v1→v2).

---

## Books (optional, high-signal)

| Book | For |
|---|---|
| *The Phoenix Project* (Kim et al.) | **Why** DevOps exists — narrative, read it early |
| *The DevOps Handbook* | The practices behind the story |
| *Site Reliability Engineering* (Google, **free online**) | SRE mindset — sre.google/books |
| *Terraform: Up & Running* (Brikman) | IaC depth once you know basics |
| *Kubernetes Up & Running* | K8s mental model |

---

## Communities

- **r/devops**, **r/aws**, **r/kubernetes** (Reddit) — real job-market talk, "is this cert worth it" threads
- **CNCF Slack** — Kubernetes/cloud-native, where maintainers hang out
- **HashiCorp Discuss** — Terraform/Vault questions
- **DevOps / Platform Engineering Discords** — pairing, project feedback
- **Dev.to / Hashnode** — write up your projects; a public build log is portfolio signal

> Referrals beat cold applications. Being active in these communities — answering questions, sharing your labs — is how those referrals happen.

---

## Stay current (2026 stack)

The field moves fast. Keep an eye on these so your knowledge stays current:

| Topic | What changed recently |
|---|---|
| **IaC** | OpenTofu (MPL-2 fork) is now a real choice alongside Terraform (BSL) |
| **Helm** | **v4** has breaking changes — avoid v3-era tutorials |
| **Observability** | **OpenTelemetry** is the standard now, not "rising" — de-emphasize ELK-default |
| **Secrets** | Cloud-native first (Secrets Manager / Key Vault); Vault **v2.0** for self-hosted |
| **Platform Engineering** | "Internal developer platforms" (Backstage) replacing "the DevOps team does everything" |
| **AIOps** | Use AI to generate/explain config — but be able to read & debug it. Judgment > generation |

---

## What to skip (dated advice you'll still see online)

- **Jenkins-first** → start with **GitHub Actions**
- **Raw CloudFormation over Terraform** for learning → Terraform/OpenTofu transfers across clouds
- **ELK as the default observability stack** → OTel → Prometheus → Grafana
- **Nagios** → Prometheus + Grafana
- **Chef/Puppet as your primary config tool** → Ansible (and IaC)
- **Standing up full cloud k8s clusters before local** → kind/k3s/minikube first

---

*Last verified: June 2026. Links and versions drift — confirm on the official site. Sources in [/research](../../research/).*
