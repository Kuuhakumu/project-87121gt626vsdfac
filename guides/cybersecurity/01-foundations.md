# 📁 Phase 1: Foundations — Hardware & Operating Systems

> **~140 hrs total** · your pace, no deadline
> Maps to **CompTIA A+ (220-1201 / 220-1202)**. This is the IT bedrock security sits on. If you already work in IT support, you can test out fast and move to [Phase 2](02-core.md).

[← Phase 0](00-prep.md) · [Back to hub](README.md) · [Next: Phase 2 →](02-core.md)

---

## Should you take the A+?

- **Yes, if** you have no IT background. It's the baseline filter for help-desk roles, which are the most common on-ramp into security.
- **Skip the exam (study the content only), if** you already have IT/help-desk experience. Don't pay ~$492 to prove what your resume already shows — jump to Network+ and Security+.

> 💰 **Don't waste the money:** don't book until you're scoring **85%+ on fresh practice tests** from 2+ sources. Take **Core 1 first, then Core 2** — never both at once. (A+ = 220-1201 + 220-1202, ~$246 each in 2026. See [certifications.md](certifications.md).)

---

## Hardware & how computers work (Core 1) (~40 hrs)

**Cover:** CPU (Intel/AMD, x86/x64, cores, cache), RAM (DDR4/DDR5, ECC, dual-channel), storage (HDD vs SSD, SATA/NVMe/M.2, RAID 0/1/5/10), motherboard (BIOS/UEFI, CMOS, PCIe), PSU & connectors, ports (USB types, HDMI, DisplayPort, Thunderbolt), mobile devices, printers.

**Theory:** [Professor Messer A+ 220-1201](https://www.professormesser.com/) (free, full playlist) + [Branch Education](https://www.youtube.com/@BranchEducation) for 3D hardware deep-dives.

**Labs:**

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Virtualization & cloud basics | [HTB Academy](https://academy.hackthebox.com/) (free modules) | Allocate virtual hardware, understand hypervisor types | Free |
| Intro to Cybersecurity | [Codecademy](https://www.codecademy.com/learn/introduction-to-cybersecurity) | OS layers, CIA triad, virtualization concepts | Freemium |

**Practice gate:** 75%+ on [ExamCompass](https://www.examcompass.com/) hardware quizzes.

---

## Operating systems — Windows & Linux (Core 2) (~50 hrs)

**Windows:** editions, NTFS permissions & inheritance, Registry (`HKLM`, `HKCU`), CLI (`ipconfig`, `ping`, `tracert`, `netstat`, `tasklist`, `sfc /scannow`), Task Manager, Event Viewer, Windows Firewall, UAC.

**Linux:** filesystem hierarchy (`/etc`, `/var/log`, `/home`), core commands (`ls`, `grep`, `find`, `chmod`, `chown`, `ps`, `kill`, `top`, `apt`), octal permissions (755/644/700), users & groups (`sudo`, `/etc/shadow`).

> **2026 reality:** identity is now **hybrid** — learn on-prem Active Directory fundamentals (Kerberos, LDAP, GPOs) but know they sync to **Microsoft Entra ID** (Azure AD) in most real environments. Pure on-prem-only AD is a dated mental model.

**Theory:** Professor Messer A+ 220-1202 + [TCM Security free Help Desk course](https://academy.tcm-sec.com/p/practical-help-desk-training).

**Labs:**

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Windows Fundamentals 1–3](https://tryhackme.com/room/windowsfundamentals1xbx) | TryHackMe | Filesystem, registry, UAC, Defender in a live browser VM | Free |
| Windows Fundamentals module | [HTB Academy](https://academy.hackthebox.com/) | Guided CLI/PowerShell against live targets | Free |
| [OverTheWire — Bandit](https://overthewire.org/wargames/bandit/) (0–15) | OverTheWire | SSH into real Linux boxes; `cat`, `grep`, `find`, `ssh`, `base64` | **Free** |
| Linux Fundamentals 1–3 | [TryHackMe](https://tryhackme.com/room/linuxfundamentalspart1) | Navigate filesystem, permissions, cron, SSH | Free |

**Practice gate:** 78%+ on ExamCompass OS quizzes.

---

## Networking basics + security & procedures (Core 1 & 2) (~40 hrs)

**Cover:** OSI model, TCP/IP, IP addressing & subnetting (CIDR), key ports (SSH 22, DNS 53, HTTP 80, HTTPS 443, SMB 445, RDP 3389), DNS resolution, wireless (WPA2/WPA3), plus Core 2 security basics (malware types, social engineering, basic hardening) and operational procedures.

**Theory:** [PowerCert](https://www.youtube.com/@PowerCertAnimatedVideos), [NetworkChuck](https://www.youtube.com/@NetworkChuck), Professor Messer A+ networking sections.

**Labs:**

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Intro to Networking](https://tryhackme.com/room/introtonetworking) | TryHackMe | OSI, ping, traceroute interactively | Free |
| Intro to Networking module | [HTB Academy](https://academy.hackthebox.com/) | OSI/TCP-IP, subnetting, DNS, ARP | Free |
| [SubnettingPractice.com](https://www.subnettingpractice.com/) | Web | `/24`–`/30` drills until automatic | **Free** |

**Practice gate:** 80%+ on ExamCompass networking quizzes.

---

## Practice-exam sprint & booking (~10 hrs)

| Resource | Cost | Gate |
|---|---|---|
| [Professor Messer practice exams](https://www.professormesser.com/practice-exams/) | ~$15 | **85%+ on 3 fresh attempts** |
| Jason Dion A+ tests (Udemy) | ~$10–15 on sale | 80%+ on 2 fresh attempts |
| [ExamCompass](https://www.examcompass.com/) | Free | Domain quizzes |

**Exam-day:** flag PBQs, answer all multiple-choice first, then return to PBQs. In PBQ terminals, type `help` to list valid commands.

---

✅ **Exit check:** comfortable in both a Windows and Linux shell, can subnet on paper, and either passed A+ or can score 85%+ on its practice exams.

[← Phase 0](00-prep.md) · [Back to hub](README.md) · [Next: Phase 2 — Networking & Security Core →](02-core.md)
