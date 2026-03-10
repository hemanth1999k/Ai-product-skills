---
name: assumption-mapping
description: "Use when the user needs to identify and prioritize risky assumptions in a product idea, feature, or strategy. Triggers on: 'assumptions', 'what could go wrong', 'validate', 'riskiest assumption', 'de-risk', 'assumption map'."
---

# Assumption Mapping

## Purpose
Surface hidden assumptions in a product idea and prioritize which ones to test first based on risk and importance.

## The 4 Risk Categories (VUBF)

### Value Risk
Will customers want this? Will it solve a real problem?
- "Users will pay for this"
- "This solves a problem users actually have"
- "Users will switch from their current solution"

### Usability Risk
Can customers figure out how to use it?
- "Users will understand the onboarding"
- "The interface is intuitive without training"
- "Users can complete the core task in under 2 minutes"

### Business Viability Risk
Can we build a sustainable business around this?
- "Our CAC will be below $X"
- "Enterprises will buy this, not just use free tier"
- "The margin after infrastructure costs is positive"

### Feasibility Risk
Can we actually build it?
- "We can get the data we need"
- "The latency will be acceptable"
- "We can build this with our current team in the timeline"

## Prioritization Grid

Map each assumption on 2 axes:
- **X-axis**: Importance to the idea succeeding (Low → High)
- **Y-axis**: Evidence we have right now (Strong → Weak)

**Priority 1 (Top Right — High Importance, Weak Evidence):** Test immediately
**Priority 2 (Top Left — Low Importance, Weak Evidence):** Test eventually
**Priority 3 (Bottom Right — High Importance, Strong Evidence):** Monitor
**Priority 4 (Bottom Left):** Ignore for now

## For Each Priority 1 Assumption, Define:
1. The assumption stated clearly
2. The riskiest version of this assumption
3. The cheapest/fastest experiment to test it
4. What "validated" looks like (success metric)
5. What "invalidated" means for the product

## Output Format
- Table: Assumption | Category | Importance (H/M/L) | Evidence (H/M/L) | Priority
- Top 3-5 assumptions to test with experiment suggestions
