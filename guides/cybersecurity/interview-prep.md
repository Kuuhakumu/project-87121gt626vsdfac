# cybersecurity interview prep meow

> entry-level security interviews are mostly "can u reason out loud without pretending."
> this keeps the Q-bank, but adds answer shapes and `can u explain it?` checks so u practice mechanism, not flashcards qwq.

[<- Job Hunt](05-job-hunt.md) | [Hub](README.md) | [Resources](resources.md)

---

## how to use this

- [ ] **first pass:** answer each question out loud with no notes.
- [ ] **second pass:** compare against the answer shape here.
- [ ] **third pass:** do the `can u explain it?` prompt without looking.

if u can recite the answer but cant tell the story of what happens, keep practicing.
interviewers can feel the difference fast meow.

---

## how entry-level interviews usually run

most entry-level security roles use a 3-4 stage loop:

1. **recruiter screen** - motivation, work authorization, cert status, schedule, basic fit.
2. **technical screen** - quiz, log-analysis scenario, short take-home, or CTF-style task.
3. **technical panel / hiring manager** - scenario questions like the bank below.
4. **behavioral** - STAR stories and communication checks.

the common fail is not "didnt memorize enough acronyms."
its "could not walk through a scenario."
practice every answer as a story: signal -> mechanism -> decision -> next step.

---

## networking fundamentals

- **Q: explain the OSI model. at which layer does a firewall operate? a switch? a router?**
  **answer shape:** OSI is a layered model for network responsibilities: physical, data link, network, transport, session, presentation, application. switches mostly work at Layer 2 using MAC addresses. routers work at Layer 3 using IP. firewalls can work at Layer 3/4 for IP/port rules and Layer 7 for application-aware inspection.
  **can u explain it?** say why a switch does not need an IP route to forward frames on the same LAN, but a router does.

- **Q: walk me through what happens when you type `https://example.com` and press Enter.**
  **answer shape:** DNS resolves name to IP, TCP does SYN -> SYN-ACK -> ACK to port 443, TLS validates certificate and negotiates a symmetric session key, HTTP sends a GET request through the encrypted tunnel, server returns status/body, browser renders.
  **can u explain it?** explain exactly what the certificate proves, and why TLS gives confidentiality plus integrity against a MITM.

- **Q: whats the difference between TCP and UDP? give a real protocol using each.**
  **answer shape:** TCP is connection-oriented and reliable: sequencing, retransmission, flow control. UDP is connectionless and lower overhead: no built-in delivery guarantee. HTTPS/SSH use TCP; DNS often uses UDP; streaming/VoIP/gaming often use UDP where latency matters.
  **can u explain it?** if a UDP packet is lost, who notices and fixes it, if anyone?

- **Q: whats the TCP three-way handshake?**
  **answer shape:** client sends SYN, server replies SYN-ACK, client replies ACK. both sides synchronize sequence numbers before data flows.
  **can u explain it?** why does TCP need sequence numbers before it can promise ordered delivery?

- **Q: what are the port numbers for SSH, DNS, HTTP, HTTPS, SMB, RDP?**
  **answer shape:** SSH 22, DNS 53, HTTP 80, HTTPS 443, SMB 445, RDP 3389.
  **can u explain it?** dont just list them; say one suspicious thing u might investigate for each exposed port.

- **Q: whats the difference between a public and private IP? what is NAT doing?**
  **answer shape:** public IPs route on the internet. private ranges like `10.0.0.0/8`, `172.16.0.0/12`, and `192.168.0.0/16` are internal and not internet-routed. NAT rewrites source/destination address/port mappings so many private hosts can share one public IP.
  **can u explain it?** explain why a reverse shell often works through NAT better than a bind shell.

- **Q: what is DNS and how does recursive resolution work?**
  **answer shape:** DNS maps names to records like A/AAAA/CNAME/MX. a recursive resolver checks cache, then asks root -> TLD -> authoritative server, returns the answer, and caches it for the TTL.
  **can u explain it?** say how a poisoned resolver or malicious authoritative answer could send users to the wrong IP.

- **Q: subnet this: how many usable hosts in a `/29`?**
  **answer shape:** `/29` leaves 3 host bits, so 8 total addresses. subtract network and broadcast = 6 usable hosts.
  **can u explain it?** do the same logic for `/26`, `/27`, and `/28` without a calculator.

---

## security concepts

- **Q: define the CIA triad. give an example control for each leg.**
  **answer shape:** confidentiality = prevent unauthorized reading, e.g. encryption/access control. integrity = prevent/detect unauthorized alteration, e.g. hashing/signatures/change control. availability = keep systems usable, e.g. redundancy, backups, DDoS protection.
  **can u explain it?** classify ransomware impact across CIA instead of saying "availability only."

- **Q: symmetric vs asymmetric encryption - when do you use each? where do they combine?**
  **answer shape:** symmetric uses one shared key and is fast for bulk data. asymmetric uses public/private keys and solves identity/key-exchange problems but is slower. TLS combines them: asymmetric/ephemeral key exchange authenticates and agrees on a symmetric session key, then symmetric crypto protects the traffic.
  **can u explain it?** why doesnt HTTPS encrypt the whole session with the servers public key?

- **Q: what is hashing and how is it different from encryption? why salt a hash?**
  **answer shape:** hashing is one-way fingerprinting; encryption is reversible with a key. hashes verify integrity or store passwords safely. a salt is unique random data added before hashing so identical passwords dont produce identical hashes and precomputed rainbow tables fail.
  **can u explain it?** explain why password hashes still need slow algorithms like bcrypt/Argon2.

- **Q: what is PKI? walk through how a certificate proves a sites identity.**
  **answer shape:** PKI is the trust system of certificates, certificate authorities, private keys, and validation chains. server presents a cert for its domain; browser checks domain name, expiry, signature chain to a trusted root/intermediate CA, and revocation status where available.
  **can u explain it?** what could still go wrong if the private key is stolen?

- **Q: explain defense in depth and give three layers.**
  **answer shape:** defense in depth means overlapping controls so one failure does not equal full compromise. examples: MFA, least privilege, endpoint protection, network segmentation, logging/monitoring, backups.
  **can u explain it?** map one phishing attack through at least three layers that could stop or detect it.

- **Q: what is least privilege? give an example of violating it.**
  **answer shape:** users/services get only the permissions needed for the task, for only as long as needed. violation: daily user is local admin; service account has domain admin; S3 bucket policy allows `*` read; cloud role has `AdministratorAccess` for a narrow job.
  **can u explain it?** explain why least privilege reduces blast radius after credential theft.

- **Q: what is zero trust and how does it differ from perimeter security?**
  **answer shape:** zero trust assumes network location is not enough proof. every access is explicitly verified using identity, device posture, context, least privilege, and continuous monitoring. perimeter security trusts "inside" more than "outside"; zero trust treats inside as still needing verification.
  **can u explain it?** give a remote-work example where VPN alone is not enough.

---

## SOC, detection, and incident response

- **Q: a SIEM alert fires for 10,000 failed logins on one account in 5 minutes. walk triage.**
  **answer shape:** check account criticality, source IPs/geos, one source vs many, password spray vs brute force, any success after failures, MFA prompts, device/user history, known scanner/service, lockout status. contain if active: disable/reset account, block source, revoke sessions, escalate with evidence.
  **can u explain it?** explain the difference between brute force and password spraying from the log pattern.

- **Q: walk me through investigating a phishing email from alert to closure.**
  **answer shape:** preserve message, inspect headers, SPF/DKIM/DMARC, sender/domain reputation, URLs/attachments in sandbox, extract IOCs, search mail gateway for other recipients, check clicks/credential submissions, contain affected accounts/endpoints, block indicators, document and close/escalate.
  **can u explain it?** explain what SPF, DKIM, and DMARC each prove and what they do not prove.

- **Q: what is the incident response lifecycle?**
  **answer shape:** PICERL: Preparation, Identification, Containment, Eradication, Recovery, Lessons Learned. NIST can also be framed as preparation; detection/analysis; containment/eradication/recovery; post-incident activity.
  **can u explain it?** for ransomware, name one action in each phase.

- **Q: difference between an event, an alert, and an incident?**
  **answer shape:** event = any recorded activity. alert = detection logic flagged an event or pattern. incident = confirmed or strongly suspected security event requiring response.
  **can u explain it?** why should not every alert become an incident ticket?

- **Q: what is MITRE ATT&CK and how would you use it in an investigation?**
  **answer shape:** ATT&CK is a knowledge base of adversary tactics, techniques, and procedures. use it to name behavior, map detections, communicate coverage, and identify next likely steps. example: PowerShell execution maps to `T1059.001`.
  **can u explain it?** difference between a tactic and a technique.

- **Q: IDS vs IPS - whats the difference and when choose each?**
  **answer shape:** IDS detects and alerts, usually out-of-band. IPS sits inline and can block. choose IDS when visibility and low risk of disruption matter; IPS where blocking known-bad traffic is worth the false-positive risk.
  **can u explain it?** why is IPS tuning more operationally risky than IDS tuning?

- **Q: false positive vs false negative, and why is tuning important?**
  **answer shape:** false positive = benign activity alerted. false negative = malicious activity missed. tuning reduces noise without hiding real attacks; too many false positives cause alert fatigue, too much suppression creates blind spots.
  **can u explain it?** describe a tuning change that reduces noise but keeps detection value.

- **Q: you see `powershell.exe` spawned by `winword.exe`. why suspicious?**
  **answer shape:** Office spawning PowerShell can indicate macro/maldoc execution, LOLBin abuse, payload download, or script-based post-exploitation. check command line, parent/child process tree, network connections, file writes, user context, and whether it was expected.
  **can u explain it?** what evidence would make it benign vs malicious?

- **Q: difference between EDR and traditional antivirus?**
  **answer shape:** traditional AV often focuses on known signatures/files. EDR collects endpoint telemetry like process, network, registry, file, and command-line behavior, then supports detection, investigation, containment, isolation, and response actions.
  **can u explain it?** why can EDR catch suspicious behavior even when the file hash is new?

---

## vulnerability management

- **Q: what is CVSS and how do you use it to prioritize patching?**
  **answer shape:** CVSS scores technical severity using base/temporal/environmental factors. use it as one input, not the only input. prioritize by exploitability, asset criticality, exposure, CISA KEV/known exploitation, compensating controls, and business impact.
  **can u explain it?** why might a CVSS 7 on an internet-facing auth server beat a CVSS 9 on an isolated lab host?

- **Q: a scan returns 4,000 findings. how do you prioritize?**
  **answer shape:** deduplicate, identify internet-facing and critical assets, look for known exploited vulns, privilege/remote exploitability, business owners, patch availability, compensating controls, and quick wins. group by remediation campaign instead of ticketing every finding blindly.
  **can u explain it?** say how u would communicate the top 10 to IT without dumping a scanner PDF.

- **Q: difference between vulnerability, threat, and risk?**
  **answer shape:** vulnerability = weakness. threat = actor/event that could exploit it. risk = likelihood and impact of that threat exploiting that vulnerability against an asset.
  **can u explain it?** turn "RDP exposed" into asset, threat, vulnerability, impact, and treatment.

- **Q: what is patch management and why is a test ring important?**
  **answer shape:** patch management is inventorying, testing, deploying, verifying, and reporting updates. test rings deploy to a small group first so broken patches are caught before hitting critical systems.
  **can u explain it?** balance emergency patching for active exploitation against change-control risk.

---

## web and application security

- **Q: what is SQL injection? how do you prevent it?**
  **answer shape:** SQLi happens when user input is concatenated into a query and interpreted as SQL code. prevent with parameterized queries/prepared statements, least-privilege DB accounts, safe ORM patterns, and input validation as a secondary control.
  **can u explain it?** why does parameterization work better than blocking `' OR 1=1` strings?

- **Q: what is XSS? name types and mitigations.**
  **answer shape:** XSS is attacker-controlled script running in another users browser. reflected returns immediately from a request; stored persists in the app; DOM-based happens in client-side JS. mitigate with output encoding by context, sanitization for allowed HTML, CSP, and avoiding unsafe sinks.
  **can u explain it?** why is output encoding context-dependent?

- **Q: what does the OWASP Top 10 cover, and whats #1 in the 2025 list?**
  **answer shape:** OWASP Top 10 names common web-app risk categories and their impact. the current guide tracks OWASP 2025, where Broken Access Control remains the top risk. use it as vocabulary, then prove skills in PortSwigger labs.
  **can u explain it?** give an IDOR example and why authentication alone does not fix authorization.

- **Q: what is CSRF and how does a token defend against it?**
  **answer shape:** CSRF tricks a logged-in browser into sending an unintended state-changing request. a CSRF token is unpredictable and tied to the user/session/request, so an attacker site cannot forge a valid request even though the browser sends cookies. SameSite cookies help too.
  **can u explain it?** why does CSRF mainly matter for cookie-based auth?

---

## cloud security

- **Q: explain the shared responsibility model. who secures what in IaaS vs SaaS?**
  **answer shape:** provider secures of the cloud: facilities, hardware, managed backplane. customer secures in the cloud: data, identity, access, config, and often OS/app depending on service model. IaaS leaves OS/network/app/data more to customer; SaaS shifts stack to provider but customer still owns users/data/access policy.
  **can u explain it?** draw the line for EC2 vs Microsoft 365.

- **Q: whats the most common cloud breach cause?**
  **answer shape:** misconfiguration, especially public storage, over-permissive IAM, exposed management ports, weak secrets handling, and missing logs. cloud makes mistakes scale fast because resources are API-created.
  **can u explain it?** explain how a public bucket policy and sensitive object become actual exposure.

- **Q: what does least privilege look like in cloud IAM? roles vs users vs service accounts?**
  **answer shape:** use roles/service principals for workloads, avoid long-lived human keys, scope policies to needed actions/resources, use conditions, rotate secrets, monitor privilege changes, and prefer temporary credentials where possible. users are human identities; roles/service accounts are assumed by workloads or sessions.
  **can u explain it?** why are long-lived access keys risky compared with temporary role credentials?

- **Q: which API calls would worry you in CloudTrail logs?**
  **answer shape:** context matters, but examples include `CreateUser`, `CreateAccessKey`, `AttachUserPolicy`, `PutBucketPolicy`, `AuthorizeSecurityGroupIngress`, `GetSecretValue`, `AssumeRole` anomalies, disabling logs, or GuardDuty/SecurityHub tampering.
  **can u explain it?** pick one call and say what attacker objective it might serve.

---

## 2026-current differentiators

- **Q: what is a Sigma rule and why is it useful?**
  **answer shape:** Sigma is vendor-neutral detection-as-code in YAML. it describes log source, field selections, condition, false positives, severity, and ATT&CK tags; converters turn it into SPL, KQL, Elastic, or other SIEM query formats.
  **can u explain it?** walk from raw Windows event -> Sigma selection -> SIEM query.

- **Q: what are the NIST CSF 2.0 functions?**
  **answer shape:** GOVERN, IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER. Govern is the 2.0 addition and frames risk management, roles, policy, oversight, and supply-chain governance.
  **can u explain it?** map MFA, log monitoring, and incident lessons learned to CSF functions.

- **Q: what is prompt injection?**
  **answer shape:** prompt injection is malicious or untrusted input that manipulates an LLM/agent into ignoring instructions, revealing data, taking unintended actions, or misusing tools. OWASP LLM Top 10 2025 labels this under LLM01.
  **can u explain it?** why is "just tell the model not to do that" not a complete defense?

- **Q: how does AI-assisted triage change the SOC analyst role?**
  **answer shape:** AI can summarize alerts, draft queries, cluster events, and speed first-pass investigation. the analyst still validates evidence, checks context, decides escalation/containment, and owns the risk of wrong conclusions.
  **can u explain it?** give one place AI helps and one place a human must verify.

---

## behavioral questions (STAR format)

answer with **Situation -> Task -> Action -> Result**.
prep 4-5 stories and reuse them across questions, oki.

- **Tell me about a time you explained something technical to a non-technical person.**
  **answer shape:** choose a real moment where u simplified without lying. result should show understanding changed or a decision improved.

- **Describe a project or home lab you built. Why, and what did you learn?**
  **answer shape:** use a portfolio project: goal, setup, problem hit, evidence, lesson, what ud improve. lean on CTF writeups or repo proof.

- **Tell me about a time you failed or got something wrong. What did you change?**
  **answer shape:** pick a small honest failure, not a fake weakness. show debug process and changed behavior.

- **How do you stay current with security news and threats?**
  **answer shape:** name exact sources, but more importantly say how u translate news into mechanisms/controls. examples: The Hacker News, Risky Business, BleepingComputer, vendor blogs, r/cybersecurity.

- **Describe a time you had to learn something difficult quickly.**
  **answer shape:** show a learning loop: break down topic, lab it, ask targeted questions, document, apply.

- **Tell me about a disagreement on a team and how you handled it.**
  **answer shape:** show listening, facts, tradeoff, decision, and outcome. no blame dump.

- **Why cybersecurity? Why this company?**
  **answer shape:** tie your mechanism interest to their role. "i like figuring out normal vs suspicious from evidence" beats "i like hacking."

- **Where do you see yourself in your security career in three years?**
  **answer shape:** pick a direction but stay coachable: SOC -> detection engineering, GRC -> risk/compliance, cloud security, DFIR, etc.

**can u explain it?** for behavioral prep: after every story, say what skill it proves and which project/lab backs it up.
if the story has no evidence, pick a better story meow.

---

## practical components

some employers add hands-on screens.
be ready to:

- [ ] analyze a **PCAP in Wireshark** and identify suspicious traffic.
- [ ] write a basic **SPL or KQL query** to find a pattern in logs.
- [ ] review a mock incident or vuln-scan output and prioritize next steps.
- [ ] triage a simulated alert queue.
- [ ] explain your own repo/writeup without reading it.

specific practice:

- [TryHackMe - Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics)
- [KC7](https://kc7cyber.com/)
- [Kusto Detective Agency](https://detective.kusto.io/)
- [Splunk Free Training](https://www.splunk.com/en_us/training/free-courses/overview.html)
- [LetsDefend - SOC Analyst Learning Path](https://app.letsdefend.io/path/soc-analyst-learning-path)
- [CyberDefenders - DanaBot](https://cyberdefenders.org/blueteam-ctf-challenges/danabot/)

---

## prep plan: the week before

- [ ] re-read your own CTF writeups and lab notes.
- [ ] say every core concept out loud as a scenario: CIA, PKI, PICERL, OSI, shared responsibility, least privilege.
- [ ] run 3-5 fresh LetsDefend alerts or 2 KC7/Kusto cases.
- [ ] prepare 5 STAR stories.
- [ ] research the company stack from the job description: Microsoft? AWS? Splunk? Sentinel? EDR?
- [ ] prepare 3 questions to ask them: training, alert volume, escalation process, tooling, growth path.

**final can u explain it?** - pick your strongest project and explain it twice:

1. to a SOC analyst, with logs/tools/mechanism.
2. to a non-technical manager, with risk/impact/decision.

same facts, different language.
thats the communication bar entry-level security actually needs.

[<- Job Hunt](05-job-hunt.md) | [Hub](README.md) | [Resources](resources.md)
