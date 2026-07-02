# Goal 4: build your portfolio meow

> **~110h total** - your pace, no deadline.
> in data, a portfolio that answers a real question beats a pile of certs.
> build as u learn; dont wait.

[Previous: Goal 3](03-specialization.md) - [Hub](README.md) - [Next: Goal 5](05-job-hunt.md)

---

- [ ] **understand what a data portfolio proves**
- [ ] **meet repo standards**
- [ ] **build a signature project by track**
- [ ] **add one judgment project**
- [ ] **make it visible**
- [ ] **exit check** - 2-3 polished projects, track match, judgment project, public dashboard/app

## what a data portfolio must prove

hiring managers skim for three things:

- [ ] can u manipulate data? SQL/Python runs.
- [ ] can u reason? real question, not random charts.
- [ ] can u communicate? conclusion a non-technical person can follow.

common mistake: notebook full of charts with no question and no conclusion. every project needs a "so what."

## project standards

every repo needs:

- [ ] clear `README`: business question, data source, approach, findings
- [ ] reproducible raw data or download script + notebook/SQL
- [ ] plain-language conclusion
- [ ] clean commented code, no dead cells
- [ ] visual that supports the conclusion

## signature projects by track

| Track | Centerpiece project |
|---|---|
| **Data / BI Analyst** | SQL analysis on public dataset -> BI dashboard -> written business answer |
| **Analytics Engineer** | dbt project: raw -> staging -> marts, with tests + docs + CI check |
| **Data Engineer** | batch pipeline: API -> cloud storage -> Prefect/Airflow -> containerized |
| **Data Scientist** | ML project: framing -> EDA -> features -> model -> honest evaluation -> what next |

## universal judgment project

do this regardless of track:

- [ ] choose a case where the obvious answer is wrong
- [ ] show the misleading metric/correlation/model
- [ ] explain why its wrong
- [ ] write what a better decision would use

this shows judgment, which separates a strong candidate from a chart-generator.

## AI-awareness bonus

add one small LLM-augmented feature, like classifying free text or drafting/debugging SQL, then write where u would and would not trust it.

dont overclaim. this is awareness, not pretending to be an ML platform engineer.

## where to get good data

| Source | Best for | Cost |
|---|---|---|
| [Kaggle Datasets](https://www.kaggle.com/datasets) | many domains, context included | **Free** |
| [data.gov](https://data.gov) | government / civic data | **Free** |
| [Our World in Data](https://ourworldindata.org) | clean global indicators | **Free** |
| [UCI ML Repository](https://archive.ics.uci.edu/) | classic ML datasets | **Free** |
| Public APIs | pipeline projects | **Free** |

avoid Titanic/Iris as your only showcase. fine for learning, weak as a final signal.

## make it visible

- [ ] pin 2-3 best repos on GitHub
- [ ] put question + conclusion at the top of READMEs
- [ ] write a short project post or README narrative
- [ ] publish one dashboard or app: Power BI, Tableau Public, Streamlit

## exit check

- [ ] 2-3 polished projects on GitHub, each with a question + conclusion
- [ ] at least one matches your target track exactly
- [ ] one judgment project where the obvious answer is wrong
- [ ] one publicly viewable dashboard or app
- [ ] each README readable by a non-technical hiring manager

[Next: Goal 5 - Resume & Job Hunt](05-job-hunt.md)
