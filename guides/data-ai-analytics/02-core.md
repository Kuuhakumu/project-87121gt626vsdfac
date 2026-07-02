# Goal 2: core analyst skills meow

> **~160h total** - your pace, no deadline.
> turn raw SQL + Python into employable analytics: BI, warehouses, cleaning, and storytelling.

[Previous: Goal 1](01-foundations.md) - [Hub](README.md) - [Next: Goal 3](03-specialization.md)

---

- [ ] **BI / visualization tool** (~70h)
- [ ] **cloud data warehouse** (~50h)
- [ ] **real-world cleaning + EDA** (~40h)
- [ ] **AI-assisted workflow literacy** (~40h parallel)
- [ ] **exit check** - dashboards, warehouse query, messy dataset, business summary, AI verification

## BI / visualization tool (~70h)

pick **one** and go deep. a dashboard u can show beats three tools u half-know.

- **Power BI** - learn first for employability; Microsoft dominates enterprise. cert: **PL-300**.
- **Tableau** - strong second, common in US tech / analytics-heavy shops.
- **Looker** - Google Cloud-native, LookML is niche but useful.

cover:

- [ ] connecting to files, databases, warehouses
- [ ] data modeling and star schema basics
- [ ] Power BI DAX or Tableau calculated fields/LOD expressions
- [ ] chart choice and visual clarity
- [ ] filters, slicers, drill-down, parameters
- [ ] publishing and sharing dashboards

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [MS Learn: Power BI (PL-300 path)](https://learn.microsoft.com/en-us/training/powerplatform/power-bi) | Official | guided Power BI track | **Free** |
| [Tableau Public](https://public.tableau.com) | Official | build + publish dashboards | **Free** |
| [Maven Analytics Data Playground](https://www.mavenanalytics.io/data-playground) | Web | real datasets to visualize | **Free** |

Tableau Public doubles as portfolio hosting.

## cloud data warehouse (~50h)

modern data work happens in a cloud warehouse, not only on your laptop.

- [ ] what a columnar warehouse is and why analytics queries are fast
- [ ] BigQuery sandbox or Snowflake trial
- [ ] loading data and running SQL at scale
- [ ] partitioning/clustering basics
- [ ] cost awareness; why `SELECT *` can be expensive
- [ ] connecting BI to the warehouse

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [BigQuery Sandbox](https://cloud.google.com/bigquery/docs/sandbox) | Google | query public datasets, no card | **Free** |
| [Snowflake Free Trial](https://signup.snowflake.com) | Snowflake | $400 credits, 30 days | **Free** trial |
| [Google Cloud Skills Boost](https://www.cloudskillsboost.google) | Google | guided BigQuery labs | Freemium |

## real-world data cleaning and EDA (~40h)

clean data is most of the job. this is where judgment starts showing.

- [ ] missing values: drop vs impute
- [ ] outliers
- [ ] type conversions, dates, encodings
- [ ] deduplication, messy joins, pivot/melt
- [ ] exploratory data analysis
- [ ] write-up: business answer for a non-technical stakeholder

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Kaggle: Data Cleaning](https://www.kaggle.com/learn/data-cleaning) | Kaggle | hands-on cleaning micro-course | **Free** |
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Kaggle | messy real data | **Free** |
| [data.gov](https://data.gov) / [Our World in Data](https://ourworldindata.org) | Web | public datasets for projects | **Free** |

## AI-assisted workflow literacy (~40h parallel)

in 2026, juniors are expected to use LLM tools and check them.

- [ ] use an LLM to write/debug SQL and explain errors
- [ ] prompt with schema + question, then verify the query
- [ ] understand RAG/vector DBs at a high level
- [ ] keep judgment, validation, and communication as your job

dont over-invest here. fine-tuning, production RAG, and LangChain internals are senior/ML-engineering territory.

## exit check

- [ ] built + published at least 2 dashboards in your chosen BI tool
- [ ] loaded data into BigQuery or Snowflake and queried it
- [ ] cleaned a genuinely messy public dataset end-to-end
- [ ] wrote a plain-language business question -> data answer summary
- [ ] used an LLM to draft SQL, then caught/fixed at least one thing it got wrong

[Next: Goal 3 - Pick Your Track](03-specialization.md)
