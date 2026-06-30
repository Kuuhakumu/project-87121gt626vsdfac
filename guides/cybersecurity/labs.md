# Cybersecurity verified lab index meow (July 2026)

> this is the lab shelf for the cyber guide.
> use the goal files as the roadmap; use this page when u need the exact lab, drill, practice-test source, or current replacement link.
>
> rule stays the same: never "open a VM and look around." every primary item below names the exact thing to do, what it proves, and whether it is free/freemium/paid.

[<- Hub](README.md) | [Resources](resources.md) | [Certifications](certifications.md)

---

## how to use this page meow

- **Start from the goal file first.** `01-foundations.md` through `05-job-hunt.md` tell u the order. this file is the verified index behind those tasks.
- **A lab is done only when the gate passes.** "i opened the site" does not count. pass the named level, score, alert, report, or artifact.
- **Write the explanation too.** after the measurable gate, do the `can u explain it?` check from the goal file. both pass or the topic isnt done yet qwq
- **Paid cert training is optional.** the free/freemium lab path is the default. paid bundles are listed only so u dont buy stale or wrong things.

---

## currency fixes baked in (do not undo these)

| Old link / claim | Current status | Use this instead |
|---|---|---|
| old subnetting drill site | broken / rotted to unrelated staging host | [subnetipv4.com](https://subnetipv4.com/) plus [Practical Networking - Subnetting Mastery](https://www.youtube.com/playlist?list=PLIFyRwBY_4bQUE4IB5c4VPRyDoLgOdExE) |
| `professormesser.com/practice-exams/` and "~$15 exams" | dead/soft-404; products moved | current per-course Professor Messer Success Bundles: [A+ Core 1](https://www.professormesser.com/220-1201-success-bundle/), [A+ Core 2](https://www.professormesser.com/220-1202-success-bundle/), [Network+](https://www.professormesser.com/n10-009-success-bundle/), [Security+](https://www.professormesser.com/sy0-701-success-bundle/) |
| `securityblue.team` / old BTL1 URLs | redirects after rebrand | [Centri - Blue Team Level 1](https://www.centri.org/certifications/blue-team-level-1) |
| "AZ-500 successor TBA" | stale | Azure security path is now [SC-500 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500); AZ-500 retires 2026-08-31 |
| AWS Security `SCS-C02` PDFs | retired / stale | [AWS Certified Security - Specialty exam page](https://aws.amazon.com/certification/certified-security-specialty/) and [official SCS-C03 exam guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03.html) |
| "INE PTS/eJPT training is free" | stale; PTS is paywalled behind INE subscription | use [INE eJPT v2 cert page](https://ine.com/security/certifications/ejpt-certification/) only for cert logistics; free prep is TryHackMe Jr Pentester + PortSwigger + HTB Starting Point |

last checked from R5/RC/RD research notes in July 2026. re-check paid prices before buying anything.

---

## foundations, networking, and first CTF reps

| Exact resource | Cost | What u do | Gate |
|---|---:|---|---|
| [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) | free | SSH into real Linux levels; files, permissions, pipes, search, keys | clear levels 0-15 unaided for foundations; keep going to 34 for more reps |
| [TryHackMe - Linux Fundamentals 1](https://tryhackme.com/room/linuxfundamentalspart1) | freemium/free room | browser Linux VM; filesystem, commands, permissions | finish parts 1-3 if u need hand-holding before Bandit |
| [TryHackMe - Windows Fundamentals 1](https://tryhackme.com/room/windowsfundamentals1xbx) | freemium/free room | Windows basics, Registry, UAC, Defender | finish parts 1-3 before Windows logging work |
| [TryHackMe - Intro to Networking](https://tryhackme.com/room/introtonetworking) | freemium/free room | OSI/TCP/IP, packets, routing basics | finish room, then explain DNS -> TCP -> HTTP in order |
| [TryHackMe - Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics) | freemium/free room | load PCAPs, filter, inspect traffic | identify one TCP handshake and one HTTP request in a capture |
| [subnetipv4.com](https://subnetipv4.com/) | free | generate IPv4 subnet drills | solve `/26`, `/27`, `/28` network ID, broadcast, usable range, host count in under 60s each |
| [CyLab Security Academy](https://cylabacademy.org/) | free | picoCTF-style beginner General Skills / Forensics / Crypto | solve 10 beginner challenges and write 3 short notes on what command/tool solved each |
| [OverTheWire Natas](https://overthewire.org/wargames/natas/) | free | browser web basics: source, cookies, auth, injection | clear Natas 0-6 before PortSwigger, then 7-15 as a stretch |

TryHackMe may return `429` to automated checks; that usually means the room is alive but bot-limited. use a browser.

---

## practice-test gates and cert-aligned drills

these are not "labs" in the VM sense, but they are still objective gates. use them when a goal asks for a real score.

| Exact resource | Cost | Use it for | Gate |
|---|---:|---|---|
| [ExamCompass A+ practice tests](https://www.examcompass.com/comptia/a-plus-certification/free-a-plus-practice-tests) | free | A+ Core 1/2 topic checks | 80%+ on 3 fresh current-code attempts for the domain u just studied |
| [ExamCompass Network+ practice tests](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests) | free | N10-009 networking checks | 85%+ on 3 fresh N10-009 attempts; ignore retired legacy sets |
| [ExamCompass Security+ practice tests](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) | free | SY0-701 security checks | 85%+ on 3 fresh SY0-701 attempts; ignore retired SY0-601 sets |
| [ISC2 CC Practice Quiz](https://cloud.connect.isc2.org/cc-quiz) | free, lead-gated | CC-style fundamentals checkpoint | pass the quiz, then use the guide's `can u explain it?` gates as the real free fundamentals checkpoint before any paid CC exam |
| [ISC2 CC Flash Cards](https://cloud.connect.isc2.org/cc-flashcards) | free, lead-gated | CC vocab reinforcement | only use after mechanisms make sense; dont memorize first |
| [Messer A+ Core 1 Success Bundle](https://www.professormesser.com/220-1201-success-bundle/) | paid optional | paid A+ Core 1 practice exams | 85%+ on 3 fresh attempts before booking |
| [Messer A+ Core 2 Success Bundle](https://www.professormesser.com/220-1202-success-bundle/) | paid optional | paid A+ Core 2 practice exams | 85%+ on 3 fresh attempts before booking |
| [Messer Network+ Success Bundle](https://www.professormesser.com/n10-009-success-bundle/) | paid optional | paid N10-009 practice exams | 85%+ on 3 fresh attempts before booking |
| [Messer Security+ Success Bundle](https://www.professormesser.com/sy0-701-success-bundle/) | paid optional | paid SY0-701 practice exams | 85%+ on 3 fresh attempts before booking |
| [Microsoft SC-900 official practice assessment](https://learn.microsoft.com/en-us/credentials/certifications/exams/sc-900/practice/assessment?assessment-type=practice&assessmentId=25) | free | Microsoft security/compliance/identity fundamentals | 80%+ across 2 fresh runs before booking |
| [Microsoft SC-200 official practice assessment](https://learn.microsoft.com/en-us/credentials/certifications/exams/sc-200/practice/assessment?assessment-type=practice&assessmentId=59) | free | Sentinel/Defender SOC checkpoint | 80%+ after finishing the SC-200 Learn paths |
| [AWS Skill Builder - Security Specialty exam-prep plan](https://skillbuilder.aws/exam-prep/security-specialty) | free/freemium | current AWS Security Specialty `SCS-C03` practice | 80%+ on official practice questions before booking |

---

## web app security

| Exact resource | Cost | What u do | Gate |
|---|---:|---|---|
| [PortSwigger Web Security Academy - all labs](https://portswigger.net/web-security/all-labs) | free | free live web labs with Burp Community | use category gates below; dont just browse the list |
| [PortSwigger - SQL injection](https://portswigger.net/web-security/sql-injection) | free | SQLi Apprentice labs first | solve all Apprentice SQLi labs and explain why parameterized queries stop it |
| [PortSwigger - Cross-site scripting](https://portswigger.net/web-security/cross-site-scripting) | free | reflected, stored, DOM XSS | solve all Apprentice XSS labs and explain output encoding vs sanitization |
| [PortSwigger - Access control](https://portswigger.net/web-security/access-control) | free | IDOR / broken authorization | solve the Apprentice access-control labs and explain server-side authorization |
| [PortSwigger - SSRF](https://portswigger.net/web-security/ssrf) | free | server-side request forgery | solve at least 2 Apprentice SSRF labs before cloud metadata topics |
| [PortSwigger - File path traversal](https://portswigger.net/web-security/file-path-traversal) | free | path traversal / file inclusion | solve 2 Apprentice labs and explain canonicalization |
| [PortSwigger - OS command injection](https://portswigger.net/web-security/os-command-injection) | free | command injection | solve 2 Apprentice labs and explain command execution context |
| [TryHackMe - OWASP Top 10](https://tryhackme.com/room/owasptop102021) | freemium | guided room across common web flaws | finish the room if PortSwigger feels too abrupt |

---

## SOC, SIEM, blue team, and DFIR

| Exact resource | Cost | What u do | Gate |
|---|---:|---|---|
| [LetsDefend - SOC Fundamentals](https://app.letsdefend.io/training/lessons/soc-fundamentals) | free | SOC roles, alert flow, EDR/SOAR/log basics | complete course and explain alert -> evidence -> verdict |
| [LetsDefend - SOC Analyst Learning Path](https://app.letsdefend.io/path/soc-analyst-learning-path) | freemium | close real-style alert queue cases | close at least 5 alerts with written justification |
| [TryHackMe - SOC Level 1 path](https://tryhackme.com/path/outline/soclevel1) | freemium | guided SOC modules: SIEM, EDR, SOAR, threat intel, packet analysis | finish the intro/blue modules that match your weak area |
| [CyberDefenders - DanaBot](https://cyberdefenders.org/blueteam-ctf-challenges/danabot/) | mostly free | PCAP/IOC investigation | submit correct answers to all questions and write a mini timeline |
| [CyberDefenders - Lockdown](https://cyberdefenders.org/blueteam-ctf-challenges/lockdown/) | mostly free | multi-artifact DFIR scenario | finish all questions and explain intrusion timeline from artifacts |
| [Blue Team Labs Online](https://blueteamlabs.online/) | freemium | phishing/DFIR investigations behind login | complete any 1 free investigation at 80%+; specific public labs are login-gated |
| [Splunk Free Training](https://www.splunk.com/en_us/training/free-courses/overview.html) | free | SPL fundamentals before BOTS/Splunk projects | finish intro/search material and write one search isolating failed logins |
| [Splunk BOTS v3 dataset](https://github.com/splunk/botsv3) | free | real attack dataset for SOC report project | write an incident report with timeline, IOCs, ATT&CK mapping, recommendations |
| [KC7](https://kc7cyber.com/) | free | KQL investigation game | solve 3 cases and record table/field names used |
| [Kusto Detective Agency](https://detective.kusto.io/) | free | KQL puzzles for Sentinel-style thinking | solve first case and explain each KQL operator used |
| [Microsoft Learn - Configure your Microsoft Sentinel environment](https://learn.microsoft.com/en-us/training/paths/sc-200-configure-azure-sentinel-environment/) | free | SC-200 SIEM setup path | complete sandbox exercises if using Microsoft SOC track |
| [Microsoft Learn - Connect logs to Microsoft Sentinel](https://learn.microsoft.com/en-us/training/paths/sc-200-connect-logs-to-azure-sentinel/) | free | Sentinel connectors/log ingestion | connect or simulate a log source and explain connector -> table |
| [Microsoft Learn - Create queries for Sentinel using KQL](https://learn.microsoft.com/en-us/training/paths/sc-200-utilize-kql-for-azure-sentinel/) | free | KQL for Sentinel | write one KQL query that finds brute-force-like behavior |
| [Microsoft Learn - Create detections and investigations](https://learn.microsoft.com/en-us/training/paths/sc-200-create-detections-perform-investigations-azure-sentinel/) | free | analytics rules, investigations, playbooks | build one test analytics rule and map it to ATT&CK |
| [Microsoft Learn - Perform threat hunting in Sentinel](https://learn.microsoft.com/en-us/training/paths/sc-200-perform-threat-hunting-azure-sentinel/) | free | hunting with KQL/search/notebooks | produce one hunt query and explain hypothesis -> result |
| [Centri - Blue Team Level 1](https://www.centri.org/certifications/blue-team-level-1) | paid optional | practical BTL1 course/labs/exam | buy only when free SOC/DFIR labs feel comfortable and u want the 24h practical checkpoint |

---

## red team and pentest practice

| Exact resource | Cost | What u do | Gate |
|---|---:|---|---|
| [TryHackMe - Jr Penetration Tester path](https://tryhackme.com/path/outline/jrpenetrationtester) | freemium | guided recon, web, enum, privesc basics | complete the beginner modules that match eJPT-level prep |
| [TryHackMe - Offensive Pentesting path](https://tryhackme.com/path/outline/offensivepentesting) | freemium | AD, buffer overflow, harder offensive rooms | use after Jr Pentester; finish AD/pivot rooms before PNPT/CPTS-style work |
| [Hack The Box - Starting Point intro](https://help.hackthebox.com/en/articles/6007919-introduction-to-starting-point) | freemium | Tier 0 boxes: Meow, Fawn, Dancing, etc. | complete Meow, Fawn, Dancing without walkthroughs |
| [HTB Academy - Penetration Tester path preview](https://academy.hackthebox.com/path/preview/penetration-tester) | freemium/paid | CPTS-aligned modules from methodology through report | use as the deep paid/offensive track if CPTS is your checkpoint |
| [PortSwigger Web Security Academy](https://portswigger.net/web-security/all-labs) | free | offensive web practice | Apprentice SQLi + XSS + access control before any paid web module |
| [VulnHub - Kioptrix series](https://www.vulnhub.com/series/kioptrix,8/) | free | classic vulnerable VMs | root Kioptrix Level 1 and write a short report |
| [VulnHub - Kioptrix Level 1](https://www.vulnhub.com/entry/kioptrix-level-1-1,22/) | free | first full recon -> exploit -> root VM | root it and document commands/evidence/remediation |
| [VulnHub - Stapler 1](https://www.vulnhub.com/entry/stapler-1,150/) | free | next-rung enumeration/privesc practice | root it after Kioptrix |
| [VulnHub - FristiLeaks 1.3](https://www.vulnhub.com/entry/fristileaks-13,133/) | free | web foothold + privesc practice | root it after Kioptrix |
| [TCM Practical Ethical Hacking](https://tcm-sec.com/academy/practical-ethical-hacking/) | paid optional | PEH methodology, AD, web, reporting | use if buying PNPT prep; current URL replaces old Teachable links |
| [TCM PNPT certification](https://certifications.tcm-sec.com/pnpt/) | paid optional | 5-day AD pentest + 2-day report + live debrief | only after u can write a clean report from free labs |
| [INE eJPT v2 certification](https://ine.com/security/certifications/ejpt-certification/) | paid optional | entry practical pentest exam logistics | do not present INE PTS as free; free prep is THM + PortSwigger + HTB Starting Point |

---

## cloud security

| Exact resource | Cost | What u do | Gate |
|---|---:|---|---|
| [Microsoft Learn SC-900 course](https://learn.microsoft.com/en-us/training/courses/sc-900t00) | free | Microsoft security/compliance/identity fundamentals | finish the 4 SC-900 learning paths and score 80%+ on official practice |
| [SC-900 - Security/compliance/identity concepts](https://learn.microsoft.com/en-us/training/paths/describe-concepts-of-security-compliance-identity/) | free | shared responsibility, Zero Trust, encryption basics | finish path and explain shared responsibility |
| [SC-900 - Microsoft Entra](https://learn.microsoft.com/en-us/training/paths/describe-capabilities-of-microsoft-identity-access/) | free | identity, access, MFA, Conditional Access | explain user vs role vs policy |
| [SC-900 - Microsoft security solutions](https://learn.microsoft.com/en-us/training/paths/describe-capabilities-of-microsoft-security-solutions/) | free | Defender, Sentinel, secure score | explain SIEM vs XDR vs CSPM |
| [SC-900 - Microsoft Purview and privacy](https://learn.microsoft.com/en-us/training/paths/describe-capabilities-of-microsoft-compliance-solutions/) | free | DLP, classification, retention | explain data classification -> policy -> evidence |
| [Microsoft SC-500 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500) | free | current Azure/AI cloud-security objectives | use as syllabus after SC-900; dedicated SC-500 learning path was still pending in RD3 |
| [AWS Certified Security - Specialty page](https://aws.amazon.com/certification/certified-security-specialty/) | free page / paid exam | current AWS Security Specialty overview | confirm it says `SCS-C03` before booking |
| [AWS SCS-C03 official exam guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03.html) | free | current domains/weights | map weak topics to labs; do not use old SCS-C02 PDFs |
| [AWS Skill Builder - Security Specialty exam-prep plan](https://skillbuilder.aws/exam-prep/security-specialty) | free/freemium | official SCS-C03 prep and practice questions | 80%+ on practice questions before booking |
| [Azure free account](https://azure.microsoft.com/en-us/free/) | free trial / card required | Azure sandbox for Defender/Sentinel/IAM | set budget alerts; tear down resources |
| [AWS Free Tier](https://aws.amazon.com/free/) | free tier / card required | AWS sandbox for IAM, S3, GuardDuty, Config | set budget alerts; tear down resources |
| [flaws.cloud](http://flaws.cloud/) | free | classic AWS S3/IAM misconfiguration walkthrough | clear levels 1-3 unaided; intentionally HTTP-only origin |
| [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) | free tool, cloud usage may cost | vulnerable-by-design AWS scenarios in your own account | complete one scenario, then write the defensive fix |
| [ScoutSuite](https://github.com/nccgroup/ScoutSuite) | free | multi-cloud posture audit report | scan an account u own, remediate one finding, re-scan |
| [Prowler](https://github.com/prowler-cloud/prowler) | free | AWS/Azure/GCP benchmark scanner | scan an account u own, remediate one finding, re-scan |

---

## GRC and risk artifacts

| Exact resource | Cost | What u do | Gate |
|---|---:|---|---|
| [NIST SP 800-30 Rev. 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) | free | risk assessment method | build a 3-asset risk register with likelihood, impact, treatment, residual risk |
| [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) | free | map controls to CSF categories and references | map 5 controls to Function + Category |
| [NIST CSF 2.0 Quick Start Guides](https://www.nist.gov/cyberframework/quick-start-guides) | free | beginner on-ramp to CSF 2.0 | read before the Reference Tool if CSF feels huge |
| [CIS Controls list](https://www.cisecurity.org/controls/cis-controls-list) | free | concrete safeguard list | map 3 lab findings to CIS controls |
| [Prabh Nair - GRC Practical Approach Part 1](https://www.youtube.com/watch?v=mq_vSLHm4r0) | free | practical GRC analyst workflow | write a one-page summary: requirement -> control -> evidence -> finding -> remediation |

---

## dead, moved, stale, or paywalled traps

| Resource | Status | Use instead |
|---|---|---|
| old subnetting drill site | broken | [subnetipv4.com](https://subnetipv4.com/) |
| `professormesser.com/practice-exams/` | soft-404 / page-not-found | per-course Success Bundles listed above |
| `securityblue.team` / old BTL1 pages | redirected after rebrand | [Centri BTL1](https://www.centri.org/certifications/blue-team-level-1) |
| INE Penetration Testing Student as "free" | stale; paywalled | free prep stack: [TryHackMe Jr Pentester](https://tryhackme.com/path/outline/jrpenetrationtester), [PortSwigger labs](https://portswigger.net/web-security/all-labs), [HTB Starting Point](https://help.hackthebox.com/en/articles/6007919-introduction-to-starting-point) |
| SCS-C02 exam guide PDFs | retired | [SCS-C03 HTML exam guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03.html) |
| AZ-500 as a new learner target | retires 2026-08-31 | [SC-500 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500) |
| Old SC-200 guessed "Microsoft Sentinel" slugs | some 404; old slug names still resolve | use the exact SC-200 Learn path URLs in the SOC section |
| Cybrary free labs | gutted/restricted since older guides | LetsDefend, CyberDefenders, BTLO, KC7 |
| SANS CyberAces | discontinued | TryHackMe Pre-Security, HTB free modules, Bandit |
| RangeForce Community | restricted | KC7, LetsDefend, CyberDefenders |

---

*Verification notes: R5/RC/RD research checked these URLs in July 2026 using status checks plus content checks where possible. `PortSwigger` can 404 on HEAD but load on GET. `TryHackMe` commonly returns 429 to bots but works in-browser. Some app catalogs are login-gated; where that happens, this index names the exact path/page and marks the gate honestly.*
