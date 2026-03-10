---
name: user-story-creation
description: "Use when the user needs to write user stories, acceptance criteria, job stories, or backlog items. Triggers on: 'user story', 'write stories', 'acceptance criteria', 'as a user I want', 'story format', 'backlog items', 'job story'."
---

# User Story & Job Story Creation

## Purpose
Write precise, testable, valuable stories that teams can build from — not vague wish lists.

## User Story Format (Classic)
**As a [persona], I want to [goal], so that [benefit].**

### Quality Criteria (INVEST)
- **I**ndependent: Can be built without other stories
- **N**egotiable: Not a fixed contract — open to discussion
- **V**aluable: Delivers value to users or business
- **E**stimable: Team can estimate the work
- **S**mall: Fits in one sprint
- **T**estable: Clear pass/fail acceptance criteria

### Bad Story vs Good Story
❌ "As a user, I want a better dashboard"
✅ "As a Sales Manager, I want to see team deal velocity on the dashboard so that I can identify which reps need coaching before end of quarter"

## Acceptance Criteria (Given/When/Then)
**Given** [context / starting state]
**When** [action taken]
**Then** [expected outcome]

Example:
```
Given I am a Sales Manager with 3+ direct reports
When I open the Team Dashboard
Then I see each rep's deal velocity for the current quarter ranked highest to lowest
And I can click any rep's name to see their individual pipeline
And deals with no activity in 14+ days are highlighted in red
```

## Job Story Format (Alternative to User Story)
Focuses on context and motivation, not persona.
**When [situation], I want to [motivation], so I can [outcome].**

Use when: Context and triggers matter more than persona type.
"When I get back from a sales call, I want to log notes quickly, so I can capture details before I forget them."

## WWA Format (Why-What-Acceptance)
For complex features requiring business context:
- **Why**: The business/user problem being solved
- **What**: The solution approach
- **Acceptance**: Testable criteria for "done"

## Story Map Structure (Jeff Patton)
For features that span multiple stories:
```
ACTIVITY (what users do overall)
  TASKS (steps within the activity)
    STORIES (specific actions to implement)
      [baseline release]
      [enhancement 1]
      [enhancement 2]
```

## Story Writing Checklist
- [ ] Written from user's perspective, not system's
- [ ] Persona is specific (not "a user")
- [ ] Goal is a user goal, not a feature request
- [ ] Benefit explains WHY they want this
- [ ] Acceptance criteria are testable (binary pass/fail)
- [ ] Story is small enough to complete in one sprint
- [ ] Definition of Done is clear

## Output Format
- User stories in correct format for all submitted items
- Acceptance criteria (Given/When/Then) for each story
- Story size estimate (S/M/L)
- Dependencies flagged
