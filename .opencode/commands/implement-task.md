---
description: Implement an approved plan from prompts/, touching only the files it lists.
agent: build
---

Implement the approved plan: $ARGUMENTS

Before writing code:
- Open the plan file. If it is not marked approved in this session, stop and ask.
- Read the context files and skills the plan names.
- Check installed versions of any library you will call.

While implementing:
- Change only the files in "Files to create" / "Files to modify".
- If you need another file or a different approach, stop and propose a plan update.
- No unrelated refactors.

After implementing, run the narrowest relevant checks and report:
- changed files
- commands run + real results
- acceptance criteria: met / not met
- open issues
