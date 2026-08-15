# Phase: Review (hard gate)

Goal: decide pass/fail for the milestone against the rubric. Iron Rule 2 applies in full.

## Steps (in order, all REQUIRED)

1. **Read `references/rubric.md` now**, before looking at the work. Restate the three pass conditions so the bar is visible before the verdict.
2. **Read the actual work.** Real diff/files in the learner's repo. Never review from their description.
3. **Code review.** Findings ranked by consequence: correctness, security, reliability, maintainability. What is wrong, why, consequence, better alternative. No style trivia.
4. **Oral exam**, minimum three questions, unaided, in this session, calibrated to what was taught and demonstrated in this milestone (no questions about concepts merely encountered, no trivia about flags or API names):
   - Explain-back: walk me through what you built and why it works. Prefer reconstruction from the original problem over recitation of the lesson.
   - One prediction question ("what does X print if we do Y?").
   - "What breaks first?" and its consequence.
   A wrong answer is diagnosed (which piece is missing) before it is graded; a wrong answer caused by something never taught is a gap in the plan, not the learner, and is journaled as such.
5. **Verdict.** Pass only if all three rubric conditions hold. Otherwise fail with a concrete gap list: what is missing, what demonstrating it looks like. Failing is normal; say so without softening the verdict. `explain` mode: same review, same grades, gaps named, progression allowed.
6. **Ledger and journal.** Concepts demonstrated unaided here become `practiced` (same-session, so not `retrievable`; that needs a later cold recall). Set review dates. Record independence level for the milestone (0 to 4) in the journal and, if the milestone belongs to a chosen skill area, one line in `~/.claude/memory/independence.md`. Note a transfer scenario per major concept as its "Next useful step" so a later session can run it. On pass: mark `passed` in PLAN.md, route to `phases/wrapup.md`. On fail: milestone stays open; next session starts in build with the gap list as agenda.

## Guardrails

- "Can we do the questions next time?" → verdict today is fail; nothing personal, retriable tomorrow.
- Exam answers come without notes or file-peeking. Peeking converts the question into a new one.
- Do not escalate difficulty because the first answers were good; the gate tests the milestone's model, not the learner's ceiling.
