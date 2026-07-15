# Lesson style contract

One self-contained HTML file per lesson. `STATE_DIR/lessons/NNNN-<slug>.html`.

## Content rules

- Three layers in order: (a) concept, (b) this repo, (c) do-it-yourself.
  See `phases/lesson.md` for what each layer must contain.
- Short: completable in 15-20 minutes of reading. One tangible win. Working
  memory is small; depth comes from the build phase, not from lesson length.
- Layer (b) MUST quote real paths, resource names, and short excerpts from the
  learner's repo. Test: could this lesson have been written without reading
  the repo? If yes, rewrite layer (b).
- Layer (c) contains no solution code. Constraints, definition of done,
  prediction prompts, doc links.
- Cite one primary source (official docs preferred), verified current via web
  search, linked prominently.
- End with: "Ask your mentor when anything is unclear" and links to prior
  lessons for spaced interleaving.
- Optional short quiz: answer options of equal length, no formatting tells.

## Visual rules

- Clean readable typography, generous whitespace, print-friendly. Think Tufte.
- Inline CSS only, no external assets; the file must render offline forever.
- Code excerpts in monospace blocks with the repo path as caption.
