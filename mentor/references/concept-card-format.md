# Concept card format (fallback, used when no external ledger is detected)

One file per concept: `STATE_DIR/concepts/<concept-slug>.md`

```markdown
---
name: <concept-slug>
description: <one line>
status: shaky | solid
review: <YYYY-MM-DD>
topic: <topic>
---

# <Concept name>

**Recall log:** <append per recall: date, what came back clean, what was
missed, what to probe next>

Related: [[other-concept-slug]], [[not-yet-written-is-fine]]

## Core idea
<2-4 lines: the anchor analogy + the technical statement + the seam where
the abstraction leaks.>

## Recall question
<One question answerable without notes. This is what gets asked cold at the
start of a future session.>

## Exercise (optional)
<Small hands-on retrieval task.>
```

Frontmatter is the source of truth for status/review (machine-readable,
Obsidian-queryable). Wikilinks use basenames only; keep basenames unique.

Spaced repetition: first review ~3 days out, then ~1 week, ~3 weeks,
~2 months. Shaky recall resets the interval. `solid` still gets reviews;
it decays.
