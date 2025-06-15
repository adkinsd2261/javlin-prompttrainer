# PromptTrainer by Javlin — UI Spec v1.1

---

## 🗺️ Page Routes

- `/dashboard` — Overview of XP, cert status, recent history
- `/train` — Skill Drills with rubric and feedback
- `/evaluate` — Evaluator Sim: timed prompt trials
- `/certify` — Final certification prompt
- `/admin` — Prompt manager + user cert view

---

## 🧱 Component Guide

### Global
- Top nav (app name, user avatar, XP bar)
- Sidebar (Trainer, Evaluator, Cert, Admin links)
- Modal for feedback, error, or success states

### `/train`
- Prompt card
- Textarea for user input
- Rubric scale (5 sliders or pill buttons)
- Feedback modal (on submit)

### `/evaluate`
- Timer (60–90 seconds)
- Lock input when time runs out
- Show results summary after 5 prompts

### `/dashboard`
- XP tracker ("Signal Points")
- Badge display (certs, ranks)
- Progress snapshot: % passed, history, cert eligibility

---

## 🧩 UI Behavior

| Scenario | Behavior |
|----------|----------|
| User not logged in | Redirect to login |
| Trainer mode active | Feedback shown after submit |
| Evaluator mode active | No feedback until full session ends |
| Score <16 | Show "Needs Work" modal |
| Score 16–20 | Show "Retry" option |
| Score 21–25 | Show "Pass" with XP boost |

---

## 📱 Mobile-First Design Rules

- Collapse sidebar into hamburger menu
- Use stacked card layout for prompts
- Increase tap areas (min 44px)
- Modal buttons full-width on mobile
- Swipeable prompt history preview on `/dashboard`

---

## 🧠 UX Feedback System

- Feedback delivered via modal w/ rubric lines:
  - “Clarity: You missed key supporting detail.”
  - “Brevity: Response was overly long for platform X.”
- Retry option = resets prompt
- XP = awarded only for Pass

---

## 🧪 Trainer vs Evaluator UX Differences

| Feature         | Trainer Mode    | Evaluator Sim       |
|-----------------|------------------|----------------------|
| Feedback        | Instant, by rubric | Only after session |
| Timer           | None             | 60–90 seconds        |
| Retry option    | Unlimited        | 1 retry max          |
| XP awarded      | Yes              | Bonus if passed      |

---

**Version**: v1.1  
**Last Updated**: 2025-06-15  
