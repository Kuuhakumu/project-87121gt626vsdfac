# Cybersecurity Lab & Platform Inventory — 2026

> Research date: 2026-06-13. Verified via `curl` (WebFetch/WebSearch were down). Status key: ✅ live (HTTP 200) · ⚠️ alive but bot-blocked (429/403) · ❌ dead/moved · 🔒 free tier removed.

## Verified Free / Freemium Platforms

| Platform | Best For | Cost | Status |
|---|---|---|---|
| [PortSwigger Web Security Academy](https://portswigger.net/web-security) | Web app security (SQLi, XSS, SSRF, IDOR) — 250+ labs | **100% Free** | ✅ |
| [HTB Academy](https://academy.hackthebox.com/) | Structured modules, live targets, offensive + defensive | Freemium (many free modules) | ✅ |
| [CyberDefenders](https://cyberdefenders.org/) | DFIR, packet/memory forensics, blue-team scenarios | Mostly Free | ✅ |
| [LetsDefend](https://app.letsdefend.io/) | SOC alert-queue simulation, phishing, log analysis | Freemium | ✅ |
| [picoCTF](https://picoctf.org/) | Beginner CTF, all domains, 400+ challenges | **Free** | ✅ |
| [OverTheWire (Bandit)](https://overthewire.org/wargames/bandit/) | Linux CLI fundamentals via wargame | **Free** | ✅ |
| [KC7 Cyber](https://kc7cyber.com/) | KQL log analysis, detection, SOC analyst skills | **Free** | ✅ |
| [Kusto Detective Agency](https://detective.kusto.io/) | KQL practice, Sentinel prep | **Free** | ✅ |
| [pwn.college](https://pwn.college/) | Binary exploitation, OS internals, privesc (ASU-backed) | **Free** | ✅ |
| [Blue Team Labs Online](https://blueteamlabs.online/) | DFIR, phishing, SOC scenarios | Freemium | ✅ |
| [Microsoft Learn](https://learn.microsoft.com/training/) | Azure/Sentinel/KQL, SC-200 prep, cloud security | **Free** | ✅ (browse stable; old SC-200 deep links 404) |
| [Splunk Free Training](https://www.splunk.com/en_us/training/free-courses/overview.html) | Splunk/SPL Fundamentals 1 | **Free** | ✅ |
| [TryHackMe](https://tryhackme.com/) | Guided beginner paths, SOC/blue team, Linux/Windows | Freemium (~$14/mo full) | ⚠️ alive, rate-limits bots |
| [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) | GCP security, IAM, SCC | Freemium (credits) | ⚠️ bot-blocked, known active |
| [Codecademy](https://www.codecademy.com/) | Python, intro cybersecurity | Freemium | ✅ |

## Topic → Lab Map (verified)

| Topic | Lab | Platform | Cost |
|---|---|---|---|
| Linux CLI | Bandit (34 levels) | OverTheWire | Free |
| Linux/Windows fundamentals | Linux/Windows Fundamentals modules | HTB Academy | Freemium |
| Networking | Introduction to Networking module | HTB Academy | Freemium |
| Packet analysis | PacketMaze + BOTS datasets | CyberDefenders | Free |
| Cryptography | Cryptography module / Crypto picoCTF | HTB Academy / picoCTF | Free |
| SIEM (Splunk) | Splunk Fundamentals 1 + BOTS | Splunk / CyberDefenders | Free |
| SIEM (Sentinel/KQL) | Kusto Detective Agency + KC7 | Microsoft / KC7 | Free |
| SIEM (home lab) | Wazuh 4.9.2 self-host + THM Wazuh room | wazuh.com / TryHackMe | Free |
| Log analysis | KC7 modules 1–5 | KC7 | Free |
| Phishing / SOC triage | SOC Analyst path | LetsDefend | Freemium |
| DFIR | 100+ blue-team labs | CyberDefenders | Free |
| Vuln scanning | Info Gathering / Vuln Assessment | HTB Academy | Freemium |
| Web app security | Web Security Academy (250+ labs) | PortSwigger | Free |
| Privilege escalation | PrivEsc dojos | pwn.college | Free |
| Python/PowerShell | Intro to Python 3 (security) | HTB Academy | Freemium |
| CTF | picoGym year-round | picoCTF | Free |
| Cloud security | AWS Free Tier / Azure / CloudGoat / flaws.cloud | AWS/Azure/Rhino | Free |
| Detection (Sigma) | Detection Engineering path | LetsDefend / KC7 | Freemium/Free |

## Dead / Paywalled (avoid; with replacements)

| Old resource | Status | Replacement |
|---|---|---|
| docs.wazuh.com interactive start | ❌ DNS fail | wazuh.com + THM Wazuh room |
| SC-200 direct path URLs | ❌ 404 (restructured) | MS Learn browse + KC7/Kusto |
| Cybrary free labs | 🔒 gutted ~2022–23 | LetsDefend, CyberDefenders, BTLO |
| SANS CyberAces | ❌ discontinued ~2022 | THM Pre-Security, HTB free modules |
| RangeForce Community | 🔒 degraded | LetsDefend, KC7, CyberDefenders |

## Notes
- TryHackMe & HTB Academy module deep-links redirect to login; link to room/catalog roots. THM `tryhackme.com/room/<slug>` URLs are valid.
- Don't hardcode Microsoft SC-200 path URLs — use the browse page with a `sentinel` filter (stable).
- PortSwigger is the single best free web-security resource — prioritize it.
