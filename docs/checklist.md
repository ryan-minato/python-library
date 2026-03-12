# Rename Checklist

Use this page as a pre-release sweep after creating your repository from the template.

## Required replacements

- Replace `python-helloworld` with your distribution name.
- Replace `python_helloworld` with your import package name.
- Replace `Hello from python-helloworld!` with a real example or remove it.
- Replace `zenless-lab/python-helloworld` with your repository path.

## Files that usually need edits

| File | Why it matters |
| --- | --- |
| `pyproject.toml` | Package metadata, authors, dependencies, and tool config. |
| `zensical.toml` | Docs title, site URL, repository URL, theme, and navigation settings. |
| `README.md` | Public landing page for users and contributors. |
| `src/python_helloworld/__init__.py` | Placeholder implementation and package name. |
| `tests/test_example.py` | Placeholder test and import path. |
| `.github/workflows/docs.yml` | Confirm documentation deployment still matches your docs strategy. |

## Structural renames

Review these directory or package-level changes:

- Rename `src/python_helloworld/`.
- Update imports that still point to the old package name.
- Decide whether `scripts/` is needed.
- Decide whether `notebooks/` is needed.

## Content review

Before calling the project ready, verify that:

- the README describes the real library
- docs no longer speak about the repository as a template unless that is intentional
- the first example is valid and tested
- the package can be installed and imported with the final name
- repository links do not point back to the template

## Final verification commands

```bash
uv sync
uv run pytest
uv run ruff check .
uv run ty check
uv run zensical build --clean
```
