# Lesson style contract

The HTML lesson is a VISUAL TEACHING AID the learner inspects and revisits. Chat is the interactive tutor: orientation happens in chat before the page, questions and exercises happen in chat after it. Reading the page is not evidence of learning.

One self-contained HTML file per lesson. `STATE_DIR/lessons/NNNN-<slug>.html`.

## Content rules

- Three layers in order: (a) concept, (b) this repo, (c) do-it-yourself. See `phases/lesson.md`.
- Layer (a) opens with the problem the concept solves, then the model, then ONE worked example (toy domain or the repo's shape), then the seam. Diagrams, flows, and progressions wherever they beat prose. Worked examples are welcome; they are how a novice gets a model.
- Short: 15-20 minutes of reading. One tangible win. Depth comes from the build phase, not lesson length.
- Layer (b) MUST quote real paths, resource names, and short excerpts from the learner's repo. Test: could this lesson have been written without reading the repo? If yes, rewrite (b).
- Layer (c) contains no solution code for the deliverable. Constraints, definition of done, prediction prompts, doc links.
- Cite one primary source (official docs preferred), verified current via web search, linked prominently.
- End with: "Ask your mentor when anything is unclear" and links to prior lessons for interleaving.

## Interactivity (optional)

Predict-then-reveal blocks and short quizzes are allowed when they add something the chat cannot (e.g. an offline revisit). If used: plain inline `<script>`, no frameworks, no external requests, feedback per option, options of equal length, correct position varied, reveal disabled until a prediction is entered, readable when printed. They never replace the chat prompts in `phases/lesson.md` step 5.

## Visual rules

- Clean readable typography, generous whitespace, print-friendly. Think Tufte.
- Inline CSS only, no external assets; must render offline forever.
- Code excerpts in monospace blocks with the repo path as caption.
