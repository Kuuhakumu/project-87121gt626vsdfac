# Goal 2: core support skills meow

> **~160h total** - your pace, no deadline.
> this is what support roles do all day: identity, tickets, M365, networking depth.

[Previous: Goal 1](01-foundations.md) - [Hub](README.md) - [Next: Goal 3](03-specialization.md)

---

- [ ] **identity: Active Directory + Entra ID** (~50h)
- [ ] **ticketing, ITSM, support workflow** (~50h)
- [ ] **M365 admin + networking depth** (~60h)
- [ ] **exit check** - AD/Entra tasks, AD lab, ITSM, M365/Intune, VLANs/Wireshark

## identity - Active Directory + Entra ID (~50h)

in 2026, identity is hybrid. on-prem Active Directory still runs many enterprises; Entra ID is where cloud identity lives. u need both.

- [ ] AD domains, OUs, users, groups, GPO basics
- [ ] Entra ID users, groups, roles
- [ ] hybrid identity: AD sync to Entra ID
- [ ] daily tasks: create/disable users, reset passwords, groups, unlock accounts
- [ ] MFA, SSO, conditional access basics
- [ ] "i cant log in" causes: locked, expired, wrong OU, MFA, sync delay

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [AD home lab in VMs](https://www.virtualbox.org) | Local | domain controller + Windows 11 client | **Free** |
| [Free M365 Dev Tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | Entra ID tenant practice | **Free** |
| [Microsoft Learn: Identity](https://learn.microsoft.com/en-us/training/) | Official | Entra ID / AD paths | **Free** |

build the AD lab. a domain controller + client VM maps directly to real help-desk work.

## ticketing, ITSM, and support workflow (~50h)

the job runs through tickets. workflow makes u hireable.

- [ ] ticket lifecycle: intake -> triage -> categorize -> resolve -> document -> close
- [ ] incident vs request vs problem vs change
- [ ] SLAs, P1-P4, response vs resolution time
- [ ] ServiceNow, Jira Service Management, Freshservice/Zendesk awareness
- [ ] clear ticket notes and knowledge-base articles
- [ ] remote support etiquette
- [ ] customer communication

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [ServiceNow free dev instance](https://developer.servicenow.com) | ServiceNow | real PDI to learn ticketing | **Free** |
| Ticket lifecycle write-up | Self | intake -> close portfolio piece | **Free** |

AI handles some simple tickets. dont be only a ticket-closer; own escalation, document well, and build scripting/identity skill.

## M365 admin and networking depth (~60h)

### M365 administration

- [ ] M365 Admin Center: licenses, users, mailbox basics, Teams/SharePoint
- [ ] Exchange Online: mailbox management, distribution lists
- [ ] Intune / endpoint management: enrollment, compliance policies, app deployment
- [ ] Autopilot: zero-touch provisioning

### networking depth

- [ ] VLANs and switching
- [ ] routing basics and default gateway
- [ ] firewalls and NAT
- [ ] Wireshark packet reading
- [ ] VPNs and remote access

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Intune in M365 dev tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | enroll test device, push policy | **Free** |
| [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco | VLANs + inter-VLAN routing | **Free** |
| [Wireshark](https://www.wireshark.org) | Local | capture and read traffic | **Free** |

## exit check

- [ ] can create/disable users and reset passwords in AD and Entra ID
- [ ] built working AD domain lab
- [ ] understand ticket lifecycle and ITSM vocabulary
- [ ] hands-on time in ServiceNow or another ITSM tool
- [ ] can do basic M365 admin and enroll a device in Intune
- [ ] can build VLANs in Packet Tracer and read Wireshark capture
- [ ] on track for or passed **A+ Core 2** and progressing toward **Network+**

[Next: Goal 3 - Specialize](03-specialization.md)
