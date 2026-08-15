# Phase: Lesson

Goal: teach the current milestone's concepts properly, grounded in the learner's repo, BEFORE they build. Chat is the teacher; the HTML page is the visual aid they revisit. Style contract: `references/lesson-style.md`.

## Steps (in order, all REQUIRED)

1. **Re-read the relevant repo files.** Real paths and resource names. A lesson that could have been written without the repo is a failed lesson.
2. **Check the ledger** for the milestone's concepts and their stages. Pick the teaching method per concept using `references/methods.md` (worked example first for true novices, struggle-first only with adjacent prior knowledge); record the pick and reason in the journal.
3. **Orient in chat first.** Before any page: the problem each concept exists to solve, framed as an engineering situation ("Postgres acknowledged the commit and lost power 5 ms later..."), the simplest mental model, why an engineer cares. Short. This is teaching, not a quiz: questions here are predictions from intuition only.
4. **Write the visual aid** to `STATE_DIR/lessons/NNNN-<slug>.html` (NNNN increments). Three layers in order:
   - **(a) Concept.** Anchor analogy, term, one worked example (toy domain or the repo's shape), the seam where it leaks. Diagrams and flows where they beat prose. One primary source.
   - **(b) This repo.** Map the concept onto real files: "in your repo, X at `path` is the thing that...".
   - **(c) Do it yourself.** Task spec for the deliverable: what to build, constraints, definition of done, prediction prompts to answer before running commands. No solution code for the deliverable. Doc links.
5. **Open it** (`open <file>` on macOS, `xdg-open` on Linux), then **return to chat**: 2 to 3 stage-appropriate prompts (predict, explain the model back, apply to the repo). Wrong answers get diagnosed and repaired, not "try again".
6. **Ledger and journal.** Concepts taught here become `introduced` (teaching explanation labeled as Claude's in "My model"); note lesson number and method picks in the journal. Mark milestone `lesson-done` in PLAN.md.

Session may end here; build can start immediately if the learner wants. Reading the page is not evidence; the build is where practice happens.
