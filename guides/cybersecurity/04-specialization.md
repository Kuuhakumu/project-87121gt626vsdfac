# Goal 4: Specialization Paths meow (~160h)

> **goal:** pick one primary security lane, build the signature skill for that lane, and add the GRC layer that keeps the work tied to risk.
>
> **pace:** ~160 hours total ~= 11-12 weeks at 2h/day. this is **not** 160h per lane. do the chooser, pick one primary depth lane, then add the GRC layer beside it.
>
> **cert checkpoint:** certs sit on top of the topic. learn the craft first; the exam is the byproduct, not the reason.

[<- Goal 3: Scripting, Logs & CTF Level-Up](03-scripting-ctf.md) | [Back to hub](README.md) | [Next: Portfolio & Job Hunt ->](05-job-hunt.md)

---

## read this first meow

real talk: this is where people get tempted to study four careers at once.
dont do that qwq

blue, red, and cloud are the primary technical lanes.
GRC is a governance/risk layer that sits on top of all of them.

u can absolutely be **GRC-first** if writing, evidence, risk, and frameworks feel like your thing.
just dont think of it as "not technical."
good GRC translates technical reality into business decisions, and bad GRC is just paperwork cosplay.

the move here is:

- try a tiny sample of each lane
- pick the one whose boring parts u can stand
- go deep enough to build a portfolio artifact
- use the cert group as a checkpoint, not a silo

dw, u dont marry your first track meow.

---

## how to track your progress meow

the `- [ ]` boxes here are display-only in this public repo.
fork the repo, or copy this checklist into Obsidian/OneNote, if u want boxes u can actually tick.

the real progress signal is always:

1. **measurable gate** - a scored lab, rooted box, fixed cloud finding, mapped control set, or finished artifact.
2. **can u explain it?** - out loud or written, unaided, naming the mechanism.

both must pass before a topic is really done.
a checkbox alone doesnt mean anything meow

---

## the path (todo-tree)

- [ ] **Goal 4 - choose one specialization lane** (~160h total): pick one primary lane, build one signature project, and add the GRC layer.
  - [ ] **Chooser - run the good-Tuesday self-test** (~8h): spend one evening sampling each lane before committing.
  - [ ] **Pick ONE primary depth lane** (~120-140h): blue, red, or cloud. GRC-first is allowed if the layer is the work u want.
    - [ ] **CERT-D1 - Blue / SOC**: SIEM, detection engineering, ATT&CK, Sigma, triage, IR.
    - [ ] **CERT-D2 - Red / pentest**: recon, exploit, privesc, AD, pivoting, report.
    - [ ] **CERT-D3 - Cloud security**: shared responsibility, IAM, CSPM, misconfig remediation, cloud detection.
  - [ ] **Add CERT-D4 - GRC layer** (~25-40h): risk assessment, SLE/ALE, control crosswalks, audit evidence.
  - [ ] **exit check**: one signature artifact exists, the two gates pass, and u can explain why this lane fits your next job target.

---

## cert groups so u know what the topics cover

| Group | Lane | Certs / checkpoints layered on top | what the group proves |
|---|---|---|---|
| **CERT-D1** | Blue / SOC | BTL1 (Centri), CySA+ **CS0-004**, SC-200 | u can investigate alerts, query logs, map detections, and write IR notes |
| **CERT-D2** | Red / pentest | eJPT v2, HTB CPTS, PNPT; OSCP later | u can follow the attack chain and write the report |
| **CERT-D3** | Cloud security | SC-900 -> **SC-500**; AWS Security Specialty **SCS-C03** | u can secure customer-side cloud config and prove posture improved |
| **CERT-D4** | GRC layer | Security+ **SY0-701** Domain 5, SC-900 compliance; CISA/CISM later after experience | u can turn technical facts into risk, controls, evidence, and decisions |

heads up: **AZ-500 retires August 31, 2026**, so if youre starting Azure security now, use **SC-500** as the Microsoft cloud-security target.
for AWS, use **SCS-C03**. **SCS-C02 is retired**, and old SCS-C02 PDFs are stale.

---

## choosing your lane without getting lost meow

rule zero: u dont marry your first track.
these lanes overlap more than the internet admits.

a SOC analyst who writes Sigma is doing detection engineering.
a pentester who understands Active Directory teaches blue team what to detect.
cloud touches identity, logs, config, and incident response.
GRC needs someone who understands the technical work well enough to write real risk.

pick by which boring Tuesday sounds livable, not by which title sounds coolest hehe.

| if a good Tuesday is... | your lane | the honest day-job version |
|---|---|---|
| "i found the one alert in 4,000 that was real, and figured out the whole story from the logs." | **Blue / SOC** | most common entry door, but competitive. lots of alert triage; sometimes shift work. the fun part is investigation and building detections that catch the next one faster. |
| "i found the one misconfigured thing nobody thought about and chained it to Domain Admin." | **Red / pentest** | rarely hires true beginners. most people start in SOC/IT and pivot. the report is half the job, and the work is mostly being stuck until one small thing opens. |
| "i automated a check across 3,000 cloud resources and killed a whole class of misconfig at once." | **Cloud security** | strong remote odds and now baseline, not niche. best for people who like infrastructure, IAM, automation, and scale. |
| "i turned 'the DB is unpatched' into a risk the CFO actually funded, and proved a control works." | **GRC layer / GRC-first** | underrated and underserved. strong for writers/communicators. less hands-keyboard hacking, more evidence, control mapping, policy, and decision support. |

**honest tie-breakers**

- **fastest realistic first job:** SOC or GRC-first are the real entry doors. red is usually a second job, so plan a stepping-stone.
- **best remote odds:** cloud and GRC.
- **least "why am i competing with 500 people":** GRC is genuinely underserved; SOC is crowded.
- **if u like breaking more than defending but cant get red yet:** do SOC with detection-engineering + Active Directory focus. u learn attacks from the defender chair and can pivot later.
- **the overlap cheat:** logs/telemetry, attack chains, identity/config, and risk evidence show up everywhere. learn one deep; the other lanes become easier to read for free.

**the lost-track-of-time self-test**

before committing ~160h, spend one evening on each free featured lab:

- Blue: [CyberDefenders - DanaBot](https://cyberdefenders.org/blueteam-ctf-challenges/danabot/)
- Red: [Hack The Box - Starting Point Tier 0 intro](https://help.hackthebox.com/en/articles/6007919-introduction-to-starting-point)
- Cloud: [flaws.cloud](http://flaws.cloud/) (intentionally HTTP-only)
- GRC: [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) + one page of [NIST SP 800-30 Rev. 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final)-style risk rows

pick the one u lost track of time on.
that signal beats a personality quiz because depth beats breadth, and youll only go deep on the thing u dont have to force yourself to open.

---

## CERT-D1 - Blue / SOC meow (~120-140h if primary)

### SIEM detection and incident triage meow (~120-140h)

**the idea** - blue team work is turning messy telemetry into a defensible answer: "is this an attacker, what happened, and what do we do next?"

**cert group layered on top** - **CERT-D1** maps to BTL1, CySA+ **CS0-004**, and SC-200.
study the SOC craft once, then pick the cert that matches your target: BTL1 for practical proof, CySA+ for vendor-neutral/DoD-style SOC coverage, SC-200 for Microsoft Sentinel/Defender shops.

heads up: CySA+ owns more vulnerability management and reporting.
SC-200 is Microsoft-heavy: KQL, Sentinel, Defender XDR.
BTL1 is the hands-on pressure test.
same craft, different checkpoint.

**domain map** - this block covers the shared SOC core:

| cert | domains / modules this block serves |
|---|---|
| **CySA+ CS0-004** | Security Operations, Incident Response, Reporting; Vulnerability Management is a CySA+-heavy add-on after the SOC core |
| **SC-200** | Manage the security operations environment; respond to incidents; perform threat hunting with Sentinel/Defender |
| **BTL1** | SIEM, Incident Response, Threat Intelligence, Digital Forensics, Phishing Analysis |

**how/why it actually works** - a SIEM does not magically "know bad."
it runs a pipeline:

1. **collection** - agents, forwarders, and connectors send logs into one place: Windows Security Event Log, Sysmon, EDR, firewall logs, CloudTrail, Entra sign-ins.
2. **normalization / parsing** - raw events become structured fields like `src_ip`, `user`, `process`, `event_id`, and `host`, so one query can compare different log sources.
3. **indexing + storage** - events are stored by time and fields so u can search millions of rows fast.
4. **correlation** - a detection rule is a saved query. it matches thresholds, sequences, or joins: ">=5 failed logons from one `src_ip` in 5 minutes, then a success from the same source" = brute-force-then-success.
5. **enrichment** - the alert gets context: IP reputation, asset criticality, user role, known threat intel, and prior events.
6. **triage** - analyst pulls the raw events, builds a timeline, checks expected behavior, decides true positive vs false positive, and tunes the rule if it was noisy.

**Sigma** makes detection logic portable.
a Sigma rule is YAML: `logsource` says which log, `detection` says which field pattern, `condition` says how it matches, and `tags` map it to MITRE ATT&CK.
a converter turns that same logic into SPL, KQL, Elastic, or another SIEM query.

**MITRE ATT&CK** gives the shared language.
the tactic is the attacker goal, like Persistence or Lateral Movement.
the technique is the method, like `T1110` Brute Force or `T1059.001` PowerShell.
mapping detections to ATT&CK shows what u can see and what blind spots still exist.
thats why blue team is not just "watch alerts"; its building a visibility map meow.

**words u gotta be able to say**

- **SIEM** - log store plus correlation engine
- **normalization / parsing** - raw log into common fields
- **correlation rule** - query that fires an alert
- **true positive / false positive** - real attack vs benign match
- **alert fatigue** - too much noisy signal
- **IOC** - IP, domain, hash, artifact
- **enrichment** - context added to an alert
- **MITRE ATT&CK** - tactics and techniques with IDs
- **Sigma** - vendor-neutral detection YAML
- **SPL / KQL** - Splunk and Microsoft query languages
- **PICERL** - IR lifecycle: prep through lessons learned
- **order of volatility** - collect fragile evidence first

**study sources (pick what fits your style)**

- [LetsDefend - SOC Fundamentals](https://app.letsdefend.io/training/lessons/soc-fundamentals) - SOC roles, alert flow, EDR/SOAR/log-management basics before the harder labs. **free**
- [Wazuh Quickstart](https://documentation.wazuh.com/current/quickstart.html) - deploy a free SIEM/XDR spine for your home lab. **free**
- [SigmaHQ main rule repository](https://github.com/SigmaHQ/sigma) - read real portable detection rules and their ATT&CK tags. **free**
- [Uncoder.io](https://uncoder.io/) - convert Sigma logic into SPL/KQL-style SIEM queries. **freemium**
- [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) - map detections to tactics/techniques and see coverage gaps. **free**

**do this** - complete [CyberDefenders - DanaBot](https://cyberdefenders.org/blueteam-ctf-challenges/danabot/), a free blue-team PCAP/IOC investigation.
then author one Sigma rule for behavior u observed, convert it with Uncoder.io into SPL or KQL, and tag it with the right ATT&CK technique.

**measurable gate:** submit correct answers to **all DanaBot questions**, save the Sigma YAML, save the converted SPL/KQL, and include one paragraph explaining why the ATT&CK technique tag fits.

**CTF thread:** after DanaBot, do one bigger blue scenario like [CyberDefenders - Lockdown](https://cyberdefenders.org/blueteam-ctf-challenges/lockdown/) or one LetsDefend alert case.
write it as `alert -> evidence -> timeline -> verdict -> detection improvement`.

**can u explain it?** ✅ - unaided, walk one alert from raw log line -> normalized fields -> correlation condition -> fired alert -> enrichment -> triage verdict -> ATT&CK technique -> Sigma rule.
if u cant say why it is a true positive or false positive, the block isnt done yet qwq.

---

## CERT-D2 - Red / Pentest meow (~140-160h if primary)

### the attack chain and the report meow (~140-160h)

**the idea** - red team / pentest work is a legal, scoped simulation of an attacker: find the way in, prove impact, and write the fix clearly enough that defenders can act.

**cert group layered on top** - **CERT-D2** maps to eJPT v2, HTB CPTS, and PNPT.
eJPT proves the beginner methodology under low pressure.
CPTS goes broad and deep technically.
PNPT is Active Directory plus report plus live debrief.
OSCP is later, when this whole chain already feels normal.

heads up: the report is the real product.
eJPT is auto-graded and has no report.
CPTS grades a report.
PNPT makes u defend the report out loud.
thats not extra; thats the job.

**domain map** - this block covers the offensive superset:

| cert | domains / modules this block serves |
|---|---|
| **eJPT v2** | Assessment Methodologies, Host and Network Pentesting, Host and Networking Auditing, Web App Pentesting |
| **HTB CPTS** | Nmap/enumeration, common services, web attacks, AD enumeration/attacks, privesc, pivoting, reporting |
| **PNPT** | OSINT -> external -> internal AD -> Domain Controller compromise -> report -> live debrief |

**how/why it actually works** - the attack chain repeats until scope ends:

1. **recon / enumeration** - passive OSINT first, then active scanning. `nmap -sS` sends SYN probes; SYN-ACK means open, RST means closed. `-sV` grabs service/version banners. enumeration asks each service the next specific question: SMB shares, FTP anonymous login, HTTP directories, DNS records, SNMP strings.
2. **exploitation / initial access** - a found weakness becomes code execution or valid access. SQL injection abuses unsafe query construction; a vulnerable service may give RCE; stolen credentials may just log in. the result is usually a shell.
3. **shell choice** - a reverse shell dials back out to u, which often works through NAT/firewalls because outbound traffic is allowed. a bind shell listens on the target and needs inbound access.
4. **privilege escalation** - u make a higher-privileged process do something on your behalf: SUID/sudo misconfig on Linux, weak service permissions or token impersonation on Windows.
5. **lateral movement** - in enterprise, this usually means Active Directory. u use creds, hashes, tickets, or ACL paths to move from one host/account toward the Domain Controller.
6. **impact / exfil proof** - in a sanctioned test, u document access and impact without actually stealing data.
7. **report** - exec summary, scope, findings, evidence, CVSS/risk, remediation, and appendix. no clear report = no useful pentest.

Active Directory is where red work stops being "one box" and becomes "an environment."
**Kerberoasting** works because any authenticated domain user can request a service ticket (TGS) for an SPN-backed service account.
that ticket is encrypted with the service account password hash, so the attacker can take it offline and crack it without touching the domain again.
a long random service-account password kills the attack because offline cracking becomes impractical.

**BloodHound** turns AD into a graph.
users, groups, computers, sessions, and ACLs become nodes and edges.
then it computes paths like "this user can write to that group, that group can admin this host, that host has a Domain Admin session."
its not magic hacking; its graph math over permissions.
dw this clicks when u see one path light up meow.

**words u gotta be able to say**

- **scope / rules of engagement** - legal boundary of the test
- **recon / enumeration** - find and question attack surface
- **SYN scan** - infer ports from TCP replies
- **banner grab** - service and version clue
- **exploit / RCE** - bug to code execution
- **reverse shell / bind shell** - dial-out vs listen
- **privilege escalation** - low privilege to high privilege
- **Active Directory** - enterprise identity system
- **Kerberoasting / TGS** - crack service ticket offline
- **Pass-the-Hash** - authenticate with stolen hash
- **BloodHound** - graph paths through AD permissions
- **pivoting** - route through a foothold
- **report** - the actual deliverable

**study sources (pick what fits your style)**

- [Hack The Box - Introduction to Starting Point](https://help.hackthebox.com/en/articles/6007919-introduction-to-starting-point) - guided first boxes; Tier 0 teaches one service at a time. **freemium**
- [PortSwigger Web Security Academy - SQL injection](https://portswigger.net/web-security/sql-injection) - free web labs for SQLi mechanism and exploitation. **free**
- [PortSwigger Web Security Academy - Cross-site scripting](https://portswigger.net/web-security/cross-site-scripting) - reflected/stored/DOM XSS labs. **free**
- [PortSwigger Web Security Academy - Access control](https://portswigger.net/web-security/access-control) - IDOR and authorization-bypass practice. **free**
- [VulnHub - Kioptrix Level 1](https://www.vulnhub.com/entry/kioptrix-level-1-1,22/) - classic full recon -> exploit -> privesc beginner VM. **free**

**do this** - root HTB Starting Point **Meow**, **Fawn**, and **Dancing** unaided.
then root [Kioptrix Level 1](https://www.vulnhub.com/entry/kioptrix-level-1-1,22/) and write a short pentest report for it.

**measurable gate:** all three HTB Starting Point Tier 0 boxes are completed without a walkthrough, Kioptrix Level 1 reaches root, and the report contains scope, commands/evidence, finding, impact, and remediation.

**CTF thread:** solve every PortSwigger **Apprentice** lab in SQLi, XSS, and access control before u call web "covered."
keep one writeup per category with "what broke" and "how a defender would detect/prevent it."

**can u explain it?** ✅ - given an `nmap -sV` output, name the next enumeration step for each open port.
then explain why a reverse shell beats a bind shell through NAT, and explain Kerberoasting: which ticket, why it cracks offline, and what BloodHound adds after u get a foothold.

---

## CERT-D3 - Cloud Security meow (~120-140h if primary)

### shared responsibility and CSPM meow (~120-140h)

**the idea** - cloud security is mostly securing the customer's half of the cloud: identity, data, network exposure, logging, and configuration at scale.

**cert group layered on top** - **CERT-D3** maps to SC-900 -> **SC-500** for Microsoft cloud security, and AWS Security Specialty **SCS-C03** for AWS.
SC-900 is fundamentals.
SC-500 is the Azure/AI cloud-security successor path.
SCS-C03 is the current AWS Security Specialty.

do **not** start AZ-500 now unless an employer explicitly requires it before retirement.
it retires **August 31, 2026**.
do **not** study from SCS-C02 exam guides; SCS-C02 is retired, and **SCS-C03** is current.

**domain map** - this block covers cloud-security fundamentals plus implementer-level posture work:

| cert | domains / modules this block serves |
|---|---|
| **SC-900** | Microsoft security/compliance/identity fundamentals: Entra, Defender, Sentinel, Purview concepts |
| **SC-500** | identity/access/governance; secure storage/databases/networking; secure compute incl. AI; manage and monitor posture |
| **AWS SCS-C03** | Detection, Incident Response, Infrastructure Security, IAM, Data Protection, Security Foundations and Governance |

**how/why it actually works** - the first mechanism is **shared responsibility**.
the provider secures **of the cloud**: data centers, hardware, hypervisor, managed-service backplane.
the customer secures **in the cloud**: data, IAM, network rules, resource config, app config, secrets, and sometimes OS patching.

the line moves by service model:

- **IaaS** - u own more: OS, patches, security groups, IAM, data.
- **PaaS** - provider owns runtime more, u still own identity, data, network exposure, app settings.
- **SaaS** - provider owns the stack, u still own users, data classification, access policy, retention, and audit.

the second mechanism is **CSPM**: cloud security posture management.
because cloud risk is usually misconfiguration at huge scale, u cant eyeball the console.
a CSPM loop does this:

1. authenticate with read-only credentials.
2. enumerate resources through provider APIs: buckets, roles, policies, security groups, DBs, logs.
3. evaluate each resource against a benchmark or policy: CIS, provider best practice, internal standard.
4. produce findings with severity, affected resource, evidence, and remediation.
5. triage by real risk: public + sensitive + reachable beats noisy low-impact findings.
6. remediate, then re-scan to prove the finding is gone.

thats the whole day-job loop: **scan -> triage -> fix -> re-scan**.
shift-left is the same loop before deploy, scanning Terraform/CloudFormation so the bad config never lands.

**words u gotta be able to say**

- **shared responsibility** - provider of cloud, customer in cloud
- **IaaS / PaaS / SaaS** - service models moving the line
- **misconfiguration** - wrong setting exposed at scale
- **IAM / least privilege** - identity is the perimeter
- **role / user / STS** - temporary role assumption pattern
- **security group** - virtual firewall rule set
- **public bucket / blob** - exposed object storage
- **CSPM** - continuous config posture scanning
- **finding** - detected config risk
- **secure score** - posture score / trend
- **CloudTrail / Activity Log** - who-did-what audit logs
- **IaC scanning** - catch config before deploy

**study sources (pick what fits your style)**

- [flaws.cloud](http://flaws.cloud/) - classic free AWS S3/IAM misconfiguration lab; intentionally HTTP-only. **free**
- [ScoutSuite](https://github.com/nccgroup/ScoutSuite) - open-source multi-cloud posture audit reports. **free**
- [Prowler](https://github.com/prowler-cloud/prowler) - open-source AWS/Azure/GCP security benchmark scanner. **free**
- [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) - vulnerable-by-design AWS scenarios in your own account. **free tool, cloud usage may cost**
- [Microsoft SC-500 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500) - official current Microsoft cloud/AI security objectives. **free**

**do this** - clear [flaws.cloud](http://flaws.cloud/) through at least **level 3** unaided.
then run ScoutSuite or Prowler against a cloud account u own, remediate one real finding, and re-scan to prove it is gone.

**measurable gate:** flaws.cloud levels 1-3 are complete, the posture scan report is saved, one finding is remediated, and the before/after evidence shows the scanner no longer reports that finding.

**CTF thread:** if u want the attack-side version, deploy one [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) scenario in an account u control, complete it, then write the defensive fix.
delete resources after the lab so u dont pay for ghosts.

**can u explain it?** ✅ - draw the shared-responsibility line for IaaS vs SaaS.
then explain a public-S3 exposure: what setting exposed it, why IAM/resource policy allowed access, what exact setting fixed it, and what a CSPM tool read to catch it.

---

## CERT-D4 - GRC Layer meow (~25-40h beside any lane, ~100h if GRC-first)

### risk, SLE/ALE, and control crosswalks meow (~25-40h)

**the idea** - GRC is the layer that asks: are we doing the right controls, can we prove they work, and does the cost match the risk?

**cert group layered on top** - **CERT-D4** maps to Security+ **SY0-701** Domain 5 and SC-900 compliance.
CISA/CISM are later-career signals because they require years of experience to hold.
dont try to shortcut that with study time.
for entry, the signal is framework fluency plus clean risk/evidence artifacts.

GRC is a **layer**, not a box off to the side.
blue uses it when an incident becomes a risk and a control improvement.
red uses it when a finding becomes a business-prioritized remediation.
cloud uses it when a CSPM finding maps to CIS/NIST/ISO evidence.

**domain map** - this block covers the governance layer that certs mostly test as program management:

| cert | domains / modules this block serves |
|---|---|
| **Security+ SY0-701** | Domain 5.0 Security Program Management and Oversight |
| **SC-900** | compliance, privacy, risk, Microsoft Purview, and security/compliance concepts |
| **CISA/CISM later** | the same audit/management topics, but experience-gated; not an entry checkpoint |

**how/why it actually works** - the first mechanism is risk assessment.
risk is **likelihood * impact** on an asset.
the workflow is:

1. scope the system and risk tolerance.
2. identify assets, threats, vulnerabilities, and possible events.
3. score likelihood and impact.
4. record the result in a risk register.
5. choose a treatment: avoid, mitigate, transfer, or accept.
6. note residual risk, owner, due date, and review date.

qualitative risk uses Low/Medium/High and heat maps.
quantitative risk uses dollars:

- **SLE = Asset Value * Exposure Factor**
- **ALE = SLE * ARO**

if a server is worth `$100,000`, one incident damages 30%, and it happens about once every 5 years, then:
SLE = `$100,000 * 0.30 = $30,000`.
ARO = `0.2`.
ALE = `$30,000 * 0.2 = $6,000/year`.

that does not make the decision for u, but it gives the business a number to compare against the control cost.

the second mechanism is control crosswalking.
a **framework** organizes outcomes, like NIST CSF 2.0: GOVERN, IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER.
a **control catalog** supplies safeguards, like NIST SP 800-53 or CIS Controls.
an **ISMS standard** like ISO 27001 wraps management process around the controls.

control mapping asks: "this MFA control satisfies which CSF subcategory, which 800-53 control, which CIS safeguard, and which ISO Annex A control?"
then evidence proves it is operating: screenshots, policy docs, logs, tickets, scan output, or audit samples.
the gap between "control required" and "control evidenced" becomes a finding.
thats GRC in one sentence: **requirement -> control -> evidence -> finding -> remediation**.

**words u gotta be able to say**

- **risk** - likelihood times impact
- **asset / threat / vulnerability** - value, danger, weakness
- **SLE / ALE / ARO** - single-loss and annualized-loss math
- **risk appetite / tolerance** - how much risk is acceptable
- **residual risk** - risk left after controls
- **avoid / mitigate / transfer / accept** - four risk responses
- **risk register** - owned list of ranked risks
- **framework** - organizes security outcomes
- **control catalog** - supplies specific safeguards
- **ISMS** - management system for security
- **crosswalk** - map one control across frameworks
- **evidence** - proof a control operates
- **finding** - control gap requiring remediation

**study sources (pick what fits your style)**

- [NIST SP 800-30 Rev. 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) - official risk-assessment method. **free**
- [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) - official crosswalk/filter tool for CSF subcategories and references. **free**
- [NIST CSF 2.0 Quick Start Guides](https://www.nist.gov/cyberframework/quick-start-guides) - short on-ramp before the full framework. **free**
- [CIS Controls list](https://www.cisecurity.org/controls/cis-controls-list) - open list of the 18 CIS Controls. **free**
- [Prabh Nair - GRC Practical Approach Part 1](https://www.youtube.com/watch?v=mq_vSLHm4r0) - practical GRC analyst day-job framing. **free**

**do this** - produce a mock NIST SP 800-30 risk assessment for **at least 3 assets**.
each row needs asset, threat event, vulnerability, likelihood, impact, treatment, residual risk, owner, and review date.
then use the [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) to map **5 controls** to their CSF 2.0 Function + Category.

**measurable gate:** the risk register has >=3 complete assets, at least one row includes an SLE/ALE calculation, and 5 controls are correctly mapped through the CSF Reference Tool.
if u also ran Prowler or ScoutSuite in the cloud block, map 3 failed findings to CIS or NIST control IDs as the evidence layer.

**CTF / artifact thread:** for any blue/red/cloud lab above, add a tiny GRC appendix:
"what risk did this expose, which control would reduce it, what evidence proves the fix worked?"
this is how u turn lab work into business-readable work.

**can u explain it?** ✅ - compute ALE from AV/EF/ARO without notes.
then explain the difference between a framework, a control catalog, and an ISMS, and walk one control from requirement -> mapped control -> evidence -> finding -> remediation.

---

## exit check - done with Goal 4

- [ ] u picked one primary lane using the good-Tuesday test, not vibes.
- [ ] u completed the primary lane's measurable gate:
  - [ ] Blue: DanaBot all answers + Sigma rule + ATT&CK tag + SPL/KQL conversion.
  - [ ] Red: HTB Starting Point Meow/Fawn/Dancing + Kioptrix Level 1 + report.
  - [ ] Cloud: flaws.cloud level 1-3 + CSPM scan + one remediated finding + re-scan.
  - [ ] GRC-first: SP 800-30 risk register + 5 CSF Reference Tool mappings.
- [ ] u added the CERT-D4 layer to your primary lane: risk, control, evidence, remediation.
- [ ] u can explain the mechanism of your lane unaided, not just list tools.
- [ ] u have one portfolio-ready artifact for Goal 5:
  - [ ] Blue: alert timeline + Sigma/KQL/SPL detection writeup.
  - [ ] Red: pentest report with evidence and remediation.
  - [ ] Cloud: before/after CSPM remediation report.
  - [ ] GRC: risk assessment + control crosswalk + evidence appendix.

**final can u explain it?** - unaided, tell this story:

> "i chose this lane because the day-job loop fits me. here is the mechanism: raw signal or finding -> analysis -> decision -> artifact -> remediation. here is the cert group it maps to, here is the lab i passed, and here is the evidence that proves i understand why it works."

if u can do that, ur ready for [Portfolio & Job Hunt](05-job-hunt.md).
if not, the part u stumble on tells u exactly which block to redo.
dw, thats the point meow

---

[<- Goal 3: Scripting, Logs & CTF Level-Up](03-scripting-ctf.md) | [Back to hub](README.md) | [Next: Portfolio & Job Hunt ->](05-job-hunt.md)
