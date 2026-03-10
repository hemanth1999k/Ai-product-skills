---
name: north-star-metric
description: "Use when the user needs to define a North Star Metric, NSM, leading indicators, or core product metric. Triggers on: 'north star', 'NSM', 'north star metric', 'core metric', 'what metric should we track', 'define our metric'."
---

# North Star Metric (NSM) Framework

## Purpose
Define the single metric that best captures the core value your product delivers to customers — and connect it to sustainable business growth.

## What Makes a Good NSM

A good North Star Metric is:
1. **Leads revenue** — it predicts future revenue, doesn't just lag it
2. **Represents customer value** — when it goes up, customers are genuinely better off
3. **Actionable by the team** — product, engineering, and design can influence it
4. **Measurable** — you can track it consistently
5. **Single number** — not a ratio of two things you don't understand separately

**Bad NSM examples**: Revenue (lags), DAU (doesn't guarantee value), # features shipped (output, not outcome)
**Good NSM examples**: Airbnb → Nights Booked, Spotify → Time Listening, Slack → Messages Sent per DAU

## Product Game Classification (Sean Ellis / Amplitude)

| Business Type | NSM Direction | Examples |
|---|---|---|
| Attention products | Maximize time/frequency | TikTok: Time in App |
| Transaction products | Maximize transaction value/frequency | Stripe: Payment Volume |
| Productivity products | Maximize tasks completed | Asana: Projects Created |
| Network products | Maximize connections/interactions | LinkedIn: Connections Made |
| Content products | Maximize content consumed or created | YouTube: Watch Time |

## NSM Selection Process

### Step 1: Define the Value Moment
What is the specific moment when a user gets real value from your product?
"The moment when..." — be specific.

### Step 2: Generate NSM Candidates
List 5-10 candidates. For each, ask:
- Does this increase when customers are getting more value?
- Does it predict revenue growth?
- Can the team move it through product decisions?

### Step 3: Pressure Test Each Candidate
- What if this metric went up but customers were worse off? (Goodhart's Law)
- Could this metric be gamed? (e.g., notification spam inflates opens)
- Is it a symptom of value, or actual value?

### Step 4: Define It Precisely
- Exact formula
- Measurement frequency
- Segment scope (all users? paying users?)

## Supporting Metrics (Input Metrics)

The NSM is the output. Identify 3-5 input metrics that drive it:

```
NSM: Weekly Active Teams
↑ driven by:
  → Activation Rate (teams that complete onboarding)
  → Retention Rate (teams active week-over-week)
  → Expansion (teams adding members)
  → Recovery (churned teams reactivated)
```

Each input metric maps to a team/squad.

## Counter-Metrics
For every NSM, define a counter-metric that guards against gaming:
- NSM: Sessions per user → Counter: Session length (not just opening and closing)
- NSM: Messages sent → Counter: Spam rate / unsubscribes

## Output Format
- Recommended NSM with rationale
- NSM formula precisely defined
- 3-5 input/driver metrics
- Counter-metrics
- Current baseline and target
