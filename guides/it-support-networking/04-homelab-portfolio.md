# Goal 4: home lab and portfolio meow

> **~100h total** - your pace, no deadline.
> in IT support, a documented home lab is your portfolio.

[Previous: Goal 3](03-specialization.md) - [Hub](README.md) - [Next: Goal 5](05-job-hunt.md)

---

- [ ] **understand why home lab beats cert alone**
- [ ] **build the Windows domain lab**
- [ ] **build your track project**
- [ ] **document it for GitHub**
- [ ] **exit check** - AD lab, PowerShell script, track project, subnetting, README/screenshots

## why a home lab beats cert alone

anyone can pass A+. the candidate who built a Windows domain with a Server 2025 DC, Windows 11 clients, GPO, and PowerShell user creation has already practiced the job.

certs get u past filters. the lab gets u the offer.

document everything. screenshots, write-ups, and GitHub turn "i practiced" into proof.

## core build: Windows domain lab

build it in VirtualBox, VMware Workstation Player, or Proxmox.

| Step | What u build | Skill proven |
|---|---|---|
| 1 | Windows Server 2025 VM | server install, VM management |
| 2 | promote to Domain Controller | AD setup |
| 3 | join 2-3 Windows 11 clients | DNS, domain join, networking |
| 4 | create OUs, users, groups | AD administration |
| 5 | apply Group Policy | GPO management |
| 6 | automate bulk users with PowerShell | scripting |
| 7 | connect to free Entra ID dev tenant | hybrid identity |

**lab platforms:** [VirtualBox](https://www.virtualbox.org), [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html), [Proxmox](https://www.proxmox.com), and [Microsoft 365 dev tenant](https://developer.microsoft.com/en-us/microsoft-365/dev-program).

## portfolio projects by track

| Track | Signature project |
|---|---|
| **Help Desk / Support** | Windows domain lab + ticket lifecycle write-up |
| **Networking** | multi-VLAN network in Packet Tracer or GNS3 |
| **Sysadmin** | domain lab + PowerShell scripts |
| **Cloud / Identity** | Intune device enrollment in free M365 tenant |

subnetting is interview gold. be able to subnet on a whiteboard from memory.

## document it for GitHub

each project repo needs:

- [ ] clear `README`: what it is, diagram, how u built it, what next
- [ ] screenshots: domain join, GPO applied, VLAN ping, etc.
- [ ] scripts with comments
- [ ] "what broke and how i fixed it" note

that troubleshooting narrative is exactly what employers want.

## exit check

- [ ] built and documented Windows AD domain lab
- [ ] automated at least one task with PowerShell
- [ ] built track signature project
- [ ] can subnet by hand on a whiteboard
- [ ] every project has README with diagram + screenshots
- [ ] connected at least one lab to free Entra ID dev tenant

[Next: Goal 5 - Job Hunt](05-job-hunt.md)
