# Phase: Intake

Goal: co-author PLAN.md. No teaching, no lessons yet.

## Steps (in order, all REQUIRED)

1. **Sparring interview.** One question at a time, wait for each answer:
   - Why this technology? What should exist at the end that doesn't today?
   - Current level: what have they already used or read? Probe one answer with a follow-up to calibrate depth honestly.
   - Time budget per week, target horizon.
   - Which capabilities they want to OWN at the end (framing, navigation, design, debugging, implementation) vs merely operate. These become the independence-tracked areas.
   - Mode: `drill` (strict ladder while building), `guide` (ladder plus toy examples and a boilerplate carve-out, default), or `explain` (direct code examples, soft gates). All three teach fully first; they differ in rescue during the build. One line each; record the choice in PLAN.md.
2. **Repo audit.** Read the repo before proposing anything: structure, README(s), tooling already present, what is manual today. Note 3-5 concrete artifacts (file paths, resource names) the curriculum can anchor to.
3. **Research sweep.** Name the topic explicitly with the learner ("Learn Terraform deployments on Azure"), then survey it properly via web search:
   - the official docs' own learning path / getting-started sequence,
   - 2-3 community curricula or roadmaps for the same topic (how do experienced people order it?),
   - current state: latest stable version, recommended practice, deprecations.
   Synthesize into a topic map: the concepts this topic is made of, in the order the field teaches them. Cite the primary source plus the best curriculum found.
4. **Map topics to mission.** Cross the topic map with the mission and repo audit: keep what serves the mission, cut the rest explicitly (note cuts in the plan so they're a decision, not an oversight). Milestones come from this intersection.
5. **Ledger check.** If `~/.claude/memory/convention.md` exists, read the ledger index for this topic. `retrievable`/`transferable` → skip or compress; `introduced`/`practiced` → plan a short refresh, not a re-teach; `encountered` → treat as new ground.
6. **Draft PLAN.md** per `references/plan-format.md`: mission, milestone list. Milestones are real deliverables in the learner's repo, ordered primitive-first (raw mechanism before the abstraction that hides it). Each milestone names its concepts and its deliverable.
7. **Learner approves the plan.** Present it, invite pushback, revise. No milestone starts until they approve.
8. **Journal** the session per `references/journal-format.md`.

## Guardrails

- Interview before audit conclusions: do not prescribe a curriculum the mission doesn't need (YAGNI applies to learning plans too).
- Milestone 1 must be completable in one or two sessions. Early wins compound.
