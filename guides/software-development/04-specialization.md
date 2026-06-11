# 🎯 Phase 4: Specialization Paths

> **~80 hrs total** · your pace, no deadline
> Pick **ONE** track and go deep. A focused full-stack-leaning portfolio beats a shallow tour of everything.

[← Phase 3](03-dsa-interview.md) · [Hub](README.md) · [Next: Phase 5 →](05-portfolio.md)

---

## Choosing your track

| Track | Best if you like… | Core stack (2026) | Market note |
|---|---|---|---|
| 🎨 **Frontend** | Visual polish, UX, immediate feedback | TS, React, Next.js, Tailwind | Most saturated at junior level — go deep to stand out |
| ⚙️ **Backend** | Data, logic, systems, APIs | Python/FastAPI or Node, PostgreSQL, Docker | Less crowded than frontend; strong demand |
| 🔗 **Full-Stack** | Building whole products end-to-end | Next.js + API + DB + auth | Most common title at startups/SMBs |
| 📱 **Mobile** | Shipping apps to real devices | Kotlin / Swift / React Native / Flutter | Narrower but less competition |

> **Most junior roles are "full-stack" at small companies** — usually frontend-heavy with some backend. Full-stack is the safest default if you're unsure.

---

## 🎨 Track A: Frontend

You own the UI layer — what users see and interact with.

### What to cover
- **TypeScript** beyond basics: types, interfaces, generics, strict mode (the professional default now — plain JS signals 2019)
- **React** with hooks (functional components only — class components are legacy at this point)
- **Next.js** (App Router — the current default; Pages Router is maintenance-mode)
- **Tailwind CSS** (the dominant utility framework; Bootstrap is dated)
- **State management** (React Context, then a library if needed)
- **Accessibility** (WCAG 2.2 basics, keyboard nav, ARIA), responsive design, **Core Web Vitals**
- **Fetch/async** data from APIs (not jQuery AJAX)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Learn React | [Scrimba](https://scrimba.com/) | Build notes app, quiz app — edit instructor code live | Freemium |
| Front End Libraries cert | [freeCodeCamp](https://www.freecodecamp.org/learn) | React + 5 projects | **Free** |
| Real UI challenges | [Frontend Mentor](https://www.frontendmentor.io/) | Implement real designs pixel-accurately, peer review | Freemium |
| Frontend roadmap | [roadmap.sh/frontend](https://roadmap.sh/frontend) | Ordered topic graph | **Free** |

### Build
A polished, deployed frontend app (Vercel/Netlify) consuming a real API — with an accessibility audit (Lighthouse score in the README).

---

## ⚙️ Track B: Backend

You build the server logic, APIs, and data layer.

### What to cover
- **Your language + framework:** Python + **FastAPI** (modern, async, auto-docs) or Django (batteries-included); or Node + Express/Fastify
- **REST API design:** resource naming, HTTP methods & status codes, versioning, pagination
- **Databases:** **PostgreSQL** (the default), schema design, relationships, indexes, transactions; an ORM (SQLAlchemy/Prisma/Django ORM)
- **Auth:** JWT vs sessions, password hashing, OAuth basics
- **Validation & error handling**, environment/secrets management
- **Docker** for local dev (`docker compose`) — now a baseline expectation
- **Testing:** pytest (Python) or Vitest/Jest (Node)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Backend path | [Boot.dev](https://www.boot.dev/) | HTTP servers, REST, SQL, Docker (Python→Go) | Freemium |
| Relational DB cert | [freeCodeCamp](https://www.freecodecamp.org/learn) | SQL + PostgreSQL, 5 projects | **Free** |
| SQL fundamentals | [SQLBolt](https://sqlbolt.com/) | 19 interactive lessons: joins, aggregations | **Free** |
| Backend roadmap | [roadmap.sh/backend](https://roadmap.sh/backend) | Ordered topic graph | **Free** |

### Build
A REST API from scratch with auth, a PostgreSQL database, input validation, OpenAPI docs, Dockerized, tested, and deployed (Railway/Render/Fly.io free tiers).

---

## 🔗 Track C: Full-Stack

Frontend + backend competence. The most common junior title at startups.

### What to cover
Everything in Frontend **and** Backend basics, plus:
- A **full-stack metaframework:** Next.js (React + API routes/server actions) is the default
- Connecting a real database (PostgreSQL via Supabase/Railway)
- End-to-end **auth** (NextAuth/Auth.js or Clerk) — the #1 thing juniors fumble
- Basic **deployment & CI/CD** (GitHub Actions → Vercel/Railway)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Full Stack Open | [fullstackopen.com](https://fullstackopen.com/en/) | React, Node, REST, GraphQL, TS — free certificate | **Free** |
| Full-stack path | [The Odin Project](https://www.theodinproject.com/) | Build full apps to GitHub, local-first | **Free** |
| Full-stack roadmap | [roadmap.sh/full-stack](https://roadmap.sh/full-stack) | Ordered topic graph | **Free** |

### Build
A useful full-stack app (habit tracker, recipe manager, finance dashboard) with auth, a real DB, CI/CD, and real users — even 5 friends counts.

---

## 📱 Track D: Mobile

You ship apps to real devices and stores.

### What to cover
- **Android:** Kotlin + Jetpack Compose
- **iOS:** Swift + SwiftUI
- **Cross-platform:** React Native (reuses your React/TS skills) or Flutter (Dart)
- App lifecycle, navigation, local storage, calling REST APIs, store submission

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Android roadmap | [roadmap.sh/android](https://roadmap.sh/android) | Kotlin-first ordered syllabus | **Free** |
| iOS roadmap | [roadmap.sh/ios](https://roadmap.sh/ios) | Swift/SwiftUI ordered syllabus | **Free** |
| React Native roadmap | [roadmap.sh/react-native](https://roadmap.sh/react-native) | Cross-platform from web React | **Free** |

### Build
A real app published to the App Store or Play Store (even a free one). Shipping to a store is a significant differentiator.

---

## Phase 4 exit checklist
- [ ] Chosen ONE track and built its signature project
- [ ] Comfortable with the track's core stack (current 2026 tools, not legacy)
- [ ] At least one project deployed with a live URL
- [ ] Tests written for non-trivial logic
- [ ] Ready to assemble the portfolio in Phase 5

Next: [Phase 5 — Portfolio & Job Hunt →](05-portfolio.md)
