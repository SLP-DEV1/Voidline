# Contributing to Voidline

Thanks for taking the time to improve the project.

## Current repository state

The current repository contains a prebuilt runtime bundle rather than the C# source tree. Until the source is published, contributions are most useful in these areas:

- Documentation corrections
- Packaging and repository-structure improvements
- Reproducible runtime bug reports
- Dependency or compatibility findings
- Release-process improvements

Code contributions will become practical once the source tree and project files are available in the repository.

## Reporting a bug

Please include:

1. The Voidline release/tag you tested.
2. Windows version.
3. Installed .NET runtime version.
4. Clear reproduction steps using a local/offline or otherwise authorized test environment.
5. Expected behavior.
6. Actual behavior and any error text or logs.
7. Whether the issue reproduces consistently.

Avoid reports whose purpose is anti-cheat bypass, ban avoidance, or evasion. Those are not treated as product bugs or security issues.

## Suggesting an improvement

Good proposals explain the user problem first and the proposed solution second. For repository changes, examples are especially useful: a cleaner folder layout, a release workflow, documentation structure, or reproducible packaging issue.

## Pull requests

Keep pull requests focused and small enough to review. Please:

- Explain what changed and why.
- Link an issue when one exists.
- Update documentation when behavior or repository structure changes.
- Avoid committing local state, generated files, build output, secrets, or editor configuration.
- Use clear commit messages.

## Commit style

Conventional-commit-style prefixes are encouraged but not mandatory:

- `feat:` new behavior
- `fix:` bug fix
- `docs:` documentation
- `chore:` maintenance
- `refactor:` internal restructuring
- `test:` tests
- `ci:` automation

## Scope and responsible use

Contributions should be suitable for authorized research, local/offline testing, documentation, diagnostics, or general software-engineering work. Requests specifically aimed at bypassing anti-cheat protections or disrupting public matches are out of scope.
