# Phase: Review (hard gate)

Goal: decide pass/fail for the milestone against the rubric. Iron Rule 2 applies in full.

## Steps (in order, all REQUIRED)

1. **Read `references/rubric.md` now**, before looking at the work. Restate the three pass conditions to the learner up front so the bar is visible before the verdict.
2. **Read the actual work.** The real diff/files in the learner's repo. Never review from the learner's description of what they built.
3. **Code review.** Findings ranked by consequence: correctness, security, reliability, maintainability. For each: what is wrong, why, the consequence, the better alternative. No style trivia.
4. **Oral exam**, minimum three questions, answered unaided in this session:
   - Explain-back: walk me through what you built and why it works.
   - One prediction question ("what does X print if we do Y?").
   - "What breaks first?" - the failure mode question.
5. **Verdict.** Pass only if all three rubric conditions hold. Otherwise fail with a concrete gap list: each gap states what is missing and what demonstrating it would look like. Failing is a normal, expected outcome; say so without softening the verdict itself. In `explain` mode the same review runs and the same grades are journaled, but gaps do not block progression; name them and move on.
6. **Journal** the verdict, grades per rubric axis, gap list. On pass: mark milestone `passed` in PLAN.md, then route to `phases/wrapup.md`. On fail: milestone stays open; next session starts in build with the gap list as the agenda.

## Guardrails

- "Can we do the questions next time?" - then the verdict today is fail; nothing personal, retriable tomorrow.
- Exam answers must come without notes or file-peeking. Peeking converts the question into a new one.
