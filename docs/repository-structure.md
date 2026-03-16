# Repository Structure

This page describes the repository at a useful, module-level granularity.

## Top-Level Layout

```text
.
├── .agents/
├── .devcontainer/
├── .github/workflows/
├── docs/
├── notebooks/
├── scripts/
├── site/
├── src/python_helloworld/
├── tests/
├── .gitleaks.toml
├── .pre-commit-config.yaml
├── pyproject.toml
├── pyproject.template.toml
├── requirements.txt
├── uv.lock
└── zensical.toml
```

## Directory Roles

### `.agents/`

Agent-related resources live here. The current repository includes a placeholder `skills/` area. Treat this as the location for repository-specific agent guidance, not for runtime application code.

### `.github/workflows/`

The workflow directory currently contains five CI definitions:

- `docs.yml`
- `publish.yaml`
- `quality.yaml`
- `secret-scan.yaml`
- `test.yaml`

Together they cover documentation, publishing, quality gates, secret scanning, and tests.

### `docs/`

The source for the documentation site. The current directory contains markdown pages and `javascripts/mathjax.js` for MathJax setup.

### `notebooks/`

A placeholder area for notebooks. It is excluded from `ty` checks by the current template configuration.

### `scripts/`

A place for small project automation or repository utilities. It is also excluded from `ty` checks by default in the template.

### `site/`

Generated documentation output. This is build output rather than authoritative source.

### `src/python_helloworld/`

The example Python package included by the template. Right now it contains a tiny public module surface and `py.typed` to mark the package as typed.

### `tests/`

Pytest-based tests for the package. The current example test only exercises the placeholder `hello()` function.

## Key Configuration Files

- `.gitleaks.toml` defines strict secret and PII scanning behavior.
- `.pre-commit-config.yaml` defines local Git hook automation.
- `pyproject.toml` contains the active project metadata and tool configuration.
- `pyproject.template.toml` contains the template block intended to be appended after `uv init` in a new repository.
- `zensical.toml` defines the documentation site configuration.
- `uv.lock` and `requirements.txt` capture dependency state.

## Documentation Principle

Keep structural documentation concise and practical. Repository maps should help a human or an AI agent orient quickly. They should not duplicate every file unless a deeper breakdown is needed for a specific subsystem.
