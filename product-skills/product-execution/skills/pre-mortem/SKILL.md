---
name: pre-mortem
description: "Use when the user wants to identify risks before a launch or project, run a pre-mortem, or proactively find failure modes. Triggers on: 'pre-mortem', 'premortem', 'what could go wrong', 'risk assessment', 'anticipate failure', 'risk identification', 'failure modes'."
---

# Pre-Mortem Analysis

## Purpose
Prevent failure by imagining it first. More effective than traditional risk review because it gives people permission to voice fears.

## The Pre-Mortem Method (Gary Klein)

Traditional risk review: "What risks should we consider?"
Pre-mortem: "It's 6 months from now. The project failed catastrophically. What happened?"

This reframing:
- Removes optimism bias
- Makes it safe to voice concerns (you're explaining an already-happened failure)
- Surfaces risks that polite status meetings suppress

## Pre-Mortem Workshop Format (60-90 min)

### Setup (5 min)
"Imagine we launched [product/feature] 6 months ago. It was a complete failure. Not a minor stumble — a significant, visible failure. You're writing the post-mortem. What went wrong?"

### Silent Writing (10 min)
Each person writes as many failure reasons as possible on separate cards.
No discussion yet — individual generation prevents groupthink.

### Share Out (20-30 min)
Go around the room. Each person shares their top failure reason.
Facilitator clusters on whiteboard/Miro/FigJam.

### Analysis (20-30 min)
For each cluster:
- How plausible is this failure mode? (1-10)
- How severe would the impact be? (1-10)
- What's our current mitigation?
- What should we do differently?

### Action Planning (15 min)
Top 3-5 risks: assign owner, mitigation action, and check-in date.

## Tigers / Paper Tigers / Elephants (Alternative Framework)

### Tigers 🐯
Real, serious risks that are widely acknowledged but not sufficiently addressed.
"We all know the API rate limit is a risk but we haven't built proper fallbacks"

### Paper Tigers 📄
Things that SEEM scary but are actually manageable.
"We're worried about competitors copying us, but our moat is relationships, not features"

### Elephants 🐘
Real, serious risks that nobody is talking about.
"The sales team is promising enterprise features in Q2 that we haven't scoped yet"

Elephants are the most dangerous — bring them into the open.

## Common Failure Modes by Type

### Product Failures
- Wrong customer segment targeted
- Value proposition not compelling
- Onboarding too complex
- Core use case not validated before build

### Technical Failures
- Scaling under load not tested
- Third-party dependency fails
- Data migration corrupts production data
- Security vulnerability exploited post-launch

### Organizational Failures
- Cross-team dependencies not resolved
- Launch team burned out / departures
- Stakeholder misalignment discovered post-launch
- Marketing and product timelines misaligned

### Market Failures
- Competitor launched first with better execution
- Market timing wrong (too early / too late)
- Pricing misaligned with willingness to pay
- Regulatory change makes product non-compliant

## Output Format
- Pre-mortem workshop format
- Risk register: Failure mode | Plausibility | Severity | Owner | Mitigation
- Top 3 "Elephants" — unspoken risks surfaced
- Action items with owners and dates
