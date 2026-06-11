# ⚙️ Phase 0: Pre-Flight Setup

> **~20 hrs total** · your pace, no deadline
> Goal: working lab, right mindset, plugged into a community — before you touch a single security topic.

[← Back to hub](README.md) · [Next: Phase 1 →](01-foundations.md)

---

## Mindset & expectations

- **Cybersecurity is a specialization, not an entry point.** It sits on top of networking, operating systems, and a little scripting. Skipping those is the #1 reason people stall.
- **The market is real but competitive at the bottom.** The reliable path is usually *help desk / NOC → SOC*, not *cert dump → SOC*. Build something demonstrable. See [job market notes](05-job-hunt.md).
- **Consistency beats intensity.** Two focused hours a day beats a 14-hour weekend once a month.
- **Curiosity beats memorization.** Learn *why* a tool works and *what footprint it leaves*, not just which button to click.

## Pace & timeline

This guide is measured in **study hours**, not weeks — so it works at any pace. Total to job-ready: **~500–700 hours**.

| Pace | Hours/week | ~Time to job-ready |
|---|---|---|
| Casual | 5–8 | 18–24 months |
| Part-time (recommended) | 10–15 | 12–18 months |
| Full-time | 20–30 | 8–12 months |

---

## Build your lab (~8 hrs)

You don't need to buy hardware — a free hypervisor on your existing machine is enough to start.

1. **Install a hypervisor:** [VirtualBox](https://www.virtualbox.org/) (free) or VMware Workstation (free for personal use).
2. **Import two VMs:**
   - [Kali Linux](https://www.kali.org/get-kali/) (attacker / tooling)
   - [Windows 10/11 Evaluation](https://www.microsoft.com/en-us/evalcenter/) ISO (target)
3. **Isolate the network:** put both VMs on the same **Host-Only** or **internal NAT** network so nothing leaks to your home LAN.

```
┌─ Host Machine ─────────────────────────────┐
│  ┌─ Hypervisor (VirtualBox) ─────────────┐ │
│  │  [ Kali Linux ] ◄──► [ Windows VM ]   │ │
│  │        Isolated Host-Only network     │ │
│  └───────────────────────────────────────┘ │
└─────────────────────────────────────────────┘
```

> **Cloud alternative:** if your machine can't spare the RAM, most early labs in this guide run **in-browser** (TryHackMe, HTB Academy, PortSwigger) and need no local VM at all.

## Free on-ramp courses (~6 hrs)

Pick one to get your bearings before the cert grind:
- [Google Cybersecurity Professional Certificate](https://www.coursera.org/professional-certificates/google-cybersecurity) — structured, beginner-first, financial aid available.
- [HTB Academy — Pre-Security path](https://academy.hackthebox.com/) — free modules covering the web, networking, and Linux basics.
- [TryHackMe — Pre-Security path](https://tryhackme.com/) — gentle in-browser intro.

## Plug into the community + tooling (~6 hrs)

- **Communities:** r/cybersecurity and r/ITCareerQuestions (read the wikis/megathreads first), the TryHackMe and HTB Discords, and any local OWASP / BSides chapter.
- **Note-taking system:** set up [Obsidian](https://obsidian.md/) or OneNote now. You'll build a personal knowledge base for the next year — many practical exams are open-book, and good notes are the difference between pass and fail.
- **Get oriented on the 2026 landscape:** skim the [tooling & trends summary](../../research/lab-inventory/tooling-trends-2026.md) so you study current tools (Sentinel, Splunk, Wazuh, MITRE ATT&CK v19) and not retired ones.

---

✅ **Exit check:** lab boots, both VMs talk only to each other, note system is running, you've joined at least one community, and one on-ramp course is underway.

[← Back to hub](README.md) · [Next: Phase 1 — Foundations →](01-foundations.md)
