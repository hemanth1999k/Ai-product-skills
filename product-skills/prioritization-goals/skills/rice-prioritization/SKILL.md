---
name: rice-prioritization
description: "Use when the user wants to prioritize using RICE scoring, calculate reach/impact/confidence/effort, or rank a backlog quantitatively. Triggers on: 'RICE', 'RICE score', 'RICE prioritization', 'prioritize with RICE', 'reach impact confidence effort'."
---

# RICE Prioritization Framework

## Purpose
Score and rank product initiatives using the RICE framework to make defensible, data-driven prioritization decisions.

## RICE Formula

**RICE Score = (Reach × Impact × Confidence) / Effort**

### R — Reach
How many users/customers will this affect in a given time period?
- Use real data: users per month, transactions per quarter, etc.
- Be specific: "2,000 users per month" not "all users"
- Count only users affected, not all users

### I — Impact
How much will this move the needle per user who is affected?
Use a multiplier scale:
- 3 = Massive impact (primary action changed)
- 2 = High impact (significantly changes behavior)
- 1 = Medium impact (noticeable improvement)
- 0.5 = Low impact (minor improvement)
- 0.25 = Minimal impact (barely noticeable)

### C — Confidence
How confident are you in the Reach and Impact estimates?
- 100% = Data and validated research backs this up
- 80% = Some data, reasonable assumption
- 50% = Gut feeling, no strong data
- Use low confidence to flag "needs more research before we commit"

### E — Effort
Total work required across all team members (not just engineering)
- Measured in person-months or person-weeks
- Include: design, engineering, QA, PM, data
- 0.5 = half a week; 1 = 1 person-month; 3 = 3 person-months

## Scoring Example

| Initiative | Reach | Impact | Confidence | Effort | RICE |
|---|---|---|---|---|---|
| Onboarding redesign | 500/mo | 2 | 80% | 2 | 400 |
| AI suggestions feature | 2000/mo | 1 | 50% | 4 | 250 |
| Export to CSV | 300/mo | 0.5 | 100% | 0.5 | 300 |
| Search improvements | 1500/mo | 1 | 80% | 1 | 1200 |

**Search improvements wins** — high reach, reasonable impact, manageable effort.

## RICE Pitfalls to Avoid

1. **Inflating confidence** — Gut feelings are 50%, not 80%. Be honest.
2. **Ignoring compounding effort** — Include all team time, not just engineering
3. **Scope creep** — Score the MVP version, not the dream version
4. **Comparing apples to oranges** — Only compare items at similar stages of definition

## When to Use RICE
- Large backlog with competing items
- Cross-team prioritization discussions
- When stakeholders each have a "favorite" initiative
- After discovery, before sprint planning

## When NOT to Use RICE
- Strategic bets (innovation) — RICE favors safe, high-reach improvements
- Early-stage when you don't have reliable data for inputs
- When the initiative is about risk reduction (hard to quantify impact)

## Output Format
- RICE scoring table for all submitted initiatives
- Ranked list with scores
- Commentary on assumptions + confidence
- Top 3 recommended items to tackle next
