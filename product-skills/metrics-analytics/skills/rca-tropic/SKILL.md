---
name: rca-tropic
description: "Use when the user needs to diagnose a metric drop, find root cause of a problem, or apply the TROPIC framework. Triggers on: 'metric dropped', 'why did X go down', 'RCA', 'root cause analysis', 'TROPIC', 'diagnose the metric', 'figure out what happened'."
---

# Root Cause Analysis: TROPIC Framework

## Purpose
Systematically diagnose why a metric changed — avoiding the trap of jumping to conclusions before understanding the cause.

## The TROPIC Framework (Lewis Lin)
Source: https://www.lewis-lin.com/blog/tropic-product-metrics-framework

TROPIC is a structured hypothesis tree for diagnosing metric changes. When a metric moves unexpectedly, walk through each category:

### T — Typical Fluctuation
Is this actually a problem, or normal variance?
- Is this within historical variance bounds?
- Is it a day-of-week effect (weekends always lower)?
- Is it seasonal (holiday, fiscal quarter end)?
- How long has the trend persisted?

**Check**: Plot the metric over 3+ months. Is this outside the normal range?

### R — Reporting / Instrumentation
Is the data trustworthy?
- Was there a logging or tracking code change?
- Did we change how we define/calculate this metric?
- Is this a data pipeline issue (delay, missing data)?
- Did a third-party analytics tool have an outage?

**Check**: Look at raw event counts. Are they consistent? Check dashboard data vs raw data.

### O — Organic / External Causes
Did something outside the product change?
- Seasonality, holidays, major events
- Competitor launch or marketing blitz
- Press coverage (positive or negative)
- Search algorithm change (SEO)
- Platform policy change (App Store, Google)
- Macro economic events

**Check**: What else changed in the world at this time?

### P — Product Changes
Did we ship something that caused this?
- What did we deploy in the relevant timeframe?
- Any A/B tests running that could affect this metric?
- Were there UI changes that could affect the funnel?
- Any infrastructure or performance changes (latency)?

**Check**: Overlay deployment history with metric timeline. Correlation ≠ causation, but it's a starting point.

### I — Internal / Business Changes
Did something change in our go-to-market or business?
- Sales or marketing mix change (new channels, campaign)
- Pricing change
- Support quality change
- New customer segment being acquired (different behavior)
- Operational changes (e.g., sales team quota change)

**Check**: Segment the metric by acquisition channel / cohort. Did the change affect all users equally?

### C — Competitive / Market
Did the competitive landscape change?
- Did a competitor launch a better solution?
- Did a competitor slash prices?
- Did the market itself shrink (regulatory, economic)?

**Check**: Monitor competitor activity, industry news, social listening.

## TROPIC Diagnosis Workflow

1. **Isolate the metric precisely**: Exactly which metric? Which segment? What time window?
2. **Quantify the drop**: How large? Relative and absolute. Is this statistically meaningful?
3. **Walk through TROPIC**: Generate hypotheses for each category
4. **Prioritize hypotheses**: Most likely given the evidence
5. **Test each hypothesis**: Segment analysis, data deep-dives, data pulls
6. **Identify root cause(s)**: Often 1-2 causes, sometimes compound
7. **Recommend action**: Fix the root cause, not the symptom

## Segmentation Technique
When diagnosing, always segment:
- Platform (iOS, Android, Web)
- User type (new vs returning, free vs paid)
- Geography
- Cohort (users acquired in different periods)
- Feature flag / experiment groups

If the metric dropped for only ONE segment, you've narrowed the root cause dramatically.

## Output Format
- TROPIC hypothesis table (category → hypothesis → evidence → verdict)
- Root cause identified (or top 2-3 candidates if inconclusive)
- Recommended investigation steps
- Proposed fix(es) with confidence level
