# 🛠️ Phase 2: Core Skills

> **~160 hrs total** · your pace, no deadline
> Turn raw SQL + Python into employable analytics: a BI tool, cloud warehouses, real-world data cleaning, and storytelling.

[← Phase 1](01-foundations.md) · [Hub](README.md) · [Next: Phase 3 — Track Specialization →](03-specialization.md)

---

## A BI / visualization tool (~70 hrs)

Pick **one** and go deep — a dashboard you can actually show beats three tools you half-know.

### Which to learn first
- **Power BI** — learn this first for employability; Microsoft dominates enterprise. Cert: **PL-300**.
- **Tableau** — strong second, common in US tech / analytics-heavy shops.
- **Looker** — Google Cloud-native, LookML is a real but niche skill (a differentiator, not a baseline).

### What to cover
- Connecting to data (files, databases, warehouses)
- Data modeling: relationships, star schema basics
- **Power BI:** DAX measures, calculated columns; **Tableau:** calculated fields, LOD expressions
- Visual best practices: pick the right chart, avoid chartjunk, design for the reader
- Interactivity: filters, slicers, drill-down, parameters
- Publishing & sharing dashboards

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [MS Learn: Power BI (PL-300 path)](https://learn.microsoft.com/en-us/training/powerplatform/power-bi) | Official | Full guided Power BI track | **Free** |
| [Tableau Public](https://public.tableau.com) | Official | Build + publish dashboards to a public portfolio | **Free** |
| [Maven Analytics Data Playground](https://www.mavenanalytics.io/data-playground) | Web | Real datasets to visualize | **Free** |

> **Tableau Public doubles as portfolio hosting** — every dashboard you build gets a shareable link. Use it.

---

## Cloud data warehouses (~50 hrs)

Modern data work happens in a cloud warehouse, not on your laptop. Pick one and get comfortable in it.

### What to cover
- What a columnar warehouse is and why it's fast for analytics
- **BigQuery** (free sandbox, no card) **or** **Snowflake** (30-day free trial) — pick one
- Loading data, running SQL at scale, partitioning/clustering basics
- Cost awareness: why `SELECT *` on a huge table is expensive
- Connecting your BI tool to the warehouse

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [BigQuery Sandbox](https://cloud.google.com/bigquery/docs/sandbox) | Google | Query big public datasets, no credit card | **Free** |
| [Snowflake Free Trial](https://signup.snowflake.com) | Snowflake | $400 credits, 30 days | **Free** trial |
| [Google Cloud Skills Boost](https://www.cloudskillsboost.google) | Google | Guided BigQuery labs | Freemium |

---

## Real-world data cleaning & EDA (~40 hrs)

Clean data is 80% of the job — this is where you build real judgment.

### What to cover
- Handling missing values (drop vs impute — and when each is wrong)
- Detecting & treating outliers
- Type conversions, parsing dates, fixing encodings
- Deduplication, joining messy datasets, reshaping (pivot/melt)
- **Exploratory Data Analysis (EDA):** systematically understanding a dataset before modeling
- **The write-up:** turning findings into a business answer a non-technical stakeholder understands

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Kaggle: Data Cleaning](https://www.kaggle.com/learn/data-cleaning) | Kaggle | Hands-on cleaning micro-course | **Free** |
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Kaggle | Messy real data to practice on | **Free** |
| [data.gov](https://data.gov) / [Our World in Data](https://ourworldindata.org) | Web | Public datasets for projects | **Free** |

---

## AI-assisted workflow literacy (~40 hrs, parallel)

In 2026, juniors are expected to *use* LLM tools to accelerate work — and to check their output.

### What to cover
- Using an LLM to write/debug SQL and explain errors
- Prompting for data tasks: give schema + question, get a query, **then verify it**
- High-level RAG concept: what a vector DB does, why it matters (awareness only)
- The line: AI accelerates mechanical tasks; **judgment, validation, and communication are yours**

> **Don't over-invest here.** Fine-tuning, production RAG pipelines, and LangChain internals are senior/ML-Eng territory. A junior needs *awareness* and *good usage habits*, not depth.

---

## Phase 2 exit checklist
- [ ] Built + published at least 2 dashboards in your chosen BI tool
- [ ] Loaded data into BigQuery or Snowflake and queried it
- [ ] Cleaned a genuinely messy public dataset end-to-end
- [ ] Wrote a plain-language "business question → data answer" summary
- [ ] Used an LLM to draft a SQL query, then caught/fixed at least one thing it got wrong

Next: [Phase 3 — Pick your track (Analyst / Analytics Eng / Data Eng / DS) →](03-specialization.md)
