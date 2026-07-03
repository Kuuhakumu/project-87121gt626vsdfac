# goal 2: networking & security core meow (~180h)

> **goal:** turn the foundation into security thinking: packets, controls, crypto/TLS, identity, access control, attacks, operations, IR, and risk.

certs are not the spine of this file.
the spine is labs, CTF reps, packet work, VM artifacts, and explain gates.
if u want exam-domain maps, prices, practice tests, or booking gates, use [certifications.md](certifications.md).

[<- Goal 1: Foundations](01-foundations.md) | [Back to hub](README.md) | [Next: Scripting, Logs & CTF ->](03-scripting-ctf.md)

---

## read this first meow

this file is not "study Network+, then study CC, then study Security+."

we study the **topics** in dependency order:
networking floor -> security properties -> crypto -> identity/access -> attacks -> operations -> IR -> risk.

the cert file can tell u which exam those topics cover.
this file tells u what to do so the topics become real in your hands.
the study sources give u the theory and vocabulary; the labs, CTF reps, and artifacts make it usable.
thats how u can become exam-ready without making the exam the center of the guide.
dw, thats the part that keeps u from getting lost qwq

also: **u dont need a paid textbook for this file.** deeper references helped shape the rewrite, but the learner path below stands on the explanations here, free/freemium resources, and real labs.

---

## how to track your progress meow

the `- [ ]` boxes here are display-only in this public repo.
fork the repo, or copy this checklist into Obsidian/OneNote, if u want boxes u can actually tick.

the real progress signal is always:

1. **measurable gate** - a solved lab, solved room, packet capture, timed drill, report, runbook, or artifact.
2. **can u explain it?** - out loud or written, unaided, naming the mechanism.

both must pass before the topic is really done.
a practice test can catch vocab gaps later; it does not replace the lab proof meow

---

## the path (todo-tree)

- [ ] **Block 1 - networking floor** (~55h): packets, ports, subnetting, implementation, operations, troubleshooting.
- [ ] **Block 2 - security foundations** (~15h): CIA, control types, AAA, Zero Trust, first access-control labs.
- [ ] **Block 3 - crypto + identity + access control** (~40h): TLS/PKI, hashes, password storage, authn/authz, DAC/MAC/RBAC/ABAC.
- [ ] **Block 4 - attacks + CTF thread** (~30h): MITM/replay/DoS, malware classes, SQLi, XSS, Natas + PortSwigger.
- [ ] **Block 5 - operations + IR + GRC** (~40h): VM baseline, logging/SOC flow, IR runbook, risk note, control evidence.
- [ ] **exit check** - can explain the whole chain: normal network -> control -> attack -> detection -> response -> risk update.

---

## block 1 - networking floor meow (~55h)

- [ ] packets, ports, and protocols (~18h)
- [ ] subnetting, switching, routing, and wireless (~22h)
- [ ] network operations + troubleshooting (~15h)

### packets, ports, and protocols meow (~18h)

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
- **stateful firewall** - tracks connection state across packets

**study sources (pick what fits your style)**
- [TryHackMe - Intro to Networking](https://tryhackme.com/room/introtonetworking) - guided OSI, ping, traceroute, and packet basics. **freemium**
- [TryHackMe - Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics) - packet-capture practice. **freemium**
- [Professor Messer N10-009 course, Section 1: Networking Concepts](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#section-1-networking-concepts) - clean free explanation if the vocab is still fuzzy. **free**
- [Professor Messer N10-009 YouTube playlist](https://www.youtube.com/playlist?list=PLG49S3nxzAnl_tQe3kvnmeMid0mjF8Le8) - same course on YouTube if that player works better. **free**

**do this** - complete **TryHackMe Intro to Networking** and **Wireshark: The Basics**, then capture or inspect one HTTP/HTTPS session and label where DNS, TCP, TLS, and HTTP show up.

**measurable gate:** both rooms are complete, and your packet notes correctly label **SYN -> SYN-ACK -> ACK**, destination port, source port, DNS answer, and one HTTP or TLS clue from the capture.

**can u explain it?** ✅ - unaided: explain what happens when a client opens `https://example.com`, naming DNS -> TCP -> TLS -> HTTP and saying what each layer is responsible for. then explain why a switch, router, and firewall are not the same device.

### subnetting, switching, routing, and wireless meow (~22h)

**the idea** - subnetting decides which IPs are local, routing decides where non-local packets go, switching moves local frames, and wireless adds radio + authentication problems.

**how/why it actually works** - an IPv4 address is split into **network bits** and **host bits** by the subnet mask/CIDR prefix. if two hosts share the same network ID, they talk locally through a switch; if not, they send traffic to a **default gateway** router.

**VLANs** split one physical switch into multiple logical broadcast domains, so user traffic, server traffic, guest Wi-Fi, and admin traffic dont all share one flat LAN.

**NAT/PAT** rewrites private inside addresses to a public address so many internal hosts can share one public IP. **Wi-Fi** adds radio exposure, so modern networks use WPA2/WPA3 and often **802.1X/RADIUS** so a password alone isnt the whole trust boundary.

**words u gotta be able to say**
- **CIDR / subnet mask** - which bits are network bits
- **network ID / broadcast / usable host** - subnet boundaries
- **default gateway** - router for non-local traffic
- **switch / router** - local frames / routed packets
- **VLAN / trunk** - logical LAN / carries multiple VLANs
- **NAT / PAT** - address/port rewriting at the edge
- **WPA2/WPA3 / RADIUS / 802.1X** - Wi-Fi security / centralized auth / port-based auth
- **blast radius** - how far compromise can spread

**study sources (pick what fits your style)**
- [subnetipv4.com](https://subnetipv4.com/) - free IPv4 subnetting drill generator. **free**
- [Professor Messer - Calculating IPv4 Subnets and Hosts, N10-009 1.7](https://www.professormesser.com/network-plus/n10-009/n10-009-video/calculating-ipv4-subnets-and-hosts-n10-009/) - worked subnetting examples. **free**
- [Practical Networking - Subnetting Mastery playlist](https://www.youtube.com/playlist?list=PLIFyRwBY_4bQUE4IB5c4VPRyDoLgOdExE) - method-first subnetting series. **free**
- [Professor Messer N10-009 course, Section 2: Network Implementation](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#1d643e1) - cabling, Wi-Fi, routing/switching, NAT/PAT. **free**

**do this** - drill at [subnetipv4.com](https://subnetipv4.com/) until `/26`, `/27`, and `/28` feel boring. draw a tiny network with three VLANs (users, servers, guest Wi-Fi), one router/firewall, and NAT at the edge.

**measurable gate:** given a random IP in a `/26`, write the network ID, broadcast, first usable, last usable, and host count in **under 60 seconds**, then repeat for `/27` and `/28`. check each on subnetipv4.com. your tiny network diagram must show which VLANs can talk and which should be blocked.

**can u explain it?** ✅ - unaided: explain why a `/26` gives 62 usable hosts, including why the network and broadcast addresses are not assignable. then explain why VLANs reduce blast radius but do not magically encrypt traffic.

### network operations + troubleshooting meow (~15h)

**the idea** - operations means keeping the network observable and documented; troubleshooting means changing one thing at a time instead of panic-clicking.

**how/why it actually works** - a network that cant be observed is basically a rumor. **syslog** records device events, **SNMP** polls device health, **NetFlow** summarizes who talked to whom, and diagrams/runbooks stop "tribal knowledge" from being the only map.

the troubleshooting method exists to slow u down in a good way: identify the problem, establish a theory, test the theory, make a plan, implement, verify, document. the order matters because a random "fix" can hide the root cause or cause a second outage.

tools each answer a narrow question: `ping` tests reachability, `tracert`/`traceroute` shows path, `nslookup`/`dig` tests DNS, `netstat`/`ss` shows sockets, `nmap` maps listening services.

**words u gotta be able to say**
- **syslog / SNMP / NetFlow** - events / device polling / flow summary
- **SLA / baseline** - expected service level / normal behavior
- **runbook / network diagram** - repeatable steps / topology map
- **troubleshooting methodology** - ordered fault-finding process
- **reachability vs name resolution** - IP path vs DNS answer
- **listening service** - process waiting on a port
- **false positive / false negative** - alert when fine / miss when bad

**study sources (pick what fits your style)**
- [Professor Messer N10-009 course, Section 3: Network Operations](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#ced8446) - monitoring, documentation, operations. **free**
- [Professor Messer N10-009 course, Section 5: Network Troubleshooting](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/#c80f0f9) - troubleshooting tools and method. **free**
- [Nmap Reference Guide](https://nmap.org/book/man.html) - exact option meanings when u use `nmap` legally. **free**
- [Wireshark Display Filter Reference](https://www.wireshark.org/docs/dfref/) - filter syntax when packet captures get noisy. **free**

**do this** - run `ping`, `tracert`/`traceroute`, `nslookup` or `dig`, `netstat`/`ss`, and `nmap` against your own lab VM or a legal target you control. write one sentence for what each command proves and what it does **not** prove.

**measurable gate:** your notes include the command, output snippet, what it proved, and what it did not prove for all 5 tool families. then write a 7-step troubleshooting note for "site works by IP but not by name."

**can u explain it?** ✅ - unaided: explain why "establish a theory of probable cause" comes before "test the theory," and give one example where DNS is broken but IP routing still works.

---

## block 2 - security foundations meow (~15h)

### CIA, controls, AAA, and Zero Trust meow (~15h)

**the idea** - security starts by naming what promise a control protects: confidentiality, integrity, availability, identity, accountability, or risk reduction.

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
- **least privilege** - only the access needed

**study sources (pick what fits your style)**
- [Professor Messer - Security Controls, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-controls-sy0-701/) - control categories and types. **free**
- [Professor Messer - The CIA Triad, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/the-cia-triad-sy0-701/) - confidentiality, integrity, availability. **free**
- [Professor Messer - Non-repudiation, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/non-repudiation-sy0-701/) - accountability property. **free**
- [Professor Messer - Zero Trust, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/zero-trust-sy0-701/) - Zero Trust vocabulary. **free**
- [PortSwigger - Access control topic](https://portswigger.net/web-security/access-control) - hands-on broken authorization labs. **free**

**do this** - solve these two PortSwigger labs:
- [Unprotected admin functionality](https://portswigger.net/web-security/access-control/lab-unprotected-admin-functionality)
- [User ID controlled by request parameter](https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter)

**measurable gate:** both labs show **Solved**, and your notes label which property failed: confidentiality, integrity, availability, authentication, authorization, or accounting. include the exact request/URL part that made the issue visible.

**can u explain it?** ✅ - unaided: give one attack that breaks only integrity and one that breaks only availability. then explain why "logged in" is not the same as "authorized for this object."

---

## block 3 - crypto + identity + access control meow (~40h)

- [ ] cryptography, TLS, and PKI (~15h)
- [ ] authentication and password storage (~10h)
- [ ] access-control models and IAM (~15h)

### cryptography, TLS, and PKI meow (~15h)

**the idea** - crypto gives tools for secrecy, tamper detection, identity proof, and safe key agreement. the hard part is knowing which tool gives which property.

**how/why it actually works** - **symmetric encryption** uses one shared key and is fast enough for bulk data, but both sides need the same secret.

**Asymmetric crypto** uses a public/private keypair. a public key can verify a signature from the private key, or help establish a shared secret without sending that secret directly.

**Hashing** makes a fixed-size fingerprint. it does not hide data; it detects change. keyed hashes and signatures add authenticity.

**TLS** combines these: the client and server negotiate algorithms, the server proves identity with a certificate chain, key exchange creates symmetric session keys, and authenticated encryption protects the actual traffic.

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
- [Professor Messer - Public Key Infrastructure, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/public-key-infrastructure-sy0-701/) - CA and trust model. **free**
- [Professor Messer - Encrypting Data, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/encrypting-data-sy0-701/) - symmetric/asymmetric/data protection. **free**
- [Professor Messer - Certificates, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/certificates-sy0-701/) - certificate fields and chains. **free**
- [Professor Messer - States of Data, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/states-of-data-sy0-701/) - at rest, in transit, in use. **free**
- [CryptoHack - Introduction to CryptoHack](https://cryptohack.org/courses/intro/) - beginner encoding/XOR/modular arithmetic by doing. **free**
- [CryptoHack - Hash Functions challenges](https://cryptohack.org/challenges/hashes/) - hands-on hash intuition. **free**

**do this** - complete **CryptoHack - Introduction to CryptoHack** and the first **3 Hash Functions** challenges. then inspect a real HTTPS certificate chain for `https://example.com` in your browser or with `curl -vI https://example.com`. finally, create a small text file, hash it, change one character, and hash it again with `Get-FileHash` on Windows or `sha256sum` on Linux/macOS.

**measurable gate:** CryptoHack intro is complete, 3 hash challenges are solved, your notes show the leaf certificate subject/name, issuer, expiry, and at least one trust-chain observation. your hash notes show two different digests after one file change and explain why that proves integrity checking, not encryption.

**can u explain it?** ✅ - walk the PKI chain: root CA -> intermediate CA -> leaf certificate -> signature checks -> browser trust decision. then say what OCSP/CRL are checking and why a hash alone is not encryption.

### authentication and password storage meow (~10h)

**the idea** - authentication proves identity; password storage is about making stolen password databases expensive to abuse.

**how/why it actually works** - a login compares a claim to stored proof. storing plaintext passwords is catastrophic because database theft becomes instant account theft.

a password **hash** stores a one-way digest instead. a **salt** makes identical passwords produce different stored values and breaks precomputed rainbow tables.

modern password storage uses slow KDFs like bcrypt, scrypt, Argon2, or PBKDF2 because attackers can try billions of fast hashes. slowness is a feature here meow.

**MFA** adds another factor so a stolen password alone is not enough. phishing-resistant MFA goes further by binding the login to the real site/origin.

**words u gotta be able to say**
- **authentication / authorization** - prove identity / decide allowed action
- **password hash** - one-way stored verifier
- **salt** - random per-password value
- **KDF** - slow password hashing function
- **rainbow table** - precomputed hash lookup
- **MFA factor** - something u know, have, are, where, or do
- **phishing-resistant MFA** - factor bound to real origin/device
- **session token** - proof of logged-in state after auth

**study sources (pick what fits your style)**
- [Professor Messer - Authentication, Authorization, and Accounting, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/authentication-authorization-and-accounting-sy0-701/) - AAA recap. **free**
- [Professor Messer - Multifactor Authentication, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/multifactor-authentication-sy0-701/) - factor categories and MFA limits. **free**
- [OWASP Password Storage Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html) - current defensive guidance. **free**
- [PortSwigger - Authentication vulnerabilities](https://portswigger.net/web-security/authentication) - how auth breaks in apps. **free**

**do this** - write a one-page note that compares plaintext password storage, unsalted fast hash, salted slow hash, and MFA. include the attacker question for each: "what can they do if the database leaks?"

**measurable gate:** the note names salt, KDF, MFA, session token, and phishing resistance correctly, and includes one safe design choice for a new app.

**can u explain it?** ✅ - unaided: explain why salting does not make weak passwords strong by itself, and why MFA reduces damage from password reuse.

### access-control models and IAM meow (~15h)

**the idea** - identity says who the subject is; access control decides whether that subject can do this action to that object right now.

**how/why it actually works** - access decisions always have pieces: **subject**, **object**, **operation**, and **policy**. if the app only checks "logged in" but not "allowed for this object," access control breaks.

**DAC** lets owners grant permissions. **MAC** enforces labels the user cannot override. **RBAC** maps people to roles, then roles to permissions. **ABAC** evaluates attributes like device, location, time, object label, and action.

identity lifecycle matters because stale accounts are access bugs with usernames. provisioning gives access, deprovisioning removes it, reviews catch drift, and least privilege keeps roles small.

**words u gotta be able to say**
- **subject / object / operation** - actor / target / action
- **DAC / MAC / RBAC / ABAC** - owner / label / role / attribute model
- **least privilege** - only needed access
- **segregation of duties** - split risky powers
- **provisioning / deprovisioning** - grant / remove identity access
- **federation / SSO** - trust identity across systems
- **Kerberos / LDAP / SAML / OAuth / 802.1X/EAP** - auth directory, token, and network-access protocols

**study sources (pick what fits your style)**
- [Professor Messer - Access Controls, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/access-controls-sy0-701/) - models, rights, IAM terms. **free**
- [Professor Messer - AAA, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/authentication-authorization-and-accounting-sy0-701/) - authn/authz/accounting refresh. **free**
- [PortSwigger - Access control vulnerabilities](https://portswigger.net/web-security/access-control) - practical broken authorization. **free**
- [OWASP Web Security Testing Guide - Authorization Testing](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/05-Authorization_Testing/README) - what testers check. **free**

**do this** - make a tiny access matrix for a fake clinic app: patient, nurse, doctor, billing clerk, admin; objects: patient chart, prescription, invoice, audit log. then add time/device/location conditions to one row until it becomes ABAC.

**measurable gate:** the matrix has at least 5 roles, 4 object types, allow/deny choices, one segregation-of-duties rule, and one ABAC condition. add one sentence showing how an IDOR would bypass a weak version of this design.

**can u explain it?** ✅ - explain when youd choose RBAC vs MAC vs DAC and why, with a one-line real scenario each. then take one RBAC scenario and add time/device/location conditions until it becomes ABAC.

---

## block 4 - attacks + CTF thread meow (~30h)

- [ ] network attacks + defenses (~14h)
- [ ] threats, malware, and web vulnerability classes (~16h)

### network attacks + defenses meow (~14h)

**the idea** - network attacks abuse trust assumptions in protocols: who owns this MAC, who answered DNS, who is really in the middle, and whether this message is fresh.

**how/why it actually works** - **ARP spoofing** works because ARP replies are not authenticated; a host can cache "gateway IP is at my MAC" and send traffic to the attacker.

**MITM/on-path** attacks relay traffic between two parties. TLS is the fix because the certificate chain authenticates the server, key exchange creates fresh session keys, and authenticated encryption detects tampering.

**Replay** attacks resend a valid captured message. nonces, timestamps, sequence numbers, and session binding stop old messages from being accepted as new.

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

**study sources (pick what fits your style)**
- [Professor Messer - Denial of Service, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/denial-of-service-sy0-701/) - DoS/DDoS framing. **free**
- [Professor Messer - Firewall Types, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/firewall-types-sy0-701/) - packet/state/app firewalls. **free**
- [Professor Messer - Firewalls, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/firewalls-sy0-701/) - placement and policy. **free**
- [Professor Messer - Segmentation and Access Control, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/segmentation-and-access-control-sy0-701/) - VLANs, screened subnets, NAC ideas. **free**

**do this** - draw an ARP-spoof -> MITM path on a local LAN, then add where TLS, HSTS, segmentation, and switch protections reduce the damage. use your Wireshark notes from Block 1 as the packet reference.

**measurable gate:** the diagram shows victim, gateway, attacker, ARP cache lie, traffic path, and at least 4 defenses. each defense must say whether it prevents the attack, detects it, or reduces impact.

**can u explain it?** ✅ - unaided: walk an ARP-spoof -> MITM chain end to end, then explain why proper TLS still protects the session even if the attacker sees every packet.

### threats, malware, and web vulnerability classes meow (~16h)

**the idea** - a vulnerability is a condition that lets normal system behavior produce an unsafe result.

**how/why it actually works** - **malware** is categorized by how it spreads and what it does: viruses attach to files, worms self-propagate, trojans masquerade as legit, ransomware encrypts/extorts, rootkits hide control, botnets coordinate many machines.

**SQL injection** happens when untrusted input becomes part of a query instead of data. the database obeys a query that the developer didnt mean to build.

**XSS** happens when untrusted input becomes executable script in another user's browser. the browser runs it because it came from a trusted site context.

**Buffer overflow** happens when a program writes past a memory boundary and overwrites adjacent state; if that state controls execution flow, the attacker may redirect execution. dw this gets deeper later - rn u just need the mechanism shape.

**words u gotta be able to say**
- **threat actor / vector / surface** - who / path / exposed area
- **malware family** - grouped by spread/payload behavior
- **phishing / vishing / smishing** - email / voice / SMS social engineering
- **SQLi** - input becomes database query syntax
- **XSS** - input becomes browser-executed script
- **buffer overflow** - write past memory boundary
- **zero-day** - unknown/unpatched vuln in use
- **mitigation** - control that reduces likelihood or impact

**study sources (pick what fits your style)**
- [Professor Messer - Threat Actors, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/threat-actors-sy0-701/) - actors and motivations. **free**
- [Professor Messer - Phishing, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/phishing-sy0-701/) - social engineering types. **free**
- [Professor Messer - An Overview of Malware, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/an-overview-of-malware-sy0-701/) - malware taxonomy. **free**
- [PortSwigger - SQL injection](https://portswigger.net/web-security/sql-injection) - CTF-style SQLi targets. **free**
- [PortSwigger - Cross-site scripting](https://portswigger.net/web-security/cross-site-scripting) - CTF-style XSS targets. **free**

**do this** - solve:
- [SQL injection vulnerability in WHERE clause allowing retrieval of hidden data](https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data)
- [SQL injection vulnerability allowing login bypass](https://portswigger.net/web-security/sql-injection/lab-login-bypass)
- [Reflected XSS into HTML context with nothing encoded](https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded)
- [OverTheWire Natas](https://overthewire.org/wargames/natas/) levels **4-15**

**measurable gate:** all 3 PortSwigger labs show **Solved**, Natas level 15 is cleared, and u can classify 5 short scenarios by malware/vuln type without notes.

**can u explain it?** ✅ - unaided: explain the difference between SQLi and XSS by naming where the attack executes (database vs browser). then explain, at a high level, how a buffer overflow can affect control flow.

---

## block 5 - operations + IR + GRC meow (~40h)

- [ ] hardening, logging, and monitoring (~14h)
- [ ] incident response, BC/DR, and resilience (~14h)
- [ ] risk, governance, and evidence (~12h)

### hardening, logging, and monitoring meow (~14h)

**the idea** - security operations turns controls into daily habits: reduce exposed services, keep systems patched, collect logs, detect weird behavior, and document what changed.

**how/why it actually works** - **Hardening** removes default risk: unused services, default credentials, permissive firewall rules, weak TLS settings, unnecessary admin rights.

**Patch/config management** keeps known bugs from staying exploitable and keeps systems from drifting away from a baseline.

**Logging** records events; a **SIEM** normalizes and correlates logs across systems so one weird login, DNS query, and endpoint alert can become one investigation instead of three isolated lines.

**words u gotta be able to say**
- **baseline / drift** - approved config / config moving away
- **patch management** - fixing known vulnerable code
- **asset inventory** - what exists and who owns it
- **vulnerability management** - find, prioritize, remediate, verify
- **log source** - system producing events
- **SIEM** - log collection/correlation/search platform
- **SOAR** - workflow automation around alerts
- **data classification** - label by sensitivity/handling need

**study sources (pick what fits your style)**
- [Professor Messer - Secure Baselines, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/secure-baselines-sy0-701/) - baseline concept. **free**
- [Professor Messer - Hardening Techniques, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/hardening-techniques-sy0-701/) - reduce attack surface. **free**
- [Professor Messer - Vulnerability Scanning, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/vulnerability-scanning-sy0-701/) - scan/triage cycle. **free**
- [Professor Messer - Security Monitoring, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-monitoring-sy0-701/) - monitoring/SIEM terms. **free**
- [LetsDefend - SOC Fundamentals](https://app.letsdefend.io/training/lessons/soc-fundamentals) - SOC role, alert, EDR/SOAR/log basics. **free**

**do this** - make a one-page hardening checklist for a fresh Windows or Linux VM: disable one unused service, enable/update firewall policy, list local admin/root-equivalent users, confirm updates, identify where auth/system logs live, and take a before/after note. also complete LetsDefend SOC Fundamentals if the SOC flow is new to u.

**measurable gate:** the checklist has at least 6 rows and one before/after change. your notes explain where one auth log lives and what event would make u investigate. if using LetsDefend, the SOC Fundamentals lesson is complete.

**can u explain it?** ✅ - unaided: describe what a SIEM does that plain log files do not, and name one risky default a secure baseline removes.

### incident response, BC/DR, and resilience meow (~14h)

**the idea** - incidents are handled by a repeatable lifecycle; disasters are handled by continuity and recovery plans with measurable time/data-loss targets.

**how/why it actually works** - **PICERL** is the IR loop: Prepare, Identify, Contain, Eradicate, Recover, Lessons Learned.

containment stops spread. eradication removes the cause. recovery restores service. lessons learned feeds prevention.

**BCP** keeps the business operating during disruption; **DRP** restores technology after disruption.

**RTO** is max downtime. **RPO** is max data loss. backup design follows those numbers, not vibes. forensics adds evidence discipline: preserve volatile data first when needed, maintain chain of custody, and dont "clean up" before u know what happened.

**words u gotta be able to say**
- **event / incident / breach** - observed activity / harmful security event / confirmed data exposure
- **PICERL** - prepare, identify, contain, eradicate, recover, lessons
- **BCP / DRP** - continuity plan / recovery plan
- **RTO / RPO** - max downtime / max data loss
- **MTTR / MTBF** - repair time / failure interval
- **chain of custody** - evidence handling record
- **order of volatility** - collect most fragile evidence first

**study sources (pick what fits your style)**
- [Professor Messer - Incident Response, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/incident-response-sy0-701/) - IR phases. **free**
- [Professor Messer - Digital Forensics, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/digital-forensics-sy0-701/) - evidence and process. **free**
- [Professor Messer - Resiliency, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/resiliency-sy0-701/) - HA/resilience. **free**
- [Professor Messer - Backups, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/backups-sy0-701/) - backup types and strategy. **free**

**do this** - write a mini IR runbook for "phishing email led to one user credential being used from a new country." include PICERL phase headings, first 5 actions, what logs u need, one containment action, one evidence-preservation note, RTO, and RPO.

**measurable gate:** the runbook has all 6 PICERL phases, correctly states RTO vs RPO, names at least 3 log sources, and separates containment from eradication.

**can u explain it?** ✅ - unaided: given an incident scenario, name the phase, next action, and what evidence u must preserve before changing the system.

### risk, governance, and evidence meow (~12h)

**the idea** - GRC is how an org decides what risk matters, which controls are required, and how to prove the controls exist.

**how/why it actually works** - risk is usually framed as likelihood x impact. treatment choices are **avoid**, **mitigate**, **transfer**, or **accept**.

governance documents form a stack: **policies** state intent, **standards** define mandatory requirements, **procedures** say how to do it, **guidelines** suggest good practice.

audits and assessments compare reality to a requirement. evidence proves whether the control exists and works. without evidence, a control is just a sentence qwq

**words u gotta be able to say**
- **risk appetite / tolerance** - how much risk org accepts
- **avoid / mitigate / transfer / accept** - four treatment choices
- **policy / standard / procedure / guideline** - intent / requirement / steps / advice
- **BIA** - business impact analysis
- **third-party risk** - vendor/supply-chain risk
- **audit / assessment** - formal check / evaluation
- **NIST CSF 2.0 / ISO 27001:2022** - common framework / ISMS standard
- **evidence** - artifact proving a control exists

**study sources (pick what fits your style)**
- [Professor Messer - Security Policies, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/security-policies-sy0-701/) - governance document stack. **free**
- [Professor Messer - Risk Management, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/risk-management-sy0-701/) - risk vocabulary and treatment. **free**
- [Professor Messer - Third-party Risk Assessment, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/third-party-risk-assessment-sy0-701/) - vendor risk. **free**
- [Professor Messer - Business Impact Analysis, SY0-701](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/business-impact-analysis-sy0-701/) - BIA/RTO/RPO tie-in. **free**
- [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) - map controls to CSF Functions/Categories. **free**

**do this** - pick one risk from your lab, like "Windows VM has RDP exposed to the host-only network." write: asset, threat, vulnerability, impact, likelihood, risk rating, treatment choice, control, and evidence.

**measurable gate:** the risk note has all 9 fields above, and one control is mapped to a NIST CSF 2.0 Function/Category using the Reference Tool.

**can u explain it?** ✅ - unaided: for one risk, justify whether u would avoid, mitigate, transfer, or accept it. then explain the difference between a policy and a procedure.

---

## ✅ exit check - done with Goal 2

- [ ] TryHackMe Intro to Networking and Wireshark: The Basics are complete.
- [ ] the packet notes label DNS, TCP, TLS/HTTP clues, source/destination ports, and SYN -> SYN-ACK -> ACK.
- [ ] `/26`, `/27`, and `/28` subnet drills pass under 60 seconds each, and the VLAN diagram exists.
- [ ] troubleshooting command notes exist for `ping`, route tracing, DNS lookup, socket listing, and `nmap`.
- [ ] the two PortSwigger access-control labs are solved and explained.
- [ ] CryptoHack intro + 3 hash challenges are solved, and certificate-chain/hash-change notes exist.
- [ ] the access matrix exists with RBAC and one ABAC condition.
- [ ] the ARP-spoof -> MITM defense diagram exists.
- [ ] the three PortSwigger SQLi/XSS labs are solved, and Natas is cleared through level 15.
- [ ] the VM hardening checklist, mini IR runbook, and risk note exist.
- [ ] u can explain CIA, Zero Trust, stateful firewalls, TLS/PKI, authn vs authz, DAC/MAC/RBAC/ABAC, malware and vulnerability classes, SIEM basics, PICERL, RTO/RPO, and risk treatment choices.

**final can u explain it?** - unaided, write or say a 10-minute walkthrough:

> "a user visits an HTTPS site from a segmented corporate network. explain DNS, TCP, TLS, cert validation, firewall/state, identity/authz, logging, what a MITM would try, why TLS stops it, what a SIEM would see if creds were stolen, how IR responds, and how the risk/control note changes afterward."

if u can do that, ur ready for [Scripting, Logs & CTF](03-scripting-ctf.md).
if u also want an exam checkpoint, go to [certifications.md](certifications.md) **after** this exit check.
dw, this is the point - no getting lost meow

---

[<- Goal 1: Foundations](01-foundations.md) | [Back to hub](README.md) | [Next: Scripting, Logs & CTF ->](03-scripting-ctf.md)
