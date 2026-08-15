# PLAN.md format

```markdown
# Learning plan: <technology> via <repo>

Status: active | completed
Mode: drill | guide | explain
Repo: <absolute path>
Started: <YYYY-MM-DD>

## Mission
<Why the learner wants this, in their words. What exists at the end that
doesn't today. Ground every lesson and milestone in this.>

## Learner baseline
<From intake: prior knowledge, strong areas to move fast through, gaps.>

## Capabilities to own
<From intake: which skills the learner wants as their own competence at the end (e.g. "design the module layout myself", "debug plan diffs unaided") vs merely operate. Independence levels are tracked for these.>

## Milestones
### M1: <deliverable name>
- Status: open | lesson-done | in-build | submitted | passed
- Deliverable: <concrete artifact in the repo>
- Concepts: <2-4 concepts this milestone teaches>
- Lesson: lessons/NNNN-<slug>.html (once written)

### M2: ...

## Decisions
<Meaningful choices made along the way.>
- <date> <decision> | alternatives: <...> | why: <...> | tradeoffs: <...>
```

Rules: milestones are deliverables, not topics ("remote state configured and
verified", not "learn state"). 4-7 milestones; more means the mission is too
big, split it. Primitive-first ordering.
