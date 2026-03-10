---
name: bug-triage
description: "Use when the user needs to triage bugs, prioritize defects, run a bug triage process, or manage an issue queue. Triggers on: 'bug triage', 'defect triage', 'prioritize bugs', 'bug queue', 'issue triage', 'manage defects'."
---

# Bug Triage Process

## Purpose
Systematically evaluate, classify, and prioritize bugs to focus engineering effort on what matters most — not just what was filed most recently.

## Triage Criteria

### Severity (How bad is it?)
**S1 — Critical**: System down, data loss, security breach, core feature broken for all users
**S2 — High**: Major feature broken for significant portion of users, no workaround
**S3 — Medium**: Feature broken but workaround exists; non-critical feature broken
**S4 — Low**: Cosmetic issue, minor UX imperfection, edge case affecting few users

### Priority (How urgently must we fix it?)
**P0** — Fix now (hotfix if needed), before next release
**P1** — Fix in current or next sprint
**P2** — Add to backlog, prioritize in upcoming sprint planning
**P3** — Track, fix when convenient
**Won't Fix** — Not worth fixing (too rare, too minor, by design)

Note: Severity ≠ Priority. A severe bug affecting 0.001% of users may be P2. A low-severity bug that appears on the sales homepage may be P0.

## Triage Decision Tree

1. **Is this a data loss or security issue?** → S1/P0, fix immediately
2. **Is the core product broken for >10% of users?** → S1-S2/P0-P1
3. **Is there a workaround?** If yes → lower priority
4. **Who is affected?** Enterprise customer? → escalate priority
5. **What is the frequency?** Always reproducible? Intermittent? Once? → affects severity
6. **Is there business impact?** Sales blocked? SLA at risk? → escalate priority

## Bug Report Standard

A good bug report includes:
- **Title**: [Feature] What went wrong (not "it doesn't work")
- **Environment**: Browser, OS, account type, data state
- **Steps to reproduce**: Numbered, specific, minimal
- **Expected result**: What should happen
- **Actual result**: What happens instead
- **Frequency**: Always / 50% / intermittent / once
- **Impact**: How many users? What's the business impact?
- **Attachments**: Screenshot, screen recording, logs

## Triage Meeting Structure (Weekly, 30 min)

1. Review new bugs since last triage (everyone reads, not presenter-reads)
2. Classify each: Severity + Priority + Owner
3. For P0/P1: Assign sprint, confirm owner, set ETA
4. For "Won't Fix": Document rationale
5. Metrics review: # new, # resolved, # aging (>30 days unresolved)

## Bug Aging Policy
- P0: Must be resolved within 24-48 hours
- P1: Must be resolved within current sprint
- P2: If unresolved for 60 days, re-triage or close
- P3: If unresolved for 90 days, re-triage or move to icebox

## Output Format
- Bug classification for each submitted issue (Severity + Priority + recommendation)
- Triage meeting agenda
- Aging bug report
- Recommended sprint allocation for bug work vs feature work
