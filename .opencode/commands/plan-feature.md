---
description: Inspect the real code and write an implementation plan to prompts/. Never implements.
agent: plan
---

Plan this request: $ARGUMENTS

1. Read `context/project-map.md`. Pick only the context files and skills this task needs (see AGENTS.md §3).
2. Load the `vibe-planning` skill.
3. Inspect the code you will touch. Name every file you read.
4. Write the plan using the skill template. Next free ID: check `prompts/` and `prompts/completed/`.
5. Save it as `prompts/T-XXX-<slug>.md`.
6. Reply with: plan path, a 5-line summary, and the "Decisions requiring approval" list.

Do NOT edit any file outside `prompts/`. Stop after saving the plan.
