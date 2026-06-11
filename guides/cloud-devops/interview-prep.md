# 🎯 Interview Prep — Cloud & DevOps (2026)

> Technical + behavioral question bank for **entry cloud/DevOps roles** (Cloud Support, Junior Cloud Engineer, Junior DevOps).
> Don't memorize answers — understand them well enough to whiteboard or talk through them out loud.

[← Hub](README.md) · [Job Hunt](05-job-hunt.md) · [Beyond Entry →](beyond-entry.md)

---

## How entry cloud/DevOps interviews actually run

Typical loop for a first role:
1. **Recruiter screen** — why cloud, what you've built, salary/logistics.
2. **Technical screen** — Linux + networking + cloud fundamentals, often a few "how would you debug…" scenarios.
3. **Hands-on / scenario** — sometimes a live troubleshooting task (a broken pod, a Dockerfile that won't build) or a take-home.
4. **Behavioral** — ownership, incidents, learning fast, working with developers.

For Cloud Support roles specifically, expect **heavy troubleshooting + customer-communication** weighting. For Junior DevOps, expect **more pipeline/IaC depth**.

> You will be asked things you don't know. The right move: **reason out loud, state your assumptions, say how you'd find the answer.** "I'd check the pod events with `kubectl describe`, then the logs" beats silence or a bluff.

---

## Linux & general

1. **What happens when you run a command in the shell?** — PATH lookup → fork/exec → process runs → exit code. Bonus: stdin/stdout/stderr.
2. **A server is slow — how do you investigate?** — `top`/`htop` (CPU/mem), `df -h` (disk full?), `free -m`, `iostat`, check logs in `/var/log`, `dmesg`. Narrow CPU vs memory vs disk vs network.
3. **File permissions: what does `755` mean?** — owner rwx, group r-x, others r-x. `chmod`/`chown`.
4. **Hard link vs symlink?** — hard = same inode; symlink = pointer to a path.
5. **How do you find what's listening on a port?** — `ss -tulpn` (or `netstat -tulpn`), `lsof -i :PORT`.

## Networking

6. **Walk me through what happens when you type a URL and hit enter.** — DNS resolve → TCP handshake → TLS → HTTP request → response → render. Mention each layer.
7. **TCP vs UDP?** — TCP reliable/ordered/connection-based; UDP fire-and-forget, lower latency (DNS, streaming).
8. **What's a subnet / CIDR?** — `/24` = 256 addresses. Be able to explain public vs private subnets in a VPC.
9. **Reverse proxy vs load balancer?** — Reverse proxy fronts servers (TLS, routing, caching); LB distributes traffic across instances. Overlap in practice (nginx, ALB).
10. **What's the difference between a security group and a NACL (AWS)?** — SG = stateful, instance-level; NACL = stateless, subnet-level.

## Cloud

11. **IAM users vs IAM roles — when each?** — Users = long-lived humans/credentials; roles = temporary, assumed by services/instances. **Prefer roles**; avoid long-lived keys.
12. **How do you give an EC2 instance access to an S3 bucket — securely?** — Attach an **IAM role** to the instance (instance profile), not access keys baked into code.
13. **What's a VPC?** — Isolated virtual network: subnets, route tables, gateways, security groups.
14. **Object storage (S3) vs block storage (EBS) vs file storage (EFS)?** — Object = HTTP API, infinitely scalable, not a filesystem; block = a disk for one instance; file = shared POSIX filesystem.
15. **How do you keep cloud costs down?** — Right-size, auto-scale, spot/reserved, billing alarms, tag resources, tear down unused infra. (Cloud Support loves this.)

## Docker

16. **Image vs container?** — Image = immutable template; container = running instance of it.
17. **A container exits immediately — how do you debug?** — `docker logs`, check the `CMD`/`ENTRYPOINT`, run it interactively (`docker run -it … sh`), verify the foreground process doesn't exit.
18. **What's a multi-stage build and why use it?** — Build in one stage, copy only artifacts to a slim final image → smaller, fewer CVEs.
19. **Where do you put secrets in a container?** — **Not** in the image or env baked at build. Inject at runtime via secrets manager / orchestrator secrets.

## Kubernetes

20. **A pod is in `CrashLoopBackOff` — walk me through diagnosing it.** — `kubectl describe pod` (events), `kubectl logs` (+ `--previous`), check liveness/readiness probes, resource limits (OOMKilled?), image/command errors, config/secret mounts.
21. **Pod vs Deployment vs Service?** — Pod = smallest unit; Deployment = manages replicas/rollouts; Service = stable network endpoint for pods.
22. **How does a Service find its pods?** — Label selectors → endpoints. Types: ClusterIP, NodePort, LoadBalancer.
23. **What's a liveness vs readiness probe?** — Liveness = restart if unhealthy; readiness = remove from Service until ready.
24. **ConfigMap vs Secret?** — Both inject config; Secrets are base64 (not encrypted by default — enable encryption at rest / external secrets).

## CI/CD & IaC

25. **Describe a CI/CD pipeline from `git push` to production.** — Trigger → lint → test → build image → push to registry → deploy to staging → smoke test → promote/approve → prod. Mention rollback.
26. **`terraform plan` vs `apply` — why always plan first?** — Plan shows the diff before changing real infra; apply executes it. Plan = your safety review.
27. **What is Terraform state and what breaks it?** — State maps config → real resources. Breaks: manual console changes (drift), local state without locking, lost/corrupt state. Fix: **remote state + locking** (S3+DynamoDB / TF Cloud).
28. **What is GitOps?** — Git is the source of truth for infra/deploys; a controller (ArgoCD/Flux) continuously syncs the cluster to the repo. Change = a PR, not a manual `kubectl apply`.
29. **Blue-green vs canary deployment?** — Blue-green = two full envs, switch traffic at once; canary = shift a small % first, watch, then ramp.

## Observability

30. **What are the three pillars of observability?** — Metrics, logs, traces. (OpenTelemetry → Prometheus → Grafana is the modern stack.)
31. **What's an SLO/SLI/error budget?** — SLI = a measured signal (e.g. latency); SLO = target (99.9%); error budget = allowed failure before you stop shipping and fix reliability.

---

## Behavioral (use STAR: Situation, Task, Action, Result)

- **"Something you deployed broke in production — what did you do?"** — Show calm triage: detect → mitigate (rollback) → root-cause → prevent (postmortem, no blame).
- **"A manual process you automated — what was the impact?"** — Quantify ("cut deploy from 30 min manual to a 3-min pipeline").
- **"A time you had to learn a new tool fast."** — Show your learning method (docs-first, build a small project).
- **"You disagreed with a developer about a deploy/process."** — Show you collaborate, not gatekeep. DevOps is a culture, not a wall.
- **"Tell me about a hard bug."** — Structured debugging, how you narrowed it down.

---

## Questions to ask *them* (you're being judged on these too)

- "What does your deployment pipeline look like today?"
- "On-call rotation — how's it structured for someone junior?"
- "How much is run on IaC vs clicked in the console?"
- "What would my first 90 days look like?"

---

## Final-week checklist

- [ ] Can explain DNS → TCP → TLS → HTTP out loud
- [ ] Can debug a `CrashLoopBackOff` and a dead container step by step
- [ ] Can explain IAM roles vs users and *why roles*
- [ ] Can describe a full CI/CD pipeline + a rollback strategy
- [ ] Can explain Terraform state + remote state/locking
- [ ] 3–4 STAR stories rehearsed (incident, automation, fast learning, collaboration)
- [ ] One portfolio project you can screen-share and walk through end to end

---

*Last verified: June 2026. Tooling/versions in answers reflect the 2026 stack — see [resources.md](resources.md).*
