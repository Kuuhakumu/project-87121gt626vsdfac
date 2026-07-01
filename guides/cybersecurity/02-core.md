# Goal 2: Networking & Security Core meow (~180h)

> **goal:** build the network floor, then learn the security mechanisms on top of it: CIA, crypto/TLS, identity, access control, attacks, operations, IR, and risk.
>
> **optional checkpoints layered on top:** **CompTIA Network+ (N10-009)** -> **ISC2 CC** (optional paid exam) -> **CompTIA Security+ (SY0-701)**.

[<- Goal 1: Foundations](01-foundations.md) | [Back to hub](README.md) | [Next: Scripting, Logs & CTF ->](03-scripting-ctf.md)

---

## read this first meow

this file is not "study Network+, then study CC, then study Security+" as three separate piles.

we study the **topics** in the order they depend on each other.
the certs come after, as checkpoints for what already clicked.
thats how u dont get lost qwq

also: **u dont need a paid textbook for this file.** deeper references helped shape the rewrite, but the path below is enough: the explanations here, free/freemium resources, and real labs.

**CC money note:** the ISC2 "One Million Certified" free-voucher program closed on **2026-05-20**. the CC exam is now about **$199 + $50/yr AMF** if u choose to sit it. the free checkpoint is this guide's two-part gate system: measurable lab/practice score + `can u explain it?`.

> if u test CC on or after **2026-09-01**, re-check the ISC2 outline first. ISC2 announced a new outline effective that date.

---

## how to track your progress meow

the `- [ ]` boxes here are display-only in this public repo.
fork the repo, or copy this checklist into Obsidian/OneNote, if u want boxes u can actually tick.

the real progress signal is always:

1. **measurable gate** - a real score, solved lab, solved room, or timed drill.
2. **can u explain it?** - out loud or written, unaided, naming the mechanism.

both must pass before the topic is really done. a checkbox by itself means nothing meow

---

## the path (todo-tree)

- [ ] **Block 1 - networking floor** (~55h): packets, ports, subnetting, implementation, operations, troubleshooting.
- [ ] **Blocks 2-5 - security fundamentals through labs + practice gates** (~115h): A -> D -> B -> C -> E -> F -> G -> H.
- [ ] **Block 6 - optional exam checkpoint sprint** (~10h): Network+ gate, CC optional gate, Security+ gate.
- [ ] **exit check** - can explain the whole chain: normal network -> control -> attack -> detection -> response.

---

## optional checkpoint map so u know what the learning covers

### Network+ N10-009 coverage

| N10-009 domain | Weight | Covered in this file |
|---|---:|---|
| 1.0 Networking Concepts | 23% | packets/ports/protocols, OSI/TCP-IP, IPv4/IPv6, DNS/DHCP/NTP, subnetting |
| 2.0 Network Implementation | 20% | cabling, Wi-Fi/WPA3, VLANs, routing/switching concepts, NAT/PAT |
| 3.0 Network Operations | 19% | monitoring, syslog/SNMP/NetFlow, documentation, SLAs |
| 4.0 Network Security | 14% | segmentation, IDS/IPS concepts, firewalls, zero trust, hardening |
| 5.0 Network Troubleshooting | 24% | 7-step method, `ping`, `tracert`, `nslookup`, `dig`, `ipconfig`/`ip`, `netstat`, `nmap` |

use [Professor Messer's N10-009 course index](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/) as the spine, bc the sections map cleanly to the CompTIA domains:

| Messer section | N10-009 domain | Weight | Study focus |
|---|---|---:|---|
| [Section 1: Networking Concepts](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#section-1-networking-concepts) | 1.0 Networking Concepts | 23% | OSI/TCP-IP, ports, IPv4/IPv6, DNS/DHCP/NTP, subnetting |
| [Section 2: Network Implementation](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#1d643e1) | 2.0 Network Implementation | 20% | cabling, Wi-Fi/WPA3, VLANs, switching/routing, NAT/PAT |
| [Section 3: Network Operations](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#ced8446) | 3.0 Network Operations | 19% | monitoring, documentation, SNMP/syslog/NetFlow, SLAs, DR basics |
| [Section 4: Network Security](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#012c566) | 4.0 Network Security | 14% | segmentation, zero trust, IDS/IPS concepts, hardening |
| [Section 5: Network Troubleshooting](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#c80f0f9) | 5.0 Network Troubleshooting | **24%** | **biggest domain**: 7-step method + CLI troubleshooting tools |

heads up meow: **Troubleshooting is the biggest Network+ domain at 24%**.
dont treat it like cleanup at the end.
the CompTIA **7-step troubleshooting method** is the skeleton: identify the problem -> establish a theory -> test the theory -> make a plan -> implement -> verify -> document.

**practice spine:** use [ExamCompass Network+ N10-009 practice tests](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests) for free current-code practice, not retired legacy sets. if buying practice, use the [Jason Dion N10-009 Practice Exam Pack](https://www.diontraining.com/products/comptia-network-n10-009-practice-exam), not a generic/legacy Network+ pack.

**CCNA-deeper delta:** Network+ teaches what switching, routing, VLANs, NAT, wireless, OSPF/BGP, DHCP, and troubleshooting tools *do*. **CCNA 200-301 goes deeper** by making u configure Cisco IOS interfaces, VLAN trunks, inter-VLAN routing, OSPFv2, static/default routes, ACLs, NAT/PAT, DHCP, port security, and automation basics. for this cyber path, Network+ is enough unless your target work is router/switch-heavy.

### merged CC + Security+ map

| Study cluster | ISC2 CC domain(s) | SY0-701 domain(s) | delta so ur not guessing |
|---|---|---|---|
| **A. Security Foundations & Governance Concepts** | D1 | 1.0, 5.0 | mostly **both**; ISC2 Code of Ethics = **CC only**; Zero Trust / gap analysis = **Security+ emphasis** |
| **D. Networking & Network Security** | D4 | 3.2, 4.5 (+ prereq) | **CC tests networking fundamentals explicitly (OSI/TCP/ports)**; Security+ **assumes** them and tests the security controls |
| **B. Cryptography & PKI** | D5 | 1.4, 3.3 | **both** at concept level; **Security+ deeper** on PKI/certs; obfuscation/blockchain/steganography = **Security+ only** |
| **C. Access Control & Identity (IAM)** | D3, D1 | 4.6, 1.2 | **both**; federation/SSO/Kerberos/802.1X/EAP = **Security+ deeper** |
| **E. Threats, Attacks, Vulnerabilities & Malware** | D4, D5 | 2.0 | **both** on malware/social-eng/DoS/MITM; threat-actor taxonomy + specific vuln types = **Security+ only/deeper** |
| **F. Security Operations (monitoring, hardening, automation)** | D5 | 4.0 | **both** on hardening/logging/data-handling; SIEM, vuln mgmt, asset mgmt, automation/scripting = **Security+ only/deeper** |
| **G. Incident Response, BC/DR & Resilience** | D2 | 4.8, 3.4, 5.2 | **both** on IR lifecycle + BC/DR; digital forensics + architecture-level resilience = **Security+ deeper** |
| **H. GRC & Security Program Management** | D1 | 5.0 | **both** on risk/governance/awareness; third-party risk, audits/assessments, NIST CSF/ISO frameworks = **Security+ only/deeper**; ISC2 Code of Ethics = **CC only** |

study order for this file: **A -> D -> B -> C -> E -> F -> G -> H**.
we study the superset first.
then CC or Security+ becomes a checkpoint, not a separate pile of flashcards meow.

---

## Block 1 - networking floor meow (~55h)

- [ ] packets, ports, and protocols (~18h)
- [ ] subnetting, switching, routing, and wireless (~22h)
- [ ] network operations + troubleshooting (~15h)

this sits beside the merged CC + Security+ study group below, not inside it.
finish this first if networking still feels foggy; Security+ assumes a lot of it, and CC tests some of it directly qwq.

### packets, ports, and protocols meow (~18h)

**optional checkpoint map** - Network+ D1/D5; CC D4; this is the floor Security+ leans on.

**the idea** - networks are layered so each layer gets one job: move bits, frame local traffic, route packets, connect processes, and carry app data.

**how/why it actually works** - when your browser talks to a site, the app data becomes **HTTP**, then **TLS** protects it, then **TCP** gives reliable delivery with ports and sequence numbers, then **IP** routes packets hop-by-hop, then Ethernet/Wi-Fi moves frames on the local link.

**DNS** turns names into IPs; **ports** tell the destination host which process should receive the traffic; **TCP** uses SYN -> SYN-ACK -> ACK before data flows; **UDP** skips that reliability for speed.

the layer model matters because troubleshooting gets less scary: if DNS fails, the app never finds an IP; if routing fails, packets never reach the network; if TCP fails, the service may be down or blocked; if TLS fails, identity/trust may be broken.

**words u gotta be able to say**
- **OSI / TCP-IP model** - layered naming for network jobs
- **packet / frame** - routed unit / local-link unit
- **IP address** - routable host/location identifier
- **port** - service/process number on a host
- **TCP / UDP** - reliable connection / connectionless datagram
- **DNS / DHCP / NTP** - names / automatic IP config / time sync
- **SYN, SYN-ACK, ACK** - TCP connection setup
- **stateful firewall** - tracks connection state, not just packets

**study sources (pick what fits your style)**
- [Professor Messer N10-009 course, Section 1: Networking Concepts](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#section-1-networking-concepts) - exact Network+ section for Domain 1.0. **free**
- [TryHackMe: Intro to Networking](https://tryhackme.com/room/introtonetworking) - guided OSI/ping/traceroute room. **freemium** (bot-blocked in checks, works in browser)
- [TryHackMe: Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics) - packet-capture practice. **freemium** (bot-blocked in checks, works in browser)
- [Professor Messer N10-009 YouTube playlist](https://www.youtube.com/playlist?list=PLG49S3nxzAnl_tQe3kvnmeMid0mjF8Le8) - same course if YouTube is easier. **free**

**do this** - complete **TryHackMe Intro to Networking** and **Wireshark: The Basics**, then capture or inspect one HTTP/HTTPS session and label where DNS, TCP, TLS, and HTTP show up.

**measurable gate:** score **90%+** on the [ExamCompass Network+ OSI Reference Model quiz and TCP/UDP ports quiz](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests), and correctly label the SYN -> SYN-ACK -> ACK in a packet capture.

**can u explain it?** - unaided: explain what happens when a client opens `https://example.com`, naming DNS -> TCP -> TLS -> HTTP and saying what each layer is responsible for. then explain why a switch, router, and firewall are not the same device.

### subnetting, switching, routing, and wireless meow (~22h)

**optional checkpoint map** - Network+ D1/D2; CC D4; Security+ D3.2/4.5 security controls later.

**the idea** - subnetting decides which IPs are local, routing decides where non-local packets go, switching moves local frames, and wireless adds radio + authentication problems. one sentence, lots of doors meow.

**how/why it actually works** - an IPv4 address is split into **network bits** and **host bits** by the subnet mask/CIDR prefix. if two hosts share the same network ID, they talk locally through a switch; if not, they send traffic to a **default gateway** router.

**VLANs** split one physical switch into multiple logical broadcast domains, so HR traffic, server traffic, guest Wi-Fi, and admin traffic dont all share one noisy flat LAN.

**NAT/PAT** rewrites private inside addresses to a public address so many internal hosts can share one public IP. **Wi-Fi** adds radio exposure, so modern networks use WPA2/WPA3 and often **802.1X/RADIUS** so a password alone isnt the whole trust boundary.

**words u gotta be able to say**
- **CIDR / subnet mask** - which bits are network bits
- **network ID / broadcast / usable host** - subnet boundaries
- **default gateway** - router for non-local traffic
- **switch / router** - local frames / routed packets
- **VLAN / trunk** - logical LAN / carries multiple VLANs
- **NAT / PAT** - address/port rewriting at the edge
- **WPA2/WPA3 / RADIUS / 802.1X** - Wi-Fi security / centralized auth / port-based auth
- **CCNA delta** - Network+ names these; CCNA makes u configure them

**study sources**
- [Professor Messer: Calculating IPv4 Subnets and Hosts - N10-009 1.7](https://www.professormesser.com/network-plus/n10-009/n10-009-video/calculating-ipv4-subnets-and-hosts-n10-009/) - subnetting worked examples. **free**
- [subnetipv4.com](https://subnetipv4.com/) - free IPv4 subnetting drill generator. **free**
- [Practical Networking: Subnetting Mastery playlist](https://www.youtube.com/playlist?list=PLIFyRwBY_4bQUE4IB5c4VPRyDoLgOdExE) - method-first subnetting series by the same creator. **free**
- [Professor Messer N10-009 course, Section 2: Network Implementation](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#1d643e1) - cabling, Wi-Fi, routing/switching, NAT/PAT. **free**

**CCNA-deeper delta:** Network+ asks u to recognize and reason about VLANs, trunks, routing, NAT/PAT, DHCP, and wireless security. **CCNA 200-301 goes deeper** by making u configure them on Cisco gear and troubleshoot the config live. skip CCNA for now unless networking itself is the job target.

**do this** - drill at [subnetipv4.com](https://subnetipv4.com/) until `/26`, `/27`, and `/28` feel boring. draw a tiny network with three VLANs (users, servers, guest Wi-Fi), one router/firewall, and NAT at the edge.

**measurable gate:** given a random IP in a `/26`, write the network ID, broadcast, first usable, last usable, and host count in **under 60 seconds**, then repeat for `/27` and `/28`. check each on subnetipv4.com.

**can u explain it?** - unaided: explain why a `/26` gives 62 usable hosts, including why the network and broadcast addresses are not assignable. then explain why VLANs reduce blast radius but do not magically encrypt traffic.

### network operations + troubleshooting meow (~15h)

**optional checkpoint map** - Network+ D3/D5; Security+ D4 operations later.

**the idea** - operations means keeping the network observable and documented; troubleshooting means changing one thing at a time instead of panic-clicking.

**how/why it actually works** - a network that cant be observed is basically a rumor. **syslog** records device events, **SNMP** polls device health, **NetFlow** summarizes who talked to whom, and diagrams/runbooks stop "tribal knowledge" from being the only map.

the CompTIA 7-step method exists to slow u down in a good way: identify the problem, establish a theory, test the theory, make a plan, implement, verify, document. the order matters because a random "fix" can hide the root cause or cause a second outage.

tools each answer a narrow question: `ping` tests reachability, `tracert`/`traceroute` shows path, `nslookup`/`dig` tests DNS, `netstat`/`ss` shows sockets, `nmap` maps listening services.

**words u gotta be able to say**
- **syslog / SNMP / NetFlow** - events / device polling / flow summary
- **SLA / baseline** - expected service level / normal behavior
- **runbook / network diagram** - repeatable steps / topology map
- **troubleshooting methodology** - ordered fault-finding process
- **reachability vs name resolution** - IP path vs DNS answer
- **listening service** - process waiting on a port

**study sources**
- [Professor Messer N10-009 course, Section 3: Network Operations](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#ced8446) - monitoring, documentation, operations. **free**
- [Professor Messer N10-009 course, Section 4: Network Security](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#012c566) - Network+ security controls before the CC/Security+ network-security cluster. **free**
- [Professor Messer N10-009 course, Section 5: Network Troubleshooting](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#c80f0f9) - biggest N10-009 domain. **free**
- [ExamCompass Network+ N10-009 practice tests](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests) - free practice tests + ports/acronym/topic quizzes. **free**
- [Jason Dion N10-009 Practice Exam Pack](https://www.diontraining.com/products/comptia-network-n10-009-practice-exam) - harder paid practice if u want exam confidence. **paid**

**do this** - run `ping`, `tracert`/`traceroute`, `nslookup` or `dig`, `netstat`/`ss`, and `nmap` against your own lab VM or a legal target you control. write one sentence for what each command proves and what it does **not** prove.

**measurable gate:** score **85%+ on 3 fresh ExamCompass N10-009 practice exams**, score **90%+** on the ports + OSI quizzes, and recite the CompTIA 7-step troubleshooting method in order. remember: D5 Troubleshooting is **24%**, the biggest Network+ domain, so this is not optional cleanup meow.

**can u explain it?** - unaided: explain why "establish a theory of probable cause" comes before "test the theory," and give one example where DNS is broken but IP routing still works.

---

## Blocks 2-5 - security fundamentals through labs + practice gates (~115h)

this is one learning path, not two cert silos.
u study the **superset** because the real mechanisms overlap, then u decide which exam checkpoint is worth paying for.
CC is optional proof now, not the free path itself meow.

**exact resource spine from RC1**
- [Professor Messer SY0-701 free course index](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/) - 121-video free course, organized by SY0-701 domains. **free**
- [Professor Messer SY0-701 YouTube playlist](https://www.youtube.com/playlist?list=PLG49S3nxzAnl4QDVqK-hOnoqcSKEIDDuv) - same course if YouTube is easier. **free**
- [ExamCompass Security+ SY0-701 practice tests](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) - use the current **SY0-701 Tests 1-24**, not retired SY0-601 sets. **free**
- [Professor Messer SY0-701 Pop Quiz: It's Pretty at Night](https://www.professormesser.com/security-plus/sy0-701/sy0-701-pop-quiz/its-pretty-at-night/) - verified singular `sy0-701-pop-quiz` slug example; dont use the plural pop-quizzes index. **free**
- [Messer SY0-701 Success Bundle](https://www.professormesser.com/sy0-701-success-bundle/) - current paid Messer practice bundle; this replaces old generic practice-exam links. **paid optional**
- [Dion Training SY0-701 Practice Exam Pack](https://www.diontraining.com/products/comptia-security-sy0-007-unlimited-practice-exam) - verified Dion link even though the slug says `sy0-007`; page content is SY0-701. **paid optional**
- [ISC2 CC Self-Study Resources](https://www.isc2.org/certifications/cc/cc-self-study-resources), [CC Practice Quiz](https://cloud.connect.isc2.org/cc-quiz), and [CC Flash Cards](https://cloud.connect.isc2.org/cc-flashcards) - free CC study aids, likely signup-gated. **free with signup**

**CC money note again:** the free-voucher program closed on **2026-05-20**.
the exam is now about **$199 + $50/yr AMF**.
use the free CC hub/quiz/flashcards plus these explain gates before u pay.

study order: **A -> D -> B -> C -> E -> F -> G -> H**.
that order is on purpose: foundations first, then network/security controls, then crypto and identity, then attacks, then operations, IR, and GRC.

- [ ] **Cluster A - Security Foundations & Governance Concepts** (~15h)
- [ ] **Cluster D - Networking & Network Security** (~14h)
- [ ] **Cluster B - Cryptography & PKI** (~14h)
- [ ] **Cluster C - Access Control & Identity (IAM)** (~16h)
- [ ] **Cluster E - Threats, Attacks, Vulnerabilities & Malware** (~16h)
- [ ] **Cluster F - Security Operations (monitoring, hardening, automation)** (~14h)
- [ ] **Cluster G - Incident Response, BC/DR & Resilience** (~12h)
- [ ] **Cluster H - GRC & Security Program Management** (~14h)

### Cluster A - Security Foundations & Governance Concepts meow (~15h)

**optional checkpoint map** - CC **D1 Security Principles**; SY0-701 **1.0 General Security Concepts** + **5.0 Security Program Management & Oversight**.

**deltas** - CIA/controls/AAA/governance = **both**. **CC only:** ISC2 **Code of Ethics** canons (memorize the 4 in order). **Security+ emphasis:** Zero Trust (control/data planes, PEP/PDP), gap analysis, honeypots/honeytokens.

**the idea** - security starts with knowing what promise a control is trying to protect: confidentiality, integrity, availability, identity, accountability, or risk reduction.

**how/why it actually works** - **Confidentiality** fails when someone reads data they shouldnt; encryption and access control reduce that.

**Integrity** fails when data changes without detection; hashes, MACs, signatures, approvals, and logs make tampering visible.

**Availability** fails when authorized users cant get service; redundancy, backups, rate limits, and recovery plans keep the service reachable.

**AAA** keeps identity decisions in order: authentication proves who u are, authorization decides what u may do, accounting records what happened.

**Zero Trust** says location is not trust. every request is evaluated through identity, device posture, context, policy, and least privilege. dw, this is just "verify the request every time," not spooky magic.

**words u gotta be able to say**
- **confidentiality / integrity / availability** - read control / change control / uptime
- **authenticity / non-repudiation** - genuine source / cannot deny action
- **threat / vulnerability / risk / exploit** - actor or event / weakness / likelihood x impact / use of weakness
- **control category** - managerial, operational, technical, physical
- **control type** - preventive, deterrent, detective, corrective, compensating, directive
- **AAA** - authentication, authorization, accounting
- **Zero Trust** - verify each request continuously
- **PEP / PDP** - enforcement point / decision point

**study sources (pick what fits your style)**
- [Professor Messer: Security Controls - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-controls-sy0-701/) - control categories and types. **free**
- [Professor Messer: The CIA Triad - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/the-cia-triad-sy0-701/) - confidentiality, integrity, availability. **free**
- [Professor Messer: Non-repudiation - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/non-repudiation-sy0-701/) - accountability property. **free**
- [Professor Messer: Zero Trust - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/zero-trust-sy0-701/) - Security+ emphasis. **free**
- [Professor Messer: Authentication, Authorization, and Accounting - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/authentication-authorization-and-accounting-sy0-701/) - AAA before IAM gets deeper. **free**

**do this** - take 3 fresh ExamCompass SY0-701 attempts from current Tests 1-24 that hit general security concepts. good starting picks from RC1 are [Test 1](https://www.examcompass.com/comptia-security-plus-practice-test-1-exam-sy0-701), [Test 8](https://www.examcompass.com/comptia-security-plus-practice-test-8-exam-sy0-701), and [Test 15](https://www.examcompass.com/comptia-security-plus-practice-test-15-exam-sy0-701). if sitting CC, also review the [ISC2 CC Self-Study Resources](https://www.isc2.org/certifications/cc/cc-self-study-resources).

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** AND recite the 4 ISC2 Code-of-Ethics canons in order unaided.

**can u explain it?** ✅ - say out loud the difference between a *vulnerability*, *threat*, and *risk* with one concrete example each. then name which CIA property is being protected by encryption, a hash, and a failover cluster.

### Cluster D - Networking & Network Security meow (~14h)

**optional checkpoint map** - CC **D4 Network Security**; SY0-701 **3.2 Security Architecture** + **4.5 Security Operations**.

**deltas** - **Big one:** **CC explicitly tests networking fundamentals** (OSI, TCP handshake, ports) because it has no Network+ prerequisite; Security+ **assumes** them and tests the *security controls* on top.

**the idea** - network security is the control layer on top of normal networking: filtering, segmentation, encrypted tunnels, wireless protection, and monitoring around packets that still have to route normally.

**how/why it actually works** - a **stateful firewall** tracks connection state, so an outbound TCP session can receive return traffic while an unrelated inbound SYN is blocked.

**Segmentation** splits trust zones so one compromised user machine does not sit in the same flat network as servers, admin tools, and guest Wi-Fi.

**IDS/IPS** watches traffic patterns or signatures; IDS alerts, IPS can block. placement matters because a sensor only sees traffic that passes through its view.

**VPN/IPsec/TLS** protect traffic over untrusted paths by authenticating peers and encrypting payloads. the network still routes packets; crypto makes the contents and peer identity safer.

**words u gotta be able to say**
- **OSI / TCP-IP** - layer models for network jobs
- **TCP handshake** - SYN, SYN-ACK, ACK setup
- **port / protocol** - service number / communication rule
- **stateful firewall** - allows traffic based on flow state
- **IDS / IPS** - detect only / detect and block
- **VLAN / segmentation / DMZ** - split broadcast/trust zones
- **VPN / IPsec / TLS** - encrypted tunnels or sessions
- **WPA3 / DNSSEC** - Wi-Fi protection / signed DNS records

**study sources (pick what fits your style)**
- [Professor Messer: Firewall Types - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/firewall-types-sy0-701/) - packet, stateful, next-gen, WAF. **free**
- [Professor Messer: Firewalls - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/firewalls-sy0-701/) - placement and policy. **free**
- [Professor Messer: Segmentation and Access Control - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/segmentation-and-access-control-sy0-701/) - VLANs, screened subnets, NAC ideas. **free**
- [TryHackMe: Intro to Networking](https://tryhackme.com/room/introtonetworking) - CC networking-fundamentals half if Block 1 was shaky. **freemium**
- [TryHackMe: Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics) - packet-capture practice for the TCP gate. **freemium**

**do this** - use the current [ExamCompass Security+ SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) for network-security questions, then capture or inspect one TCP connection in Wireshark and label SYN -> SYN-ACK -> ACK.

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** AND correctly label the TCP 3-way handshake from a live or saved Wireshark capture.

**can u explain it?** ✅ - explain why a stateful firewall can allow the return traffic of an outbound connection but block an unsolicited inbound one. then say why segmentation reduces blast radius but does not encrypt traffic.

### Cluster B - Cryptography & PKI meow (~14h)

**optional checkpoint map** - CC **D5 Security Operations**; SY0-701 **1.4 Cryptographic Solutions** + **3.3 Data Protection**.

**deltas** - sym/asym/hash/signatures/data-states = **both**. **Security+ deeper:** full PKI/certificate mechanics, cipher modes. **Security+ only:** obfuscation, steganography, blockchain, key stretching/salting detail.

**the idea** - crypto gives tools for secrecy, tamper detection, identity proof, and safe key agreement. the hard part is knowing which tool gives which property.

**how/why it actually works** - **symmetric encryption** uses one shared key and is fast enough for bulk data, but both sides need the same secret.

**Asymmetric crypto** uses a public/private keypair. a public key can verify a signature from the private key, or help establish a shared secret without sending that secret directly.

**Hashing** makes a fixed-size fingerprint. it does not hide data; it detects change. keyed hashes and signatures add authenticity.

**PKI** binds an identity to a public key through certificates. your browser trusts a root CA, verifies the intermediate chain, checks the server leaf certificate, then verifies the server owns the matching private key during the handshake.

**words u gotta be able to say**
- **cipher / key** - algorithm / secret parameter
- **symmetric / asymmetric** - shared key / keypair
- **hash / HMAC** - fingerprint / keyed integrity check
- **digital signature** - private-key sign, public-key verify
- **certificate / CA / PKI** - identity binding / issuer / trust system
- **chain of trust** - root to intermediate to leaf
- **OCSP / CRL** - revocation status checks
- **data at rest / in transit / in use** - stored / moving / being processed

**study sources (pick what fits your style)**
- [Professor Messer: Public Key Infrastructure - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/public-key-infrastructure-sy0-701/) - CA and trust model. **free**
- [Professor Messer: Encrypting Data - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/encrypting-data-sy0-701/) - symmetric/asymmetric/data protection. **free**
- [Professor Messer: Certificates - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/certificates-sy0-701/) - certificate fields and chains. **free**
- [Professor Messer: Blockchain Technology - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/blockchain-technology-sy0-701/) - **Security+ only** extra. **free**
- [Professor Messer: States of Data - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/states-of-data-sy0-701/) - at rest, in transit, in use. **free**

**do this** - use the current [ExamCompass Security+ SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) for crypto/PKI/data-state questions. while reviewing misses, write one sentence for which property the control gives: confidentiality, integrity, authentication, or non-repudiation.

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** for crypto/PKI/data-protection questions.

**can u explain it?** ✅ - walk the PKI chain: root CA -> intermediate CA -> leaf certificate -> signature checks -> browser trust decision. then say what OCSP/CRL are checking and why a hash alone is not encryption.

### Cluster C - Access Control & Identity (IAM) meow (~16h)

**optional checkpoint map** - CC **D3 Access Controls** + **D1 AAA**; SY0-701 **4.6 Identity and Access Management** + **1.2 Physical Security**.

**deltas** - models + least-privilege + SoD + physical = **both**. **Security+ deeper:** federation/SSO protocols, Kerberos, 802.1X/EAP.

**the idea** - identity says who the subject is; access control decides whether that subject can do this action to that object right now.

**how/why it actually works** - access decisions always have pieces: **subject**, **object**, **operation**, and **policy**. if the app only checks "logged in" but not "allowed for this object," access control breaks.

**DAC** lets owners grant permissions. **MAC** enforces labels the user cannot override. **RBAC** maps people to roles, then roles to permissions. **ABAC** evaluates attributes like device, location, time, object label, and action.

identity lifecycle matters because stale accounts are access bugs with usernames. provisioning gives access, deprovisioning removes it, reviews catch drift, and least privilege keeps roles small.

federation and SSO move trust between systems: one identity provider authenticates the user, then tokens/assertions let another app trust that result. useful, but now token handling and trust boundaries matter a lot qwq.

**words u gotta be able to say**
- **subject / object / operation** - actor / target / action
- **DAC / MAC / RBAC / ABAC** - owner / label / role / attribute model
- **least privilege** - only needed access
- **segregation of duties** - split risky powers
- **provisioning / deprovisioning** - grant / remove identity access
- **MFA factors** - know, have, are, where, behavior
- **federation / SSO** - trust identity across systems
- **Kerberos / LDAP / SAML / OAuth / 802.1X/EAP** - auth directory, token, and network-access protocols

**study sources (pick what fits your style)**
- [Professor Messer: Multifactor Authentication - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/multifactor-authentication-sy0-701/) - factor categories and MFA risk. **free**
- [Professor Messer: Access Controls - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/access-controls-sy0-701/) - models, rights, IAM terms. **free**
- [Professor Messer: Authentication, Authorization, and Accounting - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/authentication-authorization-and-accounting-sy0-701/) - AAA recap before the D3-heavy gate. **free**
- [ISC2 CC Practice Quiz](https://cloud.connect.isc2.org/cc-quiz) - CC-flavored identity/access check; likely signup-gated. **free with signup**

**do this** - use the current [ExamCompass Security+ SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) for access-control and IAM questions. make a tiny table with one real scenario each for DAC, MAC, RBAC, and ABAC.

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** for access control/IAM.

**can u explain it?** ✅ - explain when youd choose RBAC vs MAC vs DAC and why, with a one-line real scenario each. then take one RBAC scenario and add time/device/location conditions until it becomes ABAC.

### Cluster E - Threats, Attacks, Vulnerabilities & Malware meow (~16h)

**optional checkpoint map** - CC **D4 Network Security** + **D5 Security Operations**; SY0-701 **2.0 Threats, Vulnerabilities, and Mitigations**.

**deltas** - malware/social-eng/DoS/MITM = **both**. **Security+ only/deeper:** the full **threat-actor taxonomy** (nation-state, hacktivist, insider, etc. + motivations) and **specific named vulnerability classes** (buffer overflow, SQLi, race conditions, zero-day) - CC stays at "know the category," Security+ wants the mechanism.

**the idea** - an attack is normal system behavior pushed into an unsafe path. the job is to name which assumption broke.

**how/why it actually works** - **malware** is grouped by spread and payload: worms self-propagate, trojans pretend to be legit, ransomware encrypts/extorts, rootkits hide control, botnets coordinate many compromised hosts.

**Social engineering** attacks the human trust path: phishing, vishing, smishing, pretexting, urgency, authority, scarcity, and brand impersonation.

**DoS/DDoS** attacks availability by exhausting state, bandwidth, CPU, app workers, or upstream capacity. mitigation works by reducing state, filtering earlier, rate-limiting, or absorbing traffic.

**Buffer overflow** happens when code writes past a memory boundary. if overwritten memory influences control flow, the attacker may redirect execution. dw, later red-team material goes deeper; here u need the mechanism shape.

**words u gotta be able to say**
- **threat actor / motivation** - who is attacking and why
- **attack vector / attack surface** - path in / exposed area
- **malware family** - grouped by spread or payload
- **phishing / vishing / smishing** - email / voice / SMS social engineering
- **DoS / DDoS** - one-source / many-source availability attack
- **MITM/on-path** - attacker relays or alters traffic
- **buffer overflow / race condition** - memory boundary / timing bug
- **SQLi / XSS / zero-day** - query injection / browser script injection / unknown or unpatched vuln

**study sources (pick what fits your style)**
- [Professor Messer: Threat Actors - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/threat-actors-sy0-701/) - actor taxonomy and motivations. **free**
- [Professor Messer: Phishing - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/phishing-sy0-701/) - social engineering types. **free**
- [Professor Messer: An Overview of Malware - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/an-overview-of-malware-sy0-701/) - malware families. **free**
- [Professor Messer: Denial of Service - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/denial-of-service-sy0-701/) - DoS/DDoS mechanisms. **free**

**do this** - use the current [ExamCompass Security+ SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) for threats/vulnerabilities/mitigations. after each miss, write whether it was actor, vector, vulnerability type, malware type, or mitigation.

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** AND name the malware type + likely delivery vector from 5 short scenarios unaided.

**can u explain it?** ✅ - explain in one breath how a buffer overflow can hand control to an attacker. then explain how phishing can lead to a valid login that still becomes a security incident.

### Cluster F - Security Operations (monitoring, hardening, automation) meow (~14h)

**optional checkpoint map** - CC **D5 Security Operations**; SY0-701 **4.0 Security Operations**.

**deltas** - hardening/logging/data-handling = **both**. **Security+ only/deeper:** **SIEM**, formal **vulnerability management** cycle, **asset management**, **automation/orchestration (scripting)** - these are why SY0-701 D4 is 28% while CC D5 is only 18%.

**the idea** - security operations is the daily control loop: know what exists, harden it, patch it, log it, detect weirdness, and fix drift before it becomes an incident.

**how/why it actually works** - **asset management** starts the loop because u cant secure what u dont know exists.

**Secure baselines** reduce default risk by removing unused services, weak settings, default credentials, unnecessary admin rights, and permissive firewall rules.

**Vulnerability management** scans, prioritizes by risk, remediates, then verifies. a scan finding is not fixed until the fix is proven.

**SIEM** normalizes and correlates logs so one odd login, endpoint alert, and DNS query can become one investigation instead of three isolated lines. automation can enrich or route alerts, but bad automation just moves mistakes faster.

**words u gotta be able to say**
- **asset inventory** - what exists and who owns it
- **baseline / drift** - approved config / config moving away
- **patch management** - fixing known vulnerable code
- **vulnerability management** - find, prioritize, fix, verify
- **log source** - system producing event data
- **SIEM** - log collection, search, correlation
- **SOAR / automation** - orchestrated response workflows
- **data classification / retention / destruction** - sensitivity, storage time, disposal

**study sources (pick what fits your style)**
- [Professor Messer: Secure Baselines - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/secure-baselines-sy0-701/) - baseline concept. **free**
- [Professor Messer: Vulnerability Scanning - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/vulnerability-scanning-sy0-701/) - scan/triage cycle. **free**
- [Professor Messer: Penetration Testing - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/penetration-testing-sy0-701/) - where pentests fit in operations. **free**
- [Professor Messer: Security Monitoring - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-monitoring-sy0-701/) - monitoring/SIEM terms. **free**
- [Professor Messer: Hardening Techniques - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/hardening-techniques-sy0-701/) - reduce attack surface. **free**

**do this** - use the current [ExamCompass Security+ SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) for SecOps questions. also make a 6-row mini baseline for one Windows or Linux VM: accounts, services, firewall, updates, logs, backups.

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** for SecOps.

**can u explain it?** ✅ - describe what a SIEM does that plain log files dont, and name one thing a secure baseline removes from a fresh OS install.

### Cluster G - Incident Response, BC/DR & Resilience meow (~12h)

**optional checkpoint map** - CC **D2 BC/DR & Incident Response**; SY0-701 **4.8 Incident Response**, **3.4 Resilience**, and **5.2 Risk Metrics**.

**deltas** - IR lifecycle + BC/DR + backups + RTO/RPO = **both**. **Security+ deeper:** **digital forensics** and **architecture-level resilience** (hot/warm/cold sites, load balancing, clustering).

**the idea** - incidents are handled through a lifecycle; disasters are handled through continuity and recovery plans with measurable time and data-loss targets.

**how/why it actually works** - **PICERL** is the IR loop: Prepare, Identify, Contain, Eradicate, Recover, Lessons Learned.

containment stops spread. eradication removes the cause. recovery restores service. lessons learned feeds new controls so the same incident does not repeat.

**BCP** keeps the business operating during disruption; **DRP** restores technology after disruption.

**RTO** is max downtime. **RPO** is max data loss. backup design follows those numbers, not vibes. forensics adds evidence discipline: collect volatile evidence first when needed, preserve chain of custody, and dont clean up before u understand what happened.

**words u gotta be able to say**
- **event / incident / breach** - observed activity / harmful security event / confirmed exposure
- **PICERL** - prepare, identify, contain, eradicate, recover, lessons
- **BCP / DRP** - continuity plan / recovery plan
- **RTO / RPO** - max downtime / max data loss
- **MTTR / MTBF** - repair time / failure interval
- **hot / warm / cold site** - ready now / partial / basic recovery site
- **chain of custody** - evidence handling record
- **order of volatility** - collect most fragile evidence first

**study sources (pick what fits your style)**
- [Professor Messer: Incident Response - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/incident-response-sy0-701/) - IR phases. **free**
- [Professor Messer: Digital Forensics - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/digital-forensics-sy0-701/) - evidence and process. **free**
- [Professor Messer: Resiliency - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/resiliency-sy0-701/) - HA and architecture resilience. **free**
- [Professor Messer: Backups - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/backups-sy0-701/) - backup types and strategy. **free**

**do this** - use the current [ExamCompass Security+ SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) for IR/BCDR/resilience questions. write a 6-heading mini runbook for "phished user, credential used from a new country."

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** AND put the 6 PICERL phases in order and state RTO vs RPO in one sentence each.

**can u explain it?** ✅ - given an incident scenario, name which PICERL phase youre in and the next action. then say what evidence u preserve before changing the affected system.

### Cluster H - GRC & Security Program Management meow (~14h)

**optional checkpoint map** - CC **D1 Security Principles**; SY0-701 **5.0 Security Program Management & Oversight**.

**deltas** - risk/governance/awareness = **both**. **Security+ only/deeper:** third-party risk, formal audits/assessments, named frameworks. **CC only:** ISC2 Code of Ethics (already gated in Cluster A).

**the idea** - GRC is how an org decides which risks matter, what controls are required, and what evidence proves the controls actually exist.

**how/why it actually works** - **risk management** starts by identifying the asset, threat, vulnerability, likelihood, and impact. treatment choices are avoid, mitigate, transfer, or accept.

governance documents form a stack: **policies** state intent, **standards** define mandatory requirements, **procedures** give steps, and **guidelines** suggest good practice.

third-party risk exists because vendors become part of your trust boundary. audits and assessments compare reality to requirements and produce evidence.

frameworks like **NIST CSF 2.0** and **ISO/IEC 27001:2022** give shared language so controls, risks, owners, and evidence dont float around as vibes mhm.

**words u gotta be able to say**
- **risk appetite / tolerance** - how much risk org accepts
- **avoid / mitigate / transfer / accept** - four treatment choices
- **policy / standard / procedure / guideline** - intent / requirement / steps / advice
- **BIA** - business impact analysis
- **third-party risk** - vendor or supply-chain risk
- **audit / assessment / attestation** - formal check / evaluation / evidence statement
- **NIST CSF 2.0** - govern, identify, protect, detect, respond, recover
- **ISO/IEC 27001:2022** - information security management system standard

**study sources (pick what fits your style)**
- [Professor Messer: Security Policies - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-policies-sy0-701/) - policy/standard/procedure stack. **free**
- [Professor Messer: Risk Management - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/risk-management-sy0-701/) - risk vocabulary and treatment. **free**
- [Professor Messer: Third-party Risk Assessment - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/third-party-risk-assessment-sy0-701/) - vendor risk. **free**
- [Professor Messer: Business Impact Analysis - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/business-impact-analysis-sy0-701/) - BIA/RTO/RPO tie-in. **free**
- [Professor Messer: Audits and Assessments - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/audits-and-assessments-sy0-701/) - evidence and assessments. **free**
- [Professor Messer: Security Awareness - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-awareness-sy0-701/) - awareness and human-risk controls. **free**

**do this** - use the current [ExamCompass Security+ SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) for governance/risk/program-management questions. then write one mini risk note: asset, threat, vulnerability, impact, likelihood, treatment, control, evidence.

**measurable gate:** **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** for governance/risk.

**can u explain it?** ✅ - for a given risk, pick a treatment (avoid/mitigate/transfer/accept) and justify it in one sentence. then explain the difference between a policy and a procedure.

---

## Block 6 - optional exam checkpoint sprint (~10h)

this is where u decide whether to book exams.
dont book because u watched videos.
book when the gates say u are ready meow

### Network+ N10-009 readiness

**book only if all are true:**
- [ ] `/26`, `/27`, `/28` subnet drills pass under 60s each on paper, checked with [subnetipv4.com](https://subnetipv4.com/).
- [ ] **85%+ on 3 fresh** [ExamCompass N10-009 practice exams](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests).
- [ ] **90%+** on OSI + TCP/UDP ports quizzes.
- [ ] can recite the CompTIA 7-step troubleshooting method in order.
- [ ] if using Dion, **85%+ on 2 fresh** [Jason Dion N10-009 practice exams](https://www.diontraining.com/products/comptia-network-n10-009-practice-exam).

**can u explain it?** - explain OSI layers with one protocol per layer, why `/26` gives 62 usable hosts, and why a stateful firewall can allow return traffic while blocking unsolicited inbound traffic.

### ISC2 CC readiness (optional paid exam)

**exam money note:** about **$199 + $50/yr AMF** now. no new free 1MCC vouchers after **2026-05-20**. use the exam only if u want that checkpoint; dont treat it like it magically fixes a thin resume.

**free checkpoint before paying:**
- [ ] clusters **A, D, B, C, F, G, H** are explainable without notes and map to all 5 CC domains: Security Principles, BC/DR & IR, Access Controls, Network Security, Security Operations.
- [ ] completed [ISC2 CC Practice Quiz](https://cloud.connect.isc2.org/cc-quiz) and reviewed [CC Flash Cards](https://cloud.connect.isc2.org/cc-flashcards).
- [ ] can recite the ISC2 Code of Ethics canons in order if sitting the exam.
- [ ] if testing on/after **2026-09-01**, re-check the [CC Exam Outline](https://www.isc2.org/certifications/cc/cc-certification-exam-outline).

**can u explain it?** - without notes, map one example control to each CIA property, one access-control model to a real scenario, and one incident scenario to the correct PICERL phase.

### Security+ SY0-701 readiness

**book only if all are true:**
- [ ] all 8 merged-study clusters (**A, D, B, C, E, F, G, H**) have both gates passed: **85%+ on 3 fresh ExamCompass SY0-701 attempts on the domain-relevant sets** + the cluster's `can u explain it?`.
- [ ] reviewed weak areas through the relevant [Professor Messer SY0-701 course sections](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/) and per-episode deep links above, not by marathon-watching the whole course again.
- [ ] for final mixed practice, **85%+ on 3 fresh** [ExamCompass SY0-701 Tests 1-24](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests).
- [ ] if buying practice, use the current [Messer SY0-701 Success Bundle](https://www.professormesser.com/sy0-701-success-bundle/) or [Dion SY0-701 Practice Exam Pack](https://www.diontraining.com/products/comptia-security-sy0-007-unlimited-practice-exam). dont use old generic Messer practice-exam links.
- [ ] if using Messer free pop quizzes, use the singular `sy0-701-pop-quiz` posts linked from episode pages, like the verified example above; avoid the old plural index.
- [ ] can label whether each weak area is SY0-701 **1.0 concepts**, **2.0 threats**, **3.0 architecture**, **4.0 operations**, or **5.0 program management**.

**can u explain it?** - explain one complete story: attacker phishes creds -> logs in from unusual country -> accesses a forbidden object -> SIEM alert fires -> IR contains account -> risk owner updates policy/control. name the mechanism at each step.

---

## exit check - done with Goal 2

- [ ] Network+ gate passed, or u already had CCNA-level networking and can prove it with the subnet/troubleshooting explain gates.
- [ ] merged CC + Security+ clusters **A, D, B, C, E, F, G, H** all passed both gates: the ExamCompass measurable gate and the `can u explain it?` gate.
- [ ] CC domains are explainable; paid CC exam is optional and correctly understood as ~$199 + AMF, not free.
- [ ] Security+ readiness gate passed, or u know exactly which SY0-701 domain and cluster are still weak.
- [ ] completed the hands-on artifacts inside this file: Wireshark TCP handshake labels, one VM baseline, one IR runbook, and one risk note.
- [ ] can explain CIA, Zero Trust, stateful firewalls, TLS/PKI, authn vs authz, DAC/MAC/RBAC/ABAC, malware and vulnerability classes, SIEM basics, PICERL, RTO/RPO, and risk treatment choices.

**final can u explain it?** - unaided, write or say a 10-minute walkthrough:

> "a user visits an HTTPS site from a segmented corporate network. explain DNS, TCP, TLS, cert validation, firewall/state, identity/authz, logging, what a MITM would try, why TLS stops it, what a SIEM would see if creds were stolen, and how IR responds."

if u can do that, ur ready for [Scripting, Logs & CTF](03-scripting-ctf.md).
if not, the missing nouns tell u exactly which block to redo.
dw, this is the point - no getting lost meow

---

[<- Goal 1: Foundations](01-foundations.md) | [Back to hub](README.md) | [Next: Scripting, Logs & CTF ->](03-scripting-ctf.md)
