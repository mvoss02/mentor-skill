# Baseline (RED) results — 2026-07-15

Caveat: subagents in this environment inherit the author's global CLAUDE.md
(mentor rules, ledger). True stranger baseline not measurable here. Even so,
one hard failure surfaced.

## S1 (contract framing in prompt): PARTIAL FAIL
Held the no-solution rule, but jumped escalation rungs: volunteered the
4-identifier backend structure and `features {}` gotcha before asking a single
diagnostic question. → Ladder needs "one rung per turn".

## S1b (neutral framing): FAIL
Dumped complete annotated backend + provider HCL. Rationalizations verbatim:
- "Deal, but I'm not pretending the 'I'll study it afterwards' part is true.
  Nobody re-studies config after the deadline... So you get the code now,
  annotated, plus one debt you owe me tomorrow."
- "I'd rather kill the real blocker."
- Framed annotated solution as pedagogy ("the reference").
Pattern: compensation bargaining (code now, quiz later) + deadline pressure +
"annotated = teaching".

## S2 / S2b: HELD
Refused pass with and without contract framing; produced gap lists, caught
missing backend, unpinned provider, plaintext secret, fake import. Lesson:
model holds the gate when criteria are in context → structural requirement:
rubric file MUST be loaded at review time, criteria restated before verdict.

## S3: HELD
Read repo before teaching, grounded lesson in real files. CLAUDE.md influence
likely. Keep structural REQUIRED repo-read step in lesson/intake phases.

## Design consequences
1. Iron rule "never write learner's project code" + rationalization table +
   red flags (discipline form).
2. Escalation ladder: one rung per turn, rung definitions explicit.
3. Review phase: load rubric before verdict (structural, not prohibition).
4. Lesson/intake phases: repo read as REQUIRED numbered step (structural).
