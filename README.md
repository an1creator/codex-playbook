# Codex Playbook

Playbook for consistent, repeatable Codex-assisted development in any repository (language- and architecture-agnostic).

## What you get

- Task folders as workflow modes: `bugs/`, `features/`, `refactoring/`, `test/`, `plans/`
- Two-phase protocol: plan → approval → execution (tracked in `*-work.md`)
- Stable project contract: how to run/verify the project (docker/host/hybrid), locked after bootstrap
- Context documentation: `CONTEXT.md` near code + `docs/codex/CONTEXT_INDEX.md` generated from real changes (diff triggers)
- Completed task archive: move finished `*.md` and `*-work.md` into `*/completed/`

## Template structure

```text
<project>/
  tasks
    bugs/
        AGENTS.md
        completed/
    features/
        AGENTS.md
        completed/
    refactoring/
        AGENTS.md
        completed/
    test/
        AGENTS.md
        completed/
    plans/
        AGENTS.md
        bootstrap.md
        completed/
  docs/codex/
    PROJECT_CONTRACT.md
    AGENT_GUIDE.md
    CONTEXT_INDEX.md
    templates/
      CONTEXT.md
  AGENTS.md
  ...
  <code files and folders...>
```

## Core workflow

1) Create a task file in the right category folder:
- `features/<slug>.md`, `bugs/<slug>.md`, etc.

2) Start the session:
- Create `features/<slug>-work.md` next to the task file.
- Fill **Working set** + **Context loaded** before writing the Plan.
- Ask for approval.

3) Execute only after approval:
- No code changes until `Status: APPROVED`.

4) Verify and document (diff-driven):
- Run the relevant checks from `docs/codex/PROJECT_CONTRACT.md` (or manual verification if tools don’t exist).
- If this is the first code-changing task and `docs/codex/CONTEXT_INDEX.md` is missing:
  - Create it.
  - Add `CONTEXT.md` to key folders touched by `git diff --name-only`.
  - Add index entries pointing to those `CONTEXT.md`.

5) Complete and archive:
- Set `Status: DONE` in `<slug>-work.md`.
- Move both files to `*/completed/`:
  - `features/completed/<slug>.md`
  - `features/completed/<slug>-work.md`

## Bootstrap (one-time)

Create `plans/bootstrap.md` and run it in planning-only mode to generate:
- `docs/codex/PROJECT_CONTRACT.md` (DRAFT → LOCKED after confirmation)
- `docs/codex/AGENT_GUIDE.md`
- Ensure `docs/codex/templates/CONTEXT.md` exists (create if missing)

After the first code-changing task, generate:
- `docs/codex/CONTEXT_INDEX.md`
- initial `CONTEXT.md` files in key touched folders (diff trigger)

## Files overview

- `AGENTS.global.md` (~/.codex/): global Rules (universal for any repositories)
- `AGENTS.md` (project_root): hard gates + workflow rules + where policies live
- `<category>/AGENTS.md`: category-specific policy + `*-work.md` template
- `docs/codex/PROJECT_CONTRACT.md`: execution profiles + verification tasks (LOCKED)
- `docs/codex/AGENT_GUIDE.md`: repo map, entry points, invariants (no code)
- `docs/codex/CONTEXT_INDEX.md`: path → CONTEXT.md pointers
- `<folder>/CONTEXT.md`: local invariants/risks/boundaries
- `docs/codex/templates/CONTEXT.md`: canonical template for new CONTEXT files

## Recommended setup

- Put global, repo-agnostic rules in `~/.codex/AGENTS.md`.
- Keep all project-specific rules inside the repository.
- Treat `docs/codex/PROJECT_CONTRACT.md` as the single source of truth for run/verify commands.

## License

MIT.