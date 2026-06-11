# 🧪 Interactive Lab Inventory — Cybersecurity (2026)

> Every platform below was URL-checked June 2026. Status: ✅ live & confirmed · ⚠️ live but rate-limits/blocks automated checks (use in a browser) · ❌ dead/moved.
>
> **Rule of this guide:** never "open a VM and look around." Every topic points to a *named* lab that guides and verifies you.

---

## Platform quick-reference

| Platform | Best for | Cost | Status |
|---|---|---|---|
| [PortSwigger Web Security Academy](https://portswigger.net/web-security) | Web app security (250+ labs, Burp) | **100% free** | ✅ |
| [HTB Academy](https://academy.hackthebox.com/) | Structured modules, live targets, offensive+defensive | Freemium (many free) | ✅ |
| [CyberDefenders](https://cyberdefenders.org/) | DFIR, PCAP/memory forensics, BOTS | Mostly free | ✅ |
| [LetsDefend](https://app.letsdefend.io/) | SOC alert-queue simulation, triage | Freemium | ✅ |
| [picoCTF](https://picoctf.org/) | Beginner CTF, all domains, 400+ challenges | **Free** | ✅ |
| [OverTheWire (Bandit)](https://overthewire.org/wargames/bandit/) | Linux CLI via wargame | **Free** | ✅ |
| [KC7](https://kc7cyber.com/) | KQL log analysis, detection, SOC | **Free** | ✅ |
| [Kusto Detective Agency](https://detective.kusto.io/) | KQL practice, Sentinel prep | **Free** | ✅ |
| [pwn.college](https://pwn.college/) | Binary exploitation, OS internals, privesc (ASU) | **Free** | ✅ |
| [Blue Team Labs Online](https://blueteamlabs.online/) | DFIR, phishing, SOC scenarios | Freemium | ✅ |
| [Microsoft Learn](https://learn.microsoft.com/training/) | Azure/Sentinel/KQL, SC-200 prep | **Free** | ✅ |
| [Splunk Free Training](https://www.splunk.com/en_us/training/free-courses/overview.html) | Splunk/SPL fundamentals | **Free** | ✅ |
| [TryHackMe](https://tryhackme.com/) | Guided beginner paths, SOC/blue team | Freemium (~$14/mo) | ⚠️ |
| [Wazuh](https://wazuh.com/) | Open-source SIEM/XDR home lab (v4.9.2) | **Free** | ✅ |
| [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) | GCP security, IAM | Freemium | ⚠️ |

---

## Labs by topic

### Linux & Windows fundamentals
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Bandit (levels 0–34)](https://overthewire.org/wargames/bandit/) | OverTheWire | SSH into real boxes; files, permissions, bash, pipes | Free |
| Linux Fundamentals module | [HTB Academy](https://academy.hackthebox.com/) | Guided bash, permissions, package mgmt | Free |
| [Linux Fundamentals 1–3](https://tryhackme.com/room/linuxfundamentalspart1) | TryHackMe | Browser Linux VM: filesystem, cron, SSH | Free |
| Windows Fundamentals module | [HTB Academy](https://academy.hackthebox.com/) | Windows CLI/PowerShell against live VMs | Free |
| [Windows Fundamentals 1–3](https://tryhackme.com/room/windowsfundamentals1xbx) | TryHackMe | Registry, UAC, Defender in a live VM | Free |

### Networking & packet analysis
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Introduction to Networking | [HTB Academy](https://academy.hackthebox.com/) | OSI, TCP/IP, subnetting, DNS, ARP | Free |
| [Intro to Networking](https://tryhackme.com/room/introtonetworking) | TryHackMe | Visualize packets/routing interactively | Free |
| [Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics) | TryHackMe | Load PCAPs, filter traffic, spot anomalies | Free |
| PacketMaze / blue labs | [CyberDefenders](https://cyberdefenders.org/) | Real forensic PCAP, answer intrusion questions | Free |

### Web app security
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Web Security Academy](https://portswigger.net/web-security) | PortSwigger | 250+ labs: SQLi, XSS, SSRF, IDOR, XXE, CSRF with Burp | **Free** |
| [OWASP Top 10](https://tryhackme.com/room/owasptop102021) | TryHackMe | Exploit each Top-10 category in isolated VMs | Free |
| SQL Injection Fundamentals | [HTB Academy](https://academy.hackthebox.com/) | Live web targets, guided | Free |

### SIEM & log analysis (SOC core)
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Splunk Fundamentals 1](https://www.splunk.com/en_us/training/free-courses/overview.html) | Splunk | Ingest data, write SPL, build dashboards | Free |
| Boss of the SOC (BOTS) | [CyberDefenders](https://cyberdefenders.org/) | Hunt real attack data with SPL | Free |
| [Kusto Detective Agency](https://detective.kusto.io/) | Microsoft | Solve mysteries by writing KQL | Free |
| [KC7 (modules 1–5)](https://kc7cyber.com/) | KC7 | KQL across email/DNS/auth/endpoint logs | Free |
| Sentinel modules (browse) | [Microsoft Learn](https://learn.microsoft.com/training/browse/?terms=sentinel) | Configure Sentinel, detection rules, playbooks | Free |
| [Wazuh room](https://tryhackme.com/room/wazuhct) | TryHackMe | Pre-built Wazuh VM: query alerts, tune rules | Free |

### SOC triage, phishing, DFIR
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [SOC Analyst path](https://app.letsdefend.io/) | LetsDefend | Work a real alert queue; analyze phishing, escalate | Freemium |
| Phishing analysis | [Blue Team Labs Online](https://blueteamlabs.online/) | Headers, attachments, URLs in guided scenarios | Freemium |
| Blue Team Labs (DFIR) | [CyberDefenders](https://cyberdefenders.org/) | 100+ memory/disk/network forensic scenarios | Free |
| Digital Forensics module | [HTB Academy](https://academy.hackthebox.com/) | Windows artifacts, memory, timelines | Free |

### Detection engineering
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Sigma room](https://tryhackme.com/room/sigma) | TryHackMe | Write Sigma rules, convert to SIEM queries | Free |
| Detection scenarios | [KC7](https://kc7cyber.com/) | Write/test detection logic vs attack data | Free |
| Detection Engineering path | [LetsDefend](https://app.letsdefend.io/) | Deploy Sigma rules, test vs SIEM alerts | Freemium |

### Privilege escalation & CTF
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Linux/Windows PrivEsc](https://tryhackme.com/room/linuxprivesc) | TryHackMe | SUID, sudo, cron, kernel, PATH on live VMs | Free |
| PrivEsc dojo | [pwn.college](https://pwn.college/) | University-grade OS-level privesc | Free |
| [picoCTF practice](https://picoctf.org/) | picoCTF | 400+ challenges across all domains | Free |
| Starting Point | [Hack The Box](https://www.hackthebox.com/) | Guided beginner machines | Freemium |

### Cloud security
| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [AZ-900 Cloud Concepts](https://learn.microsoft.com/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/) | Microsoft Learn | Cloud models + Azure security with sandbox | Free |
| Sentinel investigation | [Microsoft Learn](https://learn.microsoft.com/azure/sentinel/investigate-cases) | Deploy Sentinel on free Azure trial, run KQL | Free (trial) |
| CloudGoat / flaws.cloud | [flaws.cloud](http://flaws.cloud/) | Deliberately vulnerable AWS to exploit | Free |
| GCP Security Fundamentals | [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) | IAM, VPC, Security Command Center | Freemium |

---

## Dead / moved (don't link these)
| Old resource | Status | Use instead |
|---|---|---|
| Old SC-200 path URLs | ❌ 404 (MS restructured) | Browse [MS Learn](https://learn.microsoft.com/training/browse/?terms=sentinel) |
| Cybrary free labs | 🔒 gutted ~2022 | LetsDefend, CyberDefenders, BTLO |
| SANS CyberAces | ❌ discontinued | THM Pre-Security, HTB free modules |
| RangeForce Community | 🔒 restricted | KC7, LetsDefend, CyberDefenders |
| docs.wazuh.com (interactive) | ⚠️ flaky | [wazuh.com](https://wazuh.com/) + THM Wazuh room |

---

*Notes: TryHackMe rate-limits automated checks but all `tryhackme.com/room/<slug>` links are valid in a browser. HTB Academy module URLs redirect to login — filter the catalog by "Free." Don't hardcode Microsoft SC-200 path URLs; use the browse link. See `research/lab-inventory/cybersecurity-2026.md` for raw findings.*
