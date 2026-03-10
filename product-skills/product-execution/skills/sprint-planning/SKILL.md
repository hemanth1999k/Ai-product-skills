---
name: sprint-planning
description: "Use when the user needs to plan a sprint, select stories, estimate capacity, or structure a sprint planning session. Triggers on: 'sprint planning', 'plan the sprint', 'sprint capacity', 'what goes in this sprint', 'sprint goal', 'sprint scope'."
---

# Sprint Planning

## Purpose
Set a meaningful sprint goal, select the right work, and create a shared commitment the team can confidently execute.

## Pre-Planning Inputs
- Groomed backlog (top 10+ ready stories)
- Team capacity (who is available, for how many days?)
- Sprint length (1 or 2 weeks)
- Previous sprint velocity (story points or stories completed)
- Outstanding blockers or carryover

## Sprint Planning Structure (2-4 hours for 2-week sprint)

### Part 1: Set the Sprint Goal (30 min)
The sprint goal is a single sentence that captures WHY we're doing this sprint.
- Connects to quarterly OKR
- Guides decision-making during the sprint ("Does this story help us hit the goal?")
- Used to re-prioritize if unexpected issues arise

Good sprint goal: "Enable new users to complete their first report without help documentation"
Bad sprint goal: "Work on onboarding, reporting, and bug fixes"

### Part 2: Capacity Calculation (15 min)
```
Available days = (team size × sprint days) − planned time off
Velocity buffer = Available days × 0.7 (account for meetings, unplanned work)
Target points = Previous velocity × (Available days / Previous available days)
```

Don't over-commit. Sustainable pace beats heroics.

### Part 3: Story Selection (60-90 min)
1. Present candidate stories (top backlog items aligned with sprint goal)
2. For each story: is it truly sprint-ready? (Definition of Ready checklist)
3. Team estimates if not already estimated
4. Select stories until target capacity is filled
5. Identify one "stretch goal" story — only if capacity allows

### Part 4: Task Breakdown (Optional, for complex stories)
For stories > 3 points, break into engineering tasks:
- Backend API
- Frontend implementation
- Unit tests
- QA / acceptance test
- Design review

### Part 5: Risk Identification
- What could prevent us from hitting the sprint goal?
- Any dependencies on other teams?
- Any stories with unclear requirements?
- Any stories that might be bigger than estimated?

## Sprint Commitment Principles
- The team commits to the sprint goal, not every story
- If new work comes in mid-sprint, something must come out
- The PM's job during the sprint: protect the team from scope creep

## Definition of Done (DoD)
Define once, apply to every story:
- [ ] Feature works as specified in AC
- [ ] Unit tests written and passing
- [ ] Code reviewed and merged to main
- [ ] QA sign-off
- [ ] Feature flagged / instrumented if applicable
- [ ] Documentation updated

## Output Format
- Sprint goal statement
- Capacity calculation
- Selected stories with points
- Stretch goal (if applicable)
- Risk log
