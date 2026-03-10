---
name: opportunity-scoring
description: "Use when the user wants to apply Outcome Driven Innovation scoring, opportunity scoring, or Anthony Ulwick's importance-satisfaction framework. Triggers on: 'opportunity scoring', 'ODI', 'outcome driven innovation', 'importance satisfaction', 'underserved needs', 'Ulwick'."
---

# Opportunity Scoring (Outcome-Driven Innovation)

## Purpose
Identify underserved customer needs using Anthony Ulwick's Opportunity Scoring — so you invest where customers care most but are least satisfied.

## The Core Formula

**Opportunity Score = Importance + max(Importance − Satisfaction, 0)**

Where:
- **Importance**: How important is this outcome to the customer? (1-10 scale)
- **Satisfaction**: How satisfied are they with current solutions? (1-10 scale)

The formula amplifies the gap when importance exceeds satisfaction.

## Score Interpretation

| Score | Interpretation |
|---|---|
| ≥ 15 | Extreme opportunity — heavily underserved |
| 12-15 | Strong opportunity — high priority |
| 10-12 | Moderate opportunity |
| < 10 | Overserved — don't invest here |

**Overserved outcomes** (satisfaction > importance): Users are already over-satisfied. Reducing investment here won't hurt.

## How to Run Opportunity Scoring

### Step 1: Define the Job
What is the main "job" the customer is trying to do?
Example: "Complete a project on time with my team"

### Step 2: List Desired Outcomes
Outcomes = customer's criteria for doing the job well
- Must be measurable ("minimize the time it takes to find the latest version of a file")
- Must be from customer's perspective, not feature perspective
- Aim for 50-150 outcomes across the full job

Format: [Direction] + [Metric] + [Object] + [Context]
"Minimize the time it takes to find relevant past decisions when starting a new project"

### Step 3: Survey Customers
For each outcome:
- "How important is it for you to [outcome]?" (1-10)
- "When you [do the job], how satisfied are you with current solutions at [outcome]?" (1-10)

Sample: 100-400 customers per target segment.

### Step 4: Calculate Scores
Apply formula. Rank by opportunity score.

### Step 5: Identify Opportunities
Top 5-10 outcomes = your product roadmap input.
- These are WHAT customers need, not HOW to solve it
- Generate multiple solutions for each opportunity
- The solution with the best product-solution fit wins

## Opportunity Landscape Map

Plot outcomes on a chart:
- X-axis: Satisfaction (low → high)
- Y-axis: Importance (low → high)

**Top-left quadrant** (high importance, low satisfaction) = invest here
**Top-right quadrant** (high importance, high satisfaction) = table stakes, don't break these
**Bottom-left quadrant** (low importance, low satisfaction) = ignore
**Bottom-right quadrant** (low importance, high satisfaction) = overserved, cut investment

## Output Format
- Outcome list with importance, satisfaction, opportunity scores
- Ranked opportunity table
- Opportunity landscape map (described)
- Top 5 opportunities with product implications
