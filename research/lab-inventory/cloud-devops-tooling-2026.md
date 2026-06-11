# Cloud & DevOps Tooling & Trends — 2026

> curl + GitHub API verified 2026-06-13. ✅ VERIFIED · ⚠️ PARTIAL · ⛔ UNVERIFIED.

## Verified current versions (GitHub releases)
| Tool | Latest stable | Conf |
|---|---|---|
| Kubernetes | v1.36 | ✅ |
| Terraform | v1.15 (BSL license) | ✅ |
| OpenTofu | v1.12 (MPL-2, open fork) | ✅ |
| Helm | **v4** (breaking changes vs v3) | ✅ |
| Prometheus | v3.x | ✅ |
| ArgoCD | v3.x | ✅ |
| Docker Engine (Moby) | v29.x | ✅ |
| containerd | v2.x | ✅ |
| Flux | v2.8 | ✅ |
| OpenTelemetry Collector | v1.x | ✅ |
| Grafana | v13.x | ✅ |
| Vault | v2.0 (breaking changes) | ✅ |
| Backstage | v1.5x | ✅ |

## Big calls

**Cloud provider to learn first:** AWS (#1 market share) — most jobs, most cert recognition. Azure #2 (enterprise/Microsoft shops), GCP #3 (data/ML). Market-share ordering ⚠️ PARTIAL (Gartner/SO survey behind paywall/403) but consensus-solid. Start with ONE, AWS unless targeting a Microsoft shop.

**IaC:** Teach Terraform (still dominant, enterprise) AND mention OpenTofu (open MPL-2 fork, CNCF, at parity). OpenTofu is the principled open default; Terraform is what most jobs still use. HCL skills transfer 1:1 between them.

**Containers/orchestration:** Docker for build/local. Kubernetes v1.36 — but teach LOCAL clusters first (k3s, kind, minikube), NOT full cloud clusters day one. containerd is the runtime under the hood. Helm v4 (warn learners off stale v3 tutorials).

**CI/CD:** GitHub Actions = dominant default to teach. GitLab CI = strong alternative. Jenkins = legacy (still in enterprise, teach awareness not depth). 
**GitOps:** ArgoCD v3 primary (CNCF graduated), Flux as k8s-native alt.

**Observability:** OpenTelemetry → Prometheus → Grafana is THE stack. OTel is now the definitive standard, not "rising". De-emphasize ELK as the default.

**Secrets:** Teach cloud-native first (AWS Secrets Manager, Azure Key Vault). Vault v2.0 as self-hosted/enterprise option.

**Platform Engineering:** Real framing shift — "internal developer platforms" (Backstage v1.5x) replacing "DevOps team does everything". Worth a dedicated section.

**AI in DevOps/AIOps:** Real for IaC generation, log/incident summarization, pipeline assist. For a junior in 2026: use AI to generate/explain config, but be able to read and debug it. Judgment > generation. Don't over-teach.

## Teach this / cut that

**MUST TEACH (baseline):** Linux, networking basics, Git, one scripting lang (Python/Bash), Docker, one cloud (AWS), CI/CD concepts (GitHub Actions), IaC basics (Terraform/OpenTofu).

**TEACH AS DIFFERENTIATOR:** Kubernetes (local clusters), Terraform depth + modules, Ansible, observability (OTel/Prometheus/Grafana), GitOps (ArgoCD), second cloud, Vault/secrets, platform-eng concepts.

**CUT / DE-EMPHASIZE:** Jenkins-first (→ GitHub Actions), raw CloudFormation over Terraform, manual kubectl-only over GitOps, Nagios (→ Prometheus/Grafana), ELK-as-default (→ OTel), standing up full k8s clusters before local, Chef/Puppet as primary (→ Ansible/Terraform).

## Portfolio projects that impress
1. Deploy a 3-tier app with Terraform/OpenTofu + a CI/CD pipeline (GitHub Actions) + monitoring (Prometheus/Grafana). Zero console clicks.
2. GitOps: ArgoCD syncing a k8s app from a Git repo; show a config change auto-deploying.
3. Multi-stage Dockerfile → push to registry → deploy to local k8s (kind) → smoke test in pipeline.
4. Full observability stack on a sample app: OTel instrumentation → Prometheus → Grafana dashboard → alert on an SLO breach.
5. DevSecOps: add Trivy image scanning + secret scanning + SAST to a pipeline; Vault for secrets.

Sources: GitHub releases API (per-tool repos), opentofu.org, kubernetes.io, cncf.io — curl-verified 2026-06-13.
