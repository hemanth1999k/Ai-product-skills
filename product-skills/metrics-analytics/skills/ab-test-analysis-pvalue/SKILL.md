---
name: ab-test-analysis-pvalue
description: "Use when the user wants to analyze A/B test results, interpret p-values, determine statistical significance, or make a ship/no-ship decision. Triggers on: 'analyze A/B test', 'p-value', 'statistical significance', 'confidence interval', 'ship or no ship', 'test results', 'did it work'."
---

# A/B Test Analysis & Ship/No-Ship Decision

## Purpose
Correctly interpret A/B test results using statistical thinking and make principled ship/no-ship decisions.

## Understanding P-Values

**P-value**: The probability of seeing results this extreme (or more) if there were actually no difference.

- p = 0.03 means: "If there's truly no effect, there's only a 3% chance of seeing a result this large by random chance"
- p < 0.05: Conventional threshold for "statistically significant"
- p ≥ 0.05: Fail to reject null hypothesis — cannot conclude effect is real

### What p-value is NOT:
- NOT the probability that the null hypothesis is true
- NOT the probability that your variant is better
- NOT a measure of effect size
- NOT a reason to celebrate without checking effect size

## What Actually Matters: Effect Size

Statistical significance ≠ practical significance.

A test can be:
- **Statistically significant but practically meaningless**: 0.01% lift with huge sample
- **Practically meaningful but not significant**: Real 5% lift but too little data

Always report:
1. **Observed lift**: (Treatment − Control) / Control
2. **Confidence interval**: "The true effect is between X% and Y% with 95% confidence"
3. **P-value**: Was this likely due to chance?
4. **Power**: Did we have enough sample to detect this effect?

## Ship / No-Ship Decision Framework

### Ship ✅
All of these:
- Primary metric: statistically significant (p < 0.05) AND positive
- Effect size: meets or exceeds the minimum detectable effect you pre-specified
- Guardrail metrics: none significantly harmed
- No sample ratio mismatch detected
- Test ran for minimum required duration

### No-Ship ❌
Any of these:
- Primary metric: negative AND statistically significant
- Guardrail metrics: statistically significant decline
- Sample ratio mismatch detected (invalidates the test)
- Test ended early / not enough data

### Iterate / Extend 🔄
When:
- Results trending positive but underpowered (need more time/sample)
- Segmented effect: works for some users, hurts others → segment-specific rollout
- Guardrail violated but primary metric strong → redesign to protect guardrail

### Inconclusive → Learn 📚
When:
- p ≥ 0.05, effect near zero: No meaningful effect (not the same as "proved no effect")
- Ask: Is the hypothesis wrong? Or is the execution wrong?

## Bayesian vs Frequentist
- **Frequentist** (traditional): p-value, significance threshold — binary decision
- **Bayesian** (modern): "Probability that variant is better" — more intuitive
- Tools: VWO, Optimizely use Bayesian; most custom setups use Frequentist

## Segmented Analysis

After primary analysis, check:
- New vs returning users (novelty effect)
- Mobile vs desktop
- User cohort (new signup vs existing)
- Geographic region

Only report segments you pre-planned (post-hoc segmentation is p-hacking).

## Common Analysis Errors

| Error | Description | Fix |
|---|---|---|
| Peeking | Stopping when p < 0.05 appears | Run to predetermined sample size |
| Multiple comparisons | Testing 10 metrics, one "wins" | Use Bonferroni correction or pre-specify primary metric |
| Simpson's Paradox | Aggregated result reverses in segments | Always segment analysis |
| Survivorship bias | Analyzing only users who completed the flow | Analyze from assignment, not completion |

## Output Format
- Results summary table (Control vs Treatment: n, conversion rate, lift, CI, p-value)
- Statistical significance verdict
- Effect size interpretation
- Guardrail metrics status
- Ship / No-ship / Iterate recommendation with rationale
