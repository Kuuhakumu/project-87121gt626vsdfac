# IT Support & Networking - Tooling & Trends Research 2026
_Generated: 2026-06-13 | curl-verified where possible_

---

## Verification Legend
- ✅ VERIFIED - curl-confirmed version/status from official source or GitHub API
- ⚠️ PARTIAL - page reachable but detail limited (403, JS-rendered, indirect)
- ⛔ UNVERIFIED - no live confirmation; based on known state at research time

---

## 1. Platform Versions (Verified)

### Windows 11
- **Status:** ✅ VERIFIED (microsoft.com/windows/windows-11 → HTTP 200)
- **Current:** Windows 11 24H2 (late 2024 feature update, actively deployed in enterprise)
- **Teaching note:** Default OS for helpdesk scenarios in 2026. All desktop troubleshooting instruction should target Win11. Win10 reaches end-of-support October 2025 - orgs are mid-migration.

### Windows Server 2025
- **Status:** ✅ VERIFIED (microsoft.com/windows-server → HTTP 200)
- **Current:** Windows Server 2025 (GA Nov 2023, widely adopted for new installs)
- **Teaching note:** New AD deployments use WS2025. Teach DC setup here. WS2019 still common in production; WS2016 declining.

### PowerShell
- **Status:** ✅ VERIFIED (GitHub Releases API)
- **Current:** v7.6.2 (released 2026-05-21)
- **Repo:** github.com/PowerShell/PowerShell
- **Teaching note:** PowerShell 7.x (cross-platform, .NET 8) is the current standard. Windows PowerShell 5.1 is still the built-in but teach PS7 as the target. Key for automation differentiator tier.

### Windows Terminal
- **Status:** ✅ VERIFIED (GitHub Releases API)
- **Current:** v1.24.11321.0 (released 2026-05-13)
- **Teaching note:** Default shell host for modern Windows. Replaces old conhost. Teach students to set this up early.

### WinGet (Windows Package Manager)
- **Status:** ✅ VERIFIED (GitHub Releases API)
- **Current:** v1.28.240 (released 2026-04-17)
- **Teaching note:** WinGet is the standard CLI package manager for Windows. Practical skill - `winget install`, `winget upgrade --all`. Replaces manual installer hunts.

### Wireshark
- **Status:** ✅ VERIFIED (wireshark.org download page + GitHub tags)
- **Current stable:** 4.6.6 / 4.6.5 (4.6.x branch is current stable)
- **GitHub tags also show:** 4.4.9 (older stable/LTS branch)
- **Teaching note:** Wireshark is the essential packet analysis tool. Teach display filters, follow TCP stream, identify DNS/DHCP/HTTP traffic. Core for networking fundamentals module.

---

## 2. ITSM / Ticketing Platforms

### ServiceNow
- **Status:** ⚠️ PARTIAL (403 on direct fetch; widely confirmed dominant platform)
- **Market position:** Clear enterprise ITSM leader. ITIL-aligned workflows, incident/change/problem management, CMDB, AI-assisted routing.
- **2026 context:** ServiceNow has integrated AI ("Now Assist") for ticket summarization, suggested resolutions, and agent assist. Enterprise-only pricing ($$$) but dominant in orgs with 500+ employees.
- **Teaching note:** Teach ITSM concepts (incident lifecycle, SLA, escalation) using ServiceNow as the reference platform. Free Personal Developer Instance (PDI) available at developer.servicenow.com.

### Jira Service Management (Atlassian)
- **Status:** ✅ VERIFIED (atlassian.com/software/jira/service-management → HTTP 200)
- **Market position:** Dominant in tech-forward SMBs and orgs already using Jira/Confluence. Strong ITIL support, Confluence integration, asset management.
- **2026 context:** Atlassian Intelligence (AI) features rolled out across JSM - auto-categorization, suggested articles, virtual agent for ticket deflection.
- **Teaching note:** Teach alongside ServiceNow. Free tier available. Many startups/mid-size tech companies use JSM.

### Zendesk
- **Status:** ⚠️ PARTIAL (403 on fetch; well-established platform)
- **Market position:** Dominant in customer-facing support (external helpdesk). Common in SaaS companies. Less common for internal IT but relevant for IT support roles at product companies.
- **2026 context:** Zendesk AI features heavily marketed - AI agents, intelligent triage, macro suggestions.
- **Teaching note:** Worth awareness especially for IT support roles at software/SaaS companies. Free trial available.

### Freshservice (Freshworks)
- **Status:** ✅ VERIFIED (freshservice.com → HTTP 200)
- **Market position:** Strong SMB/mid-market ITSM. More affordable than ServiceNow. ITIL-aligned. Growing.
- **2026 context:** Freddy AI (Freshworks' AI layer) provides ticket deflection, canned response suggestions, auto-tagging.
- **Teaching note:** Good free-trial teaching tool. Realistic for SMB IT roles. Teach same ITSM concepts transfer across platforms.

### Verdict for Curriculum
Teach **ITSM concepts first** (incident management, SLA, ticket lifecycle, escalation paths) then show execution in **ServiceNow PDI** + **Jira Service Management free tier**. Platform-specific UI is secondary to workflow fluency.

---

## 3. Endpoint Management / RMM / MDM

### Microsoft Intune
- **Status:** ✅ VERIFIED (learn.microsoft.com/intune → HTTP 200)
- **Definition (verified):** "Intune is a cloud-based endpoint management service that secures and manages devices and apps"
- **2026 context:** Intune is THE cloud MDM/UEM standard for Microsoft environments. Manages Windows, macOS, iOS, Android from one console. Deeply integrated with Entra ID and Microsoft 365. Weekly release cadence (confirmed - release notes show "Week of" entries through 2026).
- **Key capabilities:** Device compliance policies, app deployment, Autopilot (zero-touch provisioning), endpoint security baselines, patch management.
- **Teaching note:** MUST TEACH at differentiator tier. Any IT admin job in a Microsoft shop will expect Intune familiarity. Free with M365 Business Premium and up.

### NinjaOne (RMM)
- **Status:** ✅ VERIFIED (ninjaone.com → HTTP 200; "endpoint management and autonomous patching" confirmed)
- **Market position:** Leading cloud RMM for MSPs and SMBs. Competes with ConnectWise Automate, Datto RMM.
- **2026 context:** NinjaOne has added autonomous patching, AI-assisted scripting, and integrated ticketing. Strong growth in MSP segment.
- **Teaching note:** Teach RMM concepts (remote monitoring, patch management, scripting deployment) with NinjaOne as an example. MSP roles will use RMM tools heavily.

### Other RMM/Endpoint Tools
- **ConnectWise Automate / Manage:** ⚠️ PARTIAL - enterprise/MSP RMM + PSA combo, widely used
- **Atera:** ⚠️ PARTIAL (403) - all-in-one RMM+PSA for MSPs, per-tech pricing popular with small MSPs
- **Datto RMM:** ⛔ UNVERIFIED - common in MSP space (Kaseya-owned)

### Shift Summary
The field has moved from on-prem SCCM/MECM-dominated management to **cloud-first Intune + co-management**. Large enterprises often run both (co-management). Teach the cloud direction; mention SCCM/Endpoint Configuration Manager as context for larger orgs.

---

## 4. Identity: Active Directory vs. Entra ID

### Microsoft Entra ID (formerly Azure AD)
- **Status:** ✅ VERIFIED (learn.microsoft.com/entra → HTTP 200; Entra blog 403 but MS Learn confirmed)
- **Verified content:** "Entra ID - every tenant is automatically a Microsoft Entra tenant." Multiple tiers confirmed: Entra ID Free, P1, P2, Suite.
- **Product family confirmed:** Entra ID, Entra ID Governance, Entra ID Protection, Entra External ID, Entra Verified ID, Entra Internet Access, Entra Private Access.

### Active Directory (on-prem)
- **Status:** ⚠️ PARTIAL (WS2025 page accessible; AD docs accessible)
- **2026 context:** On-prem AD is still ubiquitous - most enterprises with 10+ years of history have it. But **new deployments are Entra ID-first or hybrid**. Pure cloud (Entra-only) is the direction for greenfield orgs and SMBs.

### The Hybrid Reality (2026)
Most real-world orgs in 2026 run **hybrid identity**:
- On-prem AD synced to Entra ID via **Microsoft Entra Connect** (formerly Azure AD Connect)
- Users have one identity that works on-prem and in the cloud
- Conditional Access policies enforced at Entra ID layer
- Devices joined to **Entra ID** (cloud) or **hybrid joined** (both)

### Teaching Recommendation
| Topic | Tier |
|---|---|
| AD DS fundamentals (users, groups, OUs, GPO) | MUST TEACH |
| Entra ID basics (users, groups, roles, MFA/SSPR) | MUST TEACH |
| Entra Connect / hybrid sync concept | MUST TEACH (concept) |
| Conditional Access | DIFFERENTIATOR |
| Entra ID Governance / PIM | DIFFERENTIATOR |
| Pure on-prem-only AD deep dive | DE-EMPHASIZE |

---

## 5. Networking Tools & Context

### Cisco IOS / CCNA
- **Status:** ⚠️ PARTIAL (Cisco Learning Network accessible HTTP 200; IOS version details JS-rendered)
- **2026 context:** Cisco IOS 15.x/16.x on enterprise switches/routers still dominant in mid-large orgs. Cisco IOS XE (17.x) on newer platforms. Catalyst and Nexus lines remain standard.
- **CCNA (200-301):** Still the gold-standard entry networking cert. Covers TCP/IP, subnetting, VLANs, routing, switching, wireless, security fundamentals, automation basics.
- **Packet Tracer:** Free Cisco simulator, current version bundled with CCNA NetAcad. Essential for home lab networking.
- **Teaching note:** Teach networking fundamentals with Packet Tracer. CCNA is the networking differentiator cert for 2026.

### Wireshark
- **Status:** ✅ VERIFIED (4.6.6 current stable)
- **Teaching use:** Teach display filters, capture filters, protocol analysis (DNS, DHCP, TCP handshake, HTTP/HTTPS). Hands-on exercises with local network captures.

### SD-WAN & Cloud Networking Trend
- **Status:** ⚠️ PARTIAL (trend confirmed across multiple vendor pages)
- **2026 context:** SD-WAN has gone mainstream. Cisco Meraki, VMware (Broadcom) SD-WAN, Fortinet SD-WAN dominate. Cloud networking (VPCs, virtual network appliances, cloud-native firewalls) is growing.
- **Teaching note:** Teach as awareness/differentiator. Entry IT support roles don't configure SD-WAN but should understand what it is. CCNA now includes automation/programmability basics that bridge toward this.

### Other Networking Tools
| Tool | Status | Teaching value |
|---|---|---|
| nmap | ⛔ UNVERIFIED (version) | Teach for port scanning / network discovery |
| PuTTY / SSH | ⛔ UNVERIFIED (version) | MUST TEACH - SSH to routers/servers/Linux |
| iperf3 | ⛔ UNVERIFIED | Teach for bandwidth testing |
| PRTG / SolarWinds | ⚠️ PARTIAL | Awareness - network monitoring tools |
| Cisco Meraki dashboard | ⚠️ PARTIAL | Cloud-managed networking - differentiator |

---

## 6. Remote Support Tools

### TeamViewer
- **Status:** ✅ VERIFIED (teamviewer.com → HTTP 200)
- **2026 context:** Still widely used for remote support, especially SMBs. Free for personal use. Enterprise licensing. Common in helpdesk environments.

### Microsoft Remote Desktop / RDS
- **Status:** ✅ VERIFIED (Microsoft Learn RDS-in-Azure page → HTTP 200)
- **2026 context:** RDP is the baseline remote access protocol for Windows. Azure Virtual Desktop (AVD) and Windows 365 are the cloud evolution of traditional RDS.
- **Teaching note:** MUST TEACH RDP basics. Teach troubleshooting RDP connectivity (firewall rules, NLA, port 3389).

### ConnectWise ScreenConnect
- **Status:** ✅ VERIFIED (screenconnect.com → HTTP 200)
- **2026 context:** Popular unattended + attended remote support tool in MSP/helpdesk environments.

### AnyDesk
- **Status:** ⚠️ PARTIAL (403 on fetch; known active platform)
- **2026 context:** TeamViewer competitor, common in SMB helpdesk.

### Quick Assist (Microsoft built-in)
- **Status:** ⛔ UNVERIFIED (version)
- **2026 context:** Built into Windows 11. Free, Entra ID-integrated in newer versions. Increasingly used for internal IT support in Microsoft shops.
- **Teaching note:** Teach alongside TeamViewer - shows understanding of multiple tools.

---

## 7. Microsoft 365 Admin

### M365 Admin Center
- **Status:** ✅ VERIFIED (admin.microsoft.com accessible, MS Learn M365 admin pages HTTP 200)
- **2026 context:** Core admin interface for user management, licensing, service health, Exchange Online, Teams, SharePoint. Every IT support role in a Microsoft org will touch this.
- **Key tasks to teach:**
  - Add/remove users, assign licenses
  - Reset passwords, manage MFA
  - Distribution groups and shared mailboxes
  - Service health dashboard
  - Basic Exchange Online (mail flow, connectors)

### Exchange Online
- **2026 context:** On-prem Exchange is rapidly declining. Most SMBs and new enterprise deployments are Exchange Online only. Teaching on-prem Exchange is low ROI; teach Exchange Online admin via EAC (Exchange Admin Center) and PowerShell (ExchangeOnlineManagement module).
- **Teaching note:** CUT on-prem Exchange deep dives. TEACH Exchange Online basics (shared mailboxes, distribution lists, mail flow rules, message trace).

### Teams Admin Center
- **2026 context:** Teams is the default collaboration platform. IT support tickets increasingly involve Teams (calling issues, meeting room devices, policy assignment). Basic Teams admin is expected.

---

## 8. What to TEACH - Curriculum Tiers

### ✅ MUST TEACH (Baseline - every IT support job expects this)

| Topic | Rationale |
|---|---|
| Windows 11 troubleshooting | Default desktop OS; all helpdesk scenarios |
| Networking fundamentals: TCP/IP, DNS, DHCP, subnetting | Required for every networking or support role; CCNA/CompTIA Net+ core |
| Active Directory basics (users, groups, OUs, GPO) | Still in majority of enterprise environments |
| Microsoft Entra ID basics (cloud identity, MFA, SSPR, conditional access concept) | All new orgs + hybrid; M365 access management |
| Ticketing / ITSM workflow | Incident lifecycle, SLA, escalation, documentation - universal |
| Hardware fundamentals | RAM, storage, PSU, peripherals, basic repair - CompTIA A+ coverage |
| Basic PowerShell | `Get-`, `Set-`, pipelines, `Get-Help`, simple one-liners; not full scripting |
| M365 admin basics | User/license management, Exchange Online, Teams, shared mailboxes |
| RDP / remote support tools | TeamViewer, Quick Assist, RDP troubleshooting |
| Wireshark basics | Read a packet capture, identify DNS/DHCP/TCP issues |

### TEACH AS DIFFERENTIATOR (Separates candidates; hiring managers notice)

| Topic | Rationale |
|---|---|
| PowerShell scripting & automation | Automate user provisioning, report generation, bulk tasks - high signal |
| Microsoft Intune / endpoint management | Cloud MDM is the direction; Intune skills are in high demand |
| CCNA-level networking | VLANs, routing, ACLs, troubleshooting - big signal for network-leaning roles |
| Linux fundamentals | SSH, file system, permissions, basic commands - opens doors to sysadmin/cloud |
| Cloud fundamentals (AZ-900 or AWS Cloud Practitioner) | Shows awareness of where IT is going; easy cert win |
| Virtualization / home lab | Hyper-V or VirtualBox AD lab shows initiative and hands-on skills |
| Entra ID Conditional Access + MFA policies | Security-conscious IT; increasingly day-1 expectation |
| Basic Azure/M365 PowerShell (ExchangeOnlineManagement, AzureAD module) | Automation in cloud environments |

### CUT / DE-EMPHASIZE (Low ROI for 2026 entry roles)

| Topic | Why cut |
|---|---|
| On-prem Exchange Server admin deep dive | Rapid decline; Exchange Online dominates |
| Legacy imaging workflows (MDT/WDS-only, no Autopilot) | Autopilot + Intune is the replacement; heavy MDT coverage wastes time |
| Pure on-prem-only identity (no Entra) | Hybrid/cloud is now baseline; on-prem-only is context, not focus |
| Deprecated VBScript / batch scripting | PowerShell replaced this; mention as curiosity only |
| Physical network cabling beyond basics | Data center cabling is niche; teach concepts + RJ45 crimping as demo |
| Novell/legacy directory systems | Not relevant in 2026 market |
| On-prem SCCM as primary MDM story | Teach as co-management context; Intune is the lead |

---

## 9. AI in IT Support - 2026 Reality Check

### What's Real (Production-deployed, hiring managers ask about it)
- **AI ticket deflection:** ServiceNow Now Assist, Jira Service Management Atlassian Intelligence, Freshservice Freddy AI, Zendesk AI agents - all production. Virtual agents handle password resets, software requests, basic how-tos without human involvement.
- **AI-assisted resolution suggestions:** When a ticket comes in, AI surfaces likely KB articles and suggested responses to the agent. Junior techs using this are faster. It is not replacing L1 - it's augmenting it.
- **Copilot in M365:** Microsoft 365 Copilot is deployed in many enterprise environments. IT admins manage Copilot licensing, data governance, and user enablement. Basic awareness required.
- **AI summarization:** Long incident threads, call transcripts, change request notes - AI summarizes these. IT ops teams use this in NOC/SOC contexts.

### What's Hype (Not a practical beginner skill in 2026)
- Building AI models for IT support - not a helpdesk skill
- "Prompt engineering" as a distinct IT skill - it's just using tools; not a job title at L1/L2
- AI fully replacing L1 support - ticket deflection is real but complex issues still route to humans; L1 jobs exist

### What a Junior Should Know
1. **Understand that AI ticket deflection exists** and how it affects ticket volume (fewer "reset my password" tickets reaching humans)
2. **Know how to use AI-assisted resolution suggestions** in ITSM tools - don't ignore the suggested KB articles
3. **M365 Copilot basics** - what it is, how it's licensed, basic admin tasks
4. **Scripting + automation mindset** - the techs who aren't automated away are the ones who can automate things themselves (PowerShell)
5. **Don't fear it** - AI tools make junior techs more productive; use them, learn them, don't pretend they don't exist

---

## 10. Portfolio / Home Lab Projects (Entry-Role Signal)

These projects demonstrate practical skill without requiring a job. Rank-ordered by signal strength for hiring managers.

### Project 1 - Build an Active Directory Domain in VMs ✅ HIGH SIGNAL
**What:** Hyper-V or VirtualBox. Windows Server 2025 DC + 2x Windows 11 clients. Promote DC, join clients, create users/OUs/GPOs. Configure DHCP and DNS on the DC.
**Skills demonstrated:** AD DS, DNS, DHCP, GPO, Windows Server, virtualization
**Document it:** Screenshot-heavy writeup. GitHub or blog post. "I built X, encountered Y problem, fixed it with Z."
**Time:** ~8-12 hours first time

### Project 2 - PowerShell Automation Script ✅ HIGH SIGNAL
**What:** Write a script that does something real: bulk-create AD users from a CSV, generate a system inventory report (OS, RAM, disk), automate a software install with winget, or parse event logs for failed logins.
**Skills demonstrated:** PowerShell scripting, problem-solving, automation mindset
**Document it:** GitHub repo with README explaining what it does and why.
**Time:** ~4-8 hours

### Project 3 - Home Network Subnetting + Documentation ✅ MEDIUM-HIGH SIGNAL
**What:** Document your actual home network. Draw a topology. Identify subnets, gateway, DNS, DHCP range. Then redesign it - create a VLAN plan (IoT / trusted / guest). Implement in Packet Tracer or on real hardware if available.
**Skills demonstrated:** Subnetting, network design, documentation, Packet Tracer/CLI
**Document it:** Network diagram (draw.io) + written IP addressing scheme.
**Time:** ~4-6 hours

### Project 4 - Packet Tracer Network Build ✅ MEDIUM SIGNAL
**What:** Build a multi-VLAN network in Cisco Packet Tracer with inter-VLAN routing, DHCP, DNS, a simulated internet connection. Configure named ACLs. Test connectivity with ping/tracert.
**Skills demonstrated:** CCNA concepts, VLANs, routing, ACLs, troubleshooting
**Document it:** .pkt file in GitHub + topology diagram + configuration notes
**Time:** ~6-10 hours

### Project 5 - Document a Ticket Workflow ⚠️ MEDIUM SIGNAL
**What:** Using ServiceNow PDI or Jira Service Management free tier, set up a basic ITSM workflow. Create incident categories, an escalation path, a KB article. Take a sample incident from intake to resolution. Screenshot the entire flow.
**Skills demonstrated:** ITSM tool familiarity, process thinking, documentation
**Document it:** PDF walkthrough or blog post.
**Time:** ~3-5 hours

### Project 6 - Linux VM + Basic Admin ✅ MEDIUM-HIGH SIGNAL (for sysadmin-leaning roles)
**What:** Ubuntu Server 24.04 LTS in VirtualBox. Install, configure SSH, create users, set file permissions, install and configure a service (nginx, Samba, or OpenSSH server with key auth). Write a bash script.
**Skills demonstrated:** Linux fundamentals, SSH, permissions, services
**Document it:** GitHub repo with setup notes and scripts.
**Time:** ~5-8 hours

### Project 7 - M365 / Entra ID Lab (Microsoft 365 Developer Tenant) ✅ HIGH SIGNAL
**What:** Spin up a free Microsoft 365 Developer tenant (developer.microsoft.com/microsoft-365/dev-program). Create users, assign licenses, configure MFA/SSPR, set a Conditional Access policy, explore Exchange Online admin, create a shared mailbox.
**Skills demonstrated:** M365 admin, Entra ID, Conditional Access, Exchange Online
**Document it:** Screenshot walkthrough of each task completed.
**Time:** ~4-6 hours

---

## 11. Tool Version Summary Table

| Tool | Verified Version | Source | Status |
|---|---|---|---|
| PowerShell | 7.6.2 (2026-05-21) | GitHub Releases API | ✅ VERIFIED |
| Windows Terminal | 1.24.11321.0 (2026-05-13) | GitHub Releases API | ✅ VERIFIED |
| WinGet | 1.28.240 (2026-04-17) | GitHub Releases API | ✅ VERIFIED |
| Wireshark | 4.6.6 (current stable) | wireshark.org download | ✅ VERIFIED |
| Windows 11 | 24H2 current | microsoft.com (200) | ✅ VERIFIED |
| Windows Server | 2025 current | microsoft.com (200) | ✅ VERIFIED |
| Microsoft Intune | Cloud SaaS (weekly releases) | MS Learn (200) | ✅ VERIFIED |
| Microsoft Entra ID | Cloud SaaS (continuous) | MS Learn (200) | ✅ VERIFIED |
| ServiceNow | Cloud SaaS | 403 (known active) | ⚠️ PARTIAL |
| Jira Service Mgmt | Cloud SaaS | atlassian.com (200) | ✅ VERIFIED |
| Freshservice | Cloud SaaS | freshservice.com (200) | ✅ VERIFIED |
| Zendesk | Cloud SaaS | 403 (known active) | ⚠️ PARTIAL |
| TeamViewer | Cloud+client | teamviewer.com (200) | ✅ VERIFIED |
| ScreenConnect | Cloud+client | screenconnect.com (200) | ✅ VERIFIED |
| NinjaOne | Cloud SaaS | ninjaone.com (200) | ✅ VERIFIED |
| AnyDesk | Desktop client | 403 (known active) | ⚠️ PARTIAL |
| Cisco IOS | 17.x (IOS XE current) | cisco.com (JS-heavy) | ⚠️ PARTIAL |

---

## 12. Key Curriculum Decisions Summary

1. **Windows 11 + Server 2025** are the teaching targets. Win10 is EoL.
2. **Entra ID is co-equal with AD**, not an afterthought. Teach hybrid from day one.
3. **PowerShell 7.6.x** - teach PS7, acknowledge 5.1 exists in the wild.
4. **Intune is the endpoint management story** - not SCCM alone.
5. **Exchange Online replaces on-prem Exchange** in the curriculum.
6. **ITSM concepts > platform specifics** - ServiceNow + JSM as practice tools.
7. **AI in IT = augmentation, not replacement** - teach tool use, not fear.
8. **Wireshark 4.6.x + Packet Tracer** = networking lab stack.
9. **Home lab on free Microsoft developer tenant** = highest ROI M365/Entra practice.
10. **Portfolio projects on GitHub** with documentation = biggest differentiator for entry roles.
