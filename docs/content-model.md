# Content Model

3D2Y islands are plain Markdown files with small frontmatter blocks. This keeps the repo easy to read now and easy to turn into a platform later.

## Location

Each island lives here:

```txt
islands/<slug>/island.md
```

## Frontmatter

```yaml
---
title: "Rubber Band Movement"
slug: "rubber-band-movement"
difficulty: "beginner"
skills:
  - player input
  - movement
requires: []
---
```

## Fields

- `title`: The human-readable island name.
- `slug`: The stable ID used for folders, URLs, and references.
- `difficulty`: One of `beginner`, `intermediate`, or `advanced`.
- `skills`: A short list of practical things the island teaches.
- `requires`: Island slugs that should be completed first.

## Required Sections

Each island should use these sections:

- `Mission`
- `Why This Matters`
- `You Will Learn`
- `Requirements`
- `Build Steps`
- `Captain's Log`
- `Stretch Goals`

## Global Sharing Rule

Sharing is part of the overall 3D2Y loop, so individual islands do not need their own share section.
