---
name: backlog-grooming
description: "Use when the user needs to groom, refine, or clean up a product backlog. Triggers on: 'groom backlog', 'backlog refinement', 'backlog grooming', 'clean up backlog', 'refine stories', 'sprint refinement', 'backlog management'."
---

# Backlog Grooming (Refinement)

## Purpose
Keep the backlog healthy — well-estimated, well-defined, prioritized, and ready for sprint planning.

## What "Healthy Backlog" Means
- Top 2 sprints are detailed, estimated, and ready
- Next 2-3 sprints are roughly estimated with clear intent
- Everything beyond is directional, not detailed
- No zombie stories older than 90 days without a decision
- Each item has: owner, priority, acceptance criteria, and definition of done

## Grooming Session Structure (60-90 min, every sprint)

### Part 1: Backlog Hygiene (20 min)
1. Archive or delete stories >90 days old without action
2. Flag stories that have been in "ready" for 3+ sprints — why aren't they being built?
3. Merge duplicate stories
4. Ensure priorities reflect current strategy (not last quarter's)

### Part 2: Story Refinement (40 min)
For each candidate story (top 5-8 per session):
1. **Read the story aloud** — Does everyone understand it?
2. **Acceptance criteria** — Are they specific and testable?
3. **Questions / unknowns** — What do we need to know before building?
4. **Dependencies** — Does this block or get blocked by something?
5. **Estimate** — Relative sizing (t-shirt or story points)

### Part 3: Priority Review (10-20 min)
1. Do the top items reflect current priorities?
2. Did anything change this week that should reorder the backlog?
3. Are there items that should be promoted from "next" to "now"?

## Estimation Methods

### Story Points (Fibonacci: 1, 2, 3, 5, 8, 13, 21)
- Relative sizing, not time
- 1 = trivially small; 13+ = too big, break it down
- 21 = epic, not a story

### T-Shirt Sizing (XS, S, M, L, XL)
- Faster, less precise
- Good for roadmap-level estimation
- Convert to points when sprint-ready

### Planning Poker Rules
- Everyone votes simultaneously (prevent anchoring)
- Outliers explain their reasoning
- Re-vote after discussion if needed
- Don't average — reach consensus

## Story Readiness Checklist (Definition of Ready)
A story is sprint-ready when:
- [ ] Acceptance criteria are clear and testable
- [ ] Design is available (if UI work)
- [ ] Dependencies identified and resolved
- [ ] Estimated by the team
- [ ] Fits within one sprint
- [ ] Test scenarios drafted

## Backlog Categories to Maintain
- **Now** (sprint-ready, estimated, detailed)
- **Next** (roughly defined, next 2-3 sprints)
- **Later** (directional intent, not detailed)
- **Icebox** (parked, revisit quarterly)
- **Won't Do** (explicitly rejected, with reason noted)

## Output Format
- Groomed backlog assessment
- Stories ready for sprint vs needs more work
- Items recommended for archival
- Refinement agenda for next session
