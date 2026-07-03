# Goal 3: pick your track meow

> **~150h total** - your pace, no deadline.
> u have the shared base now. pick **one** track and learn its signature tooling.
> dont spread thin; depth in one track is what gets u hired.

[Previous: Goal 2](02-core.md) - [Hub](README.md) - [Next: Goal 4](04-projects.md)

---

- [ ] **choose the right track**
- [ ] **Track A: Data / BI Analyst**
- [ ] **Track B: Analytics Engineer**
- [ ] **Track C: Data Engineer**
- [ ] **Track D: Data Scientist long game**
- [ ] **exit check** - one track chosen, tool competence, labs done, cert identified, portfolio idea ready

## choose the right track

| Track | Entry difficulty | First-job reality |
|---|---|---|
| **Data / BI Analyst** | lowest barrier | genuine entry point: SQL + BI gets screens |
| **Analytics Engineer** | emerging entry | real junior roles with SQL depth + dbt |
| **Data Engineer** | harder entry | accessible, expects Python + cloud fluency |
| **Data Scientist** | rarely true-entry | often means strong analyst + some ML; real ML roles want more |

like "DevOps," the "Data Scientist" title inflates entry expectations. most people enter as **Analyst** or **Analytics/Data Engineer**, then pivot after 1-2 years.

recommendation for most beginners: start on **Data Analyst**. every other track builds on the same SQL + Python foundation.

## track A: data / BI analyst

**goal:** answer business questions with data and communicate findings clearly.

- [ ] advanced SQL: windows, complex CTEs, query optimization
- [ ] stats: A/B basics, significance, correlation vs causation
- [ ] dashboarding in Power BI or Tableau
- [ ] stakeholder communication

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [DataLemur](https://datalemur.com) | Web | SQL + analytics interview questions | **Free** |
| [StrataScratch](https://www.stratascratch.com) | Web | real company data questions | Freemium |
| [Mode SQL Tutorial](https://mode.com/sql-tutorial/) | Mode | analytics SQL + case studies | **Free** |

**cert:** Google Data Analytics + PL-300.

## track B: analytics engineer

**goal:** build clean, tested, documented data models - the bridge between raw data and analysts.

- [ ] **dbt:** staging -> marts layering, models, refs, sources
- [ ] dbt tests, docs, and CI with `dbt test`
- [ ] dimensional modeling: star schema, slowly-changing dimensions
- [ ] Git workflow for data: PRs, code review on SQL
- [ ] warehouse depth: BigQuery or Snowflake

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [dbt Fundamentals](https://courses.getdbt.com) | dbt Labs | official free dbt course | **Free** |
| [dbt + DuckDB local](https://duckdb.org) | Local | dbt project with no cloud cost | **Free** |

**cert:** dbt Analytics Engineering Certification ($200) + SnowPro Core if Snowflake-focused.

## track C: data engineer

**goal:** build reliable pipelines that move and transform data at scale.

- [ ] Python depth: APIs, Parquet, error handling
- [ ] orchestration: Prefect, Airflow, or Dagster
- [ ] batch processing with Spark / PySpark
- [ ] streaming awareness: Kafka / Pub/Sub
- [ ] Docker basics for packaging pipelines
- [ ] cloud warehouse + storage

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Prefect docs + tutorials](https://docs.prefect.io) | Official | build + run first flows | **Free** |
| [Airflow tutorials](https://airflow.apache.org/docs/) | Official | DAGs, operators, scheduling | **Free** |
| [Start Data Engineering](https://www.startdataengineering.com) | Blog | end-to-end pipeline walkthroughs | **Free** |

**cert:** AWS Data Engineer Associate (DEA-C01) or Databricks Data Engineer Associate.

## track D: data scientist long game

**goal:** model, predict, and explain - but expect to come through the Analyst door first.

- [ ] scikit-learn workflow: split -> train -> evaluate -> tune
- [ ] model evaluation: precision/recall, ROC, imbalanced accuracy
- [ ] feature engineering
- [ ] PyTorch basics if going deep learning
- [ ] communicating model results to non-technical audiences

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Kaggle Learn: ML](https://www.kaggle.com/learn) | Kaggle | intro -> intermediate ML micro-courses | **Free** |
| [scikit-learn getting started](https://scikit-learn.org/stable/getting_started.html) | Official | canonical sklearn workflow | **Free** |
| [fast.ai](https://www.fast.ai) | fast.ai | practical deep learning | **Free** |
| [Kaggle Competitions](https://www.kaggle.com/competitions) | Kaggle | real ML problems + leaderboard | **Free** |

**cert:** AWS ML Engineer Associate (MLA-C01). old MLS-C01 retired March 2026.

## exit check

- [ ] chose **one** track and can explain why it fits u
- [ ] learned that track's signature tool to working competence: dbt / Prefect / sklearn / advanced BI
- [ ] completed the track's hands-on labs
- [ ] identified the cert that matches your track
- [ ] have a concrete idea for your track's portfolio centerpiece in Goal 4

[Next: Goal 4 - Build Your Portfolio](04-projects.md)
