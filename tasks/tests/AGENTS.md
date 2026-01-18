# TESTS POLICY

## Goal
Add/improve tests or testability.

## Process
1) Working set + Context loaded.
2) Define test scope (scenarios/boundaries).
3) Plan -> approval.
4) Test implementation (and minimal code changes for testability — only if described in the plan).
5) Verification.
6) Documentation updates by triggers.

## Prohibitions
- Do not do refactoring "along the way" (except minimal for tests and described in advance).

## Template `X-work.md` (test)
# Work (test)

Status: DRAFT | APPROVED | IN_PROGRESS | DONE
Task: <category>/<slug>.md | CHAT
Slug: X
Execution profile: (from docs/codex/PROJECT_CONTRACT.md or UNKNOWN)
Source: FILE | CHAT

### Working set
- ...

### Context loaded
- docs/codex/PROJECT_CONTRACT.md
- docs/codex/AGENT_GUIDE.md: ...
- (paths to CONTEXT.md / index that were actually read)

### Context capture
- Read settings from docs/codex/CONTEXT_INDEX.md and follow them.
- Status: <On|Off>

### Input (if Source=CHAT)
- User request:
  - ...
- Artifacts/links (if any):
  - ...

### Test scope
- Scenarios:
  - ...
- Boundaries:
  - ...

### Plan (DRAFT)
1) ...
2) ...

### Verification
- (test run/manual steps)

### Git
- Branch: tests/<slug>
- Commits (draft):
  - test: ...

### Notes/Risks
- ...
