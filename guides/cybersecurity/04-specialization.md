# Phase 4: Specialization Paths

> **~160 hrs total** · your pace, no deadline
> Pick **ONE** path. Don't spread thin across all four — depth beats breadth for landing a first job.

[← Phase 3: Scripting](03-scripting-ctf.md) · [Hub](README.md) · [Phase 5: Job Hunt →](05-job-hunt.md)

---

## Choosing your path

| Path | Best if you like… | Entry roles | Remote-friendly |
|---|---|---|---|
| 🔵 **Blue Team / SOC** | Investigating, defending, log analysis | SOC Analyst I, Security Analyst | Mixed |
| 🔴 **Red Team / Offensive** | Breaking things, creative problem-solving | Junior Pentester, Security Consultant | Hybrid-heavy |
| ☁️ **Cloud Security** | Automation, infrastructure, scale | Cloud Security Analyst/Engineer | High |
| ⚖️ **GRC / Compliance** | Policy, risk, communication, frameworks | GRC Analyst, Compliance Analyst | High |

> **Market reality (2026):** SOC is the most common entry door but competitive. GRC is *underserved* — NIS2/DORA created demand the cert crowd tends to underrate. Cloud has the highest remote ceiling. Red team rarely hires true beginners — expect a stepping stone first.

---

## 🔵 Path A: Blue Team / SOC Analyst

The default entry path. You triage alerts, investigate incidents, hunt threats.

### Recommended cert
**BTL1** (Centri, ~£399/~$505) — 24-hour practical, hands-on, lifetime validity. Rapidly growing recognition; technical hiring managers trust the practical format. **Alternative:** CySA+ (**CS0-004** current; CS0-003 retires 2026-12-22, ~$464) if targeting DoD/government.

### What to cover
- **SIEM:** Splunk (SPL) + Microsoft Sentinel (KQL) — both appear constantly in postings
- **Phishing analysis:** email headers, attachment detonation, URL reputation
- **DFIR:** disk (Autopsy), memory (Volatility), Windows artifacts
- **Threat intel:** MITRE ATT&CK v19.1 mapping, IOC enrichment
- **Detection:** read Sigma rules, map to ATT&CK techniques
- **IR lifecycle:** PICERL (Preparation → Identification → Containment → Eradication → Recovery → Lessons Learned)

### Interactive labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| SOC Analyst path | [LetsDefend](https://app.letsdefend.io/) | Work a real SOC alert queue: triage, escalate, close | Freemium |
| Blue team labs | [CyberDefenders](https://cyberdefenders.org/) | 100+ DFIR scenarios: memory, disk, PCAP | Free |
| DFIR investigations | [Blue Team Labs Online](https://blueteamlabs.online/) | Scored forensic scenarios (Autopsy, Volatility) | Freemium |
| Splunk Fundamentals 1 | [Splunk](https://www.splunk.com/en_us/training/free-courses/overview.html) | Ingest data, write SPL, build dashboards | Free |
| KC7 | [kc7cyber.com](https://kc7cyber.com/) | KQL investigations across email/DNS/auth/endpoint logs | Free |
| Wazuh room | TryHackMe | Query alerts, tune rules on a live Wazuh instance | Free tier |

### Home lab
Deploy **Wazuh** (free, open-source SIEM/XDR, v4.9.2). Connect a Windows + Linux agent. Generate alerts, investigate them. This is your best free hands-on SOC environment and a portfolio centerpiece.

---

## 🔴 Path B: Red Team / Offensive Security

You simulate attacks to find weaknesses. Rarely hires true beginners — most start in SOC/IT then pivot.

### Recommended cert ladder
1. **eJPT** (INE, ~$200) — learn methodology, low stakes
2. **PNPT** (TCM, $499, free retake) — practical pentest + report writing, highly respected
   - *or* **HTB CPTS** (~$210) — more technical depth
3. **OSCP** (OffSec, ~$1,649) — the gold-standard target, when labs feel comfortable

> Skip **CEH** unless a specific job posting demands it. Skip **PenTest+** — PNPT/CPTS/OSCP beat it in every practical comparison.

### What to cover
- Recon & OSINT, Nmap enumeration
- Service enumeration (SMB, FTP, HTTP, RDP)
- Exploitation (Metasploit + manual), credential attacks (Hydra)
- Privilege escalation (Linux & Windows)
- Web attacks (SQLi, XSS, SSRF, IDOR)
- Network pivoting
- **Report writing** — the actual deliverable of a pentest

### Interactive labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Web Security Academy | [PortSwigger](https://portswigger.net/web-security) | 250+ labs: SQLi, XSS, SSRF, IDOR, XXE | Free |
| Starting Point | [Hack The Box](https://www.hackthebox.com/) | Guided beginner machines | Freemium |
| Penetration Tester path | HTB Academy | Recon → exploit → report on live targets | Freemium |
| Privilege escalation dojo | [pwn.college](https://pwn.college/) | University-grade priv-esc challenges | Free |
| Linux/Windows PrivEsc | TryHackMe | SUID, sudo, kernel, service misconfigs | Free tier |

---

## ☁️ Path C: Cloud Security

Cloud security is now **baseline**, not niche. Highest remote ceiling at entry level.

### Recommended cert
**SC-900** (~$165, never expires) → **SC-200** (Sentinel/Defender SOC focus; **2026-07-28 refresh** adds Security Copilot/Sentinel Data lake). 
> ⛔ **Do NOT pursue AZ-500 — it retires August 31, 2026.** Wait for the announced successor, or pursue AWS Security paths if you're in an AWS shop.

### What to cover
- Shared responsibility model (provider vs customer)
- IAM fundamentals: least privilege, roles vs users, service accounts, over-privileged identities
- Cloud logging: CloudTrail (AWS), Activity Log (Azure), Cloud Audit Logs (GCP)
- Common misconfigs: public S3 buckets, open security groups, exposed blobs
- Cloud alert triage (GuardDuty, Defender for Cloud findings)

### Interactive labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Azure Fundamentals (AZ-900 path) | [Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/) | Cloud concepts + security with sandbox exercises | Free |
| Sentinel investigation | [Microsoft Learn](https://learn.microsoft.com/en-us/azure/sentinel/investigate-cases) | Deploy Sentinel, ingest logs, run KQL | Free (Azure trial) |
| CloudGoat | [Rhino Security Labs](https://github.com/RhinoSecurityLabs/cloudgoat) | Deliberately vulnerable AWS — attack & defend | Free |
| flaws.cloud | [flaws.cloud](http://flaws.cloud/) | Walk through real AWS misconfigurations | Free |

---

## ⚖️ Path D: GRC / Governance, Risk & Compliance

Underrated entry path. Strong for communicators. Highly remote-friendly. EU demand rising from NIS2/DORA.

### What to cover
- **Frameworks:** NIST CSF 2.0 (all 6 functions incl. **Govern**), ISO/IEC 27001:2022, SOC 2
- **Regulations:** GDPR, NIS2 (EU), DORA (EU financial), PCI-DSS
- **Risk methodology:** qualitative vs quantitative, NIST SP 800-30
- **Business alignment:** translating technical risk into business/financial impact

### Recommended certs
Security+ (baseline) + SC-900 (compliance module). 
> CISA/CISM are valuable but gate on **5 years experience** — they're later-career, not entry.

### Interactive labs / projects

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Prowler vs AWS Free Tier | [Open source](https://github.com/prowler-cloud/prowler) | Automated compliance audit of your own cloud account | Free |
| ScoutSuite | [Open source](https://github.com/nccgroup/ScoutSuite) | Multi-cloud security audit + remediation report | Free |

### Project
Write a **mock NIST SP 800-30 risk assessment** for a fictional company, with a GDPR/NIS2 gap analysis. This demonstrates the core GRC deliverable.

---

## Phase 4 exit checklist
- [ ] Chosen ONE path and completed its cert (or scheduled the exam)
- [ ] Built the path's signature project (Wazuh lab / pentest writeup / cloud audit / risk assessment)
- [ ] Comfortable with the path's core tools
- [ ] 3–5 portfolio-ready projects on GitHub

Next: [Phase 5 — Portfolio & Job Hunt →](05-job-hunt.md)
