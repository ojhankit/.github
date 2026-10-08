# Contributing to SANCHARI

Thank you for contributing to SANCHARI.

Please follow the branch and development workflow below.

## 1. Branch Structure

We use the following branch structure:

```text
main
  │
  └── develop
        │
        ├── feature/input
        ├── feature/network
        ├── feature/routing
        ├── feature/scheduling
        ├── feature/validation
        ├── feature/simulation
        └── feature/gui
```

* `main` — stable, release-ready code
* `develop` — integration branch for ongoing development
* `feature/*` — individual feature or module development

## 2. Creating a Feature Branch

Always create your feature branch from the latest `develop`.

```cmd
git switch develop
git pull origin develop
git switch -c feature/<feature-name>
```

Example:

```cmd
git switch develop
git pull origin develop
git switch -c feature/routing
```

Do not develop directly on `main` or `develop`.

## 3. Keep Your Branch Updated

If `develop` changes while you are working, update your feature branch before creating a Pull Request.

```cmd
git switch develop
git pull origin develop

git switch feature/<feature-name>
git merge develop
```

Resolve any conflicts, run the tests, and then push your branch.

## 4. Commits

Use clear and descriptive commit messages.

Examples:

```text
feat: add path generation
fix: handle disconnected network
test: add routing validation tests
refactor: simplify network graph
docs: update setup instructions
```

## 5. Pull Requests

When your feature is complete:

```cmd
git push -u origin feature/<feature-name>
```

Create a Pull Request:

```text
feature/<feature-name> → develop
```

Before creating the PR:

* Make sure your branch is up to date with `develop`
* Run all relevant tests
* Make sure the application still works
* Keep the PR focused on one feature or change

After review and approval, the branch can be merged into `develop`.

## 6. Releases

Only stable code should be merged from:

```text
develop → main
```

The `main` branch should always remain in a usable state.

---

## Quick Workflow

For every new feature:

```cmd
git switch develop
git pull origin develop

git switch -c feature/<feature-name>

# do your work

git add .
git commit -m "feat: <description>"

git push -u origin feature/<feature-name>
```

Then open a Pull Request from:

```text
feature/<feature-name> → develop
```

For more details about project setup, see [README.md](README.md).
