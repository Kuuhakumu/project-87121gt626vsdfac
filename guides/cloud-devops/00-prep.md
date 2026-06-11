# ⚙️ Phase 0: Pre-Flight Setup

> **Day 1 — non-negotiable.** Just sign up and install — no learning to finish, do it before Phase 1.

[← Back to hub](README.md) · [Next: Phase 1 →](01-foundations.md)

---

## The honest career path (read this twice)

**"DevOps Engineer" is almost never a first job.** DevOps bridges development and operations — which means it assumes you already know one side. The reliable on-ramp looks like this:

```
[Zero experience]
      ↓
Cloud Support Associate · Cloud Ops Analyst · IT/helpdesk with cloud exposure
   (6–18 months: real AWS/Azure exposure, scripting, tickets, incidents)
      ↓
Junior Cloud Engineer · Associate Cloud Engineer
   (1–2 years: IaC, CI/CD, containers, automation projects)
      ↓
Cloud Engineer · DevOps Engineer · Platform Engineer
   (2–4 years: full ownership of pipelines, infra, observability)
      ↓
SRE · Senior Platform Engineer · Cloud Architect (4+ years)
```

So the guide's real target is **your first cloud role** — Cloud Support Associate or Junior/Associate Cloud Engineer — with the skills to grow into DevOps fast. Titles that aren't realistic from zero: "DevOps Engineer" (no level), "Platform Engineer", "SRE". Don't waste applications on them yet.

## Mindset & expectations

- **Breadth then depth.** Get a working grasp of Linux, networking, one cloud, containers, and pipelines — then go deep on one track.
- **Hands-on beats certs.** A cert gets your resume past the filter; a *deployed, automated, observable project* gets you the offer. Do both, in that order of priority.
- **Automate everything you do twice.** That instinct *is* the job.
- **Consistency beats intensity.** Two focused hours a day beats a weekend binge once a month.

## Pace & timeline

Estimated hours: **~500–700 hours**.

| Pace | Hours/week | ~Time to job-ready |
|---|---|---|
| Casual | 5–8 | 16–22 months |
| Part-time (recommended) | 10–15 | 10–16 months |
| Full-time | 20–30 | 7–11 months |

---

##  Setting up Accounts

Create these now (all free):

1. **AWS Free Tier** — [aws.amazon.com/free](https://aws.amazon.com/free/). 12 months of free-tier services + always-free items. **Set a billing alarm immediately** 
2. **GitHub** — [github.com](https://github.com/) — your portfolio lives here. Also unlocks GitHub Actions (free CI/CD minutes) and GitHub Codespaces (60 free core-hours/mo).
3. **A code editor** — [VS Code](https://code.visualstudio.com/) with the AWS, Docker, and HashiCorp Terraform extensions.
4. *(Optional)* Azure free account and Google Cloud free trial — you only need **one** cloud to start; add others later.

> 💡 **Pick one cloud to learn first.** AWS has the most jobs and the most learning material — this guide leads with AWS but the concepts transfer. Don't try to learn three clouds at once.

##  Free orientation

- [AWS Cloud Practitioner Essentials](https://aws.amazon.com/training/) (free digital course) — a solid big-picture tour of what cloud actually is.
- [roadmap.sh/devops](https://roadmap.sh/devops) — the visual DevOps roadmap. Bookmark it; it'll be your map for the whole journey.
- Skim the [tooling & trends summary](README.md#-what-makes-this-guide-different) so you're studying current tools (Kubernetes 1.36, OpenTofu, Helm v4) not retired ones.

##  Tooling & community

- **Local terminal:** on Windows, install [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install) (Ubuntu) so you get a real Linux shell. macOS/Linux already have one.
- **Notes system:** [Obsidian](https://obsidian.md/) or any markdown notes — you'll accumulate commands, gotchas, and cheat-sheets for a year.
- **Communities:** r/devops, r/aws, r/kubernetes (read the wikis first), the CNCF Slack, and the Platform Engineering community.

---

✅ **Exit check:** AWS Free Tier active with a billing alarm planned, GitHub + VS Code ready, a real Linux shell available, you understand that cloud-support/ops is the realistic first role, and roadmap.sh/devops is bookmarked.

[← Back to hub](README.md) · [Next: Phase 1 — Foundations →](01-foundations.md)
