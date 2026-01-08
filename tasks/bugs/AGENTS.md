# BUGS POLICY

## Goal
Fix bug with minimal change.

## Process
1) Repro/symptoms.
2) Root cause hypothesis.
3) Plan -> approval.
4) Fix.
5) Verification.
6) Doc updates by triggers.

## Prohibitions
- Do not refactor "along the way" without explicit item in plan.
- Do not change PROJECT_CONTRACT, unless it's a separate agreement.

## Template `X-work.md` (bugs)
# Work (bugs)

Status: DRAFT | APPROVED | IN_PROGRESS | DONE
Task: bugs/X.md
Slug: X
Execution profile: (from docs/codex/PROJECT_CONTRACT.md or UNKNOWN)

### Working set
- ...

### Context loaded
- docs/codex/PROJECT_CONTRACT.md
- docs/codex/AGENT_GUIDE.md: ...
- (CONTEXT.md paths / index that were actually read)

### Context capture
- Read settings from docs/codex/CONTEXT_INDEX.md and follow them.
- Status: <On|Off>

### Repro
- Steps:
  1) ...
- Observed:
- Expected:
- Scope/Impact:

### Root cause hypothesis
- ...

### Plan (DRAFT)
1) ...
2) ...

### Verification
- (commands/manual steps, expected result)

### Git
- Branch: bugs/X
- Commits (draft):
  - fix: ...

### Notes/Risks
- ...
