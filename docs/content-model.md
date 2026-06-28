# Content Model

3D2Y islands are plain Markdown files with small frontmatter blocks. This keeps the repo easy to read now and easy to turn into a platform later.

## Location

Each island lives here:

```txt
islands/<slug>/island.md
islands/<slug>/teach/*.html
```

`island.md` is the mission. `teach/` contains supportive HTML lessons and references for learners who want guidance before, during, or after the build.

## Frontmatter

```yaml
---
title: "Rubber Band Movement"
slug: "rubber-band-movement"
difficulty: "beginner"
godot_version: "4.7"
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
- `godot_version`: The exact Godot version the island targets.
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

## Teaching Files

Teaching files live inside each island:

```txt
islands/<slug>/teach/
```

Use teaching files for focused support material, not full walkthroughs. A good teaching file should explain one concept, give one tiny example, and help the learner return to the island.

Recommended names:

- `index.html`: Start here for the island's support material.
- `<concept>.html`: A focused lesson or reference.

Teaching files should be self-contained HTML so they can be opened directly in a browser and later rendered by a platform.

Teaching files should link to relevant high-quality sources, especially official Godot documentation for the island's `godot_version`.
