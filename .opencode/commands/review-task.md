---
description: Review an implementation against its approved plan and project rules. Read-only.
agent: plan
---

Review the implemented task: $ARGUMENTS

Do not edit code. Run `git diff` and compare against the approved plan.

Check:
- scope: any file changed that the plan did not list?
- architecture boundaries and imports
- TypeScript strictness (AGENTS.md §8)
- tenant scoping and secrets (AGENTS.md §9)
- UI: desktop / tablet / mobile / RTL / LTR / a11y
- tests, typecheck, lint evidence
- context and docs updated?

Report findings as Blocker / Should fix / Nit, each with file:line. List anything that needs human approval.
