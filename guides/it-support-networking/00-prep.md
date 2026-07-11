# B0 - lab, safety, and support evidence (~12h)

> **before endpoint repair, before networking, before identity - this is the floor.**
> preflight your environment, learn what u can and cant touch, and practice the one habit that keeps data safe: test rollback before trusting a change meow

**Time:** ~12h total (~6 days at 2 h/day)  
[Previous: Shared Foundations](../../start-here/foundations.md) · [Hub](README.md) · [Next: B1 - endpoint + OS support](01-foundations.md)

---

## where u are rn

if u just cleared [Shared Foundations](../../start-here/foundations.md) (or tested out with its cold-case evidence), ur ready for B0. this short 12h block is the actual start of IT Support work - not generic computing, but the safe lab setup, professional boundaries, and evidence habits every support role depends on.

**the honest career ladder:** Help Desk or Service Desk is the normal first step. u handle user questions, standard requests, guided troubleshooting, and clean notes inside an approved scope. Desktop Support or a NOC usually comes next, with deeper endpoint repair or network evidence work. junior systems and network roles touch shared infrastructure under change authority.

B0 teaches the floor all of them share: know what u can touch, preserve the state before changing it, and leave enough evidence for the next person to continue.

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

the artifact rules look bigger than the lab... dw, u mostly fill them as u work.

the point is simple: another tech should be able to tell what u actually saw, what u changed, what the result proves, and where the claim stops. open the exact fields when ur ready to build the first packet meow

<details>
<summary><strong>exact artifact fields + redaction rules</strong></summary>

keep these field names even if u represent them as Markdown front matter, JSON, CSV columns, or a visible table:

| Required field | Contract |
|---|---|
| `artifact_id` | Stable synthetic ID, unique within your evidence repository. |
| `artifact_type` | One value from the artifact schema used by the task. |
| `case_id` / `cluster_ids` | Exact case form and owning C-cluster(s). |
| `created_at_utc` / `updated_at_utc` | ISO 8601 UTC timestamp. |
| `author_role` / `reviewer_role` | Synthetic role, not a personal name. Use `self-review` where applicable. |
| `aid_level` | `A0`, `A1`, `A2`, or `A3`, plus the exact aid used. |
| `evidence_tier` | Exactly one of `live-owned`, `live-authorized-lab`, `simulation-supplied`, or `case-analysis`; add the product entitlement label where relevant. |
| `environment` | OS/tool/version, topology or tenant label, runtime, and disposable/owned/authorized boundary. |
| `source_refs` | Exact guide/source/case references and version/check date. |
| `commit_before_oracle` | Commit ID and timestamp, or `not_applicable` with a reason for a platform-only attempt. |
| `result` | `pass`, `repair`, or `fail`, with numeric gates and critical-error state. |
| `redaction_status` | `checked`, checker/date, and findings count. |
| `integrity` | SHA-256 for files/config exports where stable; otherwise an explicit reason it is not meaningful. |

each observation or action row in the evidence log also uses these exact fields:

`event_id`, `artifact_id`, `timestamp_utc`, `case_id`, `actor_or_source`, `claim_class` (`reported|observed|inferred|changed`), `question_or_hypothesis`, `command_or_action`, `exact_scope`, `raw_result_reference`, `exit_code_or_status`, `interpretation`, `what_it_proves`, `what_it_does_not_prove`, `next_decision`, `authorization_reference`, `aid_level`, `evidence_tier`, `redaction_note`.

copy commands exactly, including parameters and targets. give every screenshot a timestamp, caption, and text transcription of the decisive field; when exportable text or state exists, a screenshot cannot be the only evidence.

put this visible claim block in every live or supplied artifact:

```text
evidence_tier: live-owned | live-authorized-lab | simulation-supplied | case-analysis
platform: <product and version or supplied case version>
entitlement: <none, license, developer sandbox, trial, paid tenant, hardware>
performed_actions: <exact actions actually performed>
observed_only: <outputs/cards supplied rather than generated>
claims_supported: <finite claims this artifact proves>
claims_not_supported: <live/physical/admin claims it cannot prove>
expires_or_checked_at: <UTC date or not applicable>
```

mixed artifacts label each component separately. live VirtualBox work plus a supplied Packet Tracer trace is not `live Packet Tracer`, mhm.

**secret + PII boundary:** never retain or commit passwords; MFA/OTP/recovery codes; bearer/access/ID/refresh tokens; session cookies; private keys; client secrets; API keys; connection strings; password hashes; wireless PSKs; real names, personal email/phone/address, government/health/payment identifiers; real customer domains; raw production ticket text; device serial/IMEI/MAC tied to a person; unapproved internal IP/hostname; or raw consent records.

use this redaction method every time:

1. generate synthetic fixtures first (`RITN-USER1`, `DC1.corp.example`, RFC 5737 addresses) rather than collecting real data
2. export the minimum fields; for tokens, retain only nonsecret redacted claims needed by the case (`iss`, synthetic `tid`, `aud`, `exp`, scopes/roles), never the serialized token
3. replace sensitive values with typed markers such as `[REDACTED-TOKEN]` or a stable synthetic mapping; remove originals from Git history, image metadata, terminal captures, hidden columns, JSON, logs, and archives
4. crop/redact screenshots before commit, remove EXIF/metadata, and run a text/OCR review; use opaque removal, not reversible blur
5. search the final tree and commit diff for secret patterns, personal identifiers, private-key headers, JWT-shaped strings, cloud credentials, and lab passwords; inspect every positive and every image
6. if a secret was committed, revoke/rotate it first, use the maintainer-approved history process, then record the incident without reproducing the value; deleting only the current file is insufficient

redaction must preserve reproducibility: keep synthetic IDs stable, retain the timestamps/status/field names the oracle needs, and state what was removed. fabricating evidence to fill a redacted field is a critical error.

</details>

these rules apply to every C01-C03 artifact and carry forward through B1-B5. clean evidence hygiene now prevents capstone rejection later meow

---

## the path (todo-tree)

- [ ] **C01 - preflight, access, and rollback** (~5h)
- [ ] **C02 - support role scope and escalation** (~2h)
- [ ] **C03 - safety and evidence isolation** (~5h)
- [ ] ✅ **B0 exit check** - C01 8/8, C02 10/10, C03 11/12, one exit form

these public-repo boxes dont save ur progress. fork the repo, copy this list into Obsidian/OneNote, or print it if u want boxes u can actually mark. the real progress signal is still both gates, no matter where ur list lives meow

---

## C01 · preflight, access, and rollback (~5h)

**the idea** - make ur first lab recoverable before u use it for anything harder. a snapshot should undo one bad guest change, and a fresh import should prove the exported copy really boots.

**how/why it actually works** - this is ur safety net, so build it before u start breaking things on purpose...

a **VM (virtual machine)** is a guest computer presented by a **hypervisor** on a physical **host**. the hypervisor supplies virtual CPU, RAM, disk, firmware, and network devices, then schedules or translates guest work onto host resources. that boundary makes the guest disposable, but it is not magic containment: shared folders, bridged networking, host resource exhaustion, and hypervisor defects can still cross or weaken it.

network mode chooses a failure boundary. VirtualBox **NAT** normally lets the guest start outbound connections through a virtual router and keeps unsolicited LAN inbound traffic from reaching it unless u add forwarding. that does **not** mean the guest can reach a service bound only to the host's loopback. `127.0.0.1` inside the guest means the guest itself; host loopback needs an intentionally exposed host address/path. **host-only** joins the host and selected guests without external routing, while **bridged** places the guest on the physical LAN and needs explicit authorization.

three recovery objects do different jobs:

1. a **snapshot** records VM state and redirects later disk writes into a dependent chain. restore can remove one bad lab change fast, but the base disk, snapshot metadata, and host storage can fail together.
2. an **OVA/OVF export** packages the current VM state, not its snapshot tree. importing it into a new directory/name with the original VM powered off proves the imported copy no longer depends on the original VM registration or folder. it does **not** prove compatibility with every other host, and a same-disk export still shares the host's failure domain.
3. an **independent backup** is a recoverable copy on a separate protected failure domain. the copy only earns that claim after a restore/import and acceptance test succeed.

so the chain is baseline -> snapshot -> marker/change -> restore -> prove marker absent -> export -> fresh import -> acceptance test. each arrow has evidence. dw, this feels fussy once and saves hours later ;w;

**words u gotta be able to say:**

- **host** - the physical computer running the hypervisor
- **guest / VM** - the simulated computer running inside the hypervisor
- **hypervisor** - software that creates and manages VMs (VirtualBox, VMware, Hyper-V)
- **snapshot** - point-in-time guest state capture; fast rollback but stored with the VM on the same host
- **export** - portable VM package independent of the original registration/folder after a successful fresh import
- **`.ova` / OVF** - Open Virtualization Format; standard portable VM package
- **baseline** - known-good starting state before experiments
- **rollback** - restore to an earlier snapshot
- **disposable** - can be deleted and recreated without data loss
- **isolation** - guest changes dont affect the host (within hypervisor limits)
- **NAT network mode** - guest starts outbound connections through a virtual router; host loopback is still a separate boundary
- **host-only mode** - private network between host and guest(s); no external network
- **bridged mode** - guest appears as separate device on host's physical LAN (lab risk)
- **independent backup** - copy on a separate failure domain (different disk/machine/cloud)

**study sources (pick what fits your style):**

- **[VirtualBox First Steps (official manual)](https://www.virtualbox.org/manual/ch01.html)** - **free**, no account; use the VM, snapshot, import, and export sections for the recovery loop.
- **rather watch:** no video for this one. the buttons are less useful than doing the restore yourself, meow
- **[VirtualBox Networking (official manual)](https://www.virtualbox.org/manual/ch06.html)** - **free**, no account; check NAT, host-only, internal, bridged, and port-forwarding boundaries here.
- **[Cisco Packet Tracer training/download](https://www.netacad.com/courses/packet-tracer)** - **free**, with a Cisco account/download flow that may apply; use it for the small switch-and-PC preflight.
- **[Microsoft Learn - Using Hyper-V checkpoints](https://learn.microsoft.com/en-us/windows-server/virtualization/hyper-v/checkpoints)** - **free** reference; the checkpoint warning makes the snapshot-versus-backup boundary concrete.

**do this - C01-LAB-A (preferred live route):**

use VirtualBox plus Packet Tracer when ur host and access allow it. no Extension Pack is required. commit the eight-result packet before opening either oracle.

**required artifacts (8/8):**

1. **host report** - actual CPU/RAM/free storage, OS, VirtualBox version, base-package license, and whether the planned guest fits without starving the host
2. **VM boot** - one disposable small VM using legitimate media boots; Windows is optional
3. **network mode** - record NAT or host-only (not bridged for lab safety)
4. **snapshot-before** - baseline snapshot named `B0-baseline` created **before** making the marker file
5. **marker changed** - after the baseline, create `C:\LAB-MARKER-A.txt` on Windows or `/tmp/LAB-MARKER-A.txt` on Linux with a synthetic learner ID and UTC date, then take a second snapshot
6. **marker absent after restore** - roll back to `B0-baseline`, boot, verify marker file does not exist (proves rollback works and that snapshot was taken before marker creation)
7. **export validation** - export to `.ova`, record size and SHA-256, power off the original, import into a new directory/name, boot, and pass the marker/expected-OS acceptance test. claim only independence from the original registration/folder; record host compatibility and whether storage is a separate failure domain
8. **Packet Tracer test** - complete the network preflight case below

**Packet Tracer network preflight case (C01-PT-A):**

if u have Packet Tracer installed, build this exact topology and prove ping:

- **supplied topology:** one switch (2960 or similar), two PCs connected to switch ports
- **addresses:** PC1 = `192.168.1.10/24`, PC2 = `192.168.1.11/24`
- **test:** ping from PC1 to PC2; verify success in simulation mode or realtime
- **evidence:** save as `C01-network-test.pkt`; record ping result (success/reply count)

**C01-PT-A supplied fallback prompt (if account/download is unavailable):**

- **supplied scenario:** two PCs (`PC1` at `192.168.1.10/24`, `PC2` at `192.168.1.11/24`) connected to one switch; switch ports Fa0/1 and Fa0/2 are up/up
- **supplied event cards:** PC1 begins with no ARP entry; the first frame is an ARP request to `ff:ff:ff:ff:ff:ff`; PC2 returns an ARP reply; four ICMP replies follow; the switch table begins empty
- **commit these decisions:** the address PC1 needs, how it learns that address, the first broadcast/forwarding behavior, the learned port entries, and why the later ICMP frame is directed
- **claim boundary:** label this component `simulation-supplied`; it supports Packet Tracer/network reasoning, not installation, live device, or physical cabling claims

<details>
<summary><strong>C01-PT-A oracle - open only after commitment</strong></summary>

PC1 needs PC2's MAC, broadcasts ARP, learns the MAC from PC2's reply, then sends the ICMP Ethernet frame to that destination. the switch learns PC1 on Fa0/1 from the source MAC, floods the broadcast, learns PC2 on Fa0/2 from the reply, and directs later frames by its MAC table. four replies satisfy the supplied Packet Tracer test.

</details>

**access-limited route:**

if ur machine cannot run a VM or legitimate media is unavailable, use supplied cards to rehearse the decisions and label them `simulation-supplied`. that practice does **not** replace the live snapshot, restore, export, or fresh-import proof. dont invent a timestamp, hash, address, or live/admin result to fill a blank one. come back to C01 when u have an authorized host/media route; buying hardware or opening a cloud tenant is not required.

the Packet Tracer item is the exception: its event-card fallback above can satisfy the network-reasoning part when account/download access is blocked, as long as the artifact says `simulation-supplied`.

`none` cloud access is accepted. the cloud label is inventory, not a tenant gate.

**C01 measurable gate:** all **8/8** items pass, with live evidence for the VM/snapshot/restore/export chain and either live or honestly labelled supplied evidence for the Packet Tracer item.

<details>
<summary><strong>C01-LAB-A oracle - open only after the eight-item commitment</strong></summary>

1. the report must state actual access/capacity or the supplied access limits; neither missing hardware nor missing media is failure.
2. `Running` plus the expected console state supports boot; a supplied console supports no live-install/admin claim.
3. name the selected network mode and its boundary. NAT normally supports guest-originated outbound traffic without unsolicited LAN inbound; host-only normally gives host/guest local reachability without an automatic external route. guest `127.0.0.1` is always the guest itself.
4. the baseline snapshot must predate the marker.
5. the marker is the controlled changed state.
6. marker absent plus baseline match proves rollback to the recorded point; it does not prove backup.
7. fresh import with the original powered off proves independence from its registration/folder and a working import on the tested host. it does not prove other-host compatibility or separate-failure-domain recovery; same-disk storage is a lab copy.
8. the Packet Tracer truth is in its separately opened oracle above. `none` cloud access is accepted.

</details>

**changed retry - C01-LAB-B:** commit a fresh **8/8** form at `A0`. the B form changes the marker, VM name, network-mode question, export directory/name, and Packet Tracer addresses. use the values on that form, not guesses from the A form.

the B oracle keeps the same boundaries: the access/tier claim stays bounded, the baseline precedes the marker, restore removes the marker, the fresh import proves only original-registration/folder independence on the tested host, and same-failure-domain storage is still a lab copy rather than resilient backup. the changed Packet Tracer trace still needs the ARP, switch-learning, and directed-forwarding decisions.

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

if ur VM media has an expiry or license boundary, write that in the artifact and keep the lab disposable. the recovery decisions stay the same meow

---

## C02 · support role scope and escalation (~2h)

**the idea** - scope tells u which actions belong to u and which need a clean handoff. a technically correct fix can still be wrong when u lack authorization or leave nobody owning the user update.

**how/why it actually works** - real talk: the hardest support skill isnt technical, its knowing when to stop...

every organization draws **scope** a lil differently. first-line support normally handles known procedures, standard requests, and guided troubleshooting inside a documented baseline. shared production changes, higher privilege, security incidents, vendor repair, and policy exceptions need explicit **authorization** and usually another owner.

why the boundary? shared changes need **evidence and rollback**. restarting one approved local service may be documented and reversible. changing a firewall rule, patching a domain controller, or granting admin rights affects other people, so it needs a change record, approval, a way back, and someone with that authority.

**escalation** transfers work or authority to a team with broader capability, while the original owner retains **responsibility** for tracking, user updates, and validation until closure. escalation is not "throw it over the wall and forget." a good handoff contains: record ID, symptom in user's words, scope, timeline, evidence collected, tests run, actions taken, exact reason for escalation, and requested next action.

the operational loop has seven useful moves:

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

**study sources (pick what fits your style):**

- **Guide-owned:** the mechanism above and the O*NET role-boundary practical below define scope. no external playlist owns this topic.
- **[O*NET OnLine - Computer User Support Specialists, 15-1232.00](https://www.onetonline.org/link/details/15-1232.00)** - **free**, no account; use the task list for the first-line side of the classification case.
- **[O*NET OnLine - Computer Network Support Specialists, 15-1231.00](https://www.onetonline.org/link/details/15-1231.00)** - **free**, no account; compare which tasks need network authority.
- **[Atlassian - What is a service request?](https://www.atlassian.com/itsm/service-request-management)** - **free** reference; useful when incident, request, problem, and change start blurring together. local policy still owns the workflow.
- **[Google SRE - Effective Troubleshooting](https://sre.google/sre-book/effective-troubleshooting/)** - **free** text; read the hypothesis and evidence parts when u catch urself jumping at the first plausible cause.


**do this - C02-ROLE-A:**

you'll classify ten O*NET tasks under a supplied authority matrix, then provide evidence/owner/user-update/trigger for each. commit answers before checking the oracle.

**supplied authority matrix for this case:**

- **Service Desk (L1) may perform:** user inquiry, bounded command observation within approved endpoint scope, approved equipment setup from standard build (deviations escalate), help-desk documentation, and user training after content approval
- **Service Desk must gather evidence and escalate (retaining user-update ownership):** major product faults, network diagnosis/change, and security-breach indicators
- **Network Support owns (under change authority):** router/switch configuration and fiber repair

**ten exact current task quotations from the two O*NET occupation pages above:**

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


**changed retry:** if <10/10 or boundary questions miss authority/escalation, take **C02-ROLE-B** using ten supplied case-local task summaries based on the same occupation families. these are deliberately labelled paraphrases, not exact O*NET quotations:

**supplied authority matrix for C02-ROLE-B:**

- **Service Desk may perform:** equipment inspection for delivery, maintain support records, bounded minor endpoint repair within approved scope, telephone connectivity support; contributes evidence to evaluations and requirements discussions
- **Service Desk must gather evidence and escalate:** performance evaluation decisions, network backup execution, wireless configuration, network documentation approval
- **Network Support owns (under change authority):** network backup execution, LAN/WAN performance evaluation and decisions, network change documentation approval, wireless equipment installation/configuration

**ten supplied paraphrases for this B case:**

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

**how/why it actually works** - **ESD** is charge equalizing between objects at different electrical potential. a grounded mat and resistor-limited wrist strap keep u, the de-energized chassis, and the work surface near the same potential. the strap protects components; it is never protection from live mains.

unplugging a PC and holding its power button can drain some low-voltage rails, but it does not make a sealed PSU, UPS power section, display high-voltage section, or laser-printer power area safe. capacitors can retain energy. a hot fuser routes through power-down, the vendor-specified cooling time, and the vendor procedure - never touching it or continuing around it while hot.

lithium-ion swelling means gas has formed inside a damaged cell. stop charging, do not press/puncture/bend it, isolate it from heat and combustibles, then use the manufacturer and local hazardous-waste route. toner and cleaning products follow the product label and **SDS (Safety Data Sheet)**; an unknown chemical is a stop, not a guessing game.

after the hazard screen, troubleshooting becomes evidence control: record scope/baseline -> form a falsifiable hypothesis -> predict evidence -> change one safe variable -> compare the result -> validate the original function -> document or roll back. safety, data, privacy, and authorization can stop that chain before technical diagnosis starts.

**words u gotta be able to say:**

- **stop-work condition** - observed hazard, missing authorization, or evidence-destroying risk that requires immediate halt
- **swollen / bulging battery** - lithium cell damage; mandatory power-down and isolation (fire/thermal runaway risk)
- **hot fuser** - printer hazard requiring power-down, vendor cooling time, and vendor procedure
- **mains voltage / line voltage** - AC power from the building supply; internal PSU or UPS work needs the qualified, authorized route
- **ESD (electrostatic discharge)** - charge equalization that can damage semiconductor gates
- **potential equalization** - bringing technician, chassis, and mat near the same electrical potential
- **Safety Data Sheet (SDS)** - hazard/handling info for toner, cleaning agents, compressed air, or any chemical; replaces legacy term MSDS
- **proper ventilation** - adequate airflow when using aerosol cleaners, handling toner, or working with chemical solvents
- **two-person lift** - heavy equipment (UPS, server, large printer) requires coordinated lift to prevent back injury
- **warranty seal / tamper-evident label** - manufacturer seal; breaking it may void warranty and require vendor repair path instead
- **baseline / known-good state** - documented working configuration before the change; required to prove rollback
- **reversible action** - change that can be undone to restore prior state (service restart, config rollback, reconnect cable)
- **evidence-destroying action** - step that overwrites logs, changes timestamps, or removes the ability to prove what failed (power cycle that clears volatile error state, reinstall that wipes logs, part replacement before testing)


**study sources (pick what fits your style):**

- **Guide-owned:** the safety triage below and the exact stop triggers are the primary learning material. no external safety video can substitute for recognizing the exact mandatory stops in the assessment.
- **[Professor Messer - Managing Electrostatic Discharge](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/managing-electrostatic-discharge-220-1202/)** - **free** video/transcript; see what the mat and strap protect, and what they do not.
- **[Professor Messer - Safety Procedures 220-1202](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/safety-procedures-220-1202/)** - **free** video/transcript; use for electrical, lifting, laser, and PPE breadth.
- **[iFixit - What to do with a swollen battery](https://www.ifixit.com/Wiki/What_to_do_with_a_swollen_battery)** - **free** reference; use it for the battery stop-work boundary.
- **[OSHA - Electrical](https://www.osha.gov/electrical)** - **free U.S. reference**; use it for electrical context, then follow ur local authority and site procedure.
- **[US EPA - Electronics Donation and Recycling](https://www.epa.gov/recycle/electronics-donation-and-recycling)** - **free U.S. reference**; use it for the electronics handoff, not as a universal local disposal rule.

**do this - C03-SAFE-A (12-case safety triage):**

you'll classify twelve support scenarios into one of three exact classes, then complete a four-column evidence/hypothesis log for one safe case. commit classifications and reasoning before checking the oracle.

**three exact safety classes:**

- **proceed with controls** - safe to continue with documented precautions (ESD protection, proper tools, two-person lift, ventilation, or baseline/rollback prep)
- **power down and isolate** - immediate stop, power off, disconnect from mains/charging, secure area, inform affected users, escalate to qualified owner
- **stop and escalate** - halt work without touching the system further, preserve evidence/error state, document the observation, and escalate to the named qualified or safety owner

**twelve scenarios:**

1. Desktop tower power supply is open for inspection. AC mains cable is disconnected.
2. Laptop battery is visibly swollen and the case is slightly separated. User says it still charges.
3. User reports "computer wont start." You open the case and find one RAM stick unplugged; others are seated.
4. Laser printer has just finished a long job; the fuser area is still hot. a ticket asks u to clear paper beside it now.
5. A small toner spill came from a known cartridge; its product label, current SDS, and vendor cleanup procedure are available.
6. A heavy UPS must be moved after a normal shutdown and disconnection; its cabinet will remain closed.
7. A USB-C cable jacket is frayed near the connector. the supplied label gives no capability beyond the cable being damaged.
8. User spilled water on a laptop keyboard 10 minutes ago. Laptop was immediately powered off and unplugged; visible moisture remains.
9. Cleaning agent bottle on the tech bench has no label. Another tech says "its just the usual screen cleaner."
10. A dead, intact lithium-ion battery must be discarded; the ticket does not name an approved recycler or local disposal procedure.
11. Workspace bench has a grounded ESD mat; wrist strap is connected to mat ground point; device is unplugged.
12. Desktop case fan intake is blocked by dust buildup; system runs but is warmer than baseline.

**required four-column evidence/hypothesis log for one randomly selected safe case (from proceed/power-down classes only):**

| Observation | Predicted risk if ignored | Required control | How control reduces risk |
|---|---|---|---|

**measurable gate:** at least **11/12** correct classifications; **all four mandatory stops** (open PSU, swollen battery, wet laptop, unknown chemical) must be correct. Any missed mandatory stop is automatic retry. commit classification table and one evidence log before oracle.

<details>
<summary><strong>truth oracle (click to reveal after commitment)</strong></summary>

1. **stop and escalate** - a disconnected open PSU can retain hazardous energy; **mandatory stop**. do not touch or probe it; hand off to the qualified/vendor route
2. **power down and isolate** - swollen battery is **mandatory stop**; thermal runaway/fire risk; immediate power-down, stop charging, isolate, notify safety team
3. **proceed with controls** - RAM reseat is safe; ESD precaution (grounded wrist strap on bare chassis ground), power disconnected, baseline snapshot if applicable
4. **power down and isolate** - do not touch or work around the hot fuser. power down, wait the vendor-specified cooling time, then follow the vendor jam/service procedure
5. **proceed with controls** - use the named vendor cleanup, SDS, ventilation, and PPE; do not improvise with compressed air or an ordinary vacuum
6. **proceed with controls** - keep the UPS closed and use the approved team-lift/move procedure after shutdown/disconnection; internal UPS work is out of scope
7. **power down and isolate** - stop using the damaged cable and replace it with a compatible undamaged cable. the supplied label does not prove any wider capability
8. **power down and isolate** - liquid exposure is **mandatory stop** until completely dry; continued power risks short/corrosion; requires minimum dry time per vendor manual, inspection before re-power
9. **stop and escalate** - unknown chemical is **mandatory stop**; cannot assume safety without SDS; escalate to supervisor/safety officer for identification and proper SDS
10. **stop and escalate** - do not use general waste. identify the battery and hand it to the manufacturer/local approved hazardous-waste or recycling route
11. **proceed with controls** - the supplied grounded mat and strap provide potential equalization for this de-energized device; keep that setup intact
12. **proceed with controls** - shut down/disconnect as the service manual requires, preserve the baseline, and use only the vendor-approved cleaning method before retesting airflow/temperature

**Four mandatory stops that override the 11/12 count:**
- Scenario 1 (open PSU with mains voltage exposure)
- Scenario 2 (swollen battery)
- Scenario 8 (wet laptop without dry time)
- Scenario 9 (unknown/unlabelled chemical)

Missing any mandatory stop is a **critical error** and requires C03-SAFE-B retry regardless of the 11/12 score.

</details>


**changed retry:** if <11/12 or any mandatory stop is wrong, commit **C03-SAFE-B** before opening its oracle:

1. A live UPS cabinet requires internal inspection while it remains connected to mains.
2. A disconnected battery pack is leaking and the area around it is not yet isolated.
3. M.2 SSD is disconnected; no other components were touched; system is powered off and unplugged.
4. A laser printer is powered down, its vendor cooling time has elapsed, and the external inspection area is cool.
5. Sealed OEM toner cartridge arrived in original packaging; manufacturer installation instructions included.
6. A heavy multi-function printer must move a short distance; the vendor move procedure and a trained two-person team are available.
7. A laptop charger cable has visible wire strands near its connector.
8. A laptop was powered off immediately after liquid exposure, has dried for the vendor-specified interval, and has no visible moisture. the next step is the vendor inspection, not automatic power-on.
9. Aerosol electronics cleaner has manufacturer label intact and current SDS available in the work area.
10. A dead, intact lithium battery and a labelled approved battery-recycling container are available under the local procedure.
11. ESD-safe work mat is grounded to building ground; wrist strap is connected to mat ground point; device power is disconnected.
12. Desktop intake vents show dust accumulation; system boots and runs; internal temperatures are slightly elevated but within manufacturer thermal limits.

same three classes. the dry laptop and labelled cleaner are deliberately changed facts, so classify the evidence u received instead of repeating A.

**C03-SAFE-B measurable gate:** at least **11/12**, with every mandatory stop present in B correct. any mandatory-stop miss voids the numeric score; the separately hidden packet identifies them when u score.

<details>
<summary><strong>C03-SAFE-B truth packet - open only after commitment</strong></summary>

1. **stop and escalate** - **mandatory stop**; do not open/touch live UPS internals. isolate access and route to the qualified/vendor electrical owner.
2. **power down and isolate** - **mandatory stop**; keep people/ignition away, do not touch or clean the leaking pack, and invoke the approved battery/emergency procedure.
3. **proceed with controls** - de-energized SSD reseat under verified ESD and service-manual controls.
4. **proceed with controls** - the printer is powered down, cool, and within the vendor inspection procedure; touching a hot fuser would still fail.
5. **proceed with controls** - install the sealed known toner only under its manufacturer instructions/SDS.
6. **proceed with controls** - use the trained team, clear path, and vendor move procedure; do not improvise or open it.
7. **power down and isolate** - stop using the damaged low-voltage lead and replace it with the correct undamaged part; do not infer a capability the supplied card does not state.
8. **proceed with controls** - continue only to the vendor inspection after the stated drying interval; the evidence does not authorize blind power-on.
9. **proceed with controls** - verify the label/SDS, ventilation, PPE, material compatibility, and vendor method before use.
10. **proceed with controls** - place the dead intact battery in the approved labelled route exactly as local procedure permits; record disposition.
11. **proceed with controls** - the device is de-energized and the verified mat/strap supplies potential equalization.
12. **proceed with controls** - power down/disconnect as required, use the vendor-approved dust method, then compare temperature/airflow with baseline.

score all twelve against this packet. only cases 1 and 2 are mandatory-stop overrides on B.

</details>

**critical errors:**
- missing any mandatory stop identified by the selected form's scoring packet
- treating ESD wrist strap as protection against mains voltage (strap grounds chassis, not live mains)
- touching or continuing work around a hot fuser instead of power-down, vendor cooling time, and vendor procedure
- bypassing vendor-specified dry time or safety procedures
- disposing batteries, toner, or electronics in general waste without following approved disposal procedures

**can u explain it?** ✅ - score 7/8:

*"Explain why a swollen laptop battery requires immediate power-down and isolation, even if the device still charges and runs. Include the words thermal runaway, fire risk, and mandatory stop. Then explain what potential equalization does for a de-energized chassis, why that is different from live mains protection, and why the strap cannot make AC work safe. Finally, describe one scenario where u have the technical skill to fix the problem but authorization requires escalation, and what evidence the receiving team needs."*

---

## shared-foundation test-out (if skipping foundations)

if u have prior experience and want to skip Shared Foundations, try the **SF-XFER-A** cold case when ur ready. a cert, course, or job title permits the attempt but waives nothing. pass its practical and explain gates, then enter B0. if one layer misses, the re-entry table sends u back to that exact Shared Foundations block.

<details>
<summary><strong>open the SF-XFER-A test-out case</strong></summary>

### SF-XFER-A - Northstar kiosk evidence failure

read the prompt and supplied cards now. commit all eight decisions and the explanation before opening the separate oracle.

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

<details>
<summary><strong>SF-XFER-A oracle - open only after commitment</strong></summary>

1. Memory pressure (1.55 GiB / 2 GiB); stopping `reporter` frees memory
2. Process loads from storage into RAM; scheduler allocates CPU time slices
3. Exit 126 = permission denied (missing execute bit)
4. `chmod u+x collect.sh` on owned copy; `./collect.sh >out.txt 2>err.txt; echo $?` captures all three streams
5. Stale DNS returns `.44` (times out); correct address is `.45` (works with `--resolve`)
6. TLS validation must remain enabled (hosts file bypasses DNS but is not authorized repair for shared DNS)
7. Diagnosis separates reported/observed/inferred/changed; no real hostnames/IPs beyond RFC 5737 examples
8. `git add diagnosis.md; git commit -m "SF-XFER-A diagnosis"; git status` shows clean with commit ID

</details>

**changed retry SF-XFER-B prompt:** a 4 GiB host has a CPU-bound `collector` with normal memory; the script is executable but its noninteractive `PATH` omits `/opt/lab/bin`, so its command lookup fails with exit 127; DNS is correct but the server certificate is for `old-kb.lab.example`; the repository has a staged secret-like test string. commit a new eight-decision packet at A0 using the same mechanism layers and safe boundaries before opening B truth.

<details>
<summary><strong>SF-XFER-B oracle - open only after the changed commitment</strong></summary>

1. CPU, not memory, is the constrained execution resource; normal commit means the A-form memory repair must be rejected.
2. trace stored program -> process in RAM -> CPU scheduling, then cite CPU evidence without claiming storage or memory pressure.
3. executable permission is already present; exit 127 points to command lookup failure in the noninteractive environment.
4. preserve least privilege and correct the owned test environment/path or invoke the exact approved executable; capture stdout, stderr, and status separately.
5. DNS reaches the intended address and TCP can connect, but TLS hostname validation fails on `old-kb.lab.example`.
6. do not use `-k`, replace trust material blindly, or edit shared DNS; route the wrong certificate/name binding to its owner.
7. remove the staged secret-like fixture from both the file/staging area before committing, record the redaction check, and never reproduce a real secret.
8. commit only the redacted diagnosis/evidence on the named case branch and show clean status plus commit ID.

</details>

**re-entry if failed:**
- execution/memory fail → Shared Foundations Block 1, then SF-XFER-B execution card
- shell/path/permissions fail → Shared Foundations Block 2, then SF-XFER-B shell card
- DNS/TCP/TLS/HTTP fail → Shared Foundations Block 3, then SF-XFER-B network card
- Git/evidence hygiene fail → Shared Foundations Block 4, then SF-XFER-B repository card
- if pass → enter B0 at C01

</details>

---

## B0 exit case

normal route uses A. B is the parallel repair form. for a test-out, calculate `SHA256(learner_id + UTC date + "B0")`; the low bit selects A/B and the next bit selects the C01 marker set. record the seed, selected form, aid level, and commit **before** opening that form's truth.

### B0-EXIT-A - constrained host and unsafe battery

ur host has 8 GiB RAM, 11 GiB free storage, a valid VirtualBox base install without the Extension Pack, a supplied Packet Tracer form, and cloud/access tier `none`. a pictured spare laptop pack is swollen; a fictional manager asks u to keep charging it. the intended B1 live plan needs two simultaneous 4 GiB VMs and 35 GiB storage.

the supplied local authority matrix says Service Desk owns approved documentation and user updates; Network Support owns router changes under change authority. classify these two tasks: `Document help desk requests and resolutions.` and `Configure wide area network (WAN) or local area network (LAN) routers or related equipment.`

commit **8/8** decisions: capacity conflict; viable continuation route; battery action; safety/disposal owner; snapshot/export/independent-backup distinction; cloud-tier interpretation; both task owners; and retained owner/next update.

<details>
<summary><strong>B0-EXIT-A truth - open only after the selected-form commitment</strong></summary>

1. **capacity:** two 4 GiB guests leave no RAM for the host, and 11 GiB free is below the 35 GiB plan.
2. **route:** use sequential/smaller VMs or the supplied-case tier; storage can be remediated if available. buying hardware is not required.
3. **battery:** refuse use/charging, power down if safe, isolate from heat/combustibles, and invoke the approved battery procedure.
4. **owner:** the named local safety/facilities/vendor/disposal owner decides handling; Service Desk documents and hands off.
5. **recovery:** snapshot is dependent rollback; fresh import proves export independence only from the original registration/folder; independent backup needs tested recovery on a separate protected failure domain.
6. **access:** `none` is accurate and not a failure; no B0 tenant is required.
7. **tasks:** documentation is `L1 perform`; router configuration is `network support` under change authority.
8. **ownership:** Service Desk retains user communication unless policy explicitly transfers it and gives a concrete next-update time.

</details>

### B0-EXIT-B - limited storage and unknown cleaner

ur host has 16 GiB RAM but insufficient free storage. the only exported VM sits on the same physical disk as the original. Packet Tracer account/download is unavailable, a complete supplied `.pkt`/trace form is available, cloud/access tier is `none`, and an unlabelled cleaning fluid sits on the bench.

the supplied local matrix says Service Desk owns bounded telephone-connectivity support and user updates; Network Support owns LAN/WAN performance decisions. classify these supplied B-form paraphrases: `Provide telephone connectivity support for a user.` and `Evaluate LAN/WAN performance data and decide capacity needs.`

commit **8/8** decisions: storage conflict; safe continuation/remediation; Packet Tracer evidence route/claim; export failure-domain limit; chemical action/owner; cloud-tier interpretation; both task owners; and retained owner/next update.

<details>
<summary><strong>B0-EXIT-B truth - open only after the selected-form commitment</strong></summary>

1. **capacity:** RAM is not the current blocker; insufficient storage is. do not start/grow the VM until space and rollback are safe.
2. **route:** free/relocate verified storage or use the supplied-case tier; no purchase is required.
3. **Packet Tracer:** the complete supplied form preserves the network decisions at `simulation-supplied`; it supports no install/live-device/physical claim.
4. **recovery:** a same-disk export can prove a fresh import but shares disk failure with the original, so it is not resilient independent recovery.
5. **chemical:** stop and escalate without using or smelling it; secure the area and route identification/SDS/disposal to the local safety owner.
6. **access:** `none` remains accepted; no cloud tenant is required.
7. **tasks:** bounded telephone support is `L1 perform`; LAN/WAN performance/capacity decision is `network support`.
8. **ownership:** Service Desk records evidence, handoff target, requested action, and the next user-update owner/time.

</details>

**completion gate:** C01 artifacts 8/8, C02 classifications 10/10, C03 triage 11/12 with all mandatory stops, one exit form 8/8, and all explain gates 7/8. when all pass, B1 is unlocked meow

### repair only what failed

| Failed evidence | Required re-entry | Return test |
|---|---|---|
| C01 | B0 C01 only | Rebuild preflight and repeat snapshot/export/restore acceptance with a changed marker. |
| C02 | B0 C02 only | Reclassify ten changed O*NET-derived tasks with ownership and escalation triggers. |
| C03 | B0 C03 only | Repeat twelve changed safety/evidence cases; every mandatory stop present on that form must pass. |
| Explanation below `7/8` or causal chain below `2` | Owning mechanism only | Make one specific repair, then give the changed near-transfer explanation at `A0`. |
| Any critical error | Owning safety, authorization, or redaction boundary | Record the repair, then take the changed full form; the prior numeric score is void. |

### where these skills come back

- before every **destructive, update, and domain lab**, C01 returns as an access/recovery recheck: baseline, rollback, independent recovery, and available access tier
- at **portfolio exit**, C02 returns as a task-to-artifact remap of the same ten tasks; remove the two claims ur artifacts cannot support
- C03 returns as a safety/data/authorization distractor in **printer, laptop, update, remote-support, and capstone** work; stop before technical diagnosis whenever the boundary requires it

---

## optional: how does this connect to certifications?

dw, none of this is required to pass B0. only open it **after** the owning practical and explain gates pass, and only if A+ helps ur situation.

- **A+ Core 1 220-1201 Domain 4:** virtualization is **4.1**. C01 builds its VM/resource/network/snapshot boundary. cloud is **4.2** and is learned later; B0 does not teach those comparison cards.
- **A+ Core 2 220-1202 Domain 2:** the optional F3 cards below translate physical-control names after C03. they do not change the safety learning order.
- **A+ Core 2 220-1202 Domain 4:** C03 supports safety **4.4** and the bounded SDS/environment portion of **4.5**. C02/artifact work begins documentation **4.1**, which is assessed more fully in later operations work.
- **late wording note:** Network+ writes the troubleshooting loop as seven steps. A+ combines planning and implementation into a six-step version. same job mechanism, slightly different exam wording.

### optional F3 - physical-control placement (15/15)

after C03 passes, commit a purpose and local-policy owner for every card. use this supplied local matrix: **Facilities** owns perimeter/structure/lighting; **Physical Security Engineering** owns access hardware; **Security Operations** owns monitoring/response/screening; **IT Asset Custodian** owns device/equipment restraints.

1. bollard at a vehicle approach
2. access vestibule at a restricted entrance
3. badge reader at a staff door
4. video surveillance covering an entry
5. intrusion alarm
6. motion sensor in a restricted room
7. choose among door, equipment, and cable locks for the named asset/boundary
8. security guard at a controlled entrance
9. perimeter fence
10. key fob
11. smart card
12. mobile device used as a key
13. biometric reader
14. perimeter/entry lighting
15. magnetometer at a screened entrance

**gate:** **15/15** cards name the primary deterrence/detection/prevention claim and the supplied local-policy owner. commit before truth.

**changed retry `BR-A2-2.1-PHYS-B`:** use the same four-owner matrix and classify these exact changed placements at A0: loading-bay bollard; data-centre vestibule; lab badge reader; warehouse camera; after-hours door alarm; archive motion sensor; door/equipment/cable locks for a server room, rack, and laptop; lobby guard; yard fence; contractor key fob; employee smart card; phone-based visitor key; fingerprint reader; car-park lighting; event-entry magnetometer. commit all fifteen before opening B truth.

<details>
<summary><strong>F3 A truth - open only after the A-form commitment</strong></summary>

1. bollard - prevention/deterrence; Facilities
2. vestibule - access prevention; Physical Security Engineering
3. badge reader - access prevention/verification; Physical Security Engineering
4. video surveillance - detection/evidence; Security Operations
5. alarm - detection/response trigger; Security Operations
6. motion sensor - detection; Security Operations
7. door lock - boundary prevention / Physical Security Engineering; equipment or cable lock - asset prevention / IT Asset Custodian
8. guard - verification/prevention/response; Security Operations
9. fence - deterrence/prevention; Facilities
10. key fob - access prevention/verification; Physical Security Engineering
11. smart card - access prevention/verification; Physical Security Engineering
12. mobile key - access prevention/verification; Physical Security Engineering
13. biometric - access prevention/verification; Physical Security Engineering
14. lighting - deterrence/detection support; Facilities
15. magnetometer - screening/detection; Security Operations

these are claims under the supplied matrix, not universal ownership titles.

</details>

<details>
<summary><strong>F3 B truth - open only after the changed-form commitment</strong></summary>

1. loading-bay bollard - prevention/deterrence; Facilities
2. data-centre vestibule - access prevention; Physical Security Engineering
3. lab badge reader - access prevention/verification; Physical Security Engineering
4. warehouse camera - detection/evidence; Security Operations
5. after-hours alarm - detection/response trigger; Security Operations
6. archive motion sensor - detection; Security Operations
7. server-room door lock - boundary prevention / Physical Security Engineering; rack/laptop equipment or cable locks - asset prevention / IT Asset Custodian
8. lobby guard - verification/prevention/response; Security Operations
9. yard fence - deterrence/prevention; Facilities
10. contractor key fob - access prevention/verification; Physical Security Engineering
11. employee smart card - access prevention/verification; Physical Security Engineering
12. phone-based visitor key - access prevention/verification; Physical Security Engineering
13. fingerprint reader - access prevention/verification; Physical Security Engineering
14. car-park lighting - deterrence/detection support; Facilities
15. event-entry magnetometer - screening/detection; Security Operations

these remain claims under the supplied B matrix; the site labels do not create universal owner titles.

</details>

### optional dated local-rule lookup

after C03, look up the official authority for **ur actual jurisdiction** and record the URL, page title, jurisdiction, `checked_at_utc`, and the stated battery/electronics/toner route. this is the only A+ 4.4 regulation bridge in B0. it is a dated policy lookup, not a second practical and not permission to treat OSHA/EPA wording as worldwide law.

### optional F4 - SDS + vendor cleaning boundaries (4/4)

commit the action for all four supplied cards:

1. an old procedure asks for an `MSDS`; name the current document u must retrieve
2. Vendor Card A permits compressed air only after power-down, outdoors/in specified ventilation, can upright, with short bursts; choose the compliant action
3. Vendor Card B prohibits an ordinary household vacuum and permits only its named ESD-safe service vacuum; choose the compliant action
4. the product SDS requires ventilation and a named local hazardous-waste route; choose the document, ventilation control, and disposal handoff

**gate:** **4/4**. no generic cleaning habit overrides the supplied vendor card or SDS.

**changed retry `BR-A2-4.5-B`:** (1) a legacy ticket requests an `MSDS`; (2) changed Vendor Card A says `do not use compressed air or any aerosol; disconnect power and use the supplied lint-free tool`; (3) changed Vendor Card B says `after disconnection, use only Model ESD-4 antistatic service vacuum; household vacuums prohibited`; (4) the changed SDS requires local exhaust ventilation and handoff to the named municipal hazardous-household-waste program. commit all four actions at A0 before B truth.

<details>
<summary><strong>F4 A truth - open only after commitment</strong></summary>

1. retrieve the current **SDS (Safety Data Sheet)**; `MSDS` is the legacy label.
2. power down/disconnect as directed, use the stated ventilation, keep the can upright, and use short bursts only because this exact vendor card permits them.
3. do not use the household vacuum; use only the named ESD-safe service vacuum and procedure.
4. use the SDS-specified ventilation and local hazardous-waste/disposal handoff; do not generalize one product's rule.

</details>

<details>
<summary><strong>F4 B truth - open only after the changed commitment</strong></summary>

1. `MSDS` still maps to current `SDS`.
2. disconnect power and use the supplied lint-free tool; compressed air/aerosol is prohibited on this form.
3. after disconnection, use only Model ESD-4; an ordinary vacuum fails.
4. use local exhaust ventilation and the named municipal hazardous-household-waste handoff, record the local owner/date, and make no universal claim.

</details>

the difference is simple: the job mechanism and gates come first; these bounded cards only translate what u already proved into exam wording qwq

**the order stays mechanism → lab → explain → optional checkpoint translation**. ur not studying for the exam - ur learning the actual job, and exam readiness is the side effect meow


---

## next session - what changes after B0?

**retrieval check (first 5 minutes next time u sit down):**

without opening this file, answer these cold prompts from B0:

1. name three things a hypervisor isolates and two limits of that isolation
2. classify "evaluate LAN/WAN performance and recommend changes" under a Help Desk vs Network Support authority matrix
3. **changed safety micro-case:** a desktop UPS (uninterruptible power supply) is beeping and showing a red "replace battery" indicator. The UPS is plugged into mains power and currently supporting two monitors and a desk phone. What is your **classification** (proceed/power-down/stop-escalate), **immediate action**, and **who owns** the battery replacement?

<details>
<summary><strong>retrieval oracle - open only after committing all three answers</strong></summary>

1. a hypervisor separates guest CPU/memory/device state and virtual disks/networks; shared folders, bridged LAN exposure, host resource pressure, and the shared host failure domain limit that boundary.
2. under the supplied B0 matrix, Service Desk gathers/retains communication while Network Support owns the LAN/WAN performance decision.
3. **power down and isolate** - preserve the indicator, shut down the supported devices normally, disconnect the UPS from mains only when that can be done safely, label/secure it, and route battery service to the qualified/vendor owner. Service Desk does not open the UPS. local policy decides whether further electrical authority is required.

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

when both gates are real in ur own tracker, [B1 - Foundations](01-foundations.md) is the next file. if any gate isnt solid, stay here and fix it. B1 will not slow down to reteach snapshot/export/stop-work patterns meow

---

*This block was last verified 2026-07-11. VirtualBox 7.2.12 base package GPLv3; Packet Tracer's free route may require a Cisco account; no M365/Entra/Intune tenant is required for B0.*
