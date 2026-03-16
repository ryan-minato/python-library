# Python HelloWorld Template

This documentation set explains how the template is structured, how to reuse it safely, and what conventions are already encoded in the repository.

## Documentation Map

- [Getting Started](getting-started.md)
- [Repository Structure](repository-structure.md)
- [Development Workflow](development-workflow.md)

## What This Template Optimizes For

This repository is intentionally opinionated. It favors:

- Fast local setup with `uv`
- A single, consistent formatting and linting path with `ruff`
- A dedicated type-checking step with `ty`
- A familiar and flexible testing stack based on `pytest`
- Documentation that can be versioned and published through `zensical`
- Repository metadata that helps AI coding agents operate with better context

## Current Repository Components

The current repository includes these top-level areas:

- `.agents/` for agent-related resources
- `.github/workflows/` for CI automation
- `docs/` for the documentation source
- `notebooks/` as a notebook workspace placeholder
- `scripts/` for utility scripts
- `site/` for generated documentation output
- `src/python_helloworld/` for the example Python package
- `tests/` for the pytest suite

Configuration files such as `.gitleaks.toml`, `.pre-commit-config.yaml`, `pyproject.toml`, `pyproject.template.toml`, `uv.lock`, and `zensical.toml` complete the development and publishing setup.

## Why the Template Works This Way

The template is optimized for the first hour of a new project. It gives you enough structure to start immediately, while keeping the example code deliberately small so it can be replaced quickly after project creation.

It is also built for AI-assisted programming. The goal is not to automate thought, but to reduce ambiguity. The clearer the repository structure and conventions are, the more reliably a coding agent can make correct changes.

## Next Step

Start with [Getting Started](getting-started.md) if you are creating a new repository from this template.
