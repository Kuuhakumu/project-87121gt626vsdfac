# Cloud & DevOps Technology Stack — 2026 Research Report
*For: Zero-to-First-Job Career Guide | Date: June 2026*

---

## How to Read This Document

Every factual claim carries a confidence tag:
- ✅ **VERIFIED** — confirmed via direct curl of authoritative source (GitHub Releases API, official project site)
- ⚠️ **PARTIAL** — inferred from adjacent verified data or reliable secondary source
- ⛔ **UNVERIFIED** — could not be confirmed via curl (Cloudflare-blocked or no public API)

Sources cited as `[GitHub API: org/repo]` were queried via `https://api.github.com/repos/{org}/{repo}/releases/latest`.

---

## 1. Cloud Providers — Market Position & Beginner Pick

### Current Standing (2026)

The three-tier cloud hierarchy has been stable for years and remains intact in 2026:

- **AWS** — market leader, widest service catalog (~200+ services), most job postings reference AWS skills ⚠️ PARTIAL (market share data not curl-verifiable)
- **Azure** — #2, dominant in enterprises with Microsoft/Office 365 footprints, strongest in hybrid/on-premises scenarios ⚠️ PARTIAL
- **GCP** — #3, strongest in data engineering, ML/AI workloads (Vertex AI), Kubernetes (GCP invented it) ⚠️ PARTIAL

The AWS/Azure/GCP tier gap below them (Oracle Cloud, IBM Cloud, Alibaba Cloud) remains large for general DevOps hiring.

### What Beginners Should Pick First

**Teach AWS first.** The reasoning:
- Largest job market breadth
- Best free-tier resources for learning (EC2, S3, Lambda, RDS all have free tiers)
- Most CNCF tooling tutorials assume AWS for examples
- AWS certifications (Cloud Practitioner → Solutions Architect Associate) are the most recognized entry credentials

Azure is the right second pick for anyone targeting enterprise/Microsoft environments. GCP is worth a module if data/ML is the intended specialization.

**Key AWS services for a beginner curriculum:**
- Compute: EC2, Lambda (serverless)
- Storage: S3, EBS
- Networking: VPC, Route 53, CloudFront
- Database: RDS, DynamoDB
- IAM (identity & access — foundational for everything)
- EKS (Elastic Kubernetes Service) for containers

⚠️ PARTIAL — CNCF survey data at `cncf.io` and Stack Overflow Developer Survey at `survey.stackoverflow.co` returned Cloudflare 403; market position based on consistent industry consensus.

---

## 2. Infrastructure as Code (IaC)

### Terraform vs OpenTofu: The 2023 Fork Situation

In August 2023, HashiCorp changed Terraform's license from MPL 2.0 to BSL (Business Source License), restricting commercial use. The community responded by forking the project as **OpenTofu** under the Linux Foundation. This is now a permanent split.

**OpenTofu current status:** ✅ VERIFIED
- Latest stable: **v1.12.2** (released 2026-06-12)
- Previous stable: v1.11.0 (2025-12-09), v1.10.0 (2025-06-23)
- Active development, Linux Foundation project, CNCF landscape member
- Notable adopters: Fidelity Investments published a migration story in October 2025
- Source: `opentofu.org` blog + `[GitHub API: opentofu/opentofu]`

**Terraform (HashiCorp/IBM) current status:** ✅ VERIFIED
- Latest stable: **v1.15.6** (released 2026-06-10)
- Still under active development by HashiCorp (now IBM-owned after 2024 acquisition)
- BSL license limits: cannot use in a competing SaaS product; individual/enterprise internal use is fine
- Source: `[GitHub API: hashicorp/terraform]`

### The Teaching Decision: OpenTofu vs Terraform

For a beginner guide, **teach OpenTofu as the default, with a clear note that the HCL syntax is ~99% identical to Terraform**. Reasoning:
- OpenTofu is MIT/MPL-licensed — no commercial restrictions, safe to use in any context
- HCL syntax is nearly identical; skills transfer directly
- Enterprise teams are actively migrating (Fidelity being a public example)
- OpenTofu 1.8+ added features Terraform hasn't shipped (ephemeral values, write-only attributes)
- However: Terraform still has larger market install base in established enterprises — acknowledge this

**Practical approach for guide:** Teach OpenTofu syntax. Show Terraform equivalence. Note BSL implications.

### Other IaC Tools

| Tool | Status 2026 | Teach? |
|------|-------------|--------|
| **Pulumi** | Strong growth — uses real languages (Python, TypeScript, Go) instead of HCL | Teach as "IaC for developers" differentiator |
| **CloudFormation** | AWS-native, JSON/YAML, still widely used in AWS-only shops | Mention; don't lead with it |
| **Bicep** | Azure-native ARM template replacement, Azure-specific | Teach only in Azure track |
| **Ansible** | Config management + ad-hoc provisioning, not declarative IaC | Still relevant for server config; covers a different use case |
| **CDK (AWS/CDKTF)** | Code-first IaC using TypeScript/Python generating CF or TF configs | Teach as advanced differentiator |

⚠️ PARTIAL for market share and adoption trends; version data ✅ VERIFIED via GitHub API.

---

## 3. Containers & Orchestration

### Docker Engine

✅ VERIFIED — Latest stable: **v29.5.3** (released 2026-06-03)
- Moby project (Docker Engine open source) still actively maintained
- Notable: Docker 29.x ships with containerd v2.2.4 as the default image store backend
- Source: `[GitHub API: moby/moby]`

**Docker remains the universal starting point for containers.** Despite the containerd vs Docker Engine architectural debate, Docker CLI is still what beginners and most CI systems interact with. Teach Docker first, explain containerd as the underlying runtime.

### containerd

✅ VERIFIED — Latest stable: **v2.3.1** (released 2026-05-20)
- containerd is the CNCF-graduated low-level container runtime that Docker Engine wraps
- Kubernetes uses containerd directly (not Docker) since the dockershim removal in K8s 1.24 (2022)
- Beginners don't interact with containerd directly — it's infrastructure knowledge
- Source: `[GitHub API: containerd/containerd]`

**Teaching note:** Explain the layering (OCI spec → containerd → Docker Engine) conceptually, but don't make students operate containerd directly.

### Podman

- Daemonless, rootless Docker alternative from Red Hat
- Syntax is Docker-compatible (`alias docker=podman` works for most cases)
- Default on RHEL/Fedora
- ⚠️ PARTIAL: growing adoption in enterprise Linux environments but Docker still dominant for beginners
- **Teach as a brief "also know about" topic**, especially if Red Hat/OpenShift environments are likely

### Kubernetes

✅ VERIFIED — via `kubernetes.io/releases` + `[GitHub API: kubernetes/kubernetes]`

**Current supported releases (as of June 2026):**
| Version | Latest Patch | EOL |
|---------|-------------|-----|
| **1.36** | 1.36.2 (2026-05-13) — **current latest** | 2027-06-28 |
| 1.35 | 1.35.5 (2026-05-12) | 2027-02-28 |
| 1.34 | 1.34.8 (2026-05-12) | 2026-10-27 |
| 1.33 | 1.33.12 (2026-05-12) | 2026-06-28 |

K8s 1.37 release is in planning phase as of June 2026.

**What to teach about Kubernetes:**
- Core objects: Pod, Deployment, Service, ConfigMap, Secret, Namespace, Ingress
- `kubectl` commands for the 20 scenarios that matter
- YAML manifest writing and Helm chart consumption
- Do **not** teach cluster installation from scratch (kubeadm) as a primary skill — use managed services (EKS/GKE/AKS) or local alternatives

**Local Kubernetes for learning:**
- **kind** (Kubernetes IN Docker) — preferred for CI and fast iteration ⚠️ PARTIAL
- **k3s** (Rancher Labs, lightweight K8s) — good for Raspberry Pi / resource-constrained environments ⚠️ PARTIAL
- **minikube** — original local K8s tool, still works, somewhat heavier ⚠️ PARTIAL
- **Docker Desktop** includes a K8s option — easiest for absolute beginners

Teach **kind** as the default local environment for course exercises.

### Helm

✅ VERIFIED — Latest stable: **v4.2.1** (released 2026-06-12)
- Helm 4.x is the current major version (breaking changes from Helm 3 are minimal for basic usage)
- Source: `[GitHub API: helm/helm]`
- Helm is the de-facto Kubernetes package manager — teach chart consumption first, chart authoring second

---

## 4. CI/CD

### Current Landscape

**GitHub Actions** has become the dominant CI/CD platform for new projects and the default reference implementation for beginner education. ⚠️ PARTIAL (no curl-verifiable market share data, but consistent with community consensus)

**Teaching priority order:**

1. **GitHub Actions** — Teach first. YAML-based, free for public repos, massive marketplace of reusable actions, tightly integrated with the largest code hosting platform. Every beginner already has a GitHub account.

2. **GitLab CI** — Teach as second. Very similar YAML DSL, dominant in enterprise self-hosted Git deployments. Good to cover because many enterprise jobs use GitLab.

3. **ArgoCD** (GitOps) — Teach as a distinct paradigm shift (pull-based vs push-based). See section 6.

4. **Jenkins** — Mention as legacy context only. Huge installed base in enterprises, but it's maintenance burden, not a growth skill. Don't lead a 2026 curriculum with Jenkins.

5. **CircleCI / TeamCity** — Brief mention. Niche market share; skills transfer from GitHub Actions.

**GitOps tools — Flux:**
✅ VERIFIED — Flux v2 latest: **v2.8.8** (released 2026-05-20)
- Source: `[GitHub API: fluxcd/flux2]`
- Flux and ArgoCD are the two dominant GitOps controllers; both are CNCF graduated projects

---

## 5. Observability

### Prometheus

✅ VERIFIED — Latest stable: **v3.12.0** (released 2026-05-28)
- Prometheus 3.x is the current major version (3.0 released late 2024 with breaking changes from 2.x)
- Source: `[GitHub API: prometheus/prometheus]`
- Prometheus is the de-facto metrics standard in Kubernetes environments; teach it as the baseline

### Grafana

✅ VERIFIED — Latest stable: **v13.0.2** (released 2026-06-09)
- Grafana 13.x is the current major version
- Grafana Labs is a CNCF member; the Grafana stack (Loki, Tempo, Mimir, Pyroscope) confirmed in CNCF landscape ✅ VERIFIED via `[GitHub API: cncf/landscape]` raw YAML
- Source: `[GitHub API: grafana/grafana]`

### OpenTelemetry (OTel)

✅ VERIFIED — OTel Collector latest: **v1.60.0 / v0.154.0** (released 2026-06-08)
- Source: `[GitHub API: open-telemetry/opentelemetry-collector]`
- OTel specification versioning confirmed at `opentelemetry.io/status`
- **OpenTelemetry is the rising unification standard** for traces, metrics, and logs. It replaces vendor-specific SDKs (Jaeger client, Zipkin client, etc.) with a single, vendor-neutral instrumentation layer.

**Why this matters for the guide:**
- OTel traces → export to Jaeger, Zipkin, or commercial APM (Datadog, New Relic, Honeycomb)
- OTel metrics → export to Prometheus
- OTel logs → export to Loki, Elasticsearch
- Teaching OTel gives students a framework that works regardless of which backend an employer uses

### The Grafana LGTM Stack

The open-source observability stack increasingly taught alongside Prometheus:
- **L**oki — log aggregation (lightweight alternative to Elasticsearch for logs) ✅ VERIFIED (CNCF landscape)
- **G**rafana — dashboards ✅ VERIFIED
- **T**empo — distributed tracing ✅ VERIFIED (CNCF landscape)
- **M**imir — long-term Prometheus metrics storage ✅ VERIFIED (CNCF landscape)

### ELK Stack

- Elasticsearch + Logstash + Kibana — still widely deployed, especially for centralized log management
- OpenSearch (AWS fork of Elasticsearch) is the open-source alternative since the Elastic license change
- ⚠️ PARTIAL: ELK remains in production at many enterprises but Loki is the lighter-weight default for new K8s deployments
- **Teach Loki first for logs in a K8s context; mention ELK/OpenSearch as enterprise context**

### Datadog / Commercial APM

- Dominant commercial observability platform ⛔ UNVERIFIED (no public API for pricing/market position)
- Extremely common in enterprise job descriptions
- **Teach the concepts via open-source tools (Prometheus/Grafana/OTel); note that "Datadog/New Relic/Dynatrace do this commercially"**

---

## 6. Platform Engineering & GitOps

### Is "Platform Engineering" Replacing "DevOps"?

⚠️ PARTIAL — This is a real and observable trend. The framing is shifting:

- **Old framing (2015-2022):** "DevOps engineer" — a person who bridges dev and ops, automates everything
- **New framing (2023-2026):** "Platform engineer" — builds the internal developer platform (IDP) that enables dev teams to self-serve infrastructure

The distinction matters for curriculum framing:
- DevOps: focus on CI/CD pipelines, automation, cultural practices
- Platform Engineering: focus on building and operating the platform itself — developer portals, golden paths, self-service tooling

For a **zero-to-first-job** guide, "DevOps" remains the correct job title target. Platform Engineering is a growth path for mid/senior level.

### Backstage (Internal Developer Portal)

✅ VERIFIED — Latest stable: **v1.51.2** (released 2026-06-10)
- Source: `[GitHub API: backstage/backstage]`
- Confirmed as CNCF member project ✅ VERIFIED via CNCF landscape YAML
- Backstage is the Spotify-originated Internal Developer Platform (IDP) framework
- Adopted by thousands of organizations as the foundation for developer portals

**Teaching recommendation:** Mention Backstage as the leading IDP tool; don't build a course module around it at beginner level. It's a differentiator to name-drop and understand conceptually.

### GitOps — ArgoCD

✅ VERIFIED — Latest stable: **v3.4.3** (released 2026-05-28)
- Source: `[GitHub API: argoproj/argo-cd]`
- ArgoCD is a CNCF graduated project; confirmed in CNCF landscape ✅ VERIFIED
- ArgoCD 3.x is the current major version
- **GitOps with ArgoCD is a must-teach differentiator in 2026.** It represents the shift from "CI system pushes to cluster" to "cluster pulls desired state from Git." Every K8s job will expect familiarity.

**What to teach for GitOps:**
1. The GitOps principles (Git as single source of truth, declarative, reconciliation loop)
2. ArgoCD installation and basic Application resource
3. A simple app deployment via ArgoCD from a GitHub repo
4. Optional: Flux as alternative (same concepts, different operator style)

---

## 7. AI in DevOps / AIOps

### What's Real for Juniors in 2026

⚠️ PARTIAL — No single authoritative source; synthesis from project release notes and community direction.

**Real and usable today:**
- **IaC generation:** GitHub Copilot, Claude, ChatGPT can generate Terraform/OpenTofu modules, Kubernetes manifests, Dockerfile content, GitHub Actions workflows. This is genuinely useful and accelerates beginners.
- **AI-assisted debugging:** Pasting error logs into an LLM to get root-cause explanations is a standard debugging workflow.
- **Security scanning:** Snyk, Trivy, and similar tools are incorporating AI-generated remediation suggestions.
- **Incident summarization:** Tools like PagerDuty and Datadog now offer AI-assisted incident summaries.

**Still mostly hype for juniors:**
- "Autonomous AIOps" that self-heals production incidents — requires deep training data from your specific environment; not plug-and-play at junior level
- AI-generated runbooks that are actually production-safe — useful for drafts, not trustworthy without expert review

**What to teach:**
- Using AI tools as productivity accelerators, not replacements for understanding
- How to prompt for IaC and CI/CD YAML generation
- How to critically review AI-generated config (AI makes subtle IAM/security mistakes)
- Security: never paste secrets or production config into public AI tools

---

## 8. Config & Secrets Management

### HashiCorp Vault

✅ VERIFIED — Latest stable: **v2.0.2** (released 2026-06-05)
- Vault 2.0 is a major version milestone (breaking change: removed `cap_ipc_lock` for container compatibility)
- Source: `[GitHub API: hashicorp/vault]`
- Vault is still the industry-standard self-hosted secrets manager; widely deployed in enterprises
- BSL license (same as Terraform) — same caveats apply

### Cloud-Native Secret Managers

⚠️ PARTIAL — teach these alongside Vault:
- **AWS Secrets Manager** + **AWS Parameter Store** — AWS-native; integrated with IAM
- **Azure Key Vault** — Azure-native
- **GCP Secret Manager** — GCP-native
- **Kubernetes Secrets** — native but base64-encoded (not encrypted at rest by default) — teach the limitation and how to fix it (Sealed Secrets, External Secrets Operator)

**Teaching approach:** Teach cloud-native secret managers for cloud-specific tracks. Teach Vault for platform-agnostic / multi-cloud scenarios. Always teach "never put secrets in code or environment variables in plain text" as a foundational principle.

**External Secrets Operator** — worth a mention: bridges K8s with external secret backends (Vault, AWS Secrets Manager, etc.). Common in production K8s setups.

---

## 9. Verified Versions Table (June 2026)

| Tool | Latest Stable | Release Date | Source | Confidence |
|------|--------------|-------------|--------|------------|
| Kubernetes | **1.36.2** | 2026-05-13 | GitHub API: kubernetes/kubernetes + kubernetes.io/releases | ✅ VERIFIED |
| Terraform (HashiCorp) | **1.15.6** | 2026-06-10 | GitHub API: hashicorp/terraform | ✅ VERIFIED |
| OpenTofu | **1.12.2** | 2026-06-12 | GitHub API: opentofu/opentofu | ✅ VERIFIED |
| Helm | **4.2.1** | 2026-06-12 | GitHub API: helm/helm | ✅ VERIFIED |
| Prometheus | **3.12.0** | 2026-05-28 | GitHub API: prometheus/prometheus | ✅ VERIFIED |
| Grafana | **13.0.2** | 2026-06-09 | GitHub API: grafana/grafana | ✅ VERIFIED |
| ArgoCD | **3.4.3** | 2026-05-28 | GitHub API: argoproj/argo-cd | ✅ VERIFIED |
| Docker Engine (Moby) | **29.5.3** | 2026-06-03 | GitHub API: moby/moby | ✅ VERIFIED |
| containerd | **2.3.1** | 2026-05-20 | GitHub API: containerd/containerd | ✅ VERIFIED |
| Flux v2 | **2.8.8** | 2026-05-20 | GitHub API: fluxcd/flux2 | ✅ VERIFIED |
| OTel Collector | **1.60.0 / v0.154.0** | 2026-06-08 | GitHub API: open-telemetry/opentelemetry-collector | ✅ VERIFIED |
| Backstage | **1.51.2** | 2026-06-10 | GitHub API: backstage/backstage | ✅ VERIFIED |
| HashiCorp Vault | **2.0.2** | 2026-06-05 | GitHub API: hashicorp/vault | ✅ VERIFIED |

*Note: All versions confirmed via GitHub Releases API on 2026-06-13. Helm 4.x represents a major version jump from Helm 3 (which was ~3.16.x); Helm 4 has been released and is the current version.*

---

## 10. "Teach This / Cut That" — Three-Tier Summary

### ✅ MUST TEACH (Baseline for Employment)

These are the skills hiring managers expect at entry level in 2026. A candidate without these will be filtered out.

**Cloud Fundamentals**
- One cloud provider to depth: AWS (preferred) or Azure
- Core services: compute, storage, networking, IAM, managed databases
- Cloud CLI usage (aws-cli / az cli)

**Linux & Scripting**
- Linux command line (the underlying OS for everything)
- Bash scripting for automation
- Basic Python for tooling scripts

**Containers**
- Docker: build, run, compose, push/pull from registry
- Writing a production-quality Dockerfile (multi-stage builds, non-root user, .dockerignore)
- Docker Compose for local multi-service development

**Kubernetes Core**
- kubectl for the 20 common operations
- Writing Deployment, Service, ConfigMap, Secret YAML
- Consuming a Helm chart
- Understanding Ingress, namespaces, RBAC basics

**IaC**
- OpenTofu (or Terraform — syntax identical): write and apply a basic infrastructure module
- Remote state, workspaces, variable files
- At least one cloud provider module (e.g., `aws_instance`, `aws_vpc`)

**CI/CD**
- GitHub Actions: write a workflow that builds, tests, and deploys
- Understanding triggers, jobs, steps, secrets in CI
- Container image build and push to a registry (GHCR, ECR, Docker Hub)

**Version Control**
- Git: branch, merge, PR workflow — the foundation everything else builds on
- Git as source of truth for infrastructure (GitOps mindset)

**Observability Basics**
- Prometheus + Grafana: deploy, write a basic PromQL query, build a dashboard
- Understanding metrics vs logs vs traces as three observability pillars
- Reading application logs from `kubectl logs`

**Secrets hygiene**
- Never commit secrets; use env vars + secret managers
- Cloud-native secret manager (AWS Secrets Manager or equivalent)

---

### 🚀 TEACH AS DIFFERENTIATOR (Growth Path)

These skills move a candidate from "entry level" to "strong hire." Not required day one, but teach them to create standout portfolios.

**GitOps with ArgoCD**
- Deploy an application via ArgoCD from a GitHub repo
- Understand the reconciliation loop and why it's superior to CI push
- This is increasingly expected even at junior level in cloud-native shops

**OpenTelemetry**
- Instrument a simple app with OTel SDK
- Export traces to Jaeger or Tempo, metrics to Prometheus
- This demonstrates understanding of modern observability architecture

**Pulumi**
- IaC using a real programming language (Python or TypeScript)
- Especially differentiating for candidates from a software development background

**Security fundamentals**
- Container image scanning (Trivy)
- IAM least-privilege design
- Network policies in Kubernetes
- Supply chain basics (SBOM awareness)

**Platform Engineering concepts**
- What an Internal Developer Platform is
- Backstage: what it is, why organizations adopt it
- "Golden path" concept

**Multi-cloud awareness**
- Know the equivalent service across clouds (EC2 ≈ Azure VMs ≈ GCE)
- Understand why organizations go multi-cloud and what tools (Terraform/OpenTofu) enable it

**Ansible for configuration management**
- Covers a different problem than Terraform (configuring existing servers, not provisioning)
- Still common in hybrid environments

**Serverless**
- AWS Lambda + API Gateway as a deployment pattern
- When serverless is and isn't appropriate

---

### ✂️ CUT or DE-EMPHASIZE (Dated — Don't Lead With These)

These tools have large installed bases but are declining as first-hire expectations, and leading a 2026 curriculum with them signals outdated focus.

| Tool / Practice | Why Cut | What Replaces It |
|----------------|---------|-----------------|
| **Jenkins as primary CI/CD** | Groovy DSL, maintenance burden, "legacy" label in most communities | GitHub Actions / GitLab CI |
| **Raw CloudFormation** (JSON/YAML) | Verbose, AWS-only, painful to write; superseded by CDK for AWS-specific IaC | Terraform/OpenTofu or AWS CDK |
| **Nagios / Zabbix** | Pre-cloud monitoring tools; rarely mentioned in new job descriptions | Prometheus + Grafana |
| **ELK as default log stack** | Heavy resource requirements; Loki is the K8s-native default | Grafana Loki |
| **Manual `kubectl apply` in production** | Not reproducible; unsafe | GitOps (ArgoCD/Flux) |
| **Puppet / Chef** | Configuration management tools from pre-container era; niche survival | Ansible (simpler), or fully container-based (no server config needed) |
| **Docker Swarm** | Effectively deprecated in favor of Kubernetes | Kubernetes (or k3s for lighter workloads) |
| **VM-centric operations** (SSH into servers to fix things) | "Pet vs cattle" — immutable infrastructure is the modern approach | Containers + K8s + GitOps |
| **Helm 2** | Tiller was removed in Helm 3; Helm 4 is current | Helm 4 |
| **Terraform as the only IaC option** (ignoring BSL) | Students need to understand the license split | Teach OpenTofu as default, note Terraform equivalence |

---

## 11. Portfolio Project Ideas

These are projects that demonstrate real hiring signal — they show the full DevOps loop, not just individual tools.

### Project 1 — "The Full Stack" (Core Portfolio Piece)
**Deploy a 3-tier web app with full IaC + CI/CD + monitoring**

Components:
- A simple web app (Node.js / Python Flask / whatever) with a frontend, API, and database
- Dockerized (multi-stage Dockerfile, Docker Compose for local dev)
- Infrastructure provisioned with OpenTofu: VPC, EC2/ECS or EKS cluster, RDS
- GitHub Actions pipeline: lint → test → build image → push to ECR → deploy
- Prometheus + Grafana monitoring stack deployed alongside
- Alerting rule: alert if HTTP error rate > 1%

*Why it impresses:* Shows the complete automation loop. Every piece is something a real team does.

### Project 2 — "GitOps Delivery" (Differentiator)
**Multi-environment GitOps deployment with ArgoCD**

Components:
- A Kubernetes cluster (EKS, GKE, or kind locally)
- An application with staging and production environments as separate ArgoCD Applications
- Helm chart for the application with environment-specific `values.yaml`
- Promotion flow: merge to `main` → ArgoCD syncs staging automatically → manual promotion to prod
- Demonstrate a rollback by reverting a Git commit

*Why it impresses:* GitOps is the #1 differentiator skill in 2026 K8s job descriptions. Most candidates can't demo it.

### Project 3 — "Observability First" (Differentiator)
**Instrument, collect, and visualize with the full OTel stack**

Components:
- A small microservices app (2-3 services) with OpenTelemetry SDK instrumentation
- OTel Collector receiving traces, metrics, logs
- Traces → Grafana Tempo; Metrics → Prometheus → Grafana; Logs → Loki → Grafana
- A Grafana dashboard showing RED metrics (Rate, Errors, Duration) per service
- A trace showing a request crossing service boundaries

*Why it impresses:* Observability is a senior skill in many orgs; showing OTel fluency at entry level is rare and noticed.

### Project 4 — "Secure by Default" (Security-Focused)
**A Kubernetes deployment with security hardening**

Components:
- Trivy scanning in CI pipeline (fail build on HIGH/CRITICAL CVEs)
- Kubernetes NetworkPolicy restricting pod-to-pod traffic
- RBAC: separate ServiceAccounts with least privilege per workload
- Secrets managed via External Secrets Operator pulling from AWS Secrets Manager
- Pod Security Admission configured (restricted policy)
- A brief README explaining each security decision

*Why it impresses:* Security is the gap most bootcamp grads have. Demonstrating it at junior level is a strong differentiator.

### Project 5 — "Mini Platform" (Advanced / Platform Engineering)
**A simple Internal Developer Platform using Backstage**

Components:
- Backstage running locally with a custom Software Catalog
- A GitHub Actions template (Software Template) that scaffolds a new microservice with Dockerfile, CI pipeline, and Kubernetes manifests
- The scaffolded repo auto-registers in the Backstage catalog

*Why it impresses:* Shows Platform Engineering thinking; positions the candidate for the next career step beyond entry-level DevOps.

---

## Sources & Verification Log

| Claim | Source URL | Status |
|-------|-----------|--------|
| OpenTofu v1.12.2 | `https://api.github.com/repos/opentofu/opentofu/releases/latest` | ✅ VERIFIED |
| OpenTofu v1.12.0 release date + blog posts | `https://opentofu.org/blog/` (via curl) | ✅ VERIFIED |
| Kubernetes v1.36.2 current, release history | `https://kubernetes.io/releases/` (via curl) + GitHub API | ✅ VERIFIED |
| Terraform v1.15.6 | `https://api.github.com/repos/hashicorp/terraform/releases/latest` | ✅ VERIFIED |
| Helm v4.2.1 | `https://api.github.com/repos/helm/helm/releases/latest` | ✅ VERIFIED |
| Prometheus v3.12.0 | `https://api.github.com/repos/prometheus/prometheus/releases/latest` | ✅ VERIFIED |
| Grafana v13.0.2 | `https://api.github.com/repos/grafana/grafana/releases/latest` | ✅ VERIFIED |
| ArgoCD v3.4.3 | `https://api.github.com/repos/argoproj/argo-cd/releases/latest` | ✅ VERIFIED |
| Docker Engine v29.5.3 | `https://api.github.com/repos/moby/moby/releases/latest` | ✅ VERIFIED |
| containerd v2.3.1 | `https://api.github.com/repos/containerd/containerd/releases/latest` | ✅ VERIFIED |
| Flux v2.8.8 | `https://api.github.com/repos/fluxcd/flux2/releases/latest` | ✅ VERIFIED |
| OTel Collector v1.60.0 | `https://api.github.com/repos/open-telemetry/opentelemetry-collector/releases/latest` | ✅ VERIFIED |
| Backstage v1.51.2 | `https://api.github.com/repos/backstage/backstage/releases/latest` | ✅ VERIFIED |
| HashiCorp Vault v2.0.2 | `https://api.github.com/repos/hashicorp/vault/releases/latest` | ✅ VERIFIED |
| CNCF landscape members (Argo, Flux, Grafana stack, Backstage, OTel) | `https://raw.githubusercontent.com/cncf/landscape/master/landscape.yml` | ✅ VERIFIED |
| Cloud provider market share (AWS #1, Azure #2, GCP #3) | cncf.io, survey.stackoverflow.co — Cloudflare 403 | ⛔ UNVERIFIED via curl |
| GitHub Actions market dominance | No curl-accessible survey data | ⚠️ PARTIAL |
| OpenTofu Fidelity migration story | `https://opentofu.org/blog/` (October 2025 entry) | ✅ VERIFIED |
