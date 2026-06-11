# 🎯 Phase 4: Kubernetes & Specialization

> **~160 hrs total** · your pace, no deadline
> Learn Kubernetes (the field's biggest differentiator), then go deep on **one** track.

[← Phase 3](03-iac-cicd.md) · [Hub](README.md) · [Next: Phase 5 →](05-job-hunt.md)

---

## Why Kubernetes

K8s is the clearest **differentiator** at entry level — most juniors have never run a cluster, so even basic fluency plus a local lab sets you apart. You don't need to be an expert. You need to understand the core objects, run a local cluster, deploy an app, and debug a broken pod.

> **Don't stand up a full cloud cluster on day one.** Learn locally first with **k3d**, **kind**, or **minikube** — free, fast, disposable. Move to managed (EKS/AKS/GKE) only once the concepts click.

---

## Kubernetes fundamentals (~80 hrs)

**Cover:**
- **Core objects:** Pod, Deployment, ReplicaSet, Service (ClusterIP / NodePort / LoadBalancer), ConfigMap, Secret, Namespace, Ingress
- **Workloads:** Deployment vs StatefulSet vs DaemonSet vs Job/CronJob — when each applies
- **`kubectl`:** get/describe/logs/exec/apply/delete, contexts, `-o yaml`, label selectors
- **Config:** ConfigMaps & Secrets, environment injection, volumes & PersistentVolumeClaims
- **Networking:** Service types, basic Ingress, DNS inside the cluster
- **RBAC:** Role, RoleBinding, ServiceAccount — the relationship
- **Debugging:** diagnosing `CrashLoopBackOff`, `ImagePullBackOff`, `Pending`; reading events with `kubectl describe`
- **Packaging:** **Helm v4** (note: v4 has breaking changes from v3 — follow current docs, not old tutorials)

> **2026 versions:** Kubernetes ~v1.36, Helm **v4** (major bump), containerd is the default runtime. Tutorials from 2021–2023 may use Docker-as-runtime and Helm v3 — verify against current docs.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Kubernetes Basics | [killercoda.com](https://killercoda.com/) | Browser scenarios: deploy, scale, debug on a live cluster | **Free** |
| Play with Kubernetes | [labs.play-with-k8s.com](https://labs.play-with-k8s.com/) | Spin up a multi-node cluster in-browser | **Free** |
| Local cluster | [k3d](https://k3d.io/) / [kind](https://kind.sigs.k8s.io/) / [minikube](https://minikube.sigs.k8s.io/) | Run a real cluster on your own machine | **Free** |
| KodeKloud K8s | [kodekloud.com](https://kodekloud.com/) | Guided labs + the popular CKA/CKAD prep | Freemium |
| killer.sh | [killer.sh](https://killer.sh/) | The official CKA/CKAD exam simulator (if you pursue the cert) | Bundled w/ exam |

**Practice gate:** from an empty cluster, deploy a multi-container app with a Service and ConfigMap, expose it, then deliberately break it and diagnose the failure from `kubectl` alone.

---

## Pick ONE specialization (~80 hrs)

Go deep on one track. Breadth got you this far; depth is what gets you hired.

### Track 1 — Cloud Engineer (provider depth)
**Focus:** deep AWS/Azure/GCP services, networking, IAM, cost optimization.
**Cert:** AWS SAA-C03 (or AZ-104 / GCP ACE).
**Signature project:** deploy a multi-tier app (web + DB + CDN) via the console, then rebuild it entirely in IaC.

### Track 2 — Platform / IaC Engineer
**Focus:** Terraform/OpenTofu modules, Ansible, reusable infrastructure, internal platforms (Backstage).
**Cert:** Terraform Associate (TA-004, $70).
**Signature project:** provision a full K8s cluster + app on a cloud using **only** IaC — zero console clicks.

### Track 3 — CI/CD & Release Engineering
**Focus:** pipeline design, GitHub Actions/GitLab CI, artifact management, GitOps (**ArgoCD** primary, Flux alternative), deployment strategies (blue-green, canary).
**Signature project:** full pipeline — lint → test → build image → push → deploy to staging → smoke test → promote to prod on approval, with ArgoCD doing the deploy.

### Track 4 — SRE / Observability
**Focus:** Prometheus, Grafana, **OpenTelemetry** (now the standard — not ELK), SLOs/SLIs, alerting, incident response, post-mortems.
**Reality:** hardest track to enter cold — usually reached via 2–3 yrs of cloud ops first.
**Signature project:** full observability stack (OTel → Prometheus → Grafana + alertmanager) for a sample app; define an SLO and an alert that fires on breach.

### Track 5 — DevSecOps
**Focus:** IAM least-privilege, secret management (cloud-native first, then Vault), security scanning in pipelines (Trivy, Snyk), compliance-as-code.
**Signature project:** add secret scanning + container image scanning (Trivy) + SAST to a pipeline; replace env-var secrets with a managed secrets store.

---

## Phase 4 exit checklist
- [ ] Can deploy, expose, scale, and debug an app on Kubernetes from `kubectl`
- [ ] Ran a local cluster (k3d/kind/minikube) and a managed one
- [ ] Chosen ONE specialization track and built its signature project
- [ ] (Optional) CKA or Terraform Associate booked or passed

Next: [Phase 5 — Portfolio & Job Hunt →](05-job-hunt.md)
