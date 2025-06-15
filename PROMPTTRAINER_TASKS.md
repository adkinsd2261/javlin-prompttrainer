# PromptTrainer Development Tasks

## Priority Legend
- **P0** = Must deliver in MVP  
- **P1** = Important but can wait until post-MVP  
- **P2** = Nice-to-haves

---

## 1. Backend

- [P0] Auth & User Management  
  - Signup / Login / JWT middleware  
- [P0] Prompt API  
  - `GET /prompts/daily` → returns today’s drills  
  - `POST /prompts/rank` → save rank & feedback  
- [P0] Coaching API  
  - `POST /prompts/coach` → generate 5/5 exemplar via OpenAI  
- [P0] Stats API  
  - `GET /user/stats` → streaks, XP, recent scores  
- [P1] Admin API  
  - `POST /admin/prompts` → upload new prompt sets  
  - `GET /admin/usage` → basic analytics

## 2. Frontend

- [P0] Auth Pages  
  - Login / Signup forms  
- [P0] Practice Component  
  - Drill card, rank slider, submit flow  
- [P0] Coaching Panel  
  - Exemplar display, “helpful” toggle  
- [P0] Rewrite Component  
  - Text area + “Coach Me” button  
- [P0] Dashboard Page  
  - Streak counter, calendar, XP bar, recent activity  
- [P1] Onboarding Tour  
  - Tooltip library integration  
- [P1] Billing UI  
  - Plan switcher, Stripe integration  
- [P2] Leaderboard & Friends

## 3. DevOps & QA

- [P0] CI/CD pipeline (GitHub Actions)  
- [P0] Environment setup docs (`.env.example`)  
- [P0] Unit tests for core APIs  
- [P0] E2E tests: practice → coach → dashboard  
- [P1] Analytics integration (PostHog or GA4)  
- [P1] Rate-limiting / request throttling  
- [P2] Performance monitoring (Sentry)
