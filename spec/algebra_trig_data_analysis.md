# Algebra, Trigonometry, and Data Analysis — Course Spec

The course design notes and the **course map**. Structure (units and lessons) comes from this
file; the mathematical **content** comes from the Virginia Standards of Learning documents in
`spec/`. This is the single source of truth for what the course covers and in what order.

## Course identity

**Algebra, Trigonometry, and Data Analysis** is a full-year secondary course that combines two
Virginia SOL courses:

- **Algebra, Functions, and Data Analysis (AFDA)** — 2023 SOL, a full-year course for students
  who have completed Algebra 1 and are transitioning toward Algebra 2. Function families,
  systems and optimization, the data cycle, experimental design, probability, and the normal
  distribution.
- **Trigonometry (T)** — 2023 SOL, written as a **one-semester** course. Right-triangle and
  circular trigonometry, graphs of trigonometric functions, identities and equations.

The combined course is therefore **applications-and-modeling first**. Where the Linear Algebra
course prizes geometric intuition, this one prizes **modeling, interpretation of real data, and
contextual reasoning**: nearly every AFDA standard ends in "including those in contextual
situations," and the Trigonometry standards call for "the application of trigonometric concepts
throughout the course of study."

**Teaching posture**, taken from the two SOL prefaces:

- **Context is the default, not the garnish.** Data comes "from science, business, and finance";
  trigonometry problems involve elevation, depression, navigation, and periodic phenomena.
  Author from a scenario, then extract the mathematics.
- **Transformational graphing is the spine of the function work.** AFDA explicitly adopts "a
  transformational approach to graphing functions and writing equations when given the graph."
  Parent function first, then the transformation, in both directions.
- **Technology is assumed.** Both SOL prefaces call for graphing technology to visualize,
  analyze, verify, and (for AFDA.DA) to produce scatterplots and regressions. Show technology
  output as a **pre-made figure** to read, and reserve student keystrokes for the activity.
- **Communicate.** Both courses require oral and written communication of method and result.
  Every component should ask "what does this mean in context, and how do you know?"
- **The data cycle** (formulate questions → collect or acquire data → organize and represent →
  analyze and communicate results) frames all of AFDA.DA.1 and AFDA.DA.2. Name the phase
  students are in.

## Where the content lives

| File | What it is |
| --- | --- |
| `spec/11AFDA2023ApprovedMathSOL.pdf` | The AFDA standards — the authoritative list of standards and their Knowledge & Skills bullets |
| `spec/12AFDAUnderstanding the Standards.pdf` | VDOE's clarifications for AFDA: scope limits, notation, worked expectations. **Read the relevant pages before authoring an AFDA lesson** |
| `spec/13Trig2023ApprovedMathSOL.pdf` | The Trigonometry standards |
| `spec/13TrigUnderstanding the Standards.pdf` | VDOE's clarifications for Trigonometry. Same rule — read before authoring |
| `spec/course_planning.md` | The running handoff log (build state + next steps). Created and maintained by the lesson-planning skill |

The two "Understanding the Standards" documents are where the *grain* lives — they say how far
a standard goes and what is out of scope. The "Approved SOL" PDFs give the standard text and
its lettered Knowledge & Skills; those letters are the standard codes a lesson cites
(e.g. `AFDA.AF.1c`, `T.CT.2a`).

## The standards

### AFDA — Algebra and Functions

| Standard | The student will… |
| --- | --- |
| **AFDA.AF.1** | Investigate, analyze, and compare linear, quadratic, and exponential function families, algebraically and graphically, using transformations. (a) parent functions; (b) describe the transformation; (c) determine which family best models a representation; (d) write the equation from a graph via transformations; (e) use a graphical or algebraic representation to solve problems in context; (f) graph from an equation via transformations, verify with technology; (g) compare families across multiple representations |
| **AFDA.AF.2** | Investigate and analyze characteristics of the graphs of linear, quadratic, exponential, and piecewise-defined functions. (a) domain and range, including context limits; (b) increasing/decreasing/constant intervals; (c) absolute max and min; (d) zeros and intercepts; (e) points on the graph ↔ value of the function; (f) end behavior; (g) horizontal and vertical asymptotes; (h) relate characteristics across the four families, in context |
| **AFDA.AF.3** | Represent and interpret contextual situations with constraints requiring optimization, using linear programming. (a) model with systems of equations or inequalities; (b) solve systems of ≤ 4 equations/inequalities graphically, algebraically when appropriate; (c) identify the feasible region; (d) identify vertices of the feasible region; (e) determine and describe the max/min over the region; (f) interpret validity of solutions and justify reasonableness in context |

### AFDA — Data Analysis

| Standard | The student will… |
| --- | --- |
| **AFDA.DA.1** | Apply the data cycle with a focus on **bivariate data in scatterplots** and the curve of best fit using linear, quadratic, and exponential functions. (a) formulate investigative questions needing two quantitative variables; (b) collect/acquire data from a representative sample; (c) represent with a scatterplot using technology and describe the relationship in context; (d) make predictions, decisions, and critical judgments from the data, the scatterplot, or the model equation |
| **AFDA.DA.2** | Apply the data cycle with a focus on the **design and implementation of an experiment and/or observational study**. (a) formulate questions and assess data type (quantitative vs. categorical); (b) best sampling techniques — simple random, stratified, cluster; (c) plan and conduct a study addressing control, randomization, and minimization of experimental error; (d) collect/acquire data; (e) handle errors, missing values, bias; (f) identify biased sampling methods; (g) identify and reduce sources of bias in an observational-study plan; (h) select/create/use visual representations; (i) apply appropriate statistical methods; (j) communicate the design, data, analysis, and validity of conclusions |
| **AFDA.DA.3** | Calculate and interpret probabilities, including in context. (a) theoretical probability and prediction; (b) conditional probability for dependent, independent, mutually exclusive events; (c) represent with Venn diagrams, probability trees, organized lists, two-way tables, simulations; (d) interpret simulation/experiment probabilities to decide and justify; (e) define and exemplify complementary, dependent, independent, mutually exclusive events; (f) classify given events; (g) compare and contrast permutations and combinations in context; (h) permutations of *n* objects taken *r* at a time, no repetition; (i) combinations of *n* objects taken *r* at a time, no repetition |
| **AFDA.DA.4** | Describe and apply the properties of the **normal distribution**, including in context. (a) properties of a normal distribution; (b) when normal is a reasonable representation; (c) how mean and standard deviation affect the graph; (d) calculate and interpret a *z*-score; (e) compare two normally distributed sets using the standard normal and *z*-scores; (f) probability as area under the standard normal curve; (g) determine probabilities from areas, using technology or a table; (h) relate a normally distributed data set to its descriptive statistics |

### T — Triangle Trigonometry

| Standard | The student will… |
| --- | --- |
| **T.TT.1** | Determine the six trigonometric ratios of the acute angles in a right triangle and use them to solve for missing sides and angles, in context. (a) define and represent the six ratios; (b) special right triangles (30-60-90, 45-45-90); (c) use the trig functions, the Pythagorean Theorem, the Law of Sines, and the Law of Cosines in contextual problems; (d) contextual right-triangle problems including angles of elevation and depression |
| **T.TT.2** | Find the area of any triangle and solve non-right triangles with the Laws of Sines and Cosines. (a) apply the Law of Sines / Law of Cosines as appropriate; (b) recognize the **ambiguous case** and the potential for two solutions; (c) integrate both laws with the area formula (Area = ½·*ab*·sin *C*) to find the area of any triangle, in context |

### T — Circular Trigonometry

| Standard | The student will… |
| --- | --- |
| **T.CT.1** | Determine degree and radian measure; sketch angles in standard position; determine the six function values from a point on the terminal side or from another function value. (a) define the radian via the intercepted arc; (b) degree and radian measure for negative and positive rotations; (c) positive and negative coterminal angles; (d) quadrant/axis of the terminal side; (e) draw a reference right triangle from a point on the terminal side; (f) draw a reference right triangle from a given function value; (g) all six function values from a point on the terminal side; (h) given one function value, determine the other five; (i) arc length in radians; (j) area of a sector |
| **T.CT.2** | Develop and apply the properties of the **unit circle** in degrees and radians. (a) convert between radian and degree measure of special angles without technology; (b) define the six circular functions on the unit circle; (c) use right-triangle trig, special triangles, and the unit circle to get function values of 0°, 30°, 45°, 60°, 90° and their related angles, in degrees and radians, without technology |

### T — Graphs of Trigonometric Functions

| Standard | The student will… |
| --- | --- |
| **T.GT.1** | Graph and analyze trigonometric functions and use them to represent periodic phenomena. (a) sketch the six parent trig functions over ≥ two periods; (b) domain, range, amplitude, period, asymptote locations from a graph or an equation; (c) effect of the parameters *A*, *B*, *C*, *D* using graphing technology; (d) sketch a transformed sine, cosine, or tangent in standard form over ≥ two periods, positive and negative domain; (e) apply trig functions and graphs to periodic phenomena |
| **T.GT.2** | Graph the six inverse trigonometric functions. (a) domain and range of the inverses; (b) use domain restrictions to determine a value of an inverse function; (c) graph inverse trigonometric functions |

### T — Identities and Equations

| Standard | The student will… |
| --- | --- |
| **T.IE.1** | Evaluate expressions involving the six trig functions and the inverse sine, cosine, and tangent. (a) values with and without graphing technology; (b) angle measures via inverse functions, with and without technology; (c) composite functions mixing trig and inverse trig |
| **T.IE.2** | Use basic trigonometric identity substitutions to simplify and verify identities. (a) reciprocal, Pythagorean, sum and difference, double-angle, and half-angle identities; (b) apply sum, difference, and half-angle identities to evaluate function values of angles that are not integer multiples of the special angles, in context |
| **T.IE.3** | Solve trigonometric equations and inequalities. (a) equations with and without restricted domains, algebraically and graphically; (b) inequalities algebraically and graphically; (c) verify and justify algebraic solutions using graphing technology |

## Course map — the proposed unit sequence

**One unit per standard cluster**, AFDA first (it builds on Algebra 1 and carries the data
strand), Trigonometry second (it is self-contained and the SOL frames it as a semester). The
map below is the default; **confirm it with the user before authoring a new unit**, since a
combined course often reorders or compresses.

| Unit | Title | Standards | Notes |
| --- | --- | --- | --- |
| 1 | Function Families and Transformations | AFDA.AF.1 | Parent functions; the transformational spine of the course |
| 2 | Analyzing Graphs of Functions | AFDA.AF.2 | Adds piecewise-defined; domain/range in context |
| 3 | Systems, Inequalities, and Linear Programming | AFDA.AF.3 | Optimization; feasible regions |
| 4 | Bivariate Data and Curves of Best Fit | AFDA.DA.1 | Data cycle; scatterplots; linear/quadratic/exponential regression |
| 5 | Experimental Design and Observational Studies | AFDA.DA.2 | Data cycle; sampling, bias, control, randomization |
| 6 | Probability, Permutations, and Combinations | AFDA.DA.3 | Two-way tables, trees, Venn diagrams, simulation |
| 7 | The Normal Distribution | AFDA.DA.4 | *z*-scores; area as probability |
| 8 | Right Triangle Trigonometry | T.TT.1, T.TT.2 | Six ratios; special triangles; Laws of Sines/Cosines; area; ambiguous case |
| 9 | Circular Trigonometry and the Unit Circle | T.CT.1, T.CT.2 | Radians, coterminal angles, reference triangles, arc length, sectors |
| 10 | Graphs of Trigonometric Functions | T.GT.1, T.GT.2 | Parent graphs, *A*/*B*/*C*/*D*, periodic phenomena, inverses |
| 11 | Trigonometric Identities and Equations | T.IE.1, T.IE.2, T.IE.3 | Evaluate, simplify/verify, solve equations and inequalities |

**Sequencing notes**

- Unit 4 (bivariate data, curve of best fit) depends on Units 1–2: students must know the three
  function families before choosing which one models a scatterplot. Keep it after them.
- Units 8–9 are the natural pair: the right-triangle ratios of Unit 8 become the reference
  triangle of Unit 9. Do not separate them.
- Unit 10 depends on Unit 1's transformation vocabulary — *A*, *B*, *C*, *D* are the same
  transformations applied to a new parent function. Make that connection explicit.
- If the year is short, the compressible units are 5 (design) and 11 (identities beyond the
  reciprocal and Pythagorean ones). Confirm any cut with the user.

## Decomposing a unit into lessons

**Convention: one lesson per Knowledge-and-Skills cluster**, not one lesson per lettered bullet —
the letters are finer-grained than a 55-minute class. Group the letters into coherent
teachable chunks, in the order the standard lists them, and number lessons `<unit>.<n>`.

Worked example — **Unit 8 (Right Triangle Trigonometry)**:

| Lesson | Standards | Topic | Likely context |
| --- | --- | --- | --- |
| 8.1 | T.TT.1a | The six trigonometric ratios in a right triangle | ramp slopes, roof pitch |
| 8.2 | T.TT.1b | Special right triangles (30-60-90, 45-45-90) | exact values without technology |
| 8.3 | T.TT.1c–d | Solving right triangles; elevation and depression | surveying, aviation sightlines |
| 8.4 | T.TT.2a–b | Law of Sines and the ambiguous case | non-right triangulation |
| 8.5 | T.TT.2a, c | Law of Cosines and the area of any triangle | land parcels, truss geometry |

Always **present the proposed lesson map for the unit and confirm it with the user before
authoring** — bullets merge and split depending on the class.

## Mapping content into a lesson

| Lesson element | Source |
| --- | --- |
| Lesson title (`\LessonNumberName`) | "Lesson X.Y: \<Topic\>" |
| **Primary Objective** (lesson plan) | What students will be able to *do / model / interpret / justify*, in student terms |
| **Priority Ideas & Skills** (gold box) | Left: the lettered Knowledge & Skills this lesson covers, in student language. Right: "Key Understandings" — the *why*, drawn from the matching "Understanding the Standards" pages |
| **Vocabulary, Concepts & Theorems** | Terms and notation the standard introduces (use `\TallMath{...}` for tall formulas) |
| **Hook** | A scenario from the course's application domains — science, business, finance for AFDA; elevation/depression, navigation, and periodic phenomena for Trigonometry |
| **Learning Targets** (cover, "I can…") | One target per lettered skill, reworded as "I can …" |
| Activity / homework contexts | Real or realistic data and scenarios; compute *then* interpret |
| Connections line | The unit's core idea, the **standard codes covered** (e.g. `AFDA.AF.1c, 1d`), and links to prior/next lessons |

Every lesson cites its standard codes — that is the accountability spine of a SOL course, and it
is what the Connections line and the lesson plan's Priority Ideas box are for.

## The technology and "sketch" question

Both SOL courses assume graphing technology, and several Trigonometry standards say **sketch**
(T.CT.1e, T.CT.1f, T.GT.1a, T.GT.1d). The course's standing rule is that students are never
asked to construct a graph on a blank page. Reconcile the two this way:

- Give a **pre-drawn, pre-scaled axis system** — the grid, the tick labels, the asymptote
  guides — and have students plot, label, or complete on it. That satisfies "sketch the graph"
  while removing the setup burden that eats the class period.
- For a reference triangle (T.CT.1e–f), pre-draw the axes and the terminal ray; students draw
  the perpendicular and label the sides.
- For technology output (scatterplots, regressions, parameter sweeps), show the calculator or
  Desmos result as a **figure to read and interpret**, and put the actual keystrokes in the
  activity where a teacher is circulating.
