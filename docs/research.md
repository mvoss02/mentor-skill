# Evidence base

The mentor's design maps onto learning-science findings. Per claim: key
citations and the nuance that shaped the design.

## Retrieval practice (gates, sparring, ledger recall)
- Roediger & Karpicke 2006, *Psychological Science*: testing beat restudy at
  2-day and 1-week delays. https://journals.sagepub.com/doi/10.1111/j.1467-9280.2006.01693.x
- Adesope et al. 2017, *Rev. Ed. Research* meta-analysis (~272 studies),
  g ≈ 0.5-0.6. https://journals.sagepub.com/doi/abs/10.3102/0034654316689306
- Nuance: advantage shows at delays, not immediately; feedback amplifies.

## Spacing (ledger review intervals)
- Cepeda et al. 2006, *Psych. Bulletin*: 317 experiments; optimal gap grows
  with retention interval. https://augmentingcognition.com/assets/Cepeda2006.pdf
- Nuance: massed practice looks better immediately, which is why learners
  misjudge it. The ledger's expanding intervals implement this.

## Productive failure (struggle-first method)
- Sinha & Kapur 2021, *Rev. Ed. Research* meta-analysis (53 studies):
  problem-solving-then-instruction beats instruction-first, g = 0.36, gains
  in conceptual knowledge and transfer.
  https://journals.sagepub.com/doi/10.3102/00346543211019105
- Nuance: needs prior adjacent knowledge and consolidation afterwards.

## Worked examples + expertise reversal (novice entry, fading)
- Sweller & Cooper 1985, *Cognition and Instruction*: novices learn more from
  worked examples than problem solving.
- Kalyuga et al. 2003, *Educational Psychologist*: the same guidance that
  helps novices hurts advanced learners.
  https://www.tandfonline.com/doi/abs/10.1207/S15326985EP3801_4
- Design consequence: the ledger's status field selects struggle-first vs
  walkthrough-first per concept.

## Pretesting / generation (predict-then-reveal, prediction drills)
- Kornell, Hays & Bjork 2009, *JEP:LMC*: wrong guesses + feedback beat extra
  study. https://web.williams.edu/Psychology/Faculty/Kornell/Publications/Kornell.Hays.Bjork.2009.pdf
- Pan & Carpenter 2023, *Ed. Psych. Review*: review confirming the effect.
- Nuance (2025 meta): benefit lands on the pretested content itself
  (g = 0.66) not general absorption (g = 0.01) — aim predictions at the
  concepts that matter.

## Engagement hierarchy (build + oral exam over passive explanation)
- Chi & Wylie 2014, ICAP framework, *Educational Psychologist*.
- Nuance: strict interactive > constructive ordering doesn't always
  replicate (npj Sci. of Learning 2023); the robust part is
  constructive/interactive > active > passive, which is all this design needs.

## LLM tutoring: guardrails decide the sign of the effect
- Kestin et al. 2025, *Scientific Reports* (Harvard RCT, ~190 students):
  scaffolded GPT-4 tutor ≈ doubled learning gains vs active-learning class.
  https://www.nature.com/articles/s41598-025-97652-6
- Bastani et al. 2025, *PNAS* (field RCT, ~1,000 students): unrestricted
  ChatGPT access +48% on practice, **-17% on unassisted exams** vs no AI;
  a hint-only guardrailed tutor eliminated the harm.
  https://www.pnas.org/doi/10.1073/pnas.2422633122
- Design consequence: the escalation ladder and hard gates are not
  pedagogical taste; they are the difference between the two arms of the
  Bastani study.

## Tutoring effect size, honestly stated
- Bloom 1984 "2 sigma" is real but overstated: small studies, tutoring +
  mastery learning combined. Modern syntheses: human tutoring d ≈ 0.79
  (VanLehn 2011), large-scale tutoring RCTs ~0.3-0.4 SD (Nickow et al. 2020,
  NBER w27476). Tutoring is among the best-known interventions, not magic.

## Desirable difficulties (the umbrella)
- Bjork 1994; Bjork & Bjork 2011: conditions that slow apparent progress
  (spacing, testing, generation) raise long-term retention and transfer.
- Nuance: only difficulties the learner can overcome are desirable; hence
  the two-failures-drop-a-level rule in `references/methods.md`.
