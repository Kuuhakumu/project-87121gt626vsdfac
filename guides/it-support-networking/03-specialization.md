# 🎯 Phase 3: Pick Your Track

> **~140 hrs total** · your pace, no deadline
> You have the shared support base. Now pick **one** direction to go deeper — this is what turns a help-desk job into a *career* and decides your pivot.

[← Phase 2](02-core.md) · [Hub](README.md) · [Next: Phase 4 — Home Lab & Portfolio →](04-homelab-portfolio.md)

---

## Which track? (where each one leads)

| Track | You'll grow toward | Pick if you like… |
|---|---|---|
| **Networking** | Network Admin → Network Engineer | Routers, switches, packet flow, infrastructure |
| **Sysadmin / Identity** | Sysadmin → Cloud/M365 Admin | Servers, AD/Entra, automation, the Windows ecosystem |
| **Cloud / Identity pivot** | Cloud Support → Cloud Engineer | Azure/AWS, scaling out of pure support |

> You don't have to choose forever. All three build on the same A+/Net+ base, and help desk → any of these is a normal move. Pick the one that excites you and go deep enough to interview for it.

---

## Track A: Networking (CCNA path)

**Goal:** understand and configure networks at real professional depth.

### What to cover
- Subnetting until it's automatic (VLSM, CIDR) — interviewers *will* test this
- Routing: static + dynamic (OSPF basics), inter-VLAN routing
- Switching: VLANs, trunking, STP, EtherChannel
- Network services: DNS, DHCP, NAT at depth
- Network security: ACLs, port security
- **CCNA** (200-301) is the gold-standard networking cert

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco | Build & configure full multi-router topologies | **Free** |
| [GNS3](https://www.gns3.com) | Local | Emulate real network gear | **Free** |
| [Professor Messer / CCNA content](https://www.professormesser.com) | Web | Free structured networking training | **Free** |

**Cert:** Cisco CCNA (200-301).

---

## Track B: Sysadmin / Identity (PowerShell + Windows)

**Goal:** administer servers, identities, and endpoints — and automate the repetitive parts.

### What to cover
- **PowerShell scripting** (the differentiator): variables, loops, pipelines, bulk AD/Entra tasks, scheduled scripts
- Windows Server: roles, GPO depth, file/print, DNS/DHCP servers
- **Intune / Autopilot** at depth — modern endpoint management
- Patch management, backups, disaster-recovery basics
- Hybrid identity: AD Connect / Entra Connect sync

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [PowerShell home lab](https://www.virtualbox.org) | Local | Automate bulk user creation, disk reports | **Free** |
| [Microsoft Learn: PowerShell](https://learn.microsoft.com/en-us/training/) | Official | Guided scripting paths | **Free** |
| [Free M365 Dev Tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | Real Intune/Entra automation | **Free** |

**Cert:** MD-102 (Endpoint Administrator) + AZ-900.

---

## Track C: Cloud / Identity pivot

**Goal:** use support as a launchpad into cloud — the highest-growth direction from here.

### What to cover
- **Azure** (AZ-900 → AZ-104) or **AWS** (Cloud Practitioner → SysOps) fundamentals
- Cloud identity: Entra ID at depth, conditional access, RBAC
- Cloud endpoint & device management (Intune)
- Basic scripting + automation (PowerShell / CLI)
- Networking in the cloud (VNets, NSGs) — your Net+ knowledge transfers

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Microsoft Learn sandboxes](https://learn.microsoft.com/en-us/training/) | Microsoft | Free Azure sandbox, no card | **Free** |
| [Azure free account](https://azure.microsoft.com/free/) | Azure | Real cloud resources, free tier | Free tier |
| [Free M365 Dev Tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | Identity + endpoint practice | **Free** |

**Cert:** AZ-900 → AZ-104 (or AWS CLF-C02). See the **[Cloud & DevOps guide](../cloud-devops/)** if you want to fully commit to this path.

---

## Phase 3 exit checklist
- [ ] Chose **one** track and can explain why it fits you
- [ ] Reached working competence in that track's signature skill (subnetting / PowerShell / Azure)
- [ ] Completed the track's hands-on labs
- [ ] Identified the cert that matches your track
- [ ] Have a concrete idea for your home-lab portfolio centerpiece (built in Phase 4)

Next: [Phase 4 — Home Lab & Portfolio →](04-homelab-portfolio.md)
