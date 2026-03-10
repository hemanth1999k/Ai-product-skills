---
name: job-story-creation
description: "Use when the user wants to write job stories, JTBD-based requirements, or situation-motivation-outcome format stories. Triggers on: 'job story', 'JTBD story', 'situation motivation outcome', 'when I want I can', 'Alan Klement', 'jobs based requirements'."
---

# Job Story Creation

## Purpose
Write requirements grounded in user context and motivation — not assumed personas. Job stories are more flexible and contextually grounded than user stories.

## Job Story Format
**When [situation], I want to [motivation], so I can [outcome].**

### Components Explained

**Situation (When)**
The context that triggers the need.
- Be specific about what state the user is in
- Include environmental, emotional, or workflow context
- Not just "when I'm using the product" — what specific moment?

**Motivation (I want to)**
The user's underlying drive — not the feature.
- What do they want to ACCOMPLISH, not what feature they want
- Connects to emotional or functional job
- Often reveals opportunities for multiple solutions

**Outcome (So I can)**
The result the user is trying to achieve.
- Connects to a broader goal beyond this task
- Often the key to understanding the real value

## Job Story vs User Story

| | User Story | Job Story |
|---|---|---|
| Frame | Persona-based | Context-based |
| Focus | Who the user is | What situation they're in |
| Flexibility | Fixed by persona | Adapts to context |
| JTBD alignment | Weaker | Stronger |
| Best for | Clear user types | Complex contexts, multiple user types |

Use Job Stories when:
- Multiple personas share the same situation
- The context matters more than the persona type
- You're doing JTBD-based discovery

## Writing Good Job Stories

### Bad Job Stories:
❌ "When I use the reporting section, I want to see charts, so I can understand data"
(Too vague — no specific situation, no real motivation)

### Good Job Stories:
✅ "When I'm preparing for my weekly stakeholder meeting on Monday morning, I want to quickly see which KPIs changed since last week, so I can walk into the meeting without surprises and look prepared"

✅ "When a deal is stuck in the pipeline for more than 14 days without activity, I want to receive a contextual nudge, so I can re-engage before the deal goes cold"

## Job Story Workshop

1. **Pick a specific job**: "Complete a performance review for a direct report"
2. **Identify triggering situations**: When in the job does this user need help?
3. **Map motivations**: For each situation — what are they trying to accomplish?
4. **Define outcomes**: What larger goal does this serve?
5. **Write the story**: Combine into When/Want/Can format

## Job Stories to Acceptance Criteria
After writing the job story, define testable acceptance criteria:
```
Job Story: When preparing for a stakeholder meeting, I want to see KPI deltas since last week...

AC:
- Given I open the Weekly Digest dashboard on any day
- When I view the KPI summary section
- Then each KPI shows: current value, value from 7 days ago, % change, and trend arrow
- And metrics that changed by > 20% are highlighted in yellow
```

## Output Format
- Job stories in When/Want/Can format for all submitted items
- Context analysis: What triggered this job story?
- Acceptance criteria for each story
- Mapping to user value (which JTBD does this serve?)
