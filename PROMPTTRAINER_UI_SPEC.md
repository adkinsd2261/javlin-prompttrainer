# PromptTrainer UI Specification

## 1. Onboarding Flow
1. **Welcome Splash**  
   - Headline: “Welcome to Javlin”  
   - Subhead: “Master AI evaluator tests—one drill at a time.”  
   - CTA: “Let’s Get Started”

2. **Tour Step 1: Ranking Demo**  
   - Show sample prompt + two colored example responses  
   - Tooltip: “Drag to rank 1 (poor)–5 (excellent)”

3. **Tour Step 2: Coaching Preview**  
   - After selecting a rank, show AI‐coaching panel  
   - Tooltip: “Here’s why a 5/5 looks like this”

4. **Tour Step 3: Rewrite Demo**  
   - Display a low‐score response with an edit box  
   - Tooltip: “Rewrite this and click ‘Coach Me’ for feedback”

## 2. Practice Screen
- **Layout**: Prompt at top, answer cards beneath.  
- **Controls**:  
  - Rank slider (1–5) on each card  
  - “Submit” button  
- **Post‐submit**:  
  - Show AI exemplar in a right‐side panel  
  - “Was this helpful? Yes/No” toggle

## 3. Rewrite Mode
- **Trigger**: Button on practice result panel  
- **UI**:  
  - Text area pre‐filled with original response  
  - “Coach Me” button  
  - Coaching panel beneath with AI critique

## 4. Dashboard
- **Streak Display**: Large counter + calendar heatmap  
- **XP Bar**: Shows progress toward next level  
- **Recent Activity**: List of last 5 drills with scores  
- **Badges Shelf**: Icons for milestones (e.g. “First 5/5”)

## 5. Account & Billing
- Profile info (email, plan)  
- Plan selector (Free / Pro / Team)  
- Payment method form (Stripe embed)  
- Notification preferences (email / push)

## 6. Error & Empty States
- **Network Error**: Full‐screen retry CTA  
- **No Prompts Left** (free tier): Upsell banner to Pro  
- **Loading**: Skeleton cards for prompts, spinner for panels  
