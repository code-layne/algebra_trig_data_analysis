# Algebra, Trigonometry, and Data Analysis — Course Spec

The course design notes and the **course map**. Structure (units and lessons) comes from this
file; the mathematical **content** comes from the Virginia Standards of Learning documents in
`spec/`. This is the single source of truth for what the course covers and in what order.

## Course identity

**Algebra, Trigonometry, and Data Analysis (ATDA)** is a full-year secondary **bridge course
from Algebra 2 to either Statistics or Precalculus**. From the curriculum guide:

> This course builds on the concepts begun in Algebra 2, providing the opportunity to review
> key skills and learn others as a bridge course to precalculus or a statistics course.
> Algebraic skills to be covered will include factoring polynomials, simplifying algebraic
> expressions, and the basics of exponential and logarithmic functions. In addition to the
> algebra content, trigonometric skills, and data analysis will be surveyed. The topics of
> trigonometry will include special right triangle trigonometry, unit circle trigonometry,
> and oblique triangle trigonometry. Data analysis skills will consist of counting
> principles, probability rules, random variables, the binomial distribution, and the normal
> distribution. Students are required to have a TI-84 Plus or TI-84 graphing calculator.

The course draws its content from four Virginia 2023 SOL courses:

- **Algebra, Functions, and Data Analysis (AFDA)** — the conceptual core: function families
  via transformations, graph analysis, probability, and the normal distribution.
- **Algebra 2 (A2)** — the review strand: simplifying expressions, radicals and rational
  exponents, factoring polynomials, rational expressions, and the exponential/logarithmic
  function families (A2 is where logarithms carry SOL codes).
- **Probability and Statistics (PS)** — the statistics bridge: probability rules, discrete
  random variables, and the binomial distribution.
- **Trigonometry (T)** — the precalculus bridge: right-triangle, oblique-triangle, and
  unit-circle trigonometry, closing with a survey of sinusoidal graphs.

**Audience**: students who have completed Algebra 2. This is a *review-and-extend* course —
most topics are re-introductions at a more fluent level, plus genuinely new material
(logarithms, random variables, all of trigonometry). Scaffold generously, but assume the
Algebra 1/2 toolkit: solving linear and quadratic equations, function notation, graphing.

**Teaching posture**, carried over from the SOL prefaces:

- **Context is the default, not the garnish.** Data comes from science, business, and finance;
  trigonometry problems involve elevation, depression, navigation, and periodic phenomena.
  Author from a scenario, then extract the mathematics.
- **Transformational graphing is the spine of the function work.** Parent function first, then
  the transformation, in both directions.
- **Technology is assumed — the TI-84 specifically.** The course requires a TI-84 Plus.
  Show calculator output as a **pre-made figure** to read, and reserve student keystrokes for
  the activity. Every distribution computation (binompdf/cdf, normalcdf, invNorm) gets an
  explicit TI-84 treatment.
- **Communicate.** Every component should ask "what does this mean in context, and how do
  you know?"

## Where the content lives

| File | What it is |
| --- | --- |
| `spec/11AFDA2023ApprovedMathSOL.pdf` | The AFDA standards — standards text and Knowledge & Skills bullets |
| `spec/12AFDAUnderstanding the Standards.pdf` | VDOE's AFDA clarifications: scope limits, notation. **Read the relevant pages before authoring an AFDA-based lesson** |
| `spec/12Alg22023ApprovedMathSOL.pdf` | The Algebra 2 standards — source of codes for Units 1 and 3 (A2.EO, A2.EI, A2.F) |
| `spec/13Trig2023ApprovedMathSOL.pdf` | The Trigonometry standards |
| `spec/13TrigUnderstanding the Standards.pdf` | VDOE's Trigonometry clarifications. Same rule — read before authoring |
| `spec/15ProbStat2023ApprovedMathSOL.pdf` | The Probability & Statistics standards — source of codes for Units 4–6 (PS.P) |
| `spec/15ProbStatUnderstanding the Standards.pdf` | VDOE's Prob/Stat clarifications. Same rule — read before authoring Units 5–6 |
| `spec/course_planning.md` | The running handoff log (build state + next steps). Maintained by the lesson-planning skill |

The "Understanding the Standards" documents are where the *grain* lives — they say how far a
standard goes and what is out of scope. The "Approved SOL" PDFs give the standard text and its
lettered Knowledge & Skills; those letters are the codes a lesson cites (e.g. `AFDA.AF.1c`,
`A2.EO.3b`, `PS.P.2e`, `T.CT.2a`).

**Content deliberately excluded** (the curriculum guide's topic list omits it): linear
programming (AFDA.AF.3), bivariate data and regression (AFDA.DA.1), experimental design
(AFDA.DA.2), inverse trig graphs (T.GT.2), and trig identities and equations (T.IE.1–3).
Sinusoidal graphs (T.GT.1) survive only as a one-lesson survey closing the course.

## The standards in play

### Algebra 2 — the review strand (Units 1, 3)

| Standard | The student will… |
| --- | --- |
| **A2.EO.1** | Perform operations on and simplify rational expressions. (a) add/subtract/multiply/divide and simplify; (b) equivalent forms with monomial and binomial factors (linear and quadratic only); (c) simplify complex fractions; (d) demonstrate equivalence of forms |
| **A2.EO.2** | Perform operations on and simplify radical expressions. (a) simplify with numeric and algebraic radicands; (b) add/subtract/multiply/divide, incl. rationalizing denominators; (c) convert between radicals and rational exponents |
| **A2.EO.3** | Perform operations on and factor polynomial expressions. (a) sums/differences/products of polynomials; (b) factor completely (≤ 4 terms, integers); (c) polynomial quotients by monomial/binomial/trinomial divisors; (d) verify polynomial identities — difference of squares, sum/difference of cubes, perfect square trinomials |
| **A2.EI.2** | Solve quadratic equations over the complex numbers *(used here only for real solutions by factoring)* |
| **A2.EI.6** | Solve polynomial equations. (a) factored form from zeros/intercepts; (b) number and type of solutions; (d) verify and interpret in context |
| **A2.F.1** | Investigate and compare square root, cube root, rational, **exponential, and logarithmic** function families via transformations. (a) parent graphs; (b) equation from graph; (c) graph from equation; (e) compare across representations |
| **A2.F.2** | Characteristics of functions incl. **exponential, logarithmic**, piecewise. (a) domain/range/zeros/intercepts; (b) compare families; (c) increasing/decreasing; (g) end behavior; (h) asymptotes (exponential, logarithmic); (i–j) inverses |

*Scope note:* log **properties** and solving exponential/logarithmic **equations** exceed the
A2 codes — they are the course's deliberate precalculus-bridge extension; cite the nearest
A2.F code and label the lesson "bridge extension" in the plan.

### AFDA — the conceptual core (Units 2, 3, 4, 6)

| Standard | The student will… |
| --- | --- |
| **AFDA.AF.1** | Investigate, analyze, and compare linear, quadratic, and exponential function families, algebraically and graphically, using transformations. (a) parent functions; (b) describe the transformation; (c) determine which family best models a representation; (d) write the equation from a graph via transformations; (e) use a graphical or algebraic representation to solve problems in context; (f) graph from an equation via transformations, verify with technology; (g) compare families across multiple representations |
| **AFDA.AF.2** | Investigate and analyze characteristics of the graphs of linear, quadratic, exponential, and piecewise-defined functions. (a) domain and range, including context limits; (b) increasing/decreasing/constant intervals; (c) absolute max and min; (d) zeros and intercepts; (e) points on the graph ↔ value of the function; (f) end behavior; (g) horizontal and vertical asymptotes; (h) relate characteristics across the four families, in context |
| **AFDA.DA.3** | Calculate and interpret probabilities, including in context. (a) theoretical probability and prediction; (b) conditional probability for dependent, independent, mutually exclusive events; (c) represent with Venn diagrams, probability trees, organized lists, two-way tables, simulations; (d) interpret simulation/experiment probabilities to decide and justify; (e) define and exemplify complementary, dependent, independent, mutually exclusive events; (f) classify given events; (g) compare and contrast permutations and combinations in context; (h) permutations of *n* objects taken *r* at a time; (i) combinations of *n* objects taken *r* at a time |
| **AFDA.DA.4** | Describe and apply the properties of the **normal distribution**, including in context. (a) properties; (b) when normal is reasonable; (c) how mean and standard deviation affect the graph; (d) calculate and interpret a *z*-score; (e) compare two normally distributed sets using *z*-scores; (f) probability as area under the standard normal curve; (g) probabilities from areas, via technology or a table; (h) relate a normal data set to its descriptive statistics |

### Probability & Statistics — the statistics bridge (Units 4, 5, 6)

| Standard | The student will… |
| --- | --- |
| **PS.P.1** | Organize information and apply probability rules in context. (a) classify complementary/dependent/independent/mutually exclusive events and compute; (b) Venn diagrams, tree diagrams, two-way tables; (c) addition, multiplication, complement rules; (d) conditional probability to determine association or independence |
| **PS.P.2** | Represent and interpret situations using **discrete random distributions, including binomial**. (a) identify discrete random variables and valid probability distribution tables; (b) mean (expected value) and standard deviation of a discrete RV, interpreted in context; (c) conditions for a binomial distribution; (d) design and conduct a simulation of a binomial; (e) binomial probabilities in context; (f) mean and SD of a binomial; (g) center, shape, spread of a discrete RV |
| **PS.P.3** | Represent and interpret situations using **normal distributions**. (a) discrete vs. continuous distributions; (b) probability as area via the Empirical Rule and technology; (c) center/shape/spread in context; (d) compare sets using *z*-scores, percentiles, probabilities; (e) standardize and interpret a *z*-score; (f) probabilities via technology in context |
| **A2.ST.3** | Compute and distinguish permutations and combinations. (a) compare/contrast to count; (b) ⁿPᵣ; (c) ⁿCᵣ; (d) contextual problems; (e) verify with technology |

### T — Triangle Trigonometry (Unit 7)

| Standard | The student will… |
| --- | --- |
| **T.TT.1** | Determine the six trigonometric ratios of the acute angles in a right triangle and use them to solve for missing sides and angles, in context. (a) define and represent the six ratios; (b) special right triangles (30-60-90, 45-45-90); (c) use the trig functions, the Pythagorean Theorem, the Law of Sines, and the Law of Cosines in contextual problems; (d) contextual right-triangle problems including angles of elevation and depression |
| **T.TT.2** | Find the area of any triangle and solve non-right triangles with the Laws of Sines and Cosines. (a) apply the Law of Sines / Law of Cosines as appropriate; (b) recognize the **ambiguous case** and the potential for two solutions; (c) integrate both laws with the area formula (Area = ½·*ab*·sin *C*), in context |

### T — Circular Trigonometry (Unit 8)

| Standard | The student will… |
| --- | --- |
| **T.CT.1** | Determine degree and radian measure; sketch angles in standard position; determine the six function values from a point on the terminal side or from another function value. (a) define the radian via the intercepted arc; (b) degree and radian measure for negative and positive rotations; (c) positive and negative coterminal angles; (d) quadrant/axis of the terminal side; (e) draw a reference right triangle from a point on the terminal side; (f) draw a reference right triangle from a given function value; (g) all six function values from a point on the terminal side; (h) given one function value, determine the other five; (i) arc length in radians; (j) area of a sector |
| **T.CT.2** | Develop and apply the properties of the **unit circle** in degrees and radians. (a) convert between radian and degree measure of special angles without technology; (b) define the six circular functions on the unit circle; (c) function values of 0°, 30°, 45°, 60°, 90° and their related angles, in degrees and radians, without technology |
| **T.GT.1** *(survey only)* | Graph and analyze trigonometric functions for periodic phenomena. Used for one closing lesson: read and interpret sine and cosine graphs — amplitude, period, midline — from pre-drawn figures. Full T.GT treatment is out of scope |

## Course map — eight units

Sequence: **Algebra (U1–U3) → Data Analysis (U4–U6) → Trigonometry (U7–U8)** — the course
finishes with trig. Every unit opens with **Lesson X.0, a unit-opener lesson**: a hook
scenario for the unit's big idea, a prerequisite-skills diagnostic, a vocabulary preview, and
the unit's learning-target roadmap — no new content.

| Unit | Title | Standards base | Lessons |
| --- | --- | --- | --- |
| 1 | Algebraic Expressions and Factoring | A2.EO.1–3, A2.EI.2/6 | 8 |
| 2 | Functions, Transformations, and Graph Analysis | AFDA.AF.1, AFDA.AF.2 | 8 |
| 3 | Exponential and Logarithmic Functions | AFDA.AF.1/2 (exp), A2.F.1/2 (log) | 8 |
| 4 | Counting and Probability | AFDA.DA.3, A2.ST.3, PS.P.1 | 7 |
| 5 | Random Variables and the Binomial Distribution | PS.P.2 | 6 |
| 6 | The Normal Distribution | AFDA.DA.4, PS.P.3 | 6 |
| 7 | Right Triangle and Oblique Triangle Trigonometry | T.TT.1, T.TT.2 | 8 |
| 8 | Unit Circle Trigonometry | T.CT.1, T.CT.2, T.GT.1 (survey) | 8 |

59 lessons total (51 content + 8 unit openers).

**Sequencing notes**

- Unit 1's factoring feeds Unit 1.7 (rational expressions) and Unit 2's quadratic work; the
  exponent rules of 1.1–1.2 are the algebra beneath Unit 3's logarithms.
- Unit 3 must follow Unit 2: exponential graphs are analyzed with the transformation
  vocabulary and characteristics framework Unit 2 builds.
- Units 4 → 5 → 6 are a strict chain: probability rules → random variables built on them →
  the normal distribution as the continuous capstone (PS.P.3a contrasts discrete vs.
  continuous, which lands only after Unit 5).
- Units 7 → 8 are the natural pair: the right-triangle ratios of Unit 7 become the reference
  triangles of Unit 8. Do not separate or reorder them.
- Lesson 8.7 (sinusoidal graphs survey) is the precalculus send-off; it leans on Unit 2's
  transformation language. Keep it read-and-interpret only — pre-drawn graphs, no sketching
  from scratch.

## The lesson maps

One lesson per Knowledge-and-Skills cluster, numbered `<unit>.<n>`; `<unit>.0` is the unit
opener. Confirmed with the user 2026-08-04.

### Unit 1 — Algebraic Expressions and Factoring

| Lesson | Standards | Topic |
| --- | --- | --- |
| 1.0 | — | Unit opener: why algebra fluency matters for precalc & stats; diagnostic |
| 1.1 | A2.EO.3a | Simplifying algebraic expressions and exponent rules |
| 1.2 | A2.EO.2a–c | Radicals and rational exponents |
| 1.3 | A2.EO.3b | Factoring: GCF and grouping |
| 1.4 | A2.EO.3b | Factoring trinomials |
| 1.5 | A2.EO.3b, d | Special forms: difference of squares, sum/difference of cubes, perfect square trinomials |
| 1.6 | A2.EI.2b, A2.EI.6a–b | Solving polynomial equations by factoring |
| 1.7 | A2.EO.1a–b | Simplifying rational expressions |

### Unit 2 — Functions, Transformations, and Graph Analysis

| Lesson | Standards | Topic |
| --- | --- | --- |
| 2.0 | — | Unit opener: functions as models; diagnostic |
| 2.1 | AF.2a, e | Function fundamentals: notation, domain and range in context |
| 2.2 | AF.1a–b | Parent functions and transformations |
| 2.3 | AF.1d, f | Equation ↔ graph in both directions, verified on the TI-84 |
| 2.4 | AF.2b–d | Intercepts, zeros, max/min, increasing/decreasing intervals |
| 2.5 | AF.2f–g | End behavior and asymptotes |
| 2.6 | AF.2 | Piecewise-defined functions |
| 2.7 | AF.1c, e, g; AF.2h | Choosing and comparing models in context |

### Unit 3 — Exponential and Logarithmic Functions

| Lesson | Standards | Topic |
| --- | --- | --- |
| 3.0 | — | Unit opener: growth stories; diagnostic |
| 3.1 | AF.1, AF.2 | Exponential growth and decay |
| 3.2 | AF.2g, A2.F.2h | Graphs of exponentials: asymptotes and transformations |
| 3.3 | A2.F.1a, A2.F.2i–j | The logarithm as the inverse; evaluating logs |
| 3.4 | A2.F.1 *(bridge ext.)* | Properties of logarithms |
| 3.5 | *(bridge ext.)* | Solving exponential equations with logs |
| 3.6 | *(bridge ext.)* | Solving logarithmic equations |
| 3.7 | AF.1e | Applications: compound interest, half-life, pH and decibels |

### Unit 4 — Counting and Probability

| Lesson | Standards | Topic |
| --- | --- | --- |
| 4.0 | — | Unit opener: chance and counting; diagnostic |
| 4.1 | DA.3c | Fundamental counting principle; organized lists and trees |
| 4.2 | DA.3g–i, A2.ST.3 | Permutations and combinations |
| 4.3 | DA.3a, d | Theoretical and experimental probability; simulation |
| 4.4 | DA.3e–f, PS.P.1c | Complement, addition rule, mutually exclusive events |
| 4.5 | DA.3b, PS.P.1d | Conditional probability and independence; two-way tables |
| 4.6 | DA.3c–d, PS.P.1b | Venn diagrams and probability trees; justify decisions |

### Unit 5 — Random Variables and the Binomial Distribution

| Lesson | Standards | Topic |
| --- | --- | --- |
| 5.0 | — | Unit opener: from events to variables; diagnostic |
| 5.1 | PS.P.2a | Discrete random variables and probability distributions |
| 5.2 | PS.P.2b, g | Expected value and standard deviation of a random variable |
| 5.3 | PS.P.2c–d | The binomial setting; simulating a binomial |
| 5.4 | PS.P.2e | Binomial probabilities on the TI-84 |
| 5.5 | PS.P.2f–g | Mean and SD of a binomial; interpretation in context |

### Unit 6 — The Normal Distribution

| Lesson | Standards | Topic |
| --- | --- | --- |
| 6.0 | — | Unit opener: the bell curve everywhere; diagnostic |
| 6.1 | DA.4a–b, PS.P.3a | Density curves; discrete vs. continuous; when normal is reasonable |
| 6.2 | DA.4c, h; PS.P.3b | Mean, standard deviation, and the Empirical Rule |
| 6.3 | DA.4d–e, PS.P.3d–e | *z*-scores and comparing distributions |
| 6.4 | DA.4f–g, PS.P.3f | Probability as area; normalcdf and invNorm on the TI-84 |
| 6.5 | DA.4, PS.P.3 | Applications and synthesis in context |

### Unit 7 — Right Triangle and Oblique Triangle Trigonometry

| Lesson | Standards | Topic |
| --- | --- | --- |
| 7.0 | — | Unit opener: measuring the inaccessible; diagnostic |
| 7.1 | TT.1a | The six trigonometric ratios |
| 7.2 | TT.1b | Special right triangles (30-60-90, 45-45-90) |
| 7.3 | TT.1c–d | Solving right triangles; angles of elevation and depression |
| 7.4 | TT.2a | Law of Sines |
| 7.5 | TT.2b | The ambiguous case |
| 7.6 | TT.2a | Law of Cosines |
| 7.7 | TT.2c | Area of any triangle; applied triangulation |

### Unit 8 — Unit Circle Trigonometry

| Lesson | Standards | Topic |
| --- | --- | --- |
| 8.0 | — | Unit opener: angles beyond the triangle; diagnostic |
| 8.1 | CT.1a–d | Angles in standard position; degree and radian measure; coterminal angles |
| 8.2 | CT.1i–j | Arc length and sector area |
| 8.3 | CT.1e, g | Reference triangles; function values from a point on the terminal side |
| 8.4 | CT.1f, h | The other five values from one function value |
| 8.5 | CT.2a–b | The unit circle in degrees and radians |
| 8.6 | CT.2c | Exact values of special angles without technology |
| 8.7 | GT.1 *(survey)* | Reading sine and cosine graphs: amplitude, period, midline, periodic phenomena |

## Mapping content into a lesson

| Lesson element | Source |
| --- | --- |
| Lesson title (`\LessonNumberName`) | "Lesson X.Y: \<Topic\>" |
| **Primary Objective** (lesson plan) | What students will be able to *do / model / interpret / justify*, in student terms |
| **Priority Ideas & Skills** (gold box) | Left: the lettered Knowledge & Skills this lesson covers, in student language. Right: "Key Understandings" — the *why*, drawn from the matching "Understanding the Standards" pages |
| **Vocabulary, Concepts & Theorems** | Terms and notation the standard introduces (use `\TallMath{...}` for tall formulas) |
| **Hook** | A scenario from the course's application domains — science, business, finance for algebra and data; elevation/depression, navigation, and periodic phenomena for trigonometry |
| **Learning Targets** (cover, "I can…") | One target per lettered skill, reworded as "I can …" |
| Activity / homework contexts | Real or realistic data and scenarios; compute *then* interpret |
| Connections line | The unit's core idea, the **standard codes covered** (e.g. `A2.EO.3b`, `PS.P.2e`), and links to prior/next lessons |

Every lesson cites its standard codes — the accountability spine of a SOL-aligned course.
Bridge-extension lessons (3.4–3.6) cite the nearest A2.F code and say "bridge extension" in
the Connections line.

**Unit openers (X.0)** have no new-content codes. Their lesson plan lists the codes of the
*whole unit* as "coming attractions," the warmup is the prerequisite diagnostic, the notes
component is the vocabulary preview and roadmap, and the activity is the hook scenario.

## The technology and "sketch" question

The course requires a TI-84, and several Trigonometry standards say **sketch** (T.CT.1e–f).
The standing rule: students are never asked to construct a graph on a blank page.

- Give a **pre-drawn, pre-scaled axis system** — grid, tick labels, asymptote guides — and
  have students plot, label, or complete on it.
- For a reference triangle (T.CT.1e–f), pre-draw the axes and the terminal ray; students draw
  the perpendicular and label the sides.
- For calculator output (distribution screens, graph windows, tables), show the TI-84 result
  as a **figure to read and interpret**, and put the actual keystrokes in the activity where
  a teacher is circulating.
