# Goal 4: Kubernetes and specialization meow

> **~160h total** - your pace, no deadline.
> learn Kubernetes, then go deep on **one** track.

[Previous: Goal 3](03-iac-cicd.md) - [Hub](README.md) - [Next: Goal 5](05-job-hunt.md)

---

- [ ] **understand why Kubernetes matters**
- [ ] **Kubernetes fundamentals** (~80h)
- [ ] **pick one specialization** (~80h)
- [ ] **exit check** - deploy/debug K8s app, run clusters, build one signature project

## why Kubernetes

K8s is the clearest differentiator at entry level. most juniors have never run a cluster.
u dont need to be an expert. u need core objects, local cluster reps, app deployment, and broken-pod debugging.

dont stand up a full cloud cluster on day one. learn locally with **k3d**, **kind**, or **minikube** first. free, fast, disposable.

## Kubernetes fundamentals (~80h)

- [ ] **Core objects:** Pod, Deployment, ReplicaSet, Service, ConfigMap, Secret, Namespace, Ingress
- [ ] **Workloads:** Deployment vs StatefulSet vs DaemonSet vs Job/CronJob
- [ ] **`kubectl`:** get, describe, logs, exec, apply, delete, contexts, `-o yaml`, label selectors
- [ ] **Config:** ConfigMaps, Secrets, environment injection, volumes, PVCs
- [ ] **Networking:** Service types, Ingress, cluster DNS
- [ ] **RBAC:** Role, RoleBinding, ServiceAccount
- [ ] **Debugging:** `CrashLoopBackOff`, `ImagePullBackOff`, `Pending`, events from `kubectl describe`
- [ ] **Packaging:** Helm v4

2026 versions: Kubernetes ~v1.36, Helm v4, containerd default runtime. older tutorials may use Docker-as-runtime and Helm v3, so check current docs.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Kubernetes Basics | [killercoda.com](https://killercoda.com/) | browser scenarios: deploy, scale, debug | **Free** |
| Play with Kubernetes | [labs.play-with-k8s.com](https://labs.play-with-k8s.com/) | multi-node cluster in-browser | **Free** |
| Local cluster | [k3d](https://k3d.io/) / [kind](https://kind.sigs.k8s.io/) / [minikube](https://minikube.sigs.k8s.io/) | real cluster on your machine | **Free** |
| KodeKloud K8s | [kodekloud.com](https://kodekloud.com/) | guided labs + CKA/CKAD prep | Freemium |
| killer.sh | [killer.sh](https://killer.sh/) | official CKA/CKAD simulator | bundled w/ exam |

**practice gate:** from an empty cluster, deploy a multi-container app with a Service and ConfigMap, expose it, deliberately break it, and diagnose the failure using `kubectl`.

## pick one specialization (~80h)

go deep on one track. breadth got u here; depth gets u hired.

### Track 1 - Cloud Engineer

- [ ] **focus:** deep AWS/Azure/GCP services, networking, IAM, cost optimization
- [ ] **cert:** AWS SAA-C03, AZ-104, or GCP ACE
- [ ] **signature project:** deploy a multi-tier app via console, then rebuild it entirely in IaC

### Track 2 - Platform / IaC Engineer

- [ ] **focus:** Terraform/OpenTofu modules, Ansible, reusable infrastructure, Backstage
- [ ] **cert:** Terraform Associate (TA-004)
- [ ] **signature project:** provision a full K8s cluster + app on cloud using only IaC

### Track 3 - CI/CD and Release Engineering

- [ ] **focus:** pipeline design, GitHub Actions/GitLab CI, artifact management, GitOps, ArgoCD, deployment strategies
- [ ] **signature project:** lint -> test -> build -> push -> deploy to staging -> smoke test -> promote to prod with ArgoCD doing deploy

### Track 4 - SRE / Observability

- [ ] **focus:** Prometheus, Grafana, OpenTelemetry, SLOs/SLIs, alerting, incident response, post-mortems
- [ ] **reality:** hardest track to enter cold; usually reached through 2-3 years cloud ops
- [ ] **signature project:** OTel -> Prometheus -> Grafana + alertmanager for a sample app, with SLO and alert

### Track 5 - DevSecOps

- [ ] **focus:** IAM least privilege, secret management, Trivy/Snyk, compliance-as-code
- [ ] **signature project:** pipeline with secret scanning, container image scanning, SAST, and managed secrets

## exit check

- [ ] can deploy, expose, scale, and debug an app on Kubernetes from `kubectl`
- [ ] ran a local cluster and a managed one
- [ ] chosen one specialization track and built its signature project
- [ ] optional: CKA or Terraform Associate booked or passed

[Next: Goal 5 - Portfolio & Job Hunt](05-job-hunt.md)
