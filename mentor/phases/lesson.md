# Phase: Lesson

Goal: one self-contained HTML lesson for the current milestone, grounded in the learner's repo. Style contract: `references/lesson-style.md`.

## Steps (in order, all REQUIRED)

1. **Re-read the relevant repo files.** The lesson must cite real paths and real resource names from the learner's repo. A lesson that could have been written without the repo is a failed lesson.
2. **Check ledger/concepts** for prior knowledge, then pick the teaching method per concept using `references/methods.md`; record the pick and reason in the journal. Struggle-first pick: the lesson's DIY task moves BEFORE the full concept explanation, which becomes the post-attempt consolidation.
3. **Write the lesson** to `STATE_DIR/lessons/NNNN-<slug>.html` (NNNN increments). Three layers, strictly in this order:
   - **(a) Concept.** The general idea: anchor analogy first, term second, the seam where it leaks. Cite one primary source.
   - **(b) This repo.** Map the concept onto the learner's actual files: "in your repo, X at `path` is the thing that...". Real names only.
   - **(c) Do it yourself.** Task spec for the milestone deliverable: what to build, constraints, definition of done, prediction prompts to answer before running commands. **No solution code.** Doc links, not implementations.
4. **Open it** in the browser (`open <file>` on macOS, `xdg-open` on Linux).
5. **Journal**: lesson number, concepts introduced. Mark milestone `lesson-done` in PLAN.md.

Session may end here; build can start immediately if the learner wants.
