# 🚀 Beyond Entry-Level — Years 2+

> You're hired into your first data role. This is the map for what comes next — how the analyst/AE entry door opens into the rest of the field.

[← Job Hunt](05-job-hunt.md) · [Hub](README.md)

---

## The honest progression

```
Data / BI Analyst  ──┐
Analytics Engineer ──┼──► Senior Analyst / Senior AE
                     │         ↓
                     ├──► Data Engineer ──► Senior DE ──► Data Architect / Platform
                     │
                     └──► Data Scientist ──► Senior DS ──► ML Engineer / Applied Scientist
                                                ↓
                                         Data / Analytics Lead → Manager
```

Most people come in as an **Analyst** or **Analytics Engineer** and branch after 1–2 years once they know which problems they enjoy: pipelines (→ DE), modeling (→ DS), or the business side (→ analytics lead).

---

## Track-by-track: what "senior" adds

### Analyst → Senior Analyst / Analytics Lead
- Owning a metric/domain end-to-end, not just answering tickets
- Defining metrics and a "single source of truth" others rely on
- Mentoring juniors, influencing product/business decisions
- Experiment design (running A/B tests, not just reading them)

### Analytics Engineer → Senior AE
- Data modeling at scale: semantic layers, large dbt projects, performance tuning
- Owning data quality, testing strategy, and CI/CD for the warehouse
- Cost optimization on the warehouse (query cost is real money)
- Setting team conventions and reviewing others' models

### Data Engineer → Senior DE → Data Architect
- Streaming systems (Kafka, Flink) beyond batch
- Distributed systems depth (Spark internals, partitioning strategy)
- Designing the whole platform: ingestion → storage → serving
- Reliability: SLAs on data freshness, lineage, observability (data contracts)

### Data Scientist → Senior DS → ML Engineer
- Productionizing models: deployment, monitoring, drift detection
- ML system design and MLOps (the gap most juniors miss)
- Causal inference, experimentation at scale
- **ML Engineer** is the SWE-heavy specialization: serving infra, latency, scale

---

## The GenAI / LLM frontier (where this is heading)

By the time you're 2+ years in, expect these to be normal:
- **RAG pipelines** — retrieval-augmented generation over company data; vector databases (pgvector, etc.) as part of the stack
- **LLM-as-a-tool in pipelines** — classification, extraction, summarization on unstructured text
- **Evaluation of LLM outputs** — the new hard problem (how do you test a non-deterministic system?)
- **AI/ML platform roles** — serving, prompt management, cost control at scale

The junior skill that ages well: **judgment over generation.** Anyone can prompt; the value is knowing whether the output is actually right and being able to debug it when it's not.

---

## Skills that compound

| Skill | Why it pays off long-term |
|---|---|
| **Communication / storytelling** | The thing that separates senior analysts from query-writers |
| **SQL depth** | Never stops mattering, every track, every level |
| **One cloud platform deep** | DE/architecture roles demand it |
| **Data modeling** | Transfers across AE, DE, and architecture |
| **Statistics intuition** | The DS/experimentation moat |
| **Git + software engineering habits** | What turns an analyst into an analytics engineer |

---

## How to keep growing

- **Go deep on one warehouse/platform** rather than skimming a dozen tools.
- **Read other people's code** — dbt projects, pipeline repos, Kaggle notebooks.
- **Write** — a blog post explaining a project teaches you and builds your profile.
- **Contribute to open source** — dbt packages, a Polars/pandas issue, an Airflow provider.
- **Pick the next cert based on your actual track**, not by collecting badges (see [certifications.md](certifications.md)).

---

> **The meta-skill:** the field's tooling will churn (it already has — Hadoop → Spark, MLS-C01 → MLA-C01, ELK → OTel everywhere else). SQL, statistics, data modeling, and clear communication don't churn. Invest there.

[← Job Hunt](05-job-hunt.md) · [Hub](README.md)
