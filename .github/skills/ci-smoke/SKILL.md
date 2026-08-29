---
name: ci-smoke
description: "Triggered when GitHub Actions validates skill checks in CI; follows scoped editing conventions."
review:
  state: draft
---

# CI smoke skill

Minimal skill file used to dogfood ModelBound Skill Check in CI.

Follow project conventions when editing agent skills in this repository.

Run lint and verify trust score before merging.

## Scope Constraints (hard limits — split task if exceeded)

- **Max files per task:** 5
- **Max lines of code changed per task:** 250
- **Max features per task:** 1

If any of these would be exceeded, STOP and produce a split plan instead of writing code:

<task-split>
  <reason>Why this exceeds scope</reason>
  <subtasks>
    <task name="..." files="..." exit-criteria="..." />
  </subtasks>
</task-split>
