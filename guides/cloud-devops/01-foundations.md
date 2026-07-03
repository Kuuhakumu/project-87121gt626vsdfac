# goal 1: foundations - Linux, networking, Git, scripting meow

> **~140h total** - your pace, no deadline.
> goal: Linux shell comfort, networking mental model, Git fluency, and one scripting language.
> cloud and DevOps tools sit on top of this. skip it and later tools feel like magic u cant debug.

[Previous: Goal 0](00-prep.md) - [Hub](README.md) - [Next: Goal 2](02-core.md)

---

- [ ] **Linux** (~50h)
- [ ] **networking** (~35h)
- [ ] **Git + GitHub** (~20h)
- [ ] **Bash or Python scripting** (~35h)
- [ ] **exit check** - Linux, subnetting/DNS, Git, automation scripts

## Linux (~50h)

this is the single most important foundation. youll spend your whole career in a Linux shell.

**cover:** filesystem hierarchy, navigation, file ops, viewing/editing, permissions, users/groups, processes, services, packages, text processing, `cron`, environment variables, SSH.

**theory:** [Linux Journey](https://labex.io/linuxjourney) (freemium), [The Missing Semester (MIT)](https://missing.csail.mit.edu/), NetworkChuck Linux series. **⚠️ TODO verify exact NetworkChuck Linux video/playlist before using it as a primary instruction.**

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [OverTheWire - Bandit](https://overthewire.org/wargames/bandit/) | Web | SSH into real boxes; learn CLI by solving puzzles | **Free** |
| [Linux Journey](https://labex.io/linuxjourney) | Web | guided lessons + exercises | **Freemium** |
| Linux Fundamentals 1-3 | [TryHackMe](https://tryhackme.com/) | in-browser Linux VMs | Free tier |
| [KillerCoda Linux scenarios](https://killercoda.com/) | Web | live browser terminal playgrounds | **Free** |

**practice gate:** navigate, manage permissions/processes, write a `cron` job, and SSH into a remote box without looking things up.

## networking (~35h)

u cant debug cloud infra if u dont understand the network underneath it.

**cover:** OSI/TCP-IP, IP addressing, CIDR, public/private IPs, DNS, DHCP, HTTP/HTTPS, TLS/SSL, SSH, ports 22/53/80/443/3389, NAT, firewalls/security groups, load balancers, forward vs reverse proxy, VPN basics.

**theory:** PowerCert, Practical Networking, NetworkChuck. **⚠️ TODO verify exact videos/playlists before making these primary instructions.**

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Intro to Networking | [TryHackMe](https://tryhackme.com/) | OSI, ping, traceroute interactively | Free tier |
| Computer Networking full course | freeCodeCamp YouTube **⚠️ TODO verify exact video** | comprehensive networking fundamentals | **Free** |
| [subnetipv4.com](https://subnetipv4.com/) | Web | `/24`-`/30` drills until automatic | **Free** |

**practice gate:** subnet a CIDR block on paper, explain DNS resolution end-to-end, and describe what a load balancer and reverse proxy each do.

## Git and GitHub (~20h)

everything-as-code means everything lives in Git. no getting around it.

**cover:** `init`, `add`, `commit`, `push`/`pull`, branching, merging, conflicts, `.gitignore`, pull requests, forking, tags, `rebase` basics, Git vs GitHub/GitLab, GitOps basics.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Learn Git Branching](https://learngitbranching.js.org/) | Web | visual puzzles: commit, branch, merge, rebase | **Free** |
| [GitHub Skills](https://skills.github.com/) | GitHub | guided courses inside real repos | **Free** |

**practice gate:** create a repo, branch, open a PR, resolve a merge conflict, and explain rebase vs merge.

## Bash or Python scripting (~35h)

automation is the heart of the job. u need to read and write scripts.

- [ ] **Bash:** variables, loops, conditionals, functions, exit codes, arguments, pipes, `if`/`case`.
- [ ] **Python:** variables, data types, control flow, functions, file I/O, `requests`, JSON, `boto3` basics.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Language track | [Exercism](https://exercism.org/) | Bash and Python exercises with free mentorship | **Free** |
| [freeCodeCamp](https://www.freecodecamp.org/learn) | Web | Python fundamentals, in-browser | **Free** |
| Shell scripting | [The Missing Semester](https://missing.csail.mit.edu/) | real-world shell scripting and automation | **Free** |

**project gate:** write a Bash or Python script that automates something real, like checking URLs or parsing logs. put it on GitHub with a README.

## exit check

- [ ] comfortable in Linux shell: permissions, processes, services, cron, text processing
- [ ] can subnet, explain DNS, and describe load balancers / reverse proxies
- [ ] Git/GitHub fluent: branch, PR, conflict resolution
- [ ] can write a useful Bash or Python automation script
- [ ] 1-2 small automation scripts on GitHub with READMEs

[Next: Goal 2 - Cloud Core & Containers](02-core.md)
