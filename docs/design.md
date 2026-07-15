# Design: `mentor` — project-grounded teaching skill

Date: 2026-07-15
Status: approved (brainstorm session with Moritz)

## Problem

Existing teaching tools teach *topics* in isolation. The learner has a real repo (e.g. a working Kubernetes cluster with no IaC) and wants to learn a technology (e.g. Terraform/OpenTofu) *by improving that repo*. Nothing today builds a curriculum from a repo audit, teaches per-milestone, gates progression on demonstrated understanding, and tracks it all durably.

## Goal

A single publishable Claude Code skill: a principal-engineer mentor that

1. spars with the learner and audits their repo to co-author a learning plan,
2. per milestone: generates a project-grounded HTML lesson → learner builds → mentor reviews with a hard gate (code review + oral exam),
3. tracks concepts with spaced repetition, integrating with an existing learning ledger when one is present.

Success: "the feature works AND the learner understands why," enforced by gates, not vibes.

## Non-goals

- Not a code generator. Mentor never writes the learner's project code (escalation: question → hint → direction → solution).
- Not a plugin (no hooks/commands bundle) in v1. Optional hook snippet documented in README only.
- No dependency on the caveman plugin or any personal CLAUDE.md; those compose on top.

## Audience

Standalone-first. Works for a stranger with zero setup. Detects the author's personal setup (`~/.claude/memory/convention.md` ledger) and uses it as an enhancement.

## Shape

One skill, state-routed. Single entry point; SKILL.md is a thin router (~80 lines) that reads state and loads exactly one phase file (progressive disclosure, token-lean).

```
mentor/
  SKILL.md            # router: persona core + state detection
  phases/
    intake.md         # sparring + repo audit → PLAN.md
    lesson.md         # HTML lesson generation (3-layer)
    build.md          # learner implements; mentor coaches via escalation ladder
    review.md         # hard gate: code review + oral exam vs rubric
    wrapup.md         # ledger update, journal entry, next-session prep
  references/
    plan-format.md
    journal-format.md
    concept-card-format.md
    rubric.md
    lesson-style.md
  README.md           # install, publishing, optional hook snippet, ledger integration
```

## State

Global, per-project: `~/.claude/mentor/<project-slug>/`

- `PLAN.md` — mission (why the learner wants this), curriculum, milestones with status (`open | lesson-done | in-build | submitted | passed`), meaningful decisions (decision / alternatives / why / tradeoffs).
- `JOURNAL.md` — append-only session log: date, phase, what happened, grades, gap lists.
- `lessons/NNNN-<slug>.html` — project-grounded lessons.
- `concepts/` — concept cards (status, next-review, recall question) — **fallback only**. If `~/.claude/memory/convention.md` exists, cards are written there per that convention (topic dir, Status/Next-review/frontmatter, `index.md` updated) and `concepts/` is not used.

Rationale: `~/.claude` is commonly git-tracked/dotfile-synced; state survives machine moves; learner repos stay clean.

## Routing (SKILL.md)

On invoke, resolve project slug from cwd, then:

1. No `PLAN.md` → **intake**.
2. Milestone open, no lesson for it → **lesson**.
3. Lesson exists, work not submitted → **sparring first** (cold recall on lesson + predictions), then **build**.
4. Work submitted → **review**.
5. All milestones passed → retrospective + rebuild-from-scratch exercise.

The user can override the route explicitly (e.g. "review my work now").

## Phases

### intake
- Sparring interview: why this topic, current level, desired deliverable, time budget. One question at a time.
- Repo audit: read the actual repo (structure, tooling, gaps). Web-check current state of the target technology (versions, recommended practice) — never trust parametric knowledge for load-bearing claims.
- Output: co-authored `PLAN.md`; learner approves before anything else happens. Milestones are real deliverables in the repo, ordered primitive-first (show the raw thing before the abstraction).

### lesson
Generate one self-contained HTML lesson per milestone, three layers:
(a) the concept in general (anchor/analogy first, term second),
(b) how it maps to **this repo's actual files** (real paths, real snippets),
(c) DIY task spec: what to build, constraints, definition of done — no solution code.
Open in browser. Session may end here.

### build
Learner writes the code. Mentor coaches strictly via escalation ladder, asks for predictions before commands run (`what will tofu plan show?`), suggests controlled breakage experiments where safe.

### review (hard gate)
- Read the actual diff/files, never assume.
- Grade against `references/rubric.md`: correctness, understanding (unaided explain-back), tradeoffs, "what breaks first".
- Pass requires: working code AND unaided explanation AND failure-mode answer. No social passes.
- Fail → concrete gap list in JOURNAL.md, milestone stays open, redo.
- Pass → grade recorded, milestone closed.

### wrapup
- Create/update concept cards (ledger if detected, else local), set next-review dates (spaced repetition: ~3d, ~1w, ~3w, ~2mo; shaky recall resets).
- Journal entry. Surface fuzzy areas as next-session sparring seeds.

## Persona (in SKILL.md, applies to all phases)

Principal engineer who thoroughly enjoys teaching. Precise, concise, harsh when necessary, never cruel. Explains with anchor-before-abstraction, defines terms on first use, ends explanations with the "so what", shows where abstractions leak. Token-lean by default. Never writes the learner's project code.

## Integration seams (author's setup)

1. **Ledger detection**: `~/.claude/memory/convention.md` present → concept cards follow that convention; `index.md` updated at wrapup.
2. **Double-recall avoidance**: if a session-start hook already surfaced due concepts, mentor sparring absorbs those (same topic) into its recall round — quiz once, update ledger once.
3. **Caveman plugin**: composes; README notes it. No dependency.
4. **Personal CLAUDE.md mentor rules**: consistent with skill persona; reinforce, no conflict.

## Publishing

Repo `mentor-skill`, skill folder installable to `~/.claude/skills/mentor/` (or via plugin marketplace later). README covers install, first run, state locations, ledger convention (documented so strangers can adopt it), optional SessionStart hook snippet for auto-surfacing due milestones.

## Testing

- Dry-run intake on the real k8s repo (author's Terraform/OpenTofu mission) as first live use.
- Fresh-machine test: no ledger, no caveman → skill bootstraps local concepts/ and works.
- Router test: each state → correct phase file loaded, nothing else.
