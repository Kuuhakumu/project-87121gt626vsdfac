# 🎤 Interview Prep — Data, AI & Analytics

> Question bank + format guide. Interviews differ by track — find your track below, then drill the shared SQL bank (every track screens for SQL).

[← Job Hunt](05-job-hunt.md) · [Hub](README.md)

---

## Interview formats by role

| Role | Typical pipeline |
|---|---|
| **Data / BI Analyst** | SQL screen → take-home analysis (CSV + notebook) → stakeholder presentation |
| **Analytics Engineer** | SQL screen → dbt/modeling exercise → data-modeling design discussion |
| **Data Engineer** | Python/SQL coding screen → pipeline design whiteboard → data architecture system design |
| **Data Scientist** | SQL screen → stats/probability → ML take-home → explain-the-model to a non-technical audience |
| **ML Engineer** (not entry) | LeetCode-style coding → ML system design → model-debugging exercise |

> Worth noting: **every** track starts with a SQL screen. SQL is the one thing you can't skip.

---

## SQL bank (all tracks — drill these cold)

1. **Second-highest value** — return the 2nd-highest salary/score without `LIMIT 1 OFFSET 1` tricks. (Window function or subquery.)
2. **Top-N per group** — top 3 products per category. (`ROW_NUMBER() OVER (PARTITION BY ...)`)
3. **Running total / cumulative sum** — `SUM(...) OVER (ORDER BY ...)`
4. **Month-over-month change** — `LAG()` and a self-comparison.
5. **JOIN types** — explain INNER vs LEFT vs FULL; what happens to unmatched rows.
6. **De-duplicate** — keep the latest row per key (`ROW_NUMBER` + filter).
7. **Gaps & islands** — find consecutive-day streaks. (Classic hard one.)
8. **`WHERE` vs `HAVING`** — when each filters, and why you can't put an aggregate in `WHERE`.
9. **`COUNT(*)` vs `COUNT(col)`** — NULL handling difference.
10. **Anti-join** — rows in A not in B (`LEFT JOIN ... WHERE b.id IS NULL` or `NOT EXISTS`).

> Practice on [DataLemur](https://datalemur.com), [StrataScratch](https://www.stratascratch.com), and [Mode SQL](https://mode.com/sql-tutorial/).

---

## Analyst / BI questions

- **"Walk me through how you'd investigate a metric drop."** Frame: clarify the metric → segment (time, geography, cohort) → check data quality first → form hypotheses → test → recommend.
- Correlation vs causation — give a real example where they diverge.
- A/B test basics: what's a p-value in plain words, what's statistical significance, what's a sample-size pitfall.
- "A stakeholder wants a dashboard — how do you decide what goes on it?" (Start from the decision they need to make, not the data you have.)
- DAX or LOD: a calculation you've built and why.

---

## Analytics Engineer questions

- **dbt:** staging vs marts layers — what belongs in each? What does `ref()` do and why not hardcode table names?
- What's a dbt test and which would you put on a primary key? (`unique`, `not_null`.)
- Star schema: fact vs dimension table — give an example of each.
- Slowly-changing dimensions — what problem do they solve?
- Why run `dbt test` in CI on a pull request?
- Idempotency in a transformation — why it matters.

---

## Data Engineer questions

- **"Design a pipeline that ingests an API daily and lands it in a warehouse."** Cover: extraction, scheduling/orchestration, idempotency, failure handling, storage format (Parquet), and how you'd backfill.
- Batch vs streaming — when each, with a concrete example.
- What's orchestration and why not just cron? (Dependencies, retries, observability, backfills.)
- Parquet vs CSV — why columnar formats for analytics.
- How do you handle a pipeline that fails halfway? (Idempotency, checkpoints, retries.)
- Partitioning a large table — why and how.

---

## Data Science questions

- **Model evaluation:** why accuracy lies on imbalanced data; explain precision vs recall and when you'd optimize each.
- Overfitting — what it is, how you detect it (train/val gap), how you fix it (regularization, more data, simpler model).
- Train/validation/test split — why three, not two.
- "Your model has 99% accuracy — are you happy?" (Probe: base rate, what the cost of each error type is.)
- Explain a model you built to a non-technical stakeholder.
- Feature engineering — a feature you created and why it helped.

---

## The GenAI / LLM question (any track, 2026)

You will likely get: **"How do you use AI tools in your data work?"**

Good answer signals: *I use LLMs to draft and debug SQL, explain unfamiliar errors, and scaffold boilerplate — but I read, test, and own the output. I won't ship a query I can't explain.* Mention you understand RAG / vector-DB concepts at a high level. **Don't overclaim** fine-tuning or production LLM pipelines unless you've actually done them.

---

## Behavioral (STAR) prompts

- "A time your analysis changed a decision."
- "A time you found a data-quality problem — what did you do?"
- "Explaining a technical result to a non-technical person."
- "A project that failed or a model that was wrong — what you learned."
- "Disagreeing with a stakeholder about what the data said."

> Structure every answer: **S**ituation → **T**ask → **A**ction → **R**esult. Lead with the result if it's strong.

---

## The take-home (most common for analyst/DS)

You'll get a CSV and an open prompt. Graders look for:
- **A clear question** stated up front, and an answer at the end (not just charts)
- **Clean, commented code** in a notebook — readable beats clever
- **Data-quality checks** before analysis (nulls, duplicates, outliers)
- **Honest caveats** — what your analysis can't conclude
- **A short written summary** a non-technical reader could follow

> Time-box it. A focused 3-hour submission with a clear narrative beats a sprawling 12-hour one that never lands on a conclusion.

---

[← Job Hunt](05-job-hunt.md) · [Hub](README.md) · [Certifications](certifications.md)
