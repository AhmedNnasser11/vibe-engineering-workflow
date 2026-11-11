---
description: Sync context files after an approved decision or completed task.
agent: build
---

Synchronize context for: $ARGUMENTS

Edit only `context/`, `decisions/`, and `prompts/`.

1. `context/progress-tracker.md` — mark the task done, one line, link the plan.
2. `context/project-map.md` — add/remove any paths the task created or deleted. Do not invent paths.
3. If an architecture decision was approved, write `decisions/ADR-XXX-<slug>.md` from the template.
4. Move the finished plan to `prompts/completed/`.
5. Report which files changed.
