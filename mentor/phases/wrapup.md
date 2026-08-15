# Phase: Wrapup

Goal: persist what was actually learned (not what was written); prime the next session.

## Steps (in order, all REQUIRED)

1. **Concept cards.** For each concept touched this session:
   - Ledger present (`~/.claude/memory/convention.md`): create/update the file per that convention. Stage by evidence: taught today → `introduced`; used with guidance → `practiced`; cold-recalled unaided in a LATER session → `retrievable`; transferred → `transferable`. Add dated Evidence lines. Update the index line.
   - No ledger: `STATE_DIR/concepts/<concept>.md` per `references/concept-card-format.md`.
   - Never promote because the notes are good. Never write a card that knows more than the learner and label it as theirs; Claude's explanation is labeled as Claude's.
2. **Learner-authored summary** (periodically, for concepts at `practiced` or above with some spacing): ask the learner to write the concept in their own words from memory. Compare with the canonical model in chat: retained / distorted / omitted / nuance that can wait. Their version becomes "My model" on the card.
3. **Wrap questions**, briefly: what did you learn, what is still unclear, what would you struggle to rebuild tomorrow, what surprised you. Unclear/struggle answers become next session's sparring seeds.
4. **Independence.** One line: which parts of today's work the learner did that Claude used to do (framing, locating, hypothesis, decomposition, implementation). Level 0 to 4 for the milestone in the journal; notable shifts in `~/.claude/memory/independence.md`. Say what scaffolding will fade next time.
5. **Journal** per `references/journal-format.md`.
6. **Next step**, one line: which milestone, which phase, what the learner could do solo before then.

## All milestones passed?

Run the retrospective instead of step 6:
- Rebuild exercise: learner re-derives the architecture from scratch, verbally: components, data flow, tradeoffs, what they would change.
- Transfer: one meaningfully different scenario using the plan's core concepts, minimal framing. Result feeds the ledger (`transferable` only if passed).
- Review the mission: achieved? Natural next mission?
- Close the plan (status: completed) and name soberly the two or three hardest things they now own.
