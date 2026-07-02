# Interview prep - Cloud & DevOps meow

> technical + behavioral question bank for entry cloud/DevOps roles.
> dont memorize answers. understand them well enough to talk through out loud.

[Hub](README.md) - [Job Hunt](05-job-hunt.md) - [Beyond Entry](beyond-entry.md)

---

- [ ] **know the interview loop**
- [ ] **practice Linux + networking questions**
- [ ] **practice cloud + Docker + Kubernetes questions**
- [ ] **practice CI/CD + IaC + observability questions**
- [ ] **prepare STAR stories**
- [ ] **ask good questions**
- [ ] **finish the final-week checklist**

## how entry interviews run

- [ ] **Recruiter screen:** why cloud, what youve built, logistics.
- [ ] **Technical screen:** Linux, networking, cloud fundamentals, troubleshooting.
- [ ] **Hands-on / scenario:** broken pod, broken Dockerfile, or take-home.
- [ ] **Behavioral:** ownership, incidents, learning fast, working with developers.

Cloud Support roles lean troubleshooting + customer communication. Junior DevOps leans pipeline/IaC depth.

u will be asked things u dont know. reason out loud, state assumptions, say how youd find the answer. that beats bluffing.

## Linux and networking

- [ ] what happens when u run a command in the shell?
- [ ] server is slow - how do u investigate?
- [ ] file permissions: what does `755` mean?
- [ ] hard link vs symlink?
- [ ] how do u find whats listening on a port?
- [ ] what happens when u type a URL and hit Enter?
- [ ] TCP vs UDP?
- [ ] what is subnet/CIDR?
- [ ] reverse proxy vs load balancer?
- [ ] AWS security group vs NACL?

## cloud, Docker, and Kubernetes

- [ ] IAM users vs IAM roles - when each?
- [ ] how do u give EC2 access to S3 securely?
- [ ] what is a VPC?
- [ ] S3 vs EBS vs EFS?
- [ ] how do u keep cloud costs down?
- [ ] image vs container?
- [ ] container exits immediately - how debug?
- [ ] multi-stage build and why use it?
- [ ] where do secrets go in containers?
- [ ] pod in `CrashLoopBackOff` - diagnose it.
- [ ] Pod vs Deployment vs Service?
- [ ] how does a Service find pods?
- [ ] liveness vs readiness probe?
- [ ] ConfigMap vs Secret?

## CI/CD, IaC, and observability

- [ ] describe CI/CD from `git push` to production.
- [ ] `terraform plan` vs `apply` - why plan first?
- [ ] what is Terraform state and what breaks it?
- [ ] what is GitOps?
- [ ] blue-green vs canary deployment?
- [ ] three pillars of observability?
- [ ] SLO vs SLI vs error budget?

## behavioral prompts

use STAR: Situation, Task, Action, Result.

- [ ] something u deployed broke in production - what did u do?
- [ ] manual process u automated - what was the impact?
- [ ] time u learned a new tool fast.
- [ ] disagreed with a developer about a deploy/process.
- [ ] tell me about a hard bug.

## questions to ask them

- [ ] what does your deployment pipeline look like today?
- [ ] how is on-call structured for someone junior?
- [ ] how much is IaC vs clicked in the console?
- [ ] what would my first 90 days look like?

## final-week checklist

- [ ] can explain DNS -> TCP -> TLS -> HTTP out loud
- [ ] can debug `CrashLoopBackOff` and a dead container step by step
- [ ] can explain IAM roles vs users and why roles
- [ ] can describe CI/CD + rollback strategy
- [ ] can explain Terraform state + remote state/locking
- [ ] 3-4 STAR stories rehearsed
- [ ] one portfolio project ready to screen-share end to end

---

*Last verified: June 2026. Tooling/versions reflect the 2026 stack - see [resources.md](resources.md).*
