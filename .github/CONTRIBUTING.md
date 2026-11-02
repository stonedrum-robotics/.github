# Contributing

Thanks for helping improve Stonedrum Robotics open-source dexterous-hand tooling. The repositories contain Python interfaces, mock-mode examples and reference documents. Each repository's README says what it covers.

## Issue Reporting

Use GitHub Issues for reproducible bugs, missing documentation, integration problems and feature requests. Issues are public: please do not include credentials, tokens, customer or supplier information, private logs or recordings, and report vulnerabilities privately as described in the security policy (`SECURITY.md`).

For bugs, include:

- Repository name and SDK version or commit SHA.
- Operating system, Python version and, if relevant, ROS 2 distribution.
- Whether you used mock mode, a simulator or other hardware, and which.
- Minimal code, launch command or trimmed output that reproduces the issue.
- Expected behavior and actual behavior.
- Any safety-relevant context, such as unexpected motion or limit handling.

For feature requests, include:

- The use case and target user.
- The hand model, robot arm, simulator or ROS 2 package involved.
- A proposed API or workflow if you already have one.
- Whether you are willing to test or contribute the change.

## Pull Request Process

1. Fork the relevant repository.
2. Create a focused branch from `main`.
3. Make the smallest coherent change that solves the issue.
4. Add or update tests for new behavior.
5. Run the local checks described in the repository before opening a pull request.
6. Open a pull request against `main` with a clear summary and test notes.

Accepted branch prefixes:

- `fix/` for bug fixes.
- `feat/` for new features.
- `docs/` for documentation updates.
- `chore/` for maintenance, dependency or workflow changes.

## Code Standards

- Follow the checks and conventions documented in the repository you are changing. For `dexterous-hand-sdk` these are listed in its `CONTRIBUTING.md`.
- Public functions, classes and methods should have docstrings and type hints.
- Public APIs should remain vendor-neutral unless the change is explicitly a vendor adapter.
- Hardware-facing code must fail safely, document assumptions and avoid silent limit bypasses.
- Examples should run in mock mode whenever possible so they are useful without hardware.

## Test Requirements

New code should include tests that run without physical hardware. For ROS 2 or hardware-related changes, include a mock-mode test, a manual verification checklist, or both.

## Commit Message Format

Use Conventional Commits:

```text
feat: add tripod grasp preset
fix: validate unknown joint names in mock driver
docs: expand UR integration checklist
chore: update CI Python matrix
```

Use `feat`, `fix`, `docs`, `test`, `refactor`, `build`, `ci` or `chore` as the type. Keep the subject concise and explain hardware or safety implications in the body when relevant.
