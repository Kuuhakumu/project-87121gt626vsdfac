# Certification guide - Cloud & DevOps meow

> verified via official sources, June 2026.
> prices in USD; confirm on the official site before booking bc codes and prices shift.

[Hub](README.md)

---

- [ ] **know what to actually get**
- [ ] **use the cert data sheet**
- [ ] **rank employer signal**
- [ ] **pick a recommended path**
- [ ] **avoid dated cert advice**

## what to actually get

- **certs matter more here than in software dev.** AWS Solutions Architect Associate is a real ATS filter for cloud roles.
- **start cheap:** AWS **Cloud Practitioner (CLF-C02, $100)** -> **Solutions Architect Associate (SAA-C03, $150)**.
- **top differentiators:** **Terraform Associate ($70)** and **CKA ($395, hands-on)**.
- **do not pursue AZ-204** - retiring **July 2026**. **AZ-400** retirement is flagged. **Docker DCA** is discontinued.
- **hands-on beats cert-stacking.** a reproducible IaC project beats a 4th cert.

## cert data sheet

| Cert | Code | Price | Format | Pass | Valid | Status |
|---|---|---|---|---|---|---|
| AWS Cloud Practitioner | CLF-C02 | $100 | 65 MCQ, 90m | 700/1000 | 3 yr | verified |
| AWS Solutions Architect Assoc. | SAA-C03 | $150 | 65 MCQ, 130m | 720/1000 | 3 yr | verified |
| AWS Developer Assoc. | DVA-C02 | $150 | 65 MCQ, 130m | 720/1000 | 3 yr | verified |
| AWS SysOps Admin Assoc. | SOA-C02 | $150 | 65 MCQ, 130m | 720/1000 | 3 yr | verified |
| AWS DevOps Engineer Pro | DOP-C02 | $300 | 75 MCQ, 180m | 750/1000 | 3 yr | verified |
| Azure Fundamentals | AZ-900 | ~$165 | ~45 MCQ, 45-60m | 700/1000 | no expiry | verified |
| Azure Administrator Assoc. | AZ-104 | ~$165 | MCQ+case, 100m | 700/1000 | 1 yr free renew | verified |
| Azure Developer Assoc. | AZ-204 | ~$165 | MCQ+case | 700/1000 | **retiring Jul 2026** | verified |
| Azure DevOps Engineer Expert | AZ-400 | ~$165 | MCQ+case | 700/1000 | **retirement flagged** | verified |
| GCP Cloud Digital Leader | CDL | $99 | ~50-60 MCQ, 90m | pass/fail | 3 yr | verified |
| GCP Associate Cloud Engineer | ACE | $200 | ~50-60 MCQ, 120m | pass/fail | 3 yr | verified |
| HashiCorp Terraform Associate | TA-004 | $70.50 | ~57 MCQ, 60m | ~70% | 2 yr | verified |
| CNCF KCNA | KCNA | $250 | MCQ | 75% | 2 yr | verified |
| CNCF CKAD | CKAD | $395 | hands-on | 66% | 2 yr | verified |
| CNCF CKA | CKA | $395 | hands-on | 66% | 2 yr | verified |
| CNCF CKS | CKS | $395 | hands-on | 67% | 2 yr | verified |
| CompTIA Linux+ | XK0-006 | ~$370 | MCQ+PBQ, 90m | 720/900 | 3 yr CE | partial |
| CompTIA Cloud+ | CV0-004 | ~$370 | MCQ+PBQ, 90m | 750/900 | 3 yr CE | partial |
| Docker DCA | - | - | **discontinued** | - | - | verified |

AWS/GCP associate certs recommend experience but dont require it. CKA/CKAD/CKS are performance-based, so passing one proves u can work in a live cluster.

## employer signal ranking

### baseline filter

- [ ] **AWS SAA-C03** - de facto entry bar for AWS roles.
- [ ] **AZ-900** - Azure baseline.
- [ ] **AWS CLF-C02** - cheap logical first step.

### strong differentiator

- [ ] **CKA** - hands-on and hard to fake.
- [ ] **Terraform Associate** - IaC fluency for low cost.
- [ ] **CKAD** - app-platform/SRE signal.
- [ ] **GCP ACE** - less saturated market.
- [ ] **AZ-104** - Azure beyond support.

### nice-to-have

- [ ] **AWS DVA-C02**
- [ ] **GCP CDL**
- [ ] **KCNA**
- [ ] **CompTIA Linux+/Cloud+** in gov/MSP/consulting markets

### skip for entry-level

- [ ] **AWS SOA-C02** if it overlaps too much with SAA for your path
- [ ] **AWS DOP-C02** before real experience
- [ ] **CKS** before CKA
- [ ] **AZ-204**
- [ ] **AZ-400**
- [ ] **Docker DCA**

## recommended paths

- [ ] **cheapest -> first job (~$320, 3-5 mo):** `CLF-C02` -> `Terraform Associate` -> `SAA-C03`
- [ ] **AWS-focused (~$400):** `CLF-C02` -> `SAA-C03` -> `Terraform Associate` -> `DVA-C02` or `SOA-C02`
- [ ] **Azure-focused (~$330):** `AZ-900` -> `AZ-104` -> `Terraform Associate`
- [ ] **Kubernetes / platform (~$645):** `CLF-C02` -> optional `KCNA` -> `CKAD` -> `CKA`, then Terraform Associate

## whats dated in old lists

| Outdated | 2026 reality |
|---|---|
| AWS CLF-C01 / SA-C02 / DVA-C01 | CLF-C02 / SAA-C03 / DVA-C02 |
| Terraform Associate 002/003 | TA-004 |
| CompTIA Linux+ XK0-005 / Cloud+ CV0-003 | XK0-006 / CV0-004 |
| Docker DCA | discontinued |
| AZ-204 | retiring July 2026 |
| AZ-400 | retirement flagged |
| no K8s fundamentals cert | KCNA exists |
| Terraform as only IaC option | OpenTofu exists; no cert yet |

---

*Sources: official cert pages, curl-verified June 13, 2026. Raw findings in `research/cert-analysis/cloud-devops-2026.md`.*
