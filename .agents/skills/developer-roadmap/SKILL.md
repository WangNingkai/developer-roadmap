```markdown
# developer-roadmap Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill covers the core development patterns, coding conventions, and content workflows for the `developer-roadmap` project. The codebase is primarily written in TypeScript, uses the Astro framework, and organizes roadmap content and structure in markdown and JSON files. The repository emphasizes clear commit messages, consistent file organization, and streamlined content synchronization from external sources.

## Coding Conventions

### File Naming

- All files use **kebab-case**.
  - Example: `roadmap-content.ts`, `frontend.json`, `question-group.spec.ts`

### Import Style

- **Relative imports** are used throughout the codebase.
  - Example:
    ```typescript
    import roadmapData from '../data/roadmaps/frontend/content/roadmap-content';
    ```

### Export Style

- **Mixed export styles**: Both named and default exports are present.
  - Example (default export):
    ```typescript
    export default function Roadmap() { ... }
    ```
  - Example (named export):
    ```typescript
    export const getRoadmapData = () => { ... }
    ```

### Commit Messages

- **Conventional commit** format is used.
- Common prefixes: `chore`, `fix`, `docs`
- Example:
  ```
  chore: sync content to repo
  fix: correct typo in backend roadmap
  docs: update contributing guidelines
  ```

## Workflows

### sync-content-to-repo

**Trigger:** When you want to update the repository with the latest content from an external source or CMS.  
**Command:** `/sync-content`

1. Fetch new or updated content files from the external source.
2. Copy or update multiple markdown files in the appropriate `src/data/roadmaps/*/content/` and `src/data/question-groups/*/content/` directories.
3. Commit all changes with a standardized message, such as:
   ```
   chore: sync content to repo
   ```

**Files involved:**
- `src/data/roadmaps/*/content/*.md`
- `src/data/question-groups/*/content/*.md`

### fix-or-update-single-content-file

**Trigger:** When you need to fix a typo, update a resource link, or improve formatting in a single roadmap topic.  
**Command:** `/edit-content`

1. Edit the relevant markdown file in `src/data/roadmaps/*/content/`.
2. Commit the change with a descriptive message, for example:
   ```
   fix: update link in frontend roadmap
   ```

**Files involved:**
- `src/data/roadmaps/*/content/*.md`

### add-or-update-roadmap-json

**Trigger:** When you want to update the roadmap structure or fix/add resource links.  
**Command:** `/edit-roadmap-json`

1. Edit the roadmap JSON file (e.g., `frontend.json`, `mlops.json`, `rust.json`) in `src/data/roadmaps/*/`.
2. Commit the change with a descriptive message, such as:
   ```
   chore: update frontend roadmap structure
   ```

**Files involved:**
- `src/data/roadmaps/*/*.json`

## Testing Patterns

- **Framework:** Playwright
- **Test file pattern:** `*.spec.ts`
- Example test file: `roadmap.spec.ts`
- Example test:
  ```typescript
  import { test, expect } from '@playwright/test';

  test('roadmap page loads', async ({ page }) => {
    await page.goto('/roadmaps/frontend');
    await expect(page).toHaveTitle(/Frontend Roadmap/);
  });
  ```

## Commands

| Command            | Purpose                                                      |
|--------------------|--------------------------------------------------------------|
| /sync-content      | Synchronize content from an external source or CMS           |
| /edit-content      | Edit or fix a single roadmap content markdown file           |
| /edit-roadmap-json | Update roadmap structure or resource links in JSON files     |
```
