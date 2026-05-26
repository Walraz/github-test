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

---

## Pull Request Procedure

This section defines the guidelines for creating Pull Requests (PRs). Use these rules when preparing and submitting code changes.

### 1. Show Draft First
Before executing any PR creation command, the AI assistant must present a draft of the PR title and description to the user for review and explicit approval.

### 2. Standardized PR Description Template
The PR description must adhere to the following structure:
- **Overview**: A high-level summary of the purpose of the PR and the problem being solved.
- **Changes Proposed**: A list of key modifications, file creations, or configuration changes.
- **Verification**: Documented proof that the changes work as intended (e.g., successful build output logs, manual visual check results).

### 3. Creation via GitHub CLI
Always use the GitHub CLI (`gh`) to automate PR creation. To prevent shell escaping errors, write the body of the PR to a temporary markdown file and reference it:
```bash
gh pr create --title "<title>" --body-file <path_to_temporary_body_file>
```

---

## Automatic Version Bumping

This project uses a Git hook to automatically bump the npm package version after every successful commit.

### 1. Mechanism
A `post-commit` Git hook is installed locally at `.git/hooks/post-commit`.

### 2. Logic
- Every time a commit is made, the hook triggers `npm version patch`.
- To prevent an infinite recursion loop (since `npm version patch` itself makes a commit), the hook inspects the commit message. If the message matches a semantic version (e.g. `v1.0.1` or `1.0.1`), it exits silently.


