# Software Development - Tech Stack & Trends (2026)

> Research date: 2026-06-13. Source: Stack Overflow Developer Survey 2025 (49k+ resp) ✅, roadmap.sh ✅, GitHub Octoverse ⚠️, TIOBE Jun 2026 ✅. Confidence tags inline.

## First language verdict (by goal, not hype)
| Goal | Start with | Add next |
|---|---|---|
| Web frontend | JavaScript → TypeScript | React, CSS fundamentals |
| Fullstack web | JavaScript → TypeScript | Node/Express, then React |
| Backend/API | Python | FastAPI or Django, SQL |
| Data/ML/AI | Python | NumPy, pandas, then PyTorch/scikit-learn |
| Mobile iOS | Swift | SwiftUI |
| Mobile Android | Kotlin | Jetpack Compose |
| Enterprise | Java | Spring Boot |
| Game dev | C# (Unity) or GDScript | - |

SO2025 usage: JavaScript 66% (#1) ✅ · Python 57.9% (#4, fastest-growing +7pt) ✅ · TypeScript 43.6% (treat as default, not optional) ✅ · Java 29.4% · C# 27.8% · Go 16.4% · Rust 14.8% (most admired 72%, NOT a first language).

## Frameworks (2026)
**Frontend:** React 44.7% (hiring benchmark) · Next.js 20.8% (App Router default) · Angular 18.2% (enterprise) · Vue 17.6% · jQuery 23.4% (LEGACY - don't start). Tailwind CSS now dominant utility framework (over Bootstrap).
**Backend:** Node.js 48.7% (+ Express 19.9%) · FastAPI 14.8% (modern Python choice - async, typed, auto-docs) · Django 12.6% · Flask 14.4% · Spring Boot 14.7% · ASP.NET Core 19.7%.
**Databases:** PostgreSQL 55.6% (default for new projects) · MySQL 40.5% · SQLite 37.5% (dev/test) · Redis 28% · MongoDB 24% · Supabase 6% (rising). **Learn SQL first, always.**

## Tooling every junior must know
🔴 Critical: Git+GitHub · VS Code (75.9%) · npm/pnpm (JS) or pip/uv (Python) · basic Linux/CLI.
🟠 High: Docker (+17pt jump 2025, near-universal - know Dockerfile + docker compose) · testing (Vitest/Jest, pytest).
🟡 Important: GitHub Actions CI basics · .env/secrets · project manifest (package.json/pyproject.toml).

## AI-assisted dev (2026)
Adoption (among AI users): ChatGPT 81.7% · GitHub Copilot 67.9% · Gemini 47.4% · Claude/Claude Code 40.8% · Cursor 17.9% (IDE). VS Code still dominant at 75.9%.
Reality: 52% say AI helped productivity ✅ BUT 46% distrust accuracy vs 33% trust; only 3% "highly trust" ✅. **The differentiating skill is judgment** - knowing when output is wrong, explaining every line you ship. Submitting AI code you can't explain disqualifies candidates.

## Portfolio progression (no to-do apps)
1. **Responsive static/component site** - HTML/CSS/JS (+ optional React/Tailwind), deployed (Vercel/Netlify), Lighthouse a11y score in README.
2. **Backend API + database** - FastAPI/Node + PostgreSQL, auth (JWT), validation, OpenAPI docs, Dockerized, tested, deployed (Railway/Render/Fly).
3. **Full-stack app w/ auth + DB + deploy** - the core piece. React+Next (or Vue+Nuxt) + backend + PostgreSQL + auth + CI/CD. Real users = significant.
4. **Real API integration / data pipeline** - external API, data transform, error handling, caching, visualization.
5. **Specialization signal (optional):** RAG/LLM app (real retrieval, not just a chat call) · containerized multi-service + Actions CI + Terraform · merged OSS PR · shipped mobile app.
What hiring managers want: decision-making evidence, tests, clean commit history, real README, deployed URL, stack breadth.

## Learn-this-not-that
TypeScript not plain JS (new) · React hooks not class components · Next.js App Router not Pages Router · FastAPI not Flask (new APIs) · PostgreSQL not Mongo-by-default · write tests not none · Docker Compose not "works on my machine" · GitHub Actions not Jenkins · pnpm/npm not Yarn 1.x · Tailwind not Bootstrap · Supabase/Railway/Render not Heroku · fetch/async-await not jQuery AJAX · **Vite not Create React App (CRA deprecated)**.

## Dated - 2021 cut-list
jQuery as primary skill · React class components · Create React App · REST-only thinking (GraphQL/tRPC/server actions exist) · Heroku deploy target · "master vanilla JS before any framework" (parallel is fine now) · PHP as first backend · certs as a hiring signal for general web dev · Express as the only Node option.
