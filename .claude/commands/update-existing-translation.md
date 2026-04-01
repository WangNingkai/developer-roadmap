---
name: update-existing-translation
description: Workflow command scaffold for update-existing-translation in developer-roadmap.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-existing-translation

Use this workflow when working on **update-existing-translation** in `developer-roadmap`.

## Goal

Updates an existing translation, such as fixing typos, updating images, or syncing with the main roadmap.

## Common Files

- `translations/<language>/*`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit the relevant translation file(s) (readme.md, roadmap images, or JSON)
- Commit changes with a message referencing the language and nature of the update

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.