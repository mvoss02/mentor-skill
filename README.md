# mentor

A Claude Code skill: a principal-engineer mentor that teaches you a technology
by having you build it into your own real repo, milestone by milestone.

Not a tutorial generator, and not an examiner guarding the answer key. The
mentor audits your repo, spars with you to build a learning plan, teaches each
milestone's concepts properly (orientation, mental model, worked example, with
a project-grounded HTML page as the visual aid), coaches while YOU write every
line, and gates each milestone behind a hard review: working code, unaided
explanation, and a "what breaks first" answer. Transfer is checked later,
spaced. It never writes your project code.

## Install

```bash
git clone <this-repo>
cp -r mentor ~/.claude/skills/mentor
```

Then in any project: `/mentor` (it is slash-command only by design; a teaching
session should be deliberate).

Arguments: `/mentor drill|guide|explain` requests a mode change (applied at
session boundaries only), `/mentor status` shows plan progress, any other text
becomes context for the session.

## First run

`/mentor` in your repo with a goal in mind, e.g. "I want to learn
OpenTofu by putting this cluster under IaC". The intake interview builds
`PLAN.md` with you; nothing is taught until you approve the plan.

## State

Everything lives in `~/.claude/mentor/<repo-name>/`:

- `PLAN.md` — mission, milestones, decisions
- `JOURNAL.md` — session log, verdicts, gap lists
- `lessons/` — self-contained HTML lessons (offline, printable)
- `concepts/` — concept cards with an explicit learning stage
  (encountered → introduced → practiced → retrievable → transferable)

If `~/.claude` is a dotfiles repo, your learning state syncs across machines
for free.

## Integrations (all optional, all auto-detected)

- **Learning ledger**: if `~/.claude/memory/convention.md` exists (a global,
  topic-organized concept ledger), concept cards are written there instead of
  `concepts/`, so one spaced-repetition system covers everything you learn.
- **caveman plugin**: composes cleanly; the mentor is token-lean by design and
  caveman compresses the chrome further.
- **SessionStart hook** (opt-in): surface due reviews when you open a shell.
  Add to `~/.claude/settings.json` hooks:

  ```json
  {
    "hooks": {
      "SessionStart": [{
        "hooks": [{
          "type": "command",
          "command": "grep -rlE 'stage: (introduced|practiced|retrievable)' ~/.claude/mentor/*/concepts/ 2>/dev/null | head -3 | xargs -I{} echo 'Mentor: concept to review {}'"
        }]
      }]
    }
  }
  ```

## Philosophy

- Orient → teach → model → practice together → fade scaffolding → retrieve
  (spaced) → transfer. Teach first when background is missing; struggle is a
  tool, not the teaching.
- Learn by building something real; the repo improves as you do.
- Predictions before commands; wrong predictions are the best teachers.
- Questions calibrated to what was taught and demonstrated. A card existing
  never means the concept is known.
- Hard gates, honest journal, no social passes.
- Escalation ladder when stuck on something already taught: question → hint →
  direction → fragment. Rescue on the deliverable kills retention.
- Three modes, picked at intake: `drill` (strict ladder, no rescue),
  `guide` (ladder plus toy examples and a boilerplate carve-out, default),
  `explain` (direct code examples, soft gates). Mode changes happen at
  session start, never mid-struggle.
