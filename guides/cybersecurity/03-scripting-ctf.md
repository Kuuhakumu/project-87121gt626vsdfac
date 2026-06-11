# Phase 3: Scripting, Databases & CTFs

> **~100 hrs total** · your pace, no deadline
> Goal: automation literacy + hands-on offensive/defensive practice. No new cert here — this phase builds the skills that differentiate you.

[← Phase 2: Core](02-core.md) · [Hub](README.md) · [Phase 4: Specialization →](04-specialization.md)

---

Scripting is the clearest **differentiator** at entry level (per market research). You don't need to be a software engineer — you need to read code, automate repetitive tasks, and parse logs. That's it.

---

## Python for Security (~40 hrs)

### What to cover
Variables, data types, control flow, functions, file I/O, `requests`, `socket`, regex, JSON parsing, working with APIs. Focus on **security use cases**: log parsing, IOC extraction, simple scanners, automation.

### YouTube / courses
freeCodeCamp Python (free, YouTube) · [Codecademy Learn Python 3](https://www.codecademy.com/learn/learn-python-3) (free tier)

### Interactive labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Introduction to Python 3 | HTB Academy | Security-focused Python with live code runner | Free module |
| Python for cybersecurity | TryHackMe | Build hash crackers, port scanners in-browser | Free tier |
| Python exercises | [Exercism](https://exercism.org/tracks/python) | Mentored Python practice, graded | Free |

### Project
**Port scanner** using `socket` — scan ports 1–1000 on a target, output to CSV. Put it on GitHub with a README.

---

## PowerShell & Bash (~30 hrs)

### What to cover
- **PowerShell:** cmdlets, pipeline, `Get-WinEvent`, filtering, basic AD queries, scripting an audit report. Critical for Windows-heavy SOC work.
- **Bash:** variables, loops, `grep`/`awk`/`sed`, pipes, cron, log parsing one-liners.

### Resources
- [Microsoft Learn PowerShell paths](https://learn.microsoft.com/en-us/training/) (free, Cloud Shell sandbox)
- PowerShell room (TryHackMe, free tier)
- *PowerShell in a Month of Lunches* — Don Jones (book)

### Project
**PowerShell system audit script** → outputs an HTML report (installed software, local users, open ports, patch status).

---

## SQL, KQL & CTF Practice (~30 hrs)

### Databases & query languages
- **SQL:** SELECT, JOINs, WHERE, aggregations — enough to understand SQL injection and query a database
- **KQL (Kusto):** the query language for Microsoft Sentinel — a genuine 2026 differentiator
- **SPL:** Splunk's search language

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Kusto Detective Agency | [detective.kusto.io](https://detective.kusto.io/) | Solve mysteries with KQL | Free |
| KC7 | [kc7cyber.com](https://kc7cyber.com/) | Multi-stage KQL log investigations | Free |
| SQL Injection labs | [PortSwigger](https://portswigger.net/web-security/sql-injection) | Exploit SQLi on live targets (Apprentice tier) | Free |

### Capture the Flag (CTF)
CTFs build real problem-solving muscle. Start beginner-friendly:

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| picoGym | [picoCTF](https://picoctf.org/) | 400+ challenges: web, forensics, crypto, RE | Free |
| Bandit → Natas | [OverTheWire](https://overthewire.org/wargames/bandit/) | CLI wargame → web exploitation progression | Free |
| XSS labs (Apprentice) | [PortSwigger](https://portswigger.net/web-security/cross-site-scripting) | Reflected/stored/DOM XSS | Free |

### Portfolio action
Create a **`ctf-writeups`** GitHub repo. For each challenge: Problem → Analysis → Exploit → Fix/Lesson. This becomes interview gold.

---

## Phase 3 exit checklist
- [ ] Can write a Python script that reads a file, parses it with regex, and outputs structured data
- [ ] Can write a basic PowerShell or Bash script to automate a task
- [ ] Can write basic SQL and KQL queries
- [ ] 2+ projects on GitHub with READMEs
- [ ] Started a CTF writeups repo

Next: [Phase 4 — Specialization Paths →](04-specialization.md)
