---
name: ship-no-ship-logic
description: "Use when the user needs a framework for making ship vs no-ship decisions, evaluating whether to release something, or thinking through launch risk. Triggers on: 'ship or no ship', 'should we ship', 'ship decision', 'release decision', 'launch risk', 'ready to ship'."
---

# Ship / No-Ship Decision Logic

## Purpose
Make defensible, principled decisions about whether to release — balancing quality, risk, speed, and business impact.

## The Ship Decision Framework

### Step 1: Define "Done" Upfront
The ship decision starts before building, not at the end.
Before starting a feature, define:
- What does "shippable" look like? (Acceptance criteria)
- What are the quality gates? (Test exit criteria)
- What are the launch blockers? (P0 bugs, security issues, etc.)

If you haven't defined done, you'll argue about it at launch time.

### Step 2: Severity Classification

**P0 — Ship Blocker** (Never ship with these)
- Data loss or corruption risk
- Security vulnerability exploitable by users
- Core user journey broken for >1% of users
- Financial calculation error
- Legal / compliance violation

**P1 — Strong Preference to Fix**
- Major feature not working for >10% of use cases
- Significant UX confusion that damages trust
- Performance degradation >50% over baseline
- Broken on a major platform/browser

**P2 — Judgment Call**
- Minor UX imperfection
- Edge case not working
- Non-critical feature slightly wrong
- Cosmetic issue

**P3 — Track and Iterate**
- Minor visual inconsistency
- Enhancement that didn't make the cut
- Nice-to-have missing

### Step 3: The Ship Decision Matrix

| P0s | P1s | P2s | Decision |
|---|---|---|---|
| Any open | Any | Any | NO-SHIP — resolve P0s first |
| None | ≥ 3 open | Any | NO-SHIP or stage rollout |
| None | 1-2 open with mitigation | < 5 | CONDITIONAL SHIP — monitor closely |
| None | None | Any | SHIP — track P2/P3 in next sprint |

### Step 4: Risk-Adjusted Thinking

For each known issue, evaluate:
- **Probability**: How likely is this to affect users?
- **Severity**: How bad is it if it does?
- **Reversibility**: Can we fix forward quickly if needed?
- **Detectability**: Will users notice? Will it cause escalations?

High probability × high severity × low reversibility = DO NOT SHIP

### Step 5: Speed vs Risk Trade-off

Factors that justify shipping faster (higher risk tolerance):
- Feature flag / gradual rollout available
- Quick rollback path exists
- Low usage feature affecting small % of users
- Competitive urgency (lose deal, missing window)
- Minor issue with known fix already in progress

Factors requiring more caution:
- Affects payments, authentication, or data
- No rollback path
- High traffic path
- Enterprise customer with SLA
- Regulatory context

### The "Would I be okay explaining this?" Test
Would you be comfortable explaining your ship decision to:
- A customer who was affected?
- Your engineering team?
- Your CEO?

If the answer to any is "no" — don't ship.

## Output Format
- Open issues classified by severity (P0-P3)
- Ship recommendation: Ship / Conditional / No-Ship
- Conditions for Conditional Ship
- Risk summary and mitigation plan
