# beyond entry-level meow (years 2+)

once u land the first role and get 1-2 years of real incidents, tickets, alerts, users, audits, or production systems under your hands, the game changes.

entry-level is about proving u can learn and do the basics.
mid-level is about owning a lane deeply enough that other people trust your judgment qwq.

[<- Goal 5: Portfolio & Job Hunt](05-job-hunt.md) | [Hub](README.md) | [Certifications](certifications.md)

> [!WARNING]
> **dont cert-chase.**
> do not pay for a pile of advanced certs with your own money just because they sound serious.
> go deep in one path, build real work evidence, and let your employer sponsor the expensive stuff whenever possible.

---

## the years-2+ todo-tree

- [ ] **pick one depth lane** - blue/IR, red/pentest, cloud security, or GRC/management.
- [ ] **build work evidence inside that lane** - detections, incident reports, pentest reports, cloud remediation, risk/control artifacts.
- [ ] **choose one advanced cert only if it matches your job** - cert after skill, not before.
- [ ] **teach or document what u learned** - internal runbook, public writeup, brown-bag talk, detection repo, control mapping.

the checkbox is still just display.
the real gate is: can u point to work evidence and explain the judgment behind it?

---

## 1. blue team / incident response

**where this goes:** Tier 2/3 SOC, detection engineering, threat hunting, DFIR, incident response.

**skills to deepen**

- advanced scripting with Python, PowerShell, and Bash for repeatable IR work.
- detection engineering: Sigma, YARA, KQL/SPL, false-positive tuning, detections-as-code in Git.
- enterprise identity and endpoint architecture: Entra ID, Conditional Access, EDR, network segmentation.
- incident command: timeline, containment decision, stakeholder update, lessons learned.

**specific resources + optional checkpoints**

- [Centri - Blue Team Level 2](https://www.centri.org/certifications/blue-team-level-2) - advanced blue-team training/cert covering malware analysis, threat hunting, vulnerability management, advanced SIEM, and emulation. **paid; employer-sponsor if possible**
- [GIAC GCIH](https://www.giac.org/certifications/certified-incident-handler-gcih) - incident handling, attacker techniques, detection/response. **paid/expensive**
- [GIAC GCFA](https://www.giac.org/certifications/certified-forensic-analyst-gcfa) - deeper forensics and advanced incident investigations. **paid/expensive**
- [GIAC CyberLive](https://www.giac.org/cyberlive) - GIACs hands-on VM-based testing format. useful context before spending money.
- [Microsoft SC-200 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-200) - worth it if your shop runs Microsoft Sentinel / Defender XDR.

**can u explain it?** ✅ - walk one real or lab incident from first alert -> evidence -> timeline -> containment -> eradication -> recovery -> detection improvement.
if u cant say why u contained that way, keep building reps.

---

## 2. red team / penetration testing

**where this goes:** internal pentest, consulting, red team, adversary emulation.

**skills to deepen**

- Active Directory / Entra ID attacks: Kerberoasting, AS-REP roasting, Pass-the-Hash, token abuse, ACL paths.
- deep privilege escalation, DLL hijacking, service exploitation, pivoting, tunneling.
- web app depth beyond OWASP basics: auth logic, SSRF, deserialization, business logic flaws.
- report writing and live debriefs. the report is the product, not the afterthought meow.

**specific resources + optional checkpoints**

- [OffSec PEN-200 / OSCP](https://www.offsec.com/courses/pen-200/) - the classic pentest filter; do it after the red-chain in Goal 4 feels normal. **paid/expensive**
- [OffSec Learn One](https://www.offsec.com/products/learn-one/) - current subscription-style training bundle; compare before buying.
- [TCM PNPT](https://certifications.tcm-sec.com/pnpt/) - AD-focused practical with report and live debrief. **paid**
- [HTB Academy Penetration Tester path](https://academy.hackthebox.com/path/preview/penetration-tester) - CPTS-aligned technical depth path.
- [HTB CPTS certification preview](https://academy.hackthebox.com/preview/certifications/htb-certified-penetration-testing-specialist/) - broad practical pentest cert with report component.

**can u explain it?** ✅ - take one compromise chain and narrate it like a consultant:
scope -> recon -> foothold -> privilege escalation -> lateral movement -> impact -> prioritized remediation.
if u can hack it but cant explain the fix, ur not done yet qwq.

---

## 3. cloud security architecture

**where this goes:** cloud security engineer, cloud detection engineer, platform security, DevSecOps, security architecture.

**skills to deepen**

- IaC security: scan Terraform/CloudFormation with Checkov, Trivy, tfsec-style tooling before deploy.
- IAM at scale: SCPs, cross-account roles, PIM, service principals, workload identities, permission boundaries.
- cloud detection: CloudTrail/GuardDuty/Security Hub, Sentinel/Defender, logs -> alert -> response.
- DevSecOps: embed scans in GitHub Actions/GitLab CI and turn findings into fixable tickets.

**specific resources + optional checkpoints**

- [AWS Certified Security - Specialty](https://aws.amazon.com/certification/certified-security-specialty/) - current AWS security-specialty landing page.
- [AWS SCS-C03 official exam guide](https://docs.aws.amazon.com/aws-certification/latest/security-specialty-03/security-specialty-03.html) - use this, not stale SCS-C02 PDFs.
- [AWS Skill Builder Security Specialty exam-prep plan](https://skillbuilder.aws/exam-prep/security-specialty) - official prep/practice path.
- [Microsoft SC-500 certification page](https://learn.microsoft.com/en-us/credentials/certifications/cloud-and-ai-security-engineer-associate/) - Azure/AI cloud security successor path.
- [Microsoft SC-500 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/sc-500) - current SC-500 objective map.
- [ISC2 CCSP](https://www.isc2.org/certifications/ccsp) - vendor-neutral cloud-security cert; requires real experience to hold.
- [CCSP exam outline](https://www.isc2.org/certifications/ccsp/ccsp-certification-exam-outline) - check domains and experience requirements before planning it.
- [CCSP experience requirements](https://www.isc2.org/certifications/ccsp/ccsp-experience-requirements) - confirms the work-experience gate.

**heads up:** **AZ-500 retires August 31, 2026.**
if youre starting Azure security now, point at **SC-500**, not AZ-500.

**can u explain it?** ✅ - explain one cloud finding from API evidence -> risk -> exact config fix -> re-scan proof.
bonus: say how the same control differs between AWS IAM and Entra/Azure RBAC.

---

## 4. GRC, audit, and security management

**where this goes:** GRC analyst -> risk lead, auditor, security program manager, control owner, security manager.

**skills to deepen**

- risk frameworks: NIST SP 800-30, NIST CSF 2.0, ISO 27001, CIS Controls.
- regulatory and assurance work: SOC 2, PCI DSS, GDPR, NIS2, DORA where relevant.
- third-party risk: questionnaires, SOC 2 report review, evidence requests, remediation tracking.
- translating technical risk into business decisions without watering it down.

**specific resources + optional checkpoints**

- [ISACA CISA](https://www.isaca.org/credentialing/cisa) - audit-focused credential. not entry-level; experience-gated.
- [CISA certification requirements](https://www.isaca.org/credentialing/cisa/get-cisa-certified) - check the five-year experience rule before planning it.
- [ISACA CISM](https://www.isaca.org/credentialing/cism) - security management credential. not entry-level; experience-gated.
- [CISM certification requirements](https://www.isaca.org/credentialing/cism/get-cism-certified) - check the work-experience rule before planning it.
- [ISC2 CISSP experience requirements](https://www.isc2.org/certifications/cissp/cissp-experience-requirements) - senior generalist credential; requires five years across two or more CISSP domains.
- [NIST CSF 2.0 Reference Tool](https://csrc.nist.gov/projects/cybersecurity-framework/filters) - keep using this for real control mapping.
- [NIST SP 800-30 Rev. 1](https://csrc.nist.gov/pubs/sp/800/30/r1/final) - risk-assessment method.

**can u explain it?** ✅ - take one technical finding and translate it into:
asset -> threat -> vulnerability -> likelihood -> impact -> control -> evidence -> residual risk -> decision.
thats the GRC muscle mhm.

---

## the principle

pick **one** track for depth.
go deep enough that your work artifacts show judgment, rather than only tools.

advanced certs should answer a real question:

- "my job uses this stack."
- "my employer will sponsor it."
- "this cert unlocks a specific role i am already close to."
- "the exam forces a practical skill i need anyway."

if none of those are true, keep building and documenting.
depth beats a wall of unrelated credentials meow.
