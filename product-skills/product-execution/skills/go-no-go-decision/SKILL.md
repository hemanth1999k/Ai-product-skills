---
name: go-no-go-decision
description: "Use when the user needs to run a go/no-go meeting, make a launch readiness decision, or create launch gates. Triggers on: 'go no go', 'launch readiness', 'launch gate', 'should we ship', 'ready to launch', 'go live decision'."
---

# Go / No-Go Decision Framework

## Purpose
Make a principled, defensible go/no-go launch decision by evaluating readiness across all dimensions — not just "is it built?"

## Go / No-Go Decision Meeting Structure

### Participants
- PM (owns the decision)
- Engineering lead
- QA lead
- Data/Analytics
- Customer Success / Support lead
- Marketing (for externally visible launches)

### Meeting Flow (30-60 min)

1. **Review release scope** — What exactly are we deciding to ship?
2. **Work through gates** — Each team owner presents their readiness
3. **Identify blockers** — Any "No" triggers discussion
4. **Make the call** — PM makes final decision, documents rationale

## Go / No-Go Gates

### Gate 1: Technical Readiness
- [ ] All planned features are complete and reviewed
- [ ] All P0 and P1 bugs are resolved
- [ ] Performance testing passed (load, latency benchmarks)
- [ ] Security review completed (for sensitive features)
- [ ] Database migrations rehearsed
- [ ] Rollback plan documented and tested

### Gate 2: Quality Readiness
- [ ] QA sign-off on all acceptance criteria
- [ ] Regression suite passing
- [ ] Edge cases tested
- [ ] No known data integrity issues

### Gate 3: Monitoring Readiness
- [ ] Analytics events instrumented and validated
- [ ] Alerting configured for key metrics
- [ ] On-call rotation assigned for launch window
- [ ] Baseline captured before release

### Gate 4: Communication Readiness
- [ ] Internal stakeholders briefed
- [ ] Support team trained
- [ ] Help documentation published or scheduled
- [ ] Customer comms ready (email, in-app, changelog)

### Gate 5: Business Readiness
- [ ] Success metrics defined
- [ ] Rollback criteria defined
- [ ] Pricing/billing changes coordinated (if applicable)
- [ ] Legal/compliance sign-off (if applicable)
- [ ] Sales/CS briefed on customer-facing changes

## Decision Matrix

| Gate | Status | Blocker? | Owner |
|---|---|---|---|
| Technical | ✅ Go / ❌ No-Go / ⚠️ Conditional | Y/N | Name |
| Quality | ✅ / ❌ / ⚠️ | Y/N | Name |
| Monitoring | ✅ / ❌ / ⚠️ | Y/N | Name |
| Communication | ✅ / ❌ / ⚠️ | Y/N | Name |
| Business | ✅ / ❌ / ⚠️ | Y/N | Name |

**GO**: All gates pass, no blockers
**CONDITIONAL GO**: Minor issues with clear resolution plan and timeline
**NO-GO**: Any P0 blocker unresolved

## No-Go Scenarios (Automatic)
- P0 bug in core user path
- Data loss risk
- Security vulnerability unpatched
- Rollback plan untested
- On-call coverage gap during launch window
- Customer comms not ready for externally visible change

## Output Format
- Go/no-go gate table filled in
- Blockers identified with owner and ETA to resolve
- Final decision: Go / Conditional Go / No-Go with rationale
- Next check-in time if Conditional
