# certification guide - cybersecurity meow (July 2026)

> Verified via official sources + repo research, July 2026.
> prices are USD unless noted.
> **⚠️ price caveat:** CompTIA store prices are JS-gated / redirect-heavy, so the CompTIA prices below are current-best figures from the July 2026 research pass. confirm the checkout price at the official store before booking, oki.

Confidence: ✅ official/current page verified · ⚠️ price/store JS-gated or region-priced · ⛔ blocked / not worth using.

---

## TL;DR - how to use this file

dont start here.
start in the goal files, pass the lab/CTF/project gates, then come back here only when u are asking "is an exam worth paying for now?" meow.

the path is:

**mechanism explanation -> interactive lab / CTF / project gate -> `can u explain it?` -> optional cert checkpoint**

certs do not replace the work.
they are just outside checkpoints after the work is already visible.

- **Support on-ramp checkpoint:** CompTIA **A+ (220-1201 / 220-1202)**, about **$274/exam ⚠️**. useful if u have no IT background; skip the paid exam if real support work already proves the floor.
- **Networking floor checkpoint:** CompTIA **Network+ (N10-009)**, about **$399 ⚠️**. useful when subnetting, ports, routing, Wi-Fi, and troubleshooting still need an outside bar.
- **Security fundamentals checkpoint:** ISC2 **CC**, about **$199 + $50/yr AMF**. optional now; the 1MCC free-voucher program closed to new enrollments on **2026-05-20**.
- **Entry-filter checkpoint:** CompTIA **Security+ (SY0-701)**, about **$439 ⚠️**. still the cleanest HR baseline, but book it after the Goal 2 gates, not after a video binge.
- **Specialization checkpoints:** Blue / SOC, Red / Pentest, Cloud, or GRC certs sit after the Goal 3/4 labs and reports.
- **do not start AZ-500 now** unless an employer explicitly needs it before retirement. it retires **August 31, 2026**; use **SC-500** as the Microsoft cloud-security successor path.
- **Skip for most beginners:** CEH, PenTest+, Cloud+, CASP+/SecurityX, CISA/CISM at entry. wrong tier, weak ROI, or experience-gated.

---

## cert data sheet

| Cert | Code | Price | Format / pass | Valid | why it matters |
|---|---|---:|---|---|---|
| CompTIA A+ | **220-1201 / 220-1202** | ⚠️ **~$274/exam** (~$548 both cores) | MCQ+PBQ, <=90q, 90m each. Core 1 **675/900**, Core 2 **700/900** | 3 yr | support-role on-ramp; teaches hardware, OS, networking, basic security |
| CompTIA Network+ | **N10-009** | ⚠️ **~$399** | MCQ+PBQ, <=90q, 90m, **720/900** | 3 yr | the network floor Security+ assumes |
| ISC2 CC | **CC** | **~$199 exam + $50/yr AMF** | **100-125 items**, 120m, **700/1000** | 3 yr / 45 CPE | fundamentals checkpoint; DoD 8140.03 approved; new outline effective **2026-09-01** |
| CompTIA Security+ | **SY0-701** | ⚠️ **~$439** | MCQ+PBQ, <=90q, 90m, **750/900** | 3 yr | entry security baseline / HR filter |
| CompTIA CySA+ | **CS0-004 (V4 current)**; CS0-003 retires **2026-12-22** | ⚠️ ~$464 | MCQ+PBQ, <=85q, 165m, **750/900** | 3 yr | blue-team / SOC differentiator, especially DoD/government-adjacent |
| CompTIA PenTest+ | **PT0-003** | ⚠️ ~$439 | MCQ+PBQ, <=85q, 165m, **750/900** | 3 yr | usually loses to PNPT/CPTS/OSCP for offensive signal |
| Microsoft SC-900 | **SC-900**; English update scheduled **2026-07-28** (agent ID / Entra agent identities) | ⚠️ ~$99 region-priced | MCQ+scenario, 45m, **700/1000** | no expiry | light Microsoft security/compliance/identity on-ramp |
| Microsoft SC-200 | **SC-200**; English update scheduled **2026-07-28** (Security Copilot, Sentinel Data lake, Sentinel Graph) | ⚠️ ~$165 region-priced | MCQ+interactive, 100m, **700/1000** | 1 yr, renewal free | Microsoft Sentinel / Defender SOC signal |
| Microsoft AZ-500 | **AZ-500** | ⚠️ region-priced | 100m, Microsoft role-based format | **retires 2026-08-31** | dont start it now; use the successor path after retirement |
| Microsoft SC-500 | **SC-500**; beta/GA window **July 2026** | ⚠️ region-priced | Microsoft role-based, **700/1000** pass | Microsoft associate renewal pattern | AZ-500 successor: Cloud and AI Security Engineer Associate; re-check exam page after GA |
| BTL1 (Centri) | [Blue Team Level 1](https://www.centri.org/certifications/blue-team-level-1) | **£399** (~$505) | 24h practical, **70%** pass | lifetime | practical SOC proof; good "can u actually investigate?" checkpoint |
| INE eJPT | **eJPT v2** | ⚠️ ~$249 voucher; INE Fundamentals sub may bundle voucher | practical, auto-graded | 3 yr | beginner red-team stepping stone; PTS training is no longer free |
| HTB CPTS | **CPTS** | ⚠️ ~$210 | practical engagement + report | no expiry | strong technical pentest signal; exact exam logistics JS-gated |
| TCM PNPT | **PNPT** | $499; $399 sale noted through **2026-07-15** | 5-day practical + report/debrief | lifetime | practical AD/pentest report signal |
| OffSec OSCP | **PEN-200 / OSCP** | ⚠️ ~$1,649 Learn One | 24h practical + report | no expiry | pentest baseline filter, later not entry |
| Cisco CCNA | **200-301** | ⚠️ ~$330 | MCQ+sim, 120m | 3 yr | stronger networking signal than Network+ if u go deep |
| GIAC GSEC | **GSEC** | ⚠️ ~$949 exam-only figure | CyberLive labs, 106q, 4h, **72%** | 4 yr | strong SANS brand; usually employer-sponsored |
| EC-Council CEH | **CEH v13** | ⚠️ ~$950-$1,999 | 125 MCQ, 4h | 3 yr | only if a specific job requires it |
| Google Cybersecurity Cert | Coursera cert | ⚠️ ~$49/mo (~$294 at 6 mo) | 8-course program, no proctored exam | n/a | pre-Security+ confidence builder, not a replacement |

---

## optional checkpoint signal ranking

this ranking is not a todo list.
it just tells u how employers tend to read the checkpoint **after** your labs, reports, and GitHub already show the skill qwq.

### baseline filters

- **Security+ SY0-701** - the broadest entry security keyword. DoD/government/contractor/MSP screens still care.
- **ISC2 CC** - DoD 8140.03 approved fundamentals checkpoint. useful proof if u want it, but not magic by itself.
- **A+** - baseline for IT-support entry roles, not direct security roles. good if support is your bridge.
- **OSCP** - baseline only for dedicated pentest roles, and usually after u can already do the red-chain work.

### strong differentiators

- **CySA+ CS0-004** - SOC / defensive analyst signal, especially where CompTIA/DoD language matters.
- **BTL1 (Centri)** - practical SOC exam; nice because it tests investigation under time pressure.
- **SC-200** - Microsoft Sentinel / Defender XDR shops.
- **CCNA** - real networking depth; respected outside CompTIA-heavy environments.
- **PNPT / HTB CPTS** - offensive certs technical interviewers tend to respect more than MCQ pentest certs.
- **GSEC** - strong SANS signal, but expensive enough that employer funding matters.
- **Network+** - not flashy, but it stops Security+ networking questions from feeling like fog.

### nice-to-have

- **SC-900** - easy Microsoft security/compliance/identity primer.
- **Google Cybersecurity Cert** - gentle pre-Security+ on-ramp for career changers.
- **eJPT v2** - beginner red-team confidence before CPTS/PNPT.

### skip for most people

- **PenTest+ PT0-003** - usually loses to PNPT/CPTS/OSCP for offensive signal.
- **CEH** - high cost, low practical signal; take only if a job explicitly names it.
- **Cloud+** - beaten by vendor cloud certs.
- **CASP+ / SecurityX** - expert tier; not entry.
- **CISA / CISM** - experience-gated. learn the GRC topics now; certify later.
- **AZ-500** - retiring **August 31, 2026**.

---

## study-order map - certs as byproducts

this is the anti-getting-lost part.
do the topic groups in order, then use the exam as a checkpoint.
dont build separate cert silos qwq.

for this map:

- **Goal 2** = [Networking & Security Core](02-core.md): Network+, CC/Security+ superset, crypto, IAM, attacks, SecOps, IR, GRC.
- **Goal 3** = [Scripting, Logs & CTF](03-scripting-ctf.md): Python, PowerShell, KQL/SPL, regex, log parsing, CTF reps.
- **Goal 4** = [Specialization](04-specialization.md): Blue / SOC lane, Red / pentest lane, Cloud security lane, and the GRC layer.

| Optional checkpoint | finish these lab/topic gates first | u are ready when... |
|---|---|---|
| **A+ 220-1201 / 220-1202** | [Goal 1](01-foundations.md) Blocks 1-4: hardware -> OS -> networking/security intro -> practice sprint | Core 1 + Core 2 ExamCompass gates pass, and u can explain hardware/OS/network basics unaided |
| **Network+ N10-009** | Goal 1 networking intro -> Goal 2 Block 1 networking floor -> subnetipv4 drills -> Wireshark / TryHackMe networking labs -> Block 6 Network+ readiness | subnetting `/26`-`/28` is automatic, troubleshooting tools make sense, and ExamCompass/Dion gates pass |
| **ISC2 CC** | Goal 2 security foundations -> crypto + identity/access -> operations + IR + GRC -> CC practice quiz/flashcards | all 5 CC domains are explainable; if testing on/after **2026-09-01**, re-check the ISC2 outline first |
| **Security+ SY0-701** | Goal 2 networking floor -> foundations -> crypto/IAM -> attacks + CTF thread -> operations/IR/GRC -> Security+ readiness | 85%+ fresh SY0-701 practice gates pass, the VM baseline/risk note/IR runbook exist, and u can tell one full attack/detect/respond story |
| **CySA+ CS0-004** | Security+ readiness -> Goal 3 KQL/SPL/regex + log parsing -> Goal 4 Blue / SOC lane -> SOC reports | u can triage alerts, query logs, explain vuln management, and write the report/comms side |
| **BTL1 (Centri)** | Security+ readiness -> Goal 3 log tooling + CTF reps -> Goal 4 Blue / SOC lane -> CyberDefenders/LetsDefend cases | u can complete blue-team cases, build timelines, and justify IR decisions under time pressure |
| **SC-200** | Security+ readiness -> Goal 3 KQL -> Goal 4 Blue / SOC lane, Microsoft-flavored -> Sentinel/Defender labs | Sentinel/Defender incident flow, hunting, KQL, and detection tuning feel normal |
| **eJPT v2** | Goal 2 networking + attacks -> Goal 3 CTF level-up hub -> Goal 4 Red lane beginner boxes -> PortSwigger/HTB/THM reps | u can enumerate services, get a shell legally, and explain what each step proved |
| **HTB CPTS / PNPT** | eJPT-level comfort -> Goal 4 Red lane AD/privesc/pivoting -> full pentest report path | u can chain recon -> exploit -> privesc -> AD/pivoting -> report without living in walkthroughs |
| **OSCP** | CPTS/PNPT-style report discipline -> more Red lane lab reps under time pressure | u can solve boxes consistently under time pressure and write clean evidence/remediation |
| **SC-900** | Goal 4 Cloud intro -> GRC layer basics -> Microsoft Learn/practice-assessment checks | Entra, Defender, Sentinel, Purview, compliance, and identity terms are clear |
| **Cloud security successor path** | Security+ -> SC-900 -> Goal 4 Cloud lane -> flaws.cloud + Prowler/ScoutSuite + before/after remediation evidence | shared responsibility, IAM, CSPM, logging, and misconfig remediation are portfolio-visible; use SC-500 for Microsoft cloud security and SCS-C03 for AWS |
| **GRC / compliance path** | Security+ Domain 5 -> Goal 4 GRC layer -> risk register + control crosswalk + evidence appendix | u can produce a risk register, control crosswalk, and evidence appendix; CISA/CISM wait until experience |

---

## lab-first checkpoint overlays by lane

this is the part to use when u are deciding what exam, if any, fits your next move.
notice the order: labs first, explanation second, exam last.

### universal beginner - security core

**do the work first:**
- [ ] [Goal 0](00-prep.md): set up notes + lab accounts, then start the beginner CTF thread with OverTheWire Bandit and picoCTF/CyLab style reps.
- [ ] [Goal 1](01-foundations.md): pass the A+ Core 1/Core 2 practice gates and explain hardware, OS, accounts, malware basics, and troubleshooting unaided.
- [ ] [Goal 2](02-core.md): complete the networking and security mechanism blocks, including TryHackMe Intro to Networking, Wireshark packet labels, subnet drills, a VM baseline, an IR runbook, and a risk note.

**measurable gate:** current-code ExamCompass gates pass, subnet drills pass, networking labs are complete, and the VM baseline / IR runbook / risk note artifacts exist.

**can u explain it?** ✅ - unaided, narrate one normal system -> attack -> detection -> response chain: DNS/TCP/TLS, identity/authz, logging, SIEM signal, IR containment, and risk/control update.

**after these gates, optional checkpoints become realistic:**
- **A+ 220-1201 / 220-1202** only if u need the support-role on-ramp signal.
- **Network+ N10-009** only if networking is still the thing employers will question.
- **ISC2 CC** only if u want the paid fundamentals checkpoint and understand it is **~$199 + $50/yr AMF**, not free.
- **Security+ SY0-701** when the Goal 2 merged-study gates pass and u can tell one attack -> detect -> respond story without notes.

### blue team / SOC

**do the work first:**
- [ ] [Goal 3](03-scripting-ctf.md): Python, PowerShell, regex, KQL, SPL, and log parsing gates pass.
- [ ] [Goal 4 Blue / SOC](04-specialization.md): complete LetsDefend SOC Fundamentals or SOC Analyst path work, CyberDefenders DanaBot, a bigger blue scenario like Lockdown, Wazuh/Splunk/KC7/Kusto practice, and one Sigma -> SPL/KQL detection writeup.
- [ ] portfolio proof exists: alert -> evidence -> timeline -> verdict -> detection improvement.

**measurable gate:** DanaBot answers are correct, at least one larger blue scenario or LetsDefend alert case is complete, and the Sigma + SPL/KQL detection artifact is saved.

**can u explain it?** ✅ - unaided, walk one alert from raw log -> parsed fields -> correlation rule -> enrichment -> triage verdict -> ATT&CK technique -> detection improvement.

**after these gates, optional checkpoints become realistic:**
- **BTL1 (Centri)** if u want a 24h practical SOC checkpoint.
- **CySA+ CS0-004** if vendor-neutral SOC, vulnerability management, reporting, or DoD language matters.
- **SC-200** if the target shop uses Microsoft Sentinel / Defender XDR and KQL.

quick caveat: no verified Savill cram exists for this exam.
use Microsoft Learn + Sentinel/Defender labs instead.

### red team / pentest

**do the work first:**
- [ ] [Goal 2](02-core.md): network/security controls and attack-mechanism clusters pass.
- [ ] [Goal 4 Red / pentest](04-specialization.md): HTB Starting Point **Meow**, **Fawn**, and **Dancing** are rooted; PortSwigger Apprentice SQLi/XSS/access-control labs are solved; Kioptrix Level 1 is rooted; a pentest report exists.
- [ ] CTF/project proof exists: recon -> exploit -> privesc -> evidence -> remediation, with permission and scope written down.

**measurable gate:** the HTB boxes are complete, PortSwigger Apprentice labs are solved, Kioptrix reaches root, and the report includes scope, evidence, impact, and remediation.

**can u explain it?** ✅ - unaided, read an `nmap -sV` result and name next enumeration steps; then explain reverse shell vs bind shell, one privesc vector, and why the report is the actual deliverable.

**after these gates, optional checkpoints become realistic:**
- **eJPT v2** as the beginner methodology checkpoint. INE PTS is not free anymore; use TryHackMe Jr Pentester + PortSwigger + HTB Starting Point as the free prep stack.
- **HTB CPTS** if u want the broadest technical path plus a graded report.
- **PNPT** if u want the AD chain, 5-day assessment, 2-day report, and live debrief.
- **OSCP** later, when boxes and reports are already normal under time pressure.

red usually isnt the first job.
thats not gatekeeping; its just hiring reality rn.
SOC, IT, cloud, or GRC can be the bridge while u keep the CTF/report thread alive.

### cloud security

**do the work first:**
- [ ] [Goal 4 Cloud security](04-specialization.md): flaws.cloud levels 1-3 are clear, ScoutSuite or Prowler has scanned an account u own, one finding is remediated and re-scanned, and the before/after evidence is saved.
- [ ] optional attack-side proof: one CloudGoat scenario is completed in an account u control, then deleted so it does not keep billing.
- [ ] detection proof exists: Sentinel/KQL or GuardDuty/CloudTrail flow is explained from log source -> alert -> triage.

**measurable gate:** flaws.cloud levels 1-3 are complete, one ScoutSuite/Prowler finding is fixed and absent on re-scan, and the before/after evidence is saved.

**can u explain it?** ✅ - unaided, draw the shared-responsibility line, explain one public-storage or open-security-group exposure, name the exact fix, and trace one cloud log source into an alert.

**after these gates, optional checkpoints become realistic:**
- **SC-900** for Microsoft security/compliance/identity fundamentals.
- **SC-500** for the Microsoft cloud + AI security successor path after AZ-500.
- **AWS Security Specialty SCS-C03** if AWS is the lane.
- **SC-200** only if the job is more SOC/Sentinel than cloud posture.

do **not** start AZ-500 now unless an employer explicitly requires it before **2026-08-31**.
do **not** study from old **SCS-C02** PDFs; **SCS-C03** is current.

### GRC / compliance

**do the work first:**
- [ ] [Goal 2 Cluster H](02-core.md): Security+ Domain 5 mechanisms pass: risk, policy/standard/procedure, BIA, third-party risk, audits, awareness.
- [ ] [Goal 4 GRC layer](04-specialization.md): produce the NIST SP 800-30 risk register, 5 CSF Reference Tool mappings, and a control/evidence appendix from a blue/red/cloud lab.
- [ ] if cloud evidence exists, map 3 Prowler/ScoutSuite findings to CIS or NIST control IDs.

**measurable gate:** the risk register has at least 3 assets, 5 controls are mapped in the CSF Reference Tool, and the evidence appendix ties a lab finding to a control and remediation.

**can u explain it?** ✅ - unaided, compute ALE from AV/EF/ARO, then walk requirement -> control -> evidence -> finding -> remediation without hiding behind framework names.

**after these gates, optional checkpoints become realistic:**
- **Security+ SY0-701 Domain 5** and **SC-900** are the entry-friendly checkpoints.
- **CISA / CISM** are later-career. they require years of experience to hold, so dont build an entry study plan around them.

GRC is not "less technical."
it asks whether the technical control matches risk, whether evidence proves it works, and whether the business decision is defensible.

---

## practice-test sources that are current

dont use the old generic Professor Messer practice-exams page.
the July 2026 research pass caught it as a soft-dead page / wrong target.
Messer practice exams now live inside the per-course Success Bundles.

| Cert | default practice source | paid optional practice |
|---|---|---|
| **A+ Core 1 / Core 2** | [ExamCompass A+ current-code practice tests](https://www.examcompass.com/comptia/a-plus-certification/free-a-plus-practice-tests) - pick the **220-1201** and **220-1202** sets, not retired sets | Messer Success Bundles: [Core 1 220-1201](https://www.professormesser.com/220-1201-success-bundle/) + [Core 2 220-1202](https://www.professormesser.com/220-1202-success-bundle/) ($119 each); Dion Training packs: [Core 1 220-1201](https://www.diontraining.com/products/comptia-a-core-1-220-1201-practice-exam-1) + [Core 2 220-1202](https://www.diontraining.com/products/comptia-a-core-1-220-1202-practice-exam) |
| **Network+ N10-009** | [ExamCompass Network+ N10-009 practice tests](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests) - pick current-code N10-009 | [Messer N10-009 Success Bundle](https://www.professormesser.com/n10-009-success-bundle/) ($119); [Dion Training N10-009 Practice Exam Pack](https://www.diontraining.com/products/comptia-network-n10-009-practice-exam) |
| **Security+ SY0-701** | [ExamCompass Security+ SY0-701 practice tests](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) - pick current-code SY0-701 | [Messer SY0-701 Success Bundle](https://www.professormesser.com/sy0-701-success-bundle/) ($119); [Dion Training SY0-701 Practice Exam Pack](https://www.diontraining.com/products/comptia-security-sy0-007-unlimited-practice-exam) |
| **ISC2 CC** | [ISC2 Practice Quiz](https://cloud.connect.isc2.org/cc-quiz) + [ISC2 Flash Cards](https://cloud.connect.isc2.org/cc-flashcards) - official, likely email-gated | no Messer / ExamCompass / Dion pack verified for CC. use the guide's explain gates before paying |
| **CompTIA official option** | n/a | [CompTIA CertMaster Practice](https://www.comptia.org/en-us/resources/certmaster-training/practice/) - official adaptive practice, paid per cert |

practice-test rule:
dont book because u watched videos.
book when u are hitting **85%+ on fresh attempts** and can explain why the answer is right.

---

## whats dated in a 2021-era list

| old advice | July 2026 reality |
|---|---|
| A+ 220-1101 / 220-1102 | -> **220-1201 / 220-1202** |
| A+ ~$246/exam | -> ⚠️ **~$274/exam** (~$548 both cores) |
| Security+ SY0-601 | -> **SY0-701** |
| Security+ ~$593 | -> ⚠️ **~$439** |
| Network+ N10-008 | -> **N10-009** |
| CySA+ CS0-002 / "CS0-003 is current forever" | -> **CS0-004 (V4)** current; **CS0-003 retires 2026-12-22** |
| ISC2 CC as a bundled-voucher exam path for new learners | -> paid exam now: **~$199 + $50/yr AMF**; old 1MCC voucher path closed **2026-05-20** |
| BTL1 via Security Blue Team | -> **Centri**: <https://www.centri.org/certifications/blue-team-level-1> |
| eJPT v1 | -> **eJPT v2** |
| AZ-500 with no caveat | -> **retires August 31, 2026** |
| CASP+ | -> renamed / replaced by **SecurityX** branding |
| CEH as a differentiator | -> displaced by PNPT / CPTS / OSCP unless a job names CEH directly |
| Google cert missing | -> useful pre-Security+ on-ramp, but not a proctored security baseline |
| OSCP standalone voucher assumption | -> commonly sold through OffSec subscription-style training bundles |

---

## source notes

primary research files used for this rewrite:

- `research/_working/RC1-secfund-study-path.md` - merged CC + Security+ study order and practice sources.
- `research/_working/RC2-aplus-study-path.md` - A+ 220-1201/220-1202 topic map, practice gates, and current resources.
- `research/_working/RC3-networkplus-study-path.md` - Network+ N10-009 topic map, subnetting gates, and practice resources.
- `research/_working/RC4-practice-tests-logistics.md` - July 2026 logistics/practice-test fix list.
- `research/_working/R6-cert-ladder-domains.md` - cert domain -> topic map.
- `research/_working/R2-isc2-cc-domains.md` - CC outline, $199 exam fee, $50 AMF, 1MCC closure.
- `research/_working/RD1-blueteam-study-path.md` - SOC/blue-team optional checkpoints: CySA+ CS0-004, SC-200, BTL1.
- `research/_working/RD2-redteam-study-path.md` - red-team optional checkpoints: eJPT v2, HTB CPTS, PNPT.
- `research/_working/RD3-cloud-study-path.md` - cloud optional checkpoints: SC-900, SC-500, AWS SCS-C03, AZ-500 retirement.
- `research/_working/RD4-grc-study-path.md` - GRC framework/artifact path and experience-gated CISA/CISM framing.

official pages spot-checked:

- ISC2 CC and 1MCC closure: <https://www.isc2.org/certifications/cc> and <https://www.isc2.org/landing/1mcc>
- Microsoft SC-900 / SC-200 update notices and AZ-500 retirement: <https://learn.microsoft.com/en-us/credentials/certifications/exams/sc-900/>, <https://learn.microsoft.com/en-us/credentials/certifications/exams/sc-200/>, <https://learn.microsoft.com/en-us/credentials/certifications/exams/az-500/>
- Centri BTL1: <https://www.centri.org/certifications/blue-team-level-1>

dw, the point isnt "collect all badges."
the point is: know which topic group proves which skill, then pay only when the checkpoint is worth it.
