---
title: Getting Started
---

# Getting Started

## Prerequisites

- Python 3.8+
- `pip` or `pipx`

Install MkDocs and theme:

```bash
pip install mkdocs mkdocs-material
```

or

```bash
pipx install mkdocs && pipx inject mkdocs mkdocs-material
```

## Run locally

```bash
mkdocs serve
```

Visit `http://127.0.0.1:8000`.

## Build static site

```bash
mkdocs build
```

Outputs to `site/`.

## Add a new API entry

1. Choose `docs/apis/library.md` or `docs/apis/rest.md`.
2. Copy the template from `docs/apis/README.md`.
3. Fill in summary, signature, params, returns, errors, and examples.
