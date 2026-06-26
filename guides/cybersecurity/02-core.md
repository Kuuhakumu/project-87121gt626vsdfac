# Goal 2: Networking & Security Core meow (~180h)

> **goal:** build the network floor, then learn the security mechanisms on top of it: CIA, crypto/TLS, identity, access control, attacks, operations, IR, and risk.
>
> **cert checkpoints layered on top:** **CompTIA Network+ (N10-009)** -> **ISC2 CC** (optional paid exam) -> **CompTIA Security+ (SY0-701)**.

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
- [ ] **Block 2 - security foundations** (~15h): CIA, controls, AAA, Zero Trust, CC-only ethics note.
- [ ] **Block 3 - crypto + identity + access control** (~40h): TLS/PKI, password hashing, authn/authz, DAC/MAC/RBAC/ABAC.
- [ ] **Block 4 - attacks + CTF thread** (~30h): network attacks, malware, web vuln classes, Natas + PortSwigger.
- [ ] **Block 5 - operations + IR + GRC** (~30h): hardening, logging, monitoring, BC/DR, risk, governance.
- [ ] **Block 6 - cert readiness sprint** (~10h): Network+ gate, CC optional gate, Security+ gate.
- [ ] **exit check** - can explain the whole chain: normal network -> control -> attack -> detection -> response.

---

## cert-domain map so u know why each block exists

### Network+ N10-009 map

| N10-009 domain | Weight | Covered in this file |
|---|---:|---|
| 1.0 Networking Concepts | 23% | packets/ports/protocols, OSI/TCP-IP, IPv4/IPv6, DNS/DHCP/NTP, subnetting |
| 2.0 Network Implementation | 20% | cabling, Wi-Fi/WPA3, VLANs, routing/switching concepts, NAT/PAT |
| 3.0 Network Operations | 19% | monitoring, syslog/SNMP/NetFlow, documentation, SLAs |
| 4.0 Network Security | 14% | segmentation, IDS/IPS concepts, firewalls, zero trust, hardening |
| 5.0 Network Troubleshooting | 24% | 7-step method, `ping`, `tracert`, `nslookup`, `dig`, `ipconfig`/`ip`, `netstat`, `nmap` |

### merged CC + Security+ map

| Study cluster | ISC2 CC domain(s) | SY0-701 domain(s) | delta so ur not guessing |
|---|---|---|---|
| security foundations | D1 Security Principles | 1.0, parts of 5.0 | both; ISC2 Code of Ethics is **CC only** |
| crypto + PKI | D5 Security Operations | 1.4, 3.3 | both; Security+ goes deeper on PKI/certs/data states |
| access control + IAM | D3 Access Controls, D1 AAA | 4.6, 1.2 | both; Security+ goes deeper on SSO/federation/Kerberos/802.1X |
| networking + network security | D4 Network Security | 3.2, 4.5 | CC tests networking fundamentals; Security+ assumes them |
| threats + vulnerabilities | D4 attacks, D5 awareness | 2.0 | Security+ goes deeper on threat actors and vuln classes |
| security operations | D5 Security Operations | 4.0 | Security+ goes deeper on SIEM, vuln mgmt, automation |
| IR + BC/DR | D2 BC/DR & IR | 4.8, 3.4, 5.2 | Security+ goes deeper on forensics/resilience metrics |
| GRC + program mgmt | D1 risk/governance | 5.0 | Security+ goes deeper on third-party risk, audits, frameworks |

---

## Block 1 - networking floor (~55h)

- [ ] packets, ports, and protocols (~18h)
- [ ] subnetting, switching, routing, and wireless (~22h)
- [ ] network operations + troubleshooting (~15h)

### packets, ports, and protocols meow (~18h)

**cert map** - Network+ D1/D5; CC D4; this is the floor Security+ leans on.

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
- [Professor Messer N10-009 course, Section 1: Networking Concepts](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/) - exact Network+ course index; Section 1 maps to D1. **free**
- [TryHackMe: Intro to Networking](https://tryhackme.com/room/introtonetworking) - guided OSI/ping/traceroute room. **freemium** (bot-blocked in checks, works in browser)
- [TryHackMe: Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics) - packet-capture practice. **freemium** (bot-blocked in checks, works in browser)
- [Professor Messer N10-009 YouTube playlist](https://www.youtube.com/playlist?list=PLG49S3nxzAnl_tQe3kvnmeMid0mjF8Le8) - same course if YouTube is easier. **free**

**do this** - complete **TryHackMe Intro to Networking** and **Wireshark: The Basics**, then capture or inspect one HTTP/HTTPS session and label where DNS, TCP, TLS, and HTTP show up.

**measurable gate:** score **90%+** on the [ExamCompass Network+ OSI Reference Model quiz and TCP/UDP ports quiz](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests), and correctly label the SYN -> SYN-ACK -> ACK in a packet capture.

**can u explain it?** - unaided: explain what happens when a client opens `https://example.com`, naming DNS -> TCP -> TLS -> HTTP and saying what each layer is responsible for. then explain why a switch, router, and firewall are not the same device.

### subnetting, switching, routing, and wireless meow (~22h)

**cert map** - Network+ D1/D2; CC D4; Security+ D3.2/4.5 security controls later.

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
- [Professor Messer N10-009 course, Section 2: Network Implementation](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/) - cabling, Wi-Fi, routing/switching, NAT/PAT. **free**

**do this** - drill at [subnetipv4.com](https://subnetipv4.com/) until `/26`, `/27`, and `/28` feel boring. draw a tiny network with three VLANs (users, servers, guest Wi-Fi), one router/firewall, and NAT at the edge.

**measurable gate:** given a random IP in a `/26`, write the network ID, broadcast, first usable, last usable, and host count in **under 60 seconds**, then repeat for `/27` and `/28`. check each on subnetipv4.com.

**can u explain it?** - unaided: explain why a `/26` gives 62 usable hosts, including why the network and broadcast addresses are not assignable. then explain why VLANs reduce blast radius but do not magically encrypt traffic.

### network operations + troubleshooting meow (~15h)

**cert map** - Network+ D3/D5; Security+ D4 operations later.

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
- [Professor Messer N10-009 course, Section 3: Network Operations](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/) - monitoring, documentation, operations. **free**
- [Professor Messer N10-009 course, Section 5: Network Troubleshooting](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/) - biggest N10-009 domain. **free**
- [ExamCompass Network+ N10-009 practice tests](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests) - free practice tests + ports/acronym/topic quizzes. **free**
- [Jason Dion N10-009 Practice Exam Pack](https://www.diontraining.com/products/comptia-network-n10-009-practice-exam) - harder paid practice if u want exam confidence. **paid**

**do this** - run `ping`, `tracert`/`traceroute`, `nslookup` or `dig`, `netstat`/`ss`, and `nmap` against your own lab VM or a legal target you control. write one sentence for what each command proves and what it does **not** prove.

**measurable gate:** score **85%+ on 3 fresh ExamCompass N10-009 practice exams**, score **90%+** on the ports + OSI quizzes, and recite the 7-step troubleshooting method in order.

**can u explain it?** - unaided: explain why "establish a theory of probable cause" comes before "test the theory," and give one example where DNS is broken but IP routing still works.

---

## Block 2 - security foundations (~15h)

- [ ] CIA, controls, AAA, and Zero Trust (~15h)

### CIA, controls, AAA, and Zero Trust meow (~15h)

**cert map** - CC D1; Security+ 1.0 and parts of 5.0; Network+ D4 vocabulary.

**heads up** - CIA/controls/AAA are both CC and Security+. **ISC2 Code of Ethics is CC only.** Zero Trust, gap analysis, honeypots/honeytokens are Security+ emphasis.

**the idea** - security is not one single "safe" sticker. **Confidentiality**, **Integrity**, and **Availability** are separate guarantees, and different controls protect each one.

**how/why it actually works** - confidentiality fails when someone reads data they shouldnt, even if nothing changed. encryption and access control protect it.

integrity fails when data changes without detection, even if nobody can read it. hashes, MACs, signatures, and audit logs protect it.

availability fails when authorized users cant get service. redundancy, backups, rate limits, failover, and DDoS defenses protect it.

**AAA** keeps identity decisions orderly: authentication proves who u are, authorization decides what u can do, and accounting records what happened. **Zero Trust** is the design rule that no network location is automatically trusted; each request is evaluated using identity, device posture, context, and least privilege.

**words u gotta be able to say**
- **confidentiality** - only authorized reading
- **integrity** - unauthorized changes detectable
- **availability** - service reachable when needed
- **authenticity** - identity/source is genuine
- **non-repudiation** - action cant be credibly denied
- **threat / vulnerability / risk / exploit** - actor/capability / weakness / likelihood x impact / use of weakness
- **preventive / detective / corrective control** - stops / notices / fixes
- **AAA** - authentication, authorization, accounting

**study sources**
- [Professor Messer: Security Controls - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-controls-sy0-701/) - control categories/types. **free**
- [Professor Messer: The CIA Triad - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/the-cia-triad-sy0-701/) - CIA + examples. **free**
- [Professor Messer: Non-repudiation - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/non-repudiation-sy0-701/) - accountability property. **free**
- [Professor Messer: Zero Trust - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/zero-trust-sy0-701/) - Security+ emphasis. **free**
- [ISC2 CC Exam Outline](https://www.isc2.org/certifications/cc/cc-certification-exam-outline) + [CC self-study resources](https://www.isc2.org/certifications/cc/cc-self-study-resources) - CC blueprint and free study aids; exam itself is paid. **free/freemium**

**do this** - solve these two PortSwigger labs:
- [Unprotected admin functionality](https://portswigger.net/web-security/access-control/lab-unprotected-admin-functionality)
- [User ID controlled by request parameter](https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter)

**measurable gate:** both labs show **Solved**, and u can label which CIA property each lab violated. then score **85%+ on 3 fresh ExamCompass SY0-701 attempts** that include general-security/concepts questions.

**can u explain it?** - unaided: give one attack that breaks only integrity and one that breaks only availability. for each, name a control that would have reduced the risk.

---

## Block 3 - crypto + identity + access control (~40h)

- [ ] cryptography, TLS, and PKI (~14h)
- [ ] authentication + password hashing (~12h)
- [ ] access-control models + IAM (~14h)

### cryptography, TLS, and PKI meow (~14h)

**cert map** - CC D5 and D4; Security+ 1.4 and 3.3.

**heads up** - both certs test symmetric/asymmetric/hash/signatures. Security+ goes deeper on PKI, certificate status, data states, obfuscation, steganography, and blockchain.

**the idea** - crypto gives three core tools: symmetric encryption for fast secrecy, public-key crypto for identity/key exchange/signatures, and hashes for tamper-evident fingerprints. not magic, just carefully used math.

**how/why it actually works** - **symmetric encryption** uses one shared key and is fast enough for bulk traffic, but key-sharing is the hard part.

**asymmetric crypto** uses a public/private keypair. a public key can verify something signed by the private key, or help establish a shared secret without sending that secret directly.

**hashes** are one-way fixed-length fingerprints. change one bit, and the digest changes wildly. hashes support integrity checks, MACs, signatures, and password storage when wrapped in a slow KDF.

**TLS 1.3** combines them: ClientHello and ServerHello exchange supported suites and ephemeral key shares; both sides derive session keys; the server presents a certificate chain binding its domain to a public key; CertificateVerify proves it owns the matching private key; Finished messages MAC the handshake transcript. after that, AEAD encrypts and authenticates traffic. thats why proper HTTPS gives confidentiality, integrity, and server authentication even on a hostile network.

**words u gotta be able to say**
- **cipher / key** - algorithm / secret parameter
- **symmetric / asymmetric** - shared key / keypair
- **hash / MAC / HMAC** - fingerprint / keyed integrity check / hash-based MAC
- **digital signature** - private-key sign, public-key verify
- **certificate / CA / PKI** - identity-key binding / issuer / trust system
- **AEAD** - encryption plus integrity tag
- **Diffie-Hellman** - shared secret over public channel
- **forward secrecy** - old sessions survive future key theft

**study sources**
- [Professor Messer: Public Key Infrastructure - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/public-key-infrastructure-sy0-701/) - PKI overview. **free**
- [Professor Messer: Encrypting Data - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/encrypting-data-sy0-701/) - symmetric/asymmetric/data protection. **free**
- [Professor Messer: Certificates - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/certificates-sy0-701/) - leaf/intermediate/root certs. **free**
- [CryptoHack: Introduction to CryptoHack](https://cryptohack.org/courses/intro/) - beginner encoding/XOR crypto course. **free**
- [CryptoHack: Hash Functions challenges](https://cryptohack.org/challenges/hashes/) - hashes by doing. **free**

**do this** - complete **CryptoHack: Introduction to CryptoHack** and the first **3 Hash Functions** challenges. then run [SSL Labs Server Test](https://www.ssllabs.com/ssltest/) against one HTTPS site and compare cert behavior against [badssl.com](https://badssl.com/).

**measurable gate:** CryptoHack intro shows complete, 3 hash challenges solved, and your SSL Labs notes identify the certificate chain, negotiated TLS version, and whether forward secrecy is present.

**can u explain it?** - unaided: walk the TLS 1.3 handshake and say which step gives confidentiality, which step gives integrity, which step gives authentication, and why stealing the server key later should not decrypt captured past sessions.

### authentication + password hashing meow (~12h)

**cert map** - CC D3 and D1 AAA; Security+ 4.6 and 1.2; CC/Security+ D5 crypto overlap.

**heads up** - both certs test auth factors and AAA. Security+ goes deeper on federation, SSO, Kerberos, 802.1X/EAP, and password-attack mitigations.

**the idea** - **authentication** proves who u are; **authorization** decides what u can do; password storage is about surviving the day the database leaks. grim, but realistic qwq.

**how/why it actually works** - a login request authenticates the user once, but authorization has to happen on every sensitive action and every object. if the app checks "is logged in" but not "is this your object," u get IDOR/broken access control.

MFA requires different factor categories: something u know, have, are, somewhere u are, or something u do. two passwords are not MFA. FIDO2/WebAuthn is stronger because the authenticator signs an origin-bound challenge, so a fake site cant easily reuse it elsewhere.

passwords must not be stored raw. a **salt** is a unique random value stored beside the hash, so identical passwords produce different hashes and rainbow tables stop scaling. a slow adaptive KDF like **bcrypt**, **scrypt**, or **Argon2** makes every guess expensive; a **pepper** is an optional secret kept outside the database.

**words u gotta be able to say**
- **authentication / authorization** - who u are / what u may do
- **accounting** - record of what happened
- **MFA factor** - know/have/are/location/behavior category
- **TOTP / FIDO2 / WebAuthn** - time code / phishing-resistant challenge signing
- **hash / KDF** - fast fingerprint / deliberately slow password hash
- **salt / pepper** - unique public random / secret app-wide value
- **rainbow table** - precomputed hash lookup
- **rate limiting / lockout** - slows or blocks guesses

**study sources**
- [Professor Messer: Authentication, Authorization, and Accounting - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/authentication-authorization-and-accounting-sy0-701/) - AAA cleanly explained. **free**
- [Professor Messer: Multifactor Authentication - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/multifactor-authentication-sy0-701/) - factor categories. **free**
- [PortSwigger: Authentication vulnerabilities](https://portswigger.net/web-security/authentication) - auth bug explanations + labs. **free**
- [TryHackMe: Crack the Hash](https://tryhackme.com/room/crackthehash) - hash identification/cracking room. **freemium** (exact room verified; needs login)

**do this** - solve these:
- [PortSwigger: Username enumeration via different responses](https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses)
- [PortSwigger: Password brute-force via password change](https://portswigger.net/web-security/authentication/other-mechanisms/lab-password-brute-force-via-password-change)
- [TryHackMe: Crack the Hash](https://tryhackme.com/room/crackthehash), Task 1 Level 1

**measurable gate:** both PortSwigger labs show **Solved**, TryHackMe Task 1 answers are accepted, and u can identify whether a given example hash is unsalted fast hash vs salted password hash.

**can u explain it?** - unaided: explain why a stolen DB of salted bcrypt hashes is harder to crack than unsalted SHA-256. name both effects: no shared rainbow table and each guess is slow. then state the difference between authn and authz in one sentence.

### access-control models + IAM meow (~14h)

**cert map** - CC D3; Security+ 4.6 and 1.2.

**heads up** - DAC/MAC/RBAC/least privilege/physical controls are both. Security+ goes deeper on federation, SSO, Kerberos, SAML/OAuth, and 802.1X.

**the idea** - access control is the rule system that decides whether a subject can perform an operation on an object. tiny sentence, huge job.

**how/why it actually works** - **DAC** lets the owner decide permissions, like UNIX file permissions or NTFS ACLs. flexible, but malware running as the user inherits that user's access.

**MAC** uses centrally enforced labels the user cant override, like classified systems or SELinux/AppArmor policy. rigid, but strong when policy must beat user preference.

**RBAC** assigns permissions to roles, then users to roles. this scales in businesses because "help desk technician" or "billing admin" is easier to manage than one-off permissions for everyone.

**ABAC** decides from attributes: subject, object, action, and environment. "doctor can read this chart only during shift from a managed device for a patient on their ward" is ABAC, not simple RBAC.

**words u gotta be able to say**
- **subject / object / operation** - actor / thing / action
- **ACL / capability** - per-object permissions / per-subject token
- **DAC** - owner-controlled permissions
- **MAC** - mandatory labels/policy
- **RBAC** - permissions through roles
- **ABAC** - attributes/context decide
- **least privilege** - only the access needed
- **separation of duties** - split risky powers across people

**study sources**
- [Professor Messer: Access Controls - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/access-controls-sy0-701/) - Security+ IAM/access-control coverage. **free**
- [PortSwigger: Access control vulnerabilities](https://portswigger.net/web-security/access-control) - broken access-control mechanisms + labs. **free**
- [OverTheWire: Natas](https://overthewire.org/wargames/natas/) - browser-only web security wargame; starts with view-source/cookies/auth. **free**

**do this** - solve these:
- [PortSwigger: User role controlled by request parameter](https://portswigger.net/web-security/access-control/lab-user-role-controlled-by-request-parameter)
- [PortSwigger: URL-based access control can be circumvented](https://portswigger.net/web-security/access-control/lab-url-based-access-control-can-be-circumvented)
- [OverTheWire Natas](https://overthewire.org/wargames/natas/) levels **0-6**

**measurable gate:** both PortSwigger labs show **Solved** and Natas level 6 is cleared. write one note naming the intended access model and the failed enforcement point for each PortSwigger lab.

**can u explain it?** - unaided: choose an access model for a hospital records system and justify it. then change the rule to "only during shift, only assigned ward, only managed device" and explain why the answer becomes ABAC.

---

## Block 4 - attacks + CTF thread (~30h)

- [ ] network attacks + defenses (~16h)
- [ ] threats, malware, and web vulnerability classes (~14h)

### network attacks + defenses meow (~16h)

**cert map** - CC D4; Security+ 2.0, 3.2, 4.5; Network+ D4.

**the idea** - network attacks abuse trust assumptions in protocols: who owns this MAC, who answered DNS, who is really in the middle, and whether this message is fresh.

**how/why it actually works** - **ARP spoofing** works because ARP replies are not authenticated; a host can cache "gateway IP is at my MAC" and send traffic to the attacker.

**MITM/on-path** attacks relay traffic between two parties. TLS is the fix because the certificate chain authenticates the server, CertificateVerify proves private-key possession, and AEAD/Finished MACs detect tampering.

**replay** attacks resend a valid captured message. nonces, timestamps, sequence numbers, and session binding stop old messages from being accepted as new.

**DoS/DDoS** attacks availability. SYN floods fill half-open connection state; SYN cookies avoid keeping state until the final ACK. amplification attacks spoof the victim as source and make reflectors send bigger replies at the victim.

**words u gotta be able to say**
- **spoofing** - forged identity a protocol trusts
- **ARP poisoning** - fake MAC mapping on a LAN
- **MITM/on-path** - attacker relays/reads/alters traffic
- **replay** - resend captured valid message
- **nonce / timestamp / sequence** - freshness controls
- **DoS / DDoS** - one-source / many-source availability attack
- **SYN flood / SYN cookies** - half-open exhaustion / stateless defense
- **HSTS / DNSSEC / DAI** - HTTPS-only / signed DNS / switch ARP defense

**study sources**
- [Professor Messer: Denial of Service - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/denial-of-service-sy0-701/) - DoS/DDoS exam framing. **free**
- [Professor Messer: Firewall Types - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/firewall-types-sy0-701/) - packet/state/app firewalls. **free**
- [Professor Messer: Firewalls - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/firewalls-sy0-701/) - placement and policy. **free**
- [Professor Messer: Segmentation and Access Control - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/segmentation-and-access-control-sy0-701/) - VLANs/segmentation/security zones. **free**
- [CyberDefenders: PacketMaze](https://www.cyberdefenders.org/blueteam-ctf-challenges/packetmaze/) - packet-analysis blue-team CTF. **free**

**do this** - complete **CyberDefenders PacketMaze**, then use [badssl.com](https://badssl.com/) to predict which bad certificate cases your browser blocks and why.

**measurable gate:** PacketMaze challenge questions are accepted by the platform, and your badssl notes correctly classify expired, self-signed, wrong-host, and revoked-style certificate failures.

**can u explain it?** - unaided: walk an ARP-spoof -> MITM chain end to end, then explain why proper TLS still protects the session even if the attacker sees every packet.

### threats, malware, and web vulnerability classes meow (~14h)

**cert map** - CC D4/D5; Security+ 2.0.

**heads up** - malware, social engineering, DoS, and MITM are both. Security+ goes deeper on threat actors, motivations, SQLi, XSS, race conditions, buffer overflow, memory injection, and zero-day language.

**the idea** - a vulnerability is a condition that lets normal system behavior produce an unsafe result. thats the lens: "what assumption broke?"

**how/why it actually works** - **malware** is categorized by how it spreads and what it does: viruses attach to files, worms self-propagate, trojans masquerade as legit, ransomware encrypts/extorts, rootkits hide control, botnets coordinate many machines.

**SQL injection** happens when untrusted input becomes part of a query instead of data. the database obeys a query that the developer didnt mean to build.

**XSS** happens when untrusted input becomes executable script in another user's browser. the browser runs it because it came from a trusted site context.

**buffer overflow** happens when a program writes past a memory boundary and overwrites adjacent state; if that state controls execution flow, the attacker may redirect execution. dw this gets deeper later - rn u just need the mechanism shape.

**words u gotta be able to say**
- **threat actor / vector / surface** - who / path / exposed area
- **malware family** - grouped by spread/payload behavior
- **phishing / vishing / smishing** - email / voice / SMS social engineering
- **SQLi** - input becomes database query syntax
- **XSS** - input becomes browser-executed script
- **buffer overflow** - write past memory boundary
- **zero-day** - unknown/unpatched vuln in use
- **mitigation** - control that reduces likelihood or impact

**study sources**
- [Professor Messer: Threat Actors - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/threat-actors-sy0-701/) - actors and motivations. **free**
- [Professor Messer: Phishing - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/phishing-sy0-701/) - social engineering types. **free**
- [Professor Messer: An Overview of Malware - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/an-overview-of-malware-sy0-701/) - malware taxonomy. **free**
- [PortSwigger: SQL injection labs](https://portswigger.net/web-security/sql-injection) - CTF-style SQLi targets. **free**
- [PortSwigger: Cross-site scripting labs](https://portswigger.net/web-security/cross-site-scripting) - CTF-style XSS targets. **free**

**do this** - solve:
- [PortSwigger: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data](https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data)
- [PortSwigger: SQL injection vulnerability allowing login bypass](https://portswigger.net/web-security/sql-injection/lab-login-bypass)
- [PortSwigger: Reflected XSS into HTML context with nothing encoded](https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded)
- [OverTheWire Natas](https://overthewire.org/wargames/natas/) levels **7-15**

**measurable gate:** all 3 PortSwigger labs show **Solved**, Natas level 15 is cleared, and u can classify 5 short scenarios by malware/vuln type without notes.

**can u explain it?** - unaided: explain the difference between SQLi and XSS by naming where the attack executes (database vs browser). then explain, at a high level, how a buffer overflow can affect control flow.

---

## Block 5 - operations + IR + GRC (~30h)

- [ ] hardening, logging, and monitoring (~12h)
- [ ] incident response, BC/DR, and resilience (~10h)
- [ ] risk, governance, and program management (~8h)

### hardening, logging, and monitoring meow (~12h)

**cert map** - CC D5; Security+ D4 (the heaviest SY0-701 domain).

**heads up** - hardening, logging, data handling, and patching are both. Security+ goes deeper on SIEM, asset management, vulnerability management, and automation/orchestration.

**the idea** - security operations turns controls into daily habits: reduce exposed services, keep systems patched, collect logs, detect weird behavior, and document what changed. very unglamorous, very real.

**how/why it actually works** - **hardening** removes default risk: unused services, default credentials, permissive firewall rules, weak TLS settings, unnecessary admin rights.

**patch/config management** keeps known bugs from staying exploitable and keeps systems from drifting away from a baseline.

**logging** records events; a **SIEM** normalizes and correlates logs across systems so one weird login, DNS query, and endpoint alert can become one investigation instead of three isolated lines.

**words u gotta be able to say**
- **baseline / drift** - approved config / config moving away
- **patch management** - fixing known vulnerable code
- **asset inventory** - what exists and who owns it
- **vulnerability management** - find, prioritize, remediate, verify
- **log source** - system producing events
- **SIEM** - log collection/correlation/search platform
- **SOAR** - workflow automation around alerts
- **data classification** - label by sensitivity/handling need

**study sources**
- [Professor Messer: Secure Baselines - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/secure-baselines-sy0-701/) - baseline concept. **free**
- [Professor Messer: Hardening Techniques - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/hardening-techniques-sy0-701/) - reduce attack surface. **free**
- [Professor Messer: Vulnerability Scanning - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/vulnerability-scanning-sy0-701/) - scan/triage cycle. **free**
- [Professor Messer: Security Monitoring - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-monitoring-sy0-701/) - monitoring/SIEM terms. **free**
- [ExamCompass Security+ SY0-701 practice tests](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests) - domain practice. **free**

**do this** - make a one-page hardening checklist for a fresh Windows or Linux VM: disable one unused service, enable/update firewall policy, list local admin/root-equivalent users, confirm updates, and identify where auth/system logs live.

**measurable gate:** complete the checklist on one VM and score **85%+ on 3 fresh ExamCompass SY0-701 attempts** that include SecOps questions.

**can u explain it?** - unaided: describe what a SIEM does that plain log files do not, and name one risky default a secure baseline removes.

### incident response, BC/DR, and resilience meow (~10h)

**cert map** - CC D2; Security+ 4.8, 3.4, 5.2.

**heads up** - IR lifecycle, BC/DR, backups, RTO/RPO are both. Security+ goes deeper on forensics, order of volatility, chain of custody, and architecture-level resilience.

**the idea** - incidents are handled by a repeatable lifecycle; disasters are handled by continuity and recovery plans with measurable time/data-loss targets. boring plans matter when things are on fire.

**how/why it actually works** - **PICERL** is the IR loop: Prepare, Identify, Contain, Eradicate, Recover, Lessons Learned. containment stops spread; eradication removes the cause; recovery restores service; lessons learned feeds prevention.

**BC** keeps the business operating during disruption. **DR** restores systems after disruption. **RTO** is how long u can be down; **RPO** is how much data u can lose. backup design follows from those numbers, not vibes.

forensics adds evidence discipline: preserve volatile data first when needed, maintain chain of custody, and dont "clean up" before u know what happened.

**words u gotta be able to say**
- **event / incident / breach** - observed activity / harmful security event / confirmed data exposure
- **PICERL** - prepare, identify, contain, eradicate, recover, lessons
- **BCP / DRP** - continuity plan / recovery plan
- **RTO / RPO** - max downtime / max data loss
- **MTTR / MTBF** - repair time / failure interval
- **chain of custody** - evidence handling record
- **order of volatility** - collect most fragile evidence first

**study sources**
- [Professor Messer: Incident Response - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/incident-response-sy0-701/) - IR phases. **free**
- [Professor Messer: Digital Forensics - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/digital-forensics-sy0-701/) - evidence and process. **free**
- [Professor Messer: Resiliency - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/resiliency-sy0-701/) - HA/resilience. **free**
- [Professor Messer: Backups - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/backups-sy0-701/) - backup types and strategy. **free**

**do this** - write a mini IR runbook for "phishing email led to one user credential being used from a new country." include PICERL phase headings, first 5 actions, what logs u need, and one containment action.

**measurable gate:** runbook has all 6 PICERL phases, correctly states RTO vs RPO, and u score **85%+ on 3 fresh ExamCompass attempts** that include IR/resilience questions.

**can u explain it?** - unaided: given an incident scenario, name the phase, next action, and what evidence u must preserve before changing the system.

### risk, governance, and program management meow (~8h)

**cert map** - CC D1; Security+ D5.

**heads up** - risk/governance/awareness are both. Security+ goes deeper on third-party risk, audits/assessments, compliance, and named frameworks. ISC2 Code of Ethics remains CC only.

**the idea** - GRC is how an org decides what risk matters, which controls are required, and how to prove the controls exist. its the "show me evidence" layer mhm.

**how/why it actually works** - risk is usually framed as likelihood x impact. treatment choices are **avoid**, **mitigate**, **transfer**, or **accept**.

governance documents form a stack: **policies** state intent, **standards** define mandatory requirements, **procedures** say how to do it, **guidelines** suggest good practice.

audits and assessments compare reality to a requirement. awareness training reduces human-risk patterns like phishing, credential reuse, and bypassing certificate warnings.

**words u gotta be able to say**
- **risk appetite / tolerance** - how much risk org accepts
- **avoid / mitigate / transfer / accept** - four treatment choices
- **policy / standard / procedure / guideline** - intent / requirement / steps / advice
- **BIA** - business impact analysis
- **third-party risk** - vendor/supply-chain risk
- **audit / assessment** - formal check / evaluation
- **NIST CSF 2.0 / ISO 27001:2022** - common framework / ISMS standard

**study sources**
- [Professor Messer: Security Policies - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-policies-sy0-701/) - governance doc stack. **free**
- [Professor Messer: Risk Management - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/risk-management-sy0-701/) - risk vocabulary. **free**
- [Professor Messer: Third-party Risk Assessment - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/third-party-risk-assessment-sy0-701/) - vendor risk. **free**
- [Professor Messer: Business Impact Analysis - SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/business-impact-analysis-sy0-701/) - BIA/RTO/RPO tie-in. **free**
- [ISC2 CC Practice Quiz](https://cloud.connect.isc2.org/cc-quiz) + [CC Flash Cards](https://cloud.connect.isc2.org/cc-flashcards) - free with likely signup; useful if sitting CC. **free with signup**

**do this** - pick one risk from your lab, like "Windows VM has RDP exposed to the host-only network." write: asset, threat, vulnerability, impact, likelihood, risk rating, treatment choice, and control.

**measurable gate:** complete the risk note and score **85%+ on 3 fresh ExamCompass attempts** that include governance/risk questions. if sitting CC, recite the 4 ISC2 Code of Ethics canons in order.

**can u explain it?** - unaided: for one risk, justify whether u would avoid, mitigate, transfer, or accept it. then explain the difference between a policy and a procedure.

---

## Block 6 - cert readiness sprint (~10h)

this is where u decide whether to book exams.
dont book because u watched videos.
book when the gates say u are ready meow

### Network+ N10-009 readiness

**book only if all are true:**
- [ ] `/26`, `/27`, `/28` subnet drills pass under 60s each on paper, checked with [subnetipv4.com](https://subnetipv4.com/).
- [ ] **85%+ on 3 fresh** [ExamCompass N10-009 practice exams](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests).
- [ ] **90%+** on OSI + TCP/UDP ports quizzes.
- [ ] can recite the 7-step troubleshooting method in order.
- [ ] if using Dion, **85%+ on 2 fresh** [Jason Dion N10-009 practice exams](https://www.diontraining.com/products/comptia-network-n10-009-practice-exam).

**can u explain it?** - explain OSI layers with one protocol per layer, why `/26` gives 62 usable hosts, and why a stateful firewall can allow return traffic while blocking unsolicited inbound traffic.

### ISC2 CC readiness (optional paid exam)

**exam money note:** about **$199 + $50/yr AMF** now. no new free 1MCC vouchers after **2026-05-20**. use the exam only if u want that checkpoint; dont treat it like it magically fixes a thin resume.

**free checkpoint before paying:**
- [ ] can explain all 5 CC domains: Security Principles, BC/DR & IR, Access Controls, Network Security, Security Operations.
- [ ] completed [ISC2 CC Practice Quiz](https://cloud.connect.isc2.org/cc-quiz) and reviewed [CC Flash Cards](https://cloud.connect.isc2.org/cc-flashcards).
- [ ] can recite the ISC2 Code of Ethics canons in order if sitting the exam.
- [ ] if testing on/after **2026-09-01**, re-check the [CC Exam Outline](https://www.isc2.org/certifications/cc/cc-certification-exam-outline).

**can u explain it?** - without notes, map one example control to each CIA property, one access-control model to a real scenario, and one incident scenario to the correct PICERL phase.

### Security+ SY0-701 readiness

**book only if all are true:**
- [ ] watched or reviewed the relevant [Professor Messer SY0-701 course sections](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/) by weak domain, not by marathon-watching.
- [ ] **85%+ on 3 fresh** [ExamCompass SY0-701 practice tests](https://www.examcompass.com/comptia/security-plus-certification/free-security-plus-practice-tests).
- [ ] if buying practice, use the current [Messer SY0-701 Success Bundle](https://www.professormesser.com/sy0-701-success-bundle/) or [Dion SY0-701 Practice Exam Pack](https://www.diontraining.com/products/comptia-security-sy0-007-unlimited-practice-exam). dont use old generic Messer practice-exam links.
- [ ] can label whether each weak area is D1 concepts, D2 threats, D3 architecture, D4 operations, or D5 program management.

**can u explain it?** - explain one complete story: attacker phishes creds -> logs in from unusual country -> accesses a forbidden object -> SIEM alert fires -> IR contains account -> risk owner updates policy/control. name the mechanism at each step.

---

## exit check - done with Goal 2

- [ ] Network+ gate passed, or u already had CCNA-level networking and can prove it with the subnet/troubleshooting explain gates.
- [ ] CC domains are explainable; paid CC exam is optional and correctly understood as ~$199 + AMF, not free.
- [ ] Security+ readiness gate passed, or u know exactly which SY0-701 domain is still weak.
- [ ] completed Natas 0-15, CryptoHack intro + 3 hash challenges, TryHackMe Crack the Hash Task 1, PacketMaze, and the listed PortSwigger Apprentice labs.
- [ ] can explain CIA, TLS/PKI, salted password hashing, authn vs authz, DAC/MAC/RBAC/ABAC, ARP-spoof -> MITM, SYN flood, SIEM basics, PICERL, RTO/RPO, and risk treatment choices.

**final can u explain it?** - unaided, write or say a 10-minute walkthrough:

> "a user visits an HTTPS site from a segmented corporate network. explain DNS, TCP, TLS, cert validation, firewall/state, identity/authz, logging, what a MITM would try, why TLS stops it, what a SIEM would see if creds were stolen, and how IR responds."

if u can do that, ur ready for [Scripting, Logs & CTF](03-scripting-ctf.md).
if not, the missing nouns tell u exactly which block to redo.
dw, this is the point - no getting lost meow

---

[<- Goal 1: Foundations](01-foundations.md) | [Back to hub](README.md) | [Next: Scripting, Logs & CTF ->](03-scripting-ctf.md)
