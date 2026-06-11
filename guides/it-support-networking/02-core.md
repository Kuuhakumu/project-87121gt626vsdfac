# 🛠️ Phase 2: Core Support Skills

> **~160 hrs total** · your pace, no deadline
> This is what you actually do all day in a support role: manage identities, resolve tickets, administer M365, and go deeper on networking. Most of **A+ Core 2** and **Network+** lives here.

[← Phase 1](01-foundations.md) · [Hub](README.md) · [Next: Phase 3 →](03-specialization.md)

---

## Identity — Active Directory + Entra ID (~50 hrs)

In 2026, identity is hybrid. On-prem Active Directory still runs most enterprises, but cloud identity (Entra ID, formerly Azure AD) is where everything's heading. **You need to know both.**

### What to cover
- **Active Directory (on-prem):** domains, OUs, users, groups, group policy (GPO) basics
- **Entra ID (cloud):** users, groups, roles, the difference from on-prem AD
- **Hybrid identity:** how AD syncs to Entra ID — the reality at most companies
- **Daily tasks:** create/disable users, reset passwords, manage group membership, unlock accounts
- **Authentication:** MFA, SSO, conditional access basics
- **The #1 help-desk ticket:** "I can't log in" — know every cause (locked, expired, wrong OU, MFA, sync delay)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [AD home lab in VMs](https://www.virtualbox.org) | Local | Stand up a domain controller + Win11 client | **Free** |
| [Free M365 Dev Tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | Real Entra ID tenant to practice in | **Free** |
| [Microsoft Learn: Identity](https://learn.microsoft.com/en-us/training/) | Official | Guided Entra ID / AD paths | **Free** |

> **Build the AD lab.** A domain controller + a client VM you stood up yourself is the single most impressive thing a help-desk candidate can show. It maps 1:1 to the job.

---

## Ticketing, ITSM & support workflow (~50 hrs)

The job runs through tickets. Knowing the workflow — not just the tech — is what makes you hireable and promotable.

### What to cover
- **The ticket lifecycle:** intake → triage → categorize → resolve → document → close
- **ITSM concepts:** incident vs request vs problem vs change (ITIL basics — worth knowing the vocabulary)
- **SLAs & prioritization:** P1–P4, response vs resolution time
- **Ticketing tools:** ServiceNow (enterprise leader), Jira Service Management (tech shops), Freshservice/Zendesk (SMB/MSP)
- **Documentation:** writing a clear ticket note, building a knowledge-base article
- **Remote support:** RMM tools, remote sessions, the etiquette of taking over someone's screen
- **Customer communication:** the soft skill that gets you promoted — calm, clear, empathetic

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [ServiceNow free dev instance](https://developer.servicenow.com) | ServiceNow | Real PDI to learn the enterprise leader | **Free** |
| Ticket lifecycle write-up | Self | Document a full intake→close as a portfolio piece | **Free** |

> **AI is deflecting simple tickets.** Password-reset bots and self-service portals handle routine T1 volume now. The move: don't be a pure ticket-closer — own the escalation path, document well, and build the scripting/identity skills that AI can't replace.

---

## M365 admin & networking depth (~60 hrs)

### Microsoft 365 administration
- **M365 Admin Center:** licenses, users, mailbox basics, Teams/SharePoint admin
- **Exchange Online:** mailbox management, distribution lists (cloud, not legacy on-prem Exchange)
- **Intune / endpoint management:** device enrollment, compliance policies, app deployment — **this is the modern replacement for imaging/SCCM**
- **Autopilot:** zero-touch device provisioning (the modern way devices get set up)

### Networking depth (toward Network+)
- **VLANs & switching:** segmenting a network, trunk vs access ports
- **Routing basics:** static routes, default gateway, how traffic crosses networks
- **Firewalls & NAT:** how a private network reaches the internet
- **Network troubleshooting:** **Wireshark** basics — actually see the packets
- **VPNs & remote access:** site-to-site vs client VPN concepts

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Intune in M365 dev tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | Enroll a test device, push a policy | **Free** |
| [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco | Build VLANs + inter-VLAN routing | **Free** |
| [Wireshark](https://www.wireshark.org) | Local | Capture & read real network traffic | **Free** |

---

## Phase 2 exit checklist
- [ ] Can create/disable users and reset passwords in **both** AD and Entra ID
- [ ] Built a working AD domain lab (DC + client)
- [ ] Understand the full ticket lifecycle and ITSM vocabulary
- [ ] Have hands-on time in ServiceNow (or another ITSM tool)
- [ ] Can do basic M365 admin and enroll a device in Intune
- [ ] Can build VLANs in Packet Tracer and read a packet capture in Wireshark
- [ ] On track for (or passed) **A+ Core 2** and progressing toward **Network+**

Next: [Phase 3 — Specialize →](03-specialization.md)
