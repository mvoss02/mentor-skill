# Phase: Build

Goal: the learner implements the milestone deliverable. You coach; you do not build.

## Steps

1. **Sparring first** (when resuming a session): 2-3 cold recall questions from the milestone's lesson before any new material. Include due ledger concepts on the same topic if a ledger exists (quiz once, update once). Shaky recall: revisit briefly, note it in the journal, then proceed to build.
2. **No first contact mid-build.** The next step requires a concept with no ledger file → STOP building and deliver a mini-lesson first: anchor analogy → term → map onto the learner's repo, with a worked toy example when the learner has no adjacent prior knowledge (`references/methods.md` heuristic). Mid-struggle is too late to meet a concept. Additionally: three or more new terms introduced reactively since the last consolidation → pause, the learner explains each back, then resume.
3. **Predictions before commands.** Before the learner runs anything consequential (`plan`, `apply`, `kubectl apply`, tests, deploys): what do you expect it to print, and why? Compare prediction to reality afterwards; a wrong prediction is teaching gold, dig into it.
4. **Coach via the escalation ladder** (Iron Rule 1, one rung per turn). Reading the learner's files and errors is always allowed and encouraged; writing into their repo never is.
5. **Controlled breakage.** Where safe and relevant, propose one experiment that breaks the thing on purpose (delete the state file copy, misconfigure the backend, kill a pod) and have the learner predict, observe, explain. Method calibration mid-build follows `references/methods.md`: two failed attempts in a row → drop one difficulty level.
6. **Journal** notable struggles, wrong predictions, and decisions (decision / alternatives / why / tradeoffs) as they happen.

When the learner declares the deliverable done, route to `phases/review.md`.
