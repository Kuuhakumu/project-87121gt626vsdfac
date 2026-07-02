# Interview prep: Product Management meow

> PM interviews assess judgment, not correctness.
> structure, tradeoffs, and honest reasoning matter more than guessing the interviewer's favorite answer.

[Previous: Goal 5](05-job-hunt.md) - [Hub](README.md)

---

- [ ] **product sense**
- [ ] **metrics**
- [ ] **estimation**
- [ ] **technical**
- [ ] **behavioral**
- [ ] **strategy and roadmap**
- [ ] **AI / LLM answer**
- [ ] **APM prep**

## interview formats

| Format | Whats tested |
|---|---|
| **Product sense / product design** | frame a user problem, prioritize, propose measurable solution |
| **Analytical / metrics** | define metric, diagnose drop, design fair experiment |
| **Estimation / market sizing** | reason from assumptions to a defensible number |
| **Technical** | work credibly with engineers, understand basic systems |
| **Behavioral / leadership** | influence without authority, collaboration, recovery from failure |
| **Strategy / roadmap** | defend prioritization with incomplete information |

there is no universal right answer.
interviewers evaluate how u think.

## product sense / product design

prompts:

- [ ] "Design a product for elderly users who want to stay connected with family."
- [ ] "How would you improve Google Maps?"
- [ ] "Design an alarm clock for blind users."

### framework

1. **Clarify scope** - ask 1-2 questions before diving in.
2. **Define the user** - pick a specific segment, not "all users."
3. **State goals and pain points** - what are they trying to do? where does it break?
4. **Brainstorm solutions** - generate 3-5 options before choosing.
5. **Prioritize** - pick top 1-2 and justify with impact, feasibility, need.
6. **Define success** - metric, North Star, or leading indicator.
7. **Acknowledge tradeoffs** - downsides, risks, what to watch.

**practice gate:** u can handle an unfamiliar product design prompt in under 8 minutes with clear structure.

## analytical / metrics

prompts:

- [ ] "DAU on messaging dropped 15% last Tuesday. investigate."
- [ ] "New onboarding flow launched. what metric measures success?"
- [ ] "Define the North Star metric for Spotify."

### diagnosing a metric drop

1. **Confirm data** - real drop or instrumentation issue?
2. **Segment** - platform, region, cohort, new vs retained users.
3. **Check external events** - holiday, competitor, media, store policy.
4. **Trace the funnel** - acquisition, activation, engagement, retention.
5. **Form hypotheses** - 3-5 plausible causes ranked by likelihood.
6. **Propose investigation** - query or experiment for each hypothesis.
7. **Recommend response** - what to do once cause is known.

### good PM metric

- [ ] measurable
- [ ] leading, not lagging
- [ ] sensitive to what youre building
- [ ] not gameable in harmful ways

**practice gate:** u can run a coherent "metric dropped X%" investigation and end with prioritized hypotheses plus next step.

## estimation

prompts:

- [ ] "How many Uber rides happen in New York City on a Friday night?"
- [ ] "Estimate market size for subscription dog food."
- [ ] "How many iPhones are sold globally per year?"

estimation is about decomposition and assumptions, not the exact number.

approach:

1. state the approach before calculating.
2. make assumptions explicit.
3. do math out loud with round numbers.
4. sanity-check the result.
5. name the biggest uncertainty.

**practice gate:** u can estimate "how many X" end to end in under 5 minutes with assumptions and sanity check.

## technical

PM-level technical questions do not require code.
they test whether u can work with engineers.

topics:

- [ ] APIs: REST endpoints, failure modes, client calls
- [ ] databases: relational SQL vs NoSQL, when each fits
- [ ] system architecture: client -> server -> database, microservices, CDN
- [ ] latency vs throughput, p99 latency
- [ ] A/B testing infrastructure, randomization, holdouts
- [ ] SQL basics: `SELECT`, `GROUP BY`, `JOIN`

common prompts:

- [ ] "What happens when a user clicks Post on Instagram?"
- [ ] "Feature works for 99% of users but times out for 1%. how do u prioritize?"
- [ ] "Synchronous vs asynchronous processing. why choose each?"
- [ ] "Our API is slow under load. what questions do u ask engineering?"

**practice gate:** u can explain what happens between a click and data appearing on screen without handwaving "the computer just does it."

## behavioral / leadership

PM behavioral questions test influence without authority, collaboration, and ambiguity.

use STAR: **Situation -> Task -> Action -> Result**.
lead with result if strong.

### question bank

- [ ] "Tell me about a time you got engineering to prioritize something they didnt want to build."
- [ ] "Tell me about a time you had to cut scope. how did u decide?"
- [ ] "Tell me about a time you disagreed with a designer, engineer, or stakeholder."
- [ ] "Tell me about a time you pushed back on leadership for the user."
- [ ] "Tell me about a product decision that didnt work out."
- [ ] "Tell me about a time u made a decision with incomplete information."

what interviewers want: evidence, tradeoffs, communication, whether u changed your mind when the data said to.

## strategy and roadmap

prompts:

- [ ] "Youre PM for Gmail. what would you work on next quarter and why?"
- [ ] "We have 20 enterprise requests and 6 weeks of engineering time. what do we build?"

approach:

1. frame strategy: what is the product trying to accomplish in this horizon?
2. segment ideas: growth, activation, retention, monetization, infrastructure/debt.
3. apply a framework: RICE or ICE, and say what u would score.
4. show tradeoffs: what gets deprioritized and why.
5. define success metric.

## AI / LLM question

u will be asked:
**"How do you see AI changing product management?"**
or:
**"How do you use AI in your PM work?"**

strong answer signals:

- [ ] u use AI now for drafts, user research summaries, acceptance criteria drafts
- [ ] u verify and own the output
- [ ] u understand tactical Product Owner work is most exposed
- [ ] u understand durable PM value: discovery, empathy, prioritization judgment, stakeholder influence
- [ ] if interested in AI PM, u understand non-deterministic outputs, evaluation, responsible AI, model drift

dont overclaim.
"i use Claude to draft user stories and then review carefully" is better than pretending u built a full LLM pipeline.

## APM-specific prep

APM interviews differ from standard PM loops.
expect:

- [ ] product design questions
- [ ] analytical cases from charts or drop-off data
- [ ] why PM / why this company
- [ ] estimation
- [ ] behavioral examples showing influence, user empathy, curiosity

APM prep resource: [Exponent](https://www.tryexponent.com) has an APM question bank. use the free tier at minimum.

## quick-drill list

run 2-3 per day.

**product sense**

- [ ] improve YouTube home feed
- [ ] design a product for chronic illness management
- [ ] choose a health metric for Slack

**metrics**

- [ ] define "active user" for B2B SaaS
- [ ] retention dropped 8% month over month. investigate.
- [ ] onboarding sign-ups rose 12% but day-7 retention dropped 5%. what now?

**estimation**

- [ ] pizzas ordered in the US on Super Bowl Sunday
- [ ] TAM for grocery delivery

**technical**

- [ ] what happens when a user searches on Google?
- [ ] whats a webhook, and when use it instead of polling?

**behavioral**

- [ ] a time u said no to a customer request
- [ ] a time u changed your mind based on data
- [ ] a feature u shipped that youre proud of and one youd redo

---

[Previous: Goal 5](05-job-hunt.md) - [Hub](README.md) - [Certifications](certifications.md)
