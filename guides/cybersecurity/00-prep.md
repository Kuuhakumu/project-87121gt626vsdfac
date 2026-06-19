# ⚙️ Prep — Before You Start (~20h)

> **goal:** working lab, right mindset, plugged into a community — before u touch a single security topic meow

**Total: ~20 hours** (≈ 2 weeks at 2h/day). go at whatever pace fits your life — theres no deadline.

[← Back to hub](README.md) · [Next: Foundations →](01-foundations.md)

---

## the path (todo-tree)

- [ ] **mindset + honest expectations** — cybersecurity is a specialization, not an entry point (~1h read)
- [ ] **build your lab** — hypervisor + 2 VMs, isolated network (~8h)
- [ ] **free on-ramp** — pick one beginner course to get your bearings (~6h)
- [ ] **plug into the community + tooling** — notes system, communities, current landscape (~5h)
- [ ] ✅ **exit check** — lab boots, notes ready, CTF account created

---

## okok so what even is cybersecurity meow (~1h)

**the idea** — security isnt a starting point, its a specialization that sits ON TOP of networking + operating systems + a lil scripting.

**real talk first:** thats the #1 reason ppl stall — they skip the floor and try to build the roof qwq

heres the *why* tho: an attack is just someone abusing a system thats working exactly as designed. so if u dont know how the system works normally (how a TCP handshake goes, how the OS hands out memory, what a cookie is), u literally cant tell whats abuse and whats normal. thats why **fundamentals first** — if u already cleared the [Shared Foundations](../../start-here/foundations.md) (command line, networking, Git), youre golden. if not, go do that now and come back. this guide assumes u can already navigate a terminal, explain how DNS→TCP→TLS→HTTP works, and push to GitHub meow

**the market is real but competitive at the bottom.** the reliable path is usually *help desk / NOC → SOC analyst*, not *cert dump → SOC*. build something demonstrable (a GitHub with CTF writeups, a home lab, real troubleshooting stories). see [job market notes](05-job-hunt.md) for the honest version.

**consistency beats intensity.** two focused hours a day beats a 14-hour weekend once a month. dw if 2h/day sounds like a lot — the guide is measured in study hours, not weeks, so it works at any pace. total to job-ready: **~500–700 hours**.

| Pace | Hours/week | ~Time to job-ready |
|---|---|---|
| Casual | 5–8 | 18–24 months |
| Part-time (recommended) | 10–15 | 12–18 months |
| Full-time | 20–30 | 8–12 months |

**curiosity beats memorization.** learn *why* a tool works and *what footprint it leaves*, not just which button to click. thats the instinct that actually transfers to new situations meow

---

## why we start CTF on day one meow (~read this, its important)

heres the thing — watching a video feels like learning but its passive. your brain goes "yeah yeah i get it" and then cant do it when it counts qwq

a **CTF (capture-the-flag)** challenge makes u actually DO the thing. u either get the flag or u dont, no lying to urself :3

and its legal + sandboxed so u literally cant break anything real. its just... a puzzle that happens to teach u how systems get abused. thats the instinct the whole field runs on — "ok but how could this break?" — and u only get it by breaking stuff on purpose in a safe place mhm

**so we dont save CTF for the end.** we start OverTheWire Bandit level 0 basically day one (its literally aimed at absolute beginners — the site says so), right next to the linux stuff, and keep a lil CTF thread going the whole way. each study topic gets a matching challenge from the running CTF ladder below, so the puzzle reinforces what u just learned.

why this works (real pedagogy, not hype):
- **active recall > passive video** — being forced to produce the answer builds way more durable memory than rewatching (this is "the testing effect," one of the most replicated findings in learning science). a CTF is retrieval practice with a scoreboard.
- **a solved flag is proof of understanding** — it maps exactly onto this guides `can u explain it?` gate. u literally cannot capture the flag without the mechanism working in your head. so CTF = built-in checkpoint, not extra work.
- **low-stakes + fun = momentum** — the dopamine of a captured flag is what carries a self-learner through the boring floor (subnetting, permissions). momentum is the #1 predictor of a self-study plan surviving qwq
- **its the fields native training format** — picoCTF (now **CyLab Security Academy**, CMU-run) exists specifically to teach beginners this way: 1M+ learners, 14,000+ classrooms, "no experience needed." the on-ramps are designed for day one; theres no reason to wait.

dw if "break stuff" sounds scary rn — the first challenge is literally just `ls` and `cat` on a server u SSH into. youve got this meow

---

## build your lab (~8h)

u dont need to buy hardware — a free hypervisor on your existing machine is enough to start.

**do this:**
1. **install a hypervisor:** [VirtualBox](https://www.virtualbox.org/) (**free**) or VMware Workstation Player (**free** for personal use)
2. **import two VMs:**
   - [Kali Linux](https://www.kali.org/get-kali/) — the attacker / tooling VM (download the VirtualBox `.ova` or `.vbox` image)
   - [Windows 10/11 Evaluation ISO](https://www.microsoft.com/en-us/evalcenter/) — the target VM (90-day eval, **free**)
3. **isolate the network:** put both VMs on the same **Host-Only** or **Internal** network so nothing leaks to your home LAN or the internet. [VirtualBox network guide](https://www.virtualbox.org/manual/ch06.html) shows how.

```
┌─ Host Machine ─────────────────────────────┐
│  ┌─ Hypervisor (VirtualBox) ─────────────┐ │
│  │  [ Kali Linux ] ◄──► [ Windows VM ]   │ │
│  │        Isolated Host-Only network     │ │
│  └───────────────────────────────────────┘ │
└─────────────────────────────────────────────┘
```

**measurable gate:** both VMs boot, they can ping each other (test with `ping <ip>`), and they CANNOT reach the internet (test with `ping 8.8.8.8` — it should fail). this proves isolation. write down the steps u took in your notes (youll rebuild this setup later for different scenarios) meow

> **cloud alternative:** if your machine cant spare the RAM (~8GB for both VMs), most early labs in this guide run **in-browser** (TryHackMe AttackBox, HTB Academy Pwnbox, PortSwigger labs) and need no local VM at all. the local lab is recommended but not required until later phases.

---

## free on-ramp course (~6h)

pick ONE to get your bearings before the deep topics. these are gentle, structured, beginner-first intros:

- [HTB Academy — "Introduction to Cybersecurity" module](https://academy.hackthebox.com/) — **free tier**, covers the big-picture roles + basic concepts. ✅ verified live July 2026
- [TryHackMe — "Pre-Security" path](https://tryhackme.com/path/outline/presecurity) — **free**, in-browser, maximum hand-holding. teaches networking + Linux + web basics with guided rooms. ⚠️ (site rate-limits bots but loads fine in browser)
- [Google Cybersecurity Professional Certificate (Coursera)](https://www.coursera.org/professional-certificates/google-cybersecurity) — **~$49/mo** (financial aid available), structured 6-course sequence. covers SOC analyst foundations. ✅ verified live

**do this:** complete at least ONE of the above. doesnt matter which — theyre all good on-ramps. the goal is "i know what a SOC analyst / pentester / IR analyst does, and i can name the 5 main security domains (IAM, network sec, app sec, incident response, governance)."

**measurable gate:** finish the chosen course and be able to name, out loud, **3 cybersecurity job roles** (e.g. SOC analyst, pentester, security engineer) and what each one does day-to-day. no memorizing — just "i read about it and it stuck" meow

---

## plug into the community + tooling (~5h)

**notes system (do this first):**
set up [Obsidian](https://obsidian.md/) (**free**) or OneNote now. youll build a personal knowledge base for the next year — many practical exams (Security+, PenTest+, later OSCP) are open-book, and good notes are the difference between pass and fail. structure: one folder per topic (networking, web-exploitation, incident-response), one note per technique/tool. link liberally.

**join communities:**
- [r/cybersecurity](https://www.reddit.com/r/cybersecurity/) + [r/ITCareerQuestions](https://www.reddit.com/r/ITCareerQuestions/) — read the wikis/megathreads FIRST before posting (the "breaking in" questions are answered there)
- **TryHackMe Discord** + **Hack The Box Discord** — active, helpful, real-time help when ur stuck on a lab
- local **OWASP chapter** or **BSides conference** (search "<your city> OWASP" / "<your city> BSides") — free meetups, real humans, sometimes hiring leads

**get oriented on 2026 tooling:**
skim [../../research/lab-inventory/tooling-trends-2026.md](../../research/lab-inventory/tooling-trends-2026.md) (5min read) so u study current tools (Microsoft Sentinel, Splunk, Wazuh, MITRE ATT&CK v19, Ghidra, Burp Suite) and not retired ones (ArcSight, old Snort configs). the landscape shifts every ~2 years; this keeps u aligned with what employers actually use in 2026.

**create your CTF accounts (do this now):**
- [CyLab Security Academy](https://cylabacademy.org/) (was picoCTF — same free challenges, CMU-run, **always free**, 500+ challenges) — create account ✅
- [OverTheWire](https://overthewire.org/wargames/bandit/) — no account needed, just SSH in ✅
- [TryHackMe](https://tryhackme.com/) — free account ⚠️
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — free account, needed for the labs ✅

ull start hitting these in the next phase (Foundations), so getting accounts now means no friction later meow

**measurable gate:** notes system is running (create a test note, link it to another note, search works), youve joined ≥1 community (lurking counts), and u have accounts on OverTheWire + CyLab + PortSwigger. these are the objective bars — either u did them or u didnt.

---

## your running CTF ladder (the whole journey)

this is your **"whats my next challenge?"** spine — each rung maps to a study phase, so u always have a CTF at your level. dont rush the rungs; stay on easy till easy is boring, THEN climb mhm

### Rung 0 — absolute beginner (week 1, alongside "what even is a terminal")
- **OverTheWire Bandit 0 → 5** — SSH in, `ls`, `cat`, `file`, hidden files, `find` by size/type. this is the single best day-one on-ramp. ✅
- **CyLab (picoCTF) "General Skills" beginner** — e.g. *"Obedient Cat," "Wave a flag," "strings it"*-style challenges (pure "learn to use the tools"). ✅

### Rung 1 — beginner (weeks 2–5, as Linux + networking + HTTP land)
- **Bandit 6 → 20** — permissions, `grep`, `sort|uniq`, `nc`, SSH keys, basic scripting ✅
- **CyLab General Skills (rest) + first Forensics** — `strings`, `binwalk`, metadata ✅
- **CyLab Cryptography beginner** — base64/ROT13/XOR "decode me" challenges ✅
- **OverTheWire Natas 0 → 6** — browser-only server-side web (view source, HTTP auth, cookies) ✅

### Rung 2 — beginner→intermediate (weeks 6–12, web + crypto + first exploitation)
- **PortSwigger Web Security Academy — Apprentice labs** — SQLi (retrieve hidden data, login bypass) + XSS (reflected/stored) ✅
- **Natas 7 → 15** — LFI, command injection, SQLi in a wargame ✅
- **CryptoHack — "Introduction to CryptoHack" + "Modular Arithmetic" courses** ✅
- **CyLab Web Exploitation + Reverse Engineering beginner** ✅
- **TryHackMe OWASP Top 10 room** — one exploit per Top-10 category ⚠️

### Rung 3 — intermediate (stretch goals, the "keep going" pointer)
- **pwn.college "Start Here"** → binary exploitation dojos ✅
- **OverTheWire Krypton (crypto), Leviathan → Narnia (RE → binary)** ✅
- **Hack The Box — Starting Point + machines** ⚠️

**the anti-stall rules (important — this is where beginners quit):**
1. **the 20–30 min rule** — if one challenge eats >25 min with zero progress, its above your rung. read a writeup, learn the trick, move on. reading a writeup after a real attempt is still learning (its "worked-example" study). no shame, no grinding qwq
2. **always keep an easy one in reserve** — end each session on a solvable challenge so u leave on a win. protects momentum.
3. **never gate a study goal on a hard flag** — a goal is "done" on its two-part gate (measurable + explain); the CTF is reinforcement, not a blocker.
4. **writeup habit from day one** — create a `ctf-writeups` repo on GitHub. after each flag: problem → analysis → exploit → lesson-learned, in markdown. the act of writing it up is a second pass of retrieval (reinforces learning) AND becomes portfolio meow

> **heads up:** picoCTF rebranded to **CyLab Security Academy** in May 2026 — same challenges, same picoGym, still CMU-run and always free. old picoCTF accounts still work. ✅

---

## ✅ exit check — youre ready to start

by now u have:
- [ ] a working isolated lab (2 VMs ping each other, cant reach internet), OR youve confirmed the in-browser labs work for u
- [ ] finished one on-ramp course (HTB Intro / TryHackMe Pre-Security / Google Coursera) and can name 3 security job roles
- [ ] a notes system running (Obsidian/OneNote with ≥1 test note)
- [ ] joined ≥1 community (reddit/Discord)
- [ ] CTF accounts created (OverTheWire, CyLab, PortSwigger)
- [ ] read the "why CTF day one" section and the anti-stall rules

**both must pass:**
1. **measurable gate** — the checklist above is all ticked (objective, external, unfoolable)
2. **can u explain it?** — out loud or written, unaided: *"why is cybersecurity called a 'specialization' and not an entry point? what does 'an attack is abusing a system working as designed' mean? why do we start CTF early instead of saving it for the end?"*

if u can tick the boxes but stumble on the explain gate, re-read the "what even is cybersecurity" + "why CTF day one" sections above. both must pass before moving on meow

---

**Next up:** [01-foundations.md](01-foundations.md) — the 4 shared building blocks (computers, CLI, networking, Git+learning) that every security topic assumes u already know. if u did the Shared Foundations guide already, ull breeze through this as review qwq

[← Back to hub](README.md) · [Next: Foundations →](01-foundations.md)
