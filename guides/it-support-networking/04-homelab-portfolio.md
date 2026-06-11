# 🛠️ Phase 4: Home Lab & Portfolio

> **~100 hrs total** · your pace, no deadline
> In IT support, **a documented home lab is your portfolio.** You have no production access yet, so you build your own environment and prove you can run it.

[← Phase 3](03-specialization.md) · [Hub](README.md) · [Next: Phase 5 — Job Hunt →](05-job-hunt.md)

---

## Why a home lab beats a certificate alone

Anyone can pass A+. The candidate who says *"I built a Windows domain with a Server 2025 DC, joined three Windows 11 clients, set up group policy, and automated user creation with PowerShell"* has already done the job. Certs get you past the filter; the lab is what gets you the offer.

> **Document everything.** A lab nobody can see doesn't count. Screenshots, a short write-up per project, and a public GitHub repo turn "I practiced" into proof.

---

## The core build: a Windows domain lab

This single project covers most of what a help-desk/sysadmin interview probes. Build it in VirtualBox, VMware Workstation Player, or Proxmox — all free.

| Step | What you build | Skill proven |
|---|---|---|
| 1 | Install Windows Server 2025 as a VM | Server install, VM management |
| 2 | Promote it to a Domain Controller (AD DS) | Active Directory setup |
| 3 | Join 2–3 Windows 11 client VMs to the domain | DNS, domain join, networking |
| 4 | Create OUs, users, and groups | AD administration |
| 5 | Apply Group Policy (password policy, desktop lockdown) | GPO management |
| 6 | Automate bulk user creation with PowerShell | Scripting / automation |
| 7 | Add a hybrid twist: connect to a free Entra ID dev tenant | Modern hybrid identity |

**Lab platform:** [VirtualBox](https://www.virtualbox.org) (free) · [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html) (free) · [Proxmox](https://www.proxmox.com) (free, bare-metal). Free Microsoft 365 dev tenant: [developer.microsoft.com/microsoft-365/dev-program](https://developer.microsoft.com/en-us/microsoft-365/dev-program).

---

## Portfolio projects by track

| Track | Signature project |
|---|---|
| **Help Desk / Support** | Windows domain lab above + a documented "ticket lifecycle" write-up (intake → triage → resolution → closure) |
| **Networking** | Multi-VLAN network in [Packet Tracer](https://www.netacad.com/courses/packet-tracer) or GNS3: subnetting, inter-VLAN routing, DHCP, ACLs |
| **Sysadmin** | The domain lab + PowerShell automation scripts (bulk users, disk/health reports) on GitHub |
| **Cloud / Identity** | Intune device enrollment in a free M365 dev tenant: enroll a Windows 11 VM, push a compliance policy + app |

> **Subnetting is interview gold.** Be able to subnet on a whiteboard from memory — it's the single most common networking screen for support and network-tech roles.

---

## Document it for GitHub

Each project repo needs:
- A clear `README`: what it is, a network/architecture diagram, how you built it, what you'd do next
- Screenshots of the working result (domain joined, GPO applied, ping succeeding across VLANs)
- Any scripts (PowerShell) with comments explaining what they do
- A short "what I learned / what broke and how I fixed it" note — that troubleshooting narrative is exactly what employers want to see

---

## Phase 4 exit checklist
- [ ] Built and documented a Windows AD domain lab (DC + clients + GPO)
- [ ] Automated at least one task with PowerShell, script on GitHub
- [ ] Built your track's signature project (VLAN network / Intune enrollment / sysadmin automation)
- [ ] Can subnet by hand on a whiteboard
- [ ] Every project has a README with diagram + screenshots
- [ ] Connected at least one lab to a free Entra ID dev tenant (hybrid identity)

Next: [Phase 5 — Job Hunt →](05-job-hunt.md)
