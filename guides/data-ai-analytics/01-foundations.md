# 🧱 Phase 1: Foundations

> **~140 hrs total** · your pace, no deadline
> SQL, Python, Git, and statistical literacy. This is the base every data track stands on.

[← Phase 0](00-prep.md) · [Hub](README.md) · [Next: Phase 2 — Core Skills →](02-core.md)

---

## SQL (the most important skill in this guide) (~60 hrs)

If you learn nothing else well, learn SQL. It's the most-tested, most-used skill across every data role.

### What to cover
- **Basics:** `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`, `DISTINCT`
- **Aggregation:** `GROUP BY`, `HAVING`, `COUNT/SUM/AVG/MIN/MAX`
- **Joins:** `INNER`, `LEFT`, `RIGHT`, `FULL` — know exactly what each returns
- **Subqueries & CTEs:** `WITH ... AS` — the readable way to build complex queries
- **Window functions:** `ROW_NUMBER`, `RANK`, `LAG/LEAD`, `SUM() OVER (PARTITION BY ...)` — **the #1 thing that separates juniors from beginners in interviews**
- **Data types, `NULL` handling, `CASE` expressions, date functions**

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [SQLBolt](https://sqlbolt.com) | Web | Interactive lessons from zero | **Free** |
| [SQLZoo](https://sqlzoo.net) | Web | Query exercises with checking | **Free** |
| [PostgreSQL Exercises](https://pgexercises.com) | Web | Real Postgres puzzles | **Free** |
| [Mode SQL Tutorial](https://mode.com/sql-tutorial/) | Web | SQL + analytics context | **Free** |
| [DataLemur](https://datalemur.com) | Web | SQL interview questions (FAANG-style) | **Free** tier |
| [StrataScratch](https://www.stratascratch.com) | Web | Real company SQL/data questions | **Free** tier |

**Practice gate:** You should be able to solve a medium DataLemur window-function question without hints before moving on.

---

## Python for data (~50 hrs)

Python is the second pillar. Keep focus on data manipulation, not software engineering.

### What to cover
- **Core Python:** variables, types, lists/dicts, loops, functions, comprehensions
- **pandas** (learn this first — it's the lingua franca): `DataFrame`, indexing, filtering, `groupby`, `merge`, handling missing data. pandas 3.0 uses Copy-on-Write by default.
- **NumPy** basics: arrays, vectorized operations
- **Reading data:** CSV, Excel, JSON, Parquet, SQL queries into DataFrames
- **DuckDB** — run SQL directly on local files; "SQL on your laptop," great for SQL-first learners
- **Visualization:** matplotlib + seaborn for quick exploratory charts

> **Polars** (a faster pandas alternative) is worth knowing *exists* — show yourself the syntax — but pandas is what tutorials, colleagues, and legacy code use. Learn pandas first, treat Polars as a differentiator later.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Kaggle: Python](https://www.kaggle.com/learn/python) | Kaggle | Micro-course, in-browser | **Free** |
| [Kaggle: Pandas](https://www.kaggle.com/learn/pandas) | Kaggle | Hands-on DataFrame skills | **Free** |
| [freeCodeCamp Data Analysis w/ Python](https://www.freecodecamp.org/learn/data-analysis-with-python/) | Web | Full cert track | **Free** |
| [DuckDB docs](https://duckdb.org) | Official | SQL on Parquet/CSV locally | **Free** |

---

## Git & version control (~20 hrs)

Essential for analytics-engineer and data-engineer tracks, and increasingly expected of analysts too.

### What to cover
- `init`, `clone`, `add`, `commit`, `push`, `pull`
- Branching + merging, pull requests
- `.gitignore` (never commit data files or credentials)
- Using GitHub as your portfolio home

**Lab:** [Learn Git Branching](https://learngitbranching.js.org) (visual) + put one notebook on GitHub.

---

## Statistical literacy (~10 hrs)

You need intuition, not a math degree — know *when* to use a tool, not how to derive it from scratch.

### What to cover
- Descriptive stats: mean, median, mode, variance, standard deviation
- Distributions: normal, skew, what a percentile means
- Correlation vs causation (and why confusing them gets people fired)
- Sampling & bias
- A/B testing basics: what a p-value actually means, significance
- Reading a confidence interval

**Lab:** [Kaggle: Intro to Statistics](https://www.kaggle.com/learn) micro-courses + Khan Academy statistics.

---

## Phase 1 exit checklist
- [ ] Solve a medium window-function SQL problem unaided
- [ ] Load a CSV into pandas, clean it, and `groupby`-aggregate it
- [ ] Run a SQL query on a local file with DuckDB
- [ ] One notebook committed to GitHub via a branch + PR
- [ ] Explain p-value and correlation-vs-causation in plain English

Next: [Phase 2 — Core Skills (BI, warehouses, cleaning) →](02-core.md)
