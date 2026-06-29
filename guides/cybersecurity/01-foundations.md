# Goal 1: Foundations - A+ hardware, OS, networking meow (~140h)

> **goal:** build the IT floor security sits on: hardware, operating systems, networking, basic security, and troubleshooting. the A+ exam is optional; the knowledge is not qwq

**Total: ~140 hours** (about 10 weeks at 2h/day). this goal maps to **CompTIA A+ Core 1 (220-1201)** + **Core 2 (220-1202)**. if u already work in IT support, use the gates as a fast diagnostic and jump to [Goal 2](02-core.md) when both cores are clean.

[<- Prep](00-prep.md) · [Back to hub](README.md) · [Next: Goal 2 ->](02-core.md)

---

## how to track your progress meow

the `- [ ]` boxes below are display-only in this public repo. fork the repo if u want to tick them in your own copy, or copy this checklist into Obsidian/OneNote and track it there.

your real progress is the **two-part gate**:

1. **measurable gate** - the required score/lab result. for A+ here, that means fresh ExamCompass attempts, not vibes.
2. **can u explain it?** - u can say why the mechanism works, unaided.

both must pass before u count a topic done. the checkbox is just a map, not proof meow

---

## should u take the A+?

- **take it if** u have no IT background and want the help-desk / desktop-support door open.
- **study it but skip the paid exam if** u already have IT support experience, or if cash is tight and cybersecurity is the main goal.

real talk: you dun really need A+ if you going into cybersecurity, you can save it for another certificate. the reason we still study the content is bc A+ teaches the normal system: hardware, OS, networking, accounts, malware basics, and troubleshooting. security is just "what happens when that normal system gets abused."

if u do sit the exam, book one core at a time: **Core 1 first**, then **Core 2**. current pass scores: **Core 1 = 675/900**, **Core 2 = 700/900**. check [certifications.md](certifications.md) before paying, because prices move.

---

## the A+ study group map

the clean trick: **Professor Messer section number == CompTIA domain number**.

so Core 1 Domain 3.0 Hardware = Messer Core 1 Section 3. Core 2 Domain 2.0 Security = Messer Core 2 Section 2. no guessing through a giant channel, dw.

- [ ] **Core 1 (220-1201)** - mobile, networking, hardware, virtualization/cloud, troubleshooting (~70h)
- [ ] **Core 2 (220-1202)** - operating systems, security, software troubleshooting, operations (~60h)
- [ ] **practice calibration** - ExamCompass fresh-test gates + optional paid confidence checks (~10h)
- [ ] **exit check** - both core gates pass, both explain gates pass, ready for Goal 2

### Core 1 domain map - 220-1201

| Domain | Weight | What it means in this guide | Messer section |
|---|---:|---|---|
| 1.0 Mobile Devices | 13% | laptops, phones, tablets, mobile connectivity | Section 1: Mobile Devices |
| 2.0 Networking | 23% | ports, protocols, IP, Wi-Fi, tools | Section 2: Networking |
| 3.0 Hardware | 25% | CPU, RAM, storage, motherboards, printers | Section 3: Hardware |
| 4.0 Virtualization & Cloud Computing | 11% | VMs, hypervisors, cloud basics | Section 4: Virtualization and Cloud Computing |
| 5.0 Hardware & Network Troubleshooting | 28% | diagnose, test, fix, verify, document | Section 5: Hardware and Network Troubleshooting |

### Core 2 domain map - 220-1202

| Domain | Weight | What it means in this guide | Messer section |
|---|---:|---|---|
| 1.0 Operating Systems | 28% | Windows, Linux, macOS, command line | Section 1: Operating Systems |
| 2.0 Security | 28% | malware, auth, physical/logical controls, hardening | Section 2: Security |
| 3.0 Software Troubleshooting | 23% | fix OS/app/security symptoms | Section 3: Software Troubleshooting |
| 4.0 Operational Procedures | 21% | documentation, change, backups, safety, scripting | Section 4: Operational Procedures |

---

## Core 1 - hardware, networking, virtualization, troubleshooting meow (~70h)

**cert map** - **A+ Core 1 (220-1201)** Domains 1.0-5.0. use [Professor Messer's A+ 220-1201 Core 1 free training course](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/220-1201-training-course/) as the spine: Section 1 = Domain 1, Section 2 = Domain 2, and so on.

**the idea** - Core 1 teaches the machine as a physical + networked system: what the parts do, how they connect, how data moves, and how to troubleshoot when the chain breaks.

**how/why it actually works** - a computer is a loop wrapped in layers:

1. the **CPU** runs a fetch-decode-execute cycle: the **program counter** points to the next instruction in RAM, the control unit decodes it, and the **ALU** or another CPU unit executes it.
2. **RAM** is fast and volatile, so the OS copies programs from persistent **storage** into RAM before the CPU can run them. more RAM helps concurrency; faster SSD storage helps loading and paging.
3. the **motherboard** is the interconnect: CPU socket, RAM slots, PCIe lanes, chipset, firmware, power delivery, and connectors all decide what can talk to what.
4. networking adds another chain: DNS names become IP addresses, TCP sessions use ports, Wi-Fi/Ethernet carry frames, and routers move packets between networks.
5. virtualization works by a **hypervisor** presenting virtual hardware to guest OSs, then scheduling real CPU/RAM/storage underneath. cloud is basically someone elses virtualized infrastructure plus managed services.
6. troubleshooting works because u narrow the failure point: identify the problem, form a theory, test it, plan/implement the fix, verify full function, then document. thats not ceremony - it stops u from randomly swapping parts until lucky.

**words u gotta be able to say:**
- **CPU / core / thread / clock speed** - instruction engine / execution unit / logical execution path / cycles per second
- **fetch-decode-execute** - CPU loop for each instruction
- **program counter / register / ALU / control unit** - next address / tiny CPU storage / math logic / decode-direct unit
- **RAM / storage** - fast volatile working memory / persistent data storage
- **DDR4 / DDR5 / ECC / dual-channel** - RAM generations / error correction / paired bandwidth mode
- **SSD / HDD / NVMe / SATA / M.2** - flash drive / spinning disk / fast protocol / older bus / form factor
- **motherboard / UEFI / PCIe / PSU** - main board / boot firmware / expansion bus / power supply
- **port / protocol / DNS / DHCP / gateway** - service number / rules / name lookup / IP assignment / router out
- **hypervisor / VM / snapshot** - virtualization layer / guest machine / saved VM state
- **troubleshooting method** - structured diagnose -> fix -> verify -> document flow

**study sources (pick what fits your style):**
- [Professor Messer - A+ 220-1201 Core 1 free training course, V15](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/220-1201-training-course/) - primary course; watch Sections 1-5 because they map exactly to Domains 1.0-5.0. **free**
- [ExamCompass - A+ Core 1 Practice Test 1 (Exam 220-1201)](https://www.examcompass.com/comptia-a-plus-certification-practice-test-1-exam-220-1201) - free practice spine; use fresh 220-1201 test numbers for the gate. **free**
- [ExamCompass - A+ 220-1201 Acronyms Quiz Part 1](https://www.examcompass.com/comptia-a-plus-220-1201-exam-acronyms-quiz-part-1) - acronym drill so terms like `DIMM`, `NVMe`, `DHCP`, and `UEFI` stop feeling random. **free**
- explore more -> [PowerCert - "RAM Explained - Random Access Memory"](https://www.youtube.com/watch?v=PVad0c2cljo) - visual supplement for Core 1 D3.3 memory. **free**
- explore more -> [Branch Education - "How do SSDs Work?"](https://www.youtube.com/watch?v=5Mh3o886qpg) - deeper visual supplement for Core 1 D3.4 storage; heavier than exam depth, useful for mechanism intuition. **free**

**do this** - work through Messer Core 1 Sections 1-5, then use ExamCompass as the free practice spine. when u miss a question, tag it to the matching domain number: Domain 3 miss -> rewatch Messer Section 3. this is why the section==domain mapping matters meow

**measurable gate:** **≥85% on 3 fresh ExamCompass Core 1 (220-1201) practice tests**, with **no Core 1 domain <75%** when u group the misses by domain. fresh means different test numbers, not retaking the same set until u memorize it.

**paid confidence gate (optional):** if u are actually booking Core 1, add one paid fresh practice attempt from [Jason Dion - A+ Core 1 (220-1201) 6 Practice Exams](https://www.udemy.com/course/comptia-a-core-1-220-1201-6-practice-exams/) or [Professor Messer - Core 1 Success Bundle](https://www.professormesser.com/220-1201-success-bundle/). aim for **≥85%** before paying for the real exam. this is confidence, not required for learning.

**can u explain it?** ✅ - out loud or written, unaided: *"walk one instruction through fetch-decode-execute; explain why a program has to load from storage into RAM before the CPU can run it; explain the real difference between RAM and SSD storage; then recite the A+ troubleshooting method and show how youd use it for a no-boot or no-network case."*

---

## Core 2 - operating systems, security, software troubleshooting, operations meow (~60h)

**cert map** - **A+ Core 2 (220-1202)** Domains 1.0-4.0. use [Professor Messer's A+ 220-1202 Core 2 free training course](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/220-1202-training-course/) as the spine: Section 1 = Domain 1, Section 2 = Domain 2, Section 3 = Domain 3, Section 4 = Domain 4.

**the idea** - Core 2 teaches the OS and support layer: users, files, permissions, commands, malware, hardening, symptoms, procedures, and the habits that keep changes from making things worse.

**how/why it actually works** - the OS is the broker between apps and hardware:

1. a **process** is a running program with memory, handles, registers, and permissions. the kernel schedules processes onto CPU time and mediates their access to files, network, and devices.
2. a shell command is parsed into command + arguments; the OS searches **`PATH`**, starts the executable, connects stdin/stdout/stderr, and returns an exit code.
3. permissions are enforcement points: Windows uses NTFS ACLs, inheritance, UAC, and identities; Linux uses owner/group/other bits plus root/sudo. attackers love mis-set permissions bc the OS will obey them exactly.
4. malware is just code running with some level of privilege. removal is about stopping execution, killing persistence, cleaning files/settings, patching the entry point, and verifying it doesnt restart.
5. operational procedures exist because real systems have humans around them: documentation, change management, backups, safety, privacy, and incident notes make fixes repeatable instead of lucky.
6. software troubleshooting is symptom -> scope -> likely layer: user profile, app, OS, driver, network, security control, or hardware. u test the smallest likely cause first so u dont break five things trying to fix one.

**words u gotta be able to say:**
- **kernel / process / service / driver** - OS core / running program / background program / hardware interface code
- **PATH / environment variable / exit code** - command search list / process setting / success-failure number
- **stdin / stdout / stderr / pipe** - input / normal output / error output / stream connector
- **NTFS ACL / inheritance / UAC** - Windows permissions / child object permission flow / admin approval prompt
- **root / sudo / chmod / chown** - Linux superuser / run as root / change mode / change owner
- **Registry / HKLM / HKCU** - Windows configuration database / machine hive / user hive
- **malware / persistence / quarantine** - malicious code / survives reboot / isolate suspected file
- **MFA / least privilege / encryption** - more than one factor / minimum access / protect data with keys
- **change management / rollback / backup** - controlled change / undo path / restorable copy
- **script / variable / loop / conditional** - automation file / named value / repeat / branch

**study sources (pick what fits your style):**
- [Professor Messer - A+ 220-1202 Core 2 free training course, V15](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/220-1202-training-course/) - primary course; watch Sections 1-4 because they map exactly to Domains 1.0-4.0. **free**
- [ExamCompass - A+ Core 2 Practice Test 1 (Exam 220-1202)](https://www.examcompass.com/comptia-a-plus-certification-practice-test-1-exam-220-1202) - free practice spine; use fresh 220-1202 test numbers for the gate. **free**
- [ExamCompass - A+ 220-1202 Acronyms Quiz Part 1](https://www.examcompass.com/comptia-a-plus-220-1202-exam-acronyms-quiz-part-1) - acronym drill for OS, security, procedure, and troubleshooting terms. **free**

**do this** - work through Messer Core 2 Sections 1-4, then use ExamCompass as the free practice spine. tag misses by the domain number they belong to: Domain 2 miss -> rewatch Messer Section 2. Core 2 Domain 1 and Domain 2 matter extra for cyber because they become the OS/security floor in Goal 2.

**measurable gate:** **≥85% on 3 fresh ExamCompass Core 2 (220-1202) practice tests**, with **no Core 2 domain <75%** when u group the misses by domain. fresh means different test numbers, not a memorized retake.

**paid confidence gate (optional):** if u are actually booking Core 2, add one paid fresh practice attempt from [Jason Dion - A+ Core 2 (220-1202) 6 Practice Exams](https://www.udemy.com/course/comptia-a-core-2-220-1202-6-practice-exams/) or [Professor Messer - Core 2 Success Bundle](https://www.professormesser.com/220-1202-success-bundle/). aim for **≥85%** before the real exam.

**can u explain it?** ✅ - out loud or written, unaided: *"explain what `PATH` does when u type a command, what stdout/stderr are, why least privilege limits malware damage, name 3 malware types, and walk how youd remove one without letting it persist after reboot."*

---

## practice calibration - dont book on hope meow (~10h)

this is not a separate cert silo. its the same topic study with a clean readiness check at the end.

- [ ] **Core 1 free hard gate** - ≥85% on 3 fresh ExamCompass Core 1 (220-1201) tests, no Core 1 domain <75%.
- [ ] **Core 1 explain gate** - can explain CPU/RAM/storage + troubleshooting, unaided.
- [ ] **Core 2 free hard gate** - ≥85% on 3 fresh ExamCompass Core 2 (220-1202) tests, no Core 2 domain <75%.
- [ ] **Core 2 explain gate** - can explain OS command execution + malware removal/persistence, unaided.
- [ ] **optional paid confidence** - ≥85% on one fresh Dion or Messer Success Bundle practice exam for each core u plan to sit.

if u fail one domain, dont restart the whole goal. use the clean map: weak Core 1 Domain 2 means rewatch Core 1 Section 2. weak Core 2 Domain 4 means rewatch Core 2 Section 4. patch the exact leak, then retest with a fresh ExamCompass set.

**CTF thread:** keep the beginner CTF thread from [Prep](00-prep.md) alive while u study this. A+ gives u the normal-system vocabulary; CTF keeps asking "ok but how could this break?" they work together, not separately.

---

## ✅ exit check - youre done with Goal 1

by now u have:

- [ ] passed the **Core 1 measurable gate**: ≥85% on 3 fresh ExamCompass 220-1201 tests, no domain <75%
- [ ] passed the **Core 2 measurable gate**: ≥85% on 3 fresh ExamCompass 220-1202 tests, no domain <75%
- [ ] passed the **Core 1 explain gate**: CPU/RAM/storage + troubleshooting method
- [ ] passed the **Core 2 explain gate**: OS command execution + malware removal/persistence
- [ ] decided honestly whether the paid A+ exam is worth it for your situation

**final explain gate:** out loud, unaided: *"trace one instruction through fetch-decode-execute; explain why RAM and SSD storage solve different problems; narrate what happens when a shell runs a command through `PATH`; explain how malware persists and how least privilege limits damage; then say which Messer section youd revisit for each weak A+ domain."*

if the scores pass but the explanation is foggy, slow down and patch the mechanism. the cert is downstream of understanding, not the other way around meow

---

**next up:** [Goal 2 - Networking & Security Core](02-core.md) - Network+, ISC2 CC + Security+ merged study. A+ gave u the floor; now we turn that floor into security thinking.

[<- Prep](00-prep.md) · [Back to hub](README.md) · [Next: Goal 2 ->](02-core.md)
