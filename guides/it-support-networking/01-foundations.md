# 🧱 Phase 1: Foundations

> **~140 hrs total** · your pace, no deadline
> Hardware, operating systems, the network stack, and the command line. This is the bedrock every help-desk and networking role is built on — and most of CompTIA A+.

[← Phase 0](00-prep.md) · [Hub](README.md) · [Next: Phase 2 →](02-core.md)

---

## Hardware & operating systems (~40 hrs)

If you can't take it apart mentally, you can't support it. This block is the heart of **A+ Core 1**.

### What to cover
- **PC internals:** CPU, RAM, storage (HDD vs SSD vs NVMe), motherboard, PSU, GPU — what each does and common failure symptoms
- **Peripherals & connectors:** USB-C/Thunderbolt, HDMI/DisplayPort, RJ45, the modern port zoo
- **Mobile & laptop:** field-replaceable parts, docking, display issues
- **Operating systems:** Windows 11 (primary), macOS, and a first taste of Linux — install, update, user accounts, permissions
- **Printers & peripherals:** the classic help-desk ticket — drivers, queues, connectivity
- **The troubleshooting method:** identify → theory → test → plan → resolve → document. Memorize the CompTIA 6 steps; interviewers ask.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Professor Messer A+ Core 1](https://www.professormesser.com) | Video | Full free A+ Core 1 course | **Free** |
| [VirtualBox](https://www.virtualbox.org) | Local | Install Windows/Linux VMs, break & fix safely | **Free** |
| PC build simulator | Web | Practice assembling a PC without hardware | **Free** |

> **No spare PC?** A $0 VirtualBox VM teaches 80% of OS troubleshooting. A junked desktop from anywhere teaches the hardware half — ask around, people give them away.

---

## Networking fundamentals (TCP/IP) (~50 hrs)

Networking is the highest-leverage knowledge in this field. It never goes stale, and it's what separates a button-pusher from a real technician. This is **A+ Core + most of Network+**.

### What to cover
- **The OSI & TCP/IP models:** what each layer does, where problems live
- **IP addressing:** IPv4, subnets, CIDR, private vs public, **subnetting by hand** (interviewers love this)
- **Core protocols:** DNS (how name resolution actually works), DHCP (how a device gets an IP), HTTP/HTTPS, SSH, RDP
- **Ports & protocols:** the common-port list (53, 80, 443, 22, 3389, 25, 143…) — memorize it
- **Network hardware:** switch vs router vs firewall vs access point — what each does
- **Wi-Fi:** standards (Wi-Fi 6/6E/7), channels, common interference issues
- **Command-line networking:** `ping`, `ipconfig`/`ifconfig`, `nslookup`/`dig`, `tracert`, `netstat`

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Professor Messer Network+](https://www.professormesser.com) | Video | Full free Network+ course | **Free** |
| [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco | Build & simulate real networks | **Free** (free course) |
| [subnetting practice](https://subnetipv4.com/) | Web | Drill subnet math until it's automatic | **Free** |

**Practice gate:** subnet a /24 into 4 equal subnets on paper, and explain what happens (in order) when you type a URL and press Enter — DNS → TCP → HTTP. If you can do both, you're ahead of most T1 applicants.

---

## Command line & scripting first steps (~50 hrs)

The terminal isn't optional anymore — even at T1, what sets candidates apart is comfort with the command line.

### What to cover
- **Windows command line:** `cmd` basics, then **PowerShell** — cmdlets, the pipeline, `Get-Help`
- **Reading & running PowerShell:** run a script, understand variables, loops, `Get-`/`Set-` verbs (don't fear it)
- **Linux CLI basics:** navigation (`cd`, `ls`, `pwd`), files (`cp`, `mv`, `rm`, `cat`), permissions (`chmod`), package basics
- **Why scripting matters:** a task done once by hand is fine; a task done 50 times should be a script — that mindset is your ticket up the ladder
- **First automation:** a PowerShell one-liner that does something real (list disk space, find large files)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Microsoft Learn: PowerShell](https://learn.microsoft.com/en-us/training/) | Official | Guided PowerShell from zero | **Free** |
| [VirtualBox Linux VM](https://www.virtualbox.org) | Local | A safe Linux box to practice CLI | **Free** |
| [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) | SSH | Linux CLI puzzles, real boxes | **Free** |

---

## Phase 1 exit checklist
- [ ] Can identify PC components and diagnose common hardware failures
- [ ] Can install and troubleshoot Windows 11 (and install a Linux VM)
- [ ] Know the troubleshooting methodology cold (the CompTIA 6 steps)
- [ ] Can subnet by hand and explain DNS/DHCP from memory
- [ ] Comfortable with `ping`/`ipconfig`/`nslookup`/`tracert`
- [ ] Can read and run a basic PowerShell script without fear
- [ ] On track for (or passed) **CompTIA A+ Core 1**

Next: [Phase 2 — Core Support Skills →](02-core.md)
