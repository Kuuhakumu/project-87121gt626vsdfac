# Resources

this page is a menu, not a second roadmap meow.

use the guide files first. come here when a topic says "pick a source" or when u need a backup explanation. every item below says what to do with it and why it matters, bc "subscribe to this channel" is not a learning plan.

paid books and paid bundles are optional extras. the required path stays free/freemium sources + real labs.

[<- Hub](README.md)

---

## video and course teachers

### Professor Messer - CompTIA spine

**use it for:** A+ 220-1201/220-1202, Network+ N10-009, and Security+ SY0-701.

**do this:** use the exact course index that matches the cert/topic you are studying:

- [A+ Core 1 220-1201 training course](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/220-1201-training-course/) - hardware, mobile, networking, virtualization, troubleshooting. **free**
- [A+ Core 2 220-1202 training course](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/220-1202-training-course/) - OS, security, software, operations. **free**
- [Network+ N10-009 training course](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/) - Sections 1-5 map cleanly to Network+ domains. **free**
- [Security+ SY0-701 training course](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/) - use by weak domain, not as a binge. **free**

**why it matters:** Messer is the cleanest free cert-aligned explanation layer. it gives u exam vocabulary after the guide teaches the mechanism, so u can recognize the same idea in CompTIA wording.

**paid optional:** if u buy Messer practice, use the current per-course Success Bundles: [A+ Core 1](https://www.professormesser.com/220-1201-success-bundle/), [A+ Core 2](https://www.professormesser.com/220-1202-success-bundle/), [Network+](https://www.professormesser.com/n10-009-success-bundle/), [Security+](https://www.professormesser.com/sy0-701-success-bundle/). dont use the old `/practice-exams/` page; R5 found it dead/soft-404.

### Practical Networking + NetworkChuck - subnetting support

**use it for:** IPv4 subnetting when `/26`, `/27`, `/28` still feel like magic.

**do this:** watch [Practical Networking's Subnetting Mastery playlist](https://www.youtube.com/playlist?list=PLIFyRwBY_4bQUE4IB5c4VPRyDoLgOdExE), then drill on [subnetipv4.com](https://subnetipv4.com/) until u can solve common masks on paper in under 60 seconds. if u need a loud first pass, watch [NetworkChuck's "you need to learn Subnetting RIGHT NOW!!"](https://www.youtube.com/watch?v=5WfiTHiU4x8), then come back to the drills.

**why it matters:** subnetting is not a trivia trick. it is how u know which hosts can talk directly, where routing begins, and why segmentation works.

### PowerCert Animated Videos - visual networking and hardware

**use it for:** the first visual pass on concepts that are hard to picture.

**do this:** watch the exact short videos that match your stuck point: [OSI Model](https://www.youtube.com/watch?v=vv4y_uOneC0), [TCP/IP](https://www.youtube.com/watch?v=OTwp3xtd4dg), [DNS](https://www.youtube.com/watch?v=mpQZVYPuDGU), [Network Ports](https://www.youtube.com/watch?v=g2fT-g9PX9o), and [RAM Explained](https://www.youtube.com/watch?v=PVad0c2cljo).

**why it matters:** these are diagram-first. they help u name the layers and parts before the deeper labs make u troubleshoot them.

### Branch Education - physical computer mechanisms

**use it for:** CPU, storage, and hardware foundations when A+ vocab feels disconnected from reality.

**do this:** watch ["How does a CPU work?"](https://www.youtube.com/watch?v=cNN_tTXABUA) and ["How do SSDs work?"](https://www.youtube.com/watch?v=5Mh3o886qpg), then explain fetch/decode/execute or NAND cells in plain words.

**why it matters:** security sits on machines that physically fetch instructions, store bits, and move data. the animations make that floor less abstract qwq.

### Prabh Nair - GRC day-job bridge

**use it for:** governance, risk, compliance, audits, and policy work.

**do this:** start with [GRC Practical Approach Part 1: Introduction](https://www.youtube.com/watch?v=mq_vSLHm4r0), then [Part 2: Governance](https://www.youtube.com/watch?v=Zfq3eJNvZdY). use the [GRC playlist](https://www.youtube.com/playlist?list=PL0hT6hgexlYz1Usn1Nrnur6OzVoz59zyl) as the ordered spine, and [GRC Analyst Masterclass](https://www.youtube.com/watch?v=JswwHeEqBIc) before vendor-risk or audit-evidence projects.

**why it matters:** Security+ teaches the words; Prabh shows the analyst workflow: risk register, policies, evidence, audit language, and stakeholder translation.

### John Hammond - malware and CTF workflow

**use it for:** seeing how an experienced analyst thinks through malware and CTF problems.

**do this:** after u have Linux + basic scripting, work through one video from John Hammond's [Malware playlist](https://www.youtube.com/playlist?list=PL1H1sBF1VAKWMn_3QPddayIypbbITTGZv). write a tiny behavior summary: initial clue -> tool used -> finding -> defensive lesson.

**why it matters:** the value is not "copy the tool." its watching the investigation loop: form a guess, test it, revise, document. thats the SOC/DFIR muscle.

### The Cyber Mentor / TCM - ethical hacking and reports

**use it for:** red-team survey, methodology, and report writing.

**do this:** use Heath Adams' [Ethical Hacking in 12 Hours](https://www.youtube.com/watch?v=fNzpcB7ODxQ) as a broad first survey after Network+ basics, not before. before publishing a pentest writeup, watch [Writing a Pentest Report](https://www.youtube.com/watch?v=EOoBAq6z4Zk) and compare your report structure against the [TCM Security sample report repo](https://github.com/hmaverickadams/TCM-Security-Sample-Pentest-Report).

**why it matters:** real pentesting is methodology + evidence + remediation. the report is the product, not a cute afterthought.

**paid optional:** TCM Academy moved off old Teachable URLs. use current pages like [Practical Ethical Hacking](https://tcm-sec.com/academy/practical-ethical-hacking/) or [PNPT](https://certifications.tcm-sec.com/pnpt/) only if u are buying training/exam prep. the free guide path does not require it.

### 13Cubed - Windows forensics and memory forensics

**use it for:** DFIR after u know basic Windows, logs, and incident response.

**do this:** start with [Introduction to Windows Forensics](https://www.youtube.com/playlist?list=PLlv3b9B16ZadqDQH0lTRO4kqn2P1g9Mve), then [Introduction to Memory Forensics](https://www.youtube.com/playlist?list=PLlv3b9B16Zaf-uDlgouB0DMiPNYU_sJFN). take notes as artifact -> what it proves -> what it does *not* prove.

**why it matters:** DFIR is evidence work. u need to know where artifacts live and how not to overclaim from them.

### scripting video backups

**Ryan John - [Python for Hackers FULL Course](https://www.youtube.com/watch?v=XWuP5Yf5ILI)**
use it when `03-scripting-ctf.md` asks u to connect Python to sockets, `requests`, parsing, and tiny security tools. why it matters: scripting turns repeated investigation steps into repeatable tools.

**freeCodeCamp - [Full Ethical Hacking Course: Network Penetration Testing for Beginners](https://www.youtube.com/watch?v=3Kq1MIfTWCE)**
use it as an explore-more survey after u already have networking basics. why it matters: it ties scanning, exploitation, and post-exploitation together, but it is not the source of current cert facts.

---

## books - optional depth, never required

no paid book is a gate in this guide. if a book costs money, treat it as a deeper optional layer after the free path already makes sense.

### [The Cuckoo's Egg](https://www.simonandschuster.com/books/The-Cuckoos-Egg/Cliff-Stoll/9781668048160) - Cliff Stoll

**topic it deepens:** incident response mindset, logging, persistence, attribution caution.

**why it matters:** it shows security as patient evidence gathering. the lesson is "follow the weird signal until u can prove what happened," not movie-hacker drama.

**how to use it:** read it when SOC/IR feels too tool-heavy. after a chapter, write what clue changed the investigation.

### [Ghost in the Wires](https://www.hachettebookgroup.com/titles/kevin-mitnick/ghost-in-the-wires/9780316037723/) - Kevin Mitnick

**topic it deepens:** social engineering, trust boundaries, physical/process security.

**why it matters:** many breaches start with people and process, not a fancy exploit. this helps u see how identity, help desks, phone systems, and assumptions become attack surface.

**how to use it:** read it as a social-engineering case study, then list the control that would have interrupted each trick: MFA, callback procedure, least privilege, logging, separation of duties.

### [Learn PowerShell in a Month of Lunches, Fourth Edition](https://www.manning.com/books/learn-powershell-in-a-month-of-lunches) - Travis Plunk, James Petty, Tyler Leonhardt, Don Jones, Jeffery Hicks

**topic it deepens:** Windows automation, PowerShell objects, pipelines, remoting.

**why it matters:** defenders live in Windows. PowerShell is both an admin tool and an attacker tradecraft surface, so u need to understand typed objects and command history instead of just memorizing commands.

**how to use it:** optional paid practice after the free Microsoft Learn PowerShell path. do the pipeline/object chapters slowly; those unlock KQL/SPL-style thinking later too.

### [The Web Application Hacker's Handbook](https://portswigger.net/web-security/web-application-hackers-handbook) - Dafydd Stuttard and Marcus Pinto

**topic it deepens:** HTTP, sessions, input handling, SQLi, XSS, access-control flaws.

**why it matters:** this book shaped modern web-app testing, but PortSwigger replaced the need for a third edition with the free Web Security Academy.

**how to use it:** optional historical/deep reference only. dont buy it as the path. do [PortSwigger Web Security Academy](https://portswigger.net/web-security/all-labs) first because the labs are current and interactive.

### [Sandworm](https://www.penguinrandomhouse.com/books/597684/sandworm-by-andy-greenberg/) - Andy Greenberg

**topic it deepens:** nation-state operations, destructive malware, OT/critical infrastructure risk, NotPetya-style business impact.

**why it matters:** it connects "a vuln got exploited" to real operational consequences: shipping, hospitals, power, incident coordination, attribution pressure.

**how to use it:** read after the core security section. make a timeline of one incident: initial access -> propagation -> impact -> recovery lesson.

### [Blue Team Handbook: Incident Response](https://www.oreilly.com/library/view/blue-team-handbook/9798341649767/) - Don Murdoch

**topic it deepens:** SOC workflows, triage, IR checklists, analyst field reference.

**why it matters:** once u have done DanaBot/Lockdown/LetsDefend, a field guide helps organize the steps u keep repeating.

**how to use it:** optional desk reference after hands-on labs. dont start here cold; it works best when u already have alerts and artifacts to attach the checklist to.

---

## practice platforms - what u actually do there

### web exploitation

**[PortSwigger Web Security Academy](https://portswigger.net/web-security/all-labs) - free**
do the Apprentice labs in [SQL injection](https://portswigger.net/web-security/sql-injection), [XSS](https://portswigger.net/web-security/cross-site-scripting), and [Access control](https://portswigger.net/web-security/access-control). why it matters: u exploit real live web flaws with Burp Community, then explain why the flaw worked.

**[OverTheWire Natas](https://overthewire.org/wargames/natas/) - free**
do Natas 0-10 after HTTP basics. why it matters: it teaches view-source, cookies, auth mistakes, and server-side assumptions with almost no tooling overhead.

### Linux, Windows, and beginner CTF

**[OverTheWire Bandit](https://overthewire.org/wargames/bandit/) - free**
do Bandit 0-15 during foundations. why it matters: SSH, files, permissions, pipes, `grep`, `find`, and keys become muscle memory instead of flashcards.

**[CyLab Security Academy](https://cylabacademy.org/) - free**
this is the new home for picoCTF-style beginner challenges. start with General Skills, then beginner Forensics/Cryptography. why it matters: low-stakes flags turn passive reading into "can i actually do this?" dw, easy flags count :3

**TryHackMe - freemium**
use specific rooms/paths, not the homepage: [Linux Fundamentals 1](https://tryhackme.com/room/linuxfundamentalspart1), [Windows Fundamentals 1](https://tryhackme.com/room/windowsfundamentals1xbx), [Intro to Networking](https://tryhackme.com/room/introtonetworking), [Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics), [SOC Level 1](https://tryhackme.com/path/outline/soclevel1), and [Jr Penetration Tester](https://tryhackme.com/path/outline/jrpenetrationtester). why it matters: guided browser VMs keep beginners from getting lost while still making u touch real systems. TryHackMe rate-limits bots; `429` during checks usually means alive.

**HTB Academy + [Starting Point](https://help.hackthebox.com/en/articles/6007919-introduction-to-starting-point) - freemium**
do Starting Point Tier 0: Meow, Fawn, Dancing. then, in HTB Academy's login-gated catalog, filter for free/Tier 0 Linux, Windows, networking, and web modules. why it matters: HTB is less hand-holdy than TryHackMe, so it is the bridge from guided study to independent enumeration. the Academy module catalog is behind login, so the exact public deep-link here is the Starting Point help page.

### blue team, SIEM, and DFIR

**[LetsDefend SOC Fundamentals](https://app.letsdefend.io/training/lessons/soc-fundamentals) + [SOC Analyst Learning Path](https://app.letsdefend.io/path/soc-analyst-learning-path) - freemium**
finish SOC Fundamentals, then close at least 5 alerts with written justification. why it matters: this is the alert-queue workflow: alert -> evidence -> verdict -> escalation/closure.

**[CyberDefenders DanaBot](https://cyberdefenders.org/blueteam-ctf-challenges/danabot/) + [Lockdown](https://cyberdefenders.org/blueteam-ctf-challenges/lockdown/) - mostly free**
submit answers to all questions and write the intrusion timeline. why it matters: PCAP/forensic evidence makes u prove what happened instead of guessing from a dashboard.

**Blue Team Labs Online - freemium**
complete any free phishing/DFIR investigation after creating an account at [BTLO](https://blueteamlabs.online/). why it matters: it gives scored blue-team reps when u need more artifact practice. specific investigations are login-gated, so pick one free scenario and document the artifacts instead of relying on a public deep-link.

**[Splunk Free Training](https://www.splunk.com/en_us/training/free-courses/overview.html) - free**
do the intro/search fundamentals material before Splunk labs. why it matters: SPL is still everywhere in SOC work, and query fluency transfers to KQL.

**[KC7](https://kc7cyber.com/) and [Kusto Detective Agency](https://detective.kusto.io/) - free**
solve the first KQL cases, then write down which table/field answered the question. why it matters: SC-200/Sentinel work is mostly "ask logs better questions."

### crypto, binary, and harder CTF

**[CryptoHack courses](https://cryptohack.org/courses/) - free**
start with Introduction to CryptoHack and Modular Arithmetic after basic Python. why it matters: it teaches the difference between "crypto words" and the math/encoding mistakes attackers exploit.

**[pwn.college dojos](https://pwn.college/dojos) - free**
start with the beginner/on-ramp dojo, then save program security and binary exploitation for later. why it matters: this is where OS internals, memory, and exploitation stop being hand-wavy.

### cloud and Microsoft learning

**Microsoft Learn - free**
use exact learning paths: [SC-900 course](https://learn.microsoft.com/en-us/training/courses/sc-900t00), [SC-200 KQL for Sentinel](https://learn.microsoft.com/en-us/training/paths/sc-200-utilize-kql-for-azure-sentinel/), [Configure Microsoft Sentinel](https://learn.microsoft.com/en-us/training/paths/sc-200-configure-azure-sentinel-environment/), and [Create detections and investigations](https://learn.microsoft.com/en-us/training/paths/sc-200-create-detections-perform-investigations-azure-sentinel/). why it matters: official sandboxes let u learn cloud/Sentinel without inventing a lab from scratch.

**[AWS Skill Builder Security Specialty exam-prep plan](https://skillbuilder.aws/exam-prep/security-specialty) - free/freemium**
use it for current AWS Security Specialty SCS-C03 prep and official practice questions. why it matters: AWS changed from SCS-C02 to SCS-C03, so old PDF guides can be stale.

---

## tools to install or keep ready

**[VirtualBox](https://www.virtualbox.org/) - free hypervisor**
install this first if u are not using VMware/Hyper-V. why it matters: isolated VMs let u break lab machines without touching your real OS.

**[Kali Linux](https://www.kali.org/get-kali/) - attacker VM**
use the VM image, not a bare-metal install. why it matters: u get Nmap, Burp helpers, wordlists, and common tools without turning your daily computer into a lab.

**[Windows Evaluation ISOs](https://www.microsoft.com/en-us/evalcenter/) - target/log source**
build at least one Windows target. why it matters: SOC, PowerShell, Event Viewer, Sysmon, Defender, and Active Directory all need Windows reps.

**[Wireshark](https://www.wireshark.org/download.html) - packet analysis**
use it with TryHackMe Wireshark and CyberDefenders PCAPs. why it matters: packets show what actually crossed the network when logs are incomplete.

**[Burp Suite Community](https://portswigger.net/burp/communitydownload) - web proxy**
use it with PortSwigger labs. why it matters: u see and modify HTTP requests instead of treating the browser like a black box.

**[Wazuh Quickstart](https://documentation.wazuh.com/current/quickstart.html) - home SIEM/XDR**
deploy the current documented version instead of pinning an old version number here. why it matters: a Windows agent + Linux agent + test alerts becomes a real portfolio SOC lab.

**[MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) + [SigmaHQ rules](https://github.com/SigmaHQ/sigma)**
map detections to ATT&CK technique IDs, then read real Sigma YAML. why it matters: this is the common language between incident reports, detections, and job descriptions.

**[Obsidian](https://obsidian.md/) or [OneNote](https://www.onenote.com/) - notes/writeups**
keep lab notes in a searchable place: command, output, why it mattered, screenshot, fix. why it matters: open-book practical exams and real incidents reward organized notes, not memory.

**[Azure free account](https://azure.microsoft.com/en-us/free/) and [AWS Free Tier](https://aws.amazon.com/free/) - cloud sandboxes**
use budget alerts and tear down resources after labs. why it matters: cloud security is IAM + config + logs; u need real accounts eventually, but dont spend money by accident.

---

## frameworks and references - current versions

these are not bedtime reading. use them when a lab/report asks "what category is this?" or "what control does this map to?"

| Reference | Current version | What to do with it | Why it matters |
|---|---:|---|---|
| [MITRE ATT&CK](https://attack.mitre.org/) | v19.1 | map each attack/detection to a tactic + technique ID; use [ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) for coverage maps | shared language for adversary behavior |
| [NIST CSF](https://www.nist.gov/cyberframework) | 2.0 | use the [Quick Start Guides](https://www.nist.gov/cyberframework/quick-start-guides) and [Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) for GRC mapping | organizes security work into GOVERN, IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER |
| [OWASP Top 10 Web](https://owasp.org/www-project-top-ten/) | 2025 | pair each category with PortSwigger Apprentice labs | standard web-risk vocabulary |
| [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) | 2025 | read when building or reviewing AI/LLM features | names prompt, data, model, and agentic risks |
| [ISO/IEC 27001](https://www.iso.org/standard/27001) | 2022 | use the landing page to understand ISMS scope; the full standard is paid and optional | audit/compliance language for management systems |
| [CIS Controls](https://www.cisecurity.org/controls/v8-1) | v8.1 | use the [open 18-controls list](https://www.cisecurity.org/controls/cis-controls-list) for practical safeguard mapping | concrete control checklist from basic hygiene to mature programs |
| [NIST SP 800-30 Rev. 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) | Rev. 1 | use for the mock risk assessment project | method for likelihood, impact, and risk response |
| [NIST SP 800-53 Rev. 5](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) | Rev. 5 | use as a control catalog when mapping evidence | detailed control families used in serious GRC work |

---

## communities and news - use them on purpose

**Reddit:** [r/cybersecurity](https://www.reddit.com/r/cybersecurity/), [r/SecurityCareerAdvice](https://www.reddit.com/r/SecurityCareerAdvice/), [r/blueteamsec](https://www.reddit.com/r/blueteamsec/), [r/netsecstudents](https://www.reddit.com/r/netsecstudents/)
use them to search prior answers and ask specific blockers after u have tried the lab. why it matters: good questions get technical answers; vague "how do i start" posts get noise.

**Discords:** TryHackMe, John Hammond, TCM, and HTB community servers
use them for lab hints, writeup feedback, and finding study groups. why it matters: CTF/lab communities teach u how other learners debug the same stuck point.

**Local communities:** OWASP chapters, BSides conferences, DEF CON groups
attend one talk or volunteer once. why it matters: local security people explain what tools and constraints are common in your region, without needing a job-board list.

**News:** [BleepingComputer](https://www.bleepingcomputer.com/), [The Hacker News](https://thehackernews.com/), [Risky Business](https://risky.biz/), [Darknet Diaries](https://darknetdiaries.com/)
pick one recurring source and write a 3-line note for one story per week: what happened, initial access if known, what control could have reduced impact. why it matters: news becomes useful only when u translate it into mechanisms and controls.

---

## GitHub lists - explore more, not the path

**[Awesome Security](https://github.com/sbilly/awesome-security)** - use after u know the term u are searching for. why it matters: it is a catalog, not a curriculum.

**[Awesome Pentest](https://github.com/enaqx/awesome-pentest)** - use to discover tools after the guide has taught the technique. why it matters: tool lists are only useful when u know the job each tool performs.

**[Awesome CTF](https://github.com/apsdehal/awesome-ctf)** - use when Bandit, CyLab, PortSwigger, and beginner HTB/THM are no longer enough. why it matters: it gives u more reps without pretending every challenge belongs in the core path.

**[SigmaHQ rules](https://github.com/SigmaHQ/sigma)** - read 5 real rules and copy the YAML shape for your own lab detection. why it matters: it shows how detection logic is written in portable form before it becomes SPL, KQL, or a SIEM rule.

---

## stale links R5 already fixed

dont resurrect these in future edits meow:

| Old link/claim | Status from R5 | Use this instead |
|---|---|---|
| old subnetting drill site | dead/rotted to a staging host | [subnetipv4.com](https://subnetipv4.com/) + [Subnetting Mastery](https://www.youtube.com/playlist?list=PLIFyRwBY_4bQUE4IB5c4VPRyDoLgOdExE) |
| old Linux Journey domain as fully free | moved to LabEx and is now freemium | [LabEx Linux Journey](https://labex.io/linuxjourney), tagged **freemium** |
| old TCM Practical Help Desk Teachable URL | old Teachable URL redirects | [TCM Practical Help Desk](https://tcm-sec.com/academy/practical-help-desk/) |
| old Professor Messer generic practice-exams page and old "~$15" wording | dead/soft-404; bundles moved | current per-course Success Bundles linked above |

---

last checked against R5/R7/RC/RD research notes in July 2026. re-check prices, tiers, and cert pages before booking anything paid.
