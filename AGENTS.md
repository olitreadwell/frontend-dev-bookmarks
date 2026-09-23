# Agent instructions

This repository is one person's curated list. The rules it follows live in the
engine at <https://github.com/olitreadwell/awesome-list-template>, and
`README.md` is the only source of truth for the entries the gate checks.

## Before you change anything

```bash
uv sync --group dev
make hooks-install
make check
```

## Rules

- Every entry is `- [Name](https://example.com/) - What it is.` with a capital
  and a closing period. This list does not use tags.
- Do not write entry text with a model. Every description here came from
  upstream, and rewording one is not a revival.
- Run `make toc` after moving a heading, and never hand-edit Contents lines.
- `awesome.toml` turns `github.stats` off. Every entry points at one of this
  list's own files, so a star count would be the same one number on all
  fifty-six lines. If an entry ever links a real repository, that decision needs
  revisiting.
- The category files under `appearance/`, `architecture/` and the rest are not
  checked. They hold several thousand links from 2015 and are the work left to
  do.

## Layout

- `README.md` is an index: one entry per category file.
- `tests/test_readme.py` holds the invariants for the index.
- `docs/revival.md` records what the engine changed and what it left alone.
