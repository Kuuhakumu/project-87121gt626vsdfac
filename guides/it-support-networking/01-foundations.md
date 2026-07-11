# B1 - endpoint, OS, and local-platform support (~129h)

> **this is where a computer stops being one magic box.**
> u learn where power, firmware, hardware, Windows, Linux, macOS, printers, and remote support can fail... then u prove which layer actually failed before touching it meow

**Time:** ~129h total (~9 weeks at 2 h/day)
[Previous: B0 - Lab, Safety, and Support Evidence](00-prep.md) · [Hub](README.md) · [Next: B2 - Core Support Skills](02-core.md)

---

## where u are rn

B0 gave u a disposable Windows VM, rollback proof, safety stop rules, and the habit of separating **reported**, **observed**, **inferred**, and **changed** facts. keep that evidence habit open beside u. every case here depends on it.

[Shared Foundations](../../start-here/foundations.md) already owns the generic CPU/RAM explanation, shell basics, the URL-to-page chain, Git, and Bandit 0-15. B1 does not make u repeat them. now ur using that floor to answer support questions like `did power ever reach POST?`, `is this storage media or its cable?`, and `is the service running but still unusable?`

if one of those older mechanisms is fuzzy, return to the exact Shared Foundations block. dont restart this whole file. getting routed to one missing dependency is repair, not failure qwq

**how to track this:** copy the todo-tree into ur own notes or fork the repo. the boxes here are display-only. a topic is done only when its numeric gate **and** its 7/8 explain gate pass.

---

## the rules that travel through B1

### explain gate

score every explanation from 0-2 on four things:

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| **states and actors** | start/end state or actors are wrong | some are named but the boundary is fuzzy | correct actors and before/after state |
| **causal chain** | facts are listed with broken causality | main order has one material gap | ordered chain says what changes and why |
| **evidence and terms** | no useful evidence or terms are materially wrong | mostly right but imprecise | correct evidence/terms; observation stays separate from inference |
| **boundary and transfer** | overclaims or cannot handle a changed fact | gives a limit or variant, not both well | gives a real limit and reasons through the near variant |

**Pass:** at least **7/8**, causal chain = **2**, and no topic critical error. answer without this file or an oracle open. drawing is fine; accent, camera use, and polished grammar are not scored.

### aid + oracle rule

- **A0** - docs, `man`/`--help`, and ur own prior notes only; eligible independent evidence
- **A1** - a process hint; guided evidence
- **A2** - a concept/command hint; practice evidence
- **A3** - walkthrough, model query, answer key, or copied solution; worked-example evidence

after 20-30 min of real blocked effort, use the next aid level and label it honestly. repair the miss, then take the named parallel form at A0.

for every case, save ur answer/hypothesis packet with a timestamp, aid label, and commit ID **before** opening the truth oracle. deterministic evidence comes first. inference comes after.

### artifact envelope

every retained artifact needs these fields:

`artifact_id`, `artifact_type`, `case_id`, `cluster_ids`, `created_at_utc`, `updated_at_utc`, `author_role`, `reviewer_role`, `aid_level` plus exact aid, `evidence_tier`, `environment`, `source_refs`, `commit_before_oracle`, `result` with numeric gate and critical-error flag, `redaction_status`, and `integrity` (SHA-256 where meaningful).

use one visible evidence label too:

```text
evidence_tier: live-owned | live-authorized-lab | simulation-supplied | case-analysis
platform: <product/version or supplied case version>
entitlement: <none, license, trial, paid tenant, or hardware>
performed_actions: <what u actually did>
observed_only: <what the case supplied>
claims_supported: <finite claims this proves>
claims_not_supported: <live/physical/admin claims it does not prove>
expires_or_checked_at: <UTC date or not applicable>
```

an evidence-log row records `timestamp_utc`, actor/source, claim class, question/hypothesis, exact command/action and scope, raw result, status/exit code, interpretation, what it proves, what it does **not** prove, next decision, authorization, aid level, evidence tier, and redaction note.

when B1 asks for one of these artifacts, use the exact schema below so the next tech doesnt have to guess what ur notes meant:

- **ticket:** `ticket_id`, `record_type`, `opened_at_utc`, `requester_synthetic_id`, `service_or_asset_id`, `reported_symptom`, `exact_error`, `scope`, `impact`, `urgency`, `priority`, `priority_policy_reference`, `sla_ack_due`, `sla_update_due`, `owner`, `status`, `last_known_good`, `recent_change`, `known_good_comparison`, `workaround`, `safety_security_privacy_screen`, `consent_and_accessibility`, `acceptance_tests`, `next_update`, `linked_records`, `closure_code`, `user_confirmation`, `knowledge_decision`.
- **handoff:** `handoff_id`, `from_role`, `to_role_or_queue`, `transferred_authority`, `retained_owner`, `user_impact`, `current_state`, `timeline`, `observed_evidence`, `inferences_and_uncertainty`, `theories_tested`, `actions_and_results`, `authorization_or_change_id`, `rollback_state`, `requested_action`, `acceptance_criteria`, `risk_or_deadline`, `attachments_and_hashes`, `next_update_owner_and_time`, `user_message_sent`.
- **hypothesis row:** `hypothesis_id`, `ticket_id`, `sequence`, `candidate_cause`, `supporting_observation`, `contradicting_observation`, `prediction_if_true`, `discriminating_test`, `test_scope_and_risk`, `expected_results_by_theory`, `actual_result_reference`, `theory_status`, `revision_reason`, `next_hypothesis_or_action`.
- **rollback execution:** `trigger_observed`, `trigger_time_utc`, `stop_decision`, `before_evidence`, `steps_executed`, `actor_authority`, `config_or_snapshot_restored`, `rollback_result`, `baseline_retest_results`, `remaining_risk`, `stakeholder_update`, `next_owner_and_time`.
- **KB/runbook:** `document_id`, `title`, `purpose`, `audience`, `owner`, `version`, `last_verified_utc`, `applies_to_versions`, `symptoms_or_trigger`, `prerequisites`, `authorization_and_safety`, `inputs`, `expected_normal_state`, `decision_points`, `steps`, `expected_result_per_step`, `stop_and_escalate`, `rollback_or_recovery`, `validation`, `known_limits`, `references`, `linked_problem_or_change`, `review_due`, `revision_history`.

a handoff fails when the receiving role must repeat intake, authority/owner is vague, or the packet contains a secret or unsupported root-cause claim. a hypothesis becomes `confirmed` only when the test **and** post-fix validation support causality. timing alone isnt enough.

for the final packet, rerun one artifact from a clean directory or clean VM snapshot using only its README/notes. verify prerequisites, versions, evidence tier, hashes, exact commands, acceptance tests, negative test, rollback, and redaction scan. label a solo rerun `self-review`; dont call it peer review meow

never retain passwords, MFA/recovery codes, tokens, cookies, private keys, API/client secrets, password hashes, Wi-Fi PSKs, real PII, raw production tickets, or person-linked device identifiers. use synthetic values such as `RITN-USER1`, `corp.example`, and RFC 5737 addresses. screenshots need opaque redaction plus a text transcription of the decisive field.

---

## the path

- [ ] **C04 - power, motherboard, firmware, CPU, and enumeration** (~10h)
- [ ] **C05 - memory, storage, RAID, and thermals** (~12h)
- [ ] **C06 - connectors, displays, docks, and peripherals** (~8h)
- [ ] **C07 - laptop and mobile support** (~8h)
- [ ] **C08 - printer and MFD pipeline** (~7h)
- [ ] **C09 - Windows startup, deployment, drivers, updates, backup, and recovery** (~16h)
- [ ] **C10 - Windows processes, services, logs, and registry** (~10h)
- [ ] **C11 - Windows filesystems, access, apps, and security boundary** (~12h)
- [ ] **C14 - remote support, consent, privacy, and accessibility** (~8h)
- [ ] **C32 Stage 1 - guided ticket and printer handoff** (~6h)
- [ ] **C12 - Ubuntu service, package, permission, and log support delta** (~12h)
- [ ] **C13 - architecture-aware macOS support** (~7h)
- [ ] **C15 - virtualization, cloud, VDI, and containers** (~13h)
- [ ] ✅ **B1 exit** - one unlabeled endpoint case, 8/8 plus 7/8

**Arithmetic:** technical core `10+12+8+8+7+16+10+12+12+7+13 = 115h`; operations insertion `8+6 = 14h`; file total `115+14 = 129h`.

---

## C04 · power, motherboard, firmware, CPU, and enumeration (~10h)

**the idea** - `dead`, `powers on but no POST`, `no boot device`, and `unknown device` look related from the outside. inside, they stop at four different layers.

**how/why it actually works** - pressing the case button asks the motherboard to assert the PSU control line. the **PSU** raises its main rails and sends **power-good** only when theyre stable. then CPU reset releases and **UEFI** starts from firmware flash.

UEFI initializes the CPU, trains RAM, configures the chipset, discovers boot-critical devices, runs **POST**, and chooses a boot entry. Windows continues **enumeration** across PCIe, USB, ACPI, and other buses, reads a hardware ID, creates a device node, then binds a matching driver. so an OS driver can help an unknown device that already enumerated. it cant rescue hardware that firmware never sees.

the support version of CPU knowledge is the whole platform chain. CPU socket/chipset/firmware, RAM generation, PCIe lanes, storage protocol/keying, PSU connectors/wattage, GPU/display path, chassis form factor, and cooling all have to agree. a part can fit and still fail electrically or logically.

a surge protector clamps some brief transients. a **UPS** supplies energy during an outage, with standby, line-interactive, or online power paths. VA, W, topology, transfer behavior, load, battery condition, and runtime all matter. UPS internals are mains equipment; B0's stop-work boundary still applies.

dw, u dont need to memorize every board trace. follow the state change until the evidence stops meow

**words u gotta be able to say:**

- **standby rail / power-good** - pre-start power and stable-rail signal
- **POST / UEFI** - firmware initialization and modern firmware interface
- **chipset / PCH** - controller for many lower-speed I/O paths
- **PCIe lane / root complex** - high-speed link and its CPU/chipset origin
- **ACPI** - firmware tables/methods exposed to the OS
- **enumeration / hardware ID** - device discovery and identity
- **driver binding** - matching a driver package to a device node
- **socket / form factor** - electrical CPU interface / board-chassis size
- **UPS topology / VA / W** - power path and two load limits

**study sources (pick one route):**

- **recommended:** [Cisco Networking Academy - Computer Hardware Basics](https://www.netacad.com/courses/computer-hardware-basics) → the case board below. **free with account**, verified 2026-07-11. use it for platform orientation, not as the gate.
- **rather watch:** [Crash Course Computer Science #7 - The Central Processing Unit](https://www.youtube.com/watch?v=FZGugFqdr60). **free**, exact episode. use this if the execution path still feels floaty.
- **rather read/reference:** [Microsoft - Introduction to Plug and Play](https://learn.microsoft.com/en-us/windows-hardware/drivers/kernel/introduction-to-plug-and-play). **free**, exact enumeration/resource/driver mechanism.

**do this - `C04-PLATFORM-A`:** diagnose these five supplied evidence cards. for each, commit the last known-good layer, next safe observation, one discriminating test, and one action that would destroy evidence or add risk.

| Card | Evidence |
|---|---|
| A | no standby indication |
| B | fans run; memory POST code appeared after a DIMM change |
| C | normal POST; boot target missing |
| D | Windows boots; USB controller is unknown |
| E | workstation reboots during a brief outage; UPS reports overload |

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

the chain is `AC/adapter -> standby/control -> stable rails -> CPU reset -> UEFI/POST -> boot entry -> OS enumeration -> driver binding`.

- A stops before firmware. prove source/adapter/standby before board replacement.
- B reaches powered POST and points first to the changed DIMM/slot/training path. use the exact vendor code.
- C passed the core platform checks; inspect detected storage, boot order, and boot entry.
- D enumerated enough to create a node; use hardware ID and the OEM/system driver source.
- E needs UPS topology, load, self-test/runtime, and transfer evidence before any battery decision.

</details>

**measurable gate:** **5/5** cards identify the first failed layer and next observation. `replace motherboard` before power/POST evidence or `replace UPS battery` before load/topology evidence fails.

**changed retry:** `C04-PLATFORM-B` changes the POST code/component and UPS load. keep the same chain; do not reuse the surface answer.

**critical errors:** opening/probing a PSU or UPS; replacing the board before power/POST evidence; claiming an OS driver fixes a firmware-absent device; replacing a UPS battery before load/topology/self-test evidence.

**can u explain it?** ✅ - score 7/8. narrate the full power-to-driver chain and place all five cards at their stopping point. near variant: the device is absent in firmware instead of unknown in Windows. say what evidence and next action must change.

**revisit:** next session, draw the chain cold. in 48-72h, use `C04-PLATFORM-B`. C09 will hide this mechanism inside a no-boot ticket.

---

## C05 · memory, storage, RAID, and thermals (~12h)

**the idea** - `slow computer` is a report. memory pressure, bad RAM, storage retries, path errors, and thermal throttling are competing causes.

**how/why it actually works** - CPU caches keep hot data near execution, **RAM** holds active code/data, and persistent storage holds inactive state. Windows/Linux can page nonresident memory, but high commit + low available RAM + sustained paging together mean capacity pressure. random crashes across unrelated workloads point more toward corruption than capacity.

HDDs pay seek/rotation cost. SSDs write NAND pages, erase larger blocks, and use a controller plus **FTL** for logical mapping, garbage collection, bad-block replacement, and wear levelling. SATA/AHCI and PCIe/NVMe are different paths; `M.2` only describes form factor/keying. a growing SATA CRC count can be cable/path trouble while the media stays healthy.

**RAID** changes availability. RAID 0 stripes without redundancy; RAID 1 mirrors; RAID 5/6 use distributed parity; RAID 10 stripes mirrored pairs. a degraded array has already spent its fault tolerance, and rebuild stresses every surviving member. preserve backup, controller metadata, slot/serial order, and foreign-config state before touching it. RAID does not protect against deletion, ransomware, theft, controller failure, or a bad operator.

heat moves from silicon through interface material and a heatsink into airflow. when sensors reach limits, CPU/GPU clocks drop. thats **thermal throttling**. rising temperature plus falling clock under the same load is a causal trail; `95 C` alone is only one observation.

the numbers look dramatic sometimes. keep them as evidence, not a story, and this gets way less scary qwq

**words u gotta be able to say:**

- **working set / commit / paging** - resident pages / promised backing / page movement
- **DIMM/SODIMM / channel / ECC** - module types, memory path, error correction
- **AHCI / NVMe / M.2** - SATA interface, PCIe storage protocol, form factor
- **NAND / FTL / TRIM / SMART** - flash cells, mapping, discard hint, telemetry
- **stripe / mirror / parity** - RAID data layouts
- **degraded / rebuild / foreign configuration** - lost redundancy, reconstruction, discovered metadata
- **thermal throttling / TDP** - reduced clock at limits / cooling design target

**study sources (pick one route):**

- **recommended sequence:** [Memory](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/an-overview-of-memory-220-1201/), [Storage Devices](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/storage-devices-220-1201/), [RAID](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/raid-220-1201/), and [Cooling](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/cooling-220-1201/). **free**, exact current episodes. watch the section ur evidence needs; dont binge all four before attempting.
- **rather watch NAND deeply:** [Branch Education - How do SSDs Work?](https://www.youtube.com/watch?v=5Mh3o886qpg). **free**.
- **rather read/reference:** [Debian `smartctl(8)` manual](https://manpages.debian.org/bookworm/smartmontools/smartctl.8.en.html). **free**; use it to interpret fields, not to pretend one green status guarantees health.

**do this - `C05-RESOURCE-A`:** record safe idle/load/after CPU, memory commit/available, storage active time/latency, health, and temperature/frequency if ur system exposes them. a supplied telemetry packet is the no-hardware fallback. then classify:

1. paging pressure with a clean memory test
2. SATA CRC growth with healthy media attributes
3. rising temperature plus falling clock
4. RAID 5 degraded after one positively identified member failure
5. multiple members missing immediately after controller/cabling work

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

1 is capacity pressure, not proven corruption. 2 isolates the transport path before condemning media. 3 is a thermal chain and needs a vendor-limit stop condition. 4 requires backup + metadata/slot preservation before a vendor-approved rebuild. 5 is stop-and-preserve; restoring path/order and inspecting foreign metadata comes before initialize/import/rebuild.

</details>

**measurable gate:** before/load/after table plus **5/5** cases. backup/path isolation, a thermal stop condition, and RAID metadata preservation are mandatory.

**changed retry:** `C05-RESOURCE-B` changes capacity, interface, sensor pattern, RAID level, and member order.

**critical errors:** calling `100% disk`, `95% RAM`, or one temperature a root cause; calling RAID backup; blind initialize/import/rebuild; destructive disk or thermal stress; write-heavy testing before recovery evidence.

**can u explain it?** ✅ - score 7/8. separate capacity from corruption, media from path, and degraded from failed. then trace temperature rise -> control limit -> lower frequency -> slower workload. near variant: SMART is healthy but CRC errors rise only when one cable is used.

**revisit:** next session, answer `why can a healthy SSD still have a broken storage path?` in 48-72h, take B. C15 brings memory pressure back as VM overcommit.

---

## C06 · connectors, displays, docks, and peripherals (~8h)

**the idea** - connector shape tells u what fits. capability tells u what will actually work.

**how/why it actually works** - **USB-C** may carry USB data, USB Power Delivery, DisplayPort Alt Mode, USB4/Thunderbolt, or only some of them. CC pins detect attachment and roles. USB PD negotiates voltage/current. Alt Mode repurposes lanes for display, while USB4/Thunderbolt can tunnel DisplayPort and PCIe. host port, dock, charger, cable/e-marker, and device all need the requested mode.

USB data then enumerates separately: detect -> reset -> assign address -> read descriptors -> choose config -> bind class/device driver. so a phone can charge with no data, or enumerate while charging too slowly.

for displays, the GPU builds the image and the display engine sends a timed stream. the source reads **EDID** for supported resolution/refresh/color, then trains the HDMI or DisplayPort link. a dock shares finite lanes across display, storage, RJ45 Ethernet, and USB. one high-resolution display failing can be bandwidth or mode support, not a dead GPU.

RJ45 Ethernet still needs physical link/autonegotiation before IP matters. SATA data and power are separate. M.2 fit does not guarantee SATA/NVMe compatibility. never force a connector or improvise voltage/polarity bc it looks right.

same-shaped connectors being different is annoying... the matrix below makes it honest meow

**words u gotta be able to say:**

- **CC pin / USB PD** - role detection and power negotiation
- **Alt Mode / e-marker** - alternate protocol and cable capability chip
- **USB4/Thunderbolt tunnelling** - PCIe/DisplayPort carried through the link
- **descriptor / class driver** - USB capability data / standard driver
- **EDID / link training / MST** - display capability, negotiated link, multiple streams
- **autonegotiation / RJ45** - Ethernet link agreement / common 8P8C connector
- **HDMI / DisplayPort** - digital display interfaces

**study sources (pick one route):**

- **recommended:** capability mechanism above → [Microsoft - USB Type-C troubleshooting notifications](https://learn.microsoft.com/en-us/windows-hardware/drivers/usbcon/usb-type-c-troubleshooting-notifications) → matrix below. **free**.
- **rather watch:** [Professor Messer - Peripheral Cables](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/peripheral-cables-220-1201/) plus [Video Cables](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/video-cables-220-1201/). **free**, exact episodes; use only the one matching ur weak path.
- **rather read power detail:** [USB-IF - USB Power Delivery](https://www.usb.org/usb-charger-pd). **free**.

**do this - `C06-PATH-A`:** inventory one host, dock/hub, display, charger, and three USB-C cables. record supported data rate, display modes, and power. if unavailable, use supplied vendor spec cards and label `simulation-supplied`. solve charge/no-data, weak charging, one missing high-resolution display, and a webcam that enumerates but one app cannot use.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

classify the first break as power negotiation, data enumeration, display capability/link, or application permission/input. reduce to one direct device and one verified full-featured cable, then add the dock/adapter path back. an absent Ethernet link light stays below IP and driver/application guesses.

</details>

**measurable gate:** capability matrix has no shape-based assumption and **4/4** cases use the smallest discriminating swap/observation sequence.

**changed retry:** `C06-PATH-B` changes USB-C/Thunderbolt capabilities, display mode, cable, and app.

**critical errors:** claiming USB-C shape guarantees video/data/wattage; reinstalling drivers first when no physical link exists; inventing vendor capability; using damaged cables or unknown power adapters.

**can u explain it?** ✅ - score 7/8. trace CC/PD, data enumeration, EDID/link, and app permission. near variant: the dock works with a 40 Gbps full-featured cable but not a USB 2 + 60 W charge cable.

**revisit:** next session, state why `charging` proves almost nothing about video. 48-72h later, take B.

---

## C07 · laptop and mobile support (~8h)

**the idea** - portable devices squeeze the same layers into smaller assemblies, then add battery safety, radios, warranty, and policy boundaries.

**how/why it actually works** - a **FRU** is a part the manufacturer authorizes a field technician to replace under a model-specific service procedure. SSDs, SODIMMs, Wi-Fi cards, batteries, displays, cameras, and keyboards may be FRUs... or soldered/paired parts outside ur boundary. the current service manual and warranty decide, not a generic teardown.

a lithium battery pack has cells, temperature sensing, protection, a charge controller, and a **BMS/fuel gauge**. adapter + cable + USB PD negotiate input, then the controller decides system power and charge behavior. `plugged in` does not prove adequate wattage or a healthy pack. swelling is still a mandatory stop.

an internal display commonly uses eDP through a hinge cable with separate panel/backlight power. angle-dependent flicker points toward cable/hinge; a faint flashlight-visible image points toward backlight/power. docks reuse C06's shared power/data/display path.

mobile connectivity goes `radio -> association or cellular attach -> IP/gateway/DNS -> account/session -> app permission/cache -> MDM policy`. paired Bluetooth can still use the wrong profile/output. browser working while mail sync fails pushes the first failed layer upward toward account/app/policy.

dw, u only need the first failed stage. dont reset the whole phone bc the last app in the chain got grumpy

**words u gotta be able to say:**

- **FRU / service manual** - authorized replaceable part / model procedure
- **BMS / fuel gauge / cycle count** - battery protection, estimate, accumulated use
- **eDP / digitizer** - internal display link / touch layer
- **SIM/eSIM / hotspot** - carrier identity / shared mobile data
- **Bluetooth pairing / profile** - trusted keys / supported device function
- **sync / MDM handoff** - local-remote state reconciliation / policy-owner evidence

**study sources (pick one route):**

- **recommended:** [Professor Messer - Troubleshooting Mobile Devices](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/troubleshooting-mobile-devices-220-1201/) → six tickets below. **free**, exact episode.
- **rather watch the part boundary:** [Professor Messer - Laptop Hardware](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/laptop-hardware-220-1201/). **free**, exact episode.
- **rather read/reference:** the exact official service manual for the chosen model. record its deep URL, model, and revision in ur artifact; it varies by device and controls the real replace/escalate boundary.
- **safety reference:** [iFixit - What to do with a swollen battery](https://www.ifixit.com/Wiki/What_to_do_with_a_swollen_battery). **free**.

**do this - `C07-MOBILE-A`:** using the manual boundary, decide evidence, safe first test, and escalation owner for battery not charging, a swollen pack, hinge-angle flicker, undetected SSD, one dock display missing, and a paired-but-silent Bluetooth headset. no disassembly is required. a supplied manual/spec packet is valid `case-analysis`, not physical repair evidence.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

not charging starts with adapter/PD/cable/direct-port and battery-health evidence. swelling stops charging/use immediately. hinge flicker compares external display and lid angle without twisting the panel. missing SSD starts at firmware detection and slot/protocol/manual boundary. dock display compares direct-host and known-good dock paths. headset checks profile, app input/output, and permission before re-pairing.

</details>

**measurable gate:** **6/6** valid first tests; swelling stops immediately; display/dock separates direct paths; audio checks profile/input/output before re-pair.

**changed retry:** `C07-MOBILE-B` changes laptop manual, display symptom, dock port, and Bluetooth role.

**critical errors:** disassembly outside manual/warranty; charging or pressing a swollen battery; claiming a local reset overrides MDM; assuming adequate charge from plug state; calling case evidence hands-on replacement.

**can u explain it?** ✅ - score 7/8. trace charger negotiation -> charge controller/BMS -> system/battery, then dock -> displays/peripheral. near variant: general web works but only managed mail sync fails.

**revisit:** next session, explain `FRU` without naming a universal part list. in 48-72h, take B.

---

## C08 · printer and MFD pipeline (~7h)

**the idea** - a print job crosses software, queue, network, controller, and physical imaging. `printer broken` doesnt tell u which one.

**how/why it actually works** - an app sends a request through the OS print API. a driver produces a spool representation, the **spooler** stores/schedules it, a print processor converts it if needed, and a **port monitor** sends printer-ready data to the destination. the queue is logical; a healthy printer can sit behind a broken client queue.

network print may use IPP/IPPS, TCP 9100, LPR/LPD, SMB, or vendor protocols. DNS, reachability, firewall, certificate trust, and printer storage can fail separately.

inside a laser printer, the controller rasterizes the page, then the engine charges the drum, exposes the image, develops toner, transfers it, fuses with heat/pressure, and cleans/erases. repeating defects suggest a rotating component. toner rubbing off points toward fusing/media. a bad local self-test bypasses the client and network, so stay at the device/imaging layer.

follow the paper and data paths separately... they meet pretty late meow

**words u gotta be able to say:**

- **spooler / spool file / queue** - scheduling service, intermediate data, pending jobs
- **driver / print processor / port monitor** - render, convert, send
- **IPP/IPPS / PCL / PostScript** - print protocol and page-description languages
- **RIP / drum / fuser** - rasterizer, image carrier, heat-pressure bond
- **duplexer / ADF / maintenance kit** - two-sided path, document feeder, wear parts

**study sources (pick one route):**

- **recommended:** [Microsoft - Print Spooler Architecture](https://learn.microsoft.com/en-us/windows-hardware/drivers/print/print-spooler-architecture) → guided + constrained faults. **free**.
- **rather watch:** [Professor Messer - Troubleshooting Printers](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/troubleshooting-printers-220-1201/). **free**, exact episode.
- **rather read IPP:** [OpenPrinting CUPS - Implementation of IPP](https://openprinting.github.io/cups/doc/spec-ipp.html). **free**.

**do this - `C08-PRINT-A`:** in a disposable Windows VM, use `Microsoft Print to PDF` plus a second test queue if available. inject a paused queue, stopped Print Spooler, and wrong/unreachable destination. capture queue state, service state, destination, lowest proven layer, and final job. if a configurable port is unavailable, use a wrong queue/driver selection and prove the physical device was never reached.

no Windows VM rn? use the supplied `C08-PRINT-A` queue/service/destination captures, commit ur predicted layer and next state, then compare against the same oracle. label it `simulation-supplied`; it does not prove live queue administration.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

the chain is `application -> render/spool -> queue -> port/protocol -> controller -> imaging`. a paused queue stops at scheduling; a stopped spooler stops before jobs are processed; a wrong destination reaches the logical queue but sends nowhere useful. clear or change only the supported layer. dont delete every printer.

</details>

**measurable gate:** resolve **3/3** faults with queue, service, destination, and successful final job evidence. no delete-all/reinstall/reboot first action.

**changed retry:** `C08-PRINT-B` uses wrong queue, valid service plus DNS/port failure, and a supplied imaging defect.

**critical errors:** blaming a bad device self-test on the client driver; broad rebuild as first action; unsafe fuser access; calling a reboot diagnosis.

**can u explain it?** ✅ - score 7/8. place a stuck job, DNS/port error, and unfused toner at different layers. near variant: the self-test is good but only one client's Windows test page fails.

**revisit:** next session, draw the pipeline cold. Stage 1 later turns the stopped service into a full user-facing ticket; thats a separate operations artifact, not a duplicate gate.

---

## C09 · Windows startup, deployment, drivers, updates, backup, and recovery (~16h)

**the idea** - recovery gets safer once u name the last startup phase that worked. `firmware sees no drive`, `BCD is broken`, `Safe Mode works`, and `a file was deleted` need different tools.

**how/why it actually works** - on a normal UEFI Windows system, firmware launches `bootmgfw.efi` from the **EFI System Partition**. Windows Boot Manager reads the **BCD**, then `winload.efi` loads the kernel, HAL, SYSTEM hive, and boot-start drivers. the kernel initializes hardware and core subsystems; Session Manager and the Service Control Manager bring up services and sign-in.

**Safe Mode** loads a reduced driver/service set, so it localizes a fault without fixing it by itself. **WinRE** is a separate recovery environment with Startup Repair, update uninstall, System Restore, Command Prompt, image recovery, and reset/reinstall routes. BitLocker may require the real recovery key before offline access. never bypass that boundary.

a clean UEFI install creates GPT/ESP and OS/recovery state, applies the image, stages drivers, then reaches OOBE. an in-place upgrade tries to keep apps/data/settings. a clean install removes inherited state but demands tested recovery of data, apps, licenses, and drivers.

PnP matches hardware IDs to signed packages in the Driver Store. Windows Update scans applicability, downloads, stages, installs, then commits across restart. drivers, quality updates, feature updates, and Defender definitions have different rollback paths. test rings reduce blast radius.

System Restore protects selected system state. a file backup protects data. an image protects a larger recoverable system state. a VM snapshot gives quick local rollback but shares its host failure domain. **RPO** is the tolerated data-loss window; **RTO** is the restore-time target. a backup only becomes useful evidence when a restore passes.

recovery menus look intimidating bc there are many buttons. naming the failed phase cuts most of them out qwq

**words u gotta be able to say:**

- **ESP / BCD / Boot Manager / OS loader** - firmware partition, boot database, selector, loader
- **boot-start driver / Safe Mode / WinRE** - early driver, reduced startup, recovery environment
- **GPT / OOBE** - modern partition table / first-run setup
- **Driver Store / INF / catalog** - staged packages, match rules, signature metadata
- **quality update / feature update / test ring** - servicing, version upgrade, limited rollout
- **restore point / image / file backup** - three different recovery scopes
- **BitLocker recovery key** - secret that unlocks protected offline data
- **RPO / RTO / retention** - tolerated loss, restore time, kept versions

**study sources (pick one route):**

- **recommended:** [Microsoft - Windows startup issues troubleshooting](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/windows-boot-issues-troubleshooting) → disposable recovery run. **free**, exact PreBoot/Boot Manager/OS Loader/Kernel phase guide.
- **rather watch:** [Professor Messer - Troubleshooting Windows](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/troubleshooting-windows-220-1202/). **free**, exact episode.
- **rather read/reference:** [Microsoft - Windows Recovery Environment](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference). **free**.

**do this - `C09-RECOVERY-A`:** use ur snapshotted Windows VM, never a daily-use device. record firmware mode and partition map, list BCD, enter Safe Mode and WinRE, record one device's driver/provider/version, install one harmless app or reversible update, prove system rollback, then delete and restore a synthetic test file from a **separate backup location**. do not delete BCD entries or partitions.

if ur host cannot run the VM, use the supplied firmware/partition/BCD/Safe Mode/WinRE/driver/rollback/file-restore cards and label the packet `simulation-supplied`. it proves recovery decisions, not live deployment or restore work.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

the eight accepted artifacts are firmware mode, partition layout, BCD listing, Safe Mode evidence, WinRE evidence, driver identity, successful system rollback, and successful deleted-file restore. record backup timestamp and observed restore duration, then calculate the test's achieved RPO/RTO. System Restore and the VM snapshot do not count as the separate file backup.

</details>

**measurable gate:** **8/8** artifacts; both system rollback and file restore work; backup time and observed RPO/RTO are recorded.

**changed retry:** `C09-RECOVERY-B` injects a failed startup item instead of the harmless app. choose repair/rollback from the first failed phase.

**critical errors:** deleting BCD/partitions for practice; using a live daily device without tested recovery; calling System Restore or a snapshot file backup; random driver-download sites; reset/reinstall before securing data and recovery keys.

**can u explain it?** ✅ - score 7/8. trace firmware -> Boot Manager/BCD -> loader -> kernel/drivers -> services/sign-in. then say why four supplied symptoms need four tools. near variant: firmware sees the disk, but Boot Manager reports missing BCD.

**revisit:** next session, label the startup chain without notes. in 48-72h, take B. C15 will test the snapshot/backup boundary again.

---

## C10 · Windows processes, services, logs, and registry (~10h)

**the idea** - Task Manager, Event Viewer, Services, and Registry Editor show state. none of them turns one red value into a diagnosis.

**how/why it actually works** - a **process** owns a virtual address space, handles, security token, and threads. threads are what the scheduler runs on logical CPUs. page tables map virtual addresses to RAM or nonresident backing. a process **working set** is resident RAM; Windows **commit** is memory promised backing by RAM/pagefile. pagefile use alone does not prove pressure.

the **Service Control Manager** stores service binary, startup type, account, dependencies, security, state, and recovery behavior. `Running` only proves SCM state. the listener, dependency, credential, config, or application request can still be broken.

event providers write structured time/provider/ID/level/data records. correlate the exact symptom time, provider, repeated pattern, and nearby events. a red icon from last week is not the cause of todays failure.

the **registry** stores machine and per-user configuration as hives, keys, and values. `HKLM` is system-wide; `HKCU` belongs to the current profile. safe support queries and exports the smallest relevant branch, changes one documented test value in a disposable VM, then restores and validates it. broad cleaners destroy signal.

no registry heroics needed. one tiny branch, one reversible change, one check meow

**words u gotta be able to say:**

- **process / thread / PID / handle** - container, schedulable path, ID, object reference
- **user mode / kernel mode / context switch** - privilege boundary and thread-state swap
- **virtual address / working set / commit / pagefile** - mapped address, resident set, promised backing, disk backing
- **SCM / service account / dependency** - service database, identity, prerequisite
- **provider / event ID / channel** - event source, kind, log destination
- **hive / key / value / HKLM / HKCU** - registry file/tree/item and scopes

**study sources (pick one route):**

- **recommended:** [About Processes and Threads](https://learn.microsoft.com/en-us/windows/win32/procthread/about-processes-and-threads), [About Services](https://learn.microsoft.com/en-us/windows/win32/services/about-services), [Event Logging](https://learn.microsoft.com/en-us/windows/win32/eventlog/event-logging), and [Registry Hives](https://learn.microsoft.com/en-us/windows/win32/sysinfo/registry-hives) → reversible lab. **free**. open only the reference matching each subtest.
- **rather watch:** [Professor Messer - Task Manager](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/task-manager-220-1202/). **free**.
- **rather inspect deeply:** [Microsoft Sysinternals - Process Explorer](https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer). **free**.

**do this - `C10-STATE-A`:** in ur Windows VM, stop Print Spooler, attempt a print, capture service state plus the time-correlated event, restore service, and verify printing. create `HKCU\Software\RITN5Lab`, export the branch, change/delete the test value, restore it, and verify. compare one process identity in Task Manager and Process Explorer without terminating it.

the no-VM route uses the supplied service/event, HKCU export/restore, and matched-process captures. predict each next state before reveal and label it `simulation-supplied`; dont claim live registry/service work.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

the packet needs service before/after, failed action, provider/event ID/time, repair and successful job; registry before/export/change/restore; and the same PID/process identity in both tools. `running`, `red`, and `pagefile used` remain observations until the missing dependency/time/resource evidence supports a chain.

</details>

**measurable gate:** **3/3** reversible subtests with the exact timeline/evidence above.

**changed retry:** `C10-STATE-B` uses Windows Audio, a different HKCU leaf, and another process.

**critical errors:** calling one event, service state, or pagefile use the cause; changing HKLM/product keys; terminating a process without need; broad registry cleanup; losing the rollback export.

**can u explain it?** ✅ - score 7/8. for `service is running`, `event is red`, and `pagefile is used`, name the extra evidence needed before a causal claim. near variant: service runs and listens locally, but the app request still fails.

**revisit:** next session, explain process vs thread and working set vs commit. 48-72h later, take B. Stage 1 turns service evidence into a full ticket.

---

## C11 · Windows filesystems, access, apps, and security boundary (~12h)

**the idea** - access problems sit between identity, token, ACL, app context, and security policy. permanent admin or `Everyone: Full Control` hides the fault and creates another one.

**how/why it actually works** - NTFS records files/directories in the **MFT** and allocates clusters. its transaction log helps recover metadata consistency after interruption; it is not a user-data backup.

at sign-in, Windows builds an **access token** containing the user's SID, group SIDs, privileges, and integrity state. an object's security descriptor holds a **DACL** made of ordered **ACEs**. Windows compares the requested operation with token + explicit/inherited entries + ownership (and share permissions on a network path) to calculate **effective access**.

**UAC** gives an admin a filtered standard token for normal work and prompts before a process gets the full admin token. the prompt can mean elevation is required; it does not prove the user lacks all access. if an app works only elevated, find the exact file, registry, dependency, profile, license, or service it cannot reach.

an install crosses package type, CPU architecture, per-user/per-machine scope, files, services, drivers, registry, dependencies, profile/cache, and licensing. installation success does not guarantee launch success.

suspected malware crosses a support boundary. preserve the alert/timeline, isolate through approved policy, avoid entering privileged credentials, use approved protection, and escalate possible persistence, credential theft, lateral movement, regulated data, or legal impact. deleting one file is not eradication. certificate warnings also stay evidence; never click through or disable TLS to make a ticket disappear.

dw, stopping with clean evidence is good support. u dont have to become incident response inside one ticket

**words u gotta be able to say:**

- **MFT / cluster / transaction log** - NTFS records, allocation unit, metadata journal
- **SID / access token** - security identity and process/user identity set
- **security descriptor / DACL / ACE** - object security metadata, list, one entry
- **inheritance / effective access** - parent propagation / calculated rights
- **UAC / elevation** - controlled full-admin token use
- **MSI / MSIX / per-user / per-machine** - package formats and install scope
- **BitLocker / quarantine / containment** - volume protection, isolation, spread control

**study sources (pick one route):**

- **recommended:** [Microsoft - NTFS overview](https://learn.microsoft.com/en-us/windows-server/storage/file-server/ntfs-overview), [Access Control Lists](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists), and [How User Account Control works](https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/how-it-works) → least-privilege challenge. **free**.
- **rather watch security boundary:** [Professor Messer - Removing Malware](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/removing-malware-220-1202/). **free**, exact episode; local policy still wins.
- **rather read filesystem orientation:** [Professor Messer - File Systems](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/file-systems-220-1202/). **free** transcript/reference.

**do this - `C11-ACCESS-A`:** in a Windows VM, create local users `RITN5-Alice`, `RITN5-Bob`, group `RITN5-Readers`, and an inherited test folder. Alice reads through the group but cannot modify; Bob has no access. inject one wrong explicit ACE, diagnose with `whoami`, `icacls`, and Effective Access, remove only the bad ACE, then prove a per-user test app runs without permanent admin.

if a Windows VM is unavailable, the supplied token/group/ACL/app captures carry the same six checks. record `simulation-supplied` and keep `live ACL repair` under claims not supported.

then classify three supplied security cards:

1. an approved Defender test alert
2. a hostname-mismatch certificate warning
3. a credential-phishing report

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

ACL/app truth is token -> SID/group -> DACL/ACE -> effective access. keep intended inheritance, remove only the injected ACE, and fix the app's real scope/dependency.

security truth: the Defender alert is contained/preserved and handled under local malware policy, not `delete one file`; the hostname mismatch is not repaired by cache clearing or TLS bypass; phishing needs session/credential containment and security escalation without asking the user for a secret.

</details>

**measurable gate:** ACL/app **6/6** (Alice read-not-modify, Bob denied, inheritance retained, no `Everyone: Full Control`, bad ACE removed, app runs standard-user) plus security **3/3**.

**changed retry:** `C11-ACCESS-B` changes names, group nesting, ACE source, app context, and security indicators.

**critical errors:** broad ACL or permanent elevation; taking ownership/resetting inheritance first; live malware; deleting one file as eradication; bypassing a certificate warning; requesting a user's password/MFA/recovery code.

**can u explain it?** ✅ - score 7/8. narrate token -> SID/group -> DACL/ACE -> effective access, then explain why UAC is not proof of missing permission. near variant: local NTFS access works but an SMB share path denies the same user.

**revisit:** next session, explain explicit vs inherited entries. in 48-72h, take B. C14 now tests whether u can repair a user-facing issue without crossing consent/privacy boundaries.

---

## C14 · remote support, consent, privacy, and accessibility (~8h)

**the idea** - remote control changes the privacy boundary before it changes the computer. a technically correct fix still fails if identity, consent, secrets, or accessibility were mishandled.

**how/why it actually works** - verify the request and both identities through the approved channel first. then name the tool, purpose, expected duration, visible scope, and whether the session is logged. screen **viewing** needs explicit consent. control needs a second explicit approval when the tool separates them.

keep the session at least privilege and least visibility. narrate what ur doing. ask before opening files, mail, chats, credential stores, camera/mic, or any sensitive area. the user enters passwords, MFA, and recovery secrets privately. consent can be withdrawn at any time.

accessibility changes the channel and pace, not the technical standard. ask what works: chat, captions, keyboard-only steps, larger text, more time, or another approved accommodation. give one short instruction with its expected result, then use teach-back or visible output to check it.

close visibly. remove temporary access, validate the original journey, get user confirmation, and record who connected, why, when, what changed, and what ended the session. a solo transcript proves decision-making only. it is never a live remote-session claim.

the user should never wonder if ur still watching their screen afterward... thats the boundary meow

**words u gotta be able to say:**

- **verified interaction** - support request and identities checked independently
- **view consent / control consent** - separate explicit approvals
- **least visibility / least privilege** - only the access the task needs
- **attended / unattended access** - user-present session / persistent remote access
- **authenticator / recovery code** - user-held secret, never ticket evidence
- **accessible channel / teach-back** - usable format and result confirmation
- **session audit / visible disconnect** - who/why/when/action record and clear ending

**study sources (pick one route):**

- **recommended:** [Microsoft - Use Quick Assist to help users](https://learn.microsoft.com/en-us/windows/client-management/client-tools/quick-assist) → the role-play below. **free**, exact official procedure.
- **rather watch:** [Professor Messer - Remote Access](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/remote-access-220-1202/). **free**, exact episode.
- **rather read secret boundary:** [NIST SP 800-63B-4](https://pages.nist.gov/800-63-4/sp800-63b.html). **free**; use it for authenticator/recovery-secret handling.

**do this - `C14-REMOTE-A · Accessible Quick Assist printer correction`:**

> `RITN-USER1` reports that PDF jobs open a retired test queue instead of `Microsoft Print to PDF`. the user uses keyboard navigation and 175% text scaling. resolve it through an authorized Quick Assist test session or the supplied solo transcript. verify identity through the lab procedure, explain each boundary, ask before viewing and again before control, keep the user in control of credential prompts, preserve accessibility settings, and disconnect cleanly. never request a password, MFA code, recovery code, or private-file access.

**evidence cards:** intended queue is `Microsoft Print to PDF`; current default is `RITN-Retired`; spooler is running; intended queue succeeds when selected; no driver/service fault exists. lab policy permits attended Quick Assist but forbids unattended access, secret clipboard use, and technician credential entry as the user. the user requests text status, not a phone call.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

acceptance is **8/8**: identity procedure recorded; view consent; control consent; privacy screen; accessibility preference preserved; smallest change sets the intended default; original app plus second-app print tests pass; session ends and user confirms the PDF opens.

required messages are acknowledgement, pre-control explanation, status, and closure. a solo transcript is `simulation-supplied`; its `claims_not_supported` must say no live Quick Assist session was performed.

</details>

**measurable gate:** remote matrix **8/8**. first role rotation may use A1; scored run is A0. also score operations **12/16** with every dimension at least 3.

**changed retry:** `C14-REMOTE-B · Audio output and caption preference`. selected output is `RITN-HDMI`; approved headset passes local test; user wants captions and chat. consent, privacy, no-secret handling, one minimal output change, two-app validation, disconnect, and the same 8/8 apply. use B after A. for a delayed form, select from commit hash parity (`even=A`, `odd=B`) before opening it.

**critical errors:** asking for or entering a secret; implied consent; unattended persistence; changing scaling/input for technician convenience; opening unrelated files; copying private data; calling a solo transcript live evidence.

**can u explain it?** ✅ - score 7/8. narrate `verified interaction -> consent -> scoped session -> observed state -> minimal action -> validation -> disconnect/audit`. evidence/terms (facts vs inference) and boundary/transfer (retained ownership) must both score 2. near variant: the user withdraws control consent after viewing begins.

**revisit:** next session, answer one cold consent/ownership card. in 48-72h, run the opposite accessibility form through chat/keyboard-only and compare whether the acceptance evidence stays equivalent.

---

## C32 Stage 1 · guided ticket and printer handoff (~6h)

**the idea** - C08/C10 proved u can find a stopped service. Stage 1 proves u can carry that finding through a real ticket without losing the user, the evidence, or the next owner.

**how/why it actually works** - classify work by its purpose: an **incident** restores an unplanned interruption; a **service request** fulfils approved standard work; a **problem** tracks an underlying recurring cause; a **change** controls a modification that could affect service. one event can create linked records.

support flows intake -> classify -> scope -> impact/urgency -> local priority policy -> SLA/update -> diagnosis or fulfilment -> smallest authorized action/escalation -> technical + user validation -> closure -> knowledge decision.

**impact** is breadth/business effect. **urgency** is how quickly harm grows. **priority** comes from the supplied local matrix. job title and volume do not define it. escalation transfers technical work or authority; the ticket still needs a retained owner and next update.

troubleshooting is theory revision: exact symptom -> expected state/scope -> at least two plausible causes -> predicted evidence -> least-risky discriminating test -> raise/lower/reject theory -> act -> rerun original journey + adjacent check. a recent change is a clue, not proof.

dw if the ticket packet feels fussy rn. its what lets the next person continue instead of restarting the user from zero

**words u gotta be able to say:**

- **incident / request / problem / change** - restore, fulfil, explain recurrence, control modification
- **impact / urgency / priority / SLA** - effect, time pressure, work order, agreed targets
- **owner / handoff / escalation** - accountable role, actionable packet, authority transfer
- **hypothesis / prediction / discriminating test** - candidate, expected evidence, separating test
- **workaround / root cause / acceptance** - temporary restore, supported cause, outcome proof
- **KB decision** - reuse/update/create/problem/no-reuse choice

**study sources (pick one route):**

- **recommended:** the lifecycle above + the exact guided packet below. no ticketing product account is required.
- **rather watch communication:** [Professor Messer - Communication](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/communication-220-1202/). **free**, exact episode.
- **rather read troubleshooting:** [Google SRE - Effective Troubleshooting](https://sre.google/sre-book/effective-troubleshooting/). **free**; use it for competing hypotheses, not production-SRE scope claims.

### the required ticket packet

submit:

1. ticket header with record type, asset/service, scope, impact, urgency, priority rationale, SLA/next update, and owner
2. intake with exact error, last known good, recent change, known-good comparison, workaround, safety/security/privacy screen, consent/accessibility
3. hypothesis log with at least two candidates, predictions, tests, results, and theory updates
4. action record with authorization, before state, minimal action, rollback state, and timestamps
5. original journey + adjacent validation + user confirmation
6. acknowledgement, timed status, and closure or handoff message
7. KB update/new draft/problem link or justified `not reusable`

mark every assertion `reported`, `observed`, `inferred`, or `changed`.

**16-point operations scorecard:**

| Dimension | 0 | 1 | 2 | 3 - pass | 4 - strong transfer |
|---|---|---|---|---|---|
| **diagnosis** | no intake or unsafe guess | one cause then fix | scope/evidence but tests dont separate | expected behavior, scope/recent change, plausible theories, discriminating test, supported dependency | also rejects favourite theory, handles uncertainty/multiple causes, separates workaround/root cause |
| **technical action** | unsafe/unauthorized/destructive | broad reset/reinstall/grant | partial restore, weak rollback/validation | smallest authorized reversible action or correct escalation, evidence preserved, original + adjacent validation | also controls change risk, proves rollback/recovery, checks monitoring/prevention |
| **communication** | misleads/blames/exposes/violates consent | no useful expectation | polite but incomplete | impact reflected, plain language, next update, privacy/consent, confirmed outcome | also adapts accessibly and coordinates a clear handoff |
| **documentation** | missing/fabricated | result only | timeline/evidence/owner/closure incomplete | reconstructable classification, evidence, action, owner, validation, knowledge decision | also links records, redacts, records theory revision, leaves reusable prevention |

normal pass is **12/16**, every dimension at least 3. safety/consent/privacy/authorization or secret breach, destructive action without tested recovery, fabricated evidence, broad privilege, closure without acceptance, or escalation without owner/next update forces a changed retry.

**do this - `S1-PRINT-A · Print Spooler stopped`:**

> `nothing prints from any app. the jobs just sit there. i need a PDF for a meeting in 30 minutes.`

environment: disposable Windows 11 VM with `Microsoft Print to PDF`. setup stopped **Print Spooler** and set startup to `Manual`; no second fault exists.

guided path: acknowledge impact without promising the deadline; classify with the supplied local matrix; trace `app -> spooler -> queue -> driver/port -> destination`; write two theories and a separating prediction; use the smallest baseline-authorized repair; run two print validations; get user confirmation; close; make the KB decision.

**committed evidence cards:** queue contains the job; service is stopped/manual; event time correlates; destination and driver are valid; reboot is unnecessary.

<details>
<summary><strong>hidden oracle - open after commitment</strong></summary>

there is exactly one cause: stopped/nonbaseline Print Spooler. acceptance needs before/after service evidence, cleared queue, a new one-page PDF, the original-app job, and user confirmation that the file opens. no reboot, reinstall, or driver replacement.

</details>

**measurable gate:** technical tests **2/2**, complete seven-part ticket packet, score **12/16** with every dimension 3, no automatic retry. this guided form is A2/orientation evidence.

**changed retry / independent gate:** `S1-AUDIO-B · Windows Audio service disabled`. user reports no sound in Teams test call or browser while headset is detected. `Audiosrv` is stopped/disabled; endpoint, profile, permissions, and hardware test are good. at A0, record two theories, service/event evidence, approved startup baseline, two-app validation, user confirmation, and handoff. pass **12/16**, explain **7/8**, no reboot/reinstall/device removal.

**critical errors:** reboot/reinstall/driver or device removal before service evidence; fabricated event/output; startup policy guessed instead of supplied; closure without both app tests and user confirmation; any automatic-retry breach from the scorecard above.

**can u explain it?** ✅ - score 7/8. say why queue state supported a print-path failure but did not prove a bad printer, why reboot was too broad, and why `Running` still needs two print acceptance tests. near variant: Windows Audio is stopped but both audio endpoints remain detected.

**revisit:** next session, classify one changed service ticket cold. in 48-72h, take the opposite service form at A0. reinsert ur weakest documentation field at B1 exit.

---

## C12 · Ubuntu service, package, permission, and log support delta (~12h)

**the idea** - u already proved generic Linux shell skill in Shared Foundations. this block adds the support chain: boot state, systemd unit, journal evidence, package ownership, access context, listener, and validation.

**how/why it actually works** - firmware hands off to GRUB, which loads the Linux kernel and **initramfs**. the kernel finds the real root filesystem, then PID 1 (normally **systemd**) activates units and dependency/order relationships until the target is reached.

a service unit defines its executable, account, environment, dependencies, restart rules, and desired targets. `systemctl` shows unit state. `journalctl` queries structured events by boot, unit, time, priority, or field. `active` only proves process state; a listener, config, file permission, dependency, route, DNS result, or upstream service can still fail.

Ubuntu's package manager verifies repository metadata/packages, resolves dependencies, installs files, runs package scripts, and records state. forcing mixed repos or editing managed files blindly breaks that evidence chain.

effective file access depends on UID/GID, owner/group/other mode bits, every parent directory's traversal bit, ACLs, mount options, and possible AppArmor policy. `chmod 777` erases the question instead of answering it. process stops start with graceful `SIGTERM`; `SIGKILL` is a last resort bc cleanup cannot run.

the local network evidence chain is interface/link -> address/prefix -> route -> resolver -> listener/firewall -> app request. B2 teaches its full networking mechanics; rn u only record which Ubuntu layer is the first failed dependency.

**words u gotta be able to say:**

- **GRUB / kernel / initramfs / PID 1** - bootloader, OS core, early filesystem, first process
- **unit / target / daemon** - systemd object, synchronization group, background service
- **journal / listener** - structured log and bound service socket
- **repository / package / dependency** - managed source, software unit, requirement
- **mount point / UID / GID / rwx / ACL** - attached filesystem, identities, modes, extra access list
- **SIGTERM / SIGKILL** - graceful request / uncatchable last resort

**study sources (pick one route):**

- **recommended:** [Ubuntu Server - Install and manage packages](https://ubuntu.com/server/docs/how-to/software/package-management/) plus ur disposable Ubuntu VM service run. **free**.
- **rather watch:** [Professor Messer - Linux](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/linux-220-1202/). **free**, exact episode; skip generic shell parts u already passed.
- **rather read boot/service:** [bootup(7)](https://man7.org/linux/man-pages/man7/bootup.7.html), [systemctl(1)](https://man7.org/linux/man-pages/man1/systemctl.1.html), and [journalctl(1)](https://man7.org/linux/man-pages/man1/journalctl.1.html). **free** references.
- **optional interactive transfer:** [SadServers - Saint John](https://sadservers.com/scenario/saint-john). **freemium**; the supplied exact service/log fixture is the no-account route.

**do this - `C12-LINUX-A`:** link ur existing Shared Foundations Bandit 0-15 artifact; do **not** replay it. then pass `Saint John` or the supplied equivalent truth matrix, and use a disposable Ubuntu VM (or supplied packet) to record failed units, unit-specific journal, one package install/remove/verify cycle, one owner/group permission repair, `id` plus modes/ownership, address, route, resolver, listener/request state, and post-fix validation.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

the support chain is `firmware -> GRUB -> kernel/initramfs -> root -> systemd target -> unit/process -> listener/dependency -> request`. diagnose the first failed dependency. package state must remain managed; permission repair grants the narrow required right; service validation checks the actual listener/request, not only `active`.

</details>

**measurable gate:** prior Bandit proof linked (not repeated); `Saint John` validator **or** supplied exact truth matrix passes; Ubuntu artifact contains failed units, unit journal, package state, `id`/mode/owner, IP/route/resolver, listener/request, and successful validation.

**changed retry:** `C12-LINUX-B` is [SadServers - Alexandria](https://sadservers.com/scenario/alexandria) or its supplied equivalent plus a changed service. use A0 after 48-72h.

**critical errors:** redoing/claiming B1 ownership of Bandit; `chmod 777`; `kill -9` first; copying a walkthrough as A0; altering production; calling supplied evidence live; reinstalling Ubuntu for one failed unit.

**can u explain it?** ✅ - score 7/8. narrate the boot-to-request chain, then explain why `active` can still be unusable. near variant: unit is active and listener exists, but the request fails bc a parent directory lacks traversal permission.

**revisit:** next session, name three filters `journalctl` can use. in 48-72h, take B. no generic shell review is scheduled here meow

---

## C13 · architecture-aware macOS support (~7h)

**the idea** - the first macOS support question is `Apple silicon or Intel?` bc recovery and boot instructions split before the OS even starts.

**how/why it actually works** - on Apple silicon, immutable Boot ROM verifies the Low-Level Bootloader, which verifies paired firmware and **LocalPolicy**, then iBoot continues into the signed macOS system. holding the power button reaches startup options/RecoveryOS. Intel Macs use EFI-era paths and different key combinations; T2 models add their own secure-boot chain.

**APFS** puts volumes inside a container that can share free space. modern macOS separates system/data roles and may use local snapshots. Disk Utility shows physical device -> container -> volumes and runs First Aid in Apple's stated order. a local snapshot stays on the same storage path; Time Machine is versioned backup to another destination.

Activity Monitor shows processes/resources. Console shows time-correlated logs. **launchd** manages jobs/services. Keychain stores credentials/certificates/keys, so one app looping prompts while web sign-in works may be Keychain/app identity, not a global password failure.

FileVault protects the startup volume. Gatekeeper/notarization, Rosetta architecture, quarantine, privacy/TCC controls, profiles, and network services can each block an installed app. do not bypass FileVault, Activation Lock, MDM, firmware security, or secure boot.

Mac instructions get weird fast when the architecture is missing. ask that first and half the bad advice disappears meow

**words u gotta be able to say:**

- **Apple silicon / Intel / Boot ROM / LLB / iBoot** - architecture split and boot stages
- **LocalPolicy / RecoveryOS** - signed boot policy / repair environment
- **APFS container / volume / snapshot** - shared pool, logical filesystem, local point-in-time state
- **Signed System Volume / FileVault** - protected system content / encrypted startup volume
- **launchd / Activity Monitor / Console** - service manager, process tool, log tool
- **Keychain / Gatekeeper / TCC / Rosetta 2** - secrets, app trust, privacy, translation

**study sources (pick one route):**

- **recommended:** [Apple - macOS Recovery](https://support.apple.com/en-us/102518) plus [Apple silicon boot process](https://support.apple.com/guide/security/boot-process-secac71d5623/web) → five-ticket packet. **free**.
- **rather watch:** [Professor Messer - macOS Overview](https://www.professormesser.com/free-a-plus-training/220-1202/220-1202-video/macos-overview-220-1202/). **free**, exact episode.
- **rather read storage:** [Apple - Repair a storage device with Disk Utility](https://support.apple.com/en-us/102611). **free**, exact backup warning and First Aid order.

**do this - `C13-MAC-A`:** solve five supplied cards: enter Recovery on Apple silicon; enter it on Intel; First Aid cannot repair and no current backup exists; one app loops Keychain prompts while account web sign-in works; one app lacks camera while FaceTime works. state tool, required evidence, safe action, and stop/escalate condition.

if u own a Mac, u may add five read-only artifacts from Apple Diagnostics, Activity Monitor, Console, Disk Utility device tree, and Time Machine status. theyre supplemental. no-Mac learners use `simulation-supplied` and make no live-admin claim.

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

Apple silicon uses hold-power startup options; Intel uses the documented Intel key path. failed First Aid with no backup means preserve/escalate before erase/reinstall. Keychain and account password are separate states. camera working in FaceTime proves hardware enough to inspect the failing app's TCC permission. FileVault/recovery and security boundaries stay intact.

</details>

**measurable gate:** **5/5** architecture-correct tool/evidence/action/stop decisions. live users may add five evidence items; simulation users pass the same mechanism gate.

**changed retry:** `C13-MAC-B` changes app, protected device, storage symptom, and architecture labels.

**critical errors:** calling simulation live; erase/reinstall without backup; conflating Keychain with account password; swapping architecture recovery methods; bypassing FileVault/Activation Lock/MDM/security.

**can u explain it?** ✅ - score 7/8. compare Apple silicon and Intel entry, APFS container/volume/snapshot vs Time Machine, and Keychain vs account password. near variant: camera works in one app but not another.

**revisit:** next session, answer the architecture split cold. 48-72h later, take B.

---

## C15 · virtualization, cloud, VDI, and containers (~13h)

**the idea** - virtualization moves the failure boundary. u still troubleshoot CPU, memory, storage, and network... but now a host, hypervisor, virtual switch, image, broker, or provider may own the broken layer.

**how/why it actually works** - a **hypervisor** presents vCPU, vRAM, virtual disk, firmware, and vNIC to a guest. hardware virtualization lets most guest instructions run directly while sensitive operations return to the hypervisor. a hosted/type-2 hypervisor like VirtualBox also depends on the host OS, drivers, security controls, and resources.

vCPU is scheduled host CPU time. vRAM consumes host memory or paging. overcommit can slow every otherwise healthy VM. dynamic virtual disks grow on host storage. Guest Additions improve display, pointer, time, storage, and network behavior.

VirtualBox **NAT** gives outbound access through a virtual router. **host-only** connects host/guests without external routing. **internal** connects selected guests only. **bridged** places a guest on the physical LAN and is not used for the lab DHCP/DC work here.

a snapshot creates a dependent differencing chain. it rolls back a guest change quickly but can die with its base disk, metadata, host storage, deletion, ransomware, or corruption. an export becomes independent only after a fresh import boots and passes the same acceptance test; same-host storage is still one failure domain.

a **container** packages an app/user space while sharing the host kernel. namespaces isolate views and cgroups control resources. a VM carries a guest kernel/virtual hardware. **VDI** adds broker, session host/image, identity, profile, and network layers. cloud service models then split responsibility: IaaS leaves more OS/app control with the customer; PaaS moves runtime/platform down to provider scope; SaaS still leaves customer identity, access, configuration, and data policy.

lots of layers, yeah... but its still the same question: who owns the first broken state? qwq

**words u gotta be able to say:**

- **type 1 / type 2 / VT-x / AMD-V / VM exit** - hypervisor types, CPU support, control transfer
- **vCPU / vRAM / overcommit / dynamic disk** - virtual resources and host pressure
- **NAT / bridged / host-only / internal** - virtual network boundaries
- **snapshot / differencing image / clone / export** - dependent rollback layers and copies
- **container / image / volume / namespace / cgroup** - shared-kernel package and isolation/resource parts
- **VDI broker / session host / profile** - remote-desktop service layers
- **IaaS / PaaS / SaaS / shared responsibility** - service models and ownership split

**study sources (pick one route):**

- **recommended:** [VirtualBox - Virtual Networking](https://www.virtualbox.org/manual/ch06.html) → two-VM restore task. **free**; base package is enough, Extension Pack is not required.
- **rather watch:** [Professor Messer - Virtualization Concepts](https://www.professormesser.com/free-a-plus-training/220-1201/220-1201-video/virtualization-concepts-220-1201/). **free**, exact episode.
- **rather read snapshot boundary:** [Microsoft - Hyper-V checkpoints](https://learn.microsoft.com/en-us/windows-server/virtualization/hyper-v/checkpoints). **free**, explicitly says a checkpoint is not a full backup.

**do this - `C15-VM-A`:** build two small Linux VMs. each gets NAT for outbound access and a host-only adapter for the isolated lab. prove expected NAT, host-only addresses, peer ping/SSH, and isolation from unsolicited LAN inbound. snapshot VM1, create a marker, restore, and prove it vanished. separately export VM1, record size/checksum, power off the original, import under a new name/directory, boot, and rerun the network/file acceptance test.

capacity-limited route: run the live checks sequentially with smaller allocations where possible, or use the supplied `C15-VM-A` boot/network/snapshot/import state cards. commit predictions before the oracle and label supplied work `simulation-supplied`; it proves boundary reasoning, not live VM administration.

then solve four supplied comparison cards:

- V1: isolated legacy OS dependency
- V2: pooled remote desktop with profile persistence failure
- V3: stateless packaged service sharing the host kernel
- V4: SaaS control-plane outage while customer identity/client/network evidence remains separate

<details>
<summary><strong>truth oracle - open after commitment</strong></summary>

VM acceptance is **6/6**: expected NAT behavior, host-only addresses, peer path, marker rollback, export size/checksum, and fresh imported acceptance. state whether export storage is a separate failure domain; same-host is a lab copy, not resilient backup.

comparison truth: V1 needs a full VM rather than application virtualization alone; V2 is VDI broker/session/profile scope before blaming the thin client; V3 is a container; V4 separates provider control-plane ownership from customer identity/client/network responsibilities.

</details>

**measurable gate:** VM **6/6** plus comparison **4/4**.

**changed retry:** `C15-VM-B` changes adapter order, clone name, marker, and all four surface cases.

**critical errors:** bridged DHCP/DC work on a real LAN; snapshot called backup; VDI/container/full VM conflated; SaaS provider blamed for customer identity/data policy; paid cloud required; export called resilient without a separate failure domain.

**can u explain it?** ✅ - score 7/8. explain vCPU/vRAM scheduling, all four network modes, snapshot dependency, VM vs container, and provider/customer boundary. near variant: every VM slows at once while no guest process shows pressure.

**revisit:** next session, draw base disk + differencing image + host failure domain. in 48-72h, take B. only after this practical + explain gate passes may u open the virtualization/cloud A+ comparison bridge below.

---

## optional post-C15 virtualization/cloud comparison bridge

open this only after `C15-VM-A/B` passes. this is checkpoint translation, not a replacement lab.

**application-virtualization card (1/1):** given one locally streamed/packaged app, one full legacy-OS VM, one pooled VDI session, and one shared-kernel container, choose the right boundary and state its dependency/isolation tradeoff.

**cloud comparison cards (6/6):** distinguish:

1. public vs private vs hybrid vs community deployment
2. shared vs dedicated resources
3. metering plus ingress/egress
4. elasticity vs availability
5. file sync
6. multitenancy

**gate:** application virtualization **1/1** and cloud comparisons **6/6**. a label without the customer/provider responsibility boundary does not pass.

dw, this bridge comes here bc now the words attach to a VM u actually broke and restored. before C15 theyre floating flashcards. after C15 they name boundaries u already proved meow

---

## B1 exit · unlabeled mixed endpoint case

do this 20-30 minutes at A0. it mixes one new endpoint symptom, B0 safety, C14 consent/accessibility, one older evidence mistake, and irrelevant evidence. commit before the truth.

### `B1-EXIT-A · Docked presentation failure`

an authorized remote user reports one external display missing after an update. direct HDMI works. dock video works with a known-good 40 Gbps cable. the supplied cable supports USB 2 data and 60 W PD but **no DisplayPort Alt Mode**. firmware enumerates the dock. logs contain an unrelated red updater event. a photographed spare battery is swollen. the user requires chat and 175% scaling.

**required 8/8:**

1. stop spare-battery use and charging
2. verify interaction and preserve consent/privacy/accessibility
3. reject update anchoring from the known-good comparison
4. identify the cable capability boundary
5. cite the 40 Gbps known-good cable comparison
6. choose minimal cable replacement or authorized escalation
7. validate both direct and docked display paths
8. leave a reconstructable ticket/handoff with owner and next update

<details>
<summary><strong>exit truth - reveal after commitment</strong></summary>

the supplied cable lacks DisplayPort Alt Mode. thats causal. the update and red event are decoys. the swollen battery is a separate mandatory stop. the repair must not change 175% scaling or force voice/screenshare.

</details>

### parallel `B1-EXIT-B · Camera unavailable in one app`

camera works in the system test and browser but not the meeting app. privacy permission is denied for that app. a wet spare keyboard is a safety stop. a recent driver update is a decoy. use the same safety, consent, evidence, minimal-repair, two-context validation, and handoff matrix.

**B1 exit gate:** selected form **8/8**, explain **7/8** with causal chain 2, Stage 1 ticket linked, and no critical error. if A1-A3 aid was used, repair then take the parallel form at A0.

---

## B1 artifact check

before moving on, ur endpoint packet contains all of these with synthetic IDs and redaction checked:

- [ ] C04 no-start/power decision tree and committed case result
- [ ] C05 before/load/after table plus storage/thermal/RAID decisions
- [ ] C06 capability matrix
- [ ] C07 service-manual replace/escalate sheet, labelled physical or case evidence
- [ ] C08 print-path evidence
- [ ] C09 recovery/backup validation with RPO/RTO
- [ ] C10 service/event/registry/process timeline
- [ ] C11 least-privilege repair and three security decisions
- [ ] C14 remote-session packet or clearly labelled solo simulation
- [ ] C32 Stage 1 seven-part ticket/handoff plus scorecard
- [ ] C12 Ubuntu service/package/log evidence (prior Bandit proof linked, not repeated)
- [ ] C13 macOS five-ticket packet or labelled live supplement
- [ ] C15 VM rollback/import proof and responsibility cases
- [ ] one B1 exit form 8/8 at A0

the physical/mobile/Mac supplied paths prove diagnosis and safe decision-making. they do **not** prove live part replacement, physical Desktop Support work, or live Mac administration. keep that sentence in the artifact claim.

---

## block test-out + re-entry

a job title, A+ score, course, or screenshot permits an attempt and waives nothing. B1 test-out needs:

1. fresh practical cards from each stratum below
2. every selected numeric gate
3. C03 safety plus C14 handoff embedded in the run
4. exit **8/8**
5. explanation **7/8**, causal chain 2, no critical error

`B1-X-A` selects one fresh card from each stratum:

- `{C04, C05}`
- `{C06, C07, C08}`
- `{C09, C10, C11}`
- `{C12, C13, C15}`

before seeing any cards, commit a seed. calculate `SHA256(seed + "B1")`; use successive two-bit chunks modulo each stratum size. record the selected case IDs in the oracle. separate strata prevent collision.

physical Desktop Support claims still need real authorized hardware evidence. supplied cases earn the narrower diagnosis/safety claim. Mac simulation stays simulation.

**re-entry on a miss:**

| Failed evidence | Return here | Fresh proof after repair |
|---|---|---|
| power/POST/enumeration | C04 | `C04-PLATFORM-B` |
| memory/storage/RAID/thermal | C05 | `C05-RESOURCE-B` |
| cable/dock/display path | C06 | `C06-PATH-B` |
| mobile/FRU/battery | C07 | `C07-MOBILE-B` |
| print pipeline | C08 + Stage 1 if ticket weak | `C08-PRINT-B` or `S1-AUDIO-B` |
| startup/recovery/backup | C09 | `C09-RECOVERY-B` |
| process/service/event/registry | C10 | `C10-STATE-B` |
| ACL/app/security boundary | C11 | `C11-ACCESS-B` |
| consent/privacy/accessibility | C14 | `C14-REMOTE-B` |
| Ubuntu support delta | C12 | `C12-LINUX-B` |
| macOS architecture/boundary | C13 | `C13-MAC-B` |
| VM/network/snapshot/service boundary | C15 | `C15-VM-B` |

re-enter the failed cluster only. dont replay 129 hours bc one evidence chain was weak ;w;

---

## optional: how B1 maps to A+ after the gates

the actual requirement is the B1 evidence above. if ur considering CompTIA A+ later, the current codes are **220-1201 Core 1** and **220-1202 Core 2**. B1 naturally covers:

| B1 work | Optional exam domains it supports |
|---|---|
| C04-C08 | Core 1 Domain 1 Mobile Devices, Domain 3 Hardware, Domain 5 Hardware/Network Troubleshooting |
| C09-C13 | Core 2 Domain 1 Operating Systems, Domain 2 Security, Domain 3 Software Troubleshooting |
| C14 + Stage 1 | Core 2 Domain 4 Operational Procedures |
| C15 | Core 1 Domain 4 Virtualization and Cloud Computing; Core 2 backup/recovery wording |

some exam objectives ask for broad product/connector recognition that the real mechanism lab doesnt need. the cards below close only those finite wording/selection deltas. do them **after the owning C-topic passes**, and only if the checkpoint helps ur situation.

<details>
<summary><strong>Core 1 post-gate cards (220-1201)</strong></summary>

### after C04-C05

- **RAM selection 4/4:** DIMM vs SODIMM, DDR compatibility, ECC vs non-ECC, single/dual/quad channel.
- **storage recognition 4/4:** SAS, mSATA, removable flash/card, optical; keep the C05 RAID mechanism.
- **platform decisions 6/6:** form factor, CPU socket/multisocket, boot/Secure Boot, TPM vs HSM, add-on card/header, cooling. label supplied selection, not installation.
- **PSU decisions 6/6:** input region, rail/connector, wattage/headroom, redundancy, modularity, efficiency. no live probing.
- **date/time ticket 1/1:** separate time source from RTC/CMOS evidence before safe replacement/escalation.
- Core 1 5.2 needs no extra bridge; C05's storage/RAID **5/5** is the base.

### after C06-C07

- **FRU decisions 8/8:** keyboard, RAM, Wi-Fi card, biometric part, near-field scanner/privacy part, antenna, camera, microphone. manual/safety decides replace vs escalate.
- **accessories 11/11:** microUSB, miniUSB, Lightning, NFC, tethering/hotspot, port replicator vs dock, stylus, speaker, drawing pad, trackpad, track point.
- **mobile settings 6/6:** SIM/eSIM hotspot, manual-PIN Bluetooth, GPS/cellular location, calendar/contacts/mail/cloud sync, data cap, radio/data enable-disable. record UI version and MDM tier.
- **display/panel cold cards 12/12:** IPS/TN/VA/OLED/Mini-LED, touch/digitizer, density/refresh/resolution/gamut; mark inverter as legacy.
- **media deck 20/20:** direct-burial STP, plenum, USB 2/3, serial, DVI/VGA/DB9/Molex, SATA/eSATA, fiber/connector types, T568A/B. a simulated card does not prove termination.
- **display symptoms 5/5:** projector bulb/dim/shutdown; fuzzy/sizing/distortion; burn-in vs dead pixel; flashing/color; source/cable/audio.
- **mobile tickets 2/2:** cursor calibration and app-install storage/policy fault.

### after C08

- **MFD configuration 6/6:** setup/firmware/connectivity/share; duplex/orientation/tray/quality; secure print/badge; audit; email/SMB/cloud scan plus ADF/flatbed; PCL vs PostScript.
- **maintenance 3/3:** inkjet cartridge/head/roller/feeder; thermal feed/paper/heater; impact multipart/ribbon/head. no live fuser work.
- **printer defects 6/6:** repeating lines, speckle/ghost, fade, jam/feed/misfeed/noise, garbled render, staple/hole-punch. record first evidence before reset.

### after C15

- **application virtualization 1/1** and **cloud comparisons 6/6** are the bridge immediately above. dont repeat them.

**queued for B2, not a B1 gate:** port flapping, jitter, and VoIP metric cards belong after C20/C24. B1 does not claim them early.

</details>

<details>
<summary><strong>Core 2 post-gate cards (220-1202)</strong></summary>

### after C09-C10

- **OS/filesystem comparison 8/8:** Chrome OS/mobile support boundary, ReFS/XFS, EOL, cross-filesystem compatibility.
- **install plans 2/2:** PXE/remote install and MBR vs GPT. destructive partitioning stays supplied/disposable.
- **dated Windows edition decisions 8/8:** domain join, RDP host, BitLocker, Group Policy Editor, workstation/RAM needs, N-edition media, clean vs in-place, Windows 11 TPM/UEFI.
- **tool selection/output 14/14:** Task Manager Startup/Performance/Users; Disk Management; Task Scheduler; Device Manager; Certificate Manager; Local Users/Groups; Performance Monitor; System Information; Resource Monitor; System Configuration; Disk Cleanup; Defragment.
- **Windows command purpose/output 23/23:** `cd`, `dir`, `ipconfig`, `ping`, `netstat`, `nslookup`, `net use`, `tracert`, `pathping`, `chkdsk`, `format`, `diskpart`, `md`, `rmdir`, `robocopy`, `hostname`, `net user`, `winver`, `whoami`, command help, `gpupdate`, `gpresult`, `sfc`. risky effects stay supplied/disposable; C25 owns later cross-shell proof.
- **Windows settings outcomes 10/10:** browser/apps; device/print; sharing/network/firewall; system/index/admin; mail/sound; account/device; Explorer; power/accessibility; time/update; personalization/privacy/gaming. a dated location lookup is allowed.
- **Windows diagnostic tickets 3/3:** USB resource exhaustion, slow-profile isolation, time drift; evidence precedes repair.
- **recovery plans 2/2:** synthetic/full/incremental/differential and GFS/3-2-1 against a stated RPO/RTO.

**queued for B2:** proxy, public/private profile, metered link, WWAN, and shared printer/mapped-drive outcomes need C23 network evidence before their 5/5 gate.

### after C11

- standard-user application requirements are base-complete; no extra card.
- **malware/tool comparisons 4/4:** a malware/tool label does not prove root cause or removal.
- **threat/social-engineering classification 28/28:** named methods, attacks, vulnerabilities, and safe support response. C32 later owns the full operations decision; SQLi/XSS mechanism stays in cybersecurity.
- **A+ malware-removal wording 10/10:** optional translation only. local security/IR policy and current Windows behavior override improvised exam order.
- **baseline cases 5/5:** UEFI password, screen/logon restriction, password-lockout-guest-timeout policy, AutoRun, unused service/default control. apply current length/uniqueness policy nuance.
- **media/method/authority 6/6:** magnetic, SSD/flash, optical/paper, vendor certificate, recycle/repurpose, regulatory/environmental boundary. `standard format` is insufficient for many sanitization policies.
- **browser trust/settings 8/8:** trusted download/hash; patch/extension; password manager; certificate warning; popup/adblock; cache/private/sync limits; proxy vs secure DNS; feature enable/disable.
- PC security symptoms are base-complete through C11's three security cards.

**queued for later owners:** mobile wipe/location policy needs C31; SOHO UPnP/guest isolation needs C22; complete security/asset operations need later C32 stages.

### after C12-C13

- **macOS feature/tool/file-type deck 20/20:** app formats, folder scopes, Apple ID/restrictions, AV/update/RSR, display/network/print/scan/accessibility/Time Machine, Mission Control/Spotlight/iCloud/Gestures/Finder/Dock/Continuity, FileVault/Terminal/Force Quit. keep simulation labelled.
- **Linux purpose/output deck 36/36:** the 27 named commands from the official objectives, five config files, systemd/kernel/bootloader, and root account. distro differences stay explicit. this is translation after the Ubuntu support gate, not another generic shell course.

### after C14

- **remote method selection 4/4:** VNC, RMM, SPICE, and WinRM, each with consent, authorization, and exposure boundary. C23 later adds VPN network evidence.

</details>

this mapping doesnt mean B1 alone makes the whole A+ ready. B2/B3 own networking, scripting, identity, cloud-product, asset, and later operations evidence. the cert hub will reverse-map all of it when that file is rewritten.

---

## next session - what B2 expects

before opening B2, answer these cold:

1. draw `power -> POST -> boot -> enumeration -> driver` and place one failure at each boundary
2. explain snapshot vs rollback vs independent backup using ur C09/C15 evidence
3. trace `app -> spooler -> queue -> port -> controller -> imaging`
4. give the consent/control/secret/disconnect chain for remote support
5. compare one Windows event, one Linux journal entry, and one macOS Console entry: what does each prove, and what does it not prove?

**ur ready for B2 when:**

- [ ] all C04-C15/C14/Stage 1 measurable gates pass
- [ ] every explain gate is 7/8 with causal chain 2
- [ ] the B1 endpoint packet is complete and redaction-checked
- [ ] one B1 exit form passes 8/8 at A0
- [ ] physical/Mac/simulation claims are labelled honestly

B2 moves from local endpoints into PowerShell objects and network evidence. it assumes u can already recover a VM, read local OS state, repair access narrowly, and hand off a ticket without guessing.

if one cold answer falls apart, use the re-entry table. fix that cluster and take its B form. no full restart needed... thats the whole point of making the path this specific meow

---

[Previous: B0 - Lab, Safety, and Support Evidence](00-prep.md) · [Hub](README.md) · [Next: B2 - Core Support Skills](02-core.md)

*Verified 2026-07-11. All primary routes are free or have a labelled free/case fallback. Windows VM work uses legitimate media/evaluation only; VirtualBox base package is sufficient; no Extension Pack, paid cloud, physical disassembly, or Mac is required. Report dead links or changed access facts to the maintainer.*
