---
name: release-planning
description: "Use when the user needs to plan a product release, define release scope, create a release checklist, or coordinate a launch. Triggers on: 'release plan', 'release planning', 'launch plan', 'release checklist', 'release readiness', 'ship this feature'."
---

# Release Planning

## Purpose
Define what ships, when it ships, and ensure all teams are coordinated for a successful launch — from engineering to marketing to support.

## Release Plan Structure

### 1. Release Definition
- What's in scope (features, fixes, changes)
- What's explicitly out of scope
- Target ship date
- Release type: Full launch / Beta / Staged rollout / Feature flag

### 2. Success Metrics
Define BEFORE release:
- Primary metric: What does success look like in 30 days?
- Leading indicators: What early signals will tell us it's working?
- Guardrail metrics: What must NOT decline?
- Rollback threshold: If [metric] drops > X%, we roll back

### 3. Staged Rollout Plan
If risky, use a gradual rollout:
- Day 1: 1% of traffic (internal/beta users)
- Day 3: 10% of traffic (if no issues)
- Day 7: 50% of traffic
- Day 14: 100% (full launch)

Monitor: error rates, latency, primary metric, support tickets at each stage.

### 4. Team Coordination Checklist

**Engineering**
- [ ] Feature complete and code reviewed
- [ ] Unit tests passing
- [ ] Load/performance tested
- [ ] Database migrations tested
- [ ] Feature flag implemented
- [ ] Monitoring/alerting configured
- [ ] Runbook written

**Product/Design**
- [ ] Acceptance criteria verified
- [ ] UX reviewed on mobile and desktop
- [ ] Accessibility checked
- [ ] In-product messaging written (tooltips, empty states, errors)
- [ ] Analytics events instrumented

**QA**
- [ ] Test plan executed
- [ ] Edge cases tested
- [ ] Regression suite passed
- [ ] Cross-browser/device testing done

**Data**
- [ ] Analytics events validated
- [ ] Dashboard updated
- [ ] Baseline captured before launch

**Marketing/Comms**
- [ ] Announcement copy ready (email, in-app, social)
- [ ] Help docs updated
- [ ] Sales/CS briefed
- [ ] Blog post / changelog drafted

**Support**
- [ ] Support team briefed on new feature
- [ ] FAQ written
- [ ] Known issues documented
- [ ] Escalation path defined for launch day issues

### 5. Launch Day Runbook
- Who is on-call?
- How do we monitor for problems?
- What's the rollback process if critical bug found?
- Communication chain: who gets notified of issues and when?
- War room: how do teams coordinate if something goes wrong?

## Release Types

| Type | When | Risk | Notes |
|---|---|---|---|
| Dark launch | Backend changes, risky infra | Low to user | No UX change |
| Feature flag | Controlled rollout | Low | Can turn off instantly |
| Beta | Early access cohort | Medium | Get feedback before full launch |
| Staged rollout | Any significant feature | Low | 1% → 10% → 100% |
| Hard launch | Low risk, high visibility | Medium-High | All-at-once, coordinated |

## Output Format
- Release scope definition
- Coordinated checklist by team
- Success metrics + rollback threshold
- Launch day runbook outline
