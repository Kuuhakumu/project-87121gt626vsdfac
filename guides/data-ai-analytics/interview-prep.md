# Interview prep - Data, AI & Analytics meow

> question bank + format guide.
> every track screens for SQL, so drill that first.

[Job Hunt](05-job-hunt.md) - [Hub](README.md)

---

- [ ] **know formats by role**
- [ ] **drill SQL cold**
- [ ] **prepare track-specific answers**
- [ ] **answer the GenAI/LLM question**
- [ ] **prepare behavioral stories**
- [ ] **practice take-homes**

## formats by role

| Role | Typical pipeline |
|---|---|
| **Data / BI Analyst** | SQL screen -> take-home analysis -> stakeholder presentation |
| **Analytics Engineer** | SQL screen -> dbt/modeling exercise -> data-modeling discussion |
| **Data Engineer** | Python/SQL coding -> pipeline design -> data architecture |
| **Data Scientist** | SQL screen -> stats/probability -> ML take-home -> explain model |
| **ML Engineer** | coding -> ML system design -> model-debugging exercise |

every track starts with SQL. no skipping it, sorry qwq.

## SQL bank

- [ ] second-highest value without `LIMIT 1 OFFSET 1`
- [ ] top-N per group with `ROW_NUMBER() OVER (PARTITION BY ...)`
- [ ] running total with `SUM(...) OVER (ORDER BY ...)`
- [ ] month-over-month change with `LAG()`
- [ ] JOIN types: INNER vs LEFT vs FULL
- [ ] de-duplicate latest row per key
- [ ] gaps and islands
- [ ] `WHERE` vs `HAVING`
- [ ] `COUNT(*)` vs `COUNT(col)`
- [ ] anti-join with `LEFT JOIN ... WHERE b.id IS NULL` or `NOT EXISTS`

practice on [DataLemur](https://datalemur.com), [StrataScratch](https://www.stratascratch.com), and [Mode SQL](https://mode.com/sql-tutorial/).

## Analyst / BI questions

- [ ] investigate a metric drop: clarify, segment, check quality, form hypotheses, test, recommend
- [ ] correlation vs causation example
- [ ] A/B testing basics: p-value, significance, sample-size pitfall
- [ ] dashboard design: start from decision, not available data
- [ ] DAX or LOD calculation u built and why

## Analytics Engineer questions

- [ ] dbt staging vs marts
- [ ] what `ref()` does and why not hardcode table names
- [ ] dbt tests for primary keys: `unique`, `not_null`
- [ ] fact vs dimension table
- [ ] slowly-changing dimensions
- [ ] why run `dbt test` in CI
- [ ] idempotency in transformations

## Data Engineer questions

- [ ] design daily API ingestion into a warehouse
- [ ] batch vs streaming
- [ ] orchestration vs cron
- [ ] Parquet vs CSV
- [ ] pipeline fails halfway - recovery plan
- [ ] partitioning a large table

## Data Science questions

- [ ] why accuracy lies on imbalanced data
- [ ] precision vs recall
- [ ] overfitting detection and fixes
- [ ] train/validation/test split
- [ ] model with 99% accuracy - are u happy?
- [ ] explain a model to non-technical stakeholder
- [ ] feature u created and why it helped

## GenAI / LLM question

u will likely be asked how u use AI tools.

good answer: u use LLMs to draft/debug SQL, explain errors, and scaffold boilerplate, but u read, test, and own the output. mention RAG/vector DBs at a high level. dont overclaim fine-tuning or production LLM pipelines unless u actually did them.

## behavioral prompts

use STAR: Situation -> Task -> Action -> Result.

- [ ] analysis changed a decision
- [ ] found a data-quality problem
- [ ] explained technical result to non-technical person
- [ ] project failed or model was wrong
- [ ] disagreed with stakeholder about what data said

## take-home checklist

most common for analyst/DS: CSV + open prompt.

- [ ] clear question up front
- [ ] answer at the end
- [ ] clean commented notebook
- [ ] data-quality checks before analysis
- [ ] honest caveats
- [ ] short written summary

time-box it. focused 3-hour narrative beats a sprawling 12-hour notebook with no conclusion.

[Job Hunt](05-job-hunt.md) - [Hub](README.md) - [Certifications](certifications.md)
