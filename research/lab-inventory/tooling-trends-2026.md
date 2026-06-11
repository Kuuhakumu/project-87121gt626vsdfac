# Cybersecurity Tooling & Trends — 2026 (What to Teach vs Cut)

> Research date: 2026-06-13. Framework versions curl-verified against official sources.

## Verified Framework Versions
| Framework | Version | Source |
|---|---|---|
| MITRE ATT&CK | v19.1 | attack.mitre.org |
| NIST CSF | 2.0 (Feb 2024; adds "Govern") | nist.gov/cyberframework |
| OWASP Top 10 (Web) | 2025 | owasp.org/www-project-top-ten |
| OWASP LLM Top 10 | 2025 (LLM01–LLM10:2025) | genai.owasp.org |
| ISO/IEC 27001 | 2022 | iso.org |
| NIS2 Directive | In force (EU, Oct 2024 transposition) | enisa.europa.eu |
| Sigma | release cadence r2026-xx | github.com/SigmaHQ/sigma |
| Wazuh | 4.9.x | wazuh.com |

## SIEM
- **Teach:** Microsoft Sentinel (KQL) — dominant enterprise hiring; Splunk (SPL) — industry vocabulary; Wazuh — free home-lab SIEM/XDR (best zero-cost hands-on).
- **Differentiator:** Google SecOps/Chronicle (YARA-L), Elastic Security (EQL).
- **De-emphasize:** IBM QRadar (declining, rare in entry postings).

## EDR/XDR (analysts triage, not configure)
- **Teach conceptually:** Microsoft Defender XDR (free trial tenant = only realistic free lab), CrowdStrike Falcon, SentinelOne.
- **Core skills regardless of vendor:** process-tree analysis, lateral-movement indicators (PsExec/WMI/RDP), LOLBins (certutil/mshta/wscript), behavioral vs signature detection.

## AI in Security
- **Baseline:** AI-assisted SOC triage is table stakes (Security Copilot, Charlotte AI, Purple AI) — know conceptually; OWASP LLM Top 10 2025, esp. LLM01 Prompt Injection, LLM06 Excessive Agency, LLM02 Sensitive Info Disclosure.
- **Differentiator:** LLM red-teaming, adversarial ML (specialist).

## Cloud Security — now BASELINE, not differentiator
- Shared responsibility model; IAM least privilege (roles vs users, service accounts, overprivileged identities); cloud alert triage (CloudTrail / Azure Activity Log / GCP Audit Logs — watch CreateUser, AttachPolicy, GetSecretValue anomalies); misconfigs (public S3, open security groups).
- Teach ONE platform deep (Azure recommended for Sentinel/Defender synergy; AWS close second). Free labs: AWS Free Tier, Azure free account, CloudGoat, flaws.cloud, flaws2.cloud.

## Detection Engineering (growth path; teach concepts)
- Sigma rule literacy (YAML structure, platform-agnostic, maps to ATT&CK techniques) — reading > authoring at entry.
- YARA (malware pattern matching) — brief mention.
- Detection-as-code (version-controlled detections, CI/CD validation) — "where the industry is heading".

## Emerging (brief sections)
- Container/K8s security: Trivy (image scan, free), Falco (runtime, OSS).
- IaC scanning: Checkov (shift-left, free) on Terraform/CFN/K8s.
- Supply chain / SBOM: Syft (generate SBOM), Grype (scan); Log4Shell as motivating example; SBOM now US federal requirement.
- OT/ICS: Purdue Model, MITRE ATT&CK for ICS — only if guide targets that audience.

## CUT or De-emphasize (signals outdated curriculum)
- Snort rule-authoring as primary IDS skill (cover IDS/IPS conceptually; Suricata > Snort in deployments).
- Hash-based (MD5/SHA1) IOC hunting as primary method — teach behavioral/TTP hunting.
- "AV catches malware" mental model — teach EDR/behavioral, AV as one defense-in-depth layer.
- CEH as top cert recommendation.
- On-prem-only Active Directory — teach hybrid Entra ID (Connect sync, Conditional Access, PIM).
- IBM QRadar deep-dives.
- Long Kali tool-list memorization — teach methodology + 3–5 tools well.
- OWASP Top 10 2021 as "current" — use 2025.
- Perimeter-only thinking — assume breach / Zero Trust.
