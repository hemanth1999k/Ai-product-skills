---
name: moscow-method
description: "Use when the user wants to prioritize using MoSCoW, separate must-haves from nice-to-haves, or create a release scope decision. Triggers on: 'MoSCoW', 'must have should have could have', 'must haves', 'release scope', 'MVP scope', 'what to cut'."
---

# MoSCoW Prioritization

## Purpose
Quickly align stakeholders on which requirements are essential vs optional to deliver a successful release.

## The Four Categories

### Must Have (M)
Non-negotiable requirements. The product/release fails without these.
Test: "If we launch without this, will the launch fail or break something critical?"
- Legal / compliance requirements
- Core functionality users explicitly need
- Security essentials
- Data integrity requirements

**Must Haves should be ≤ 60% of total scope**. If everything is "Must Have," the framework isn't being applied honestly.

### Should Have (S)
Important but not critical. Can be temporarily omitted without failure.
Test: "This is painful to not have, but there's a workaround."
- Performance improvements
- Minor UX polish
- Non-critical user requests
- Features that improve but don't enable the core use case

### Could Have (C)
Nice to have. Low impact if omitted.
Test: "Users would like this, but most won't miss it if it's absent."
- "Would be nice" features
- Minor conveniences
- Future-facing items with no current demand

### Won't Have (W)
Explicitly out of scope for this release (not "never" — just "not now").
Test: "We've made a conscious decision this is not happening in this cycle."
- Feature requests that don't align with current strategy
- High-effort low-value items
- Things that belong in a different product or team

## MoSCoW for MVP Scoping

Apply MoSCoW to define a tight MVP:
- MVP = All Must Haves + NONE of the rest
- Then decide: Can we make MVP valuable to users with just the Must Haves?
- If not → your Must Have list is incomplete

## MoSCoW for Sprint Scoping
- Commit only to Must Haves + some Should Haves
- Could Haves as stretch goals
- Never commit to more than team capacity supports

## Common Mistakes
- **Everything is Must Have**: Team is avoiding hard conversations
- **No Won't Haves**: Missing the discipline of explicit exclusion
- **No alignment on criteria**: Must Have for whom? Engineering? Users? Business?

Always define MoSCoW in context: "Must Have for [release goal / user type / success definition]"

## Output Format
- MoSCoW table for submitted items
- Must Have %: flag if > 60%
- MVP definition (Must Haves only)
- Items recommended for reclassification with rationale
