# B0 - lab, safety, and support evidence (~12h)

> **before endpoint repair, before networking, before identity - this is the floor.**
> preflight your environment, learn what u can and cant touch, and practice the one habit that keeps data safe: test rollback before trusting a change meow

**Time:** ~12h total (~6 days at 2 h/day)  
[Previous: Shared Foundations](../../start-here/foundations.md) · [Hub](README.md) · [Next: B1 - Foundations](01-foundations.md)

---

## where u are rn

if u just cleared [Shared Foundations](../../start-here/foundations.md) (or tested out with its cold-case evidence), ur ready for B0. this short 12h block is the actual start of IT Support work - not generic computing, but the safe lab setup, professional boundaries, and evidence habits every support role depends on.

**the honest career ladder:** most IT Support careers start at Help Desk or Service Desk (first-line support, L1), handling user inquiries, standard requests, guided troubleshooting, and documentation within approved procedures. the next step is typically Desktop Support or NOC (Network Operations Center) roles that own endpoint repair, local troubleshooting, and network evidence gathering with more independence. from there, junior systems or network positions work on production infrastructure under change authority. B0 teaches the safety, scope, and evidence floor that every level depends on. later blocks (C01-C03 cumulative revisits in B1-B3) return to these boundaries inside real mixed scenarios.

**test-out option:** if u already have Desktop Support or NOC experience, u may attempt B0 test-out. pass the SF-XFER cold case (if skipping Shared Foundations), then submit C01 artifacts 8/8, C02 classification 10/10, C03 safety triage 11/12 with every mandatory stop correct, plus one B0-EXIT form and 7/8 explanations. a cert or job title permits the attempt but waives nothing. any gate failure routes to the exact failed cluster - no shortcuts.

dw if that sounds strict - its there so u never wonder "am i ready or just tired of this page?" the measurable gates keep u honest; the explain gates prove u understand why, not just what button meow

---

## how the two-part gate system works

every major topic below has **both**:

1. **measurable gate** - a real % on a named site, a challenge passed, an artifact built, or a working system. either it passes or it doesnt - no vibes, no self-scoring mystery.

2. **can u explain it?** - out loud or written, unaided (no guide, no notes, no oracle open). scored 0-8 on four dimensions (see rubric below). proves u understand the mechanism and can handle a near variant, not just that u followed steps once.

**both must pass** before a topic is really done. the measurable gate is the outside check; the explain gate catches "i passed the quiz but couldnt tell u why it works" - which is exactly the gap this whole rewrite exists to close qwq

---

## the 7/8 explanation rubric

every explain gate uses this four-dimension scoring unless a cluster specifies stricter criteria:

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| **States and actors** | Starting/ending state or actors materially wrong | Some actors/states named but boundary is unclear | Correct actors plus explicit before/after state |
| **Causal chain** | Facts or steps listed with broken causality | Main order present with one material gap | Ordered chain states what changes and why |
| **Evidence and terms** | No relevant evidence or material term misuse | Mostly correct but imprecise evidence/terms | Correct artifact/field/term; observation separated from inference |
| **Boundary and transfer** | Overclaims or cannot handle the changed fact | Gives a limit or a variant, but not both well | Gives a meaningful limit and reasons through the near variant |

**Pass:** score at least **7/8**, causal chain must be **2**, and no listed critical error. u may draw diagrams; accent, camera, and polish are not scored.

---

## aid labels and committed-before-oracle

**Aid labels** track honesty about help received:

- **A0** - product docs, `man`/`--help`, and your prior notes only → eligible independent evidence
- **A1** - process hint like "find the first failed layer" → guided evidence
- **A2** - concept/command hint or failure category → practice evidence
- **A3** - walkthrough, model query, answer key, or copied solution → worked-example evidence

if u get stuck after 20-30 min of real blocked effort, move to the next help level. an A1-A3 completion earns the repair loop, but the independent gate waits for an A0 parallel form (the changed retry).

**Committed-before-oracle rule:** for every case below, commit your hypothesis/answer packet (with timestamp and A0-A3 label) before opening the truth packet or test results. this proves reasoning, not oracle lookup.

---

## artifact envelope and evidence requirements

every artifact you create must contain these exact elements:

**Common artifact envelope:**
- **Artifact ID** - unique identifier (e.g., `C01-LAB-A-evidence`, `C03-SAFE-A-triage`)
- **Date and timestamp** - UTC or local with timezone (e.g., `2026-07-15T14:30:00Z`)
- **Aid level** - exactly one: `A0`, `A1`, `A2`, or `A3`
- **Evidence tier** - one of: `live` (performed action on real system), `simulation` (supplied case/reasoning), `case-analysis` (reasoning from supplied evidence without live execution)
- **Cloud/access tier** (where applicable) - `none`, `simulation-supplied`, `Entra Free`, `eligible developer sandbox`, `Intune trial`, `M365 business trial`, or `owned paid tenant`

**Evidence-log requirements:**
- separate **observed** facts (what you saw/measured) from **inferred** conclusions (what you concluded)
- label each assertion as `reported` (user statement), `observed` (your direct evidence), `inferred` (your reasoning), or `changed` (action taken)
- record **before state**, **action**, and **after state** for every change
- include **rollback evidence** where applicable
- redact real environment identifiers (company names, real user names, real domain names, production IPs) beyond synthetic examples like `corp.example`, `192.0.2.x`, or `RITN-USER1`

**Integrity fields for B0 and beyond:**
- **Commit ID or timestamp** - when you committed your answer before revealing oracle
- **Oracle revealed** - timestamp when you opened the truth
- **Pass/repair decision** - did you pass at A0, or does this require repair and changed retry?

these rules apply to every C01-C03 artifact and carry forward through B1-B5. clean evidence hygiene now prevents capstone rejection later meow

---

## the path (todo-tree)

- [ ] **C01 - preflight, access, and rollback** (~5h)
- [ ] **C02 - support role scope and escalation** (~2h)
- [ ] **C03 - safety and evidence isolation** (~5h)
- [ ] ✅ **B0 exit check** - C01 8/8, C02 10/10, C03 11/12, one exit form

---

## C01 · preflight, access, and rollback (~5h)

**the idea** - a support lab needs two things a production system never gets: reversible mistakes and independent proof u can actually recover. if u cant roll back a bad change or prove evidence survives host failure, ur practicing on borrowed trust - and borrowed trust ends the first time something breaks for real.

**how/why it actually works** - oki so this is the part where we set up the safety net before doing anything risky...

a **VM (virtual machine)** is a simulated computer running as an application on your physical **host**. the host OS uses a **hypervisor** (like VirtualBox) to create isolated **guest** environments. each guest has virtual CPU, RAM, storage, and network adapters. the guest thinks its a normal computer; the hypervisor translates guest operations into host operations and enforces isolation boundaries.

why isolation matters: the guest is **disposable**. if u break the Windows registry, delete system files, corrupt the boot loader, or install something that wont uninstall - u delete the VM and start over. no reinstall media hunt, no data-recovery panic.

**what the hypervisor isolates:**
- guest processes cannot directly access host files (unless u explicitly share folders)
- guest cannot normally execute host binaries or read host memory
- guest network adapters can be NAT'd (guest sees internet but not host) or host-only (guest + host private network)
- guest storage is one or more files on the host; deleting the VM folder deletes the guest

**what isolation doesnt prevent:**
- shared folders bridged from host become guest-writable unless read-only
- bridged network mode puts the guest directly on the host's physical LAN (can affect other systems)
- hypervisor bugs or VM-escape exploits (rare but possible - keep VirtualBox updated)
- host resource exhaustion if u allocate more RAM/CPU than the host has available

three critical mechanisms protect ur work:

1. **snapshots** - capture guest state (disk, optionally RAM/CPU registers) at one moment. rolling back to a snapshot restores that exact state in seconds. snapshots are *not* independent backups - theyre stored inside the VM folder on the host. if the host drive fails or the folder is deleted, every snapshot is gone. snapshots let u experiment within one host, but they dont survive catastrophic host failure.

2. **export (OVA/OVF)** - flattens the VM's current disk state into a portable `.ova` file. **exports do not preserve snapshots** - they capture only the current running state. exporting creates a host-independent copy that can be imported on a different machine, stored offline, or kept as recovery insurance. export proves ur baseline can be recreated elsewhere, but u lose the snapshot tree when u export.

3. **independent backup** - a copy stored on a **separate failure domain** (different physical disk, external drive, cloud storage, or another machine). same-host export is a lab convenience copy; its not resilient backup bc host failure destroys both the original and the export. true backup requires the copy to survive when the host does not.

the safe workflow is: baseline -> snapshot before the marker -> create marker -> experiment -> rollback and verify marker is gone -> then export the working baseline to independent storage (not the same host disk).

**words u gotta be able to say:**

- **host** - the physical computer running the hypervisor
- **guest / VM** - the simulated computer running inside the hypervisor
- **hypervisor** - software that creates and manages VMs (VirtualBox, VMware, Hyper-V)
- **snapshot** - point-in-time guest state capture; fast rollback but stored with the VM on the same host
- **export** - portable VM copy (`.ova`/OVF format); can be imported on a different machine
- **`.ova` / OVF** - Open Virtualization Format; standard portable VM package
- **baseline** - known-good starting state before experiments
- **rollback** - restore to an earlier snapshot
- **disposable** - can be deleted and recreated without data loss
- **isolation** - guest changes dont affect the host (within hypervisor limits)
- **NAT network mode** - guest sees internet through host translation; guest not directly visible to LAN
- **host-only mode** - private network between host and guest(s); no external network
- **bridged mode** - guest appears as separate device on host's physical LAN (lab risk)
- **independent backup** - copy on a separate failure domain (different disk/machine/cloud)

**study sources (pick what fits your style):**

- **[VirtualBox First Steps (official manual)](https://www.virtualbox.org/manual/ch01.html)** - creating a VM, snapshots, and export workflow; this is the primary path bc it walks the exact recovery loop. free, verified 2026-07-11
- **no video** - the manual plus the actual preflight give u the full loop; a demo would just show the same buttons
- **[VirtualBox Networking (official manual)](https://www.virtualbox.org/manual/ch06.html)** - reference for NAT, host-only, and bridged modes when u need to look up the exact isolation boundary
- **[Packet Tracer Getting Started](https://www.netacad.com/courses/packet-tracer)** - account setup and first simulation; ull need this for network preflight. free tier, may require Cisco account, verified 2026-07-11

**do this - C01-LAB-A (three connected proofs):**

you'll create a recoverable lab environment, prove snapshot/export independence, test Packet Tracer, and record cloud access tier. commit all evidence before checking the acceptance oracle.

**required artifacts (8/8):**

1. **host report** - CPU/RAM (at least 8 GiB RAM, 40 GiB free storage recommended), OS, VirtualBox version/license (base package is GPLv3)
2. **VM boot** - one disposable Windows VM using [Windows 11 Enterprise 90-day evaluation](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-11-enterprise) or legitimate media, boots successfully
3. **network mode** - record NAT or host-only (not bridged for lab safety)
4. **snapshot-before** - baseline snapshot named `B0-baseline` created **before** making the marker file
5. **marker changed** - create test marker file `C:\LAB-MARKER-A.txt` containing a synthetic learner ID and UTC date **after** the baseline snapshot, take a second snapshot
6. **marker absent after restore** - roll back to `B0-baseline`, boot, verify marker file does not exist (proves rollback works and that snapshot was taken before marker creation)
7. **export validation** - export the baseline VM to `.ova` in a new directory, record file size and SHA-256 hash. **validate the export:** power off (do not delete) the original VM, import the `.ova` to a new directory with a different name (e.g., `B0-baseline-imported`), boot the imported VM, run one acceptance test (e.g., marker absent, expected OS), record import timestamp. This proves the export is independent and bootable. (Note: OVA export flattens current VM state and does not preserve snapshots.)
8. **Packet Tracer test** - complete the network preflight case below

**Packet Tracer network preflight case (C01-PT-A):**

if u have Packet Tracer installed, build this exact topology and prove ping:

- **supplied topology:** one switch (2960 or similar), two PCs connected to switch ports
- **addresses:** PC1 = `192.168.1.10/24`, PC2 = `192.168.1.11/24`
- **test:** ping from PC1 to PC2; verify success in simulation mode or realtime
- **evidence:** save as `C01-network-test.pkt`; record ping result (success/reply count)

**if Packet Tracer account/download unavailable:** this is the case-analysis simulation route (no installation claim):

- **supplied scenario:** two PCs (`PC1` at `192.168.1.10/24`, `PC2` at `192.168.1.11/24`) connected to one switch; switch ports Fa0/1 and Fa0/2 are up/up
- **observed:** `ping 192.168.1.11` from PC1 returns "Reply from 192.168.1.11: bytes=32 time<1ms TTL=128" (4/4 replies)
- **questions:** (1) what layer-2 address does PC1 need to send the frame? (2) how does PC1 discover it? (3) after ARP, what destination MAC appears in the frame? (4) what does the switch do with the frame?
- **truth:** (1) PC2's MAC; (2) ARP request broadcast; (3) PC2's MAC from ARP reply; (4) learns source MAC on Fa0/1, floods broadcast, learns PC2 MAC on Fa0/2, forwards future frames directly
- **evidence tier:** `case-analysis` (reasoning only)
- **claims not supported:** installed or used Packet Tracer

**cloud tier label:** record exactly one: `none` (no M365/Entra/Intune access attempted), `simulation-supplied` (case evidence only), `Entra Free`, `eligible developer sandbox`, `Intune trial`, `M365 business trial`, or `owned paid tenant`. for B0, `none` or `simulation-supplied` is normal and expected - no tenant is required.

**measurable gate:** all 8 artifacts pass. commit evidence packet (host specs, boot screenshot, network mode, snapshot names/timestamps, marker absent proof, export hash/size, import timestamp, Packet Tracer ping result or case-analysis answers, cloud tier) before comparing with the truth oracle below.

<details>
<summary><strong>truth oracle (click to reveal after commitment)</strong></summary>

- snapshot taken **before** creating the marker; rollback restores to that prior state (marker does not exist after restore)
- export creates a portable copy independent of the original VM folder (import to new directory/name succeeds with original VM powered off)
- **OVA/OVF export flattens current VM state and does not preserve snapshots**
- same-host export is a lab copy, not resilient backup (both original and export on same disk = single failure domain)
- validation test: power off original, import to new name/directory, boot and verify one acceptance check
- Packet Tracer: same-subnet ping between .10 and .11 uses ARP discovery, switch learns MACs, ping succeeds
- case-analysis simulation: PC1 ARPs for PC2 MAC, switch floods/learns, directed forwarding follows
- `none` cloud tier is acceptable for B0 - no tenant is required or claimed
- marker content uses synthetic learner ID and UTC date, not real personal information

</details>

**changed retry:** if any artifact fails, repair and take **C01-LAB-B** - same 8 requirements but use marker `C:\LAB-MARKER-B.txt` with synthetic learner ID, different VM name `B0-baseline-B`, host-only network mode (if A used NAT), import to a different directory/name after powering off original, and Packet Tracer topology with PC1 `10.0.0.5/24` and PC2 `10.0.0.6/24` (or case-analysis variant with those addresses). same truth applies.

**critical errors (override numeric score):**
- calling snapshot or same-host export "independent backup" (they share host failure domain)
- claiming export preserves snapshots (OVF flattens current state only)
- using unlicensed/pirated media (evaluation or legitimate only)
- claiming a required cloud tenant for B0 (none needed)
- bridged network mode in a shared LAN without authorization (lab safety violation)
- including real personal information in marker files (use synthetic learner ID instead)

**can u explain it?** ✅ - out loud or written, unaided, score 7/8 minimum:

*"Explain what a snapshot captures and where its stored. Then explain why importing an .ova export to a new directory with the original VM powered off proves independence, while keeping the .ova on the same host disk does NOT prove resilient backup. Finally, describe what the hypervisor isolates (give two examples) and what isolation doesnt prevent (give two limits)."*

the near-transfer probe changes one fact: what if the host disk fails completely - does the snapshot survive? does the same-host export survive? what would constitute true independent backup? full credit requires revising the isolation/backup boundaries, not repeating the original baseline explanation.

dw if the evaluation expires in 90 days - ur building disposable lab skills, not a permanent workstation. when the eval ends, u export final evidence, delete the VM, and create a fresh one for the next block. same workflow, new baseline meow

---

## C02 · support role scope and escalation (~2h)

**the idea** - not every ticket is urs to fix. recognizing the boundary between first-line support, escalation, and production authority is the skill that keeps u employed and keeps systems safe. diving beyond ur approved scope - even with good intent - creates liability, destroys audit trails, and breaks trust.

**how/why it actually works** - real talk: the hardest support skill isnt technical, its knowing when to stop...

every organization defines **scope** differently, but the universal pattern is: first-line support handles known procedures, standard requests, and guided troubleshooting within a documented baseline. anything beyond that - production changes, privilege escalation, security incidents, vendor escalation, architectural decisions, or emergency policy exceptions - requires explicit **authorization** and usually a different team.

the reason this boundary exists: **evidence and rollback**. a help-desk ticket can say "i reset the service and it worked" bc the service restart is documented and reversible. a first-line tech cannot say "i modified the firewall rule, patched the domain controller, or granted admin rights" without a change record, peer review, rollback plan, and authorized approval - bc those actions affect shared systems, accumulate risk, and cant be undone with ctrl+z.

**escalation** transfers work or authority to a team with broader capability, while the original owner retains **responsibility** for tracking, user updates, and validation until closure. escalation is not "throw it over the wall and forget." a good handoff contains: record ID, symptom in user's words, scope, timeline, evidence collected, tests run, actions taken, exact reason for escalation, and requested next action.

the **seven-step operational loop** (current Network+ wording; A+ uses six by combining steps 4-5):

1. identify the problem
2. establish a theory of probable cause
3. test the theory to determine the cause
4. establish a plan of action to resolve the problem and identify potential effects
5. implement the solution or escalate as necessary
6. verify full system functionality and, if applicable, implement preventive measures
7. document findings, actions, outcomes, and lessons learned

this method becomes real when u update theories from evidence: reported symptom -> scope/expected behavior -> plausible causes -> predict evidence each would produce -> run least-risky discriminating test -> raise/lower/reject theories -> fix or escalate -> rerun original journey + adjacent checks.

**words u gotta be able to say:**

- **scope** - the procedures, systems, and changes ur role is authorized to perform
- **authorization** - explicit permission for an action, usually documented in policy or change record
- **baseline** - the approved configuration or standard that defines normal
- **escalation** - transferring work/authority to a team with broader capability while retaining ownership
- **ownership** - responsibility to track the ticket, update the user, and confirm closure
- **handoff** - the evidence packet that lets the receiving team act without repeating intake
- **change record** - documented plan, approval, action, and validation for a config/access change
- **rollback** - reversing a change to its prior state; not every action has one
- **production / shared system** - live infrastructure serving real users (DC, firewall, DNS, file server)
- **security incident** - suspected breach, malware, data exposure, unauthorized access; immediate security-team escalation
- **first-line / L1** - help desk / service desk initial contact and standard procedures
- **L2 / Desktop Support / NOC** - endpoint repair, local troubleshooting, network evidence gathering
- **L3 / Systems / Network** - production infrastructure changes under change authority

**study sources:**

- **Guide-owned:** the mechanism above and the O*NET role-boundary practical below define scope. no external playlist owns this topic.
- **[O*NET Computer User Support Specialists](https://www.onetonline.org/link/details/15-1232.00)** - exact task list; this is the classification source. free, verified 2026-07-11
- **[O*NET Computer Network Support Specialists](https://www.onetonline.org/link/details/15-1231.00)** - network support task list for comparison. free, verified 2026-07-11
- optional background: [Atlassian: What is ITSM?](https://www.atlassian.com/itsm) and [Incident vs. Service Request](https://www.atlassian.com/itsm/service-request-management/incident-vs-service-request) - explains incident/request/problem/change workflows. free, verified. dw, u dont need to memorize Atlassian/ServiceNow/Jira wording - every org uses different terms. the idea (classify work and know who owns it) is universal.


**do this - C02-ROLE-A:**

you'll classify ten O*NET tasks under a supplied authority matrix, then provide evidence/owner/user-update/trigger for each. commit answers before checking the oracle.

**supplied authority matrix for this case:**

- **Service Desk (L1) may perform:** user inquiry, bounded command observation within approved endpoint scope, approved equipment setup from standard build (deviations escalate), help-desk documentation, and user training after content approval
- **Service Desk must gather evidence and escalate (retaining user-update ownership):** major product faults, network diagnosis/change, and security-breach indicators
- **Network Support owns (under change authority):** router/switch configuration and fiber repair

**ten tasks from current [O*NET Computer User Support Specialists](https://www.onetonline.org/link/details/15-1232.00) and [Network Support Specialists](https://www.onetonline.org/link/details/15-1231.00):**

For each task, classify as: `L1 perform`, `L1 gather/escalate`, `network support`, or `later admin`. Then state: **evidence** needed, **owner** of execution, **user-update** duty, and **trigger** for escalation.

1. Answer user inquiries regarding computer software or hardware operation to resolve problems. (User Support)
2. Enter commands and observe system functioning to verify correct operations and detect errors. (User Support)
3. Set up equipment for employee use, performing or ensuring proper installation of cables, operating systems, or appropriate software. (User Support)
4. Refer major hardware or software problems or defective products to vendors or technicians for service. (User Support)
5. Develop training materials and procedures, or train users in the proper use of hardware or software. (User Support)
6. Identify the causes of networking problems, using diagnostic testing software and equipment. (Network Support)
7. Document help desk requests and resolutions. (User Support)
8. Configure wide area network (WAN) or local area network (LAN) routers or related equipment. (Network Support)
9. Analyze and report computer network security breaches or attempted breaches. (Network Support)
10. Install or repair network cables, including fiber optic cables. (Network Support)

**measurable gate:** all 10 classifications correct with **evidence/owner/user-update/trigger** stated for each. commit before oracle.

<details>
<summary><strong>truth oracle (click to reveal after commitment)</strong></summary>

Task classifications with required fields:

1. `L1 perform` - **evidence:** user report/symptom; **owner:** Service Desk; **user-update:** ongoing status; **trigger:** none (within scope)
2. `L1 perform` - **evidence:** command output/observation; **owner:** Service Desk within approved endpoint scope; **user-update:** result; **trigger:** major fault or network-layer issue
3. `L1 perform` - **evidence:** standard build checklist; **owner:** Service Desk for standard build only; **user-update:** setup complete; **trigger:** deviation from standard
4. `L1 gather/escalate` - **evidence:** symptom/error/attempted resolution; **owner:** Service Desk gathers, vendor/L2 executes; **user-update:** retained by Service Desk; **trigger:** major fault confirmed
5. `L1 perform` - **evidence:** approved content; **owner:** Service Desk after approval; **user-update:** training schedule; **trigger:** none (post-approval)
6. `L1 gather/escalate` - **evidence:** network tests/symptoms; **owner:** Service Desk gathers, Network Support diagnoses/changes; **user-update:** retained by Service Desk; **trigger:** network change needed
7. `L1 perform` - **evidence:** ticket record; **owner:** Service Desk; **user-update:** closure confirmation; **trigger:** none (core duty)
8. `network support` - **evidence:** change request/plan; **owner:** Network Support under change authority; **user-update:** stakeholder communication; **trigger:** n/a (different team)
9. `L1 gather/escalate` - **evidence:** preserved logs/indicators; **owner:** Service Desk gathers, Security team owns response; **user-update:** retained by Service Desk; **trigger:** suspected breach
10. `network support` - **evidence:** site authorization/safety; **owner:** Network Support with physical/site authorization; **user-update:** stakeholder communication; **trigger:** n/a (different team)

Core truth: escalation transfers technical authority, not ticket ownership by default. The original tech tracks, updates, and validates unless explicitly transferred.

</details>


**changed retry:** if <10/10 or boundary questions miss authority/escalation, take **C02-ROLE-B** using these ten different current O*NET tasks and regional authority matrix:

**supplied authority matrix for C02-ROLE-B:**

- **Service Desk may perform:** equipment inspection for delivery, maintain support records, bounded minor endpoint repair within approved scope, telephone connectivity support; contributes evidence to evaluations and requirements discussions
- **Service Desk must gather evidence and escalate:** performance evaluation decisions, network backup execution, wireless configuration, network documentation approval
- **Network Support owns (under change authority):** network backup execution, LAN/WAN performance evaluation and decisions, network change documentation approval, wireless equipment installation/configuration

**ten tasks from current O*NET pages:**

For each task, classify as: `L1 perform`, `L1 gather/escalate`, `network support`, or `later admin`. Then state: **evidence** needed, **owner** of execution, **user-update** duty, and **trigger** for escalation.

1. Inspect computer equipment received for delivery to ensure hardware and software components are present. (User Support)
2. Perform minor repairs to computer equipment, such as replacing cables or peripherals, within approved procedures. (User Support)
3. Maintain records of daily data communication transactions, problems and remedial actions taken, or installation activities. (User Support)
4. Prepare evaluations of vendor products or services for management consideration. (User Support)
5. Confer with staff, users, and management to establish requirements for new systems or modifications. (User Support)
6. Back up network data to maintain data security and integrity. (Network Support)
7. Evaluate local area network (LAN) or wide area network (WAN) performance data to determine network capacity and needs. (Network Support)
8. Maintain and administer computer networks and related computing environments, including documentation and network configurations. (Network Support)
9. Install or configure wireless networking equipment such as access points or wireless routers. (Network Support)
10. Provide telephone connectivity support for internal or external users. (User Support)

**measurable gate:** all 10 classifications correct with **evidence/owner/user-update/trigger** stated for each. commit before oracle.

<details>
<summary><strong>truth oracle for C02-ROLE-B (click to reveal after commitment)</strong></summary>

Task classifications with required fields:

1. `L1 perform` - **evidence:** delivery checklist/packing list; **owner:** Service Desk; **user-update:** receipt confirmation; **trigger:** none (within scope)
2. `L1 perform` - **evidence:** symptom/approved procedure; **owner:** Service Desk within approved minor repair scope; **user-update:** repair result; **trigger:** repair beyond approved scope or safety concern
3. `L1 perform` - **evidence:** transaction logs/tickets; **owner:** Service Desk; **user-update:** incident closure; **trigger:** none (core duty)
4. `L1 gather/escalate` - **evidence:** vendor responses/feature comparison; **owner:** Service Desk contributes evidence, management decides; **user-update:** evaluation timeline; **trigger:** final decision authority belongs to management
5. `L1 gather/escalate` - **evidence:** user/staff requirements; **owner:** Service Desk contributes evidence, systems/network teams design; **user-update:** requirements captured; **trigger:** design/implementation authority
6. `network support` - **evidence:** backup schedule/verification; **owner:** Network Support; **user-update:** stakeholder notification if backup affects service; **trigger:** n/a (different team)
7. `network support` - **evidence:** performance metrics/capacity data; **owner:** Network Support analyzes and decides; **user-update:** stakeholder communication; **trigger:** n/a (different team)
8. `network support` - **evidence:** configuration documentation/change records; **owner:** Network Support approves network documentation; **user-update:** stakeholder communication; **trigger:** n/a (different team)
9. `network support` - **evidence:** site survey/installation plan; **owner:** Network Support with site/safety authorization; **user-update:** stakeholder communication; **trigger:** n/a (different team)
10. `L1 perform` - **evidence:** user request/connectivity symptom; **owner:** Service Desk; **user-update:** connectivity restored/escalation status; **trigger:** physical infrastructure or carrier issue

Core truth: escalation transfers technical authority, not ticket ownership by default. The original tech tracks, updates, and validates unless explicitly transferred. Regional authority matrices vary but the same evidence/owner/update/trigger pattern applies.

</details>

**critical errors:**
- claiming certification/tool knowledge alone defines authority (org policy defines scope)
- treating escalation as abandonment (ownership persists for tracking/updates)
- fabricated job title, salary, or role responsibility not in O*NET or supplied matrix

**can u explain it?** ✅ - score 7/8:

*"Explain why a help-desk tech can restart a local print spooler but must escalate before restarting a shared file-server service, even if both technical procedures are identical. Include the words authorization, shared system, rollback, and change record. Then give an example where u know the technical fix but escalation is mandatory, and explain what evidence/handoff the receiving team needs."*

---

## C03 · safety and evidence isolation (~5h)

**the idea** - a wrong troubleshooting decision can destroy data, void warranty, cause injury, or turn one symptom into three faults. the skill that separates safe support from reckless support is recognizing **stop-work conditions** and preserving evidence before testing theories.

**how/why it actually works** - oki so this is the safety contract that every field tech, help desk agent, and sysadmin lives by...

support work touches three overlapping risk categories:

1. **physical safety** - swollen batteries, exposed mains voltage inside PSUs or UPS cabinets, hot components, and heavy equipment can cause fire, chemical exposure, electric shock, or injury. some repairs require licensed electricians, qualified technicians, or vendor-authorized procedures. the moment u see a safety red flag, u stop work, secure the area, and escalate to the safety-qualified owner. "it still works" is not permission to continue.

2. **data and evidence preservation** - a user's report, error message, log timestamp, or failed-component state is evidence. overwriting logs, power-cycling without capturing state, or replacing parts without testing destroys the chain that proves causality. if the first fix attempt makes diagnosis harder or creates a second fault, u just turned a 20-minute ticket into a two-day investigation.

3. **authorization and scope** - production systems, shared infrastructure, warranty-sealed components, regulated data, and any action outside documented baseline require explicit **authorization**. good intent does not grant authority. even when u know the fix, if its outside scope, the correct action is document -> handoff -> wait for authorized execution.

the safe troubleshooting pattern is: recognize stop triggers -> preserve current state -> gather least-risky evidence -> escalate or execute only within scope -> validate the fix didnt create a second fault -> document the chain.

**words u gotta be able to say:**

- **stop-work condition** - observed hazard, missing authorization, or evidence-destroying risk that requires immediate halt
- **swollen / bulging battery** - lithium cell damage; mandatory power-down and isolation (fire/thermal runaway risk)
- **hot component** - fuser, power supply under load, or thermally failing part; assess whether temperature is operational or a fault signature
- **mains voltage / line voltage** - AC power from the wall outlet (120V/240V); requires qualified technician or licensed electrician for internal PSU or UPS work
- **ESD (electrostatic discharge)** - static electricity damaging sensitive components; use grounded wrist strap on bare metal chassis ground (not mains ground pin)
- **Safety Data Sheet (SDS)** - hazard/handling info for toner, cleaning agents, compressed air, or any chemical; replaces legacy term MSDS
- **proper ventilation** - adequate airflow when using aerosol cleaners, handling toner, or working with chemical solvents
- **two-person lift** - heavy equipment (UPS, server, large printer) requires coordinated lift to prevent back injury
- **warranty seal / tamper-evident label** - manufacturer seal; breaking it may void warranty and require vendor repair path instead
- **baseline / known-good state** - documented working configuration before the change; required to prove rollback
- **reversible action** - change that can be undone to restore prior state (service restart, config rollback, reconnect cable)
- **evidence-destroying action** - step that overwrites logs, changes timestamps, or removes the ability to prove what failed (power cycle that clears volatile error state, reinstall that wipes logs, part replacement before testing)


**study sources:**

- **Guide-owned:** the safety triage below and the exact stop triggers are the primary learning material. no external safety video can substitute for recognizing the exact mandatory stops in the assessment.
- **[Professor Messer, Safety Procedures 220-1202](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/safety-procedures-220-1202/)** - covers ESD, electrical safety, physical hazards, and proper handling. free, verified 2026-07-11
- **[iFixit, What to do with a swollen battery](https://www.ifixit.com/Wiki/What_to_do_with_a_swollen_battery)** - swollen battery recognition and safe handling procedure. free, verified 2026-07-11
- optional regulatory context: [OSHA electrical safety](https://www.osha.gov/electrical) establishes regulatory baseline for electrical work

**do this - C03-SAFE-A (12-case safety triage):**

you'll classify twelve support scenarios into one of three exact classes, then complete a four-column evidence/hypothesis log for one safe case. commit classifications and reasoning before checking the oracle.

**three exact safety classes:**

- **proceed with controls** - safe to continue with documented precautions (ESD protection, proper tools, two-person lift, ventilation, or baseline/rollback prep)
- **power down and isolate** - immediate stop, power off, disconnect from mains/charging, secure area, inform affected users, escalate to qualified owner
- **stop and escalate** - halt work without touching the system further, preserve evidence/error state, document observation, escalate to specialized team (safety officer, vendor, security, qualified technician, licensed electrician)

**twelve scenarios:**

1. Desktop tower power supply is open for inspection. AC mains cable is disconnected.
2. Laptop battery is visibly swollen and the case is slightly separated. User says it still charges.
3. User reports "computer wont start." You open the case and find one RAM stick unplugged; others are seated.
4. Laser printer fuser area is hot to touch after a long print job; temperature feels consistent with previous observations during operation.
5. Sealed OEM toner cartridge arrived in original packaging with manufacturer installation instructions.
6. Rack-mounted server needs to be moved to a different rack position. Estimated weight 35 kg.
7. USB-C cable jacket is frayed, exposing internal wires near the connector. Cable carries data and 60W PD.
8. User spilled water on a laptop keyboard 10 minutes ago. Laptop was immediately powered off and unplugged; visible moisture remains.
9. Cleaning agent bottle on the tech bench has no label. Another tech says "its just the usual screen cleaner."
10. Spare lithium-ion battery in storage has visible swelling and a dented case.
11. Workspace bench has a grounded ESD mat; wrist strap is connected to mat ground point; device is unplugged.
12. Desktop case fan intake is blocked by dust buildup; system runs but is warmer than baseline.

**required four-column evidence/hypothesis log for one randomly selected safe case (from proceed/power-down classes only):**

| Observation | Predicted risk if ignored | Required control | How control reduces risk |
|---|---|---|---|

**measurable gate:** at least **11/12** correct classifications; **all four mandatory stops** (open PSU, swollen battery, wet laptop, unknown chemical) must be correct. Any missed mandatory stop is automatic retry. commit classification table and one evidence log before oracle.

<details>
<summary><strong>truth oracle (click to reveal after commitment)</strong></summary>

1. **stop and escalate** - open PSU exposes mains voltage (120V/240V AC); **mandatory stop** even when disconnected; requires qualified technician or licensed electrician; do not probe internal PSU components
2. **power down and isolate** - swollen battery is **mandatory stop**; thermal runaway/fire risk; immediate power-down, stop charging, isolate, notify safety team
3. **proceed with controls** - RAM reseat is safe; ESD precaution (grounded wrist strap on bare chassis ground), power disconnected, baseline snapshot if applicable
4. **proceed with controls** - operational heat during/after use is expected; observe/compare with baseline; fuser is not user-serviceable but external temperature assessment during normal operation is safe
5. **proceed with controls** - sealed toner with manufacturer guide; follow installation procedure; use proper handling and ventilation per manufacturer SDS
6. **proceed with controls** - heavy equipment requires **two-person lift**, proper grip, clear path, coordinated movement; no solo lift for 35 kg server
7. **proceed with controls** - frayed low-voltage cable (USB-C max 20V/5A for PD) can be replaced; inspect for short, replace cable, document; no internal PSU work required
8. **power down and isolate** - liquid exposure is **mandatory stop** until completely dry; continued power risks short/corrosion; requires minimum dry time per vendor manual, inspection before re-power
9. **stop and escalate** - unknown chemical is **mandatory stop**; cannot assume safety without SDS; escalate to supervisor/safety officer for identification and proper SDS
10. **power down and isolate** - swollen/damaged lithium battery is **mandatory stop**; swelling + dent = potential internal short or leakage; isolate, do not charge/use, escalate to approved battery disposal procedure
11. **proceed with controls** - grounded ESD mat + strap connected to mat ground; power disconnected; proper ESD path established; proceed with component work
12. **proceed with controls** - dust removal requires proper ventilation and short bursts of compressed air per manufacturer SDS, or manufacturer-approved vacuum method where specified; restores airflow and prevents thermal fault

**Four mandatory stops that override the 11/12 count:**
- Scenario 1 (open PSU with mains voltage exposure)
- Scenario 2 (swollen battery)
- Scenario 8 (wet laptop without dry time)
- Scenario 9 (unknown/unlabelled chemical)

Missing any mandatory stop is a **critical error** and requires C03-SAFE-B retry regardless of the 11/12 score.

</details>


**changed retry:** if <11/12 or any mandatory stop incorrect, take **C03-SAFE-B** with twelve changed scenarios:

1. Live UPS cabinet (mains-powered, 120V/240V internal) requires internal battery inspection during business hours.
2. Smartphone battery pack is warm and slightly expanded; user reports faster-than-normal battery drain.
3. M.2 SSD is disconnected; no other components were touched; system is powered off and unplugged.
4. Laser printer just completed warmup cycle; temperature feels normal for post-warmup state; no error codes or unusual smell.
5. Sealed OEM toner cartridge arrived in original packaging; manufacturer installation instructions included.
6. Multi-function printer needs to be relocated 4 meters. Estimated weight 50 kg.
7. Laptop charger cable (low-voltage DC, 19V 3.42A) has visible wire strands near the barrel connector.
8. Laptop was powered off immediately after liquid exposure; device has been drying in a ventilated area for 72 hours; no visible moisture remains; vendor manual specifies 72h minimum dry time before inspection.
9. Aerosol electronics cleaner has manufacturer label intact and current SDS available in the work area.
10. Approved lithium battery recycling bin is labelled and available; replacement battery is intact, non-swollen, and within expiration date.
11. ESD-safe work mat is grounded to building ground; wrist strap is connected to mat ground point; device power is disconnected.
12. Desktop intake vents show dust accumulation; system boots and runs; internal temperatures are slightly elevated but within manufacturer thermal limits.

Same three classes; same mandatory-stop rule. **Four new mandatory stops:** live UPS internal work without qualified technician/licensed electrician, swollen/expanded battery pack, wet device before minimum vendor-specified dry time, and unknown/unlabelled chemical without SDS. Truth table changes but patterns remain: recognize mains voltage boundaries, distinguish operational heat from thermal faults, verify manufacturer procedures, apply two-person lift for heavy equipment, require SDS for chemicals, and follow vendor-specified safety procedures.

**critical errors:**
- missing any mandatory stop (open PSU with mains exposure, swollen/expanded battery, wet device before vendor-specified dry time, unlabelled chemical without SDS, or live UPS/mains work without qualified technician/licensed electrician)
- treating ESD wrist strap as protection against mains voltage (strap grounds chassis, not live mains)
- claiming sealed components or warranty seals are optional (breaking seal may void warranty and require vendor-only repair path)
- bypassing vendor-specified dry time or safety procedures
- disposing batteries, toner, or electronics in general waste without following approved disposal procedures

**can u explain it?** ✅ - score 7/8:

*"Explain why a swollen laptop battery requires immediate power-down and isolation, even if the device still charges and runs. Include the words thermal runaway, fire risk, and mandatory stop. Then explain the difference between chassis ground (where the ESD wrist strap connects) and mains ground, and why the strap does not protect against AC line voltage. Finally, describe one scenario where u have the technical skill to fix the problem but authorization requires escalation, and what evidence the receiving team needs."*

---

## shared-foundation test-out (if skipping foundations)

if u have prior experience and want to skip Shared Foundations, u must pass the **SF-XFER-A** cold case below. a cert or job title permits the attempt but waives nothing - u still need the evidence. passing this lets u enter B0 directly.

<details>
<summary><strong>SF-XFER-A - Northstar kiosk evidence failure (click to reveal)</strong></summary>

**scenario:**

You are supporting an isolated training kiosk named `SUP-01`; all names and addresses are synthetic. A reporting app is slow, `/opt/support/collect.sh` will not run, the HTTPS endpoint `kb.lab.example` fails while public web works, and the case repository contains yesterday's notes but no accepted handoff. You have 45 minutes. Do not use administrator/root privileges, disable TLS validation, change shared DNS, or read an oracle. Commit a diagnosis packet that separates observations from inferences and gives the smallest authorized next action for each symptom.

**supplied evidence cards (before your attempt):**

| Card | Exact evidence |
|---|---|
| `SF-A1 execution` | `SUP-01` has 2 GiB RAM. Process `reporter` uses 1.55 GiB RSS; committed memory is 1.91/2.00 GiB; swap-in is sustained. CPU is 22%, storage latency is 2 ms, SMART is healthy. Closing `reporter` on a cloned run returns committed memory to 0.48 GiB and the UI latency clears. |
| `SF-A2 shell` | `pwd` is `/opt/support`; `command -v bash` is `/usr/bin/bash`; script first line is `#!/usr/bin/env bash`; `ls -l` shows `-rw-r----- root support collect.sh`; direct invocation returns `Permission denied` and exit **126**; `bash collect.sh` on a copy produces expected stdout and one deliberate stderr warning. |
| `SF-A3 network` | Client resolver returns `kb.lab.example A 192.0.2.44`; intended change record says `192.0.2.45`. TCP 443 to `.45` succeeds. A curl request using `--resolve kb.lab.example:443:192.0.2.45` against its HTTPS `/health` path validates a certificate for `kb.lab.example` and returns HTTP 200. `.44` times out. |
| `SF-A4 Git` | `git status --short` shows ` M evidence.md` and `?? diagnosis.md`; `git log -1 --oneline` is yesterday's baseline; no secret is present. The acceptance branch is `case/SF-XFER-A`. |

**required practical evidence (8/8):**

1. Identify memory pressure, not CPU/storage, and cite before/after process evidence
2. Trace stored program → process/RAM → scheduler/CPU sufficiently to explain why stopping the process changes available memory
3. Identify missing execute permission and exit 126; do not use `chmod 777` or privilege escalation
4. Show a safe copy-only repair (`chmod u+x` only on a learner-owned copy) and separately capture stdout, stderr, and exit status
5. Trace stub resolver → intended A record → TCP 443 → TLS name validation → HTTP 200 and identify stale DNS data as the failed dependency
6. Preserve TLS verification; a hosts-file or `-k` workaround is not accepted as repair
7. Create `diagnosis.md` with reported/observed/inferred/changed labels and redact environment identifiers beyond the synthetic values
8. `git add`, commit on `case/SF-XFER-A` with a meaningful message, and show clean status plus commit ID (no push required)

**explanation prompt:** narrate `storage → process in RAM → CPU scheduling`, shell parse → command/path → process → streams → exit code, DNS → TCP → TLS → HTTP, and working tree → staging → commit/parent. The near-transfer probe changes two facts: the process is CPU-bound with normal commit, and DNS is correct but TLS presents the wrong hostname. Full credit requires revising the layer diagnosis instead of repeating the original fixes.

**pass gate:** practical 8/8; explanation 7/8, causal chain 2; no critical error; artifact committed before oracle.

**critical errors:** unsafe elevation or broad permission; disabling TLS verification; editing shared/production DNS; claiming a snapshot is backup; including a password/token/PII; fabricating a command/result; or treating a Git screenshot/uncommitted file as reproducible evidence.

**truth oracle (commit before revealing):**

1. Memory pressure (1.55 GiB / 2 GiB); stopping `reporter` frees memory
2. Process loads from storage into RAM; scheduler allocates CPU time slices
3. Exit 126 = permission denied (missing execute bit)
4. `chmod u+x collect.sh` on owned copy; `./collect.sh >out.txt 2>err.txt; echo $?` captures all three streams
5. Stale DNS returns `.44` (times out); correct address is `.45` (works with `--resolve`)
6. TLS validation must remain enabled (hosts file bypasses DNS but is not authorized repair for shared DNS)
7. Diagnosis separates reported/observed/inferred/changed; no real hostnames/IPs beyond RFC 5737 examples
8. `git add diagnosis.md; git commit -m "SF-XFER-A diagnosis"; git status` shows clean with commit ID

**changed retry SF-XFER-B:** 4 GiB host with CPU-bound `collector` and normal memory; script is executable but invokes missing command bc noninteractive `PATH` omits `/opt/lab/bin` (exit 127); DNS correct but server cert is for `old-kb.lab.example`; repo has staged secret-like test string that must be removed before commit. Same eight claims and rubric apply.

**re-entry if failed:**
- execution/memory fail → Shared Foundations Block 1, then SF-XFER-B execution card
- shell/path/permissions fail → Shared Foundations Block 2, then SF-XFER-B shell card
- DNS/TCP/TLS/HTTP fail → Shared Foundations Block 3, then SF-XFER-B network card
- Git/evidence hygiene fail → Shared Foundations Block 4, then SF-XFER-B repository card
- if pass → enter B0 at C01

</details>

---

## B0 exit case

**B0-EXIT-A - constrained host and unsafe battery:**

youve completed C01-C03 and are ready to start B1. your host has 8 GiB RAM, 11 GiB free storage, a valid VirtualBox base install (no Extension Pack), and a working Packet Tracer simulation. a spare laptop battery from the storage room is visibly swollen; a manager asks u to "just keep it charging so we can use the laptop for one more day." ur planned B1 work will need two simultaneous 4 GiB VMs and 35 GiB storage.

**required decisions (8/8):**

1. identify the capacity conflict between current host resources and B1 requirements
2. choose the valid route: run VMs sequentially, reduce VM allocations, upgrade storage, or accept supplied-case tier for capacity-limited scenarios
3. refuse battery use and charging; explain fire/thermal-runaway risk
4. name the safety-qualified owner who decides battery disposition (safety team, disposal procedure, qualified vendor)
5. distinguish snapshot (same-host, fast rollback) from export (portable VM copy) from independent backup (separate failure domain)
6. record cloud tier as `none` without treating it as a failure or deficiency (no tenant required for B0)
7. classify two O*NET support/admin tasks using a supplied local matrix
8. state owner and next-update commitment for any ticket requiring handoff

**hidden truth:** the safe no-hardware/simulation route preserves learning; buying hardware or obtaining a cloud tenant is not required. B1 has complete supplied-case alternatives for every capacity, tenant, Mac, or hardware gate.

**parallel B0-EXIT-B:** 16 GiB RAM but insufficient free storage; exported VM exists only on the same host disk; Packet Tracer account unavailable; unlabelled cleaning fluid found on bench. Same decision matrix: storage remediation first, recognize same-disk export limitation, accept supplied `.pkt` route, and chemical stop/SDS escalation.

**completion gate:** C01 artifacts 8/8, C02 classifications 10/10, C03 triage 11/12 with all mandatory stops, one exit form 8/8, and all explain gates 7/8. when all pass, B1 is unlocked meow

---

## optional: how does this connect to certifications?

dw, u dont need a cert to do B0 - the gates above are the actual requirements. but if ur heading toward CompTIA A+ later, this work covers parts of these current objectives (A+ 220-1201 Core 1 and 220-1202 Core 2):

**Core 1 (220-1201) Domain 4 - Virtualization and Cloud Computing:**
- **4.2 Summarize aspects of client-side virtualization** - purpose of virtual machines, resource requirements (CPU/RAM/storage), emulator requirements, security requirements, network requirements (internal vs external), hypervisor (Type 1 vs Type 2)

**Core 2 (220-1202) Domain 4 - Operational Procedures:**
- **4.1 Implement best practices associated with documentation and support systems information management** - ticketing systems (user information, device information, description of problems, categories, severity, escalation levels, clear/concise written communication), asset management (inventory lists, database system, asset tags and IDs, procurement life cycle, warranty and licensing), types of documents (network topology diagrams, knowledge base/articles, incident documentation), use of documentation (to find services, policies, procedures, and updates)
- **4.4 Explain common safety procedures** - electrostatic discharge (ESD) straps, ESD mats, equipment grounding, proper power handling, proper component handling and storage, antistatic bags, compliance with government regulations, personal safety (disconnect power before repairing PC, lifting techniques, electrical fire safety, safety goggles, air filtration mask)
- **4.5 Summarize environmental impacts and local environmental controls** - material safety data sheet (MSDS)/documentation for handling and disposal (proper battery disposal, proper toner disposal, proper PC/monitor disposal), temperature/humidity-level awareness and proper ventilation, power surges/under-voltage events/power failures (battery backup, surge suppressor)

**Post-gate optional bridge content (family F3 - recognition cards):**

after passing C03, u may complete the **F3** physical-control recognition cards. these cover the A+ Core 2 objective **2.1 Summarize various security measures and their purposes** - specifically the physical-control portion (15 cards total; the remaining 10 logical-control cards appear after C29 in B3).

<details>
<summary><strong>F3 physical controls (15/15) - optional post-C03</strong></summary>

For each physical security control, state its **primary purpose** (deterrence/detection/prevention) and **local policy owner** (who decides placement/configuration):

1. Bollards (concrete/steel posts blocking vehicle access to building perimeter)
2. Access control vestibule (mantrap / double-door airlock requiring one door to close before the next opens)
3. Badge reader (RFID/NFC card reader at entry points)
4. Video surveillance (CCTV cameras recording entry/exit and sensitive areas)
5. Alarm systems (intrusion detection triggering audible alarm and security response)
6. Motion sensors (passive infrared or microwave detecting movement in restricted areas)
7. Door locks (physical key, electronic, or biometric access control)
8. Equipment locks (cable locks, locking cabinets, or rack locks for hardware)
9. Cable locks (securing mobile devices, laptops, or peripherals to fixed points)
10. Security guard (physical human presence for access verification and response)
11. Fencing (perimeter barrier controlling access to facility grounds)
12. Key fob (electronic transmitter for wireless access control)
13. Smart card (chip-embedded card for access or authentication)
14. Mobile device as key (phone/app-based access credential)
15. Biometric locks (fingerprint, iris, facial recognition for access control)

**Recognition truth:** bollards/fencing = perimeter deterrence + prevention (physical security or facilities owner); mantrap/badge/biometric/guard = access prevention + verification (security/access-control owner); cameras/alarms/motion = detection (security operations); locks = equipment/access prevention (IT/physical security depending on asset). No control is foolproof alone; defense in depth combines layers.

**Pass:** 15/15 correctly classified with purpose and policy owner. This satisfies the A+ 2.1 physical-control recognition requirement.

</details>

**Post-gate optional bridge content (family F4 - legacy labels):**

after passing C03, u may complete the **F4** legacy terminology cards. these recognize outdated terms still present in some A+ materials but replaced by current practice.

<details>
<summary><strong>F4 legacy labels (4 cards) - optional post-C03</strong></summary>

1. **MSDS (Material Safety Data Sheet)** - legacy term; now called **SDS (Safety Data Sheet)** under globally harmonized system (GHS). Modern references use SDS; MSDS appears in older A+ materials.
2. **Inverter (CCFL backlight)** - legacy laptop display technology using cold-cathode fluorescent lamp with inverter; modern laptops use **LED backlight** (no inverter). Inverter replacement was common pre-2010; current repair is LED strip or panel.
3. **Legacy video connectors (VGA, DVI-I, S-Video)** - analog or transitional connectors largely replaced by **HDMI, DisplayPort, USB-C with DisplayPort Alt Mode**. VGA/DVI still appear in legacy equipment and A+ objectives but are not preferred for new installations.
4. **Format vs sanitize distinction** - "format" suggests making a drive reusable (quick format leaves data recoverable); **sanitization** or **secure erase** (ATA Secure Erase, cryptographic erase, or approved multi-pass overwrite per NIST SP 800-88) is the correct term for data destruction before disposal or repurposing. A+ may use "format" loosely; real disposal policy requires sanitization verification.
5. **Lighting and magnetometer for physical security** - adequate lighting (deterrence/detection at perimeter/entry) and magnetometer/metal detector (contraband detection at controlled entry) belong to the physical-control set. Lighting owner is typically facilities/physical security; magnetometer owner is security operations. Both support defense in depth but do not constitute complete perimeter security alone.
6. **Vendor-specific compressed-air and vacuum cautions** - while compressed air is a common cleaning method, always follow the manufacturer SDS for proper ventilation and short-burst technique. Some manufacturers specify ESD-safe vacuum methods for certain components; others prohibit vacuum use. Never assume universal application without checking vendor guidance.

**Recognition truth:** all cards recognize legacy/insufficient terms or vendor-specific boundaries and state the current alternative or proper scope. MSDS→SDS is purely naming; inverter→LED is technology shift; legacy connectors are capability-limited; format≠sanitization is a security/disposal distinction; lighting/magnetometer recognize the physical-control breadth; compressed-air/vacuum respect manufacturer boundaries.

**Pass:** 6/6 correctly updated with modern term or practice noted.

</details>

the difference: A+ asks "what is a hypervisor?" or "what does ESD stand for?" after separate study. this guide teaches hypervisor isolation through rollback proof and safety through real triage with mandatory stops. u learn the mechanism, pass measurable + explain gates, then find urself casually handling A+ recall questions bc u already used the thing qwq

**the order stays mechanism → lab → explain → optional checkpoint translation**. ur not studying for the exam - ur learning the actual job, and exam readiness is the side effect meow


---

## next session - what changes after B0?

**retrieval check (first 5 minutes next time u sit down):**

without opening this file, answer these cold prompts from B0:

1. name three things a hypervisor isolates and two limits of that isolation
2. classify "evaluate LAN/WAN performance and recommend changes" under a Help Desk vs Network Support authority matrix
3. **changed safety micro-case:** a desktop UPS (uninterruptible power supply) is beeping and showing a red "replace battery" indicator. The UPS is plugged into mains power and currently supporting two monitors and a desk phone. What is your **classification** (proceed/power-down/stop-escalate), **immediate action**, and **who owns** the battery replacement?

**truth for retrieval 3:** **power down and isolate** - UPS contains mains voltage (120V/240V) and lead-acid or lithium battery; internal work requires qualified technician or vendor-authorized technician (some UPS systems require licensed electrician). Immediate action: document the error, safely power down supported devices using normal shutdown, unplug UPS from mains once devices are off, label as faulty, and escalate to qualified technician or vendor. Service Desk does not open or service internal UPS components.

<details>
<summary><strong>hidden B0 exit truth (click to reveal after all C01-C03 and exit form completion)</strong></summary>

The safe no-hardware/simulation route preserves learning. Buying hardware or obtaining a cloud tenant is not required. B1 has complete supplied-case alternatives for every capacity, tenant, Mac, or hardware gate. Recording `none` as your cloud tier is accurate and acceptable. Sequential VMs, smaller allocations, or supplied-case evidence are all valid continuation paths.

</details>

if u blank or give a vague answer, return to the exact explain gate that covers it. retrieval gaps caught now stay fixed; gaps discovered in B3 cost days qwq

**B1 preview:**

B0 built the recovery safety net and the professional boundaries. B1 teaches the technical floor: endpoint hardware (power, RAM, storage, displays, laptops, printers), Windows/Linux/macOS support fundamentals, and the Stage 1 guided ticket handoff.

ur VirtualBox baseline from C01 becomes the Windows client for B1. Packet Tracer stays with u through B2. by the time u finish B1, ull have handled real (or simulation-equivalent) no-start diagnosis, file recovery, service troubleshooting, ACL repair, and a documented printer ticket with handoff evidence.

the 2 h/day rhythm stays the same. B1 is 129h total, about 9 weeks at that pace. dw if that sounds long - the mechanism depth is what makes support stick instead of fading after the first job change meow

**if u skip B0 gates:**

test-out exists bc some learners already have this foundation. but if u skip the measurable gates and just read, B1 will surface every gap when it asks u to snapshot a fault, refuse unsafe work, or write ur first handoff. better to spend 12h now proving the floor than repeating B1 cases bc evidence hygiene wasnt real yet.

**ur ready for B1 when:**

- [ ] C01 8/8 artifacts committed and explained
- [ ] C02 10/10 classifications plus authority boundaries
- [ ] C03 11/12 safety triage with all mandatory stops correct
- [ ] one B0-EXIT form 8/8
- [ ] all explain gates pass 7/8 with causal chain = 2

when the checkboxes are real (not just checked bc u read the page), [B1 - Foundations](01-foundations.md) is the next file. if any gate isnt solid, stay here and fix it. B1 will not slow down to reteach snapshot/export/stop-work patterns meow

---

*This block verified 2026-07-11. VirtualBox 7.2.12 base package GPLv3; Windows 11 Enterprise evaluation 90 days; Packet Tracer free tier may require Cisco account; no M365/Entra/Intune tenant required for B0. Sources resolve; test procedures reproduce. Report dead links or incorrect facts to the maintainer.*
