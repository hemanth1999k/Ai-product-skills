---
name: concept-testing
description: "Use when the user wants to test a product concept, idea, or prototype before building it. Triggers on: 'concept test', 'test the idea', 'validate concept', 'before we build', 'fake door', 'landing page test', 'prototype test'."
---

# Concept Testing

## Purpose
Validate a product concept with real users before committing engineering resources using the cheapest, fastest method possible.

## Concept Testing Methods (by cost/speed)

### 1. Fake Door Test (Fastest, Cheapest)
Add a button/link/feature as if it exists. Measure click rate.
- Best for: Testing demand before building
- Time: 1-2 days
- Success metric: Click-through rate > X%
- Learning: Do users even want this?

### 2. Landing Page Test
Create a landing page describing the concept. Drive traffic. Measure signups/waitlist.
- Best for: New products or major features
- Time: 3-5 days
- Success metric: Email capture rate > X%
- Learning: Does the value proposition resonate?

### 3. Paper Prototype / Mockup Test
Show wireframes or mockups to users. Ask them to walk through the flow.
- Best for: UX validation, flow testing
- Time: 1 week
- Success metric: Task completion rate, confusion points
- Learning: Can users figure this out?

### 4. Concierge Test (Alberto Savoia)
Manually do the thing the product would automate. Deliver the outcome without the tech.
- Best for: Validating value before automating
- Time: 1-4 weeks
- Success metric: Do users come back? Do they pay?
- Learning: Is the outcome valuable enough?

### 5. Wizard of Oz Test
Build a frontend that looks automated but is manually operated behind the scenes.
- Best for: AI/ML features, complex workflows
- Time: 1-2 weeks
- Success metric: User retention, NPS, task completion
- Learning: Is the output good enough to retain users?

### 6. Smoke Test / Pretotype (Alberto Savoia)
Ship the absolute minimum version to test core behavior.
- Best for: Novel product hypotheses
- Time: Varies
- The goal: "Make sure you are building The Right It before you build It right"

## Concept Test Design Template

For any concept test, define:
1. **Hypothesis**: "We believe [users] will [behavior] because [reason]"
2. **Test method**: Which of the above
3. **Minimum viable test**: What's the smallest thing we can ship
4. **Success metrics**: What numbers prove/disprove the hypothesis
5. **Timeline**: When will we have enough data
6. **Decision rule**: If metric > X, we proceed. If < Y, we pivot.

## Output Format
- Concept summary
- Recommended test method with rationale
- Hypothesis statement
- Test design plan
- Success/failure thresholds
