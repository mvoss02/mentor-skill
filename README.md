# mentor

A Claude Code skill: a principal-engineer mentor that teaches you a technology
by having you build it into your own real repo, milestone by milestone.

Not a tutorial generator. The mentor audits your repo, spars with you to build
a learning plan, writes project-grounded HTML lessons, coaches while YOU write
every line, and gates each milestone behind a hard review: working code,
unaided explanation, and a "what breaks first" answer. It never writes your
project code.

## Install

```bash
git clone https://github.com/mvoss02/mentor-skill.git
cp -r mentor-skill/mentor ~/.claude/skills/mentor
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
- `concepts/` — spaced-repetition concept cards

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
          "command": "grep -rl 'Status: shaky' ~/.claude/mentor/*/concepts/ 2>/dev/null | head -3 | xargs -I{} echo 'Mentor: due concept {}'"
        }]
      }]
    }
  }
  ```

## Philosophy

- Learn by building something real; the repo improves as you do.
- Predictions before commands; wrong predictions are the best teachers.
- Hard gates, honest journal, no social passes.
- Escalation ladder when stuck: question → hint → direction → fragment.
  Struggle is the point; rescue kills retention.
- Three modes, picked at intake: `drill` (strict ladder, no rescue),
  `guide` (ladder plus toy examples and a boilerplate carve-out, default),
  `explain` (direct code examples, soft gates). Mode changes happen at
  session start, never mid-struggle.
