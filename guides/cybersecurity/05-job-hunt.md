# Phase 5: Portfolio, Resume & Job Hunt

> **~100 hrs total** · your pace, no deadline
> This phase runs *in parallel* with Phase 4 — build your portfolio as you learn, don't wait until the end.

[← Phase 4: Specialization](04-specialization.md) · [Hub](README.md) · [Beyond Entry-Level →](beyond-entry.md)

---

## GitHub Portfolio

Pin your **4–6 strongest projects**. Each repo needs:
- **README** with: what it does, architecture diagram, setup steps, and the **security impact** ("detects X", "audits Y")
- Screenshots or a demo GIF
- Clean commit history

### Project ideas by path

| Path | Portfolio projects |
|---|---|
| 🔵 Blue | Wazuh home-lab SIEM with documented detections · phishing-analysis writeups · Splunk/KQL dashboards · CyberDefenders/LetsDefend investigation reports |
| 🔴 Red | CTF writeups (Problem → Analysis → Exploit → Fix) · PortSwigger lab solutions · home pentest report (PNPT-style) · a custom Python recon tool |
| ☁️ Cloud | CloudGoat attack/defense writeup · Terraform + Checkov "shift-left" demo · cloud IAM audit report |
| ⚖️ GRC | Mock NIST SP 800-30 risk assessment · GDPR/NIS2 gap analysis · Prowler/ScoutSuite audit report |

> **Quality > quantity.** One well-documented Wazuh lab beats ten "followed-a-tutorial" repos.

---

## Resume & LinkedIn

### Resume rules
- **Lead with certs + projects**, not an objective statement
- **Quantify everything:** "Investigated 50+ simulated SOC alerts on LetsDefend", "Built a Wazuh SIEM monitoring 3 endpoints"
- **Mirror job-posting keywords** for ATS (applicant tracking systems) — if the posting says "SIEM, EDR, MITRE ATT&CK", those words must appear
- **One page** for entry level
- Link your GitHub and any blog/writeups

### LinkedIn
- **Headline:** `Aspiring SOC Analyst | Security+ | Hands-on SIEM & Detection Labs`
- Post your project writeups — visibility matters
- Connect with people in the roles you want

---

## Job titles to search for

Entry roles hide under many names. Search **all** of these:
- SOC Analyst I / Tier 1 SOC Analyst
- Junior / Associate Security Analyst
- Cybersecurity Analyst I
- Security Monitoring Analyst
- Junior Incident Responder
- IAM Analyst · Vulnerability Management Analyst (entry)
- Associate GRC / Compliance Analyst
- IT Security Technician / Security Support Specialist

> **Tip:** Also search "Analyst I", "Associate Security", "Junior Security". Many entry roles sit under IT/helpdesk titles.

---

## Where to apply

### Types of employers that hire entry-level (region-agnostic)

You don't need a list of local job boards — you need to know *which kinds of organizations* hire juniors and find their local equivalents:

- **MSSP / MDR providers (managed security services).** The single most reliable entry door. They hire SOC analysts in volume, provide structured training, and rotate you across many client environments fast. Search "MSSP" or "managed detection and response" + your region.
- **Big consulting / professional-services firms.** Most run graduate or associate programs with a cybersecurity track.
- **Finance, banking, insurance, healthcare.** Regulated industries with large internal security teams and consistent junior hiring.
- **Government & defense.** Often the largest entry-level employer in a country, though frequently citizenship- or clearance-gated.
- **Any large enterprise with an internal SOC.** Retail, telecom, energy, logistics — they all run security operations now.

### How to find the actual openings

- **Search by title, not by board.** Use the [title list above](#job-titles-to-search-for) on whatever the dominant professional network and search engines are in your country.
- **Go direct.** Identify 15–20 target employers (using the categories above) and check their careers pages directly — many roles never hit aggregators.
- **Tap communities.** Role- and region-specific Discords, subreddits, and local chapter groups (BSides, OWASP, DEF CON groups) post openings and referrals. See [resources.md](resources.md).
- **Referrals beat applications.** A warm intro from someone already inside converts far better than a cold application. Build those relationships *before* you need them.

---

## Interview prep

See the full **[Interview Prep Q&A bank →](interview-prep.md)** for ~40 technical questions and behavioral prompts.

### Quick hits — questions you *will* be asked
- Explain the OSI model and an attack at each layer
- Walk me through a phishing investigation from alert to close
- IDS vs IPS — when would you use each?
- What is SQL injection? How do you prevent it?
- You get a SIEM alert for 10,000 failed logins — walk me through triage
- Symmetric vs asymmetric encryption, with a use case
- What's a CVSS score and how do you prioritize patching?

### Behavioral (STAR format)
- "Explain a technical concept to a non-technical person"
- "Tell me about a project or lab you built"
- "How do you stay current on threats?"

---

## The honest hiring reality (2026)

- **Entry is competitive.** The "millions of unfilled jobs" headline is about *experienced* staff. Cert-only candidates with no labs struggle.
- **The path that works:** Help Desk / IT Support (6–18 mo) → SOC Analyst, *or* degree + internship → direct entry. Direct cert-only entry is possible but harder.
- **What separates you:** a demonstrable home lab, documented projects, scripting ability, and cloud fundamentals — not a longer cert list.
- **GRC is underserved** — if you communicate well, it's often an easier entry door than SOC.

Next: [Beyond Entry-Level — Years 2+ →](beyond-entry.md)
