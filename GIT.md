# Git Commit Message Conventions

This document outlines the commit message conventions to be used in this project. Use these rules whenever creating commit messages.

## Format

All commit messages should follow this pattern:

```
<type>(<file>, <short text>): <message>
```

- **type**: The type of change (see below).
- **file**: The file or component being modified (e.g. `App.vue`, `router.ts`, `LandingPage.vue`).
- **short text**: A brief context or summary of the change inside the parentheses (e.g., `add styles`, `fix alias`).
- **message**: A clear, descriptive message explaining the purpose of the commit.

---

## Commit Types

### 1. `feat`
Used when adding a new feature, component, slice, or layer.
* **Example**: `feat(LandingPage.vue, hero section): implement modern hero container with glowing gradients`

### 2. `fix`
Used for bug fixes, style adjustments, or correctness fixes.
* **Example**: `fix(tsconfig.app.json, relative mapping): change paths mapping to use relative prefix`

### 3. `bug`
Used to track or log a known issue or regression.
* **Example**: `bug(HelloWorld.vue, broken reactivity): flag count variable not updating correctly`

### 4. `change`
Used for general refactoring, updates, or maintenance modifications.
* **Example**: `change(tailwind.config.js, content scan): add source file paths to tailwind config`
