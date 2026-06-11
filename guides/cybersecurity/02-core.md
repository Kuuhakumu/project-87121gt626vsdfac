# Phase 2: Networking & Security Core

> **~180 hrs total** · your pace, no deadline
> Certs targeted: **CompTIA Network+ (N10-009)** → **ISC2 CC (free)** → **CompTIA Security+ (SY0-701)**

[← Phase 1: Foundations](01-foundations.md) · [Hub](README.md) · [Phase 3: Scripting & CTF →](03-scripting-ctf.md)

---

This is the most important phase for employability. **Security+ is the #1 baseline filter** in entry-level security job postings. Network+ makes Security+ a lot easier, and ISC2 CC is free, DoD-approved, and builds exam confidence at zero cost. See [certifications.md](certifications.md) for full exam data and ROI tiers.

---

## CompTIA Network+ (N10-009) (~80 hrs)

> **Optional but recommended** — skip only if you already have strong networking fundamentals (CCNA-level). If you skip, still master subnetting and the OSI model cold.

### Exam at a glance
- **Code:** N10-009 · **Price:** ~$399 · **Pass:** 720/900 · **Time:** 90 min · ≤90 questions (MCQ + PBQ)
- **Validity:** 3 years

### Domain weights — study proportionally

| Domain | Weight |
|---|---|
| 1.0 Networking Concepts | 23% |
| 2.0 Network Implementation | 20% |
| 3.0 Network Operations | 19% |
| 4.0 Network Security | 14% |
| 5.0 Network Troubleshooting | **24%** |

> Troubleshooting is the biggest domain. Master the CompTIA 7-step methodology cold.

### What to cover
- **Concepts:** OSI deep-dive, TCP vs UDP, IPv4/IPv6, DNS/DHCP/NTP internals, ports/protocols, cloud models (SaaS/IaaS/PaaS), SDN, VPCs
- **Implementation:** cabling (Cat5e/6/6a, fiber), Wi-Fi 6/6E (802.11ax), WPA3, RADIUS, routing (OSPF/BGP basics), switching (VLANs, STP), NAT/PAT, **subnetting mastery**
- **Operations:** SNMP, syslog, NetFlow, documentation, SLAs, monitoring
- **Security:** zero trust, SASE, IDS/IPS concepts, network hardening, segmentation
- **Troubleshooting:** the 7-step method, CLI tools (`ping`, `tracert`, `nslookup`, `dig`, `ipconfig`/`ip`, `netstat`, `nmap`)

> [!NOTE]
> **2026 reality (from research):** teach IDS/IPS as *concepts*, not Snort/Suricata rule syntax. Detection now lives in EDR/SIEM. Know what an IDS does and where it sits; don't memorize rule grammar.

### YouTube theory
Professor Messer N10-009 (free, full playlist) · PowerCert Animated Videos · Sunny Classroom · NetworkChuck

### Interactive labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Intro to Networking series | TryHackMe | OSI, ping, traceroute in browser | Free tier |
| Introduction to Networking | HTB Academy | OSI/TCP-IP, subnetting, DNS, ARP — interactive Qs | Free module |
| [SubnettingPractice.com](https://subnettingpractice.com/) | Web | `/24`–`/30` drills until automatic | Free |
| Wireshark: The Basics | TryHackMe | Filter live PCAPs, identify protocols | Free tier |
| Packet Analysis | HTB Academy | Analyze captures for lateral movement / C2 | Free module |

### Practice gate
**85%+ on 2 fresh full-length practice exams** (Jason Dion / Professor Messer) before booking.

---

## ISC2 Certified in Cybersecurity (CC) — FREE (~30 hrs)

> **Do this before Security+.** It's free, DoD 8140-approved, and a good way to build CAT exam confidence.

> [!IMPORTANT]
> ISC2 CC exam is **free** (exam + first-year membership) under the One Million Certified initiative. **A new exam outline takes effect Sept 1, 2026** — if you test after that date, use post-Sept study material.

### Exam at a glance
- **Format:** 100 MCQ, 120 min, linear (not CAT for CC) · **Pass:** 700/1000 · **Price:** Free
- **Maintenance:** ~$50/yr AMF + 45 CPEs over 3 years

### Domain weights

| Domain | Weight |
|---|---|
| 1. Security Principles | **26%** |
| 2. BC/DR & Incident Response | 10% |
| 3. Access Controls | **22%** |
| 4. Network Security | **24%** |
| 5. Security Operations | 18% |

### What to cover
CIA triad, risk management, governance, physical/logical access controls, authentication/authorization (AAA), firewalls, VPNs, OSI basics, BCP/DRP, incident response lifecycle, patch & configuration management.

### Resources
- **[Official ISC2 free online training](https://www.isc2.org/certifications/cc)** (free self-paced course + exam voucher)
- Prabh Nair (YouTube) for scenario walkthroughs
- Free lab: [Intro to Cryptography](https://tryhackme.com/) (TryHackMe) — hashing, encryption, digital signatures

### Exam strategy
Watch for "BEST," "MOST," "FIRST" wording. The exam tests scenario *application*, not memorization.

---

## CompTIA Security+ (SY0-701) — THE BASELINE (~70 hrs)

> This is the single most useful cert for landing your first job.

### Exam at a glance
- **Code:** SY0-701 · **Price:** ~$593 · **Pass:** 750/900 · **Time:** 90 min · ≤90 questions (MCQ + PBQ)
- **Validity:** 3 years · **DoD 8140/8570 baseline approved**

> [!NOTE]
> No successor (SY0-801) announced as of June 2026. SY0-701 is current. Verify before booking.

### Domain weights

| Domain | Weight |
|---|---|
| 1.0 General Security Concepts | 12% |
| 2.0 Threats, Vulnerabilities & Mitigations | **22%** |
| 3.0 Security Architecture | 18% |
| 4.0 Security Operations | **28%** |
| 5.0 Security Program Management & Oversight | 20% |

> Domain 4 (Security Operations) is the heaviest — incident response, monitoring, logging. Spend the most time here.

### What to cover
- **Concepts:** CIA + non-repudiation, zero trust, security controls (technical/managerial/operational/physical), change management, cryptography (PKI, symmetric/asymmetric, hashing, digital signatures)
- **Threats:** threat actors, attack vectors, social engineering, malware types, vulnerability types (race conditions, memory injection, supply chain)
- **Architecture:** secure network design, cloud security (**shared responsibility model**), zero trust architecture, resilience, data protection
- **Operations:** SIEM, monitoring, hardening, identity & access management, automation/orchestration, **incident response (PICERL)**, digital forensics, vuln management
- **Program management:** governance, risk management, third-party risk, compliance (GDPR, NIST CSF 2.0, ISO 27001:2022), audits, security awareness

> [!NOTE]
> **2026 updates to weave in (from research):** teach the **hybrid Entra ID + on-prem AD** reality (not pure on-prem), **behavioral detection over signature/hash**, and **cloud security as baseline**. Reference **NIST CSF 2.0** (now 6 functions — Govern is the new one) and **OWASP Top 10 2025**.

### YouTube theory
Professor Messer SY0-701 (free, complete) — download the [official CompTIA SY0-701 objectives PDF](https://www.comptia.org/) and use it as a checklist.

### Interactive labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Splunk Fundamentals 1 | [Splunk Education](https://www.splunk.com/en_us/training/free-courses/overview.html) | Ingest data, write SPL, build dashboards | Free |
| Kusto Detective Agency | [detective.kusto.io](https://detective.kusto.io/) | Solve cases with KQL queries | Free |
| KC7 | [kc7cyber.com](https://kc7cyber.com/) | Investigate attacks across email/DNS/auth logs (KQL) | Free |
| SOC Analyst alerts | [LetsDefend](https://app.letsdefend.io/) | Triage malware & phishing alerts on a SOC queue | Free tier |
| Web Security Academy | [PortSwigger](https://portswigger.net/web-security) | Exploit SQLi/XSS/SSRF to understand mitigations | Free |
| Cryptography | HTB Academy | Encode/decode, break weak ciphers, PKI | Free module |

### Practice gate
- **85%+ on 3 fresh Professor Messer practice exams**, OR
- **80%+ on 2 fresh Jason Dion practice tests**

### Exam strategy
Use the objectives PDF as a strict checklist. Read questions twice — catch "LEAST/BEST/FIRST." Flag PBQs, do all MCQ first, return to PBQs.

---

## Phase 2 exit checklist
- [ ] (Optional) Network+ passed, or subnetting + OSI mastered
- [ ] ISC2 CC passed (free)
- [ ] Security+ passed — **the key milestone**
- [ ] Comfortable running SPL (Splunk) and KQL (Sentinel/KC7) basic queries
- [ ] Can explain shared responsibility model, PICERL, CIA triad, PKI

Next: [Phase 3 — Scripting, Databases & CTFs →](03-scripting-ctf.md)
