---
name: weighted-scoring
description: "Use when the user wants to prioritize using a weighted scoring model, multiple criteria, or a custom scoring framework. Triggers on: 'weighted scoring', 'weighted matrix', 'scoring model', 'multi-criteria prioritization', 'custom scoring', 'prioritization matrix'."
---

# Weighted Scoring Prioritization

## Purpose
Create a custom prioritization model that weights multiple criteria according to your specific strategic context — more flexible than RICE when you have unique strategic factors.

## How Weighted Scoring Works

1. **Define criteria** (what matters for your prioritization)
2. **Assign weights** to each criterion (total = 100%)
3. **Score each item** on each criterion (1-5 scale)
4. **Calculate weighted score**: Σ (score × weight) for each item
5. **Rank by total weighted score**

## Criteria Categories

### Value Criteria (what we gain)
- Strategic alignment (does this advance our 1-year goal?)
- Customer value (how much do users benefit?)
- Revenue potential (near-term revenue impact)
- Competitive differentiation (does this separate us from competitors?)

### Cost Criteria (what we spend — these have negative weight or are divisors)
- Development effort
- Operational complexity
- Technical debt added

### Risk Criteria (what could go wrong)
- Technical risk
- Market/adoption risk
- Regulatory risk

### Time Criteria
- Time sensitivity (is there a window of opportunity?)
- Short-term vs long-term payoff

## Standard Weights by Business Context

**Growth-focused company:**
| Criterion | Weight |
|---|---|
| Revenue potential | 30% |
| Reach / # users affected | 25% |
| Strategic alignment | 20% |
| Development effort (inverse) | 15% |
| Competitive differentiation | 10% |

**Platform/infrastructure team:**
| Criterion | Weight |
|---|---|
| Developer productivity impact | 30% |
| Technical debt reduction | 25% |
| Scalability | 20% |
| Effort (inverse) | 15% |
| Reliability improvement | 10% |

**Enterprise product:**
| Criterion | Weight |
|---|---|
| Customer retention impact | 30% |
| Sales enablement | 25% |
| Strategic alignment | 20% |
| Effort (inverse) | 15% |
| Compliance/security | 10% |

## Weighted Scoring Table

| Initiative | Criterion A (30%) | Criterion B (25%) | Criterion C (20%) | Effort Inv (15%) | Criterion E (10%) | **Total** |
|---|---|---|---|---|---|---|
| Feature 1 | 4 (1.2) | 3 (0.75) | 5 (1.0) | 3 (0.45) | 4 (0.4) | **3.80** |
| Feature 2 | 2 (0.6) | 5 (1.25) | 3 (0.6) | 5 (0.75) | 2 (0.2) | **3.40** |

## Calibration Step
Before scoring your real backlog:
1. Score 2-3 items everyone agrees on (one obvious high priority, one obvious low)
2. Check if the model reflects those intuitions
3. Adjust weights if not

## Combining with Short/Long-Term Goals
Add two columns:
- Short-term impact score (0-3 months horizon)
- Long-term impact score (6-18 month horizon)
Weight them based on your current strategic phase.

## Output Format
- Custom criteria list with weights (validated with team)
- Weighted scoring table
- Ranked backlog with scores
- Sensitivity analysis: What changes if we adjust top weight by 10%?
