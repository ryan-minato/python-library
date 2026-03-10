# Python Library Template

> Start with a clean Python library scaffold, then replace the template pieces before your first release.

This template is designed for developers who want a practical baseline instead of an empty repository. It gives you a modern Python project layout with packaging, tests, linting, type checking, and documentation already wired together.

The current repository still ships with a deliberately tiny placeholder API so the template is runnable immediately:

```python
from python_library import hello

assert hello() == "Hello from python-library!"
```

## What is included?

### Project foundations

- `src/` package layout
- `pyproject.toml` with build metadata
- `uv` dependency management

### Quality tooling

- `pytest` for tests
- `ruff` for linting and formatting
- `ty` for static type checking
- `pre-commit` support

### Documentation and automation

- Zensical documentation setup via `zensical.toml`
- GitHub Actions–ready structure (add your own docs deployment workflow)
- A docs structure you can expand instead of rebuilding later

## Choose your starting path

### Use GitHub template

Click **Use this template** on GitHub if the default template flow works for you.

### Import the repository

Use GitHub's **Import repository** flow if you do not want the generated-from badge. The source URL is:

```text
https://github.com/zenless-lab/python-library.git
```

### Clone with Git

```bash
git clone https://github.com/zenless-lab/python-library.git your-library
cd your-library
```

## Quick setup

```bash
uv sync
uv run pytest
uv run ruff check .
uv run ty check
uv run zensical serve
```

To generate the static site output into `site/`:

```bash
uv run zensical build --clean
```

## Before you ship anything

You should update at least these parts:

- package metadata in `pyproject.toml`
- the module directory under `src/`
- the example implementation and tests
- documentation metadata and repository links in `zensical.toml`
- README title, install instructions, and examples

## Read next

- Go to the **Getting Started** page for setup options.
- Use the **Customization Guide** when adapting the template.
- Use the **Rename Checklist** before publishing the first version.
