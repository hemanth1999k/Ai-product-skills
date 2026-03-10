---
name: rollback-plan
description: "Use when the user needs to create a rollback plan, define rollback criteria, or prepare for reverting a release. Triggers on: 'rollback plan', 'rollback', 'revert release', 'undo release', 'rollback criteria', 'roll back feature'."
---

# Rollback Plan

## Purpose
Define exactly how to reverse a release if something goes wrong — before you need to, not during the crisis.

## Rollback Philosophy

"Plan for rollback like it's going to happen. Hope it doesn't."

A release without a tested rollback plan is a higher-risk release. The question isn't "will we ever roll back?" — it's "can we do it in 5 minutes or 5 hours?"

## Rollback Readiness Assessment

Before every release, answer:

1. **Is rollback technically possible?**
   - Was there a database schema migration? (Can it be reversed safely?)
   - Was data transformed or migrated? (Is it reversible?)
   - Are there external API side effects? (Emails sent, webhooks fired?)

2. **Is rollback safe?**
   - Will rolling back break users who already used the new feature?
   - Will data created under the new version work under the old version?

3. **How long does rollback take?**
   - Deploy rollback: < 5 min (acceptable)
   - Deploy + database rollback: 15-30 min (acceptable with warning)
   - Manual data correction required: 1+ hours (high risk — plan extra carefully)

## Rollback Criteria (Define Before Launch)

Set explicit thresholds that trigger automatic consideration of rollback:

| Metric | Rollback Threshold |
|---|---|
| Error rate | > X% (e.g., > 2% of requests returning 500) |
| Latency | > X ms p99 response time |
| Core funnel conversion | Drops > X% within 2 hours |
| Support ticket volume | > X tickets in first hour mentioning [feature] |
| On-call alert level | Any P0 alert fires within 30 min of deploy |

## Rollback Runbook Template

```
Feature: [Feature name]
Release date: [Date]
Deploy type: [Feature flag / Code deploy / DB migration]

ROLLBACK TRIGGER CONDITIONS:
□ Error rate > [X]%
□ [Metric] drops > [X]%
□ [Alert] fires

ROLLBACK DECISION AUTHORITY: [Name / Role]
ROLLBACK NOTIFICATION: [Slack channel, contacts]

ROLLBACK STEPS:
1. [Step]
2. [Step]
3. [Step]
Estimated time: [X] minutes

POST-ROLLBACK STEPS:
1. Notify [stakeholders]
2. Verify [metric] returns to baseline
3. File incident report
4. Schedule blameless post-mortem

KNOWN RISKS OF ROLLING BACK:
- [Risk 1]
- Mitigation: [X]
```

## Rollback Methods by Deploy Type

### Feature Flag Rollback (Fastest — seconds)
- Turn off feature flag
- No code deploy needed
- Best practice: All significant features behind flags at launch

### Code Deploy Rollback (Minutes)
- Redeploy previous version tag
- Verify health checks pass
- Monitor metrics

### Database Migration Rollback (Most Complex)
- Test down migration in staging BEFORE production deploy
- Verify data integrity after rollback
- If irreversible migration (data transformation), document what data state users will be in

## Output Format
- Rollback feasibility assessment
- Rollback criteria (thresholds)
- Step-by-step rollback runbook
- Post-rollback checklist
