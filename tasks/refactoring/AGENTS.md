# REFACTORING POLICY

## Goal
Improve structure/maintainability without changing external behavior.

## Process
1) Define boundaries and what we consider "behavior".
2) Working set + Context loaded.
3) Plan -> approval.
4) Refactoring in small steps.
5) Verification.
6) Documentation updates by triggers.

## Prohibitions
- Do not change public interfaces without an explicit item in the plan.
- Do not mix with feature/bug fix.

## Template `X-work.md` (refactoring)
# Work (refactoring)

Status: DRAFT | APPROVED | IN_PROGRESS | DONE
Task: refactoring/X.md
Slug: X
Execution profile: (from docs/codex/PROJECT_CONTRACT.md or UNKNOWN)

### Working set
- ...

### Context loaded
- docs/codex/PROJECT_CONTRACT.md
- docs/codex/AGENT_GUIDE.md: ...
- (paths to CONTEXT.md / index that were actually read)

### Context capture
- Read settings from docs/codex/CONTEXT_INDEX.md and follow them.
- Status: <On|Off>

### Goal
- ...

### Behavior boundaries (what we don't change)
- ...

### Plan (DRAFT)
1) ...
2) ...

### Verification
- ...

### Git
- Branch: refactoring/X
- Commits (draft):
  - refactor: ...

### Notes/Risks
- ...
