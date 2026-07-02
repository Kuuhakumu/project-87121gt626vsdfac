# Goal 2: cloud core and containers meow

> **~180h total** - your pace, no deadline.
> pick **one** cloud provider and go deep.
> learn Docker beside it. by the end, u have first cert readiness and real deployable skills.

[Previous: Goal 1](01-foundations.md) - [Hub](README.md) - [Next: Goal 3](03-iac-cicd.md)

---

- [ ] **pick one cloud** (~5h)
- [ ] **cloud fundamentals + first cert** (~90h)
- [ ] **Docker and containers** (~90h)
- [ ] **exit check** - core cloud services, billing alarm, Dockerfile/Compose, multi-service app

## pick one cloud (~5h)

| Provider | Pick it if... | First cert |
|---|---|---|
| **AWS** | u want most openings and widest recognition | CLF-C02 -> SAA-C03 |
| **Azure** | u target enterprise / Microsoft-heavy shops | AZ-900 -> AZ-104 |
| **GCP** | u target data/ML-heavy or GCP-native companies | Cloud Digital Leader -> ACE |

most beginners should pick AWS. concepts transfer: compute, storage, networking, IAM.

## cloud fundamentals + first cert (~90h)

AWS is the example path. Azure/GCP equivalents live in [certifications.md](certifications.md).

- [ ] **Compute:** EC2, AMIs, instance types, Lambda basics
- [ ] **Storage:** S3, storage classes, versioning, EBS
- [ ] **Networking:** VPC, public/private subnets, security groups, route tables, internet/NAT gateways, Elastic IPs
- [ ] **Identity:** IAM users, groups, roles, policies, least privilege
- [ ] **Databases:** RDS basics, DynamoDB awareness
- [ ] **Monitoring:** CloudWatch metrics/logs/alarms, billing alarms
- [ ] **big concepts:** regions, availability zones, shared responsibility, well-architected pillars

set a billing alarm on day one. a stopped-but-not-terminated instance or forgotten NAT gateway can still cost u.

### theory / courses

- [ ] [AWS Skill Builder](https://skillbuilder.aws/) - official free tier; Cloud Practitioner Essentials.
- [ ] freeCodeCamp AWS Cloud Practitioner full course on YouTube. **⚠️ TODO verify exact video before primary use.**
- [ ] [Microsoft Learn](https://learn.microsoft.com/training/) for Azure.
- [ ] [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) for GCP.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [AWS Free Tier](https://aws.amazon.com/free/) | AWS | launch EC2, create S3, set up VPC, configure IAM | **Free** |
| AWS Cloud Quest | [AWS Skill Builder](https://skillbuilder.aws/) | gamified hands-on cloud role-play | Free tier |
| [Microsoft Learn sandboxes](https://learn.microsoft.com/training/) | MS Learn | free Azure sandbox environments | **Free** |
| [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) | Google | Qwiklabs-style GCP labs | Freemium |

**cert gate:** 85%+ on practice exams before booking CLF-C02, then SAA-C03. Tutorials Dojo / Stephane Maarek are common standards, but verify current course/exam versions before buying.

## Docker and containers (~90h)

containers are the unit of modern deployment. get fluent before Kubernetes.

- [ ] container vs VM
- [ ] images vs containers; layer model
- [ ] `Dockerfile`: `FROM`, `RUN`, `COPY`, `CMD`, `ENTRYPOINT`, `EXPOSE`, multi-stage builds
- [ ] `docker build`, `run`, `ps`, `logs`, `exec`, `stop`, `rm`
- [ ] volumes and bind mounts
- [ ] container networking and port mapping
- [ ] Docker Compose YAML
- [ ] registries: Docker Hub, ECR/ACR/GCR
- [ ] image optimization: cache, `.dockerignore`, small base images

there is **no current Docker certification**. Docker DCA was discontinued. prove Docker through projects.

### theory

- [Docker official getting-started](https://docs.docker.com/get-started/)
- NetworkChuck Docker series **⚠️ TODO verify exact video/playlist**
- freeCodeCamp Docker course on YouTube **⚠️ TODO verify exact video**

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Play with Docker](https://labs.play-with-docker.com/) | Web | full Docker playground in-browser | **Free** |
| [KillerCoda Docker scenarios](https://killercoda.com/) | Web | guided Docker scenarios in live terminal | **Free** |
| Docker labs | [KodeKloud](https://kodekloud.com/) | Docker + Dockerfile labs | Freemium |

**project gate:** containerize a small web app with a Dockerfile, use Docker Compose with a database, push image to a registry, and document it on GitHub.

## exit check

- [ ] one cloud providers core services understood
- [ ] Cloud Practitioner-level cert passed, ideally Associate started or passed
- [ ] billing alarm set; comfortable in free tier
- [ ] can write a Dockerfile and `docker-compose.yml` from scratch
- [ ] containerized a real multi-service app and pushed it to a registry

[Next: Goal 3 - IaC & CI/CD](03-iac-cicd.md)
