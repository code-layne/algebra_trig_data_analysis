---
course: Algebra, Trigonometry, and Data Analysis
prefix: atda
meeting_length: 60
reference_lesson: unit01/lesson01
components: [cover, warmup, notes, activity, exit_ticket, homework, slides]
keyed: [warmup, notes, activity, exit_ticket, homework]
one_page: [warmup, exit_ticket]
doc_titles:
  warmup: Warm-Up
  notes: Guided Notes
  activity: Group Activity
  exit_ticket: Exit Ticket
  homework: Homework
note_labels:
  warmup: Warm-Up
  notes: Guided Notes
  activity: Group Activity
  exit_ticket: Exit Ticket
  homework: Homework
skeletons: templates/lesson
unit_tests: true
structure_source: standards
spec_dir: spec
course_index: spec/course_planning.md
check_target: true
point_size: 10
---

# Lesson Shape — Algebra, Trigonometry, and Data Analysis

This is the course profile the shared `lesson-planning` skill (`~/.claude/skills/lesson-planning/`)
reads before authoring anything. The skill carries the mechanism — build, LaTeX rules, workflow,
scripts; **this file carries the policy** — everything true of this course that is not
necessarily true of the others. Keep it current: when a convention changes, change it here first.
The frontmatter is machine-read by the scaffolder; the sections below are read by the skill at
Step 0. The skeletons, the per-component spec (`components.md`), and the SOL-to-lesson content
workflow (`course-workflow.md`) live in `templates/lesson/`.

**Course identity.** ATDA is a full-year secondary **bridge course from Algebra 2 to either
Statistics or Precalculus**, built from four Virginia 2023 SOL courses — Algebra 2 (the review
strand), AFDA (the conceptual core), Probability & Statistics (the statistics bridge), and
Trigonometry (the precalculus bridge). It is a **modeling and applications course**: author every
component from a context, compute, then **interpret and justify** ("what does this number mean
here, and how do you know?"), and **cite the standard codes** the lesson covers (`AFDA.AF.1c`,
`A2.EO.3b`, `PS.P.2e`, `T.CT.2a`). Audience: students who have completed Algebra 2 — assume the
Algebra 1/2 toolkit, but scaffold generously: a context first, small numbers, one new idea at a
time, worked examples, vocabulary support. The **TI-84** is assumed throughout; its output appears
as a **pre-drawn figure to read**, with student keystrokes reserved for the activity.

## 1. The lesson shape

**Every lesson is a hook-driven, tiered gradual release.** A short spiral-review warm-up opens the
period; the teacher poses a hook scenario from the course's application domains and works the
instructional progression through fill-in guided notes (context and numbers first, then the general
statement); groups then work a **three-tier applied investigation** (everyone starts at Tier R and
advances as a group); an independent exit ticket closes the period; the homework is independent
practice plus an optional extension and a preview of the next lesson.

| Phase | Minutes | Component |
| --- | --- | --- |
| Warm-up — spiral review of prerequisites, scored together | 6 | `warmup` |
| Hook + guided notes — direct instruction and guided practice, students filling in | 28 | `notes` |
| Group activity — Tier R → Tier A → Tier E, teacher circulating | 16 | `activity` |
| Exit ticket — notes closed, handed in at the door | 5 | `exit_ticket` |
| Close — collect, assign the homework, preview the next lesson | 5 | `homework` |

The table is the budget for a new plan; sum to 60 before writing the minutes. The authored plans
carry their per-section minutes inside the **Lesson** box (e.g. "1. Build the rules by counting
(10 min)") and in the teacher notes (warm-up 6–8 min, activity 15 min, exit ticket 5 min, homework
"expect 20–35 minutes" out of class). Note `\MeetingLength` was 55 minutes when Units 1–2 were
authored; the period is now 60. Do not re-pace an existing plan unless you are regenerating it.

**What each component is:**

- **`cover`** — student front page: full-bleed royal banner (course, unit, lesson), the
  `\namedateperiod` row (the one place it belongs), a `learningtargetbox` of "I can…" targets (one
  per lettered skill covered), a `tocbox` packet table with a score blank per component and a
  Total row, and a `remindbox` naming the standard codes and where they go next.
- **`warmup`** — 3–5 quick items of *prerequisite* fluency and spiral from the previous lesson,
  with work space, in one `notesbox`. Item 1 is often the lesson's first two minutes (it
  *discovers* the day's rule). **Exactly one page, blank and key.** May be a prefab PDF
  (`warmup/main.pdf` + `warmup_key/main.pdf`), in which case the plan embeds its thumbnail.
- **`notes`** — *Guided Notes*: `objectivebox` **filled in, not blank** (the cover's learning
  targets restated, identical in blank and key); `vocabbox` of `\termblanklong` terms (key:
  `\vocabans`); `hookbox` repeating the plan's hook with response lines; numbered `notesbox{Title}`
  instruction sections with `\blank`/`\writeline` fills and `work` blocks at the points students
  record steps; a closing `practicebox` ("Guided Practice") of 1–2 worked-with-class problems.
  Every function lesson uses the transformational-graphing frame (parent first, then the
  transformation, both directions); the DA units name the data-cycle phase.
- **`activity`** — *Group Activity*: an applied investigation (a data set to analyze, a scenario
  to model, a measurement to solve for) in **three `tcolorbox`es** titled **Tier R — Remediate**,
  **Tier A — Approaching Proficiency**, **Tier E — Extension** (`colframe=black!40`), escalating
  in difficulty on the same skills; the top tier reaches an interpret / justify / critique-the-model
  task. Keystrokes, if any, live here.
- **`exit_ticket`** — 2–3 independent items in one `notesbox`, no notes, at least one "what does
  this result mean?" item, and typically one item that is the *wrong conclusion* from the same
  observation an earlier item rewarded. **Exactly one page, blank and key.**
- **`homework`** — a numbered practice set written to the standard's lettered skills (a
  `notesbox`), an in-context `scenariobox`, a look-ahead `scenariobox`, an `extensionbox`
  ("Extension — optional"), and a closing `remindbox`. The key shows worked steps for the harder
  items in `work` blocks.
- **`slides`** — the Beamer deck (`aspectratio=169, 11pt`): hand-built title slide on a royal
  canvas, then `\royalheader{}` + `\sectionlabel[color]{}` frames following the lesson's
  instructional progression — hook, hook payoff, each notes section, guided practice, activity
  launch, exit ticket, homework. Every lesson owes a deck; it feeds two of the five products.

**Unit openers.** Every unit opens with **Lesson X.0**, a unit-opener lesson in the *same* component
shape: a hook scenario for the unit's big idea, a prerequisite-skills diagnostic, a vocabulary
preview, and the unit's learning-target roadmap — **no new content and no new codes**; its plan
lists the codes of the lessons that follow. `unit01/lesson00` is the model opener and
`unit02/lesson00` the model for a **graph-reading** opener.

**What this course does not have — do not re-add any of it:**

- **No `ap_practice`, no `experience` (EFFL) component, no unscored back-of-packet set.** The
  build knows exactly six student names (`STUDENT_ORDER`) and every lesson uses all of them.
- **No school year anywhere** — no `\SchoolYear` macro, nothing dated on a plan, packet, or test.
- **No DeltaMath or other platform homework.** Homework is the paper page in the packet.
- **No "sketch from a blank page" item, ever** — including where a Trigonometry standard says
  *sketch* (`T.CT.1e–f`, `T.GT.1`). Satisfy it with a **pre-drawn, pre-scaled axis system** (grid,
  tick labels, asymptote guides, the parent already plotted) that students plot, label, or complete
  on; a reference triangle with axes and terminal ray pre-drawn; a figure to read; or a table to
  fill. The key adds the image curve as an `only marks` plot *inside the same axis* so the figure's
  dimensions — and page parity — are unchanged. A grid meant for plotting needs a gridline at every
  integer; a grid meant for reading needs sparse tick labels plus `minor x/y tick num`.
- **No component's core skill may depend on a device the class may not have in hand.**

**`unit01/lesson01` is the reference implementation** of the ordinary lesson. Mirror its preamble,
box usage, pacing, and tone; the live lesson overrides every document, this one included. For a
graph-heavy lesson also open `unit02/lesson03` (the settled no-sketching pattern) and
`unit02/lesson00` (the `pgfplots` figure style: `axis lines=left`, `grid=both` at `linegray!45`,
`\scriptsize` tick/label fonts, `royal` plot, integer-friendly ticks).

## 2. Grading and homework policy

- **Every keyed component is scored on the cover.** The `tocbox` carries a `\blank{1.2cm}` score
  cell for Warm-Up, Guided Notes, Group Activity, Exit Ticket, and Homework, plus a Total row. No
  component prints `NA`. Keep the rows aligned with the components actually scaffolded (all five).
- **Warm-up** is scored together in class; **exit ticket** is collected at the door, notes closed,
  and the teacher note says what each item's miss diagnoses.
- **Homework is paper, every lesson**, authored for every lesson, worked out of class ("expect
  20–35 minutes" in the plan's Reinforcement & Extension box and Homework teacher note). There is
  no platform override and no course-wide due-date rule recorded; the plan's Reinforcement &
  Extension box states the expectation.
- Unit tests are scored on the four-part 100-point blueprint (section 6); their rationale and
  rubrics live on `unit_cover_key` page 2, never in a test key.

## 3. Where structure comes from

`structure_source: standards`. There are no AP CED files; the path is the shared skill's
`references/standards-workflow.md`, specialised by **`templates/lesson/course-workflow.md`** (read
it at Step 1 — the SOL-to-lesson loop, the content-mapping table, and the sketching/technology
rule). The documents:

- **`spec/algebra_trig_data_analysis.md`** — the course design notes and **the course map**: eight
  units, 59 lessons (51 content + 8 openers), Algebra (U1–3) → Data (U4–6) → Trig (U7–8), with the
  full lesson maps and standard codes, user-approved 2026-08-04. **This is the single source of
  truth for structure.** `course-workflow.md`'s eleven-unit table predates the restructure —
  where the two disagree, the spec wins. `COURSE_BREAKDOWN.md` is the reader-facing derivation of
  the same map plus a build-state table.
- **`spec/11AFDA…`, `12Alg2…`, `13Trig…`, `15ProbStat…ApprovedMathSOL.pdf`** — the standard text
  and its **lettered Knowledge & Skills**, the codes a lesson cites.
- **`spec/…Understanding the Standards.pdf`** (AFDA, Trig, Prob/Stat) — VDOE's scope limits and
  notation. **Read the pages for the standard before authoring**; this is where the grain lives.
  Don't invent scope the standard does not carry.

**Mapping rule: one lesson per Knowledge-and-Skills cluster**, not one per lettered bullet; group
the letters into coherent 60-minute chunks in the order the standard lists them, lesson id
`<unit>.<n>`. **Present the proposed lesson map for a unit and confirm it with the user before
authoring.** Every unit starts with the X.0 opener. Unit 3's lessons 3.4–3.6 are deliberate
**bridge extensions** past the A2 codes — cite the nearest `A2.F` code and label them as such in
the plan. **Deliberately excluded** (do not author): linear programming (`AFDA.AF.3`), bivariate
data and regression (`AFDA.DA.1`), experimental design (`AFDA.DA.2`), inverse trig graphs
(`T.GT.2`), trig identities and equations (`T.IE.1–3`); `T.GT.1` survives only as the read-only
survey in Lesson 8.7.

**Every lesson cites its codes** in the plan's Priority Ideas & Skills box and its Connections /
"where these codes go next" line, and on the cover's `remindbox`.

**The planning log — `course_index: spec/course_planning.md`.** It is the running handoff log:
**read it at Step 0** (build state and the next steps left by the previous run) and **update it at
the end of every run, even a partial one** — the user should never have to ask. Keep three
sections current and terse, overwriting stale entries rather than appending a changelog:
*Last updated* (absolute date + one-line summary of the run), *Current state* (which lessons are
authored vs skeleton vs built, confirmed lesson maps, per-lesson findings worth carrying forward),
*Next steps* (concrete actions and open questions). Also keep `COURSE_BREAKDOWN.md`'s build-state
table in step with what exists on disk.

## 4. Style notes

- **Prefix `atda`** — `shared/atda-{colors,article,boxes,key,beamer}.sty`. The packages were ported
  from the Linear Algebra course (2026-08-04) with the palette changed to royal blue / gold.
- **Course macros live in the style package.** `atda-article.sty` defines `\CourseName`
  (*Algebra, Trigonometry, and Data Analysis* — covers and title slides), `\CourseHeaderName`
  (*Algebra, Trig \& Data Analysis* — the short form `\pageheader` prints so the banner and lesson
  id fit one line), and `\MeetingLength`. A lesson plan defines only `\UnitNumberName` and
  `\LessonNumberName`; its title block is `\CourseName` alone. **There is deliberately no
  `\SchoolYear`** — do not reintroduce one.
- **Every document in this course is 10pt** — student components, keys, and the plan alike
  (`\documentclass[10pt]{article}`). The shared skill's "student components are 12pt" invariant
  does not apply here; the reference lesson overrides it. `\boxguard` counts are
  baseline-relative, so a guard size tuned in a 12pt course is not portable.
- **Palette (the only defined names — anything else is a compile error):** `royal` (#1D3F94),
  `royallight`; `mist`, `mistmid` (paired backgrounds, banner subtitle); `goldacc`, `goldbg`,
  `hookbg` (hook, extension, keep-in-mind); `plumacc` on `plumbg` (`practicebox` — deliberately
  not blue so guided practice reads apart from the notes boxes); `greenbg`/`greenacc`
  (vocabulary); `redbg`/`redacc`; `charcoal`, `slate`, `graybg` (`teachernote` background),
  `linegray`; `keyred`. Lesson-plan background aliases: `bluebox`, `goldbox`, `greenbox`,
  `redbox`, `plumbox`. **Undefined here:** `burgundy`, `blush`, `navy`, `sky`, `skymid`,
  `navylight`, `royalblue`, `skyblue`, the `forest` family, bare `gold`. Translate anything pasted
  from another course. `atda-beamer` deliberately overrides `royal`, `goldacc`, `hookbg` with
  brighter values for dark slides — never sync them back to `-colors`.
- **`fixedskillbox` exists** (`\begin{fixedskillbox}[Title]{color}`, unbreakable) beside the
  breakable `skillbox`; the plan's Spiral Review box uses it. Lesson-plan boxes take the background
  color as the last argument.
- **Vocabulary is `\termblanklong{Term}` (blank) ↔ `\vocabans{Term}{definition}` (key).** There is
  **no `\termans`** and no fixed-height `\termrowheight` row; `\termblank{Term}` here is a bold
  term + inline blank + one write-line, rarely used. **vocabpar is structural in this course**:
  `\termblank`, `\termblanklong`, and `\vocabans` each open with their own `\par`, so **do not add
  `\par\vspace{2pt}` after a vocab intro sentence** (the shared `conventions.md` prescribes it for
  other courses; here it double-spaces the box). Treat the term macros as frozen.
- **`\answerspace` is not defined** in `-article` or by convention — reserve prose room with
  `\writelines{n}` (matched by *n* `\ansline{}`s; note `\writelines{n}` here ends in `\\`, so it
  occupies **n + 1** line slots) or `\vspace`, and multi-step work with `work`. Reach for `work`
  before `\writelines`; `\ansline` *width* can cost a page even when every count matches (a wrapped
  `\ansline` trails only on its last line — grep `pdftotext -layout` for answer lines with no dotted
  trail).
- **`steptable` / `\step` / `\steprel` and `\componenttable` do not exist.** `work` takes no
  argument; its body is an amsmath `aligned`, one statement per line, `&` before the relation;
  `\setlength{\workrowsep}{6pt}` in a component's preamble (blank and key both) adds handwriting
  room without breaking parity — but it does not always buy a page back, and a guard or
  `\tcbbreak` may be the right lever instead.
- **`\boxguard` is inert inside a breakable `tcolorbox`**; to split inside one use `\tcbbreak`,
  mirrored in blank and key, and **never author a `\tcbbreak` until a build proves it is needed**.
  A guard must *exceed* its box, never approximate it. A nearly blank last page is a boxguard
  violation. Guard the stem of every figure item and every item whose `work` block is tall — in the
  blank the work block is a `\vphantom`, so a split answer space is invisible until rendered.
  Every box in the lesson plan needs a guard, including the `teachernote`s.
- `teachernote` lives in `-boxes` with an **optional** title argument (`[Warm-Up]`); a bare
  `\begin{teachernote}` still compiles.
- `\TallMath{...}` (tall inline math) is defined per document; the skeletons include it. The plan
  loads `graphicx` with `\graphicspath{{images/}}` (`-article` does not).
- **Beamer.** `atda-beamer` provides `\royalheader{Title}` and `\sectionlabel[color]{LABEL}`. It
  does **not** load `atda-article` (so `\CourseName` is undefined — write the course name
  literally) and does **not** load `tcolorbox` (use `\begin{block}{}`); beamer's `itemize` takes no
  `[leftmargin=…]` — use `\setlength{\itemsep}{…}`. Never pull text up under a `\[...\]` display
  with a negative `\vspace` (it overprints with a clean log); check `Overfull \vbox` in the deck
  log for wide tables, and **eyeball the deck** — it has hyphenated table cells mid-word at
  projection size with a clean log.
- **Tables.** Put the `X` column on the prose column, not the last notation column; a two-word
  header near its column width needs an explicit `\newline`; a label column must hold its longest
  entry on one line; a tall `\ans` in a table cell needs a shared strut in the blank; `\ans` cells
  holding fractions need `\dfrac`.
- Only `cover/main.tex` and the unit tests carry `\namedateperiod`; `\namepartnerperiod` is unused.

## 5. Lesson-plan section order

Title block (`\CourseName` / `\UnitNumberName \LessonNumberName`, no year) → **Primary Objective**
(a mist/royal `tcolorbox`, in student terms: do, model, interpret, justify) → **Priority Ideas &
Skills** (`skillbox{goldbox}`, two minipages: left the lettered Knowledge & Skills covered, tagged
with their codes, plus supporting fluency and "where these codes go next"; right the Key
Understandings — the *why*, from the Understanding the Standards pages) → **Vocabulary, Concepts &
Theorems** (`skillbox{greenbox}`, a `tabularx` term/meaning table, `\TallMath` for tall formulas)
→ **Activate Prior Knowledge & Spiral Review** (`fixedskillbox{mist}`: the warm-up items and how to
use the results; the warm-up thumbnail only if it is a prefab PDF) → **Hook** (`skillbox{mist}`, a
scenario from the course's application domains, posed as a vote or a dispute between two students,
resolved later off the notes) → **Lesson** (and *Lesson (cont.)*; `skillbox{mist}` with
`multicols{2}`, numbered sections with minutes, the questions to pose in bold) → **Explicit
Instruction: <technique>** (one `skillbox{mist}` per technique, steps left, worked example or
calculator screenshot right) → **Active Monitoring** (`skillbox{redbox}`: what to circulate for,
cold-call prompts) → **Group Work & Differentiation** (`skillbox{redbox}`, `multicols{3}` of
Tier R / Tier A / Tier E mirroring the activity) → **Individual Work & Assessment**
(`skillbox{redbox}`: exit-ticket items + a conceptual/justification check + what to do with the
results) → **Reinforcement & Extension** (`skillbox{goldbox}`: homework overview and expected time,
the extension, a preview of the next lesson) → **Teacher Notes, five, in packet order:**
`[Warm-Up]`, `[Guided Notes]`, `[Group Activity]`, `[Exit Ticket]`, `[Homework]` — pacing, answers,
common errors, what each miss diagnoses. Five full-length notes can overflow a 5-page plan; a
complete note alone on a final page is acceptable once the earlier pages are measured full.

## 6. Unit-level and course-level assessments

**Unit tests.** A unit holds `tests/` (`practice_test/`, `actual_test/`;
`include ../../shared/tests.mk`; its `drop` publishes the *practice* test to `sample_test/main.pdf`),
`test_keys/` (likewise to `sample_test_key/main.pdf`), and the two `sample_test*` drop-in dirs that
`shared/unit.mk` merges at the tail of the unit student / key packets. **The actual test and its
key are never merged into any packet.** The scaffolder creates all of it the first time a unit is
created (`--tests` re-runs it, `--no-tests` skips it). Tests keep `\namedateperiod` (taken in a
testing setting). Build: `make -C unitXX/tests all && make -C unitXX/test_keys all`, *before* the
unit packet. **The two published PDFs are build outputs that must be committed** — `unit.mk` reads
them from the source tree.

- **Blueprint (100 pts, four `\parthead` parts, mirrored by the practice and actual forms):**
  A Vocabulary matching (with two distractors), B Multiple Choice (one item per lesson's error
  class, in lesson order), C Short Answer & Computation (**one item per content lesson in lesson
  order**, then synthesis items), D Extended Response (two interpret/justify prompts). Practice and
  actual are **parallel forms** — same structure, different numbers and contexts, definitions
  reworded and relettered, MC options reordered so no letter transfers.
- **Verify every numeric claim in pure Python before authoring**, both forms. Design every graph
  backwards from integer zeros. A shared `\pgfplotsset{testaxis/.style={...}}` is defined
  identically in all four files. Practice test and key must be the same number of pages.
- **No `teachernote` in any test key** — the practice key is published into the key packet and its
  blank rides in the *student* packet. Rationale, the named Part C deductions, and the Part D
  rubrics go on **page 2 of `unitXX/unit_cover_key/main.tex`**.

**Unit cover pair.** `unit_cover/` (1 page, student) and `unit_cover_key/` (the same page 1 plus
one page of exam scoring notes, key packet only) both `\input` **`unit_cover/body.tex`**, so page 1
cannot drift; edit the cover there, never in a wrapper. Page 1: banner → overview → lesson table →
the unit's big ideas (its error streaks made explicit) → a test-blueprint `remindbox`. Keep the
notes to one page: cover + notes is one double-sided sheet. `unit.mk` compiles both itself and
merges the cover ahead of the lesson packets; a unit with no `unit_cover_key/` gets the plain cover
in both. `unit02`'s pair and tests are the model for any graph-heavy unit; `unit01`'s for an
algebra unit.

**Unit tests and covers are outside `make check`** (the gate walks `unitXX/lessonMM/` only). Check
by hand what it would have caught: blank/key parity on both forms, no `teachernote` in a test key,
no `\ans` inside math — and open all four test PDFs page by page for stranded boxes.

**Course final — `finals/`.** A cumulative final for the whole course lives in a top-level
`finals/` directory (sibling of the `unitXX/` dirs; **not yet created** — planned as the last
deliverable, after Unit 8). Trigger: any request for a "final," "final exam," or "cumulative
assessment." It follows the unit-test practice/actual pattern as **four flat subdirectories**, each
with a `main.tex`: `practice_final/` (study copy, opens with the `remindbox` "this is a practice
final" banner), `practice_final_key/`, `final/` (the real exam, plain **Instructions** line),
`final_key/`. Practice and final are parallel forms. It is **not** created by the scaffolder and
does **not** use `shared/tests.mk`; there are **no `sample_*` drop-in dirs and no `drop`/publish
step** — the final is standalone, merged into no packet, and must not be added to `shared/root.mk`
or `unit.mk`. Workflow (still bookended by reading and updating the planning log):

1. Scaffold by hand — `mkdir -p finals/practice_final finals/practice_final_key finals/final
   finals/final_key` — and write the self-contained `finals/Makefile`, which globs `*/main.tex`
   and compiles each to `target/finals/<name>/main.pdf`:

   ```make
   # finals/Makefile — build the cumulative course final exam.
   PROJECT_ROOT := $(abspath ..)
   TEXINPUTS    := $(PROJECT_ROOT)/shared//:
   PDF_DIR      := $(PROJECT_ROOT)/target/finals
   LATEXFLAGS   := -xelatex -interaction=nonstopmode -halt-on-error -file-line-error

   FINALS := $(patsubst %/main.tex,%,$(wildcard */main.tex))

   .PHONY: all clean $(FINALS)
   all: $(FINALS)
   $(FINALS):
   	@mkdir -p $(PDF_DIR)/$@
   	cd $@ && TEXINPUTS="$(TEXINPUTS)" latexmk $(LATEXFLAGS) -outdir="$(PDF_DIR)/$@" main.tex
   	@echo "OK  final -> target/finals/$@/main.pdf"
   clean:
   	rm -rf $(PDF_DIR)
   ```

2. **Design the blueprint — genuinely cumulative and balanced across the three strands** (Algebra
   U1–3, Data U4–6, Trig U7–8); do not let the trig units, freshest and last, crowd out the rest.
   Sweep every unit's `practice_test` Part A vocabulary and Part C spines. The proven shape is
   50 questions / 100 pts in four parts mirroring the unit tests: A Vocabulary (16, matching sets
   split by strand), B Multiple Choice (12, ~1 concept check per unit), C Short Answer &
   Computation (16, **at least one computational item per unit**, weighted to the heaviest
   standards), D Extended Response (6, cross-unit synthesis — Unit 1's Part D prompts are the
   model). Scale the counts to the course but keep Part C's per-unit spine. Reuse the unit tests'
   hand-verified numeric spines where you can.
3. Author the four files blank-and-key in lockstep, mirroring the newest unit's tests (preamble,
   `\parthead` strips, box usage, key style): blanks load `atda-boxes`, keys `atda-key`, every
   answer in `\ans{}`, every math macro the body needs defined in each preamble. **Only
   `finals/*_key/` may keep scoring notes in a `teachernote`** — they are merged into no packet and
   have no cover. Different numbers and reshuffled vocabulary letters between the two forms.
4. **Verify all arithmetic in pure Python before authoring, both forms** — non-negotiable. Check
   the ambiguous case explicitly on any Law of Sines item.
5. `make -C finals all`; scan all four logs for `^!` / file-line errors, grep for `\ans` inside
   `$...$` (zero), check overfull `\hbox > 15pt` (the ~10.8pt banner is fine), page-count each PDF,
   and spot-check at least one key page for red answers with no tofu.
6. Update the planning log with the deliverable, the blueprint, and both forms' Part C spines.

## 7. Legacy shapes and regeneration

**This course has only ever had one component shape** — the seven-component packet above, in force
from Lesson 1.1 with all five conventions (vocabpar structural, teachernote, namestrip, work rule,
boxguard) — so there is nothing to convert. The build knows no legacy names; every directory under
`unit*/lesson*/` is already in the current shape. What varies is only **authored vs skeleton**:

| State | How to recognize | Count (2026-09) |
| --- | --- | --- |
| **authored, built, gated** | no `TODO` markers; `make check` passes | 16 of 59 — `unit01/lesson00`–`07`, `unit02/lesson00`–`07` |
| **skeleton** | the scaffolder's `% TODO` markers still in `main.tex` and every component | 43 — all of Units 3–8 |

All 59 lesson directories, and every unit's `tests/`, `test_keys/`, `sample_test/`,
`sample_test_key/`, exist on disk; Units 1 and 2 also have their cover pair and both test forms
keyed. **Author a skeleton lesson in place** — `Read` each scaffolded file before writing it; do
not re-scaffold, the directory already exists and `new_lesson.py` refuses to overwrite it without
`--force`. Next in sequence: Unit 3, opening with Lesson 3.0.

If a shape change is ever adopted (a component added or removed), record the old shape here with a
recognition rule, a numbered conversion procedure, and a scoreboard — and remember there is **no
bulk sweep**: a project-wide retrofit re-flows the pagination of every verified lesson at once.
Convert lesson by lesson as each is reviewed, then `rm -rf .stamps/unitXX/lessonYY
target/unitXX/lessonYY` and rebuild.

## 8. Review order

When reviewing or revising a lesson, run the conventions in this order:

> **1. teachernote → 2. namestrip → 3. work rule → 4. boxguard**

vocabpar is not a step — it is structural, enforced by the term macros. The first three each change
how much vertical space a component takes; **boxguard runs last because it repairs the pagination
the other three disturb.** Re-measure after each step — a "this guard costs a page" verdict is only
valid for the box heights it was measured against. Apply only the conventions named (all four if
none are named), to the lessons named, one lesson at a time — **no bulk sweep**. Also review the
deck (every lesson has one; look at it, the log is clean when it is wrong).

| # | Convention | How to apply here | Gated? |
| --- | --- | --- | --- |
| — | vocabpar | nothing to do — the term macros carry the `\par` | n/a |
| 1 | teachernote | `python3 ~/.claude/skills/lesson-planning/scripts/movenotes.py unitNN/lessonMM` (`--check` previews); test keys by hand → `unit_cover_key` p2 | yes (lessons only) |
| 2 | namestrip | `python3 ~/.claude/skills/lesson-planning/scripts/namestrip.py --project . --unit NN --lesson MM` (`--check` previews) | yes |
| 3 | work rule | byte-identical `work` blocks; `\writelines{n}` only for prose drift; trim wrapped `\ansline`s | yes (as page parity) |
| 4 | boxguard | `\boxguard` / `\boxguard[n]` before the `\begin{...}`, blank **and** key; `\tcbbreak` inside a breakable box | **no — eyes only** |

**The convention gate — `make check`.** `check_target: true`: `make -C unitXX/lessonYY check`
(also `make -C unitXX check` and `make check` at the root) builds first, then runs
`shared/lesson_check.py`, reporting every violation in one pass and exiting 1. It enforces
**page parity** (each keyed component's page count equals its `_key`'s), **one-pagers** (`warmup`
and `exit_ticket` exactly one page, blank and key), **ans-in-math** (no `\ans`/`\ansline`/`\vocabans`
inside `$…$`, `\[…\]`, `\(…\)` — comments and escaped `\$` are understood), **teachernote** (none in
a lesson `_key`), and **namestrip** (no live name row on a worksheet component). Source checks alone:
`python3 shared/lesson_check.py unitXX/lessonYY --no-pages`. It **cannot see boxguard** — a stranded
stub changes no page count, and a nearly blank last page passes at perfect parity when the key
strands identically — so open the PDF. Unit tests, covers, and `finals/` are outside the gate but
not exempt from the conventions (section 6).

**Always finish with the evidence**, per lesson: `make -C unitXX/lessonYY all` exits 0 **and**
`make -C unitXX/lessonYY check` exits 0 — quote the gate's output rather than re-deriving page
counts — plus confirmation that you eyeballed every component's break points and last page, and
the deck. Report any violation you could not resolve and why. Then update the planning log
(section 3).
