# Method selection

Per concept, choose the teaching method deliberately and record the choice
plus one-line reason in the journal. The selector is the learner's prior
knowledge (ledger/concept cards), not habit.

## Menu

- **Struggle-first task** (productive failure): the learner attempts a scoped
  problem BEFORE the concept is explained; the consolidating explanation then
  contrasts their attempt with the canonical approach. Use when the learner
  actually holds adjacent prior knowledge (stage `practiced` or above on the
  neighbouring concepts, or demonstrated in the repo) and the target is
  conceptual understanding. A card merely existing is not prior knowledge.
  [Sinha & Kapur 2021, Rev. Ed. Research: meta-analysis, g = 0.36 for
  concept/transfer when problem-solving precedes instruction]
- **Worked walkthrough**: study an annotated example first (toy domain, never
  the milestone deliverable), then fade support toward independent work. Use
  for true novices or procedural mechanics. Fade it as expertise grows;
  guidance that helps novices hurts advanced learners.
  [Sweller & Cooper 1985; Kalyuga et al. 2003, "expertise reversal effect"]
- **Visual aid** (HTML lesson): diagrams, flows, one worked example, repo
  mapping, the DIY spec. Supports the chat teaching, never replaces it: chat
  owns orientation, teaching, questions, diagnosis, and exercises. Optional
  predict-then-reveal or quiz blocks are for revisiting later, not the
  primary interaction (`references/lesson-style.md`).
- **Prediction drill**: commit a prediction before every consequential
  command. Always on. Aim predictions at the concepts that matter; the boost
  lands on the pretested content specifically.
  [Kornell, Hays & Bjork 2009; Pan & Carpenter 2023 review]
- **Breakage lab**: break the system on purpose, predict, observe, explain.
  Use for failure-mode and reliability concepts.
- **Explain-back / rebuild**: unaided retrieval at gates, wrapups, and
  retrospectives. The single most robust effect in the literature.
  [Roediger & Karpicke 2006; Adesope et al. 2017 meta-analysis, g ≈ 0.5-0.6]

## Selection heuristic

1. Prior-knowledge check, stage-aware. Ask: does the learner hold a model
   the attempt can lean on, and is the problem surmountable with it?
   - Concept `encountered` or missing, or a prerequisite model absent →
     direct teaching / worked walkthrough first.
   - `introduced` → guided attempt (hints available) only if adjacent
     knowledge makes it surmountable; otherwise walkthrough.
   - `practiced` or above on the neighbours → struggle-first is on the table.
   Stage is evidence about prior knowledge; prior knowledge and difficulty
   are what actually decide, not the stage label and never card existence.
2. Target check: conceptual "why" → lean struggle-first (within rule 1).
   Procedural "how" → walkthrough, then fade.
3. Difficulty stays surmountable: two failed attempts in a row → drop one
   level of difficulty. A difficulty is only desirable if the learner can
   get through it. [Bjork 1994, desirable difficulties]
4. Teaching before practice is not "giving the answer". The harm in the
   literature comes from unrestricted answer access DURING practice on the
   deliverable (+48% practice, -17% unassisted exam); scaffolded hints erase
   it. [Bastani et al. 2025, PNAS; Kestin et al. 2025, Sci. Reports]. So:
   explain fully, show worked toy examples, then keep the deliverable's
   answers behind the ladder while the learner builds.
5. Calibrate questions to stage (see `~/.claude/docs/pedagogy/teaching.md`):
   prediction from intuition → core model → familiar case → basic failure
   mode → alternatives → nuance. Wrong answers are diagnosed (terminology /
   mechanism / prerequisite / boundary / order / layer / trivial detail) and
   the specific piece repaired, then one more small application.
