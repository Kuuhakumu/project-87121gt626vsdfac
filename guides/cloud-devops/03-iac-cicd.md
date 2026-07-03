# goal 3: infrastructure as code and CI/CD meow

> **~120h total** - your pace, no deadline.
> this is the heart of DevOps: stop clicking in consoles, start defining everything as code.
> IaC + CI/CD is the #1 hireable DevOps skill combo.

[Previous: Goal 2](02-core.md) - [Hub](README.md) - [Next: Goal 4](04-kubernetes-specialization.md)

---

- [ ] **Infrastructure as Code with Terraform/OpenTofu** (~70h)
- [ ] **CI/CD pipelines** (~50h)
- [ ] **exit check** - modules, remote state, GitHub Actions, end-to-end pipeline

## infrastructure as code - Terraform / OpenTofu (~70h)

IaC means your infrastructure is defined in version-controlled files, not hand-built by clicking around a console.
its reproducible, reviewable, and the backbone of DevOps work.

### Terraform vs OpenTofu in 2026

- [ ] **Terraform** is dominant in enterprise. current v1.15. BSL license since 2023.
- [ ] **OpenTofu** is the fully open-source MPL-2 fork, CNCF-adopted, feature-parity v1.12.
- [ ] **for learning, theyre interchangeable.** HCL is the same. OpenTofu is the safe open default; Terraform is what postings still name.

### what to cover

- [ ] HCL syntax: providers, resources, variables, outputs, data sources
- [ ] **state:** `terraform.tfstate`, remote state, S3 + DynamoDB lock, never committing state
- [ ] workflow: `init` -> `plan` -> `apply` -> `destroy`
- [ ] modules: reusable infrastructure components
- [ ] provisioners, `count`, `for_each`, dependencies
- [ ] secrets handling with variables and a secrets manager

always `plan` before `apply`. thats not a superstition; its how u avoid surprise infrastructure changes.

also know Ansible exists: Terraform provisions servers; Ansible configures servers after they exist.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [HashiCorp Tutorials](https://developer.hashicorp.com/terraform/tutorials) | Official | Terraform from zero to modules + remote state | **Free** |
| Terraform labs | [KodeKloud](https://kodekloud.com/) | HCL, state, modules | Freemium |
| [KillerCoda Terraform](https://killercoda.com/) | Web | live-terminal Terraform scenarios | **Free** |

**cert gate:** **HashiCorp Terraform Associate (TA-004, ~$70)** is cheap, high-signal IaC proof. strongly recommended.

**project gate:** provision VPC + subnets + EC2 or equivalent + security groups using modules and remote state. zero console clicks. put it on GitHub.

## CI/CD pipelines (~50h)

CI/CD automates the path from `git push` to running software: build -> test -> deploy.

- [ ] **CI:** lint, build, and test on every push
- [ ] **CD:** ship to staging/prod with gates
- [ ] pipeline stages, jobs, runners, artifacts, caching
- [ ] secrets in pipelines
- [ ] **GitHub Actions:** workflow YAML, triggers, jobs, marketplace actions
- [ ] GitLab CI as alternative; Jenkins as legacy-but-common enterprise tool
- [ ] deployment strategies: blue-green, canary, rolling
- [ ] Docker image build -> registry push -> deploy

GitHub Actions is the best first CI/CD tool. recognize Jenkins, but dont start there unless your target roles demand it.

### labs / theory

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [GitHub Skills](https://skills.github.com/) | GitHub | guided Actions courses inside real repos | **Free** |
| [GitHub Actions docs](https://docs.github.com/actions) | Official | build your first workflow step by step | **Free** |
| GitLab CI/CD tutorials | [GitLab Docs](https://docs.gitlab.com/ee/ci/) | build a `.gitlab-ci.yml` pipeline | **Free** |

**project gate:** build a full pipeline for your containerized app from Goal 2:
`push -> lint -> test -> build Docker image -> push to registry -> deploy to a cloud service or k8s namespace -> smoke test`.
document it with a diagram in the README.

## exit check

- [ ] can write Terraform/OpenTofu for real infrastructure using modules + remote state
- [ ] Terraform Associate passed or scheduled
- [ ] understand provisioning vs configuration management
- [ ] can write a working GitHub Actions pipeline from scratch
- [ ] built end-to-end pipeline: push -> test -> build image -> deploy
- [ ] both projects on GitHub with architecture diagrams

[Next: Goal 4 - Kubernetes & Specialization](04-kubernetes-specialization.md)
