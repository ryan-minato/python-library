# Customization Guide

The template is intentionally small, but there are still a few areas that deserve deliberate edits instead of blind search-and-replace.

## Package identity

Update the package metadata in `pyproject.toml`:

- `name`
- `description`
- `authors`
- `requires-python`

These values affect packaging, installation metadata, and the generated project description shown by tooling.

## Import path and module directory

Rename the module directory:

```text
src/python_helloworld/
```

to your real import name, for example:

```text
src/acme_tools/
```

After that, update imports in tests and any example code.

## Example implementation

The template ships with a placeholder function and a placeholder test. Replace them early so your checks validate real behavior.

Typical places to update:

- `src/<your_package>/__init__.py`
- `tests/test_example.py`

## Documentation metadata

Update these values in `zensical.toml` before publishing docs:

- `site_name`
- `site_description`
- `site_author`
- `site_url`
- `copyright`
- `repo_name`
- `repo_url`

If these remain unchanged, your docs will point to the template repository instead of your project.

## Optional folders

The template includes optional folders for common workflows.

### `scripts/`

Keep it if you maintain utility scripts such as release helpers, data migrations, or maintenance commands.

### `notebooks/`

Keep it if your project needs experiments, demos, or research notebooks.

If you do not need either folder, remove it and simplify the related configuration in `pyproject.toml`.

## Tooling policy

The lint and type-check setup is intentionally strict enough to be useful without being exhausting.

You may want to customize:

- Ruff rules in `tool.ruff.lint`
- per-file ignores for tests or scripts
- the `tool.ty.src` include and exclude lists

Change these only after the package layout is stable, otherwise you may end up tuning rules against temporary files.

## Workflow files

The repository already includes GitHub Actions workflows for docs, linting, tests, publishing, type checking, and secret scanning.

Review these files before your first release:

- `.github/workflows/docs.yml`
- `.github/workflows/lint.yml`
- `.github/workflows/test.yml`
- `.github/workflows/typecheck.yml`
- `.github/workflows/publish.yml`

In particular, `docs.yml` installs `zensical` and builds the site into `site/`, so any change to your docs toolchain should be reflected there as well.

## Release readiness

Before publishing to PyPI or another internal index, make sure you have reviewed:

- project name uniqueness
- versioning policy
- license compatibility
- Python version support
- installation instructions
- changelog or release notes strategy
