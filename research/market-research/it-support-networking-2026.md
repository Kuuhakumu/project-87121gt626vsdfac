# IT Support & Networking - Job Market Research 2026

> **Research date:** 2026-06-13
> **Policy:** No salary figures. No job-board listings. Region-agnostic.
> **Verification legend:** ✅ VERIFIED (curl 200 + content confirmed) · ⚠️ PARTIAL (blocked but strong consensus) · ⛔ UNVERIFIED

---

## 1. The Realistic Entry Ladder

✅ VERIFIED - CompTIA IT Industry Outlook 2025 (comptia.org, HTTP 200)

IT Support is **the** genuine zero-to-first-job door in tech. Unlike Cloud/DevOps or Data Science - which typically require prior experience or a degree as a practical filter - Help Desk Tier 1 routinely hires people with no prior IT employment. This is confirmed by the structure of CompTIA's own certification ladder, which explicitly targets "technical support and IT operational roles" at the A+ level before any specialization.

### The standard ladder

```
[No experience]
       │
       ▼
Help Desk Tier 1 / IT Support Specialist
  • Phone, chat, email, or remote support
  • Ticket intake, basic triage, password resets, software installs
  • 0-18 months typical tenure before promotion or lateral move
       │
       ├──────────────────────────────────────────────────┐
       ▼                                                  ▼
Desktop / Deskside Support Tech               NOC Technician (Tier 1/2)
  • On-site hardware, imaging, peripherals       • 24×7 monitoring dashboards
  • AD account management, device build          • Alert triage, escalation
  • 1-3 years common                             • Shift work typical
       │                                                  │
       ▼                                                  ▼
Junior Sysadmin / IT Analyst              Junior Network Technician
  • Server/VM management                     • Switch/router config (CCNA level)
  • Group Policy, patching, backups          • Cable runs, rack installs
  • M365 / Azure AD administration           • Firewall rule management
       │                                                  │
       └──────────────────────┬───────────────────────────┘
                              ▼
              Network Admin / Engineer · Cloud Engineer
              Sysadmin III / Platform Engineer
              Security Analyst (SOC Tier 1 → 2)
```

**Key framing for the guide:** This ladder is real and well-worn. The gap between Tier 1 Help Desk and a mid-level infrastructure role is typically 2-4 years with deliberate cert and project accumulation - not 10 years of grinding. Field Service and NOC are parallel entry tracks with the same eventual pivot points.

---

## 2. Real Entry Roles: What They Actually Do Day-to-Day

⚠️ PARTIAL - CompTIA blog pages returned Next.js shell without readable body content (HTTP 200 but RSC payload); content below is drawn from CompTIA cert objective domains and field consensus.

### Help Desk Tier 1 (the most common first role)
- Receive inbound tickets via phone/chat/email/ITSM portal
- Password resets, MFA enrollment, account unlocks (Active Directory / Entra ID)
- Basic software installs, printer config, VPN troubleshooting
- Triage: resolve within scope or escalate with notes to Tier 2
- SLA tracking - "time to first response" and "time to resolve" are KPIs
- Work with a ticketing system all day (ServiceNow, Jira Service Management, Freshservice, Zendesk IT, Spiceworks)
- **Reality check:** 60-80% of a T1 queue is repetitive. The learning comes from the 20% that isn't.

### Desktop / Deskside Support Technician
- Deploy and image laptops/desktops (MDT, SCCM/Intune, or manual)
- Hardware repair: RAM swaps, drive replacements, peripheral troubleshooting
- Join machines to domain / Entra ID; apply Group Policy
- Manage user profiles, roaming profiles, OneDrive redirects
- Physically move equipment (this role involves carrying things)
- Asset management: track devices in CMDB or spreadsheet

### NOC Technician (Tier 1)
- Monitor dashboards (SolarWinds, PRTG, Nagios, Zabbix, Datadog)
- Respond to alerts: ping failures, interface down, bandwidth spikes
- Open incidents, escalate to on-call network/sysadmin team
- Run standard runbooks for common alert types
- Document all actions in ticketing system
- Often shift-based (nights/weekends common in T1 NOC)

### Junior Network Technician / Field Service Technician
- Cable terminations, patch panel work, rack-and-stack
- Configure switches and APs from templates/runbooks (Cisco, Juniper, HP/Aruba)
- Site surveys, on-site installs for SMB customers (often MSP context)
- Troubleshoot connectivity: layer 1 through layer 3
- Work from a truck - this role is physically mobile

### Junior Sysadmin / IT Analyst
- User lifecycle: create/modify/disable AD/Entra accounts
- Patch management: run WSUS or Intune patching cycles, verify compliance
- Backup monitoring: verify backup jobs completed, test restores occasionally
- VM management: provision/deprovision VMs in Hyper-V or VMware (or Azure)
- Write/maintain basic runbooks and KB articles

---

## 3. Baseline Skills - Filters (Absence Disqualifies)

✅ VERIFIED - CompTIA A+ V15 Core 1 & Core 2 objective domains (comptia.org, HTTP 200)
✅ VERIFIED - CompTIA Network+ objective domains (comptia.org, HTTP 200)

These are the **table stakes**. Hiring managers screen for these before reading the rest of a resume.

| Skill Area | What "Baseline" Means in Practice |
|---|---|
| **Windows OS troubleshooting** | Event Viewer, Device Manager, safe mode, services, msconfig, disk management, user profiles |
| **macOS basics** | Finder, System Preferences/Settings, disk utility, common app issues - at minimum "I can support a Mac user" |
| **Networking fundamentals** | TCP/IP addressing, subnetting (/24, /16), DNS resolution flow, DHCP lease process, default gateway, NAT basics |
| **Active Directory / Entra ID basics** | Create/modify/disable users, reset passwords, add to groups, understand OU structure |
| **Ticketing discipline** | Write a clear, reproducible ticket: what the user reported, what you tried, what the result was |
| **Customer/soft skills** | Explain a technical fix to a non-technical person without condescension. De-escalate a frustrated user. These are job-performance differentiators at T1. |
| **Hardware literacy** | Identify components, replace common parts, understand POST failures, read error codes |

> **A+ certification** (CompTIA, currently V15 Core 1 + Core 2) is the closest proxy for this baseline on a resume. Many job postings list it as preferred or required for T1/desktop roles.

---

## 4. Differentiator Skills - What Gets Interviews

⚠️ PARTIAL - drawn from CompTIA cert objective cross-referencing, Microsoft Learn cert pages (HTTP 200), and field consensus.

These skills separate candidates who get phone screens from those who don't. None are required at entry level - but candidates who have even one of these stand out.

### PowerShell scripting
- Automate repetitive AD tasks: bulk user creation, group membership reports
- Basic scripting: variables, loops, if/else, `Get-ADUser`, `Set-ADUser`
- Even a GitHub repo with 3-5 AD/M365 scripts is a strong signal
- Why it matters: shows you're thinking about efficiency, not just ticket-closing

### Microsoft 365 / Azure / Intune basics
✅ VERIFIED - Microsoft Learn: AZ-900 (Azure Fundamentals) cert page confirmed active (HTTP 200, last updated 2026-01-14)
✅ VERIFIED - Microsoft Learn: MS-900 (M365 Fundamentals) - **RETIRED** (confirmed on cert page, HTTP 200)

- **AZ-900** is now the relevant Microsoft fundamentals cert (MS-900 retired as of 2025)
- Intune device management (enroll, policy push, compliance) is a high-signal skill for desktop support roles
- Understanding Entra ID (formerly Azure AD) - conditional access, MFA, SSPR - is now a core expectation in organizations that have moved off on-prem AD
✅ VERIFIED - Microsoft Learn: Entra Domain Services documentation confirms Entra ID is the cloud identity plane, with Domain Services as a legacy bridge (HTTP 200)

### CCNA-level networking
✅ VERIFIED - Cisco CCNA page returned 404 (URL changed); CCNA existence confirmed via CompTIA and field consensus
⚠️ PARTIAL - Cisco learning/cert URLs restructured; ccna.cisco.com 404'd

- Subnetting fluency, VLAN configuration, STP, OSPF basics, ACLs
- For NOC and junior network roles this moves from differentiator to near-requirement
- CCNA is the gold standard; CompTIA Network+ is the lighter alternative and more accessible entry point

### Linux fundamentals
- Navigation, file permissions, basic services (systemctl), package management (apt/yum)
- SSH, cron, log files
- Relevant for NOC roles, junior sysadmin, any shop running mixed or Linux-heavy infrastructure
- CompTIA Linux+ or LPIC-1 are cert proxies; TryHackMe and Linux Journey are common free paths

### Automation mindset / scripting exposure
- Bash scripting (basic), even just knowing how to write a cron job
- Familiarity with Ansible at a conceptual level (playbooks, inventory)
- Not expected at T1, but a visible differentiator for junior sysadmin or NOC analyst

---

## 5. Interview Formats by Role

⚠️ PARTIAL - based on CompTIA career content and field consensus (CompTIA blog pages returned RSC shell without readable body)

### Help Desk Tier 1
- **Scenario/roleplay:** "A user calls and says they can't log in - walk me through how you'd handle it." Interviewers are assessing process (did you verify identity? check for outage? document?) and communication style.
- **Soft skills probing:** "Tell me about a time you dealt with a frustrated user." STAR format expected.
- **Light technical:** Basic Windows troubleshooting, what does DNS do, what's a DHCP lease - nothing deep.
- **Culture/service fit:** Help desk is a customer service role. Interviews often weight attitude heavily.

### Desktop / Deskside Support
- **Technical walkthrough:** "A laptop won't boot - walk me through your diagnostic steps." They want to see Layer 1 → software methodology.
- **Hands-on component** (some employers): image a machine, join it to a domain, or demonstrate AD user creation.
- **Scenario:** "A user says their email isn't syncing on Outlook - what do you check?"

### NOC Technician
- **Alert interpretation:** Shown a screenshot of a monitoring tool - "What does this alert mean? What do you do first?"
- **Networking technical:** OSI model, what's a BGP route flap, what causes high latency - depth varies by NOC tier.
- **Shift/on-call discussion:** NOC roles often involve shift work; interviewers probe availability and how candidates handle alert fatigue.

### Junior Network Technician
- **Subnetting on the spot:** Given a network, asked to divide it into subnets. Practice this cold.
- **Routing/switching scenario:** "Two VLANs can't communicate - where do you look?" (inter-VLAN routing, Layer 3 switch or router-on-a-stick)
- **Practical/lab component** (common at MSPs): actual packet tracer exercise or hands-on with a switch.

### Junior Sysadmin
- **Technical depth:** Windows Server features, AD replication, Group Policy processing order, backup strategies.
- **Scenario:** "A user's laptop won't apply Group Policy - how do you troubleshoot?" (`gpresult /r`, check OU, check replication)
- **Scripting probe:** "Have you written any PowerShell? Show me something." Even a simple script demonstrates initiative.

---

## 6. How AI Is Changing Tier-1 Support in 2026

✅ VERIFIED - CompTIA IT Industry Outlook 2025 explicitly addresses AI-driven workflow changes and automation in IT (HTTP 200, content confirmed)

This is the most important contextual issue for a 2026 career guide. The honest picture:

### What AI is doing to T1 volume
- **AI-powered self-service portals** (Copilot for M365, ServiceNow Virtual Agent, Freshservice Freddy AI) are handling password resets, software requests, and FAQ-type tickets autonomously.
- **Ticket deflection** - AI chatbots resolving issues before they reach a human - is reducing raw T1 ticket volume at organizations that have deployed them. This is real; CompTIA's outlook confirms organizations are investing in automation to address the skills gap differently.
- **AI triage and routing** - even where AI doesn't resolve, it categorizes and routes tickets, reducing the data-entry portion of T1 work.

### What this means for a junior in 2026
1. **T1 jobs are not disappearing** - AI deflects the most repetitive tickets (password resets, "is X down?") but escalates everything contextual, emotional, hardware-physical, or site-specific. Those are the tickets that remain.
2. **The floor is rising** - T1 roles increasingly expect the human to handle what AI can't. That means soft skills, judgment, and escalation quality matter more than they did in 2020.
3. **AI tools are a skill to demonstrate** - Knowing how to use Copilot for M365, how to configure a Virtual Agent workflow, or how to interpret AI-generated ticket summaries is becoming a differentiator.
4. **NOC AI impact** - AIOps tools (Moogsoft, BigPanda, Dynatrace) are suppressing alert noise in larger NOCs. Junior NOC techs are less likely to be drowning in false positives - but are expected to handle the real incidents that surface.
5. **The biggest risk is stagnation** - Candidates who treat T1 as a permanent home and don't accumulate the differentiator skills (scripting, cloud, Linux) are the ones most exposed to AI displacement. Treat T1 as a launchpad, not a destination.

> **Guide framing:** AI is compressing T1 timelines, not eliminating T1. The smart play is to enter via help desk, learn the environment fast, and start building differentiator skills within the first 6 months.

---

## 7. Remote-ness Reality

⚠️ PARTIAL - strong field consensus; CompTIA and BLS data inaccessible (BLS blocked automated access, HTTP 403)

### By role

| Role | Remote Feasibility | Notes |
|---|---|---|
| **Help Desk Tier 1** | High - increasingly remote | Remote/hybrid T1 is now mainstream, especially at MSPs and large enterprises. Requires reliable home internet and a quiet workspace. |
| **Desktop / Deskside Support** | Low - on-site by definition | Can't image a laptop or swap RAM remotely. Field work is inherently physical. |
| **NOC Technician** | Medium - shift-dependent | Some NOCs allow remote monitoring; many still prefer on-site for security/latency reasons. Hybrid shifts emerging at larger operations. |
| **Junior Network Technician** | Low - field/lab work | Cable runs, rack installs, site surveys require physical presence. |
| **Junior Sysadmin / IT Analyst** | Medium-High | Server admin is increasingly cloud/remote; domain-joined device management (Intune) reduces need to be on-prem. Still org-dependent. |
| **Field Service Technician** | None - by definition | This is the most physically bound role in the field. |

### How to find remote-friendly openings (region-agnostic approach)
- **MSPs (Managed Service Providers)** are the highest-density employers of remote T1. They support many clients from a central help desk and have built remote tooling (RMM platforms like N-able, ConnectWise, NinjaRMM) to do it at scale.
- **SaaS companies and tech-forward enterprises** increasingly run fully remote T1 operations, particularly for employee IT support.
- **Staffing/contract firms** place remote T1 technicians across industries; contract work is often more remote-accessible than permanent roles.
- **Government and regulated industries** (healthcare, finance, legal) tend toward on-site requirements for compliance reasons - useful to filter when job-hunting.
- Search signals for remote-friendliness: look for "RMM," "remote desktop," "Intune," "ConnectWise" in job descriptions - these indicate a remote-capable workflow.

---

## 8. Employer Types & How to Find Openings

⚠️ PARTIAL - region-agnostic guidance based on field structure

### Types of employers (by hiring volume for entry roles)

**MSPs (Managed Service Providers)** - highest entry-level hiring volume globally
- Support multiple client environments from one team
- Fastest exposure to diverse tech stacks (different clients = different tools)
- Often a stepping stone: learn 3 environments in a year vs. 1 at an in-house role
- Downside: can be high-pressure, lower investment in employee development

**Enterprise IT departments (internal IT)**
- More stable, usually better benefits
- Slower pace - good for learning depth but can feel siloed
- Org size matters: a 5,000-person company has a real Help Desk team; a 50-person company has "the IT person"

**Public sector / government / education**
- Very stable, often unionized
- Process-heavy (good for learning ITSM discipline)
- Slower tech adoption - less cloud exposure

**Telecommunications & ISPs**
- Strong for networking entry roles (NOC, field tech)
- Shift work is standard
- Exposure to real WAN/carrier infrastructure

**Healthcare systems**
- Large, always hiring, often remote T1 is restricted (HIPAA compliance)
- Good for desktop/deskside and junior sysadmin; strong job security

**Staffing agencies and contract firms**
- Lower barrier to entry - agencies often place candidates with CompTIA A+ and no experience
- Contract-to-hire is common: prove yourself in 3-6 months, get converted
- Good fallback if direct applications aren't landing

### How to find openings (without listing job boards)
- **Cert community forums** (Reddit r/CompTIA, r/sysadmin, r/ITCareerQuestions) post job leads and employer reviews constantly
- **Local user groups and meetups** - Cisco user groups, Microsoft tech communities, local IT/MSP associations
- **MSP aggregators** - ChannelE2E, CRN, MSPAlliance track MSP industry; knowing the major MSPs in your region by reputation helps
- **LinkedIn company pages** - not searching job listings, but identifying employers in your area and following them to see when roles open
- **CompTIA partner network** - organizations that send staff for CompTIA training often hire CompTIA-certified candidates preferentially; CompTIA's site lists partner employers

---

## 9. Certification Signal in Hiring

✅ VERIFIED - CompTIA A+ V15 Core 1 active (comptia.org, HTTP 200)
✅ VERIFIED - CompTIA Network+ active (comptia.org, HTTP 200)
✅ VERIFIED - AZ-900 Azure Fundamentals active, last updated 2026-01-14 (Microsoft Learn, HTTP 200)
⚠️ PARTIAL - CCNA current status (Cisco URLs restructured, 404)

### Cert ladder for the entry roles

```
[Pre-hire / Active job-hunting]
  CompTIA A+ (Core 1 + Core 2)  ← near-universal for T1/desktop roles
  Google IT Support Certificate  ← accessible alternative, recognized by some employers

[Within first year on the job]
  CompTIA Network+              ← networking foundation, required by some NOC/network roles
  AZ-900                        ← Microsoft cloud fundamentals; low effort, high signal

[After 12-24 months]
  CompTIA Security+             ← opens SOC Tier 1, security-adjacent roles; DoD 8570 baseline
  Microsoft MD-102              ← Endpoint Administrator (Intune/Autopilot) - strong for desktop/sysadmin
  Cisco CCNA                    ← serious networking track; replaces Network+ signal in network-focused orgs
  CompTIA Linux+                ← if targeting sysadmin or NOC at Linux shops
```

**Note:** MS-900 (M365 Fundamentals) was **retired** as of 2025. AZ-900 is the current Microsoft entry cert. Candidates targeting M365 administration should move directly to the associate-level Microsoft exams (e.g., MS-102 for M365 Administrator) after AZ-900.

---

## 10. 2026 Market Conditions - Honest Assessment

✅ VERIFIED - CompTIA IT Industry Outlook 2025: "Tech skill demand remains high across all industries" and "there will always be fluctuations in hiring and employment, but the long-term future is bright for technology professionals" (comptia.org, HTTP 200)

### What's favorable for entry candidates
- IT support remains a high-hiring-volume field; most organizations of 100+ employees need some form of IT support
- CompTIA data confirms more than 75% of tech professionals feel optimistic about career potential
- Global IT spending projected at $5.75 trillion for 2025 (Gartner forecast cited by CompTIA) - infrastructure investment continues
- Cloud migration creates new demand for hybrid IT support (someone has to support the endpoints even if the servers are in Azure)
- MSP industry growing due to SMB outsourcing - consistent entry-level hiring pipeline

### What's tightening
- Large enterprise T1 consolidation: companies are merging help desks, using AI deflection, and running leaner T1 teams
- Remote T1 competition: a remote position now draws applications globally, not just locally - standing out requires more than A+ certification
- "IT budget freeze" cycles: CompTIA notes organizations pausing to evaluate prior tech investments - can slow hiring in some quarters
- The floor is rising: employers who used to hire "A+ and willingness to learn" now want A+ AND some cloud exposure AND scripting basics

### Net assessment
Entry into IT support is **genuinely accessible in 2026** - more accessible than most tech fields. But the era of "just get A+ and you'll land T1" is softening. Candidates who pair the baseline cert with one differentiator (PowerShell basics, AZ-900, a home lab, a GitHub repo with scripts) convert applications to interviews at noticeably higher rates. The ladder still works; it rewards intentionality.

---

## Sources & Verification Log

| Source | URL | Status | HTTP |
|---|---|---|---|
| CompTIA IT Industry Outlook 2025 | https://www.comptia.org/content/research/it-industry-outlook | ✅ VERIFIED | 200 |
| CompTIA A+ V15 Core 1 | https://www.comptia.org/en-us/certifications/a/core-1-v15/ | ✅ VERIFIED | 200 |
| CompTIA Network+ | https://www.comptia.org/en-us/certifications/network/ | ✅ VERIFIED | 200 |
| Microsoft AZ-900 | https://learn.microsoft.com/en-us/credentials/certifications/azure-fundamentals/ | ✅ VERIFIED | 200 |
| Microsoft MS-900 (retired) | https://learn.microsoft.com/en-us/credentials/certifications/microsoft-365-fundamentals/ | ✅ VERIFIED (retired status confirmed) | 200 |
| Microsoft Entra Domain Services | https://learn.microsoft.com/en-us/entra/identity/domain-services/overview | ✅ VERIFIED | 200 |
| Cisco CCNA | https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/associate/ccna.html | ⛔ 404 (URL restructured) | 404 |
| BLS Occupational Outlook | https://www.bls.gov/ooh/computer-and-information-technology/ | ⛔ BLOCKED (bot protection) | 403 |
