# 📁 Phase 1: Foundations — Linux, Networking, Git & Scripting

> **~140 hrs total** · your pace, no deadline
> Goal: real comfort in a Linux shell, solid networking mental model, Git fluency, and one scripting language. Cloud and DevOps tools all sit on top of these. Skip this and everything later feels like magic you can't debug.

[← Phase 0](00-prep.md) · [Hub](README.md) · [Next: Phase 2 →](02-core.md)

---

## Linux (~50 hrs)

This is the single most important foundation. You'll spend your whole career in a Linux shell.

**Cover:** filesystem hierarchy (`/etc`, `/var`, `/home`, `/proc`), navigation (`cd`, `ls`, `pwd`), file ops (`cp`, `mv`, `rm`, `mkdir`, `find`), viewing/editing (`cat`, `less`, `nano`, `vim` basics), permissions (`chmod`, `chown`, octal 755/644), users & groups (`sudo`, `/etc/passwd`), processes (`ps`, `top`, `htop`, `kill`, `&`, `jobs`), services (`systemctl` start/stop/enable/status), packages (`apt`/`yum`/`dnf`), text processing (`grep`, `awk`, `sed`, pipes `|`, redirection `>`/`>>`), `cron`, environment variables, SSH (`ssh`, keys, `scp`).

**Theory:** [Linux Journey](https://labex.io/linuxjourney) (freemium) · [The Missing Semester (MIT)](https://missing.csail.mit.edu/) · NetworkChuck Linux series.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [OverTheWire — Bandit](https://overthewire.org/wargames/bandit/) | Web | SSH into real boxes; learn the CLI by solving 30+ puzzles | **Free** |
| [Linux Journey](https://labex.io/linuxjourney) | Web | Guided lessons + exercises, beginner → intermediate | **Freemium** |
| Linux Fundamentals 1–3 | [TryHackMe](https://tryhackme.com/) | In-browser Linux VMs: filesystem, permissions, cron, SSH | Free tier |
| [KillerCoda Linux scenarios](https://killercoda.com/) | Web | Live in-browser terminal playgrounds, no setup | **Free** |

**Practice gate:** you can navigate, manage permissions and processes, write a `cron` job, and SSH into a remote box — without looking things up.

---

## Networking

You can't debug cloud infra if you don't understand the network underneath it.

**Cover:** OSI & TCP/IP models, IP addressing & subnetting (CIDR — `/24`, `/16`), public vs private IPs, DNS (records, resolution flow), DHCP, HTTP/HTTPS, TLS/SSL (certs, handshake), SSH, key ports (22, 53, 80, 443, 3389), NAT, firewalls & security groups, **load balancers**, **forward vs reverse proxy**, VPN basics. These map directly onto cloud VPCs.

**Theory:** [PowerCert](https://www.youtube.com/@PowerCertAnimatedVideos) · [Practical Networking](https://www.practicalnetworking.net/) · NetworkChuck.

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Intro to Networking | [TryHackMe](https://tryhackme.com/) | OSI, ping, traceroute interactively | Free tier |
| Computer Networking (full course) | [freeCodeCamp YouTube](https://www.youtube.com/c/Freecodecamp) | Comprehensive networking fundamentals | **Free** |
| [SubnettingPractice.com](https://subnetipv4.com/) | Web | `/24`–`/30` drills until automatic | **Free** |

**Practice gate:** you can subnet a CIDR block on paper, explain DNS resolution end-to-end, and describe what a load balancer and a reverse proxy each do.

---

## Git & GitHub

Everything-as-code means everything lives in Git. There's no getting around it.

**Cover:** `init`, `add`, `commit` (good messages), `push`/`pull`, branching, merging, **resolving merge conflicts**, `.gitignore`, pull requests, forking, tags, `rebase` basics. Understand Git (tool) vs GitHub/GitLab (host). Bonus: what a GitOps workflow is (you'll use it in Phase 4).

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Learn Git Branching](https://learngitbranching.js.org/) | Web | ~50 visual puzzles: commit, branch, merge, rebase | **Free** |
| [GitHub Skills](https://skills.github.com/) | GitHub | Guided courses inside real repos (PRs, Actions) | **Free** |

**Practice gate:** create a repo, branch, open a PR, resolve a merge conflict, and explain rebase vs merge.

---

## A scripting language (Python or Bash)

Automation is the heart of the job — you need to be able to *read* and *write* scripts.

**Bash** (start here): variables, loops, conditionals, functions, exit codes, arguments (`$1`, `$@`), pipes, `if`/`case`, writing a script that automates a real task (backup, log rotation, health check).

**Python** (the top recommendation for anything beyond glue): variables, data types, control flow, functions, file I/O, `requests` (call APIs), JSON parsing, `boto3` (the AWS SDK) basics. Python is what you'll use for real cloud automation.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Language track | [Exercism](https://exercism.org/) | Bash & Python exercises with **free human mentorship** | **Free** |
| [freeCodeCamp](https://www.freecodecamp.org/learn) | Web | Python fundamentals, in-browser | **Free** |
| Shell scripting | [The Missing Semester](https://missing.csail.mit.edu/) | Real-world shell scripting & automation | **Free** |

**Project:** write a Bash or Python script that automates something real — e.g. checks a list of URLs and reports which are down, or parses a log file and summarizes errors. Put it on GitHub with a README.

---

## Phase 1 exit checklist
- [ ] Comfortable in a Linux shell: permissions, processes, services, cron, text processing
- [ ] Can subnet, explain DNS, and describe load balancers / reverse proxies
- [ ] Git/GitHub fluent: branch, PR, conflict resolution
- [ ] Can write a useful Bash or Python automation script
- [ ] 1–2 small automation scripts on GitHub with READMEs

Next: [Phase 2 — Cloud Core & Containers →](02-core.md)
