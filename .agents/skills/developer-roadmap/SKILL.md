---
name: developer-roadmap-conventions
description: Development conventions and patterns for developer-roadmap. TypeScript project with freeform commits.
---

# Developer Roadmap Conventions

> Generated from [WangNingkai/developer-roadmap](https://github.com/WangNingkai/developer-roadmap) on 2026-04-01

## Overview

This skill teaches Claude the development patterns and conventions used in developer-roadmap.

## Tech Stack

- **Primary Language**: TypeScript
- **Architecture**: hybrid module organization
- **Test Location**: separate

## When to Use This Skill

Activate this skill when:
- Making changes to this repository
- Adding new features following established patterns
- Writing tests that match project conventions
- Creating commits with proper message format

## Commit Conventions

Follow these commit message conventions based on 200 analyzed commits.

### Commit Style: Free-form Messages

### Prefixes Used

- `feat`
- `indonesian`

### Message Guidelines

- Average message length: ~32 characters
- Keep first line concise and descriptive
- Use imperative mood ("Add feature" not "Added feature")


*Commit message example*

```text
feat: add developer-roadmap ECC bundle (.claude/commands/fix-or-update-single-content-file.md)
```

*Commit message example*

```text
indonesian: change word 'intid' to 'init.d'
```

*Commit message example*

```text
fix: electro misspelling and color for legend
```

*Commit message example*

```text
feat: add developer-roadmap ECC bundle (.claude/commands/sync-content-to-repo.md)
```

*Commit message example*

```text
feat: add developer-roadmap ECC bundle (.claude/commands/feature-development.md)
```

*Commit message example*

```text
feat: add developer-roadmap ECC bundle (.codex/agents/docs-researcher.toml)
```

*Commit message example*

```text
feat: add developer-roadmap ECC bundle (.codex/agents/reviewer.toml)
```

*Commit message example*

```text
feat: add developer-roadmap ECC bundle (.codex/agents/explorer.toml)
```

## Architecture

### Project Structure: Single Package

This project uses **hybrid** module organization.

### Guidelines

- This project uses a hybrid organization
- Follow existing patterns when adding new code

## Code Style

### Language: TypeScript

### Naming Conventions

| Element | Convention |
|---------|------------|
| Files | kebab-case |
| Functions | camelCase |
| Classes | PascalCase |
| Constants | SCREAMING_SNAKE_CASE |

### Import Style: Relative Imports

### Export Style: Named Exports


*Preferred import style*

```typescript
// Use relative imports
import { Button } from '../components/Button'
import { useAuth } from './hooks/useAuth'
```

*Preferred export style*

```typescript
// Use named exports
export function calculateTotal() { ... }
export const TAX_RATE = 0.1
export interface Order { ... }
```

## Common Workflows

These workflows were detected from analyzing commit patterns.

### Feature Development

Standard feature implementation workflow

**Frequency**: ~15 times per month

**Steps**:
1. Add feature implementation
2. Add tests for feature
3. Update documentation

**Example commit sequence**:
```
add gridsome to frontend (#701)
Add Bengali translations for introduction and backend roadmaps (#702)
Fix some grammar in "Learn a Language" (#704)
```

### Add New Language Translation

Adds support for a new language translation, including roadmap images, JSON data, and translated README.

**Frequency**: ~1 times per month

**Steps**:
1. Create translated readme file in translations/<language>/readme.md or README.md
2. Add translated roadmap images to translations/<language>/img/*.png
3. Add translated roadmap JSON files to translations/<language>/src/*.json
4. Optionally update translations/readme.md to link to new language

**Files typically involved**:
- `translations/<language>/readme.md`
- `translations/<language>/README.md`
- `translations/<language>/img/*.png`
- `translations/<language>/src/*.json`
- `translations/readme.md`

**Example commit sequence**:
```
Create translated readme file in translations/<language>/readme.md or README.md
Add translated roadmap images to translations/<language>/img/*.png
Add translated roadmap JSON files to translations/<language>/src/*.json
Optionally update translations/readme.md to link to new language
```

### Update Existing Translation

Updates an existing translation, such as fixing typos, updating images, or syncing with the main roadmap.

**Frequency**: ~2 times per month

**Steps**:
1. Edit the relevant translation file(s) (readme.md, roadmap images, or JSON)
2. Commit changes with a message referencing the language and nature of the update

**Files typically involved**:
- `translations/<language>/*`

**Example commit sequence**:
```
Edit the relevant translation file(s) (readme.md, roadmap images, or JSON)
Commit changes with a message referencing the language and nature of the update
```

### Add Or Update Roadmap Section

Adds or updates a section of the roadmap, affecting both the image and JSON representation.

**Frequency**: ~1 times per month

**Steps**:
1. Edit the relevant roadmap JSON file in src/<section>-map.json
2. Update the corresponding image in img/<section>.png
3. Optionally update translations of the same section

**Files typically involved**:
- `src/<section>-map.json`
- `img/<section>.png`

**Example commit sequence**:
```
Edit the relevant roadmap JSON file in src/<section>-map.json
Update the corresponding image in img/<section>.png
Optionally update translations of the same section
```

### Add Or Update Sponsor Info

Adds or updates sponsor logos and funding information in the repository.

**Frequency**: ~1 times per month

**Steps**:
1. Add or update sponsor logo in .github/sponsors/*.png or *.svg
2. Update README.md to reflect sponsor changes
3. Edit .github/FUNDING.yml if funding info changes

**Files typically involved**:
- `.github/sponsors/*.png`
- `.github/sponsors/*.svg`
- `.github/FUNDING.yml`
- `README.md`

**Example commit sequence**:
```
Add or update sponsor logo in .github/sponsors/*.png or *.svg
Update README.md to reflect sponsor changes
Edit .github/FUNDING.yml if funding info changes
```


## Best Practices

Based on analysis of the codebase, follow these practices:

### Do

- Use kebab-case for file names
- Prefer named exports

### Don't

- Don't deviate from established patterns without discussion

---

*This skill was auto-generated by [ECC Tools](https://ecc.tools). Review and customize as needed for your team.*
