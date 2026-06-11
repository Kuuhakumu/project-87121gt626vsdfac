# 🎯 Phase 3: Pick Your Track

> **~150 hrs total** · your pace, no deadline
> You now have the shared base. Pick **one** track and learn its signature tooling. Don't spread thin — depth in one track is what gets you hired.

[← Phase 2](02-core.md) · [Hub](README.md) · [Next: Phase 4 — Portfolio →](04-projects.md)

---

## Which track? (honest entry reality)

| Track | Entry difficulty | First-job reality |
|---|---|---|
| **Data / BI Analyst** | 🟢 Lowest barrier | The genuine entry point — SQL + a BI tool gets a screen |
| **Analytics Engineer** | 🟡 Emerging entry | Real junior roles if you have SQL depth + dbt |
| **Data Engineer** | 🟠 Harder entry | Accessible but expects Python + cloud fluency |
| **Data Scientist** | 🔴 Rarely true-entry | "Junior DS" usually wants a strong analyst + some ML; real ML roles want a master's or experience |

> **Like "DevOps," the "Data Scientist" title inflates entry expectations.** Most people enter as an **Analyst** or **Analytics/Data Engineer**, then pivot into DS after 1–2 years. **ML Engineer is not an entry role** — it's SWE + ML depth.

**Recommendation for most beginners:** start on the **Data Analyst** track. It's the realistic first job, and every other track builds on the same SQL + Python foundation.

---

## Track A: Data / BI Analyst

**Goal:** answer business questions with data and communicate the findings clearly.

### What to cover
- Advanced SQL: window functions, complex CTEs, query optimization
- Statistical literacy: A/B test basics, significance, correlation vs causation
- Deep dashboarding in your BI tool (DAX or LOD expressions)
- Stakeholder communication: turning analysis into decisions

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [DataLemur](https://datalemur.com) | Web | SQL + analytics interview questions | **Free** |
| [StrataScratch](https://www.stratascratch.com) | Web | Real company data questions | Freemium |
| [Mode SQL Tutorial](https://mode.com/sql-tutorial/) | Mode | Analytics-focused SQL + case studies | **Free** |

**Cert:** Google Data Analytics + PL-300 (Power BI).

---

## Track B: Analytics Engineer

**Goal:** build clean, tested, documented data models — the bridge between raw data and the analysts who use it.

### What to cover
- **dbt** (the defining tool): staging → marts layering, models, refs, sources
- dbt tests, documentation, and CI (run `dbt test` on pull requests)
- Dimensional modeling (star schema, slowly-changing dimensions)
- Git workflow for data: PRs, code review on SQL
- Warehouse depth (BigQuery/Snowflake)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [dbt Fundamentals](https://courses.getdbt.com) | dbt Labs | Official free dbt course | **Free** |
| [dbt + DuckDB local](https://duckdb.org) | Local | Build a dbt project with no cloud cost | **Free** |

**Cert:** dbt Analytics Engineering Certification ($200) + SnowPro Core (if Snowflake-focused).

---

## Track C: Data Engineer

**Goal:** build reliable pipelines that move and transform data at scale — the plumbing that keeps everything else running.

### What to cover
- Python depth: APIs, file formats (Parquet), error handling
- **Orchestration:** pick one — **Prefect** (easiest), Airflow (most common in postings), or Dagster
- Batch processing with **Spark / PySpark** (large-scale)
- Streaming *awareness*: Kafka / Pub/Sub concepts (batch vs real-time)
- Docker basics for packaging pipelines
- Cloud warehouse + storage

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Prefect docs + tutorials](https://docs.prefect.io) | Official | Build + run your first flows | **Free** |
| [Airflow tutorials](https://airflow.apache.org/docs/) | Official | DAGs, operators, scheduling | **Free** |
| [Start Data Engineering](https://www.startdataengineering.com) | Blog | End-to-end pipeline walkthroughs | **Free** |

**Cert:** AWS Data Engineer Associate (DEA-C01) or Databricks Data Engineer Associate.

---

## Track D: Data Scientist (the long game)

**Goal:** model, predict, and explain — just expect to come in through the Analyst door first.

### What to cover
- **scikit-learn**: the full workflow (split → train → evaluate → tune)
- Model evaluation: precision/recall, ROC, why accuracy lies on imbalanced data
- Feature engineering
- **PyTorch** basics if going deep-learning (it won the practitioner war over TensorFlow)
- Communicating model results to non-technical audiences

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Kaggle Learn: ML](https://www.kaggle.com/learn) | Kaggle | Intro → intermediate ML micro-courses | **Free** |
| [scikit-learn getting started](https://scikit-learn.org/stable/getting_started.html) | Official | The canonical sklearn workflow | **Free** |
| [fast.ai](https://www.fast.ai) | fast.ai | Practical deep learning | **Free** |
| [Kaggle Competitions](https://www.kaggle.com/competitions) | Kaggle | Real ML problems + leaderboard | **Free** |

**Cert:** AWS ML Engineer Associate (MLA-C01) — note the old MLS-C01 **retired March 2026**.

---

## Phase 3 exit checklist
- [ ] Chose **one** track and can explain why it fits you
- [ ] Learned that track's signature tool to working competence (dbt / Prefect / sklearn / advanced BI)
- [ ] Completed the track's hands-on labs
- [ ] Identified the cert that matches your track
- [ ] Have a concrete idea for your track's portfolio centerpiece (built in Phase 4)

Next: [Phase 4 — Build your portfolio →](04-projects.md)
