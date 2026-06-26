# Goal 1: Foundations — Hardware & Operating Systems meow (~140h)

> **goal:** the IT bedrock security sits on — if u dont know how computers/OS/networking work normally, u cant tell whats abuse and whats normal meow

**Total: ~140 hours** (≈ 10–12 weeks at 2h/day). this goal maps to **CompTIA A+ (220-1201 / 220-1202)** domains. if u already work in IT support, u can test out fast and jump to [Goal 2](02-core.md).

[← Prep](00-prep.md) · [Back to hub](README.md) · [Next: Goal 2 →](02-core.md)

---

## how to track your progress meow

this is the same system from the shared foundations — the `- [ ]` checkboxes below are display-only in this public repo. **fork** the repo to tick them in your own copy, OR **copy the checklist into your notes** (Obsidian/OneNote). your *actual* progress is the **two-part gate** at the end of each topic: (1) measurable (lab passed / % hit), (2) explain (u understand why). both must pass meow

---

## should u take the A+?

- **yes, if** u have no IT background. it can help with help-desk screens, which are the most common on-ramp into security.
- **skip the exam (study the content only), if** u already have IT/help-desk experience. dont pay ~$492 to prove what your resume already shows — put that money toward Network+ or Security+ instead.

> 💰 **dont waste the money:** dont book until youre scoring **85%+ on fresh practice tests** from 2+ sources. take **Core 1 (220-1201) first, then Core 2 (220-1202)** — one at a time, please. (~$246 each in 2026. see [certifications.md](../../references/certifications.md) for the full cost breakdown.)

---

## the path (todo-tree)

- [ ] **Block 1** — hardware + how computers work (~40h) · **A+ Core 1: domains 1+3+4**
- [ ] **Block 2** — operating systems (Windows + Linux) (~50h) · **A+ Core 2: domain 1**
- [ ] **Block 3** — networking basics + security intro (~40h) · **A+ Core 1: domain 2 + Core 2: domain 2**
- [ ] **Block 4** — practice-exam sprint (~10h)
- [ ] ✅ **exit check** — comfortable in both Windows and Linux shell, can subnet on paper, ready for Network+

---

## Block 1 · Hardware + How Computers Work (~40h)

### A+ Core 1 coverage: Domain 1 (Mobile Devices 13%), Domain 3 (Hardware 25%), Domain 4 (Virtualization & Cloud 11%)

**the idea** — a running computer is a loop (fetch-decode-execute), not a magic box. understanding what the CPU/RAM/storage/motherboard *do* is the floor — an attacker abuses the same hardware mechanisms u need to know for troubleshooting.

**how it actually works** — same mechanism as Shared Foundations, just with the A+ parts layered on top:

a CPU repeats the **fetch–decode–execute cycle** from boot until shutdown:
1. **fetch** — the **program counter (PC)** holds the memory address of the next instruction. that address is copied to the **memory address register (MAR)**, the value at that RAM address is pulled into the **memory data register (MDR)** and then the **current instruction register (CIR)**; the PC increments.
2. **decode** — the **control unit** interprets the bits in the CIR: which operation, which operands.
3. **execute** — the **ALU** (arithmetic logic unit) does the math/logic, or data is moved, or the PC jumps. then the loop repeats.

modern CPUs overlap these steps via an **instruction pipeline** (next fetch starts before the previous execute finishes).

why RAM vs storage matters, physically: **RAM is volatile** — fast electrical cells the CPU addresses directly, but they clear on power loss. **storage (SSD/HDD) is persistent** but far slower and *not* directly executable. so "running a program" = the OS copies it from storage into RAM, creates a **process** (its own address space + PC + registers), and the CPU runs the fetch-decode-execute loop on those in-RAM instructions. more RAM = more/bigger programs at once; an SSD speeds *launch/load*, not raw compute.

**A+ also checks this vocab:** CPU sockets/generations (Intel LGA vs AMD AM4/AM5), cores vs threads, cache (L1/L2/L3), **RAM** (DDR4/DDR5, dual-channel, ECC), **storage** (HDD vs SSD, SATA vs NVMe/M.2, RAID 0/1/5/10), **motherboard** (BIOS/UEFI, CMOS battery, PCIe slots, chipset), **PSU** (wattage, 80+ ratings, connectors), **ports** (USB 2/3/C, HDMI, DisplayPort, Thunderbolt), mobile devices (iOS/Android, screen/battery/charge ports), printers. dw this part is mostly naming things — the mechanism above is the core qwq

**words u gotta be able to say:**
- **CPU / core / thread / clock speed** — executes instructions / independent execution unit / logical core via SMT / GHz cycles/sec
- **fetch–decode–execute cycle** — the CPUs loop per instruction
- **program counter / register / ALU / control unit** — next-instruction address / tiny CPU storage / math unit / decode+direct unit
- **RAM (volatile) / storage (persistent)** — fast/clears on power loss / slow/survives power off
- **process** — a program loaded into RAM and running
- **BIOS/UEFI** — firmware that boots the OS
- **RAID 0/1/5/10** — striping/mirroring/parity/both
- **NVMe / M.2 / PCIe** — fast SSD protocol / physical form factor / expansion bus

**study sources (pick what fits your style):**
- [Professor Messer — A+ 220-1201 (Core 1) playlist](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-training-course/) — full free video course covering all Core 1 domains. **free** ✅
- [CS50x Week 0–1](https://cs50.harvard.edu/x/) — build logic in Scratch then write your first C program; see the fetch-execute cycle in action. **free** ✅
- [Branch Education — "How does a CPU work?"](https://www.youtube.com/watch?v=cNN_tTXABUA) + ["How do SSDs work?"](https://www.youtube.com/watch?v=5Mh3o886qpg) — 3D animations of the actual hardware. **free** ✅

**do this** — [HTB Academy — "Introduction to Cybersecurity" module (free tier)](https://academy.hackthebox.com/) + [Codecademy — "Intro to Cybersecurity"](https://www.codecademy.com/learn/introduction-to-cybersecurity) (OS layers, virtualization basics). both are free and browser-based. ✅

**measurable gate:** score **75%+ on 3 fresh attempts** at [ExamCompass A+ Core 1 — Hardware quizzes](https://www.examcompass.com/comptia/a-plus-certification/free-a-plus-core-1-practice-tests) (domains 1+3+4). thats the real check — either u hit the % or u didnt meow

**can u explain it?** ✅ — out loud or written, unaided: *"trace one instruction through fetch, decode, execute — name which register holds the next address. explain why a program must be copied from storage into RAM before the CPU can run it, and what makes RAM different from an SSD."*

**CTF thread (running from 00-prep):** if youve started **OverTheWire Bandit** (levels 0–5 from prep), keep going — reach **level 10** by the end of this block. each level reinforces the "files live in a filesystem the OS manages" mental model. no new CTF intro needed here; just keep the thread alive meow

---

## Block 2 · Operating Systems — Windows + Linux (~50h)

### A+ Core 2 coverage: Domain 1 (Operating Systems 28%)

**the idea** — the shell is a program that reads a line, parses it, and asks the OS kernel to do the work. the OS is the layer between hardware and your apps — if u dont know how it hands out memory, manages processes, and enforces permissions, u cant understand what an exploit abuses.

**how it actually works** — same shell/OS mechanism as Shared Foundations, now with Windows + Linux exam coverage layered on top:

when u type `ls -l /etc` and press Enter: the shell splits the line into **command + arguments**, resolves `ls` by searching each directory in your **`PATH`** environment variable, then calls the kernel to **`fork`** a new process and **`exec`** the `ls` binary into it. `ls` runs, writes to **stdout**, exits with a numeric **exit code** (0 = success).

the power comes from three OS mechanisms:
- **streams & pipes** — every process has stdin/stdout/stderr. a **pipe `|`** connects one processs stdout to the nexts stdin; **redirects** `>`/`>>` send stdout to a file.
- **the filesystem is a tree** — one root `/`, **absolute paths** start at `/`, **relative paths** start from `pwd`, `~` = home. everything (devices, config) is a file under it.
- **permissions** — each file has read/write/execute bits for owner/group/other, shown as `rwxr-xr-x`. `chmod 755` sets them via **octal** (r=4, w=2, x=1 → 7=rwx, 5=r-x). this is *the* access-control primitive an attacker abuses or a defender hardens.

`sudo` runs one command as **root** (uid 0, all-powerful); `ps`/`top` list processes; `kill` sends a signal by PID.

**A+ Core 2 Domain 1 also wants:**
- **Windows:** editions (Home/Pro/Enterprise), **NTFS permissions** (read/write/modify/full control) + inheritance, **Registry** (`HKLM`, `HKCU`), CLI (`ipconfig`, `ping`, `tracert`, `netstat`, `tasklist`, `sfc /scannow`), Task Manager, Event Viewer, Windows Defender/Firewall, **UAC** (User Account Control).
- **Linux:** filesystem hierarchy (`/etc`, `/var/log`, `/home`, `/bin`, `/usr`), core commands (`ls`, `grep`, `find`, `chmod`, `chown`, `ps`, `kill`, `top`, `apt`/`yum`), octal permissions (755/644/700), users & groups (`sudo`, `/etc/shadow`, `useradd`).
- **Hybrid identity (2026 reality):** on-prem **Active Directory** (Kerberos, LDAP, GPOs, domain/forest) syncs to **Microsoft Entra ID** (was Azure AD) in most real environments. learn classic AD, yes — just know it usually lives beside cloud identity now, not alone in a museum meow

**words u gotta be able to say:**
- **shell / kernel / PATH** — command-line program / OS core / dirs searched for a command
- **stdin / stdout / stderr / pipe `|` / redirect `>`** — input / normal output / error output / connect streams / send to file
- **absolute vs relative path / `~`** — from `/` vs from `pwd` / home shortcut
- **permissions / `chmod` / octal (755, 644)** — read/write/execute bits / change them / numeric notation
- **process / PID / `kill` / `ps` / `top`** — running program / its id / send signal / list / live monitor
- **root / `sudo`** — superuser (uid 0) / run one command with root privs
- **NTFS / inheritance / Registry / UAC** — Windows filesystem / perm propagation / system config DB / privilege escalation prompt
- **Active Directory / Kerberos / LDAP / GPO** — domain identity system / ticket-based auth / directory protocol / group policy
- **Entra ID (Azure AD)** — Microsofts cloud identity (AD syncs to it)

**study sources:**
- [Professor Messer — A+ 220-1202 (Core 2) playlist, Domain 1 (Operating Systems)](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/220-1202-training-course/) — Windows + Linux + macOS coverage. **free** ✅
- [The Missing Semester (MIT) — Lecture 1 (The Shell) + Lecture 2 (Shell Tools)](https://missing.csail.mit.edu/2020/course-shell/) — best CLI intro, text + video + exercises. **free** ✅
- [TCM Security — Practical Help Desk course (YouTube)](https://www.youtube.com/playlist?list=PLLKT__MCUeixqHJ1TRqrHsEd6_EdEvo47) — real help-desk Windows troubleshooting + Active Directory basics. **free** ✅
- [LabEx Linux Journey](https://labex.io/linuxjourney) — self-paced text lessons on CLI, filesystem, permissions. **freemium** ✅

**do this:**
- [TryHackMe — Windows Fundamentals 1–3](https://tryhackme.com/room/windowsfundamentals1xbx) (free rooms) — filesystem, Registry, UAC, Defender in a live browser VM. **free** ⚠️ (loads fine in browser)
- [HTB Academy — Windows Fundamentals module](https://academy.hackthebox.com/) (free tier) — CLI/PowerShell against live targets. **free** ✅
- [HTB Academy — Linux Fundamentals module](https://academy.hackthebox.com/) (free tier) — nav, permissions, package mgmt. **free** ✅
- **OverTheWire Bandit levels 0–15** (from prep) — SSH into Linux boxes, solve with `ls`, `cat`, `find`, `grep`, `ssh`, `base64`. **free** ✅

**measurable gate:** complete **OverTheWire Bandit levels 0–15 unaided** (the "Bandit" thread from prep) AND score **78%+ on 3 fresh attempts** at [ExamCompass A+ Core 2 — Operating Systems quizzes](https://www.examcompass.com/comptia/a-plus-certification/free-a-plus-core-2-practice-tests). both must pass — Bandit proves real CLI skill, ExamCompass proves A+ vocab coverage meow

**can u explain it?** ✅ — out loud, unaided: *"type `cat notes.txt | grep TODO | wc -l` — explain what each `|` does to the data, what stdout is, and what `chmod 640 notes.txt` would let the owner vs group vs others do."*

**CTF thread:** Bandit 0–15 completion *is* your CTF for this block (gate above). by level 15 youve used SSH keys, `nc`, pipes, `find` by perms — youre building the "navigate + search + permissions" instinct the field runs on meow

---

## Block 3 · Networking Basics + Security Intro (~40h)

### A+ Core 1 coverage: Domain 2 (Networking 23%) + Domain 5 (Troubleshooting 28% networking portion)
### A+ Core 2 coverage: Domain 2 (Security 28%)

**the idea** — typing a URL kicks off a fixed sequence (DNS → TCP → TLS → HTTP), and every piece of that chain is either a hardening point or an attack surface. A+ teaches the mechanisms; security (next goal) teaches what breaks them.

**how it actually works** — same internet chain as Shared Foundations, trimmed to what A+ cares about rn:

pressing Enter on `https://example.com` runs:
1. **DNS resolution** — the OS asks a **recursive resolver**, which walks **root → TLD (`.com`) → authoritative** nameserver, which returns the **A record** (IPv4). cached with a **TTL**.
2. **TCP three-way handshake** — **SYN → SYN-ACK → ACK** on **port 443**. establishes a reliable connection (sequence numbers, retransmit on loss).
3. **TLS handshake** — ClientHello, ServerHello + **certificate** (proves identity via **CA**), agree on a **session key**, encrypt all further traffic. stops a **man-in-the-middle** from reading (**confidentiality**) or altering (**integrity**).
4. **HTTP request/response** — `GET / HTTP/1.1` → `200 OK` + HTML.

underneath: everything is **packets** routed hop-by-hop by IP. **ports** let one machine run many services (80 HTTP, 443 HTTPS, 22 SSH, 53 DNS, 445 SMB, 3389 RDP). the **OSI/TCP-IP models** name who does what (app/transport/network/data-link/physical layers).

**A+ Core 1 Domain 2 also wants:** IPv4/IPv6 addressing, **subnetting** (CIDR `/24` `/30`, subnet masks), private vs public IPs (RFC 1918: 10.x, 172.16–31.x, 192.168.x), **DHCP/DNS/NTP**, **routing/switching/VLANs**, Wi-Fi (WPA2/WPA3, 2.4GHz/5GHz), cabling (Cat5e/6/6a, fiber), and the 7-step troubleshooting method (identify→theory→test→plan→implement→verify→document).

**A+ Core 2 Domain 2 (Security) intro:** malware types (virus/worm/trojan/ransomware/rootkit), **social engineering** (phishing/vishing/tailgating), **physical security** (badge/biometric/mantrap), **logical security** (ACLs, MFA, principle of least privilege), encryption basics (at-rest vs in-transit), **hardening** (disable unused services, patch, firewall rules).

**words u gotta be able to say:**
- **DNS / A record / CNAME / MX / TTL** — name→IP / IPv4 record / alias / mail server / cache lifetime
- **IP / IPv4 / IPv6 / subnet mask / CIDR / gateway** — network address / 32-bit / 128-bit / which bits = network / slash notation / router to other networks
- **port / well-known ports** — service id (22 SSH, 53 DNS, 80 HTTP, 443 HTTPS, 445 SMB, 3389 RDP, 25 SMTP)
- **TCP handshake (SYN/SYN-ACK/ACK) / packet** — reliable connection setup / unit data is routed in
- **TLS / certificate / CA / session key** — secure channel / identity proof / trusted issuer / symmetric key after handshake
- **confidentiality / integrity / man-in-the-middle** — cant-read / cant-alter / attacker between u and server
- **OSI model (7 layers) / TCP-IP model (4 layers)** — physical/data-link/network/transport/session/presentation/app vs link/internet/transport/app
- **DHCP / DNS / NTP** — auto IP assignment / name resolution / time sync
- **malware: virus / worm / trojan / ransomware / rootkit** — self-replicates (needs host) / self-propagates / masquerades as legit / encrypts+demands / hides in kernel
- **social engineering: phishing / vishing / tailgating** — fake email / voice scam / follow someone through a door
- **principle of least privilege / MFA / ACL** — minimal access needed / multi-factor auth / access control list

**study sources:**
- [Professor Messer — A+ 220-1201 Domain 2 (Networking)](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/220-1201-training-course/) + [A+ 220-1202 Domain 2 (Security)](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/220-1202-training-course/) — core coverage. **free** ✅
- [PowerCert Animated Videos — "OSI Model"](https://www.youtube.com/watch?v=vv4y_uOneC0) + ["TCP/IP"](https://www.youtube.com/watch?v=OTwp3xtd4dg) + ["DNS"](https://www.youtube.com/watch?v=mpQZVYPuDGU) — 5–10min visuals. **free** ✅
- [NetworkChuck — "you need to learn Subnetting RIGHT NOW!!"](https://www.youtube.com/watch?v=5WfiTHiU4x8) — energetic walkthrough. **free** ✅
- [howdns.works](https://howdns.works/) — comic walkthrough of DNS resolution. **free** ✅

**do this:**
- [HTB Academy — Introduction to Networking module](https://academy.hackthebox.com/) (free tier) — OSI, TCP/IP, subnetting, DNS, ARP interactive. **free** ✅
- [TryHackMe — Intro to Networking room](https://tryhackme.com/room/introtonetworking) (free) — OSI, ping, traceroute. **free** ⚠️
- **Subnetting drill:** [subnetipv4.com](https://subnetipv4.com/) — `/24` to `/30` until automatic. **free** ✅
- run `curl -v https://example.com` + `dig example.com` in your terminal (from fundamentals Block 3) and **annotate which lines = DNS / TCP / TLS / HTTP**.

**measurable gate:** score **80%+ on 3 fresh attempts** at ExamCompass A+ Core 1 Networking + Core 2 Security quizzes, AND correctly subnet 5 random `/25`–`/29` problems on paper unaided (use subnetipv4.com to generate/check them). both must pass meow

**can u explain it?** ✅ — out loud, unaided: *"narrate the steps from pressing Enter on `https://example.com` to the page appearing: DNS resolution → TCP SYN/SYN-ACK/ACK → TLS handshake (what the certificate proves, what the session key does) → HTTP GET/200. then say why TLS stops a man-in-the-middle."*

**CTF thread:** after Bandit 15, try **CyLab Security Academy (picoCTF) — General Skills beginner challenges** (e.g. "Obedient Cat", "strings it", "Nice netcat...") — these reinforce ports (`nc`), file forensics (`strings`), and basic tooling. **gate:** solve 5 General Skills challenges. this keeps the CTF thread alive between Bandit and the web-exploitation goal meow

---

## Block 4 · Practice-Exam Sprint (~10h)

**the idea** — u dont book the exam until practice tests already say youre ready. this block is the calm final check so exam day doesnt feel mysterious.

**do this:**
- Professor Messer A+ Success Bundles: [Core 1](https://www.professormesser.com/220-1201-success-bundle/) + [Core 2](https://www.professormesser.com/220-1202-success-bundle/) (paid optional; the old generic practice-exams page is dead) — **gate: 85%+ on 3 fresh Core 1 attempts, 85%+ on 3 fresh Core 2 attempts**. ✅
- [Jason Dion A+ Practice Tests (Udemy)](https://www.udemy.com/course/comptia-a-exams/) (~$10–15 on sale) — **gate: 80%+ on 2 fresh attempts per core**. ✅
- [ExamCompass A+ quizzes](https://www.examcompass.com/) (free) — domain-by-domain reinforcement. **free** ✅

**measurable gate:** hit the % gates above on FRESH attempts (not retakes of the same test). if youre not hitting 85%+ on Messer, dont book yet — go back to the weak domain and patch it up meow

**exam-day tips:**
- **flag PBQs** (performance-based questions — sims/drag-drop), answer all multiple-choice first, then return to PBQs with remaining time. PBQ terminals: type `help` to list valid commands.
- **Core 1 pass: 675/900**. **Core 2 pass: 700/900**. take Core 1 first (hardware/networking foundation makes Core 2 easier).
- both exams: ≤90 questions, 90 minutes, 3-year validity. book via [CompTIA store](https://www.comptia.org/) or Pearson VUE.

---

## ✅ exit check — youre done with Goal 1

by now u have:
- [ ] completed Bandit 0–15 + solved 5 CyLab General Skills challenges (CTF thread alive)
- [ ] scored 75%+ on ExamCompass Core 1 Hardware, 78%+ on Core 2 OS, 80%+ on Core 1 Networking + Core 2 Security (all on fresh attempts)
- [ ] can subnet `/25`–`/29` on paper unaided
- [ ] comfortable in both a Windows and Linux shell (can navigate, change perms, search files, manage processes)
- [ ] either **passed A+** OR scoring **85%+ on Messer/Dion practice exams** (if skipping the paid exam)

**both gates must pass:**
1. **measurable** — the checklist above is all ticked
2. **can u explain it?** — out loud, unaided: *"trace one instruction through fetch-decode-execute. explain what `cat notes.txt | grep TODO | wc -l` does at each pipe. narrate DNS → TCP → TLS → HTTP for `https://example.com` and say why TLS stops a MITM."*

if u can tick the boxes but stumble on the explain gate, re-read the mechanism sections in Blocks 1–3. both must pass before Goal 2 meow

---

**next up:** [Goal 2 — Networking & Security Core](02-core.md) — Network+, ISC2 CC + Security+ merged study (CIA triad, crypto/PKI, access control, threats, network security, SOC operations). the certs are checkpoints; the *topics* are what transfer to the job qwq

[← Prep](00-prep.md) · [Back to hub](README.md) · [Next: Goal 2 →](02-core.md)
