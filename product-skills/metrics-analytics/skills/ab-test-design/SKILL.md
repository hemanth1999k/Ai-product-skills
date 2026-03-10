---
name: ab-test-design
description: "Use when the user wants to design an A/B test, determine sample size, or set up an experiment. Triggers on: 'A/B test', 'split test', 'experiment design', 'sample size', 'statistical significance', 'design an experiment', 'test this feature'."
---

# A/B Test Design

## Purpose
Design statistically valid A/B experiments that produce trustworthy, actionable results.

## Before You Test

Ask these questions first:
1. What decision will this test inform?
2. What's your hypothesis?
3. Is this problem big enough to test? (What's the potential impact?)
4. Can you actually change user behavior, or is this a one-time event?

## Hypothesis Framework

Structure every hypothesis as:
> "If we [change], then [metric] will [increase/decrease] by [X%], because [reasoning], which matters because [business impact]."

Example:
> "If we add social proof (# of users) to the signup page, then signup conversion will increase by 5%, because users are uncertain about product quality, which matters because a 5% lift = $200K ARR."

## Sample Size Calculation

Key inputs:
- **Baseline conversion rate** (current metric value)
- **Minimum Detectable Effect (MDE)**: Smallest change worth detecting
- **Statistical power**: Usually 80% (0.8) — probability of detecting a real effect
- **Significance level (α)**: Usually 5% (0.05) — acceptable false positive rate

Formula (simplified):
```
n = 16 × σ² / δ²
where σ = standard deviation, δ = minimum detectable effect
```

**Rule of thumb**: For conversion rate tests, you need roughly:
- Detecting 1% relative lift: ~100,000 users per variant
- Detecting 5% relative lift: ~4,000 users per variant
- Detecting 10% relative lift: ~1,000 users per variant

Use: Evan Miller's A/B test calculator or statsig.com/calculator

## Experiment Design Checklist

### Setup
- [ ] One change per test (avoid multivariate when sample is limited)
- [ ] Random assignment at user level (not session)
- [ ] Control = current experience, unchanged
- [ ] Ensure traffic split is truly random (no selection bias)

### Guardrails
- [ ] Define primary metric BEFORE the test runs
- [ ] Define 1-2 guardrail metrics (must not decline)
- [ ] Define minimum run duration (at least 1-2 business cycles)
- [ ] Do NOT peek at results and stop early (p-hacking)

### Segment Considerations
- Is the effect likely to differ by segment? (device, user type, cohort)
- Plan segment analysis BEFORE running (not as post-hoc fishing)

## Test Duration

Run until:
1. Sample size reached
2. Minimum 1-2 full business cycles (avoid weekday-only data)
3. No major external events (holidays, outages) during test

Never stop early because "it looks good." That's p-hacking.

## Common Mistakes to Avoid
- **Peeking**: Looking at results before sample size is reached
- **Multiple testing**: Testing 10 metrics, one will be "significant" by chance
- **Sample ratio mismatch (SRM)**: If control/treatment split isn't 50/50 as assigned, something is wrong
- **Novelty effect**: New UI always gets inflated engagement at first; run test long enough
- **Network effects**: Spillover between control and treatment (use cluster randomization)

## Output Format
- Hypothesis statement
- Recommended sample size with calculation
- Test duration estimate
- Primary metric + guardrail metrics
- Segment analysis plan
- Decision criteria: Ship / No-ship thresholds
