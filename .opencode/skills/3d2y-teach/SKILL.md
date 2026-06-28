---
name: 3d2y-teach
description: Use when creating or improving 3D2Y Godot learning content: islands, island.md files, teach/*.html support lessons, resources, and learning records.
---

# 3D2Y Teach

Use this skill when creating or improving learning material in this repository.

3D2Y is a Godot learning journey inspired by a timeskip training arc. Learners sail between islands, build small projects independently, reflect in a Captain's Log, and return to the crew with what they made.

## Teaching Workspace

Treat the repository as a public learning workspace, not a private tutoring notebook.

Core files:

- `README.md`: The project framing and entry point.
- `islands/<slug>/island.md`: The challenge mission for one mini-project.
- `islands/<slug>/teach/*.html`: Supportive teaching files for that island.
- `templates/island.md`: The reusable island template.
- `templates/teach-lesson.html`: The reusable HTML teaching template.
- `docs/content-model.md`: The platform-readable content model.
- `docs/teaching-model.md`: The teaching rules for this repo.
- `RESOURCES.md`: Curated trusted resources for Godot, game design, and community learning.
- `learning-records/*.md`: Optional records of durable teaching decisions or learner insights.
- `NOTES.md`: Optional scratchpad for project teaching preferences.

3D2Y content should usually live inside an island. Do not create private learner-specific lessons at the repo root unless explicitly asked.

## Philosophy

3D2Y teaches through finished mini-projects.

The island is the challenge. The `teach/` directory is support. The community is where learners gain wisdom by sharing what happened.

Every teaching decision should serve this loop:

1. Pick an island.
2. Build the smallest working version.
3. Reflect in the Captain's Log.
4. Share with the crew.
5. Sail to another island.

Prefer small, concrete, playable outcomes over broad explanations.

## Island Authoring

An island is not a full tutorial. It is a mission with enough structure to help a learner finish something.

Each island lives at:

```txt
islands/<slug>/island.md
```

Use this frontmatter only:

```yaml
---
title: "Island Title"
slug: "island-slug"
difficulty: "beginner"
godot_version: "4.7"
skills:
  - one practical skill
requires: []
---
```

Required sections:

- `Mission`
- `Why This Matters`
- `You Will Learn`
- `Requirements`
- `Build Steps`
- `Captain's Log`
- `Stretch Goals`

Rules:

- Keep the mission small enough to finish.
- Make requirements observable and testable.
- Set `godot_version` to the exact Godot version the island targets.
- Do not add a per-island share section. Sharing is global to 3D2Y.
- Do not number islands unless the user explicitly asks. Use slugs and `requires` for loose structure.
- Do not solve the entire island inside `island.md`.

## Teaching Files

Teaching files live at:

```txt
islands/<slug>/teach/*.html
```

Use them when an island needs supportive explanation, reference material, or debugging help.

A good teaching file:

- Teaches one thing only.
- Is self-contained HTML.
- Is short enough to revisit.
- Uses concrete Godot examples.
- Links to high-quality sources, especially official docs for the island's `godot_version`.
- Gives the learner one tiny practice prompt or check.
- Sends the learner back to the island.

Use `templates/teach-lesson.html` as the starting point.

Preferred teaching file names:

- `index.html`: The starting support page for an island.
- `<concept>.html`: A focused concept lesson.
- `<concept>-reference.html`: A compact reference sheet.
- `<problem>-debugging.html`: A common-mistakes guide.

## Difficulty Model

Difficulty is about what the learner has already built.

- `beginner`: Can open Godot, follow concrete steps, and run scenes.
- `intermediate`: Can combine multiple Godot concepts and debug simple behavior.
- `advanced`: Can design systems, polish interactions, and make tradeoffs.

If an island feels too large, split it into smaller islands instead of adding more explanation.

## Knowledge And Resources

Prefer trusted sources over memory when writing teaching material.

Use `RESOURCES.md` to record high-quality references, including:

- Official Godot docs.
- Godot demo projects.
- Well-maintained community tutorials.
- Game design references.
- High-signal communities.

Before writing teaching files, check `RESOURCES.md` for relevant sources. If it does not exist or lacks coverage for the topic, create or update it before writing claims that depend on external knowledge.

Teaching HTML should include a `Sources` section with links used for the lesson.

## Learning Records

Use `learning-records/*.md` sparingly.

Write a learning record when the project learns something durable, such as:

- A teaching pattern that works well for 3D2Y.
- A common learner misconception worth designing around.
- A content decision that affects future islands.
- A shift in the intended audience or difficulty model.

Do not use learning records as session logs.

## Community Wisdom

3D2Y should not pretend the repo is the whole learning experience.

When a learner needs judgment, feedback, or taste, route them toward community interaction:

- GitHub Discussions.
- Pull requests.
- Showcases.
- Playtesting threads.

Teaching files can prepare learners, but the crew gives feedback.

## Output Standard

When using this skill, leave the repo more useful than before.

Good outputs include:

- A new island with a clear mission.
- A shorter, sharper existing island.
- A focused `teach/*.html` support page.
- A reference page that compresses recurring knowledge.
- A curated resource entry with a useful annotation.
- Versioned source links in teaching HTML.

Avoid:

- Long course chapters.
- Abstract theory without a build task.
- Full solutions disguised as lessons.
- Platform features before the learning loop is proven.
