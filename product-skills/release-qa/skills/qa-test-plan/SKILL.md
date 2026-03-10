---
name: qa-test-plan
description: "Use when the user needs to create a QA test plan, define testing strategy, write test cases, or plan quality assurance for a release. Triggers on: 'QA plan', 'test plan', 'test cases', 'testing strategy', 'quality assurance', 'write test cases', 'QA checklist'."
---

# QA Test Plan

## Purpose
Define a comprehensive quality assurance plan that systematically verifies a feature works as intended and doesn't break what already works.

## Test Plan Structure

### 1. Scope
- What feature/change is being tested?
- What is explicitly NOT in scope?
- What environments will be tested? (dev, staging, production)
- What platforms/browsers/devices?

### 2. Testing Types Required

**Functional Testing**
Does the feature do what it's supposed to do?
- Happy path: correct inputs, expected results
- Error paths: invalid inputs, edge cases, system errors
- Boundary conditions: min/max values, empty states, single-item lists

**Integration Testing**
Does the feature work with everything around it?
- Data flows correctly between systems
- APIs return expected responses
- Third-party integrations function correctly

**Regression Testing**
Did we break anything that was working before?
- Core user flows still work
- Adjacent features unaffected
- No performance degradation

**Performance Testing** (for impactful changes)
- Load time benchmarks
- Response time under load
- Database query performance

**Accessibility Testing**
- Screen reader compatibility
- Keyboard navigation
- Color contrast ratios
- WCAG 2.1 AA compliance

**Security Testing** (for auth/data features)
- Authorization: can users access only what they should?
- Input sanitization: XSS, SQL injection prevention
- Data exposure: sensitive data not leaked in responses

### 3. Test Case Structure

For each test case:
```
Test Case ID: TC-001
Feature: [Feature name]
Type: [Functional / Regression / Performance]
Priority: P0 / P1 / P2

Preconditions:
- User is logged in as [role]
- [Other state requirements]

Steps:
1. [Action]
2. [Action]
3. [Action]

Expected Result:
[What should happen]

Actual Result: [Fill in during testing]
Status: Pass / Fail / Blocked
```

### 4. Priority Classification
- **P0** (Critical): Must pass before any release. Core functionality, security, data integrity.
- **P1** (High): Should pass before release. Important functionality.
- **P2** (Medium): Nice to fix before release. Non-critical UX issues.
- **P3** (Low): Track and fix later. Minor issues.

### 5. Exit Criteria
Define when QA is complete:
- All P0 test cases: Pass
- All P1 test cases: Pass
- P2 cases: < 3 open, all with owner and fix date
- No open P0 or P1 defects
- Performance benchmarks met
- Regression suite passing

### 6. Defect Management
For each bug found:
- Priority (P0-P3)
- Reproducibility (always / intermittent / once)
- Steps to reproduce
- Expected vs actual behavior
- Environment (browser, OS, data state)
- Screenshots/recordings

## Acceptance Testing vs QA Testing
**QA Testing**: Done by QA team against technical spec
**Acceptance Testing** (UAT): Done by PM/stakeholder against user requirements (acceptance criteria)

Both are needed. QA catches bugs; UAT catches spec mismatches.

## Output Format
- Test plan document
- Test case list by priority
- Test coverage matrix (requirement → test case mapping)
- Exit criteria checklist
