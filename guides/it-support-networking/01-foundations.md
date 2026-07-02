# Goal 1: foundations meow

> **~140h total** - your pace, no deadline.
> hardware, operating systems, network stack, and command line.
> this is most of CompTIA A+ and the bedrock for help desk/networking.

[Previous: Goal 0](00-prep.md) - [Hub](README.md) - [Next: Goal 2](02-core.md)

---

- [ ] **hardware and operating systems** (~40h)
- [ ] **networking fundamentals** (~50h)
- [ ] **command line and scripting first steps** (~50h)
- [ ] **exit check** - hardware, Windows/Linux, troubleshooting method, subnet/DNS/DHCP, PowerShell basics

## hardware and operating systems (~40h)

if u cant take it apart mentally, u cant support it. this is the heart of **A+ Core 1**.

- [ ] PC internals: CPU, RAM, storage, motherboard, PSU, GPU
- [ ] connectors: USB-C/Thunderbolt, HDMI/DisplayPort, RJ45
- [ ] mobile/laptop parts, docking, display issues
- [ ] Windows 11, macOS, and first Linux install/update/user/permission basics
- [ ] printers: drivers, queues, connectivity
- [ ] CompTIA troubleshooting method: identify -> theory -> test -> plan -> resolve -> document

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Professor Messer A+ Core 1 | Web/video | full free A+ Core 1 course | **Free** - **⚠️ TODO verify exact V15 Core 1 link** |
| [VirtualBox](https://www.virtualbox.org) | Local | install Windows/Linux VMs, break and fix safely | **Free** |
| PC build simulator | Web | practice assembling a PC without hardware | **Free** - **⚠️ TODO verify exact simulator** |

no spare PC? VirtualBox teaches most OS troubleshooting. a junk desktop teaches the hardware half.

## networking fundamentals (~50h)

networking is the highest-leverage knowledge in support. it never goes stale.

- [ ] OSI and TCP/IP models
- [ ] IPv4, subnets, CIDR, private/public IPs
- [ ] subnetting by hand
- [ ] DNS, DHCP, HTTP/HTTPS, SSH, RDP
- [ ] ports: 53, 80, 443, 22, 3389, 25, 143
- [ ] switch vs router vs firewall vs access point
- [ ] Wi-Fi 6/6E/7, channels, interference
- [ ] `ping`, `ipconfig`, `nslookup`, `tracert`, `netstat`

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Professor Messer Network+ | Web/video | full Network+ course | **Free** - **⚠️ TODO verify exact N10-009 link** |
| [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco | build and simulate networks | **Free** |
| [subnetting practice](https://subnetipv4.com/) | Web | drill subnet math | **Free** |

**practice gate:** subnet a `/24` into 4 equal subnets on paper, and explain DNS -> TCP -> HTTP after typing a URL.

## command line and scripting first steps (~50h)

terminal comfort sets candidates apart, even at T1.

- [ ] Windows `cmd` basics
- [ ] PowerShell cmdlets, pipeline, `Get-Help`
- [ ] read and run scripts: variables, loops, `Get-`/`Set-` verbs
- [ ] Linux CLI: `cd`, `ls`, `pwd`, `cp`, `mv`, `rm`, `cat`, `chmod`
- [ ] first automation: disk space, large files, or basic report

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Microsoft Learn: PowerShell](https://learn.microsoft.com/en-us/training/) | Official | guided PowerShell from zero | **Free** |
| [VirtualBox Linux VM](https://www.virtualbox.org) | Local | safe Linux CLI practice | **Free** |
| [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) | SSH | Linux CLI puzzles | **Free** |

## exit check

- [ ] can identify PC components and common failure symptoms
- [ ] can install/troubleshoot Windows 11 and install a Linux VM
- [ ] know CompTIA 6-step troubleshooting cold
- [ ] can subnet by hand and explain DNS/DHCP
- [ ] comfortable with `ping`, `ipconfig`, `nslookup`, `tracert`
- [ ] can read and run a basic PowerShell script
- [ ] on track for or passed **CompTIA A+ Core 1**

[Next: Goal 2 - Core Support Skills](02-core.md)
