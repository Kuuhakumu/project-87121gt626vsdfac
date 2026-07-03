# goal 5: portfolio, resume & job hunt meow (~100h)

> **goal:** turn the work u already did into proof a hiring team can understand fast: pinned projects, clear writeups, a targeted resume, and a region-agnostic role-search system.
>
> **pace:** ~100 hours total ~= 7 weeks at 2h/day, but this runs beside Goal 4. dont wait until the end to start writing things up.
>
> **hard rule:** no salary tables, no job-board lists. use role types, employer types, company-direct pages, communities, and referrals.

[<- Goal 4: Specialization](04-specialization.md) | [Back to hub](README.md) | [Beyond Entry-Level ->](beyond-entry.md)

---

## read this first meow

the portfolio is not a trophy case.
its evidence.

each good artifact says three things at once:

- i can do the technical work.
- i understand why the thing worked.
- i can explain it clearly enough that someone else can trust me.

thats why every serious project below ships **two artifacts**:

1. a **repo** - configs, code, rules, screenshots, report files, and setup notes.
2. a **writeup** - the story of what happened, why it matters, and what u learned.

the repo proves u built.
the writeup proves u understood.
same two-gate idea as the whole guide, just visible to strangers now qwq.

---

## how to track your progress meow

the `- [ ]` boxes here are display-only in this public repo.
fork the repo, or copy this checklist into Obsidian/OneNote, if u want boxes u can actually tick.

the real progress signal is still:

1. **measurable gate** - a repo, report, target list, resume draft, or interview story exists and can be inspected.
2. **can u explain it?** - u can walk the reasoning unaided, not just point at a file.

both must pass before a box means anything meow.

---

## the path (todo-tree)

- [ ] **Goal 5 - convert learning into hiring signal** (~100h): build a small, sharp portfolio and target roles without getting lost in random postings.
  - [ ] **Portfolio signal** (~60h): pick 4-6 strong projects, each with a repo + writeup.
  - [ ] **GitHub mechanics** (~8h): make the profile README and pinned repos easy to scan in 20 seconds.
  - [ ] **Resume + ATS targeting** (~12h): use the NICE/JD keyword loop, not vague "keyword stuffing."
  - [ ] **Role targeting** (~12h): map titles to NICE work roles, employer types, and the help-desk/NOC -> SOC on-ramp.
  - [ ] **Interview prep** (~8h): turn each project into a short technical story and a STAR story.
  - [ ] **exit check**: 4-6 pinned repos, one targeted resume, one target-employer list, and u can explain the path u are aiming for.

---

## portfolio rule: repo + writeup meow (~60h)

**the idea** - a junior portfolio works when each project proves one hireable skill and explains the security impact clearly.

**how/why it actually works** - hiring screens are time-limited.
most people will not run your lab or read every line of code.
they skim the README, look for evidence u actually built it, then check whether the writeup makes the reasoning legible.
so the artifact has to front-load the signal:

- **security-impact line** first: "detects Kerberoasting and LLMNR poisoning across a 3-host AD lab," not "my Wazuh project."
- **diagram** next: topology, data flow, attack chain, or control map.
- **evidence** after that: screenshots, rule files, query output, report excerpts, before/after scan result.
- **writeup link** beside it: what happened, why it worked, how to detect/fix it.

quality beats quantity.
pin **4-6 strongest** repos.
an unpinned pile of tutorial-follow repos lowers signal; one clean lab with a real writeup is stronger than ten noisy ones.

blog the learning as u go.
each lab u already finish can become a short post for maybe 30 extra minutes: what u tried, what broke, why the fix worked, and what a defender or stakeholder should care about.
thats not vanity; its portable proof that u can communicate under messy conditions.

**words u gotta be able to say**

- **portfolio signal** - proof someone can inspect quickly
- **security-impact line** - one sentence saying what risk it addresses
- **writeup** - reasoning, evidence, and lesson learned
- **pinned repo** - GitHub project shown on profile
- **commit history** - visible build process over time
- **artifact** - repo, report, rule, dashboard, or post
- **proof of work** - evidence u did the thing

**study sources (pick what fits your style)**

- [GitHub Docs - Managing your profile README](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme) - official setup for the profile landing page. **free**
- [Google Technical Writing One](https://developers.google.com/tech-writing/one) - short sentences, active voice, and defining acronyms once. use it for READMEs, writeups, and resumes. **free**
- [TCM Security Sample Pentest Report](https://github.com/hmaverickadams/TCM-Security-Sample-Pentest-Report) - concrete report structure: executive summary, findings, evidence, remediation. **free**
- [TCM - How to Write a Pentest Report](https://www.youtube.com/watch?v=EOoBAq6z4Zk) - specific video walkthrough of the report structure above. **free**
- [0xdf HTB writeups](https://0xdf.gitlab.io/) - study the structure: recon -> enum -> exploit -> privesc -> beyond-root/remediation. dont copy content. **free**

**do this** - make a profile README, then create a tiny template for every serious project:

- `README.md` with the security-impact line, diagram, setup, evidence, and writeup link.
- `WRITEUP.md` or blog link with the story and lessons learned.
- `assets/` for screenshots or diagrams.
- `rules/`, `queries/`, `reports/`, or `src/` depending on the project.

**measurable gate:** profile README exists, 4-6 repos are pinned, and every pinned repo has a security-impact line, evidence screenshot/output, and a writeup link.

**can u explain it?** ✅ - unaided, point to each pinned repo and say: what risk it addresses, what u built, what evidence proves it works, and what u would improve next.

---

## the 8 concrete builds meow

pick one lane and go deep, but build **Project 1** no matter what if u can.
the AD attack+detect lab is the T-shape showpiece because it proves u understand the environment security actually runs in, not just one tool.

u do **not** need all 8 before applying.
aim for Project 1 plus 3-5 more that match your lane.

### project 1 - home AD lab: attack and detect it (~15-25h)

- [ ] **build the showpiece:** stand up a small Active Directory lab, run one realistic attack chain, then detect the same activity from the blue side.

**what it proves** - enterprise environment fluency, both-sides thinking, Windows/AD basics, attack chain reasoning, log visibility, and detection mapping.

**rough scope** - deploy [GOAD - Game of Active Directory](https://github.com/Orange-Cyberdefense/GOAD) with MINILAB, or build a tiny domain with a Domain Controller and one workstation.
run one chain end to end, such as LLMNR/NBT-NS poisoning -> hash capture -> Kerberoasting -> lateral movement.
then ship logs into [Wazuh Quickstart](https://documentation.wazuh.com/current/quickstart.html), identify which events fired, and map each step in [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/).

**ship** - GitHub repo with topology diagram, build notes, commands, detection rules, screenshots, and a two-part writeup:

- Part 1: attacking the lab.
- Part 2: detecting what i just did.

**measurable gate:** repo contains the lab topology, attack evidence, detection evidence, and ATT&CK technique mapping for each major step.

**can u explain it?** ✅ - explain why AD makes this attack possible, what log source showed each step, and which detection would have caught it earlier. dw, this is the one that makes the rest of the portfolio feel real meow.

### project 2 - home SOC with Wazuh + your own rules (~12-18h)

- [ ] **build the blue baseline:** stand up Wazuh, ingest logs from 2-3 endpoints, and write detections that are yours.

**what it proves** - SIEM setup, endpoint log collection, rule writing, false-positive tuning, and SOC triage.

**rough scope** - Wazuh manager plus a Windows Eval box and a Linux box.
generate benign and suspicious activity: failed-login burst, suspicious PowerShell one-liner, EICAR test file, or known lab telemetry.
write **3-5 custom rules/decoders**, tune one false positive, screenshot the alert firing, and document the logic.

**ship** - repo with `local_rules.xml`, dashboards/screenshots, and `DETECTIONS.md`.
each detection gets: behavior, log source, rule logic, ATT&CK ID, and false-positive notes.
add one short writeup about the false positive u tuned, bc noise reduction is the real SOC skill hiding inside this project.

**measurable gate:** 3-5 custom detections fire on generated activity, one noisy rule is tuned, and the writeup explains before/after behavior.

**can u explain it?** ✅ - take one alert from raw event -> parsed fields -> rule condition -> alert -> triage verdict -> tuning decision.

### project 3 - publish 5 Sigma rules mapped to ATT&CK (~8-12h)

- [ ] **build detection-engineering proof:** write portable Sigma rules and convert at least one into a SIEM query.

**what it proves** - log-source literacy, vendor-neutral detection logic, ATT&CK mapping, and detections-as-code habits.

**rough scope** - author **5 rules** in proper Sigma YAML:
`logsource`, `detection`, `condition`, `falsepositives`, `level`, and ATT&CK `tags`.
target real techniques like scheduled task persistence, suspicious PowerShell, brute force, or credential dumping indicators.
use [SigmaHQ - Rule Creation Guide](https://github.com/SigmaHQ/sigma/wiki/Rule-Creation-Guide) and [Sigma - Getting Started](https://sigmahq.io/docs/guide/getting-started.html) to convert at least one rule with `sigma-cli`.

**ship** - repo mirroring [SigmaHQ/sigma](https://github.com/SigmaHQ/sigma) folder style.
README shows source event -> Sigma rule -> converted query.
write a short `WRITEUP.md` explaining one rule from source event -> field selection -> Sigma condition -> converted SPL/KQL query.
stretch: open a PR upstream if the rule is genuinely useful.

**measurable gate:** 5 valid Sigma YAML files, each with ATT&CK tags and false-positive notes, plus one converted Splunk SPL or Microsoft Sentinel KQL query.

**can u explain it?** ✅ - explain the exact behavior each rule detects, what log source it needs, and why the ATT&CK technique tag fits.

### project 4 - documented HTB/TryHackMe writeup series (~2-4h each, ongoing)

- [ ] **build methodology proof:** write 5-10 permitted CTF/lab writeups that show how u think, not just commands.

**what it proves** - recon discipline, enumeration, exploitation logic, remediation thinking, and communication.

**rough scope** - use beginner rooms or **retired** boxes only.
write each as: Recon -> Enumeration -> Exploitation -> PrivEsc -> Remediation / how to detect this.
dont publish active HTB walkthroughs, dont dump flags, and follow each platform's rules.

**ship** - blog posts plus a GitHub repo that indexes the series and stores reusable notes/templates.
model structure on [0xdf HTB writeups](https://0xdf.gitlab.io/), but write your own reasoning.

**measurable gate:** 5 permitted writeups are published, each includes commands, evidence, why the step worked, and a remediation/detection section.

**can u explain it?** ✅ - pick one writeup and narrate the path from first scan to root/admin, then say how a defender could detect or prevent the same path.

### project 5 - Python or PowerShell security tool (~8-15h)

- [ ] **build automation proof:** turn one annoying security task into a small CLI tool.

**what it proves** - scripting ability, input/output handling, basic testing, and security workflow automation.

**rough scope** - write a real CLI tool, about 100-300 lines, with clear usage examples and at least a couple tests.
good beginner ideas:

- parse Linux `auth.log` for failed-login bursts -> output source IPs and counts.
- extract IOCs from a threat report -> IPs, domains, URLs, hashes, defang/refang.
- map suspicious command lines to MITRE ATT&CK technique IDs.
- summarize Wazuh alerts into a short incident note.

**ship** - repo with `README.md`, `src/`, tests, `requirements.txt` if Python, and demo output or an asciinema/GIF.
link back to the scripting work from [Goal 3](03-scripting-ctf.md).
add a short writeup explaining the security problem, why automation helps, and what edge cases your tool handles.

**measurable gate:** tool runs from the command line on sample input, produces the documented output, and has at least two tests or sample fixtures.

**can u explain it?** ✅ - explain the input, parsing logic, output, failure cases, and one security workflow it saves time in.

### project 6 - SOC investigation report from Splunk BOTS v3 (~10-15h)

- [ ] **build analyst-job proof:** investigate a real dataset and write the kind of report someone could hand to a stakeholder.

**what it proves** - querying logs at volume, building a timeline, identifying IOCs, mapping ATT&CK, and writing an incident report.

**rough scope** - load [Splunk Boss of the SOC v3 dataset](https://github.com/splunk/botsv3) into Splunk Free or use the prebuilt dataset flow.
work the scenario, then write a clean incident report: executive summary, timeline, affected assets, IOCs, ATT&CK mapping, and recommendations.

**ship** - repo with `INCIDENT-REPORT.md` or a clean PDF, selected query snippets, screenshots, and a README impact line.
use [TCM Security Sample Pentest Report](https://github.com/hmaverickadams/TCM-Security-Sample-Pentest-Report) for report shape, even though this is defensive.

**measurable gate:** report includes timeline, IOCs, ATT&CK mapping, evidence screenshots/query snippets, and recommendations.

**can u explain it?** ✅ - walk the incident from first suspicious event -> timeline -> impact -> containment/remediation.

### project 7 - cloud IAM / misconfig audit writeup (~10-15h)

- [ ] **build cloud-security proof:** find and fix cloud misconfiguration in an account u own.

**what it proves** - cloud IAM, posture scanning, prioritization, remediation, and before/after evidence.

**rough scope** - choose one:

- deploy a [CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat) scenario in your own AWS account, finish the attack path, then write the defensive fix.
- run [Prowler](https://github.com/prowler-cloud/prowler) or [ScoutSuite](https://github.com/nccgroup/ScoutSuite) against your own cloud account, remediate one real finding, then re-scan.

only scan accounts u own or are explicitly authorized to test.
say that in the writeup.

**ship** - repo with audit report, before/after findings, remediation steps, and a short blog post: "here is the misconfig, here is why it mattered, here is the fix."

**measurable gate:** before/after scan evidence proves at least one finding was remediated.

**can u explain it?** ✅ - explain the IAM/resource policy or configuration that caused the exposure, why the scanner caught it, and what exact change fixed it.

### project 8 - mock risk assessment / framework gap analysis (~10-15h)

- [ ] **build GRC proof:** turn a fictional org into a risk/control/evidence artifact.

**what it proves** - framework fluency, risk thinking, control mapping, and stakeholder communication.

**rough scope** - invent a small org and choose one:

- a [NIST SP 800-30 Rev. 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) risk assessment: asset -> threat -> vulnerability -> likelihood/impact -> treatment -> owner.
- a [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) gap analysis: current state -> target state -> control gap -> remediation roadmap.

**ship** - repo with polished docs, a risk register or gap matrix, and an executive summary.
for GRC, the writing quality is the skill being demonstrated.
the executive summary is the writeup here: it should explain the risk story in plain language, not just attach a spreadsheet.

**measurable gate:** at least 3 assets/risks or 5 control gaps are documented, each with owner, evidence, remediation, and status.

**can u explain it?** ✅ - explain one risk from asset -> threat -> vulnerability -> impact -> control -> evidence -> residual risk.

---

## resume + ATS targeting meow (~12h)

**the idea** - dont write one generic resume and pray.
for each role type, map the words in the role description to the projects and certs that prove u can do that work.

**how/why it actually works** - an Applicant Tracking System (ATS) often parses resumes before a human reads them.
it matches tokens from the role description against your resume: tools, certs, frameworks, task verbs, and acronyms.
if the description says `SIEM`, `EDR`, `MITRE ATT&CK`, `Splunk`, `KQL`, and `incident response`, those terms need to appear **in context** on your resume.
not as a fake keyword pile.
as proof-linked bullets.

the reusable engine is the **NICE Framework**.
NICE work-role Task/Knowledge/Skill statements are the vocabulary job descriptions are built from.
so the loop is:

1. **pull nouns + verbs** - highlight tools, frameworks, certs, and task verbs in the role description.
2. **match each to proof** - Project 2 for SIEM triage, Project 3 for detection engineering, Project 6 for incident reporting, Project 8 for GRC.
3. **phrase the bullet in NICE/JD language and quantify it** - "Wrote 5 Sigma detection rules mapped to MITRE ATT&CK and converted one to Splunk SPL" beats "worked on detections."

**words u gotta be able to say**

- **ATS** - parser matching resume text to role text
- **keyword** - tool, framework, cert, noun, or task verb
- **NICE work role** - standardized cyber role definition
- **Task / Knowledge / Skill** - work actions, concepts, abilities
- **proof-linked bullet** - resume line tied to evidence
- **quantified bullet** - number, scope, or outcome included

**study sources (pick what fits your style)**

- [NICE Framework - Work Role Search](https://niccs.cisa.gov/workforce-development/cyber-security-workforce-framework/workroles) - role taxonomy for decoding what a cyber role actually is. **free**; may bot-block some automated fetches, but alive.
- [NICE - Defensive Cybersecurity work role](https://niccs.cisa.gov/tools/nice-framework/work-role/defensive-cybersecurity) - SOC-style task language: validate alerts, analyze anomalies, document incidents, escalate. **free**
- [NICE - Digital Forensics work role](https://niccs.cisa.gov/tools/nice-framework/work-role/digital-forensics) - DFIR-leaning task language for evidence, artifacts, and investigations. **free**
- [Google Technical Writing One](https://developers.google.com/tech-writing/one) - make bullets shorter, clearer, and easier to parse. **free**

**do this** - build one master resume, then make a targeted version for each role type u apply to.
use this loop per application:

1. copy the role description into your notes.
2. highlight tools, frameworks, certs, and task verbs.
3. open the closest NICE work role.
4. map each major keyword to one project/cert/lab u actually have.
5. rewrite bullets so the wording matches the role without lying.

**example bullets**

- Built a Wazuh SIEM monitoring 3 endpoints; wrote and tuned 5 custom detection rules mapped to MITRE ATT&CK.
- Investigated a simulated intrusion in Splunk BOTS v3; produced timeline, IOCs, ATT&CK mapping, and remediation notes.
- Authored 5 Sigma detection rules with false-positive notes; converted one rule to Splunk SPL using `sigma-cli`.
- Completed a NIST SP 800-30 style risk assessment for 3 assets and mapped 5 controls to NIST CSF 2.0.

**ATS hygiene**

- use standard headings: `Experience`, `Projects`, `Certifications`, `Skills`, `Education`.
- keep it single-column; avoid tables, text boxes, images, and icons for core content.
- spell out acronyms once: `Security Information and Event Management (SIEM)`.
- use a text-based PDF or `.docx`, not a flattened scan.
- one page for entry level.
- lead with certs + projects if u dont have security job experience yet.
- link GitHub and your writeup/blog landing page.

**resume-resource note:** im not linking a random "security resume template" here because no free resume guide met the guide's exact verification bar for this rewrite.
use NICE for the vocabulary and Google Technical Writing for clarity.
thats stronger than a weak template anyway meow.

**measurable gate:** for 3 target role descriptions from company-direct pages, u have a targeted resume version where every major keyword maps to a truthful project, cert, or lab.

**can u explain it?** ✅ - pick any resume bullet and point to the artifact that proves it.
then say which NICE task it maps to and which role keyword it answers.

---

## role targeting without getting lost meow (~12h)

**the idea** - dont start with a board.
start with the work role, then the employer type, then the company, then the opening.

**how/why it actually works** - entry security roles have messy titles.
one company says SOC Analyst I, another says Security Monitoring Analyst, another says IT Security Technician.
the title changes, but the work-role tasks repeat: validate alerts, analyze logs, document incidents, escalate, tune detections, review access, collect evidence.

NICE gives the role dictionary.
[CyberSeek Career Pathway](https://www.cyberseek.org/pathway.html) gives the feeder-role map: help desk, NOC, sysadmin, networking, software, risk, and intelligence roles can feed into entry cyber roles.
CyberSeek has a US pay overlay; use the role map and skills, **ignore the numbers**.

that on-ramp matters because SOC work assumes u know normal IT.
u need to tell normal from abuse:

- normal password reset vs account takeover.
- normal DNS lookup vs weird beaconing.
- normal patch reboot vs suspicious service creation.
- user error vs actual incident.

help desk, NOC, and sysadmin work build that baseline.
NOC -> SOC is especially natural: both monitor alerts, triage, escalate, and document.
the difference is availability signals vs security signals.
same workflow, sharper threat model.

**words u gotta be able to say**

- **work-role taxonomy** - standardized map of job types
- **feeder role** - adjacent job that builds baseline experience
- **on-ramp** - realistic path into security work
- **MSSP / MDR** - managed provider handling client security
- **internal SOC** - security team inside one organization
- **company-direct** - applying through employer careers pages
- **referral** - warm intro from someone inside

**entry titles to search for**

- SOC Analyst I / Tier 1 SOC Analyst
- Junior Security Analyst / Associate Security Analyst
- Cybersecurity Analyst I
- Security Monitoring Analyst
- Junior Incident Responder
- IAM Analyst
- Vulnerability Management Analyst
- Associate GRC Analyst / Compliance Analyst
- IT Security Technician / Security Support Specialist
- NOC Analyst, Help Desk Analyst, IT Support Specialist, or Junior Sysadmin if u need the on-ramp first

**employer types that hire juniors**

| Employer type | why it hires juniors | reality check |
|---|---|---|
| **MSSP / MDR providers** | high-volume junior door; structured SOC training; many client environments | high tempo, sometimes shift work, but fast reps |
| **Large internal SOC** | regulated or large orgs need steady monitoring and response | slower process; may prefer prior IT |
| **Consulting / professional services** | graduate, associate, and cyber-track programs | competitive; degree-friendly, not always degree-only |
| **Gov / defense / contractor** | often a major entry employer in a country | citizenship or clearance gates may apply |
| **Internal IT -> security** | already inside the org, already know systems and people | best probability path for many career-switchers |
| **GRC / risk / compliance teams** | need people who can write, gather evidence, and map controls | less hands-on hacking; strong door if u communicate well |

**how to find the actual openings, board-free**

1. **search by title, not by board** - use the title list above on the dominant professional network and search engine in your country.
2. **go company-direct** - make a list of 15-20 target employers from the types above and check their careers pages directly.
3. **use NICE to decode weird titles** - if the tasks match Defensive Cybersecurity, Digital Forensics, IAM, or Risk Management, the title matters less.
4. **tap communities -> referrals** - local chapters, BSides, OWASP, DEF CON groups, Discords, and subreddits can point u to teams and warm intros. use [resources.md](resources.md) for community starting points.
5. **build relationships before u ask** - project writeups are a reason to connect: "i wrote this Wazuh detection, would love feedback" is better than "can u get me a job."

**do this** - build a target tracker with:

- 15-20 employers grouped by type.
- 3 role descriptions copied from company-direct careers pages.
- the NICE work role each description resembles.
- which portfolio project proves each major requirement.
- one community or referral path for each top employer, if available.

**measurable gate:** tracker has 15-20 employers, 3 company-direct role descriptions, NICE role mapping, and project-to-requirement mapping.

**can u explain it?** ✅ - explain why your first target is SOC, GRC, cloud, red, or an IT/NOC on-ramp.
then explain how your current projects prove the tasks in that role.

---

## interview prep meow (~8h)

**the idea** - interviews are mostly "can u reason out loud without pretending."
your projects are the script.

**how/why it actually works** - technical interviews test mechanisms, not trivia.
behavioral interviews test whether u can communicate under uncertainty.
if every portfolio project has a writeup, u already have the raw material for both.

use the full [Interview Prep Q&A bank](interview-prep.md), then rehearse these quick hits:

- explain the OSI model and one attack at each layer.
- walk a phishing investigation from alert to close.
- IDS vs IPS - when would u use each?
- what is SQL injection, and how do u prevent it?
- u get a SIEM alert for 10,000 failed logins - walk triage.
- symmetric vs asymmetric encryption, with a use case.
- what is CVSS, and how do u prioritize patching?

**project stories to prepare**

- **technical story:** "here is what i built, here is the mechanism, here is the evidence."
- **failure story:** "here is what broke, how i debugged it, and what i changed."
- **communication story:** "here is how i explained a technical risk to a non-technical person."
- **learning story:** "here is how i got unstuck without copying an answer."

**do this** - make a one-page interview sheet with:

- 3 project stories.
- 2 technical concepts u can whiteboard.
- 2 STAR behavioral answers.
- 5 questions to ask the interviewer about training, alert volume, tooling, and escalation process.

**measurable gate:** u can answer 10 technical questions from [interview-prep.md](interview-prep.md) and tell 3 project stories in under 2 minutes each.

**can u explain it?** ✅ - pick your strongest project and explain it to two audiences: a SOC analyst and a non-technical manager.
same facts, different language.

---

## honest hiring reality meow

entry is competitive.
the big "unfilled jobs" headline usually means experienced people, not "any cert-only beginner can walk in tomorrow."

certs help, but certs alone are thin.
what separates u is:

- a demonstrable home lab.
- documented projects.
- scripting ability.
- cloud fundamentals.
- clear writing.
- proof u can tell normal from suspicious.

the path that works most often is still:

**Help Desk / IT Support / NOC / Junior Sysadmin -> SOC Analyst**

or:

**degree/internship -> junior security role**

direct cert-only entry can happen, but its harder.
dont build your plan around the hardest door if another door gets u real experience sooner.

GRC is also a real entry path.
if u write clearly, think in evidence, and can map controls to risk, dont ignore it.
its not "less security."
its the layer that turns technical work into decisions mhm.

---

## verified resource shelf meow

these are the exact resources this file relies on, checked in the R10 research pass on 2026-07-02.

| Resource | Use | Tag |
|---|---|---|
| [TCM Security Sample Pentest Report](https://github.com/hmaverickadams/TCM-Security-Sample-Pentest-Report) | report structure for Projects 4/6/7/8 | **free** |
| [TCM - How to Write a Pentest Report](https://www.youtube.com/watch?v=EOoBAq6z4Zk) | specific report-writing walkthrough | **free** |
| [0xdf HTB writeups](https://0xdf.gitlab.io/) | writeup structure model | **free** |
| [SigmaHQ - Rule Creation Guide](https://github.com/SigmaHQ/sigma/wiki/Rule-Creation-Guide) | author Sigma detection rules | **free** |
| [Sigma - Getting Started](https://sigmahq.io/docs/guide/getting-started.html) | install `sigma-cli` and convert rules | **free** |
| [Google Technical Writing One](https://developers.google.com/tech-writing/one) | clearer READMEs, writeups, and resumes | **free** |
| [NICE Framework - Work Role Search](https://niccs.cisa.gov/workforce-development/cyber-security-workforce-framework/workroles) | region-agnostic role taxonomy | **free**; may bot-block automated fetches |
| [NICE - Defensive Cybersecurity](https://niccs.cisa.gov/tools/nice-framework/work-role/defensive-cybersecurity) | SOC task/keyword engine | **free** |
| [NICE - Digital Forensics](https://niccs.cisa.gov/tools/nice-framework/work-role/digital-forensics) | DFIR task/keyword engine | **free** |
| [CyberSeek Career Pathway](https://www.cyberseek.org/pathway.html) | feeder-role and transition map | **free**; ignore its US pay overlay |
| [GitHub Docs - Managing your profile README](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme) | profile landing-page setup | **free** |
| [GOAD - Game of Active Directory](https://github.com/Orange-Cyberdefense/GOAD) | AD attack+detect showpiece | **free** |
| [Wazuh Quickstart](https://documentation.wazuh.com/current/quickstart.html) | home SOC setup | **free** |
| [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) | technique coverage mapping | **free** |
| [SigmaHQ/sigma](https://github.com/SigmaHQ/sigma) | real Sigma rules and optional PR target | **free** |
| [Splunk Boss of the SOC v3 dataset](https://github.com/splunk/botsv3) | SOC investigation dataset | **free** |
| [DetectionLab](https://github.com/clong/DetectionLab) | optional AD/logging lab alternative | **free**, stale; prefer GOAD |

---

## exit check - done with Goal 5

- [ ] u pinned 4-6 strong repos, not every repo u have.
- [ ] every pinned repo has a security-impact line, evidence, and a writeup.
- [ ] at least one project is the AD attack+detect showpiece, or u have a clear reason it comes next.
- [ ] u have one targeted resume version for each role type u are applying to.
- [ ] each major resume bullet points to proof: repo, writeup, cert, lab, or report.
- [ ] u built a 15-20 employer target tracker by employer type, not by job-board scrolling.
- [ ] u mapped 3 real role descriptions to NICE work roles and your projects.
- [ ] u prepared 3 project stories and can tell each in under 2 minutes.
- [ ] u can explain your target path: direct SOC/GRC/cloud, or help-desk/NOC/IT -> SOC.

**final can u explain it?** - unaided, tell this story:

> "this is the role type im targeting, here is the NICE work-role language it maps to, here is the employer type im starting with, here are the 4-6 artifacts that prove i can do the tasks, and here is why my on-ramp makes sense."

if u can say that without hiding behind buzzwords, u are no longer "just studying."
u have evidence.
now keep applying, keep writing, and keep improving the artifacts as u learn meow.

---

[<- Goal 4: Specialization](04-specialization.md) | [Back to hub](README.md) | [Beyond Entry-Level ->](beyond-entry.md)
