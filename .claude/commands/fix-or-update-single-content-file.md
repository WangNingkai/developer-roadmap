---
name: fix-or-update-single-content-file
description: Workflow command scaffold for fix-or-update-single-content-file in developer-roadmap.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /fix-or-update-single-content-file

Use this workflow when working on **fix-or-update-single-content-file** in `developer-roadmap`.

## Goal

Make a targeted fix or update to a single roadmap content markdown file, such as correcting typos, fixing links, or improving formatting.

## Common Files

- `src/data/roadmaps/*/content/*.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit the relevant markdown file in src/data/roadmaps/*/content/.
- Commit the change with a descriptive message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.