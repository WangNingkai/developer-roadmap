```markdown
# developer-roadmap Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the development patterns and workflows used in the `developer-roadmap` repository, a TypeScript project focused on providing visual roadmaps for developers. The repository manages multiple language translations, roadmap images, and JSON map files, and follows consistent coding and workflow conventions to streamline contributions and maintenance.

## Coding Conventions

- **File Naming:**  
  Use **kebab-case** for all file names.
  ```
  backend-map.json
  frontend-map.json
  devops-map.json
  ```
- **Import Style:**  
  Use **relative imports** for modules and assets.
  ```typescript
  import { getNode } from './utils';
  import roadmapData from '../src/backend-map.json';
  ```
- **Export Style:**  
  Use **named exports** for functions, constants, and objects.
  ```typescript
  // utils.ts
  export function getNode(id: string) { ... }
  export const ROADMAPS = ['backend', 'frontend', 'devops'];
  ```
- **Commit Messages:**  
  - Prefix with `feat` for new features, or use language name for translation updates (e.g., `indonesian`).
  - Freeform, concise messages (~33 characters on average).
  ```
  feat: add docker to devops roadmap
  indonesian: update translation images
  ```

## Workflows

### Add New Language Translation
**Trigger:** When you want to add a full translation for a new language.  
**Command:** `/add-new-language-translation`

1. Create `translations/<language>/readme.md` with the translated roadmap description.
2. Add roadmap images to `translations/<language>/img/*.png`.
3. Add roadmap map files to `translations/<language>/src/*.json`.
4. Optionally, update `translations/readme.md` to list the new language.

**Example:**
```
translations/spanish/readme.md
translations/spanish/img/backend.png
translations/spanish/src/backend-map.json
```

---

### Update Existing Translation
**Trigger:** When you want to fix, improve, or sync an existing translation.  
**Command:** `/update-existing-translation`

1. Edit `translations/<language>/readme.md` or `README.md` as needed.
2. Update images in `translations/<language>/img/*.png` or map files in `translations/<language>/src/*.json`.
3. Optionally, update `translations/readme.md` if the change is significant.

**Example:**
```
translations/french/readme.md
translations/french/img/frontend.png
translations/french/src/frontend-map.json
```

---

### Update Roadmap Core
**Trigger:** When you want to update the main roadmap content (not language-specific).  
**Command:** `/update-roadmap-core`

1. Edit the relevant core JSON map file in `src/` (e.g., `src/backend-map.json`).
2. Update the corresponding image in `img/` (e.g., `img/backend.png`).
3. Optionally, update `README.md` to reflect the changes.

**Example:**
```
src/devops-map.json
img/devops.png
README.md
```

---

### Add Sponsor or Funding Info
**Trigger:** When you want to add or update sponsor logos or funding details.  
**Command:** `/add-sponsor`

1. Add or update sponsor logo files in `.github/sponsors/*.png` or `.github/sponsors/*.svg`.
2. Edit `README.md` to display the sponsor.
3. Edit `.github/FUNDING.yml` as needed.

**Example:**
```
.github/sponsors/new-sponsor.png
.github/FUNDING.yml
README.md
```

## Testing Patterns

- **Test File Naming:**  
  Test files use the pattern `*.test.*` (e.g., `utils.test.ts`).
- **Framework:**  
  The specific testing framework is not detected, but tests are colocated with source files using the above pattern.

**Example:**
```
src/utils.test.ts
```

## Commands

| Command                           | Purpose                                                |
|------------------------------------|--------------------------------------------------------|
| /add-new-language-translation      | Add a full translation for a new language              |
| /update-existing-translation       | Update or fix an existing translation                  |
| /update-roadmap-core               | Update core roadmap files or images                    |
| /add-sponsor                       | Add or update sponsor logos or funding information     |
```
