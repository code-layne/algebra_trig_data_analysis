# Course Workflow — from the Virginia SOL to lessons

The course structure comes from **`spec/algebra_trig_data_analysis.md`** — the design notes plus
the **course map**. The mathematical **content** comes from the **Virginia Standards of Learning
documents in `spec/`**: units are standard clusters and lessons are groups of the standards'
lettered Knowledge & Skills. This file explains how to turn the standards into lessons and how to
source and adapt them into each lesson's parts.

## Course identity (read this first)

This is **Algebra, Trigonometry, and Data Analysis**, a full-year secondary course combining two
Virginia SOL courses: **Algebra, Functions, and Data Analysis (AFDA)** — a full-year course for
students who finished Algebra 1 and are transitioning toward Algebra 2 — and **Trigonometry (T)**,
written by the state as a one-semester course.

It is a **modeling and applications course**. Nearly every AFDA standard ends in "including those
in contextual situations," and the Trigonometry preface asks for "the application of
trigonometric concepts throughout the course of study." Author accordingly:

- **Start from a context, then extract the mathematics.** AFDA data comes "from science,
  business, and finance"; trigonometry problems live in elevation and depression, navigation,
  surveying, and periodic phenomena. A bare exercise set is off-voice for this course.
- **Transformational graphing is the spine.** AFDA explicitly adopts "a transformational approach
  to graphing functions and writing equations when given the graph." Parent function first, then
  the transformation, in both directions — and reuse that same vocabulary for *A*, *B*, *C*, *D*
  in Unit 10's trigonometric graphs.
- **The data cycle frames AFDA.DA.1 and DA.2**: formulate questions → collect or acquire data →
  organize and represent data → analyze data and communicate results. Name the phase students are
  working in.
- **Technology is assumed but pre-digested.** Both SOL prefaces call for graphing technology.
  Show its output as a **pre-made figure to read and interpret**; save student keystrokes for the
  activity, where a teacher is circulating.
- **Communicate.** Both courses require oral and written communication of method and result. The
  recurring move in every component: compute *then* interpret and justify — "what does this
  number mean here, and how do you know?"
- **Audience is secondary school**, mid-track: students who need scaffolding, worked examples,
  and vocabulary support. Small numbers, concrete contexts, one new idea at a time.

## Where the content lives

- `spec/algebra_trig_data_analysis.md` — the course design notes: identity, the full standards
  inventory, and the unit map. **This is the unit/lesson map.**
- `spec/11AFDA2023ApprovedMathSOL.pdf` and `spec/13Trig2023ApprovedMathSOL.pdf` — the
  authoritative standard text and its **lettered Knowledge & Skills**. Those letters are the
  codes a lesson cites (`AFDA.AF.1c`, `T.CT.2a`).
- `spec/12AFDAUnderstanding the Standards.pdf` and `spec/13TrigUnderstanding the Standards.pdf` —
  VDOE's clarifications: **scope limits, notation, and what is out of bounds**. Read the pages
  for the standard you are authoring *before* you write anything. This is where the grain lives —
  the standard says what, this says how far.

A practical loop per lesson: find the standard's lettered skills in the Approved SOL PDF → read
the matching pages of the Understanding the Standards PDF for scope and notation → choose a
context from the course's application domains → build the components around a compute-then-
interpret spine.

## The course units

`spec/algebra_trig_data_analysis.md` holds the full course map. The default sequence is one unit
per standard cluster, AFDA first, then Trigonometry:

| Unit | Title | Standards |
| --- | --- | --- |
| 1 | Function Families and Transformations | AFDA.AF.1 |
| 2 | Analyzing Graphs of Functions | AFDA.AF.2 |
| 3 | Systems, Inequalities, and Linear Programming | AFDA.AF.3 |
| 4 | Bivariate Data and Curves of Best Fit | AFDA.DA.1 |
| 5 | Experimental Design and Observational Studies | AFDA.DA.2 |
| 6 | Probability, Permutations, and Combinations | AFDA.DA.3 |
| 7 | The Normal Distribution | AFDA.DA.4 |
| 8 | Right Triangle Trigonometry | T.TT.1, T.TT.2 |
| 9 | Circular Trigonometry and the Unit Circle | T.CT.1, T.CT.2 |
| 10 | Graphs of Trigonometric Functions | T.GT.1, T.GT.2 |
| 11 | Trigonometric Identities and Equations | T.IE.1–3 |

Dependencies worth protecting: Unit 4 needs Units 1–2 (you cannot choose a best-fit family before
you know the families); Units 8 and 9 are a pair (the right triangle becomes the reference
triangle); Unit 10 reuses Unit 1's transformation vocabulary. Read the per-unit sequencing notes
in the spec before proposing a reorder.

## Decomposing a unit into lessons

**Convention: one lesson per Knowledge-and-Skills cluster** — *not* one per lettered bullet. The
letters are finer than a 60-minute class; group them into coherent chunks in the order the
standard lists them. Lesson id is `<unit>.<n>` where *n* counts lessons within the unit (Lesson
8.1, 8.2, …). Always **present the proposed lesson map for the unit and confirm it with the user
before authoring** — bullets merge and split depending on the class.

Worked example — **Unit 8 (Right Triangle Trigonometry)**:

| Lesson | Standards | Topic | Likely context |
| --- | --- | --- | --- |
| 8.1 | T.TT.1a | The six trigonometric ratios in a right triangle | ramp slopes, roof pitch |
| 8.2 | T.TT.1b | Special right triangles (30-60-90, 45-45-90) | exact values without technology |
| 8.3 | T.TT.1c–d | Solving right triangles; elevation and depression | surveying, aviation sightlines |
| 8.4 | T.TT.2a–b | Law of Sines and the ambiguous case | non-right triangulation |
| 8.5 | T.TT.2a, c | Law of Cosines and the area of any triangle | land parcels, truss geometry |

Do the same for the other units from the spec's course map. Pull each lesson's scope and notation
from the matching "Understanding the Standards" pages, then write in the course's contextual,
modeling-first voice.

## Mapping content into a lesson

| Lesson element | Source |
| --- | --- |
| Lesson title (`\LessonNumberName`) | "Lesson X.Y: \<Topic\>" |
| **Primary Objective** (lesson plan) | What students will be able to *do / model / interpret / justify* with this topic, in student terms |
| **Priority Ideas & Skills** (gold box) | Left: the lettered Knowledge & Skills this lesson covers, in student language. Right: "Key Understandings" — the *why*, drawn from the matching "Understanding the Standards" pages |
| **Vocabulary, Concepts & Theorems** | Terms and notation the standard introduces (use `\TallMath{...}` for tall formulas) |
| **Hook** | A scenario from the course's application domains — science, business, finance for AFDA; elevation/depression, navigation, and periodic phenomena for Trigonometry |
| **Learning Targets** (cover, "I can…") | One target per lettered skill covered, reworded as "I can …" |
| Activity / homework contexts | Real or realistic data and scenarios — compute *then* interpret and connect to meaning |
| Connections line | The unit's core idea, **the standard codes covered** (e.g. `AFDA.AF.1c, 1d`), and links to prior/next lessons (spiral) |

**Every lesson cites its standard codes.** That is the accountability spine of an SOL course. Put
the codes in the lesson plan's Priority Ideas box and in the Connections line.

## Graphs, sketching, and technology

Several Trigonometry standards say **sketch** (T.CT.1e, T.CT.1f, T.GT.1a, T.GT.1d), and the
course's standing rule is that students are never asked to construct a graph on a blank page.
Reconcile them; do not choose between them:

- **Pre-draw and pre-scale the axes** — grid, tick labels, asymptote guides — and have students
  plot, label, or complete on them. That satisfies "sketch the graph" and removes the setup
  burden that eats a class period.
- **Reference triangles** (T.CT.1e–f): pre-draw the axes and the terminal ray; students add the
  perpendicular and label the sides.
- **Technology output** (scatterplots, regression curves, parameter sweeps): show the
  Desmos/calculator result as a figure to read and interpret. Put the keystrokes in the activity,
  not the notes.

Never ask for a graph sketched from a blank page, and never make a component's core skill depend
on a device the class may not have in hand.
