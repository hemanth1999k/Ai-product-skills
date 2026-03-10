---
name: heuristic-evaluation
description: "Use when the user wants to evaluate a product's UX against usability principles, run a heuristic audit, or identify UX issues without user testing. Triggers on: 'heuristic evaluation', 'UX audit', 'usability review', 'Nielsen heuristics', 'design review', 'UX principles check'."
---

# Heuristic Evaluation

## Purpose
Systematically evaluate a product's usability against established principles to identify UX issues quickly — without user testing.

## Nielsen's 10 Usability Heuristics

### H1: Visibility of System Status
Users should always know what's happening.
- Are loading states shown?
- Does the user know if an action succeeded or failed?
- Are progress indicators used for multi-step processes?

### H2: Match Between System and Real World
Speak the user's language, not system language.
- Is jargon used that users wouldn't know?
- Do labels match how users think about the task?
- Are icons universally understood?

### H3: User Control and Freedom
Easy escape from mistakes.
- Can users undo and redo?
- Can users easily cancel out of a flow?
- Is there a clear "back" path?

### H4: Consistency and Standards
Follow platform conventions.
- Are similar elements styled and labeled consistently?
- Do buttons look like buttons? Links like links?
- Does the product follow OS/platform conventions?

### H5: Error Prevention
Prevent errors before they happen.
- Are destructive actions protected with confirmation?
- Are form fields validated in real-time?
- Are clear constraints shown (character limits, required fields)?

### H6: Recognition Over Recall
Don't make users remember things.
- Are options visible rather than requiring memorization?
- Is context/state preserved when returning to a task?
- Are recently used items surfaced?

### H7: Flexibility and Efficiency of Use
Serve both novice and expert users.
- Are there keyboard shortcuts for power users?
- Can frequently used tasks be customized or accelerated?
- Is there a progressive disclosure path from simple to advanced?

### H8: Aesthetic and Minimalist Design
Remove irrelevant information.
- Does every element on screen earn its place?
- Is visual hierarchy clear?
- Is the primary action obvious?

### H9: Help Users Recognize, Diagnose, and Recover from Errors
Useful error messages.
- Are errors written in plain language (not error codes)?
- Do errors explain what went wrong and how to fix it?
- Are errors shown near where the problem occurred?

### H10: Help and Documentation
When needed, easy to find.
- Is help accessible without leaving the flow?
- Is search available in help content?
- Are docs kept current?

## Severity Rating Scale

Rate each issue found:
- **0** — Not a problem
- **1** — Cosmetic only (fix if time permits)
- **2** — Minor (low priority fix)
- **3** — Major (important to fix, high priority)
- **4** — Catastrophic (must fix before launch)

## Evaluation Process

1. **Scope the evaluation**: Which flows? Which user type?
2. **Walk through each flow** as the user would
3. **Log each violation**: Heuristic, location, description, screenshot/annotation, severity
4. **Prioritize**: Fix severity 4 and 3 first; batch severity 1 and 2

## Output Format
- Heuristic audit table (Heuristic | Issue | Location | Severity)
- Top 5 critical issues
- Quick wins list (severity 1-2, easy to fix)
- Redesign recommendations for severity 3-4
