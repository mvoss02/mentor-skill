# Concept card format (fallback, used when no external ledger is detected)

When `~/.claude/memory/convention.md` exists, follow it instead; this file mirrors its shape for standalone installs.

One file per concept: `STATE_DIR/concepts/<concept-slug>.md`

```markdown
---
name: <concept-slug>
description: <one line>
stage: encountered | introduced | practiced | retrievable | transferable
status: shaky | solid            # optional confidence within the stage
review: <YYYY-MM-DD>             # omit for encountered
topic: <topic>
independence: 0-4                # optional
---

# <Concept name>

**Why we encountered this:** the task, bug, incident, or question.

**My model:** the learner's own words when they have given them; if written by
the mentor, label it "(mentor's teaching explanation, not yet the learner's)".

**Core model:** 2-4 lines: anchor analogy + technical statement + the seam.

**What I currently misunderstand:** dated, specific, removed once repaired and re-shown.

**Evidence:** dated one-liners of what the learner actually did (predicted,
explained unaided, debugged, implemented with guidance, implemented alone,
transferred, missed X on cold recall).

**Next useful step:** one activity.

Related: [[other-concept-slug]], [[not-yet-written-is-fine]]
```

Stage rules: `encountered` is the default and writing the card never promotes.
`introduced` after real teaching; `practiced` after guided use; `retrievable`
after unaided cold recall in a later session; `transferable` after a spaced
transfer exercise. Missed recall drops a stage and shortens the interval.

Spaced repetition: ~3 days, ~1 week, ~3 weeks, ~2 months; reset on a miss.
`retrievable`/`transferable` still decay and still get reviews. Never quiz
`encountered`. Frontmatter is the source of truth; wikilinks use basenames.
