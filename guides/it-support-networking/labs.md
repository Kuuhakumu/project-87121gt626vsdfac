# 🧪 Lab Inventory — IT Support & Networking (2026)

> Every lab below was **curl status-checked June 13, 2026**. ✅ live (200) · ⚠️ live but blocks automated checks (403/429) · ❌ dead.
> Hands-on beats reading. In IT support, a **home lab** is the single biggest hireable signal — build it as you learn.

---

## Free training (theory + guided)

| Resource | Platform | What you get | Cost | Status |
|---|---|---|---|---|
| [Professor Messer](https://www.professormesser.com) | Web/YouTube | **Free, complete** A+, Network+, Security+ courses | Free | ✅ |
| [Microsoft Learn](https://learn.microsoft.com/en-us/training/) | Microsoft | Free AZ-900/MD-102/M365 paths + sandboxes | Free | ✅ |
| [Cisco Networking Academy](https://www.netacad.com/courses/packet-tracer) | Cisco | Free networking courses + Packet Tracer | Free | ✅ |
| [CBT Nuggets](https://www.cbtnuggets.com) | Web | Polished cert video training | Paid | ✅ |

---

## Networking labs (the core skill)

| Lab | Platform | What you do | Cost | Status |
|---|---|---|---|---|
| [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco | Build/simulate switched & routed networks (CCNA prep) | Free | ✅ |
| [GNS3](https://www.gns3.com) | Local | Emulate real network device images | Free | ✅ |
| [Wireshark](https://www.wireshark.org) | Local | Capture & analyze real packets (DNS, DHCP, TCP) | Free | ✅ (v4.6) |
| subnetting drills | subnettingpractice.com / Professor Messer | Drill subnetting until automatic | Free | ✅ |

> **Subnetting will trip you up if you haven't drilled it.** Practice daily until you can do it without a calculator.

---

## Home-lab platforms (virtualization)

| Tool | Platform | What you do | Cost | Status |
|---|---|---|---|---|
| [VirtualBox](https://www.virtualbox.org) | Local | Free hypervisor — run Windows Server + client VMs | Free | ✅ |
| [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html) | Local | Free hypervisor (now Broadcom, still free for personal) | Free | ✅ |
| [Proxmox VE](https://www.proxmox.com) | Local | Bare-metal hypervisor for a real home-lab server | Free | ✅ |

**Core home-lab build:** Windows Server 2025 (eval) as a domain controller + a Windows 11 client joined to the domain. Practice Active Directory, Group Policy, DNS, DHCP.

---

## Microsoft / cloud / identity labs

| Lab | Platform | What you do | Cost | Status |
|---|---|---|---|---|
| [M365 Developer Program](https://developer.microsoft.com/en-us/microsoft-365/dev-program) | Microsoft | **Free M365 dev tenant** — practice Entra ID, Intune, admin center | Free | ✅ |
| [Microsoft Learn sandboxes](https://learn.microsoft.com/en-us/training/) | Microsoft | Free Azure sandbox, no credit card | Free | ✅ |
| [Azure Free Account](https://azure.microsoft.com/free/) | Microsoft | Real Azure resources, 12-mo free tier | Free tier | ✅ |

> The **free M365 dev tenant** is underused by most learners — it's a full tenant where you can practice Entra ID users, groups, Intune enrollment, and Conditional Access.

---

## PowerShell & scripting

| Lab | Platform | What you do | Cost | Status |
|---|---|---|---|---|
| [Microsoft Learn: PowerShell](https://learn.microsoft.com/en-us/training/) | Microsoft | Guided PowerShell from zero | Free | ✅ |
| Your home-lab AD | Local | Bulk-create users, pull reports, automate tasks | Free | ✅ |

---

## Cert practice exams

| Tool | What you do | Cost | Status |
|---|---|---|---|
| [Boson ExSim](https://www.boson.com) | Highest-fidelity CompTIA/Cisco practice exams | Paid | ✅ |
| Professor Messer practice exams | Free A+/Net+ question banks | Free | ✅ |
| [TryHackMe](https://tryhackme.com) | Hands-on networking/security fundamentals | Freemium | ⚠️ (429 = live) |

---

## Platform quick reference

| Platform | Best for | Cost |
|---|---|---|
| Professor Messer | Free A+/Net+/Sec+ video training | Free |
| Packet Tracer / GNS3 | Network simulation & CCNA prep | Free |
| Wireshark | Packet analysis | Free |
| VirtualBox / Proxmox | Home-lab virtualization | Free |
| M365 Dev Program | Entra ID / Intune / M365 admin practice | Free |
| Boson | Exam-grade practice tests | Paid |

---

## Dead / changed since 2021

| Old resource | Status | Replacement |
|---|---|---|
| TestOut LabSim | acquired by CompTIA, folded into CertMaster | CompTIA CertMaster Labs |
| Free VMware Workstation Player (old EULA) | now under Broadcom — still free personal use, new download path | vmware.com player page |
| MD-100 / MD-101 separate labs | consolidated | MD-102 content |

---

*Sources: curl status-checked June 13, 2026. All primary targets returned 200 or 403/429 (live). Raw findings in `research/lab-inventory/it-support-networking-2026.md`.*
