# 🛠️ Phase 4: Build Your Portfolio

> **~110 hrs total** · your pace, no deadline
> In data, **a portfolio that answers a real question beats a pile of certs.** Build as you learn — don't wait.

[← Phase 3](03-specialization.md) · [Hub](README.md) · [Next: Phase 5 — Job Hunt →](05-job-hunt.md)

---

## What a data portfolio must prove

Hiring managers skim for three things:
1. **Can you actually manipulate data?** (SQL/Python that runs)
2. **Can you reason?** (you asked a real question, not just made a chart)
3. **Can you communicate?** (a written conclusion someone non-technical can follow)

> The most common portfolio mistake: a notebook full of charts with no **question** and no **conclusion**. Every project needs a "so what."

---

## Project standards (every repo)

- A clear `README`: the business question, the data source, your approach, your findings
- **Reproducible:** raw data (or a download script) + the notebook/SQL that produces the result
- A written conclusion in plain language — what you found and what you'd do about it
- Clean, commented code; no dead cells
- A visual (dashboard screenshot or chart) that supports the conclusion

---

## Signature projects by track

| Track | Centerpiece project |
|---|---|
| **Data / BI Analyst** | End-to-end SQL analysis on a public dataset → BI dashboard → written "business question → answer" |
| **Analytics Engineer** | dbt project: raw → staging → marts, with tests + docs + a CI check on PRs |
| **Data Engineer** | Batch pipeline: ingest API data → cloud storage → orchestrate with Prefect/Airflow → containerized |
| **Data Scientist** | Full ML project: framing → EDA → features → model → honest evaluation → "what next" |

### Universal "judgment" project (do this regardless of track)
A project where the **obvious answer is wrong** and you explain why — a model that overfits, a metric that misleads, a correlation that isn't causation. This shows judgment, which is what separates a strong candidate from a bootcamp grad.

### AI-awareness bonus (any track)
Add **one** small LLM-augmented feature — e.g. classify free-text with an LLM API call, or use it to draft/debug SQL — and write a paragraph on where you'd trust it and where you wouldn't. It shows 2026-relevant awareness without overclaiming.

---

## Where to get good data

| Source | Best for | Cost |
|---|---|---|
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Everything, with context | **Free** |
| [data.gov](https://data.gov) | Government / civic data | **Free** |
| [Our World in Data](https://ourworldindata.org) | Clean global indicators | **Free** |
| [UCI ML Repository](https://archive.ics.uci.edu/) | Classic ML datasets | **Free** |
| Public APIs (weather, transit, finance) | Pipeline projects | **Free** |

> Avoid the Titanic / Iris datasets as your *only* projects — every reviewer has seen them. They're fine for learning; just don't let them be your showcase.

---

## Make it visible

- **GitHub:** pin your 2–3 best repos; clean READMEs with the question + conclusion up top
- **A short write-up** per project (README or a blog post) — the narrative matters as much as the code
- **One dashboard** publicly viewable (Power BI / Tableau Public / a Streamlit app)

---

## Phase 4 exit checklist
- [ ] 2–3 polished projects on GitHub, each with a question + conclusion
- [ ] At least one matches your target track exactly
- [ ] One "judgment" project where the obvious answer is wrong
- [ ] One publicly viewable dashboard or app
- [ ] Each README readable by a non-technical hiring manager

Next: [Phase 5 — Resume & job hunt →](05-job-hunt.md)
