# Contributing to Terract

> First of all — thank you. Every contribution, no matter how small, helps build something that has never been built before. We are glad you are here.

---

## Table of Contents

1. [Before You Start](#before-you-start)
2. [Ways to Contribute](#ways-to-contribute)
3. [Setting Up Your Environment](#setting-up-your-environment)
4. [Project Structure](#project-structure)
5. [Development Workflow](#development-workflow)
6. [Commit Guidelines](#commit-guidelines)
7. [Pull Request Process](#pull-request-process)
8. [Reporting Bugs](#reporting-bugs)
9. [Suggesting Features](#suggesting-features)
10. [Code Style & Standards](#code-style--standards)
11. [Testing](#testing)
12. [Documentation](#documentation)
13. [Community & Communication](#community--communication)
14. [Recognition](#recognition)

---

## Before You Start

Please read the following before contributing anything:

- Read our [Code of Conduct](./CODE_OF_CONDUCT.md) fully. It applies to all contributions and all community interactions.
- Terract is currently in early private development. Not all repositories are open yet. Watch this space — when we open up, this guide will tell you exactly where to start.
- If you are unsure whether your contribution is a good fit, open a discussion first. We would rather talk it through than have you spend hours on something we cannot merge.
- All contributors must agree to the Code of Conduct before any contribution is accepted.

---

## Ways to Contribute

You do not need to write code to contribute to Terract. There are many ways to help:

### Code Contributions
- Fix bugs reported in issues
- Implement features from the roadmap
- Improve performance of core packages
- Write or improve tests
- Build example apps that showcase Terract

### Documentation
- Fix typos, grammar, or unclear explanations
- Write missing documentation for features
- Improve the interactive docs app
- Translate documentation into other languages (future)

### Community
- Help others in Discord
- Answer questions in GitHub Discussions
- Review pull requests from other contributors
- Write blog posts or tutorials about Terract
- Share Terract with people who would benefit from it

### Design
- Improve the visual design of official Terract apps and docs
- Create component designs for the standard library
- Design assets for the community

### Bug Reports
- Report bugs with clear reproduction steps
- Verify existing bug reports
- Test fixes before they are merged

### Feature Suggestions
- Suggest features through the proper process
- Participate in feature discussions
- Help define and refine how features should work

---

## Setting Up Your Environment

> Note: Terract is not yet publicly available. This section describes the setup process for when the repositories open.

### Prerequisites

- Node.js v20 or later
- npm v10 or later
- Git
- A terminal you love — you are building for it after all

### Steps

**1. Fork the repository**

Go to the repository you want to contribute to and click Fork. This creates your own copy to work on.

**2. Clone your fork**

```bash
git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
cd REPO_NAME
```

**3. Add the upstream remote**

```bash
git remote add upstream https://github.com/terractjs/REPO_NAME.git
```

**4. Install dependencies**

```bash
npm install
```

**5. Verify your setup**

```bash
npm run build
npm test
```

If everything passes you are ready to contribute.

---

## Project Structure

Terract is organized as a monorepo. Here is how it is laid out:

```
terract/
├── packages/
│   ├── core/          → VTT, reconciler, hook runtime
│   ├── renderer/      → ANSI painter, terminal writer
│   ├── router/        → file-system router, screen stack
│   ├── layout/        → flex-like layout engine
│   ├── components/    → built-in component library
│   ├── bridge/        → inter-app communication, dev tunneling
│   ├── shield/        → permission system
│   └── cli/           → terract dev, build, start, create
├── examples/          → official example apps
├── docs/              → interactive terminal docs app
└── .github/           → org profile, templates, workflows
```

Each package is independent. When contributing, make sure you understand which package your change belongs to and keep your changes scoped to that package unless the change genuinely spans multiple.

---

## Development Workflow

### 1. Sync with upstream before starting

Always start from a clean, up-to-date base:

```bash
git checkout main
git pull upstream main
```

### 2. Create a branch

Branch names should be descriptive and follow this format:

```
type/short-description
```

Examples:
```
fix/input-cursor-overflow
feat/useAsync-hook
docs/shield-compliance-guide
chore/update-dependencies
```

Types: `feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `perf`

```bash
git checkout -b feat/your-feature-name
```

### 3. Make your changes

Keep changes focused. One branch, one purpose. If you find an unrelated bug while working, open a separate issue rather than fixing it in the same branch.

### 4. Test your changes

Run the full test suite before committing:

```bash
npm test
```

If you are adding a new feature, write tests for it. If you are fixing a bug, write a test that would have caught it.

### 5. Commit your changes

Follow the [Commit Guidelines](#commit-guidelines) below.

### 6. Push and open a pull request

```bash
git push origin feat/your-feature-name
```

Then open a pull request on GitHub following the [Pull Request Process](#pull-request-process).

---

## Commit Guidelines

Terract uses [Conventional Commits](https://www.conventionalcommits.org/). Every commit message must follow this format:

```
type(scope): short description

Optional longer description explaining why this change was made,
not just what was changed. Wrap at 72 characters.

Optional footer: references to issues, breaking changes, etc.
```

### Types

| Type | When to use |
|---|---|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only changes |
| `refactor` | Code change that is not a fix or feature |
| `perf` | Performance improvement |
| `test` | Adding or updating tests |
| `chore` | Build process, dependency updates, tooling |
| `revert` | Reverting a previous commit |

### Scope

The scope is the package or area of the codebase your change affects. Examples: `core`, `renderer`, `router`, `shield`, `cli`, `docs`, `components`.

### Examples

```
feat(router): add support for nested routes

fix(renderer): prevent cursor flicker on rapid state updates

docs(shield): add permission request examples to README

perf(reconciler): reduce cell-level diff iterations by 40%

chore: update typescript to 5.4
```

### Rules

- Use the imperative mood — "add feature" not "added feature"
- Do not capitalize the first letter of the description
- Do not end the description with a period
- Keep the subject line under 72 characters
- Reference relevant issues in the footer: `Closes #42`

---

## Pull Request Process

### Before Opening a PR

- Make sure your branch is up to date with upstream main
- Make sure all tests pass
- Make sure your code follows the style guidelines
- Make sure your commit messages follow the commit guidelines
- If your PR adds a new feature, make sure it is documented

### Opening the PR

Use the pull request template provided. Fill out every section. Do not leave sections blank. A PR with an incomplete description will be asked to update before review begins.

Your PR description must include:

- **What** — What does this PR change?
- **Why** — Why is this change needed?
- **How** — How was it implemented at a high level?
- **Testing** — How was it tested? What test cases cover it?
- **Screenshots or recordings** — If your change affects the terminal UI, include a recording or screenshot

### Review Process

- Every PR requires at least one approval from a Terract maintainer before merging
- PRs that touch core packages require two approvals
- Reviewers may request changes — respond to all feedback before re-requesting review
- Do not force-push to a PR branch after review has started unless asked to
- Once approved, a maintainer will merge your PR — do not merge your own PRs

### After Merging

Your contribution will be included in the next release. Your name will appear in the changelog and contributors list. Thank you.

---

## Reporting Bugs

Found a bug? We want to know. Please report it properly so we can fix it efficiently.

### Before Reporting

- Search existing issues to make sure it has not already been reported
- Make sure you are on the latest version of Terract
- Try to reproduce it in a minimal example

### How to Report

Open an issue using the **Bug Report** issue template. Include:

- **Description** — What happened? What did you expect to happen?
- **Steps to reproduce** — Exact steps to reproduce the bug. Be specific.
- **Minimal reproduction** — A minimal code example that demonstrates the bug
- **Environment** — Node version, OS, terminal emulator, Terract version
- **Logs** — Any error messages or logs from the terminal or log file
- **Screenshots or recordings** — If the bug is visual, show it

The more detail you provide the faster we can fix it.

### Security Vulnerabilities

Do not open a public issue for security vulnerabilities. Report them privately via email at security@terract.dev or via a private GitHub security advisory. We will respond within 48 hours and work with you on a responsible disclosure timeline.

---

## Suggesting Features

Have an idea? Great. Here is how to suggest it properly.

### Before Suggesting

- Check the roadmap to see if it is already planned
- Search existing issues and discussions to avoid duplicates
- Think about whether your idea fits the philosophy of Terract

### How to Suggest

Open a feature request using the **Feature Request** issue template. Include:

- **Problem** — What problem does this feature solve? Why does it matter?
- **Proposed solution** — How do you think it should work?
- **Alternatives considered** — What other approaches did you think about?
- **Additional context** — Examples, mockups, references to similar things in other tools

Feature requests are discussed openly. The community can comment and vote. The Terract team makes the final decision on what gets built and when.

---

## Code Style & Standards

Terract is written in TypeScript. All contributions must be in TypeScript.

### General Rules

- Write clean, readable code — optimize for clarity first, performance second
- Keep functions small and focused on a single responsibility
- Name things clearly — a longer descriptive name is better than a short cryptic one
- Avoid magic numbers — use named constants
- Do not leave commented-out code in PRs
- Do not leave debug logs or console statements in PRs

### TypeScript Rules

- Use strict TypeScript — `strict: true` in tsconfig
- No `any` types — if you think you need `any`, think again
- Prefer interfaces over type aliases for object shapes
- Export types alongside their implementations
- Document all public APIs with JSDoc comments

### Formatting

Terract uses Prettier for formatting and ESLint for linting. Both run automatically on commit via pre-commit hooks. Do not disable them.

To run manually:

```bash
npm run lint
npm run format
```

Your PR will not be merged if it fails linting or formatting checks.

---

## Testing

All code contributions must include tests. We use a custom testing setup built for terminal output verification.

### What to Test

- Every new feature must have unit tests covering its core behavior
- Every bug fix must have a regression test that would have caught the original bug
- Integration tests for features that span multiple packages
- Snapshot tests for component output

### Running Tests

```bash
# Run all tests
npm test

# Run tests for a specific package
npm test --workspace=packages/core

# Run tests in watch mode
npm run test:watch

# Run tests with coverage
npm run test:coverage
```

### Coverage

We aim for at least 80% test coverage on all packages. Coverage reports are generated automatically in CI. PRs that significantly reduce coverage will be asked to add more tests.

---

## Documentation

Good documentation is as important as good code. Terract's documentation lives in two places — the `docs` package which is the interactive terminal docs app, and inline JSDoc comments in the source code.

### Inline Documentation

All public APIs must have JSDoc comments explaining:

- What the function or component does
- What each parameter expects
- What it returns
- Any important behavior or edge cases
- A simple usage example where helpful

### Docs App

The interactive terminal docs app is built with Terract itself. To contribute to the docs app, follow the same workflow as code contributions. Documentation changes that fix typos or clarify existing content can be submitted as standalone PRs without needing a linked issue.

### Writing Style

- Write in plain, clear English
- Assume the reader is intelligent but may be new to Terract
- Use examples liberally — showing is better than telling
- Be concise — say what needs to be said and no more
- Use the second person — "you" not "the developer" or "the user"

---

## Community & Communication

### Discord

Our Discord server is the main place for real-time community interaction. Join us for:

- Getting help with Terract
- Discussing ideas and features
- Connecting with other contributors
- Announcements and updates

[Join the Terract Discord →](https://discord.gg/terract)

### GitHub Discussions

For longer, async conversations — architecture decisions, feature proposals, design discussions. These are searchable and permanent, making them better than Discord for things that need a record.

### Issues

For bugs, concrete feature requests, and tasks. Keep issues focused and on-topic.

### Response Times

We are a small team. We will do our best to respond to all issues, PRs, and questions within a reasonable time. Please be patient. If something has been waiting more than a week, a polite follow-up is welcome.

---

## Recognition

Every contributor matters. Here is how we recognize contributions:

- Your name appears in the changelog for every release that includes your contribution
- Significant contributors are listed in the `CONTRIBUTORS.md` file
- Trusted Developer Status in the Terract ecosystem for sustained contributors
- A special role in the Discord server for active contributors
- Verified developer status for those who build and publish packages in the ecosystem

---

<p align="center">
  <sub>Terract — Just a terminal framework. Built by the community, for the community.</sub>
</p>
