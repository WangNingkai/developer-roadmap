---
name: add-new-language-translation
description: Workflow command scaffold for add-new-language-translation in developer-roadmap.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-new-language-translation

Use this workflow when working on **add-new-language-translation** in `developer-roadmap`.

## Goal

Adds support for a new language translation, including roadmap images, JSON maps, and readme files.

## Common Files

- `translations/<language>/readme.md`
- `translations/<language>/img/*.png`
- `translations/<language>/src/*.json`
- `translations/readme.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create translations/<language>/readme.md
- Add translations/<language>/img/*.png (roadmap images)
- Add translations/<language>/src/*.json (roadmap map files)
- Optionally update translations/readme.md to list the new language

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.