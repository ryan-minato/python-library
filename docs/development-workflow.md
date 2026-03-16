# Development Workflow

This page describes the expected local workflow and repository conventions.

## Environment Setup

Install dependencies with:

```bash
uv sync
```

Install Git hooks with:

```bash
uv run pre-commit install
```

## Formatting and Linting

Use these commands as the primary local quality loop:

```bash
uv run ruff format
uv run ruff check --fix
```

`ruff format` handles formatting, while `ruff check --fix` applies auto-fixable lint rules.

## Type Checking

Run type checks with:

```bash
uv run ty check
```

The template is configured to check `src/` and `tests/`, while excluding `scripts/` and `notebooks/` by default.

## Testing

Run the test suite with:

```bash
uv run pytest
```

Pytest is the expected test framework for this template. New tests should follow pytest conventions and stay close to user-visible behavior.

## Documentation Style

For Python docstrings, prefer the Google Python style guide:

- Use Google-style docstrings for modules, classes, and functions when documentation is needed.
- Prefer concise, descriptive English in code comments and docstrings.
- Prefer double quotes over single quotes for strings unless a specific file or framework convention requires otherwise.

Reference: [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html)

## Commit Style

When creating Git commits, use Conventional Commits style:

- `feat: add project initialization guide`
- `fix: correct gitleaks email allowlist example`
- `docs: expand repository structure page`

Reference: [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

## AI-Assisted Development Guidance

This repository is intended to work well with coding agents, but agent output quality depends on accurate repository context.

If the repository changes substantially, update `AGENTS.md` so the documented structure and conventions continue to match the real codebase. Do not assume the file stays correct automatically.
