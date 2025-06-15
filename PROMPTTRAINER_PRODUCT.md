# PromptTrainer by Javlin — Product Spec v1.1

## 🧠 Mission
Make prompt engineering learnable, repeatable, and monetizable — preparing users for evaluator jobs at Outlier, DataAnnotation, Surge, and beyond.

---

## 👤 User Roles

- **Learner**: Anyone training in prompt engineering using Skill Drills
- **Evaluator**: Simulated job-test mode with real constraints
- **Admin**: Manage prompt content, users, and certifications

---

## ✅ MVP Scope

### Included:
- Trainer Mode (prompt + rubric + feedback)
- Evaluator Mode (timed prompt sessions)
- Certification System (PromptPass)
- Admin Dashboard (prompts, scores, certs)
- XP & progress tracking (“Signal Points”)
- PromptPass Badge + downloadable Certificate PDF
- Optional: Donation prompt post-cert

### Excluded:
- Native mobile app
- Paid prompt marketplace
- Real job platform integration

---

## 🎯 Core Features

### 1. Skill Drills (Trainer Mode)
- Practice prompt responses with rubric scoring (Clarity, Relevance, Depth, Brevity, Reasoning)
- Score: 1–5 per category → Total /25
- Feedback generated per rubric area

### 2. Evaluator Sim
- Timed tests mimicking evaluator platform challenges
- No feedback until end of session
- Must pass 3/5 to unlock certification

### 3. PromptPass Certification
- Final challenge prompt scored for mastery
- Generates badge + downloadable PDF
- Verifiable via `/certs/[username]`
- Optional donation option appears after cert is issued

---

## 🧪 Prompt Structure & Logic

### Metadata:
- Difficulty: 1–5
- Category: Writing, Reasoning, Inference, etc.
- Type: Essay, List, Structured Reasoning
- Source: Curated or AI-generated (via admin prompt builder)

### Generation Flow:
1. Admin creates base prompt
2. AI generates variations
3. Admin tags metadata
4. Final prompt published

---

## 🧾 Certification Logic

- Must pass: 3/5 Evaluator prompts
- Then pass: Final Certification prompt
- Output: Verified PDF + badge
- Public proof: `/certs/[username]` link
- Post-cert: Prompt to support the mission (donate)

---

## 💸 Monetization Plan (Updated v1.1)

| Tier             | Includes                                                       | Price  |
|------------------|----------------------------------------------------------------|--------|
| **Free**         | Skill Drills (Trainer Mode), XP tracker, rubric feedback       | $0     |
| **PromptPass**   | Evaluator Mode + Cert Prompt + Feedback + PDF + Badge          | **$20** (one-time) |
| **Optional Support** | Post-cert support button (Buy Me a Coffee / Stripe)            | Custom amount |

---

## 📈 Progress & Gamification

- “Signal Points” XP for successful prompts
- Streak counter + badge unlocks
- Dashboard shows % passed, latest scores, cert eligibility

---

## 🔐 Admin Tools

- Create/edit prompts
- View flagged content
- Review response queues
- Override cert manually
- Export user/pass data
- View donation log (if enabled)

---

## 🧭 Branding

- **Product**: PromptTrainer by Javlin
- **XP**: Signal Points
- **Trainer Prompts**: Skill Drills
- **Evaluator Tests**: Trial Sim
- **Certification**: PromptPass
- **Voice**: Calm. Precise. Motivating.
- **Color Palette**: #0E0E0E, #51C2FF, #FF5151, #EAEAEA
- **Font**: Inter 500/600

---

**Version**: v1.1  
**Last Updated**: 2025-06-15