# goal 1: foundations - hardware, OS, networking meow (~140h)

> **goal:** build the normal-system floor security sits on: hardware, operating systems, networking, basic security, and troubleshooting. any paid exam is optional; the skill is not qwq

**Total: ~140 hours** (about 10 weeks at 2h/day). the path is: touch the system, solve beginner CTF reps, pass the gates, and let the exam-shaped knowledge build quietly in the background. if later u need domain maps or booking gates, [certifications.md](certifications.md) has them.

[<- Prep](00-prep.md) · [Back to hub](README.md) · [Next: Goal 2 ->](02-core.md)

---

## how to track your progress meow

the `- [ ]` boxes below are display-only in this public repo. fork the repo if u want to tick them in your own copy, or copy this checklist into Obsidian/OneNote and track it there.

your real progress is the **two-part gate**:

1. **measurable gate** - the lab, CTF level, drill, score, or artifact exists.
2. **can u explain it?** - u can say why the mechanism works, unaided.

both must pass before u count a topic done. a practice score can help catch vocab gaps later, but it is not the whole proof meow

---

## the path (todo-tree)

- [ ] **Block 1 - hardware + virtualization basics** (~35h): CPU/RAM/storage, motherboard, firmware, VM resources, troubleshooting.
- [ ] **Block 2 - operating systems + shell survival** (~45h): Windows, Linux, users, files, permissions, malware basics, Bandit.
- [ ] **Block 3 - networking + first security reps** (~45h): DNS, TCP/IP, TLS, ports, subnetting, Wi-Fi, Natas/CyLab-style beginner challenges.
- [ ] **Block 4 - review + patch weak spots** (~15h): revisit the weakest lab notes, redo the missed mechanism, and make the final explain gate clean.
- [ ] **exit check** - the lab/CTF gates pass, the explain gates pass, and any paid checkpoint is a choice, not the mission.

---

## why this still includes support topics

real talk: you dun really need a support cert to learn cybersecurity, but the **topics** matter a lot.
hardware, OS, networking, accounts, malware basics, and troubleshooting are the normal system.
security is what happens when that normal system gets abused.

so learn the topic here.
if later u want a paid support checkpoint for help-desk/support screening, go to [certifications.md](certifications.md).

---

## block 1 - hardware + virtualization basics meow (~35h)

**the idea** - a computer is a chain of mechanisms, not a magic box: CPU executes, RAM holds active work, storage persists data, firmware starts the boot path, and the motherboard connects the pieces.

**how/why it actually works** - the **CPU** runs a fetch-decode-execute loop: the **program counter** points to the next instruction in RAM, the control unit decodes it, and the **ALU** or another CPU unit executes it.

**RAM** is fast and volatile, so the OS copies programs from persistent **storage** into RAM before the CPU can run them. an SSD speeds loading and paging; it does not replace RAM.

the **motherboard** is the interconnect: CPU socket, RAM slots, PCIe lanes, chipset, firmware, power delivery, and connectors decide what can talk to what.

**Virtualization** works by a **hypervisor** presenting virtual CPU/RAM/disk/NICs to a guest OS, then scheduling real hardware underneath. snapshots matter because they give u a rollback point before u break the lab. dw, breaking the lab is part of learning meow

**words u gotta be able to say**
- **CPU / core / thread / clock speed** - instruction engine / execution unit / logical execution path / cycles per second
- **fetch-decode-execute** - CPU loop for each instruction
- **program counter / register / ALU / control unit** - next address / tiny CPU storage / math logic / decode-direct unit
- **RAM / storage** - fast volatile working memory / persistent data storage
- **SSD / HDD / NVMe / SATA / M.2** - flash drive / spinning disk / fast protocol / older bus / form factor
- **UEFI / BIOS / boot order** - firmware and startup path
- **hypervisor / VM / snapshot** - virtualization layer / guest machine / saved VM state
- **troubleshooting method** - structured diagnose -> fix -> verify -> document flow

**study sources (pick what fits your style)**
- [Professor Messer - A+ 220-1201 Core 1 free training course](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/220-1201-training-course/) - use Sections 1, 3, 4, and 5 for hardware/virtualization/troubleshooting vocab. **free**
- [Branch Education - "How does a CPU work?"](https://www.youtube.com/watch?v=cNN_tTXABUA) - visual mechanism of CPU work. **free**
- [Branch Education - "How do SSDs Work?"](https://www.youtube.com/watch?v=5Mh3o886qpg) - storage mechanism intuition. **free**
- [CS50x Week 0 and Week 1](https://cs50.harvard.edu/x/) - optional programming/computer-behavior intuition if the CPU loop still feels abstract. **free**

**do this** - in your local lab from [Prep](00-prep.md), create or inspect one VM and write a tiny hardware map: vCPU count, RAM, virtual disk size/type, network adapter mode, firmware/boot order, and snapshot name. then create a clean snapshot named something obvious like `foundation-clean`.

**measurable gate:** the VM boots, the hardware map exists in your notes, the snapshot exists, and u can restore/boot from that snapshot.

**can u explain it?** ✅ - out loud or written, unaided: *"walk one instruction through fetch-decode-execute; explain why a program has to load from storage into RAM before the CPU can run it; explain what a hypervisor is pretending to the guest OS; then show how a snapshot saves u from a bad change."*

---

## block 2 - operating systems + shell survival meow (~45h)

**the idea** - the OS is the broker between apps and hardware: it starts processes, enforces permissions, stores files, routes input/output, logs events, and decides what code is allowed to touch.

**how/why it actually works** - a **process** is a running program with memory, handles, registers, and permissions. the kernel schedules processes onto CPU time and mediates their access to files, network, and devices.

a shell command is parsed into command + arguments; the OS searches **`PATH`**, starts the executable, connects stdin/stdout/stderr, and returns an exit code.

permissions are enforcement points: Windows uses NTFS ACLs, inheritance, UAC, and identities; Linux uses owner/group/other bits plus root/sudo. attackers love mis-set permissions bc the OS obeys them exactly.

malware is just code running with some level of privilege. removal is about stopping execution, killing persistence, cleaning files/settings, patching the entry point, and verifying it doesnt restart.

**words u gotta be able to say**
- **kernel / process / service / driver** - OS core / running program / background program / hardware interface code
- **PATH / environment variable / exit code** - command search list / process setting / success-failure number
- **stdin / stdout / stderr / pipe** - input / normal output / error output / stream connector
- **NTFS ACL / inheritance / UAC** - Windows permissions / child object permission flow / admin approval prompt
- **root / sudo / chmod / chown** - Linux superuser / run as root / change mode / change owner
- **Registry / HKLM / HKCU** - Windows configuration database / machine hive / user hive
- **malware / persistence / quarantine** - malicious code / survives reboot / isolate suspected file
- **least privilege / MFA / encryption** - minimum access / more than one factor / protect data with keys

**study sources (pick what fits your style)**
- [Professor Messer - A+ 220-1202 Core 2 free training course](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/220-1202-training-course/) - use Sections 1-4 for OS/security/procedure vocab. **free**
- [The Missing Semester - Lecture 1: Course Overview + The Shell](https://missing.csail.mit.edu/2020/course-shell/) - best shell intro, with exercises. **free**
- [TCM Security - Practical Help Desk playlist](https://www.youtube.com/playlist?list=PLLKT__MCUeixqHJ1TRqrHsEd6_EdEvo47) - Windows support and AD-flavored troubleshooting. **free**
- [LabEx Linux Journey](https://labex.io/linuxjourney) - Linux CLI/filesystem/permissions practice. **freemium**

**do this** - complete [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) levels **0-15** unaided. if u need a gentler warmup first, do [TryHackMe - Linux Fundamentals 1](https://tryhackme.com/room/linuxfundamentalspart1) and [TryHackMe - Windows Fundamentals 1](https://tryhackme.com/room/windowsfundamentals1xbx), then come back to Bandit.

**measurable gate:** Bandit levels **0-15** are cleared without copy-pasting a walkthrough, and your notes include at least 8 commands u used (`ssh`, `ls`, `cat`, `grep`, `find`, `chmod`, `base64`, `nc`, etc.) with one sentence each saying what the command proved.

**can u explain it?** ✅ - out loud or written, unaided: *"explain what `PATH` does when u type a command, what stdout/stderr are, what `chmod 640 notes.txt` allows owner/group/others to do, why least privilege limits malware damage, and how malware persistence survives reboot."*

---

## block 3 - networking + first security reps meow (~45h)

**the idea** - typing a URL kicks off a real chain: DNS -> TCP -> TLS -> HTTP. every piece of that chain becomes an attack surface or a defensive control later.

**how/why it actually works** - **DNS** turns a name into an IP address. the OS asks a recursive resolver, which can walk root -> TLD -> authoritative nameservers and return an A/AAAA record with a TTL.

**TCP** sets up a reliable connection with SYN -> SYN-ACK -> ACK. **ports** tell the destination host which service should receive the traffic.

**TLS** authenticates the server with a certificate chain and negotiates session keys so the traffic is encrypted and tamper-evident. thats why HTTPS stops a normal man-in-the-middle from silently reading or changing the page.

**Subnetting** decides which IPs are local; the **default gateway** handles non-local traffic. Wi-Fi adds radio exposure, so WPA2/WPA3, good passwords, and enterprise auth matter.

**words u gotta be able to say**
- **DNS / A record / CNAME / MX / TTL** - name to IP / IPv4 / alias / mail / cache time
- **IP / IPv4 / IPv6 / subnet mask / CIDR / gateway** - address / 32-bit / 128-bit / network bits / slash / router out
- **port / well-known ports** - service id like 22 SSH, 53 DNS, 80 HTTP, 443 HTTPS, 445 SMB, 3389 RDP
- **TCP handshake / packet** - SYN/SYN-ACK/ACK setup / routed data unit
- **TLS / certificate / CA / session key** - secure channel / identity proof / trusted issuer / symmetric key
- **confidentiality / integrity / MITM** - cant read / cant alter / attacker in the middle
- **DHCP / DNS / NTP** - auto IP assignment / name resolution / time sync
- **phishing / malware / hardening** - human trick / malicious code / reduce risky defaults

**study sources (pick what fits your style)**
- [Professor Messer - A+ 220-1201 Core 1 course](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/220-1201-training-course/) - use Section 2 for networking and Section 5 for troubleshooting. **free**
- [Professor Messer - A+ 220-1202 Core 2 course](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/220-1202-training-course/) - use Section 2 for security basics. **free**
- [TryHackMe - Intro to Networking](https://tryhackme.com/room/introtonetworking) - guided OSI, ping, traceroute, and networking basics. **freemium/free room**
- [PowerCert - "OSI Model Explained"](https://www.youtube.com/watch?v=vv4y_uOneC0) and [PowerCert - "DNS Explained"](https://www.youtube.com/watch?v=mpQZVYPuDGU) - short visual refreshers. **free**
- [howdns.works](https://howdns.works/) - comic walkthrough of DNS resolution. **free**

**do this** - complete **TryHackMe Intro to Networking**, drill [subnetipv4.com](https://subnetipv4.com/) until `/25` through `/29` are boring, run `curl -v https://example.com` and `dig example.com`, and annotate which lines show DNS, TCP/TLS, HTTP status, and headers. keep the CTF thread alive by solving [OverTheWire Natas](https://overthewire.org/wargames/natas/) levels **0-3**, or 5 beginner General Skills challenges on [CyLab Security Academy](https://www.cylabacademy.org/) (catalog/login-driven) if u prefer picoCTF-style reps.

**measurable gate:** TryHackMe Intro to Networking is complete, 5 random `/25`-`/29` subnet drills are correct on paper, the `curl`/`dig` annotation exists, and either Natas 0-3 or 5 CyLab beginner challenges are solved.

**can u explain it?** ✅ - out loud or written, unaided: *"narrate the steps from pressing Enter on `https://example.com` to the page appearing: DNS resolution -> TCP SYN/SYN-ACK/ACK -> TLS handshake (what the certificate proves, what the session key does) -> HTTP GET/200. then say why TLS stops a man-in-the-middle."*

---

## block 4 - review + patch weak spots meow (~15h)

this is where u make the foundation solid before Goal 2.
the study materials already gave u the theory; this block is where u check what actually stuck.
dont collect more cert resources rn.
find the thing that still feels foggy, then redo that mechanism until it stops wobbling.

- [ ] **hardware weak spot** - update the VM hardware map and explain CPU/RAM/storage/virtualization again.
- [ ] **OS weak spot** - redo 2 Bandit levels u struggled with and rewrite the command notes cleanly.
- [ ] **networking weak spot** - redo 5 subnet drills and annotate one fresh `curl -v` / `dig` run.
- [ ] **security weak spot** - write one paragraph on how a normal system behavior became the "abuse" in a Bandit/Natas/CyLab challenge.

**measurable gate:** the weak-spot notes exist, and at least one previously fuzzy task was redone without walkthroughs.

**can u explain it?** ✅ - explain which weak spot u patched, what failed before, what u changed, and how u know it works now.

---

## ✅ exit check - done with Goal 1

by now u have:

- [ ] a working VM hardware map + clean snapshot
- [ ] Bandit levels **0-15** cleared unaided, with command notes
- [ ] TryHackMe Intro to Networking completed
- [ ] 5 subnet drills from `/25`-`/29` correct on paper
- [ ] `curl -v https://example.com` + `dig example.com` annotated in your notes
- [ ] Natas 0-3 or 5 CyLab beginner challenges solved
- [ ] one short note naming your weakest foundation area and what u redid to patch it

**final explain gate:** out loud, unaided: *"trace one instruction through fetch-decode-execute; explain why RAM and SSD storage solve different problems; narrate what happens when a shell runs a command through `PATH`; explain how Linux permissions limited or enabled one Bandit level; then walk DNS -> TCP -> TLS -> HTTP for `https://example.com`."*

if the labs pass but the explanation is foggy, slow down and patch the mechanism.
any exam checkpoint is downstream of understanding, not the other way around meow

---

**next up:** [Goal 2 - Networking & Security Core](02-core.md) - packets, crypto, identity, attacks, PortSwigger/Natas, packet cases, IR, and risk.

[<- Prep](00-prep.md) · [Back to hub](README.md) · [Next: Goal 2 ->](02-core.md)
