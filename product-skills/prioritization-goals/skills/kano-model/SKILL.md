---
name: kano-model
description: "Use when the user wants to understand feature delight vs dissatisfaction, apply Kano analysis, or think about basic vs performance vs delighter features. Triggers on: 'Kano', 'kano model', 'delighters', 'basic features', 'performance features', 'what features delight users', 'feature satisfaction'."
---

# Kano Model

## Purpose
Understand which features satisfy users, which delight them, and which they take for granted — to make smarter investment decisions.

## The Five Feature Categories

### Basic Needs (Must-Be)
Users expect these. Their presence doesn't delight; their absence enrages.
- Below baseline = users will churn
- At baseline = no reaction
- Examples: App not crashing, saving user data, basic security

### Performance Needs (One-Dimensional)
More = better. Users explicitly want more of these.
- Linear relationship: more of it → more satisfaction
- Examples: Speed, storage, battery life, report depth

### Excitement Needs (Delighters)
Users didn't know they wanted these. They create unexpected delight.
- Absence = no dissatisfaction (users didn't expect it)
- Presence = significant delight and loyalty
- Examples: Spotify Wrapped, Google Street View, iPhone autocorrect (when it works)
- **Delighters decay**: They become Performance or Basic over time

### Indifferent Features
Users don't care either way. Shipping these is waste.
- Examples: Features users never discover, marginal UX improvements in rarely-used flows

### Reverse Features
Some users prefer these absent. Presence reduces satisfaction.
- Examples: Animations for users who prefer speed, social features for privacy-conscious users

## Kano Functional/Dysfunctional Survey

For each feature, ask TWO questions:
1. "If this feature WERE present, how would you feel?" (Functional)
2. "If this feature were NOT present, how would you feel?" (Dysfunctional)

Scale: I like it / I expect it / I'm neutral / I can tolerate it / I dislike it

Use the Kano evaluation table to classify:

| | Functional (Like) | Functional (Expect) | Functional (Neutral) | Functional (Tolerate) | Functional (Dislike) |
|---|---|---|---|---|---|
| **Dysfunctional (Like)** | Q | D | D | D | R |
| **Dysfunctional (Expect)** | A | I | I | I | M |
| **Dysfunctional (Neutral)** | A | I | I | I | M |
| **Dysfunctional (Tolerate)** | A | I | I | I | M |
| **Dysfunctional (Dislike)** | O | O | O | O | Q |

A=Attractive(Delighter), O=One-Dimensional, M=Must-be, I=Indifferent, R=Reverse, Q=Questionable

## Strategic Implications

| Category | Investment Decision |
|---|---|
| Must-be | Fix problems, don't differentiate on these |
| Performance | Invest proportionally to competitor gaps |
| Delighters | Find these — they're your moat |
| Indifferent | Cut from backlog aggressively |
| Reverse | Segment users or make optional |

## Output Format
- Feature classification for each item
- Investment recommendation by category
- Top delighter opportunities
- Features recommended for cutting (indifferent)
