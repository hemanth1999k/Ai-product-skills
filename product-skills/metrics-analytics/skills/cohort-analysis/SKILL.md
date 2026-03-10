---
name: cohort-analysis
description: "Use when the user wants to analyze retention, cohort behavior, engagement trends, or understand how different user groups perform over time. Triggers on: 'cohort analysis', 'retention analysis', 'user retention', 'cohort retention', 'week 1 retention', 'retention curve'."
---

# Cohort Analysis

## Purpose
Understand how groups of users (cohorts) behave over time — to identify retention trends, product improvements, and degradation before it's too late.

## Types of Cohorts

### Acquisition Cohorts
Group users by when they joined (signup week/month).
Use for: Is our product getting better over time? Are newer cohorts retaining better?

### Behavioral Cohorts
Group users by behavior (users who used Feature X in first 7 days).
Use for: What behaviors predict retention? What's the activation metric?

### Size/Segment Cohorts
Group users by company size, plan, or channel.
Use for: Which segments retain best? Who's our best customer?

## Retention Metrics

### N-Day Retention
"What % of users who joined on Day 0 were active on Day N?"
- Day 1 retention: Did they come back the next day?
- Day 7 retention: Did they come back after a week?
- Day 30 retention: Do they still see value after a month?

### Rolling Retention
"What % of users who joined in week X were active in week Y or any later week?"
- Measures "did they ever come back after week N?"
- Better for weekly/monthly apps

### Retention Curve Shape Diagnosis

```
Healthy: Flattens asymptotically (like Slack)
         |████
         |   █
         |    ███████████████  ← holds at some % forever
         +---------------------- time

Dying:   Continues to slope to zero (commodity product)
         |████
         |   ████
         |       ████
         |           ████▼   ← approaching 0
         +---------------------- time
```

If your retention curve approaches zero, you have a product-market fit problem, not a growth problem.

## Activation Analysis (The "Aha Moment")

Find behaviors that correlate with retention:
1. Identify users with high 30-day retention
2. What did they do in their first 7 days that low-retaining users did NOT do?
3. That behavior = your activation metric

Facebook's finding: Add 7 friends in 10 days
Slack's finding: Send 2,000 messages as a team
Twitter's finding: Follow 30 users

## Cohort Retention Table

```
Cohort    | Week 0 | Week 1 | Week 2 | Week 4 | Week 8
----------|--------|--------|--------|--------|-------
Jan Cohort| 100%   | 42%    | 31%    | 24%    | 21%
Feb Cohort| 100%   | 45%    | 34%    | 27%    | 24%  ← improving
Mar Cohort| 100%   | 48%    | 37%    | 30%    | 26%  ← improving
```

Improving retention over time = product improvements working.

## Actionable Outputs from Cohort Analysis

1. **Retention problem diagnosis**: Where does the curve drop fastest?
2. **Activation metric identification**: What behavior predicts retention?
3. **Cohort improvement tracking**: Are product changes actually improving retention?
4. **Segment comparison**: Which customer type retains best → who should you target?

## Output Format
- Cohort retention table
- Retention curve shape diagnosis
- Key drop-off points identified
- Activation metric hypothesis
- Product recommendations
