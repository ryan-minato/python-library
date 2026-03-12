# Getting Started

This page covers the three main ways to start from this template and the first commands to run after you create your own repository.

## Option 1: Use GitHub's template flow

1. Open the repository on GitHub.
2. Click **Use this template**.
3. Create a new repository from it.

This is the fastest path, but GitHub may label the new repository as generated from the template.

## Option 2: Import the repository without the generated badge

If you do not want the generated-from marker:

1. Click the **+** menu in the top-right area of GitHub.
1. Choose **Import repository**.
1. Paste the source URL below into **The URL for your source repository**.

```text
https://github.com/zenless-lab/python-helloworld.git
```

1. Choose the destination owner and repository name.
1. Run the import.

## Option 3: Clone locally

```bash
git clone https://github.com/zenless-lab/python-helloworld.git your-library
cd your-library
```

If you want a clean Git history:

```bash
rm -rf .git
git init
git add .
git commit -m "Initial commit"
```

## First commands to run

Install dependencies and verify that the template works before changing anything.

```bash
uv sync
uv run pytest
uv run ruff check .
uv run ty check
uv run zensical build --clean
```

If you want a live preview while editing docs, run:

```bash
uv run zensical serve
```

## What to update first

Start with the parts that define public identity and import paths.

1. Rename the package directory under `src/`.
2. Update the `project` metadata in `pyproject.toml`.
3. Replace the sample code and tests.
4. Update the docs metadata in `zensical.toml`.
5. Rewrite the README for your real library.

## Suggested sequence

```text
Create repository
-> sync dependencies
-> rename package
-> update metadata
-> replace sample code
-> update zensical.toml and docs/
-> confirm CI workflows still match your release process
```
