# Cloud & DevOps Certification Analysis — 2026

> Research date: 2026-06-13. Verified via `curl` against official sources. Confidence: ✅ VERIFIED (curl 200, data in page) · ⚠️ PARTIAL (page live, data JS-rendered) · ⛔ UNVERIFIED (blocked).

## Cert data sheet

| Cert | Code | Price | Format | Pass | Validity | Conf |
|---|---|---|---|---|---|---|
| AWS Cloud Practitioner | CLF-C02 | $100 | 65 MCQ, 90m | 700/1000 | 3 yr | ✅ |
| AWS Solutions Architect Associate | SAA-C03 | $150 | 65 MCQ, 130m | 720/1000 | 3 yr | ✅ |
| AWS Developer Associate | DVA-C02 | $150 | 65 MCQ, 130m | 720/1000 | 3 yr | ✅ |
| AWS SysOps Associate | SOA-C02 | $150 | 65 MCQ, 130m | 720/1000 | 3 yr | ✅ |
| AWS DevOps Engineer Pro | DOP-C02 | $300 | 75 MCQ, 180m | 750/1000 | 3 yr | ✅ |
| Azure Fundamentals | AZ-900 | ~$165 | ~45 MCQ, 45-60m | 700/1000 | No expiry | ✅ |
| Azure Administrator | AZ-104 | ~$165 | MCQ+case, 100m | 700/1000 | 1 yr free renew | ✅ |
| Azure Developer | AZ-204 | ~$165 | MCQ+case | 700/1000 | **RETIRING Jul 2026** | ✅ |
| Azure DevOps Engineer | AZ-400 | ~$165 | MCQ+case | 700/1000 | **retirement flagged** | ✅ |
| GCP Cloud Digital Leader | CDL | $99 | MCQ, 90m | pass/fail | 3 yr | ✅ |
| GCP Associate Cloud Engineer | ACE | $200 | MCQ, 120m | pass/fail | 3 yr | ✅ |
| HashiCorp Terraform Associate | TA-004 | $70.50 | ~57 MCQ, 60m | ~70% | 2 yr | ✅ |
| CNCF KCNA | KCNA | $250 | MCQ | 75% | 2 yr | ✅ |
| CNCF CKAD | CKAD | $445 | performance-based | 66% | 2 yr | ✅ |
| CNCF CKA | CKA | $445 | performance-based | 66% | 2 yr | ✅ |
| CNCF CKS | CKS | $445 | performance, **CKA req** | 67% | 2 yr | ✅ |
| CompTIA Linux+ | XK0-006 | ~$370 | MCQ+PBQ | 720/900 | 3 yr CE | ⚠️ |
| CompTIA Cloud+ | CV0-004 | ~$370 | MCQ+PBQ | 750/900 | 3 yr CE | ⚠️ |
| Docker DCA | — | — | **DISCONTINUED** | — | — | ✅ (absent) |

Notes: AWS scaled 100-1000. CKA/CKAD/CKS are live-cluster performance exams (kubectl in browser) — high signal, can't fake. CKA+CKAD bundle saves ~$100. Azure uses annual FREE online renewal. Terraform 003→004 (003 retired; 003 URL now redirects to 004). OpenTofu fork has NO cert yet.

## Employer-signal ranking (entry-level cloud/devops)

🔴 **Baseline filter:** AWS SAA-C03 (de facto bar in AWS shops) · AZ-900 (Azure track) · AWS CLF-C02 (logical first step)
🟠 **Strong differentiator:** CKA (performance-based, high signal) · Terraform Associate ($70, IaC fluency) · CKAD · GCP ACE · AZ-104
🟡 **Nice-to-have:** AWS DVA-C02 · GCP CDL · KCNA (stepping stone) · CompTIA Linux+/Cloud+
⛔ **Skip (entry):** AWS SOA (overlaps SAA) · AWS DOP (pro tier, premature) · AZ-204 (retiring) · AZ-400 (flagged) · CKS (needs CKA, niche) · Docker DCA (dead)

> Cloud/DevOps is far more cert-friendly than pure SWE — certs are a genuine resume filter here.

## Recommended paths

**Cheapest → first job (~$320, 3-5 mo):** AWS CLF-C02 ($100) → Terraform Associate ($70) → AWS SAA-C03 ($150).
**AWS-focused (~$400):** CLF-C02 → SAA-C03 → Terraform Assoc → DVA-C02 (dev) or SOA-C02 (ops).
**Azure-focused (~$330):** AZ-900 → AZ-104 → Terraform Associate. (Avoid AZ-204/AZ-400.)
**Kubernetes/platform (~$645):** CLF-C02 → (KCNA optional) → CKAD → CKA (buy CKA+CKAD bundle) → + Terraform Assoc.

## What's dated in a 2021-era list

| 2021 | 2026 |
|---|---|
| AWS CLF-C01 / SAA-C02 / DVA-C01 | → CLF-C02 / SAA-C03 / DVA-C02 |
| Terraform Associate 002 | → 003 |
| CompTIA Linux+ XK0-005 / Cloud+ CV0-003 | → XK0-006 / CV0-004 |
| Docker DCA | **discontinued** |
| AZ-204 | **retiring Jul 2026** |
| AZ-400 | retirement flagged |
| no K8s fundamentals cert | KCNA added (~2022) |
| Terraform = only IaC | OpenTofu fork exists (no cert yet) |

Sources: aws.amazon.com/certification/*, learn.microsoft.com/credentials/*, cloud.google.com/learn/certification/*, developer.hashicorp.com/certifications, training.linuxfoundation.org/certification/*, comptia.org — curl-verified 2026-06-13. AZ-204 retirement + Docker DCA absence confirmed.
