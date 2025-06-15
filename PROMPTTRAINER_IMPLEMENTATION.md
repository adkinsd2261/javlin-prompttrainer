# PromptTrainer Implementation Details

## 1. Tech Stack
- **Frontend**: React + Vite + Tailwind CSS  
- **Backend**: Node.js + Express  
- **AI**: OpenAI API (Chat Completions)  
- **Database**: PostgreSQL (via Prisma ORM)  
- **Auth**: JWT tokens  
- **Payments**: Stripe

## 2. Data Models (PostgreSQL)

```sql
-- users
id           UUID PK
email        TEXT UNIQUE
passwordHash TEXT
xp           INT    DEFAULT 0
streak       INT    DEFAULT 0
plan         TEXT   ("free","pro","team")
onboarded    BOOL   DEFAULT false

-- prompts
id           UUID PK
text         TEXT
responses    JSONB  -- array of sample AI responses
tags         TEXT[] -- drill-pack tags
createdAt    TIMESTAMP

-- attempts
id           UUID PK
userId       UUID FK -> users.id
promptId     UUID FK -> prompts.id
rank         INT
feedback     TEXT
coached      BOOL
createdAt    TIMESTAMP

3. API Endpoints
Auth
POST /api/auth/signup

Body: { email, password }

→ 201 { user, token }

POST /api/auth/login

Body: { email, password }

→ 200 { user, token }

Prompts
GET /api/prompts/daily

Auth required

→ 200 { prompts: [ { id, text, responses } ] }

POST /api/prompts/rank

Body: { promptId, rank, feedback }

→ 201 { attemptId }

POST /api/prompts/coach

Body: { attemptId }

→ 200 { exemplar: { text, rationale } }

Stats
GET /api/user/stats

→ 200 { xp, streak, badges: [], recentAttempts: [] }