---
name: multivariate-test-design
description: "Use when the user wants to test multiple variables simultaneously, run an MVT, or understand factorial designs. Triggers on: 'multivariate test', 'MVT', 'test multiple variables', 'factorial design', 'test combinations', 'multivariate experiment'."
---

# Multivariate Test (MVT) Design

## Purpose
Test multiple variables simultaneously to find the best combination — more efficient than sequential A/B tests when sample is large enough.

## A/B Test vs MVT: When to Use Which

| | A/B Test | Multivariate Test |
|---|---|---|
| Variables | 1 | 2+ simultaneously |
| Variants | 2 (A and B) | 4+ (all combinations) |
| Sample needed | Lower | Much higher |
| Best for | Definitive decisions on one change | Optimizing multiple elements |
| Learning | "Does this work?" | "What combination works best?" |

**Rule**: Only use MVT when you have enough traffic to reach significance across ALL combinations.

## MVT Design Types

### Full Factorial
Test every possible combination:
- Variable A (2 variants) × Variable B (2 variants) = 4 combinations
- Variable A (3) × Variable B (2) × Variable C (2) = 12 combinations
- Pros: Finds interactions between variables
- Cons: Requires large sample

### Fractional Factorial
Test a strategic subset of combinations:
- Use when full factorial is too expensive
- Orthogonal array design (Latin squares)
- Pros: Smaller sample needed
- Cons: Cannot detect interaction effects

### Taguchi Method
Further reduced set of combinations optimized for detecting main effects:
- Use for manufacturing-derived optimization problems
- Best when interactions between variables are unlikely

## MVT Planning

### Step 1: Select Variables
Choose variables that are:
- Independent (changing one doesn't affect another)
- Measurable in the same experiment
- All on the same page/flow

Bad MVT candidates: Headline + Pricing (different decision points)
Good MVT candidates: Headline + CTA text + Hero image (same landing page)

### Step 2: Define Variants per Variable
- Minimum 2 per variable (including control)
- Maximum practical: 3 variants × 3 variables = 27 combinations (needs huge traffic)

### Step 3: Calculate Sample Size
Required n = (n for single A/B test) × (number of combinations)
Example: 1,000 users per variant × 8 combinations = 8,000 users minimum

### Step 4: Analyze Results
Two types of effects to analyze:
- **Main effect**: Each variable independently (same as A/B)
- **Interaction effect**: Does changing A change the impact of B?

Significant interaction = the variables depend on each other; the "winner" depends on context.

## Concept Testing with MVT
Apply MVT to concept testing:
- Test multiple value propositions × multiple designs
- Measure: conversion rate, time on page, scroll depth
- Find: Which message + design combination drives most action?

## Output Format
- Variable matrix (variables × variants)
- Full combination list
- Sample size requirement
- Duration estimate
- Analysis plan (main effects + interactions)
- Decision rules
