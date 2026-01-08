# Project Bootstrap for Codex

Category: plans
Mode: planning-only (do not modify code)

## Goal
Prepare a minimal set of stable documents:
1) docs/codex/PROJECT_CONTRACT.md (first DRAFT, then LOCKED after agreement)
2) docs/codex/AGENT_GUIDE.md

## Constraints
- Do not modify project code.
- Do not add dependencies.
- Do not invent commands: if cannot be proven from repository — set UNKNOWN and ask a question.

## Steps
1) Repository structure overview:
   - root folders map
   - assumed code zones
   - entry points (scripts/CLI/HTTP/jobs/cron/migrations/config)

2) Create docs/codex/AGENT_GUIDE.md:
   - folder map
   - entry points
   - invariants/risks visible from structure and documentation

3) Create docs/codex/PROJECT_CONTRACT.md (DRAFT):
   - execution profiles (docker/host/hybrid), default=UNKNOWN if unclear
   - dev/test/lint/format/build commands (if found)
   - verification tasks (present/absent/manual/unknown)

4) Local context template (CONTEXT.md)
   - Open `docs/codex/templates/CONTEXT.md`.
   - If file already exists: verify that structure is up-to-date and matches accepted format (Scope/Boundaries/Invariants/Pitfalls/Risks/Dependencies/Verification).
     - If changes needed — propose edit and apply only after explicit confirmation.


5) Questions to user (only blockers for LOCKED):
   - what is the default execution profile?
   - what are canonical commands for dev/test/lint/format/build (if not found)
   - are there mandatory manual checks (if no automated ones)

6) After response:
   - update PROJECT_CONTRACT
   - set status to LOCKED

## Output artifacts
- docs/codex/PROJECT_CONTRACT.md (LOCKED)
- docs/codex/AGENT_GUIDE.md
