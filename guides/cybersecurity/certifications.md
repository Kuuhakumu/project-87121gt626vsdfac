# Certification Guide - Cybersecurity meow (July 2026)

> Verified via official sources + repo research, July 2026.
> prices are USD unless noted.
> **⚠️ price caveat:** CompTIA store prices are JS-gated / redirect-heavy, so the CompTIA prices below are current-best figures from the July 2026 research pass. confirm the checkout price at the official store before booking, oki.

Confidence: ✅ official/current page verified · ⚠️ price/store JS-gated or region-priced · ⛔ blocked / not worth using.

---

## TL;DR - what to actually get

study the **topic** first.
the cert is just the checkpoint after the mechanism clicks, not the thing that makes u good meow.

- **Fundamentals checkpoint:** ISC2 **CC** - optional paid exam, about **$199 + $50/yr AMF**. the 1MCC voucher program closed to new enrollments on **2026-05-20**.
- **The one that matters most for entry filters:** CompTIA **Security+ (SY0-701)** - about **$439 ⚠️**, and still the cleanest HR baseline.
- **Networking floor:** CompTIA **Network+ (N10-009)** if subnetting, ports, routing, and troubleshooting still feel shaky.
- **Support on-ramp only:** CompTIA **A+ (220-1201 / 220-1202)** if u have no IT background. skip the exam if real help-desk / IT experience already proves it.
- **Then specialize:** Blue / SOC, Red / Pentest, Cloud, or GRC. pick the lane from Goal 4, then choose the matching cert.
- **do not start AZ-500 now** unless an employer explicitly needs it before retirement. it retires **August 31, 2026**.
- **Skip for most people:** CEH, PenTest+, Cloud+, CASP+/SecurityX, CISA/CISM at entry. wrong tier, weak ROI, or experience-gated.

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
| BTL1 (Centri) | [Blue Team Level 1](https://www.centri.org/certifications/blue-team-level-1) | **£399** (~$505) | 24h practical, **70%** pass | lifetime | practical SOC proof; good "can u actually investigate?" checkpoint |
| INE eJPT | **eJPT v2** | ⚠️ ~$200 | practical, auto-graded | 3 yr | beginner red-team stepping stone |
| HTB CPTS | **CPTS** | ⚠️ ~$210 | practical engagement + report | no expiry | strong technical pentest signal; exact exam logistics JS-gated |
| TCM PNPT | **PNPT** | $499 | 5-day practical + report/debrief | lifetime | practical AD/pentest report signal |
| OffSec OSCP | **PEN-200 / OSCP** | ⚠️ ~$1,649 Learn One | 24h practical + report | no expiry | pentest baseline filter, later not entry |
| Cisco CCNA | **200-301** | ⚠️ ~$330 | MCQ+sim, 120m | 3 yr | stronger networking signal than Network+ if u go deep |
| GIAC GSEC | **GSEC** | ⚠️ ~$949 exam-only figure | CyberLive labs, 106q, 4h, **72%** | 4 yr | strong SANS brand; usually employer-sponsored |
| EC-Council CEH | **CEH v13** | ⚠️ ~$950-$1,999 | 125 MCQ, 4h | 3 yr | only if a specific job requires it |
| Google Cybersecurity Cert | Coursera cert | ⚠️ ~$49/mo (~$294 at 6 mo) | 8-course program, no proctored exam | n/a | pre-Security+ confidence builder, not a replacement |

---

## employer-signal ranking

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

| Cert checkpoint | do these topic groups, in order | u are ready when... |
|---|---|---|
| **A+ 220-1201 / 220-1202** | [Goal 1](01-foundations.md) Blocks 1-4: hardware -> OS -> networking/security intro -> practice sprint | Core 1 + Core 2 practice gates pass, and u can explain hardware/OS/network basics unaided |
| **Network+ N10-009** | Goal 1 Block 3 networking intro -> Goal 2 Block 1 networking floor -> Goal 2 Block 6 Network+ readiness sprint | subnetting `/26`-`/28` is automatic, troubleshooting tools make sense, and ExamCompass/Dion gates pass |
| **ISC2 CC** | Goal 2 Block 2 security foundations -> Block 3 crypto + identity + access control -> Block 5 operations + IR + GRC -> Block 6 CC readiness | all 5 CC domains are explainable; if testing on/after **2026-09-01**, re-check the ISC2 outline first |
| **Security+ SY0-701** | Goal 2 Block 1 networking floor -> Block 2 security foundations -> Block 3 crypto + identity + access control -> Block 4 attacks + CTF thread -> Block 5 operations + IR + GRC -> Block 6 Security+ readiness | 85%+ fresh SY0-701 practice gates pass and u can tell one full attack/detect/respond story |
| **CySA+ CS0-004** | Security+ readiness -> Goal 3 Blocks 3-5 KQL/SPL/regex + log parsing -> Goal 4 Blue / SOC lane | u can triage alerts, query logs, explain vuln management, and write the report/comms side |
| **BTL1 (Centri)** | Security+ readiness -> Goal 3 Blocks 3-6 log tooling + CTF reps -> Goal 4 Blue / SOC lane | u can complete blue-team cases, build timelines, and justify IR decisions under time pressure |
| **SC-200** | Security+ readiness -> Goal 3 Block 3 KQL -> Goal 4 Blue / SOC lane, Microsoft-flavored | Sentinel/Defender incident flow, hunting, KQL, and detection tuning feel normal |
| **eJPT v2** | Goal 2 Block 1 networking + Block 4 attacks -> Goal 3 Block 6 CTF level-up hub -> Goal 4 Red / pentest lane beginner boxes | u can enumerate services, get a shell legally, and explain what each step proved |
| **HTB CPTS / PNPT** | eJPT-level comfort -> Goal 4 Red / pentest lane full report path | u can chain recon -> exploit -> privesc -> AD/pivoting -> report without living in walkthroughs |
| **OSCP** | CPTS/PNPT-style report discipline -> more Red / pentest lane lab reps under time pressure | u can solve boxes consistently under time pressure and write clean evidence/remediation |
| **SC-900** | Goal 4 Cloud security lane intro -> GRC layer basics | Entra, Defender, Sentinel, Purview, compliance, and identity terms are clear |
| **Cloud security successor path** | Security+ -> SC-900 -> Goal 4 Cloud security lane | shared responsibility, IAM, CSPM, logging, and misconfig remediation are portfolio-visible |
| **GRC / compliance path** | Security+ Domain 5 -> Goal 4 GRC layer | u can produce a risk register, control crosswalk, and evidence appendix; CISA/CISM wait until experience |

---

## recommended paths

### universal beginner - cheapest security baseline

`CC/Security+ superset study` -> `CC exam only if u want the checkpoint (~$199 + $50 AMF)` -> `Google Cybersecurity Cert if u need a gentler ramp (~$294, optional)` -> `Security+ SY0-701 (~$439)`

**Total:** about **$439-$982** depending which optional checkpoints u pay for.
Security+ only is ~$439.
Security+ + Google is ~$733.
Security+ + paid CC first-year cost is ~$688.
all three is ~$982.

if u also sit **A+** and **Network+**, add about **$548** and **$399**.
dont pay those unless they solve a real on-ramp problem for u meow.

### blue team / SOC

`Security+ (~$439)` -> `BTL1 (~$505)` -> `SC-200 (~$165)` **or** `CySA+ CS0-004 (~$464)` -> later `GSEC` only if employer-sponsored

optional before Security+: `CC (~$199 + $50 AMF)` if u want the fundamentals checkpoint.

**Total:** about **$1,109-$1,408** without CC, or **$1,358-$1,657** with paid CC first-year cost.

### red team / pentest

`eJPT v2 (~$200)` -> `HTB CPTS (~$210)` **or** `PNPT ($499)` -> `Security+ (~$439, for HR)` -> `OSCP (~$1,649)` when lab-ready

**Total before OSCP:** about **$849-$1,138**.
**Total with OSCP later:** about **$2,498-$2,787**.

red usually isnt the first job.
thats not gatekeeping; its just how hiring works rn.
do SOC/IT/cloud/GRC as a bridge if u need one.

### cloud security

`SC-900 (~$99)` -> `Security+ (~$439)` -> `SC-200 (~$165)` -> current cloud-security successor path after AZ-500 retirement, or AWS Security Specialty if AWS is your lane

optional before Security+: `CC (~$199 + $50 AMF)`.

**Total before the role-specific cloud cert:** about **$703** without CC, or **$952** with paid CC first-year cost.

do **not** start AZ-500 now unless an employer explicitly requires it before **2026-08-31**.

### GRC / compliance

`Security+ (~$439)` -> `SC-900 (~$99)` -> Goal 4 **GRC layer** artifacts -> `CISA` / `CISM` only after the experience requirement is real

optional before Security+: `CC (~$199 + $50 AMF)`.

**Total for entry-friendly checkpoints:** about **$538** without CC, or **$787** with paid CC first-year cost.

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

- `research/_working/RC4-practice-tests-logistics.md` - July 2026 logistics/practice-test fix list.
- `research/_working/R6-cert-ladder-domains.md` - cert domain -> topic map.
- `research/_working/R2-isc2-cc-domains.md` - CC outline, $199 exam fee, $50 AMF, 1MCC closure.
- `research/_working/RC1-secfund-study-path.md` - merged CC + Security+ study order and practice sources.

official pages spot-checked:

- ISC2 CC and 1MCC closure: <https://www.isc2.org/certifications/cc> and <https://www.isc2.org/landing/1mcc>
- Microsoft SC-900 / SC-200 update notices and AZ-500 retirement: <https://learn.microsoft.com/en-us/credentials/certifications/exams/sc-900/>, <https://learn.microsoft.com/en-us/credentials/certifications/exams/sc-200/>, <https://learn.microsoft.com/en-us/credentials/certifications/exams/az-500/>
- Centri BTL1: <https://www.centri.org/certifications/blue-team-level-1>

dw, the point isnt "collect all badges."
the point is: know which topic group proves which skill, then pay only when the checkpoint is worth it.
