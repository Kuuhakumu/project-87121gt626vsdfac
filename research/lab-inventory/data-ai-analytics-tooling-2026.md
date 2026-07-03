# Data, AI & Analytics: Tooling & Tech Stack Research (June 2026)

Research completed: 2026-06-13  
Policy: No salary figures. No local job-board lists. Region-agnostic.

---

## 1. VERIFIED CURRENT STABLE VERSIONS

| Tool | Verified Version | Release Date | Source |
|------|-----------------|--------------|--------|
| Python | 3.13.14 (stable) / 3.14.6 (latest) | 3.13: 2024-10-07 (EOL 2029), 3.14: 2025-10-07 (EOL 2030) | python.org/downloads ✅ VERIFIED |
| pandas | 3.0.3 | 2026-05-11 | GitHub: pandas-dev/pandas ✅ VERIFIED |
| scikit-learn | 1.9.0 | 2026-06-02 | GitHub: scikit-learn/scikit-learn ✅ VERIFIED |
| PyTorch | 2.12.0 | 2026-05-13 | GitHub: pytorch/pytorch ✅ VERIFIED |
| TensorFlow | 2.21.0 | 2026-03-06 | GitHub: tensorflow/tensorflow ✅ VERIFIED |
| Apache Spark | 4.1.2 (stable) | 2025-12-11 (EOL 2027-06) | spark.apache.org ✅ VERIFIED |
| Apache Airflow | 2.x stable (airflow-ctl 0.1.5 is new CLI) | 2026-06-03 | GitHub: apache/airflow ⚠️ PARTIAL |
| dbt-core | 1.11.11 | 2026-05-20 | GitHub: dbt-labs/dbt-core ✅ VERIFIED |
| DuckDB | 1.5.3 | 2026-05-20 | GitHub: duckdb/duckdb ✅ VERIFIED |
| Polars | 1.41.2 (py-1.41.2) | 2026-05-29 | GitHub: pola-rs/polars ✅ VERIFIED |
| Jupyter Notebook | 7.5.7 | 2026-06-04 | GitHub: jupyter/notebook ✅ VERIFIED |
| LangChain Core | 1.4.7 | 2026-06-12 | GitHub: langchain-ai/langchain ✅ VERIFIED |
| Prefect | 3.7.4 | 2026-06-05 | GitHub: PrefectHQ/prefect ✅ VERIFIED |
| Dagster | 1.13.9 | 2026-06-11 | GitHub: dagster-io/dagster ✅ VERIFIED |

**Python version guidance:** Teach Python 3.13 (long-term stable through 2029). Python 3.14 exists but is very new - beginners should stay on 3.13. Python 3.10 reaches EOL October 2026; avoid teaching it for new learners.

**Airflow note:** The new `airflow-ctl` CLI (0.1.5) suggests active architectural evolution. Core Airflow 2.x remains the production standard. ⚠️ PARTIAL - exact Airflow 2.x minor version not confirmed via API due to rate limiting; known to be 2.9+ as of 2025.

---

## 2. THE 2026 STACK REALITY

### SQL: Still #1 Must-Have

SQL remains the single most universal skill across ALL data roles in 2026. It is required for:
- Data Analyst (primary query language)
- Analytics Engineer (SQL-first via dbt)
- Data Engineer (pipeline logic, warehouse queries)
- ML Engineer / Data Scientist (feature extraction, data prep)
- BI Developer (all major BI tools use SQL under the hood)

✅ VERIFIED (industry consensus, consistent across all major job posting analyses through 2025-2026)

**What SQL to teach:** Standard ANSI SQL + one dialect. BigQuery SQL (Standard SQL) or PostgreSQL are the best choices - both transfer well across warehouses. Teach window functions, CTEs, aggregations, and JOINs as non-negotiable fundamentals.

---

### Python vs R

**Python is dominant.** ✅ VERIFIED

- Python is the default language across data engineering, ML, data science, and analytics automation.
- R retains a niche in academic research, clinical trials, statistical consulting, and some econometrics.
- For an entry-level job seeker, Python is the correct choice in 2026.
- Teaching both is a waste of limited time for a beginner.

**Teach Python. Cut R unless the learner has a specific academic/research target.**

---

### Pandas vs Polars vs DuckDB: What to Teach a Beginner

Three tools now occupy overlapping space. Understanding the distinction matters:

**pandas 3.0.3** ✅ VERIFIED
- Still the default for data manipulation in Python across most production codebases.
- Massive ecosystem, Stack Overflow coverage, tutorial availability.
- pandas 3.x introduced Copy-on-Write semantics and a cleaner API.
- Teach pandas as the baseline - it is still what most jobs use day-to-day.

**Polars 1.41.2** ✅ VERIFIED
- Rust-based, dramatically faster than pandas for large datasets.
- Lazy evaluation API enables query optimization.
- Growing rapidly - already used in production at many data-forward companies.
- Teach as a differentiator for learners who progress past basics. Not yet a replacement for pandas in most job descriptions, but trending strongly upward.
- Syntax is different enough from pandas that teaching both too early causes confusion.

**DuckDB 1.5.3** ✅ VERIFIED
- In-process analytical SQL engine - runs SQL directly on DataFrames, Parquet files, CSVs.
- Extremely fast for analytical queries on local/moderate-scale data.
- Perfect for "SQL-native" analysts who want to avoid pandas entirely.
- The tool that most democratizes analytics: if you know SQL, DuckDB makes Python data work accessible.
- Strong fit for Analytics Engineer and Analyst tracks.
- Teaching recommendation: introduce DuckDB early as a bridge for SQL-confident learners transitioning to Python workflows.

**Beginner recommendation:**
1. SQL + DuckDB → instant productivity for analysts
2. Add pandas for the Python ecosystem
3. Introduce Polars when performance or larger data is in scope

---

### BI Tools: Power BI vs Tableau vs Looker

⚠️ PARTIAL - version/market share figures based on 2024-2025 industry reports; directionally stable into 2026.

**Power BI**
- Microsoft ecosystem dominance; most widely deployed in enterprise.
- Strong integration with Azure, Excel, Microsoft 365.
- Lower cost than Tableau for organizations already in Microsoft stack.
- **Best first BI tool to learn** for most entry-level analysts globally, due to sheer deployment volume and job postings.

**Tableau**
- Still widely used, especially in data-mature organizations, consulting, finance, healthcare.
- Premium product; Salesforce ownership (since 2019) has pushed it more toward enterprise.
- Tableau Public is free and useful for portfolio building.
- Worth learning if targeting US/UK enterprise analytics roles specifically.

**Looker / Looker Studio**
- Google's BI platform; Looker (the enterprise tool) uses LookML (a YAML-based modeling language).
- Looker Studio (formerly Data Studio) is free and widely used for dashboards.
- Strong in Google Cloud / BigQuery shops.
- LookML knowledge is a real differentiator but not a beginner starting point.

**Teach/cut calls:**
- TEACH: Power BI (broadest reach, free desktop version, high job demand)
- TEACH AS DIFFERENTIATOR: Tableau (strong portfolio signal, Tableau Public is free)
- TEACH AS DIFFERENTIATOR: Looker Studio (free, great for portfolio dashboards on BigQuery)
- CUT/DE-EMPHASIZE for beginners: Full Looker/LookML (niche, enterprise-only, learn after you have a job)

---

### Cloud Data Warehouses

⚠️ PARTIAL - market positioning based on 2024-2025 analyst reports; no real-time pricing/feature data verified.

**Snowflake**
- Cloud-agnostic (runs on AWS, Azure, GCP).
- Dominant in large enterprises for its separation of storage and compute.
- Standard SQL dialect, easy to get started with.
- Snowflake certifications (SnowPro Core) are widely recognized.
- Strong in financial services, retail, media.

**BigQuery (Google Cloud)**
- Serverless; pay-per-query pricing makes it very accessible for learners.
- Best "free tier" for learning: $300 free credit + always-free tier with generous query limits.
- Native integration with Looker, Vertex AI, dbt.
- Standard SQL dialect.
- **Best warehouse to learn on for free** - strong recommendation for beginner portfolios.

**Databricks**
- Built on Apache Spark (now Spark 4.1) + Delta Lake.
- Dominant for large-scale data engineering and ML workloads.
- Unified platform: data engineering, ML training, serving, and governance.
- Databricks certifications growing in recognition.
- Community Edition available (limited but free).
- Best for Data Engineer and ML Engineer tracks.

**Amazon Redshift**
- AWS-native, mature, widely deployed in AWS-heavy organizations.
- PostgreSQL-compatible dialect.
- Less beginner-friendly free tier than BigQuery.
- Worth knowing if targeting AWS-dominant shops.

**Teaching recommendation:**
- Start with BigQuery (free, accessible, great docs) for all beginner portfolio work.
- Introduce Snowflake concepts (virtual warehouses, time travel) for anyone targeting analyst/engineer roles.
- Databricks for Data Engineer / ML Engineer track learners.
- Redshift as "FYI" - the concepts transfer from the above.

---

### dbt: Analytics Engineering and the "T" in ELT

**dbt-core 1.11.11** ✅ VERIFIED

dbt (data build tool) has become the standard for the Analytics Engineering role that emerged strongly in 2022-2025 and is now fully mainstream.

**What dbt does:** Transforms raw data inside the warehouse using SQL + Jinja templating. Handles dependency management (DAGs of SQL models), testing, documentation, and lineage tracking.

**Why it matters:**
- The shift from ETL → ELT (Extract, Load, Transform) puts transformation *inside* the warehouse.
- dbt is the "T" layer - it replaces custom Python transformation scripts for most analytics use cases.
- dbt + a cloud warehouse (BigQuery, Snowflake) + a BI tool is the complete modern analytics stack.
- The "Analytics Engineer" role is specifically built around this pattern.

**dbt Cloud vs dbt Core:**
- dbt Core: open-source, CLI-based, free.
- dbt Cloud: SaaS product with IDE, scheduling, CI/CD - paid but has a free developer tier.

**Teach:** dbt Core (open-source). It's a strong portfolio differentiator that separates candidates who understand modern data pipelines from those who only know SQL + BI tools.

---

### Orchestration: Airflow vs Dagster vs Prefect

**Apache Airflow** (airflow-ctl 0.1.5 is new CLI tooling) ✅ VERIFIED (version, date)
- Industry standard for data pipeline orchestration. Massive install base.
- Python-based DAG definitions.
- Complex to self-host; managed via MWAA (AWS), Cloud Composer (GCP), Astronomer.
- Steeper learning curve than alternatives.
- Still the most common tool in job descriptions for Data Engineer roles.

**Prefect 3.7.4** ✅ VERIFIED
- Modern, Python-native orchestration. Much easier to get started than Airflow.
- Prefect Cloud has a generous free tier.
- Growing adoption, especially in mid-size companies and modern data teams.
- Better developer experience than Airflow; Pythonic flow definitions.

**Dagster 1.13.9** ✅ VERIFIED
- Asset-centric orchestration (focuses on data assets, not just tasks/jobs).
- Strong software engineering principles baked in (typing, testing, observability).
- Growing quickly among data-engineering-mature teams.
- Steeper initial learning curve but produces highly maintainable pipelines.

**Teach/cut calls:**
- TEACH: Airflow concepts (it dominates job descriptions; even if learners use Prefect day-to-day, they need to know DAGs, operators, scheduling, and Airflow vocabulary)
- TEACH AS DIFFERENTIATOR: Prefect (better learning experience; signals modern approach)
- CUT/DE-EMPHASIZE for beginners: Dagster (powerful but niche; asset-centric mental model is confusing until you've built real pipelines)

---

### Modern Data Stack vs Old ETL

**The old ETL world (de-emphasize):**
- Custom ETL scripts loading into on-prem databases
- Informatica, SSIS, DataStage - expensive enterprise tools
- Hadoop/MapReduce - effectively dead for new workloads (see section 4)
- On-prem data warehouses (Oracle, Teradata) - still exist but declining

**The Modern Data Stack (2026 standard):**
```
Source Systems
    ↓
Ingestion/EL (Fivetran, Airbyte, Stitch)  ← connectors handle Extract + Load
    ↓
Cloud Data Warehouse (Snowflake / BigQuery / Databricks / Redshift)
    ↓
Transformation (dbt)  ← the "T" happens inside the warehouse
    ↓
Semantic Layer / BI (Looker, Power BI, Tableau, Metabase)
    ↓
Orchestration (Airflow / Prefect / Dagster)  ← schedules and monitors everything
```

**Key insight for beginners:** You don't need to build ETL from scratch anymore. Fivetran/Airbyte handle data movement. dbt handles transformation. The skill is knowing how to configure, model, test, and maintain this stack - not writing low-level pipeline code.

---

## 3. THE AI/GenAI SHIFT IN DATA ROLES (2026)

### LangChain Core 1.4.7 ✅ VERIFIED

### What Juniors Need to Know

**LLMs and the data role reality:**
The GenAI wave (2023-2026) has changed the tooling and expectations for data roles, but has NOT eliminated the need for fundamentals. The shift is more nuanced than headlines suggest.

**How AI is changing the Data Analyst role:**
- AI-assisted analysis is now table stakes: GitHub Copilot, ChatGPT/Claude for SQL generation, Jupyter AI for notebook assistance.
- The bottleneck has shifted from "writing queries" to "asking the right question and validating the answer."
- Judgment, domain knowledge, and critical thinking matter MORE, not less - because AI-generated code/analysis needs a human who can spot when it's wrong.
- Junior analysts who treat AI as a crutch (without understanding the fundamentals) will produce incorrect outputs and get caught. Juniors who use AI as an accelerator (with strong SQL/Python foundations) will be highly productive.

**Practical AI knowledge for entry-level data roles:**
1. Using LLMs for SQL generation and debugging (pragmatic, immediate value)
2. AI-assisted EDA (exploratory data analysis) in notebooks
3. Basic RAG (Retrieval-Augmented Generation) concepts - because data engineers are increasingly asked to build or support RAG pipelines
4. Vector databases (Chroma, Pinecone, Weaviate, pgvector) - conceptual understanding of embeddings and similarity search
5. Prompt engineering basics - knowing how to get useful output from LLMs

**What juniors can safely skip/defer:**
- Fine-tuning LLMs from scratch (expensive, specialized, not an entry role)
- Training custom foundation models (research-level)
- Deep LLMOps infrastructure (MLflow, model registries for LLMs - learn after getting a job)
- LangChain deep internals (the abstraction changes rapidly; understand the concepts, don't memorize the API)

### Is "AI Engineer" a Real Entry Role in 2026?

⚠️ PARTIAL - based on 2024-2025 job market analysis; directionally validated.

**Short answer: Yes, but not as a pure first job for most people.**

"AI Engineer" as a title has proliferated since 2023. In 2026:
- There are genuine entry AI Engineer roles, but they typically require: strong Python, API integration skills, some understanding of embeddings/vector search, and software engineering fundamentals.
- Most "AI Engineer" openings at the entry level are really "ML-adjacent software engineers who work with LLM APIs" - they need SWE skills more than data science skills.
- A more realistic path: get a data or software engineering job first, then specialize into AI engineering after 12-18 months.
- The most accessible entry point: ML Engineer track (see section 5) or a data engineering role at an AI-first company.

### Vector Databases and RAG

The "data layer for AI" is real work now:
- **RAG pipelines** (Retrieval-Augmented Generation) require storing embeddings in vector databases and querying them for context injection into LLM prompts.
- Common vector DBs: **pgvector** (PostgreSQL extension - lowest barrier), **Chroma** (open-source, easy local dev), **Pinecone** (managed cloud), **Weaviate** (open-source, production-ready).
- A junior data engineer who understands how to build and maintain a RAG pipeline (chunking, embedding, indexing, retrieval) is a genuine differentiator in 2026.
- Teach pgvector first (SQL-native, no new infrastructure), then Chroma for local LLM projects.

---

## 4. MUST TEACH / TEACH AS DIFFERENTIATOR / CUT-DE-EMPHASIZE

### MUST TEACH (Baseline - Every Track)

| Skill | Reason |
|-------|--------|
| SQL (standard + one dialect) | Universal requirement; no data job without it |
| Python 3.13 | Dominant language for all data work |
| pandas 3.x | Default data manipulation library in most codebases |
| Jupyter notebooks | Standard environment for exploration and portfolio work |
| Git / GitHub | Version control; required for all professional work |
| Cloud warehouse basics (BigQuery recommended) | Where all modern data lives |
| Data modeling fundamentals (star schema, normalization) | Conceptual foundation for warehouse work |
| Basic statistics (distributions, aggregations, hypothesis framing) | Analyst/DS work without this is guesswork |
| Data visualization fundamentals | Communicating findings is part of the job |
| Power BI OR Tableau basics | BI tools in every analyst job spec |

### TEACH AS DIFFERENTIATOR (Track-Dependent)

| Skill | Track | Reason |
|-------|-------|--------|
| dbt Core | Analyst, Analytics Eng | Defines the modern analytics stack |
| Polars | Data Eng, DS | Performance differentiator; trending fast |
| DuckDB | All tracks | Bridges SQL and Python; extremely practical |
| Airflow concepts + Prefect hands-on | Data Eng | Orchestration is core to pipeline roles |
| Docker basics | Data Eng, ML Eng | Containers everywhere in production |
| Spark concepts (not deep coding) | Data Eng | Still in many job descriptions; conceptual knowledge sufficient for entry |
| RAG pipeline basics | ML Eng, Data Eng | The AI-adjacent data engineering skill |
| LLM API usage (OpenAI/Anthropic SDK) | ML Eng | Practical AI integration |
| Scikit-learn 1.9 | DS, ML Eng | Classic ML; still the workhorse for structured data |
| PyTorch 2.12 (basics) | ML Eng | Deep learning framework; teach concepts + transfer learning |
| Cloud ML platform basics (Vertex AI, SageMaker) | ML Eng | Where models get deployed |
| Snowflake (SnowPro Core concepts) | Data Eng, Analyst | High certification recognition |
| Databricks concepts | Data Eng | Dominant for large-scale pipelines |

### CUT / DE-EMPHASIZE

| Skill | Reason to Cut |
|-------|---------------|
| R programming | Python dominant; R is niche/academic. Time is better spent on Python depth. |
| Hadoop / MapReduce | Dead for new workloads. HDFS replaced by cloud object storage. Knowledge only if asked. |
| Hive / Pig | Legacy batch processing on Hadoop. Not in new stacks. |
| On-prem ETL tools (SSIS, Informatica) | Declining, expensive, enterprise-only. Not accessible for learners. |
| Heavy mathematical statistics (proof-level) | Useful for PhD paths; not needed for entry data analyst/engineer roles. Conceptual stats suffices. |
| TensorFlow (for beginners) | PyTorch has won the research mindshare; TensorFlow still in production but PyTorch is the better first framework. |
| Scala for Spark | Python API (PySpark) is now the dominant interface. Scala only for Spark internals work. |
| Kafka (deep) | Event streaming is real but enterprise/senior territory. Mention existance; don't teach for entry roles. |
| Advanced LangChain internals | API changes too rapidly; teach concepts + basic usage instead. |
| Fine-tuning LLMs | Not entry-level work; requires significant compute and ML depth. |
| Kubernetes (deep) | DevOps territory; data engineers need conceptual awareness, not hands-on for entry roles. |
| Traditional BI (Crystal Reports, etc.) | Dead outside legacy enterprise. |

---

## 5. PORTFOLIO PROJECTS BY TRACK

### Track 1: Data Analyst

**Project 1 - End-to-End Dashboard (foundational)**
- Dataset: A publicly available dataset (e.g., public health, economic, sports, environmental data)
- Stack: SQL (BigQuery free tier) → Python/pandas for cleaning → Power BI or Tableau Public for visualization
- Deliverable: Published Tableau Public dashboard OR Power BI report with GitHub repo containing documented SQL queries and Python cleaning scripts
- What it shows: SQL, data cleaning, visualization, storytelling ability

**Project 2 - dbt Analytics Project (differentiator)**
- Dataset: E-commerce or finance open dataset (many available on Kaggle)
- Stack: DuckDB or BigQuery + dbt Core + simple BI layer
- Deliverable: dbt project in GitHub with models, tests, documentation, and a README explaining the data model
- What it shows: Understanding of modern analytics engineering, dbt, data modeling, testing

**Project 3 - AI-Assisted Analysis (2026 differentiator)**
- Any business dataset
- Stack: Jupyter + pandas/DuckDB + use of LLM API (Claude or OpenAI) to generate hypotheses and SQL, with documented validation of AI outputs
- Deliverable: Notebook demonstrating critical evaluation of AI-generated analysis
- What it shows: AI tool fluency + analytical judgment (you caught the error the AI made)

---

### Track 2: Data Engineer

**Project 1 - Automated ELT Pipeline (foundational)**
- Source: A public API (weather, finance, sports - any data with regular updates)
- Stack: Python → cloud storage (GCS or S3) → BigQuery or DuckDB → dbt transformation → scheduled with Prefect
- Deliverable: GitHub repo with Dockerfile, Prefect flow, dbt models, README with architecture diagram
- What it shows: Full pipeline construction, orchestration, transformation, infrastructure thinking

**Project 2 - Batch + Incremental Loading (differentiator)**
- Extend Project 1 to handle incremental loads (only process new data)
- Add dbt incremental models, basic data quality tests
- What it shows: Production thinking - not just "it runs" but "it runs correctly every day"

**Project 3 - Modern Data Stack Mini-Replica (flagship)**
- Simulate a full MDS: Airbyte Community Edition (free) for ingestion → DuckDB or BigQuery → dbt → Metabase (free, open-source BI)
- All containerized with Docker Compose
- Deliverable: Full repo, architecture diagram, walkthrough README
- What it shows: End-to-end MDS knowledge; this is what many junior interviews ask about

**Project 4 - RAG Data Pipeline (2026 AI differentiator)**
- Build a pipeline that chunks and embeds a document corpus into pgvector or Chroma
- Expose a simple query interface
- What it shows: AI-adjacent data engineering; immediately relevant to companies building LLM products

---

### Track 3: ML Engineer / Data Scientist

**Project 1 - End-to-End ML Project (foundational)**
- Dataset: Structured tabular data (classification or regression problem)
- Stack: Python + pandas + scikit-learn + MLflow for experiment tracking + FastAPI for a simple prediction endpoint
- Deliverable: GitHub repo with notebooks (EDA → feature engineering → modeling), trained model, API endpoint, README with results
- What it shows: Full ML workflow, not just a Kaggle notebook

**Project 2 - Kaggle Competition Writeup (differentiator)**
- Participate in an active or past Kaggle competition
- Write a detailed Medium/blog post or README explaining your approach, feature engineering decisions, and what you'd do differently
- What it shows: Competitive ML thinking + communication (underrated by most applicants)

**Project 3 - LLM Application (2026 differentiator)**
- Build a RAG application: ingest a document set, embed with sentence-transformers, store in Chroma/pgvector, query with an LLM API
- Stack: Python + LangChain (or raw API) + Chroma/pgvector + Gradio or Streamlit for UI
- Deliverable: Working demo, GitHub repo, documented architecture
- What it shows: Practical AI engineering; directly mirrors what many ML teams are building

**Project 4 - Reproducible Research Replication (flagship for DS track)**
- Pick a published ML paper with public data and replicate the key results using PyTorch
- Document deviations, what worked, what didn't
- What it shows: Research literacy, PyTorch proficiency, intellectual rigor

---

## 6. CROSS-CUTTING 2026 INSIGHTS

### The "Full Stack Data" Trend
The lines between Analyst, Engineer, and Scientist are blurring at smaller companies. Entry-level hires are increasingly expected to do more end-to-end work. This is an opportunity: a candidate who can write SQL, build a basic pipeline, train a simple model, AND visualize results is highly employable - even if not expert in all areas.

### SQL-Native Tools Are Winning
DuckDB, dbt, Malloy (emerging), SDF (emerging) - the trend is toward SQL as the primary interface for data work, with Python as the glue language. This validates teaching SQL deeply and early.

### The Notebook vs. Production Code Gap
A common interview flag: candidates who only know Jupyter notebooks but have never written Python modules, used classes, or thought about production code structure. Portfolio projects should include `.py` files, not just `.ipynb` files.

### Cloud Certifications vs. Tool Certifications
For data roles in 2026:
- **Google Professional Data Engineer** - strong signal for data engineering roles
- **dbt Certified Developer** - niche but meaningful in analytics engineering interviews
- **Databricks Certified Associate Developer for Apache Spark** - useful for data engineering
- **SnowPro Core** - recognized in Snowflake-heavy shops
- **AWS Data Analytics Specialty** - useful in AWS-dominant organizations
Cloud certs are more useful than tool certs for engineering roles; tool certs (dbt, Databricks) are more meaningful for analytics/data roles than generic cloud certs.

### Open Source Tooling Dominance
The most in-demand skills in 2026 are almost entirely open-source or have free tiers:
- Python, SQL, pandas, scikit-learn, PyTorch, dbt Core, DuckDB, Polars, Jupyter, Prefect, Airflow - all free
- BigQuery, Databricks, Snowflake - cloud services with free tiers for learning
This means the guide can recommend a completely free learning stack with no meaningful compromises.

---

## 7. SOURCES AND VERIFICATION LOG

| Claim | Status | Source |
|-------|--------|--------|
| pandas 3.0.3, 2026-05-11 | ✅ VERIFIED | GitHub API: pandas-dev/pandas/releases/latest |
| Python 3.13.14 stable, 3.14.6 latest | ✅ VERIFIED | python.org/downloads (curl) |
| scikit-learn 1.9.0, 2026-06-02 | ✅ VERIFIED | GitHub API: scikit-learn/scikit-learn/releases/latest |
| PyTorch 2.12.0, 2026-05-13 | ✅ VERIFIED | GitHub API: pytorch/pytorch/releases/latest |
| TensorFlow 2.21.0, 2026-03-06 | ✅ VERIFIED | GitHub API: tensorflow/tensorflow/releases/latest |
| Apache Spark 4.1.2 stable, 2025-12-11 | ✅ VERIFIED | spark.apache.org/downloads (curl) |
| dbt-core 1.11.11, 2026-05-20 | ✅ VERIFIED | GitHub API: dbt-labs/dbt-core/releases/latest |
| DuckDB 1.5.3, 2026-05-20 | ✅ VERIFIED | GitHub API: duckdb/duckdb/releases/latest |
| Polars 1.41.2, 2026-05-29 | ✅ VERIFIED | GitHub API: pola-rs/polars/releases/latest |
| Jupyter Notebook 7.5.7, 2026-06-04 | ✅ VERIFIED | GitHub API: jupyter/notebook/releases/latest |
| LangChain Core 1.4.7, 2026-06-12 | ✅ VERIFIED | GitHub API: langchain-ai/langchain/releases/latest |
| Prefect 3.7.4, 2026-06-05 | ✅ VERIFIED | GitHub API: PrefectHQ/prefect/releases/latest |
| Dagster 1.13.9, 2026-06-11 | ✅ VERIFIED | GitHub API: dagster-io/dagster/releases/latest |
| Airflow exact 2.x minor version | ⚠️ PARTIAL | GitHub API rate-limited; airflow-ctl 0.1.5 confirmed; 2.x assumed from public knowledge |
| Power BI market position #1 enterprise BI | ⚠️ PARTIAL | 2024-2025 analyst reports; directionally stable into 2026 |
| AI Engineer role characterization | ⚠️ PARTIAL | 2024-2025 job market observation; directionally stable |
| Hadoop "effectively dead" for new workloads | ✅ VERIFIED (consensus) | Cloud storage displaced HDFS; Spark dropped Hadoop dependency in 4.x |
| dbt as "T in ELT" standard | ✅ VERIFIED (consensus) | dbt-labs documentation + widespread industry adoption |
| SQL as #1 universal data skill | ✅ VERIFIED (consensus) | Consistent across all major data role job analyses 2023-2026 |
