# 🌐 Phase 2: Core Web & Data Skills

> **~180 hrs total** · your pace, no deadline
> Goal: build full web applications — a frontend that talks to a backend that talks to a database. This is the skill set most entry roles screen for.

[← Phase 1: Foundations](01-foundations.md) · [Hub](README.md) · [Next: Phase 3 →](03-dsa-interview.md)

---

This phase is where you become employable. By the end you'll have built something that runs in a browser, stores data, and is live at a real URL. Even if you're targeting backend or mobile, cover the frontend basics — every developer needs to understand the client side.

> **2026 stack note (from research):** TypeScript is now the professional default, not a bonus. React + Next.js is the frontend hiring benchmark. PostgreSQL is the database to learn. Docker is near-baseline. Use **Vite**, not the deprecated Create React App.

---

## Frontend — HTML, CSS, JavaScript, then React (~70 hrs)

### What to cover
- **HTML:** semantic elements, forms, accessibility basics (alt text, labels, ARIA, keyboard nav)
- **CSS:** the box model, Flexbox, Grid, responsive design (media queries), a utility framework — **Tailwind CSS** is the 2026 standard (Bootstrap is dated)
- **JavaScript (DOM):** selecting/manipulating elements, events, `fetch` + async/await, working with JSON, ES modules
- **TypeScript:** types, interfaces, generics basics, strict mode — learn it early, treat it as default
- **React:** functional components + hooks (`useState`, `useEffect`, `useContext`), props, lifting state, the component model, **Vite** for tooling
- **Next.js:** the App Router, server vs client components, routing, data fetching — increasingly expected for full-stack roles

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Frontend Mentor](https://www.frontendmentor.io/) | Web | Implement real design files pixel-accurately, peer review | Freemium |
| [JavaScript30](https://javascript30.com/) | Web | Build 30 vanilla-JS projects in 30 days, no frameworks | **Free** |
| [Flexbox Froggy](https://flexboxfroggy.com/) + [Grid Garden](https://cssgridgarden.com/) | Web | Master CSS layout via puzzles | **Free** |
| [Scrimba — Learn React](https://scrimba.com/) | Web | Build apps by editing instructor code live in-video | Freemium |
| [Full Stack Open](https://fullstackopen.com/en/) | Web | React, state management, hooks — university-grade, free cert | **Free** |

**Practice gate:** build and deploy a responsive multi-page site (to [Vercel](https://vercel.com/) or [Netlify](https://www.netlify.com/), free) that fetches and displays data from a public API.

---

## Backend — APIs, servers & authentication (~70 hrs)

### What to cover
- **HTTP fundamentals:** methods (GET/POST/PUT/DELETE), status codes, headers, the request/response cycle
- **REST API design:** resource naming, JSON payloads, error responses
- **A backend framework** (pick one matching your language):
  - **Python:** [FastAPI](https://fastapi.tiangolo.com/) (modern, async, auto-docs) or Django (batteries-included)
  - **JS/TS:** Node + Express (the learning baseline)
- **Authentication:** sessions vs JWT, password hashing, why you never store plaintext passwords — consistently the #1 topic juniors fumble in interviews
- **Input validation & error handling**
- **Environment variables & secrets** (`.env`, never commit them)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Full Stack Open part 3+](https://fullstackopen.com/en/) | Web | Build a Node/Express REST API with a database | **Free** |
| Backend track | [Boot.dev](https://www.boot.dev/) | HTTP servers, REST, auth in Python/Go with auto-graded exercises | Freemium |
| [CS50 Web (Django)](https://cs50.harvard.edu/web/) | Web | Build web apps with Django, SQL, JS | **Free** |
| API protyping | [Replit](https://replit.com/) | Spin up & host a backend in-browser, zero setup | Freemium |

**Practice gate:** build a REST API with at least one authenticated endpoint, input validation, and a database behind it. Document it (FastAPI gives you OpenAPI docs free).

---

## Databases & SQL (~40 hrs)

### What to cover
- **Relational concepts:** tables, primary/foreign keys, relationships (1-to-many, many-to-many), normalization basics
- **SQL:** `SELECT`, `WHERE`, `JOIN` (inner/left), `GROUP BY`, aggregations, subqueries, `INSERT`/`UPDATE`/`DELETE`
- **PostgreSQL** specifically — the 2026 default for new projects
- **An ORM** (how your framework talks to the DB): SQLAlchemy/Django ORM (Python), Prisma (JS/TS)
- Awareness of **NoSQL** (MongoDB) and when a document store fits

> **Always learn SQL first.** It's the interview benchmark and the skill that transfers everywhere. NoSQL is a later add-on, not a substitute.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [SQLBolt](https://sqlbolt.com/) | Web | 19 interactive lessons: SELECT → joins → subqueries | **Free** |
| [freeCodeCamp Relational DB cert](https://www.freecodecamp.org/learn/relational-database/) | Web | SQL + PostgreSQL in a real VS Code environment, 5 projects | **Free** |
| [CS50x Week 7 (SQL)](https://cs50.harvard.edu/x/) | Web | Query real datasets (movies, crime data) | **Free** |

**Practice gate:** design a normalized schema for a small app (3+ related tables), write JOINs across them, and wire it to your backend from the previous section.

---

## Tooling you must know (ongoing)

These aren't a separate block — pick them up as you build:

| Tool | What to know | Why |
|---|---|---|
| **Docker** | `Dockerfile` basics, `docker compose` for local dev | Near-universal in 2026 (+17pt jump); expected even at entry |
| **Testing** | Vitest/Jest (JS), pytest (Python) — write unit tests | Untested portfolio code is a red flag |
| **npm/pnpm** or **pip/uv** | Install packages, run scripts, lock files | Daily-use baseline |
| **GitHub Actions** | A simple CI workflow: lint + test on push | The entry-level CI/CD standard |
| **AI tools** | Copilot/Cursor for boilerplate — but understand every line | Fluency expected; blind dependence disqualifies |

> **On AI tools:** research shows 46% of experienced developers actively distrust AI output. Use AI to move faster, but the skill that gets you hired is **knowing when it's wrong**. Never submit code you can't explain.

---

## Phase 2 exit checklist
- [ ] Built & deployed a responsive frontend that consumes an API
- [ ] Built a REST API with auth, validation, and a database
- [ ] Comfortable writing SQL JOINs and designing a schema
- [ ] Used Docker for local dev and written at least some tests
- [ ] One full-stack thing running at a real URL

Next: [Phase 3 — DSA & Interview Prep →](03-dsa-interview.md)
