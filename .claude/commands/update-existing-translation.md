---
name: update-existing-translation
description: Workflow command scaffold for update-existing-translation in developer-roadmap.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-existing-translation

Use this workflow when working on **update-existing-translation** in `developer-roadmap`.

## Goal

Updates or fixes an existing translation, such as correcting typos, updating images, or syncing JSON map files.

## Common Files

- `translations/<language>/readme.md`
- `translations/<language>/README.md`
- `translations/<language>/img/*.png`
- `translations/<language>/src/*.json`
- `translations/readme.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit translations/<language>/readme.md or README.md
- Edit translations/<language>/img/*.png or translations/<language>/src/*.json as needed
- Optionally update translations/readme.md if the change is significant

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.