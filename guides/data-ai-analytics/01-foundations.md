# Goal 1: foundations meow

> **~160h total** - your pace, no deadline.
> SQL, Python, Git, and statistical literacy.
> this is the base every data track stands on.

[Previous: Goal 0](00-prep.md) - [Hub](README.md) - [Next: Goal 2](02-core.md)

---

- [ ] **SQL** (~60h)
- [ ] **Python for data** (~50h)
- [ ] **Git and version control** (~20h)
- [ ] **statistical literacy** (~10h)
- [ ] **exit check** - SQL window problem, pandas cleaning, DuckDB, GitHub notebook, stats explanation

## SQL (~60h)

if u learn nothing else well, learn SQL. its the most-tested and most-used skill across every data role.

- [ ] `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`, `DISTINCT`
- [ ] aggregation: `GROUP BY`, `HAVING`, `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- [ ] joins: `INNER`, `LEFT`, `RIGHT`, `FULL`
- [ ] subqueries and CTEs: `WITH ... AS`
- [ ] window functions: `ROW_NUMBER`, `RANK`, `LAG`, `LEAD`, `SUM() OVER (PARTITION BY ...)`
- [ ] data types, `NULL`, `CASE`, date functions

window functions are the big separator between beginner and junior-ready, dw this clicks with reps.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [SQLBolt](https://sqlbolt.com) | Web | interactive lessons from zero | **Free** |
| [SQLZoo](https://sqlzoo.net) | Web | query exercises with checking | **Free** |
| [PostgreSQL Exercises](https://pgexercises.com) | Web | real Postgres puzzles | **Free** |
| [Mode SQL Tutorial](https://mode.com/sql-tutorial/) | Web | SQL + analytics context | **Free** |
| [DataLemur](https://datalemur.com) | Web | SQL interview questions | **Free** tier |
| [StrataScratch](https://www.stratascratch.com) | Web | real company SQL/data questions | **Free** tier |

**practice gate:** solve a medium DataLemur window-function question without hints before moving on.

## Python for data (~50h)

keep Python focused on data manipulation, not general software engineering.

- [ ] core Python: variables, types, lists/dicts, loops, functions, comprehensions
- [ ] pandas: DataFrames, indexing, filtering, `groupby`, `merge`, missing data
- [ ] NumPy basics: arrays, vectorized operations
- [ ] read CSV, Excel, JSON, Parquet, SQL queries into DataFrames
- [ ] DuckDB for SQL on local files
- [ ] matplotlib + seaborn for quick charts

Polars is worth knowing exists, but learn pandas first.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Kaggle: Python](https://www.kaggle.com/learn/python) | Kaggle | micro-course, in-browser | **Free** |
| [Kaggle: Pandas](https://www.kaggle.com/learn/pandas) | Kaggle | hands-on DataFrame skills | **Free** |
| [freeCodeCamp Data Analysis w/ Python](https://www.freecodecamp.org/learn/data-analysis-with-python/) | Web | full cert track | **Free** |
| [DuckDB docs](https://duckdb.org) | Official | SQL on Parquet/CSV locally | **Free** |

## Git and version control (~20h)

expected for analytics-engineer and data-engineer tracks, and increasingly expected for analysts.

- [ ] `init`, `clone`, `add`, `commit`, `push`, `pull`
- [ ] branching, merging, pull requests
- [ ] `.gitignore`; never commit data files or credentials
- [ ] GitHub as portfolio home

**lab:** [Learn Git Branching](https://learngitbranching.js.org) + put one notebook on GitHub.

## statistical literacy (~10h)

u need intuition, not a math degree.

- [ ] mean, median, mode, variance, standard deviation
- [ ] distributions, skew, percentiles
- [ ] correlation vs causation
- [ ] sampling and bias
- [ ] A/B testing basics, p-value, significance
- [ ] confidence intervals

**lab:** [Kaggle: Intro to Statistics](https://www.kaggle.com/learn) micro-courses + Khan Academy statistics.

## exit check

- [ ] solve a medium window-function SQL problem unaided
- [ ] load a CSV into pandas, clean it, and `groupby`-aggregate it
- [ ] run a SQL query on a local file with DuckDB
- [ ] one notebook committed to GitHub via a branch + PR
- [ ] explain p-value and correlation-vs-causation in plain English

[Next: Goal 2 - Core Skills](02-core.md)
