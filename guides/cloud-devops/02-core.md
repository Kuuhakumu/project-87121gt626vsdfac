# 🌐 Phase 2: Cloud Core & Containers

> **~180 hrs total** · your pace, no deadline
> Pick **one** cloud provider and go deep on it. Learn Docker alongside it. By the end of this phase you'll have your first cert and real deployable skills.

[← Phase 1: Foundations](01-foundations.md) · [Hub](README.md) · [Next: Phase 3 →](03-iac-cicd.md)

---

## Pick one cloud — don't spread thin

| Provider | Pick it if… | First cert |
|---|---|---|
| **AWS** | You want the most job openings & widest recognition (the default) | CLF-C02 → SAA-C03 |
| **Azure** | You're targeting enterprise / Microsoft-heavy shops | AZ-900 → AZ-104 |
| **GCP** | You're targeting data/ML-heavy or GCP-native companies | Cloud Digital Leader → ACE |

> **Most beginners should pick AWS** — it has the largest job market and the most learning material. The concepts (compute, storage, networking, IAM) transfer to any cloud, so you're not locked in. See [certifications.md](certifications.md) for full exam data.

---

## Cloud fundamentals + first cert (~90 hrs)

Targeting **AWS** as the example (Azure/GCP equivalents in [certifications.md](certifications.md)).

### What to cover (the essential services)
- **Compute:** EC2 (instances, AMIs, instance types), Lambda (serverless basics)
- **Storage:** S3 (buckets, storage classes, versioning), EBS volumes
- **Networking:** VPC, subnets (public/private), security groups, route tables, internet/NAT gateways, Elastic IPs
- **Identity:** IAM (users, groups, roles, policies — **least privilege**), the difference between a role and a user
- **Databases:** RDS basics, DynamoDB awareness
- **Monitoring:** CloudWatch (metrics, logs, alarms), billing alarms (**set one immediately**)
- **The big concepts:** regions & availability zones, the **shared responsibility model**, the well-architected pillars

> 💰 **Set a billing alarm on day one** and use the free tier. It's easy to accidentally run up a bill — a stopped-but-not-terminated instance or a forgotten NAT gateway will cost you.

### Theory / courses
- [AWS Skill Builder](https://skillbuilder.aws/) — official, free tier (Cloud Practitioner Essentials)
- freeCodeCamp AWS Cloud Practitioner full course (YouTube, free)
- [Microsoft Learn](https://learn.microsoft.com/training/) (free, for Azure path) · [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) (GCP path)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [AWS Free Tier](https://aws.amazon.com/free/) | AWS | Launch EC2, create an S3 bucket, set up a VPC, configure IAM | **Free** (12 mo) |
| AWS Cloud Quest | [AWS Skill Builder](https://skillbuilder.aws/) | Gamified hands-on cloud role-play | Free tier |
| [Microsoft Learn sandboxes](https://learn.microsoft.com/training/) | MS Learn | Free Azure sandbox environments (no card) | **Free** |
| [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) | Google | Qwiklabs-style hands-on GCP labs | Freemium |

**Cert gate:** 85%+ on practice exams (Tutorials Dojo / Stephane Maarek on Udemy are the community standards) before booking CLF-C02, then SAA-C03.

---

## Docker & containers (~90 hrs)

Containers are the unit of modern deployment. Get fluent here before moving to Kubernetes.

### What to cover
- What a container is vs a VM (and why it matters)
- Images vs containers; the image layer model
- Writing a **Dockerfile** (`FROM`, `RUN`, `COPY`, `CMD` vs `ENTRYPOINT`, `EXPOSE`, multi-stage builds)
- `docker build`, `run`, `ps`, `logs`, `exec`, `stop`, `rm`
- Volumes (persistent data) and bind mounts
- Container networking; port mapping
- **Docker Compose** — define multi-container apps in YAML
- Registries: pushing/pulling from Docker Hub or a cloud registry (ECR/ACR/GCR)
- Image optimization: layer caching, `.dockerignore`, small base images (alpine, distroless)

> **2026 note:** there is **no current Docker certification** (the DCA was discontinued). Don't chase one — Docker skill is proven through projects and tested indirectly via the Kubernetes certs (CKAD/CKA). Current Docker Engine is v29.x; containerd is the underlying runtime.

### Theory
- [Docker official getting-started](https://docs.docker.com/get-started/) · NetworkChuck Docker series · freeCodeCamp Docker course (YouTube)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Play with Docker](https://labs.play-with-docker.com/) | Web | Full Docker playground in-browser, no install | **Free** |
| [KillerCoda Docker scenarios](https://killercoda.com/) | Web | Guided Docker scenarios in a live terminal | **Free** |
| Docker labs | [KodeKloud](https://kodekloud.com/) | Hands-on Docker + Dockerfile labs (free tier) | Freemium |

**Project:** containerize a small web app (any language) with a Dockerfile, then use Docker Compose to run it with a database (e.g. app + Postgres). Push the image to a registry. Put it on GitHub.

---

## Phase 2 exit checklist
- [ ] One cloud provider's core services understood (compute, storage, networking, IAM, monitoring)
- [ ] Cloud Practitioner-level cert passed (CLF-C02 / AZ-900 / CDL), ideally Associate (SAA-C03 / AZ-104 / ACE)
- [ ] Billing alarm set; comfortable in the free tier
- [ ] Can write a Dockerfile and a docker-compose.yml from scratch
- [ ] Containerized a real multi-service app and pushed it to a registry

Next: [Phase 3 — IaC & CI/CD →](03-iac-cicd.md)
