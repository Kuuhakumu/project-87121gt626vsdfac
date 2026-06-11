# 🎤 Cybersecurity Interview Prep

> Question bank for entry-level security roles (SOC Analyst, Jr. Security Analyst, GRC Analyst, Jr. Pentester). Technical questions grouped by domain, plus a STAR behavioral bank. Based on 2026 market research — see [/research/market-research](../../research/market-research/cybersecurity-2026.md).

[← Job Hunt](05-job-hunt.md) · [Hub](README.md) · [Resources](resources.md)

---

## How entry-level interviews actually run

Most entry-level security roles follow a **3–4 stage** process:

1. **Recruiter screen** (20–30 min) — motivation, work authorization, salary expectations, cert status. Non-technical.
2. **Technical screen** — take-home or live: log-analysis scenario, a short quiz, or a CTF-style task.
3. **Technical panel / hiring manager** — the questions below. Often scenario-driven ("walk me through…").
4. **Behavioral** — STAR-format questions, team fit.

> The most common reason juniors fail: they've memorized definitions but can't **walk through a scenario**. For every concept below, practice saying it out loud as a story, not a dictionary entry.

---

## Technical questions by domain

### Networking fundamentals

- Explain the OSI model. At which layer does a firewall operate? A switch? A router?
- Walk me through what happens when you type `https://example.com` into a browser and press Enter. *(DNS → TCP handshake → TLS handshake → HTTP request → response. Naming each step is the differentiator.)*
- What's the difference between TCP and UDP? Give a real protocol that uses each.
- What's the TCP three-way handshake? (SYN → SYN-ACK → ACK)
- What are the port numbers for SSH, DNS, HTTP, HTTPS, SMB, RDP? *(22, 53, 80, 443, 445, 3389)*
- What's the difference between a public and private IP? What is NAT doing?
- What is DNS and how does recursive resolution work?
- Subnet this: how many usable hosts in a /29? *(6)*

### Security concepts

- Define the CIA triad. Give an example of a control protecting each leg.
- Symmetric vs asymmetric encryption — when do you use each? Where do they combine? *(TLS: asymmetric to exchange a symmetric session key.)*
- What is hashing and how is it different from encryption? Why salt a hash?
- What is PKI? Walk through how a certificate proves a site's identity.
- Explain defense in depth and give three layers.
- What is the principle of least privilege? Give an example of violating it.
- What is zero trust and how does it differ from perimeter security?

### SOC / detection / incident response

- A SIEM alert fires for **10,000 failed logins** on one account in 5 minutes. Walk me through your triage. *(Check source IP/geo, is it one IP or many, did any succeed after, is the account privileged, is it a known scanner, brute-force vs password spray, contain → escalate.)*
- Walk me through investigating a **phishing email** from alert to closure. *(Headers/SPF-DKIM-DMARC, sender reputation, detonate URL/attachment in sandbox, check who else received it, search for clicks/credential entry, contain.)*
- What is the incident response lifecycle? *(PICERL: Preparation, Identification, Containment, Eradication, Recovery, Lessons Learned — or NIST's 4 phases.)*
- Difference between an **event**, an **alert**, and an **incident**?
- What is MITRE ATT&CK and how would you use it in an investigation? *(Map observed behavior to tactics/techniques, e.g. T1059 Command & Scripting; current is v19.1.)*
- IDS vs IPS — what's the difference and when would you choose each?
- What is a false positive vs false negative, and why is tuning important?
- You see `powershell.exe` spawned by `winword.exe`. Why is that suspicious? *(Office spawning a shell = classic macro/maldoc execution; LOLBin abuse.)*
- What's the difference between EDR and traditional antivirus? *(Behavioral telemetry + response vs signature matching.)*

### Vulnerability management

- What is CVSS and how do you use it to prioritize patching? *(Base/temporal/environmental; don't patch purely by score — factor exploitability and asset criticality, e.g. CISA KEV.)*
- A scan returns 4,000 findings. How do you prioritize?
- What's the difference between a vulnerability, a threat, and a risk?
- What is patch management and why is a test ring important?

### Web / application security

- What is SQL injection? How do you prevent it? *(Parameterized queries / prepared statements, input validation, least-privilege DB account.)*
- What is XSS? Name the types. *(Reflected, stored, DOM-based.)* How do you mitigate? *(Output encoding, CSP, sanitization.)*
- What does the OWASP Top 10 cover, and what's #1 in the 2025 list? *(Broken Access Control.)*
- What is CSRF and how does a token defend against it?

### Cloud security (now baseline, not optional)

- Explain the **shared responsibility model**. Who secures what in IaaS vs SaaS?
- What's the most common cloud breach cause? *(Misconfiguration — public storage buckets, over-permissive IAM.)*
- What does least privilege look like in cloud IAM? Roles vs users vs service accounts?
- Which API calls would worry you in CloudTrail logs? *(`CreateUser`, `AttachUserPolicy`, `GetSecretValue` outside normal patterns.)*

### 2026-current topics (differentiators)

- What is a Sigma rule and why is it useful? *(Vendor-neutral detection-as-code; transpiles to SPL/KQL/Elastic.)*
- What are the NIST CSF 2.0 functions? *(Govern, Identify, Protect, Detect, Respond, Recover — Govern is the 2.0 addition.)*
- What is prompt injection? *(OWASP LLM Top 10 2025, LLM01 — manipulating an LLM via crafted input.)*
- How does AI-assisted triage change the SOC analyst role? *(Summarizes/accelerates, doesn't replace judgment on escalations.)*

---

## Behavioral questions (STAR format)

Answer with **S**ituation → **T**ask → **A**ction → **R**esult. Prepare 4–5 stories you can flex across questions.

- Tell me about a time you explained something technical to a non-technical person.
- Describe a project or home lab you built. Why, and what did you learn? *(Lean on your CTF writeups / portfolio.)*
- Tell me about a time you failed or got something wrong. What did you change?
- How do you stay current with security news and threats? *(Name specifics: The Hacker News, Risky Business, r/cybersecurity, vendor blogs.)*
- Describe a time you had to learn something difficult quickly.
- Tell me about a disagreement on a team and how you handled it.
- Why cybersecurity? Why this company?
- Where do you see yourself in your security career in three years?

> **For the "project" question, always have a lab story ready.** Hiring managers consistently rank a demonstrable home lab / CTF writeup above a cert with no hands-on evidence.

---

## Practical components (increasingly common in 2026)

Some employers add a hands-on stage. Be ready to:

- Analyze a **PCAP in Wireshark** and identify suspicious traffic.
- Write a basic **SPL or KQL query** to find a pattern in logs (practice on KC7 / Kusto Detective Agency / Splunk free).
- Review a mock incident or vuln-scan output and identify gaps.
- Triage a simulated alert queue (practice on LetsDefend — it mirrors this exactly).

---

## Prep plan (the week before)

- [ ] Re-read your own CTF writeups and lab notes — interviewers ask about *your* repos.
- [ ] Say every Phase-2 concept (CIA, PKI, PICERL, OSI, shared responsibility) out loud as a scenario.
- [ ] Run 3–5 fresh LetsDefend alerts to warm up triage instincts.
- [ ] Prepare 5 STAR stories.
- [ ] Research the company: their stack (Microsoft shop? AWS? which SIEM?), recent news, the actual job description's keywords.
- [ ] Prepare 3 questions to ask them (team structure, on-call, growth path, what tools they run).

[← Job Hunt](05-job-hunt.md) · [Hub](README.md) · [Resources](resources.md)
