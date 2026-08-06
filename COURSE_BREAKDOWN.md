# Algebra, Trigonometry, and Data Analysis — Unit and Lesson Breakdown

A reader-facing map of the course: eight units, 59 lessons, the Virginia 2023 SOL codes each
lesson carries, and the current build state of the repository.

> Derived from `spec/algebra_trig_data_analysis.md`, which remains the single source of truth
> for course structure. If the two disagree, the spec wins — regenerate this file.

---

## The course at a glance

**ATDA** is a full-year bridge course from Algebra 2 to either Statistics or Precalculus. It
pulls content from four Virginia 2023 SOL courses:

| Strand | SOL source | Where it lands |
| --- | --- | --- |
| Algebra review | Algebra 2 (`A2.EO`, `A2.EI`, `A2.F`) | Units 1, 3 |
| Function analysis | AFDA (`AFDA.AF`) | Units 2, 3 |
| Probability & data | AFDA (`AFDA.DA`), Prob/Stat (`PS.P`), `A2.ST.3` | Units 4, 5, 6 |
| Trigonometry | Trigonometry (`T.TT`, `T.CT`, `T.GT`) | Units 7, 8 |

**Sequence:** Algebra (U1–U3) → Data Analysis (U4–U6) → Trigonometry (U7–U8). The course
finishes with trig as the precalculus send-off.

**Structural conventions**

- Every unit opens with **Lesson X.0**, a unit opener — hook scenario, prerequisite
  diagnostic, vocabulary preview, learning-target roadmap. No new content, no new codes.
- Every lesson ships nine components: cover, warm-up (+key), guided notes (+key), activity
  (+key), exit ticket (+key), homework (+key), and a slide deck.
- Every unit ships a unit cover pair, a practice test, and an actual test, each with a key.
- The TI-84 is assumed throughout; calculator output appears as pre-drawn figures to read,
  with keystrokes reserved for the activity.
- Students are never asked to sketch a graph on a blank page — always a pre-drawn, pre-scaled
  axis system to plot or complete on.

**Totals:** 8 units · 59 lessons (51 content + 8 openers) · 16 unit tests (8 practice, 8 actual)

---

## Unit summary

| # | Unit | Standards base | Lessons | Big idea |
| --- | --- | --- | --- | --- |
| 1 | Algebraic Expressions and Factoring | A2.EO.1–3, A2.EI.2/6 | 8 | Rebuild symbolic fluency: exponents, radicals, factoring, rational expressions |
| 2 | Functions, Transformations, and Graph Analysis | AFDA.AF.1–2 | 8 | Parent function + transformation as the spine; read every graph the same way |
| 3 | Exponential and Logarithmic Functions | AFDA.AF.1/2, A2.F.1/2 | 8 | Growth and decay, and the logarithm as the inverse that undoes it |
| 4 | Counting and Probability | AFDA.DA.3, A2.ST.3, PS.P.1 | 7 | Count the outcomes, then apply the probability rules |
| 5 | Random Variables and the Binomial Distribution | PS.P.2 | 6 | From events to variables: distributions with a mean and a spread |
| 6 | The Normal Distribution | AFDA.DA.4, PS.P.3 | 6 | The continuous capstone: area under a curve is probability |
| 7 | Right and Oblique Triangle Trigonometry | T.TT.1–2 | 8 | Measure the inaccessible with ratios and the two laws |
| 8 | Unit Circle Trigonometry | T.CT.1–2, T.GT.1 | 8 | Angles beyond the triangle; exact values without technology |

**Sequencing constraints** (do not reorder):

- Unit 1's factoring feeds 1.7 and Unit 2's quadratic work; the exponent rules of 1.1–1.2 are
  the algebra beneath Unit 3's logarithms.
- Unit 3 must follow Unit 2 — exponential graphs are analyzed with Unit 2's vocabulary.
- Units 4 → 5 → 6 are a strict chain. `PS.P.3a` (discrete vs. continuous) only lands after
  Unit 5 exists to contrast against.
- Units 7 → 8 are a pair: Unit 7's right-triangle ratios become Unit 8's reference triangles.

---

## Unit 1 — Algebraic Expressions and Factoring

*The review strand. Assume the Algebra 1/2 toolkit; raise it to fluency.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 1.0 | Unit Opener: Why Algebra Fluency Matters | — |
| 1.1 | Simplifying Algebraic Expressions and Exponent Rules | A2.EO.3a |
| 1.2 | Radicals and Rational Exponents | A2.EO.2a–c |
| 1.3 | Factoring: GCF and Grouping | A2.EO.3b |
| 1.4 | Factoring Trinomials | A2.EO.3b |
| 1.5 | Factoring Special Forms | A2.EO.3b, d |
| 1.6 | Solving Polynomial Equations by Factoring | A2.EI.2b, A2.EI.6a–b |
| 1.7 | Simplifying Rational Expressions | A2.EO.1a–b |

**Arc:** operations → radicals → three factoring lessons in increasing difficulty → factoring
put to work solving equations → factoring put to work simplifying rationals.

## Unit 2 — Functions, Transformations, and Graph Analysis

*The conceptual core. Every later function lesson borrows this vocabulary.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 2.0 | Unit Opener: Functions as Models | — |
| 2.1 | Function Fundamentals: Notation, Domain, and Range | AFDA.AF.2a, e |
| 2.2 | Parent Functions and Transformations | AFDA.AF.1a–b |
| 2.3 | Equations and Graphs in Both Directions | AFDA.AF.1d, f |
| 2.4 | Intercepts, Zeros, and Extrema | AFDA.AF.2b–d |
| 2.5 | End Behavior and Asymptotes | AFDA.AF.2f–g |
| 2.6 | Piecewise-Defined Functions | AFDA.AF.2 |
| 2.7 | Choosing and Comparing Models in Context | AFDA.AF.1c, e, g; AF.2h |

**Arc:** notation and domain → transformations → equation ↔ graph both directions → the four
characteristics lessons → synthesis by choosing a model for real data.

## Unit 3 — Exponential and Logarithmic Functions

*Genuinely new material. Lessons 3.4–3.6 are deliberate **bridge extensions** past the A2
codes — cite the nearest `A2.F` code and label them as such in the plan.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 3.0 | Unit Opener: Growth Stories | — |
| 3.1 | Exponential Growth and Decay | AFDA.AF.1, AF.2 |
| 3.2 | Graphs of Exponential Functions | AFDA.AF.2g, A2.F.2h |
| 3.3 | The Logarithm as an Inverse | A2.F.1a, A2.F.2i–j |
| 3.4 | Properties of Logarithms | A2.F.1 *(bridge ext.)* |
| 3.5 | Solving Exponential Equations | *(bridge ext.)* |
| 3.6 | Solving Logarithmic Equations | *(bridge ext.)* |
| 3.7 | Applications of Exponentials and Logarithms | AFDA.AF.1e |

**Arc:** the exponential family → its graph → invert it to get the log → log properties → two
equation-solving lessons → applications (compound interest, half-life, pH, decibels).

## Unit 4 — Counting and Probability

*Count first, then apply rules. Contexts come from science, business, and finance.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 4.0 | Unit Opener: Chance and Counting | — |
| 4.1 | The Fundamental Counting Principle | AFDA.DA.3c |
| 4.2 | Permutations and Combinations | AFDA.DA.3g–i, A2.ST.3 |
| 4.3 | Theoretical and Experimental Probability | AFDA.DA.3a, d |
| 4.4 | Probability Rules and Mutually Exclusive Events | AFDA.DA.3e–f, PS.P.1c |
| 4.5 | Conditional Probability and Independence | AFDA.DA.3b, PS.P.1d |
| 4.6 | Venn Diagrams and Probability Trees | AFDA.DA.3c–d, PS.P.1b |

**Arc:** counting techniques → what probability *is* → the rules (complement, addition) →
conditional and independence → the representation toolkit used to justify decisions.

## Unit 5 — Random Variables and the Binomial Distribution

*The shortest unit and the pivot of the statistics strand.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 5.0 | Unit Opener: From Events to Variables | — |
| 5.1 | Discrete Random Variables | PS.P.2a |
| 5.2 | Expected Value and Standard Deviation | PS.P.2b, g |
| 5.3 | The Binomial Setting | PS.P.2c–d |
| 5.4 | Binomial Probabilities on the TI-84 | PS.P.2e |
| 5.5 | Mean and Standard Deviation of a Binomial | PS.P.2f–g |

**Arc:** define the variable and its distribution table → summarize it with center and spread →
recognize the binomial conditions → compute with `binompdf`/`binomcdf` → the binomial's own
shortcut formulas, interpreted in context.

## Unit 6 — The Normal Distribution

*The continuous capstone of the data strand.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 6.0 | Unit Opener: The Bell Curve Everywhere | — |
| 6.1 | Density Curves and the Normal Model | AFDA.DA.4a–b, PS.P.3a |
| 6.2 | The Empirical Rule | AFDA.DA.4c, h; PS.P.3b |
| 6.3 | z-Scores and Comparing Distributions | AFDA.DA.4d–e, PS.P.3d–e |
| 6.4 | Normal Probabilities on the TI-84 | AFDA.DA.4f–g, PS.P.3f |
| 6.5 | Normal Distribution Applications | AFDA.DA.4, PS.P.3 |

**Arc:** discrete vs. continuous and when normal is reasonable → the Empirical Rule as the
rough tool → standardizing to compare across distributions → `normalcdf`/`invNorm` as the
precise tool → synthesis.

## Unit 7 — Right Triangle and Oblique Triangle Trigonometry

*Contexts: elevation, depression, navigation, surveying.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 7.0 | Unit Opener: Measuring the Inaccessible | — |
| 7.1 | The Six Trigonometric Ratios | T.TT.1a |
| 7.2 | Special Right Triangles | T.TT.1b |
| 7.3 | Solving Right Triangles: Elevation and Depression | T.TT.1c–d |
| 7.4 | The Law of Sines | T.TT.2a |
| 7.5 | The Ambiguous Case | T.TT.2b |
| 7.6 | The Law of Cosines | T.TT.2a |
| 7.7 | Area of Any Triangle | T.TT.2c |

**Arc:** the six ratios → exact values from the two special triangles → solve right triangles
in context → leave the right angle behind with the two laws (with the ambiguous case given its
own lesson) → area formula and applied triangulation.

## Unit 8 — Unit Circle Trigonometry

*Unit 7's reference triangles, rotated into the coordinate plane. Lesson 8.7 closes the course.*

| Lesson | Title | Standards |
| --- | --- | --- |
| 8.0 | Unit Opener: Angles Beyond the Triangle | — |
| 8.1 | Angles, Radians, and Coterminal Angles | T.CT.1a–d |
| 8.2 | Arc Length and Sector Area | T.CT.1i–j |
| 8.3 | Reference Triangles and Function Values | T.CT.1e, g |
| 8.4 | Finding the Other Five Function Values | T.CT.1f, h |
| 8.5 | The Unit Circle | T.CT.2a–b |
| 8.6 | Exact Values of Special Angles | T.CT.2c |
| 8.7 | Reading Sine and Cosine Graphs | T.GT.1 *(survey)* |

**Arc:** standard position and radian measure → the two radian applications → reference
triangles from a point, then from a value → the unit circle itself → exact values without
technology → a read-and-interpret survey of sinusoidal graphs (amplitude, period, midline)
using Unit 2's transformation language.

---

## Deliberate exclusions

The curriculum guide's topic list omits these, so the course does not cover them:

- Linear programming (`AFDA.AF.3`)
- Bivariate data and regression (`AFDA.DA.1`)
- Experimental design (`AFDA.DA.2`)
- Inverse trig graphs (`T.GT.2`)
- Trig identities and equations (`T.IE.1–3`)
- Full sinusoidal graphing — `T.GT.1` survives only as the read-only survey in Lesson 8.7

---

## Build state

Everything below is scaffolded on disk — all 59 lesson directories with their nine component
subdirectories, plus per-unit `tests/`, `test_keys/`, `sample_test/`, and `sample_test_key/`.

| Unit | Lessons authored | Unit cover | Tests |
| --- | --- | --- | --- |
| 1 | 8 / 8 ✅ | ✅ | ✅ practice + actual, both keyed |
| 2 | 8 / 8 ✅ | ✅ | ✅ practice + actual, both keyed |
| 3 | 0 / 8 — scaffolded | — | — |
| 4 | 0 / 7 — scaffolded | — | — |
| 5 | 0 / 6 — scaffolded | — | — |
| 6 | 0 / 6 — scaffolded | — | — |
| 7 | 0 / 8 — scaffolded | — | — |
| 8 | 0 / 8 — scaffolded | — | — |

**Authored: 16 / 59 lessons (27%).** Next in sequence is Unit 3, starting with Lesson 3.0.

Running build notes and next steps live in `spec/course_planning.md`.
