# Goal 3: pick your track meow

> **~140h total** - your pace, no deadline.
> u have the shared support base. now pick **one** direction to go deeper.

[Previous: Goal 2](02-core.md) - [Hub](README.md) - [Next: Goal 4](04-homelab-portfolio.md)

---

- [ ] **choose a track**
- [ ] **Track A: networking**
- [ ] **Track B: sysadmin / identity**
- [ ] **Track C: cloud / identity pivot**
- [ ] **exit check** - one track chosen, signature skill, labs done, cert chosen, home-lab idea ready

## choose a track

| Track | Youll grow toward | Pick if u like... |
|---|---|---|
| **Networking** | Network Admin -> Network Engineer | routers, switches, packet flow |
| **Sysadmin / Identity** | Sysadmin -> Cloud/M365 Admin | servers, AD/Entra, automation |
| **Cloud / Identity pivot** | Cloud Support -> Cloud Engineer | Azure/AWS and scaling beyond support |

u dont choose forever. all three build on the same A+/Net+ base.

## Track A: networking (CCNA path)

**goal:** understand and configure networks at professional depth.

- [ ] subnetting until automatic: VLSM, CIDR
- [ ] routing: static + OSPF basics, inter-VLAN
- [ ] switching: VLANs, trunking, STP, EtherChannel
- [ ] DNS, DHCP, NAT at depth
- [ ] ACLs and port security
- [ ] **CCNA 200-301**

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco | multi-router topologies | **Free** |
| [GNS3](https://www.gns3.com) | Local | emulate real network gear | **Free** |
| Professor Messer / CCNA content | Web | networking training | **Free** - **⚠️ TODO verify exact CCNA resource** |

**cert:** Cisco CCNA (200-301).

## Track B: sysadmin / identity

**goal:** administer servers, identities, endpoints, and automate repetitive work.

- [ ] PowerShell scripting: variables, loops, pipelines, bulk AD/Entra tasks
- [ ] Windows Server roles, GPO depth, file/print, DNS/DHCP servers
- [ ] Intune / Autopilot depth
- [ ] patch management, backups, DR basics
- [ ] hybrid identity: AD Connect / Entra Connect sync

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [PowerShell home lab](https://www.virtualbox.org) | Local | bulk user creation, disk reports | **Free** |
| [Microsoft Learn: PowerShell](https://learn.microsoft.com/en-us/training/) | Official | scripting paths | **Free** |
| [Free M365 Dev Tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | Intune/Entra automation | **Free** |

**cert:** MD-102 + AZ-900.

## Track C: cloud / identity pivot

**goal:** use support as a launchpad into cloud.

- [ ] Azure AZ-900 -> AZ-104 or AWS CLF-C02 path
- [ ] Entra ID depth, conditional access, RBAC
- [ ] Intune endpoint/device management
- [ ] PowerShell / CLI automation
- [ ] cloud networking: VNets, NSGs

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Microsoft Learn sandboxes](https://learn.microsoft.com/en-us/training/) | Microsoft | Azure sandbox, no card | **Free** |
| [Azure free account](https://azure.microsoft.com/free/) | Azure | real cloud resources | Free tier |
| [Free M365 Dev Tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | identity + endpoint practice | **Free** |

**cert:** AZ-900 -> AZ-104 or AWS CLF-C02. see the [Cloud & DevOps guide](../cloud-devops/) if u fully commit to cloud.

## exit check

- [ ] chose **one** track and can explain why
- [ ] reached working competence in subnetting / PowerShell / Azure
- [ ] completed the track hands-on labs
- [ ] identified the cert matching your track
- [ ] have a concrete home-lab portfolio idea for Goal 4

[Next: Goal 4 - Home Lab & Portfolio](04-homelab-portfolio.md)
