# 📁 Phase 4: The IT Management Portfolio

> **~70 hrs total** · your pace, no deadline
> An IT management portfolio is a set of thinking artifacts — the documents and decisions you'd actually produce on the job. No code, no visual design. What you write reveals whether you can manage.

[← Phase 3](03-specialization.md) · [Hub](README.md) · [Next: Phase 5 — Job Hunt →](05-job-hunt.md)

---

## What an IT management portfolio actually is

IT management portfolios aren't coding portfolios. You won't commit a GitHub repo of scripts or ship a UI. You'll produce a set of artifacts that demonstrate:

1. **You can assess operational reality** — not just recite ITIL definitions
2. **You can manage risk and communicate it to non-technical stakeholders** — in writing, clearly
3. **You can run a process** — incidents, sprints, vendor decisions, budget cases
4. **You can set direction and measure it** — OKRs, 30/60/90 plans, roadmaps
5. **You understand the full accountability loop** — problem → decision → owner → outcome

> The hiring bar for IT management artifacts is: *would I trust this person to own our IT operations?* That means showing judgment — about priorities, risk, and communication — not just ITSM acronym familiarity. Anyone can define an SLA. Fewer can write a service catalog where the SLAs are actually achievable and the costs are accounted for.

The portfolio lives in a **Notion or Confluence "IT Manager Portfolio" site** (both free at this scale) with a clean index page linking each artifact. Export 2–3 of the strongest pieces as PDF one-pagers so you have something to attach to an application or hand across a table in an interview.

---

## What makes IT management portfolio pieces strong

| Weak | Strong |
|---|---|
| Copied ITIL template with placeholders | Filled-in artifact for a specific fictional company with real decisions visible |
| "Risks: TBD" | 10 risks rated by likelihood × impact with named mitigations and owners |
| Incident timeline with no root cause | Blameless post-mortem with contributing factors, system failures, and action items with due dates |
| OKRs that can't be measured | Each KR has a named metric, a baseline, and a measurement method |
| Business case with no numbers | Cost/benefit table, TCO estimate, and a clear recommendation with rationale |

---

## The 8 portfolio artifacts

### 1. Mock IT Service Catalog

**Scenario:** A 200-person company is scaling fast. IT is reactive — employees don't know what to ask for, how long it takes, or who owns what. You've been asked to build their first IT service catalog.

**What you produce:** A Notion or Confluence page (or a clean Google Sheet) covering 8–10 IT services. For each service:
- Service name and plain-language description
- Service owner (role, not name)
- Who can request it (all staff / manager+ / IT-only)
- How to request it (ticket type, form, or direct contact)
- SLA: response time + resolution target (differentiate P1/P2/P3)
- Fully-loaded cost estimate (license cost + IT labor, even if rough)
- Linked runbook or how-to guide (even a stub)

Example services to include: laptop provisioning, new-hire onboarding, software access requests, password reset, VPN access, printer support, security incident reporting, offboarding/account deactivation, application support triage, mobile device management enrollment.

**Tool:** Notion free or Confluence free (≤10 users). A well-structured Notion database with filtered views by category and owner is particularly effective.

**What it demonstrates:** You understand service ownership, SLA setting, and cost visibility — the three things IT managers field most in budget reviews and audits. The service catalog is often the first artifact a new IT manager is asked to create or clean up.

---

### 2. Blameless Incident Post-Mortem

**Scenario:** At 9:14 AM on a Tuesday, employees across three offices lose access to the company's authentication service. SSO is down. No one can log into email, Slack, or the ERP. The incident is resolved at 11:47 AM. You're the incident commander. Write the post-mortem.

**What you produce:** A Google Doc (or Notion page) following the PagerDuty post-mortem format:
- **Incident summary:** severity (P1), duration, user impact, services affected
- **Timeline:** minute-by-minute from first alert to resolution. Be specific — "9:22 AM: Infra team paged; 9:31 AM: confirmed IdP certificate expired; 9:45 AM: emergency cert renewal initiated…"
- **Contributing factors:** what conditions made this possible? (certificate expiry monitoring not configured; on-call rotation had a gap; runbook for cert renewal was outdated)
- **What went well:** (monitoring caught the outage within 4 minutes; comms to affected users sent within 15 minutes)
- **Action items:** at least 5, each with an owner (role) and a due date. E.g., "Configure cert expiry alerts 30 days out — assigned to: SRE lead — due: [date + 7 days]"
- **Lessons learned:** one paragraph, written in the blameless spirit — systems failed, not people

Length: 600–900 words. The timeline can be a table. Keep the tone factual and forward-looking.

**Tool:** Google Docs (free). Use the PagerDuty post-mortem template at postmortems.pagerduty.com as your starting structure.

**What it demonstrates:** Incident management is the most visible part of an IT manager's job. A well-written post-mortem shows you can run the process, communicate under pressure, and turn failures into systemic improvements — without assigning blame.

---

### 3. Project Charter + RACI Matrix

**Scenario:** The company has decided to migrate 120 employees from individual app logins to a centralized SSO solution. This is a 12-week project. You are the project lead. Write the charter.

**What you produce:** A 1–2 page document (exportable as PDF) containing:
- **Project title and sponsor**
- **Business objective:** why we're doing this (security posture, helpdesk ticket reduction, compliance requirement)
- **Scope:** what's in (all cloud SaaS apps), what's out (on-prem legacy systems — Phase 2)
- **Success criteria:** measurable (e.g., "100% of Tier-1 apps integrated within 12 weeks; helpdesk password-reset tickets reduced by 60%")
- **Key milestones:** 4–6 checkpoints with target dates
- **Risks:** top 3, with mitigation notes
- **RACI matrix:** 6–8 tasks (vendor selection, technical integration, user comms, training, go-live, hypercare) × 5–6 roles (IT Manager, SysAdmin, CISO, HR, Dept Heads, End Users). Every task has exactly one A (accountable).

**Tool:** Asana's project charter template (free) or Miro's RACI template (free, 3 boards). Export the RACI as a 1-page PDF.

**What it demonstrates:** Project charters are the artifact that separates IT managers who ship things from those who work on things indefinitely. The RACI matrix shows you understand accountability structure and can prevent the "who owns this?" problem.

---

### 4. Agile IT Sprint Simulation

**Scenario:** Your IT team runs two-week sprints to manage operational work alongside project work. Set up a sprint in Jira Free, run it to completion, and document the retrospective.

**What you produce:**
- **Backlog in Jira Free:** 15–20 tickets across categories — infrastructure tasks (patch deployment, disk cleanup), security tasks (MFA enforcement audit, vulnerability remediation), vendor renewals (license check, renewal ticket), service requests (onboarding batch, software installs), and one project task (SSO integration spike)
- **Sprint planning:** pick 8–10 tickets for a two-week sprint. For each: story points (use a simple 1/2/3/5 scale), assignee (fictional roles), and acceptance criteria
- **Sprint board:** move tickets through To Do → In Progress → In Review → Done. Simulate 2–3 blockers (a vendor delayed a license renewal; a security ticket revealed a larger problem and was split)
- **Sprint retrospective doc:** what went well, what didn't, one process change for next sprint. Format: simple 3-column table (Went Well / Needs Improvement / Action Item)
- **Velocity note:** how many points did you complete vs. plan? What does that imply for next sprint's capacity?

**Tool:** Jira Free (≤10 users, atlassian.com/software/jira/free). Take screenshots of your sprint board and backlog for the portfolio page.

**What it demonstrates:** More IT teams are running agile operations. This artifact shows you can apply sprint methodology to IT work — not just dev teams — and that you understand capacity planning and retrospective practice.

---

### 5. 90-Day IT Ops Improvement Plan

**Scenario:** You've just been hired as IT Manager at a 300-person company. The outgoing IT lead left minimal documentation. The helpdesk is reactive, there's no service catalog, security policy enforcement is inconsistent, and the team morale is low. Build your 30/60/90-day plan.

**What you produce:** A Notion page or slide deck (3–5 slides or equivalent) structured as:

**Days 1–30 (Listen and assess):**
- Shadow each IT team member for one day
- Audit the current ticket backlog (volume, categories, age)
- Identify the top 3 recurring ticket types
- Meet with department heads: what are their biggest IT frustrations?
- Deliverable: a current-state assessment doc — 1 page, shared with your manager

**Days 31–60 (Quick wins and process fixes):**
- Publish a first-draft service catalog (even 5 services is better than zero)
- Reduce P1 mean-time-to-resolve by 20% through an on-call rotation and clearer escalation path
- Standardize the onboarding/offboarding checklist
- KPIs to track: ticket volume by category, MTTR, SLA breach rate, team utilization

**Days 61–90 (Strategic foundation):**
- Present a 12-month IT roadmap to leadership (3 initiatives, prioritized)
- Launch a quarterly IT team health check
- Propose a budget for one deferred security initiative
- KPIs to track: helpdesk satisfaction score (post-ticket survey), security policy compliance rate, ticket backlog trend

**Tool:** Notion free or Google Slides (free). Embed a simple KPI tracking table.

**What it demonstrates:** The 30/60/90 plan is the most-requested artifact in IT management interviews. It shows strategic thinking, operational awareness, and the ability to set priorities without knowing every detail yet.

---

### 6. Risk Register for an IT Initiative

**Scenario:** The company is migrating its file storage from an on-premises NAS to a cloud storage platform. The migration covers 8 TB of data and 280 users. Build the risk register.

**What you produce:** A Google Sheet or Asana portfolio item with 10–12 risks, each containing:
- **Risk ID** (R-01, R-02…)
- **Risk description:** specific, not generic ("Users save files to local drives during cutover, causing data loss" — not "data loss")
- **Category:** Data / Security / Vendor / People / Timeline
- **Likelihood:** 1–5 scale with descriptor (1 = Rare, 5 = Almost Certain)
- **Impact:** 1–5 scale (1 = Negligible, 5 = Critical)
- **Risk score:** Likelihood × Impact
- **Mitigation:** concrete action (not "monitor the situation")
- **Owner:** role
- **Status:** Open / Mitigated / Closed
- **Residual risk score:** after mitigation

Sort by risk score descending. The top 3 risks should have detailed mitigation notes.

Example risks to include: data corruption during transfer, user adoption failure (shadow IT increases), vendor SLA not met, cost overrun from egress fees, compliance gap if data residency requirements aren't mapped, cutover window causing downtime during business hours.

**Tool:** Google Sheets (free) or Asana's risk register template (free).

**What it demonstrates:** Risk management is a core IT manager competency, especially for projects involving data, vendors, or compliance. A well-structured risk register with likelihood × impact scoring shows you can quantify uncertainty and make defensible prioritization decisions.

---

### 7. OKR Set for an IT Department

**Scenario:** It's Q4 and you're setting OKRs for the IT department for Q1 next year. The company's strategic theme for the year is "operational resilience and security posture." Build a one-quarter OKR set.

**What you produce:** A Notion page structured as:

**Objective 1: Improve IT service reliability**
- KR 1: Reduce P1/P2 mean-time-to-resolve from 4.2 hours to under 2.5 hours
- KR 2: Achieve 99.5% uptime on Tier-1 business systems (measured monthly)
- KR 3: Publish runbooks for the top 5 recurring incident types by Week 6

**Objective 2: Strengthen security baseline**
- KR 1: Reach 100% MFA enrollment across all active accounts (from current 74%)
- KR 2: Complete vulnerability remediation for all critical and high findings from Q4 scan by Week 8
- KR 3: Deliver security awareness training to 90% of staff by end of quarter

**Objective 3: Increase IT team capacity through process efficiency**
- KR 1: Reduce ticket resolution time for Tier-1 requests (password resets, software access) by 40% via self-service portal
- KR 2: Onboard and fully configure 2 new IT team members with documented runbooks, reaching full productivity by Week 6
- KR 3: Complete automation of weekly vulnerability scan reporting (zero manual steps)

For each KR, include: current baseline, target value, measurement method (where does the data come from?), and cadence (weekly check-in metric vs. end-of-quarter binary).

**Tool:** Notion free. Reference the joelparkerhenderson OKR repo (github.com/joelparkerhenderson/objectives-and-key-results) for OKR writing patterns and anti-patterns.

**What it demonstrates:** Setting OKRs for an IT department is a specific skill — IT work is often reactive and hard to measure. This artifact shows you can translate operational work into measurable outcomes and connect IT priorities to business strategy.

---

### 8. Business Case / IT Investment Memo

**Scenario:** The company is running on a legacy helpdesk ticketing system (5 years old, no integrations, poor mobile support, no SLA tracking). You want to replace it. The CFO wants a 2-page business case before approving any budget.

**What you produce:** A Google Doc formatted as an executive memo (2 pages, PDF export):

**Problem statement (half page):**
- Current system limitations with specific evidence: X hours/month of IT staff time lost to manual workarounds; SLA compliance can't be measured; no integration with HRIS for onboarding/offboarding automation
- Business impact: slower incident response, higher IT labor cost, compliance audit risk

**Options analysis:**
| Option | Description | Year-1 Cost | Pros | Cons |
|---|---|---|---|---|
| Status quo | Keep current system | ~$8K (maintenance) | No disruption | Problem persists; tech debt grows |
| Option A | Mid-market ITSM (e.g., Freshservice) | ~$18K (license + setup) | Modern UX, integrations, SLA tracking | Migration effort; change management |
| Option B | Enterprise ITSM (e.g., ServiceNow) | ~$65K+ | Full ITIL suite | Overkill for current size; high admin burden |
| Option C | Build custom on Jira Service Management | ~$12K (license + config) | Existing Jira familiarity | Limited native ITSM features |

**Recommendation:** State Option A or C with rationale. Include a 3-year TCO comparison and the break-even point (e.g., "Option A pays back in 14 months if we recover 8 hours/week of IT staff time currently lost to manual workarounds at fully-loaded cost").

**Implementation note:** 8-week migration plan, phased rollout, hypercare period.

**Tool:** Google Docs (free). The 2-page constraint is intentional — it forces prioritization of what's actually decision-relevant.

**What it demonstrates:** IT managers must sell investments to finance and leadership. A business case that quantifies the problem, compares real options, and gives a recommendation with a payback timeline is the artifact that gets budget approved. This is the one most likely to come up in a panel interview ("walk us through a business case you've built").

---

## Suggested portfolio packaging

**The Notion/Confluence portfolio site:**
Create an index page titled "IT Management Portfolio — [Your Name]." Add a brief intro (2–3 sentences: your background, what these artifacts demonstrate). Link each artifact from the index. Group them: "Operations & Incidents" / "Planning & Strategy" / "Projects & Investment."

**PDF one-pagers to export:**
- The Project Charter + RACI (already designed for 1-page PDF output)
- The Business Case memo (2-page PDF — most likely to be requested as an attachment)
- The 90-Day IT Ops Plan (useful for interview prep: print it, reference it when answering "how do you approach a new IT Manager role?")

**What to do with optional extras:**
If you want to go deeper, add: a Vendor Evaluation Matrix (score 3 vendors on 8–10 criteria for a fictional software purchase), a Change Management Communication Plan (email + Slack sequence for a major IT policy change), or a 12-month IT Roadmap in Miro or Linear. These are strong additions but not required for the gate below.

**Sharing the portfolio:**
Publish the Notion workspace as a public page (or make the Confluence space publicly viewable). Copy the URL. Add it to your resume under "Portfolio" — a single URL, not a list of individual docs. In interviews, open the index page on your screen before the call starts.

---

> **Practice gate:** You have at least 4 artifacts published to one portfolio site, including one incident post-mortem and one business case. Each artifact covers a specific fictional scenario (not generic template placeholders), has named owners, and includes at least one measurable outcome or KPI. The portfolio is accessible via a single public URL.

---

Next: [Phase 5 — Job Hunt →](05-job-hunt.md)
