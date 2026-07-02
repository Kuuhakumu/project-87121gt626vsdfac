# Goal 2: core web and data skills meow

> **~180h total** - your pace, no deadline.
> goal: build full web applications - a frontend that talks to a backend that talks to a database.
> this is what most entry roles screen for.

[Previous: Goal 1](01-foundations.md) - [Hub](README.md) - [Next: Goal 3](03-dsa-interview.md)

---

- [ ] **frontend: HTML, CSS, JavaScript, TypeScript, React** (~70h)
- [ ] **backend: APIs, servers, auth** (~70h)
- [ ] **databases and SQL** (~40h)
- [ ] **tooling while u build** (ongoing)
- [ ] **exit check** - one deployed full-stack thing with frontend, API, DB, tests/tooling basics

this goal is where u become employable. even if u target backend or mobile, cover frontend basics; every developer needs to understand the client side.

> **2026 stack note:** TypeScript is now the professional default, not a bonus. React + Next.js is the frontend hiring benchmark. PostgreSQL is the database to learn. Docker is near-baseline. use **Vite**, not deprecated Create React App.

## frontend - HTML, CSS, JavaScript, then React (~70h)

- [ ] **HTML:** semantic elements, forms, accessibility basics (`alt`, labels, ARIA, keyboard nav)
- [ ] **CSS:** box model, Flexbox, Grid, responsive design, Tailwind CSS
- [ ] **JavaScript DOM:** select/manipulate elements, events, `fetch`, async/await, JSON, ES modules
- [ ] **TypeScript:** types, interfaces, generics basics, strict mode
- [ ] **React:** functional components, hooks, props, lifting state, component model, Vite tooling
- [ ] **Next.js:** App Router, server vs client components, routing, data fetching

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Frontend Mentor](https://www.frontendmentor.io/) | Web | Implement real design files pixel-accurately, peer review | Freemium |
| [JavaScript30](https://javascript30.com/) | Web | Build 30 vanilla-JS projects in 30 days, no frameworks | **Free** |
| [Flexbox Froggy](https://flexboxfroggy.com/) + [Grid Garden](https://cssgridgarden.com/) | Web | Master CSS layout via puzzles | **Free** |
| [Scrimba - Learn React](https://scrimba.com/) | Web | Build apps by editing instructor code live in-video | Freemium |
| [Full Stack Open](https://fullstackopen.com/en/) | Web | React, state management, hooks - university-grade, free cert | **Free** |

**practice gate:** build and deploy a responsive multi-page site to [Vercel](https://vercel.com/) or [Netlify](https://www.netlify.com/) that fetches and displays data from a public API.

## backend - APIs, servers, authentication (~70h)

- [ ] **HTTP fundamentals:** GET/POST/PUT/DELETE, status codes, headers, request/response cycle
- [ ] **REST API design:** resource naming, JSON payloads, error responses
- [ ] **backend framework:** Python [FastAPI](https://fastapi.tiangolo.com/) or Django, or JS/TS Node + Express
- [ ] **authentication:** sessions vs JWT, password hashing, never storing plaintext passwords
- [ ] **input validation and error handling**
- [ ] **environment variables and secrets:** `.env`, never commit secrets

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Full Stack Open part 3+](https://fullstackopen.com/en/) | Web | Build a Node/Express REST API with a database | **Free** |
| Backend track | [Boot.dev](https://www.boot.dev/) | HTTP servers, REST, auth in Python/Go with auto-graded exercises | Freemium |
| [CS50 Web (Django)](https://cs50.harvard.edu/web/) | Web | Build web apps with Django, SQL, JS | **Free** |
| API prototyping | [Replit](https://replit.com/) | Spin up and host a backend in-browser, zero setup | Freemium |

**practice gate:** build a REST API with at least one authenticated endpoint, input validation, and a database behind it. document it; FastAPI gives u OpenAPI docs free.

## databases and SQL (~40h)

- [ ] **relational concepts:** tables, primary/foreign keys, relationships, normalization basics
- [ ] **SQL:** `SELECT`, `WHERE`, `JOIN`, `GROUP BY`, aggregations, subqueries, `INSERT`/`UPDATE`/`DELETE`
- [ ] **PostgreSQL:** the 2026 default for new projects
- [ ] **ORM:** SQLAlchemy/Django ORM, Prisma, or the equivalent for your stack
- [ ] **NoSQL awareness:** MongoDB/document stores and when they fit

always learn SQL first. its the interview benchmark and transfers everywhere. NoSQL is later, not a substitute.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [SQLBolt](https://sqlbolt.com/) | Web | 19 interactive lessons: SELECT -> joins -> subqueries | **Free** |
| [freeCodeCamp Relational DB cert](https://www.freecodecamp.org/learn/relational-database/) | Web | SQL + PostgreSQL in a real VS Code environment, 5 projects | **Free** |
| [CS50x Week 7 (SQL)](https://cs50.harvard.edu/x/) | Web | Query real datasets (movies, crime data) | **Free** |

**practice gate:** design a normalized schema for a small app (3+ related tables), write JOINs across them, and wire it to your backend from the previous section.

## tooling while u build (ongoing)

these arent a separate block. pick them up as u build.

| Tool | What to know | Why |
|---|---|---|
| **Docker** | `Dockerfile` basics, `docker compose` for local dev | expected even at entry |
| **Testing** | Vitest/Jest or pytest unit tests | untested portfolio code is a red flag |
| **npm/pnpm** or **pip/uv** | install packages, run scripts, lock files | daily-use baseline |
| **GitHub Actions** | simple CI workflow: lint + test on push | entry-level CI/CD standard |
| **AI tools** | Copilot/Cursor for boilerplate, but understand every line | fluency expected; blind dependence disqualifies |

research shows many experienced developers distrust AI output. use AI to move faster, but the skill that gets u hired is knowing when its wrong.

## exit check

- [ ] built and deployed a responsive frontend that consumes an API
- [ ] built a REST API with auth, validation, and a database
- [ ] comfortable writing SQL JOINs and designing a schema
- [ ] used Docker for local dev and written at least some tests
- [ ] one full-stack thing running at a real URL

[Next: Goal 3 - DSA & Interview Prep](03-dsa-interview.md)
