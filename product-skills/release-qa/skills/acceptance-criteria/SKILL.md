---
name: acceptance-criteria
description: "Use when the user needs to write acceptance criteria, define done, or create testable requirements. Triggers on: 'acceptance criteria', 'AC', 'definition of done', 'how do we know it works', 'write AC', 'BDD', 'Given when then'."
---

# Acceptance Criteria

## Purpose
Define the specific, testable conditions that a feature must meet to be considered complete and releasable.

## What Good Acceptance Criteria Do
1. **End debates** about scope during development
2. **Enable QA** to write test cases without re-asking the PM
3. **Define "done"** so engineers know when to stop
4. **Prevent gold-plating** (building beyond what's needed)
5. **Surface ambiguity** early (before coding)

## AC Format: Given / When / Then (BDD)

**Given** [the context / precondition]
**When** [the user does X]
**Then** [the system does Y]

Additional:
**And** [secondary expected behavior]
**But** [exception or negative case]

### Example
```
Feature: Payment confirmation email

Given I am a registered customer
And I have a pending order #12345

When the payment is successfully processed

Then I receive a confirmation email within 2 minutes
And the email subject is "Your order is confirmed — #12345"
And the email contains: order number, item list, total amount, estimated delivery date
And the email contains a link to my order status page

But if the order total is $0 (free trial), no payment confirmation is sent
```

## What Acceptance Criteria Must Include

### Happy Path
The primary successful use case:
- Who is the user?
- What are they doing?
- What happens when everything works?

### Edge Cases
Boundary conditions:
- Empty state (no data, first use)
- Single item vs many items
- Min and max values
- Long text / large files
- Special characters

### Error Handling
What happens when things go wrong:
- Invalid input (wrong format, out of range)
- Server error (500, timeout)
- Permission denied (unauthorized)
- Not found (resource doesn't exist)

### Non-Functional Requirements (when relevant)
- Performance: "Loads in < 2 seconds on 3G"
- Accessibility: "Meets WCAG 2.1 AA"
- Security: "Session expires after 30 min of inactivity"
- Browser/device: "Works on Chrome, Firefox, Safari; iOS 14+, Android 10+"

## AC Anti-Patterns

| Anti-Pattern | Fix |
|---|---|
| "Works correctly" | Define what correct means specifically |
| "Fast loading" | Specify: "< 2 seconds on desktop broadband" |
| "User-friendly" | Specify the behavior/UX expectation |
| "Like [competitor]" | Describe the actual behavior |
| Implementation detail ("use Redis") | AC defines behavior, not implementation |

## Completeness Check
For each story's AC, ask:
- Can QA write a test case from this AC?
- If a developer did only what the AC says (nothing more), would the feature be valuable?
- Have we covered the error cases?
- Are there any "and also..." requirements not yet captured?

## Output Format
- Acceptance criteria in Given/When/Then format for all stories
- Edge cases covered
- Error scenarios specified
- Non-functional requirements called out
