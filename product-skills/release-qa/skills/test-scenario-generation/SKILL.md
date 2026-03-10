---
name: test-scenario-generation
description: "Use when the user needs to generate test scenarios, think through edge cases, or create a comprehensive test matrix. Triggers on: 'test scenarios', 'edge cases', 'test matrix', 'what to test', 'test coverage', 'generate test cases', 'testing scenarios'."
---

# Test Scenario Generation

## Purpose
Systematically think through every scenario worth testing — ensuring comprehensive coverage without missing the cases that cause real bugs.

## Scenario Generation Techniques

### 1. Equivalence Partitioning
Group inputs into classes that should behave the same way. Test one representative from each class.

For a number input accepting 1-100:
- Valid: 1-100 (test: 50)
- Invalid low: < 1 (test: 0, -1)
- Invalid high: > 100 (test: 101, 999)
- Boundary: 1 and 100 (boundary values)

### 2. Boundary Value Analysis
Errors cluster at boundaries. Test:
- Minimum value
- Maximum value
- One below minimum
- One above maximum
- Typical value (midpoint)

### 3. Decision Table
Map all combinations of conditions to expected outcomes:

| Condition A | Condition B | Condition C | Expected Result |
|---|---|---|---|
| True | True | True | Result 1 |
| True | True | False | Result 2 |
| True | False | Any | Result 3 |

### 4. State Transition
For features with states, test each transition:
- Draft → Published
- Free → Paid → Cancelled
- Active → Suspended → Active again

Test both valid transitions AND invalid ones ("can I pay from a suspended state?")

### 5. Error Guessing
Based on experience, what commonly breaks?
- Empty inputs
- Very long strings
- Special characters (&, <, >, ", ', /)
- Unicode and emoji
- Null/undefined values
- Concurrent requests (race condition)
- Slow network
- Interrupted session (back button, closing tab)

## Standard Test Categories

For any feature, always cover:

**Happy Path**
- Primary use case, ideal inputs, expected flow

**Negative Path**
- Invalid inputs
- Missing required fields
- Wrong data types

**Edge Cases**
- Empty state (no data, first time user)
- Single item (list of one)
- Large data (hundreds of items, very long text)
- Special characters and encoding

**Permission / Authorization**
- Correct role can access
- Incorrect role is blocked
- Unauthenticated user is redirected

**Performance**
- Under normal load
- Under expected peak load

**Mobile / Cross-Platform** (if applicable)
- Different screen sizes
- Touch vs mouse interaction
- Different operating systems

## Test Scenario Template

```
Scenario: [Descriptive name]
Category: [Happy path / Error / Edge case / Permission / Performance]
Priority: P0 / P1 / P2

Setup:
- [Preconditions]

Steps:
1. [Action]
2. [Action]

Expected:
- [What should happen]

Variations to test:
- [Variation 1]
- [Variation 2]
```

## Output Format
- Complete test scenario list organized by category
- Priority classification for each scenario
- Edge cases specifically called out
- Test matrix (if comparing multiple conditions)
