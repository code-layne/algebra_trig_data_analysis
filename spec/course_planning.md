# ATDA Course Planning Log

The running handoff log for the lesson-planning skill. Read at the start of every run,
update at the end. Overwrite stale entries — this is a state file, not a changelog.

## Last updated

**2026-08-05** — Built **Unit 2's summative layer**: the `unit02/unit_cover/` + `unit_cover_key/`
pair and all four unit assessments (`tests/practice_test`, `tests/actual_test`,
`test_keys/practice_test_key`, `test_keys/actual_test_key`). All four tests are **6 pages blank and
key**; the cover is 1 pp student / 2 pp key. Every numeric claim in both forms was verified in pure
Python before authoring. **Unit 2 is now complete end to end: 8 lessons + cover + two parallel test
forms + two keys.** `make -C unit02 check` passes (8 lessons, no violations); the unit packets come
out 161 pp student / 162 pp key, the +1 being the key-only scoring-notes page by design. The
boxguard eyeball pass found **three real violations invisible to every page count** — see the
`unit02/tests` entry below.

*Previous run (same day): authored **Unit 2 Lesson 2.7 (Choosing and Comparing Models in Context,
`AFDA.AF.1c, e, g`; `AFDA.AF.2h`)** in full — plan, cover, warm-up, guided notes, activity, exit
ticket, homework, all five keys, and the deck. **This closes Unit 2 as lessons.** It is the unit's
only lesson whose content is a *decision procedure* rather than a reading skill: the family is chosen
by how the outputs **change**, not by what the graph looks like. `make -C unit02/lesson07 all` and
`check` both pass; every numeric claim in both blank and key was verified in pure Python first. The
boxguard eyeball pass found **four real violations invisible to the gate** — one of them the worst
stub the course has produced (an activity page 4 holding a single write-line) — plus **two
table defects on the projected deck** (`flat-tens`, `ver-tex` hyphenated mid-word). **16 of 59
lessons authored.***

*Earlier run (same day): authored **Unit 2 Lesson 2.6 (Piecewise-Defined Functions, `AFDA.AF.2`, esp.
`AF.2h`)** in full — plan, cover, warm-up, guided notes, activity, exit ticket, homework, all five
keys, and the deck. This is the unit's **synthesis lesson**: the whole `AF.2` checklist run once more
on a graph that takes more than one rule. `make -C unit02/lesson06 all` and `check` both pass; every
numeric claim in both blank and key was verified in pure Python first. The boxguard eyeball pass
found **one real violation invisible to the gate** (homework item 4's stem and figure at the foot of
p1 with its question and all four answer lines opening p2) plus **the first slide-deck defect in the
course that no log reports** (two text lines overprinting under a `\[...\]` display).*

*Earlier run (same day): authored **Unit 2 Lesson 2.5 (End Behavior and Asymptotes,
`AFDA.AF.2f–g`)** in full — plan, cover, warm-up, guided notes, activity, exit ticket, homework, all
five keys, and the deck. This is the lesson where **five lessons' worth of plants get harvested at
once** (2.0's rational table, 2.1's excluded value, 2.2's $(0,\infty)$ range, 2.3's asymptote
landmark, 2.4's coffee). The boxguard eyeball pass found **one real violation invisible to the gate**
(homework item 8's answer space split 2+1 across a page break) plus **two table defects no check can
see** (a label column wrapping mid-equation, and a header wrapping mid-word).*

*Earlier run (same day): authored **Unit 2 Lesson 2.4 (Intercepts, Zeros, and Extrema,
`AFDA.AF.2b–d`)** in full — plan, cover, warm-up, guided notes, activity, exit ticket, homework, all five keys, and the
deck. This is the unit's **first pure graph-reading lesson**: no equation is required anywhere in the
activity, exit ticket, or the context items, which is the AFDA guidance's own scope
(characteristics are investigated "from only a graph"). `make -C unit02/lesson04 all` and `check`
both pass; every numeric claim in both blank and key was verified in pure Python first. The boxguard
eyeball pass found **one real violation invisible to the gate** (homework item 4's answer space split
across a page break) plus a **table defect no check can see** (a two-line header wrapping
mid-parenthesis), both fixed.*

*Earlier run (same day): authored **Unit 2 Lesson 2.3 (Equations and Graphs in Both Directions,
`AFDA.AF.1d, f`)** in full — the unit's first both-directions lesson and the course's first
technology lesson (the TI-84 as a verification tool, not an oracle). The boxguard pass found one real
violation invisible to the gate (the homework's remindbox alone on p4) plus a figure defect no check
can see (a pgfplots legend printing on top of its own panel title), both fixed.*

*Earlier run (same day): authored **Unit 2 Lesson 2.2 (Parent Functions and Transformations,
`AFDA.AF.1a–b`)** in full — the unit's first transformation lesson and the first to use the AFDA
guidance's own six-notation list. The boxguard pass found two real violations invisible to the gate
(a stranded write-line atop homework p4, a stranded single line atop plan p4), both fixed.*

*Earlier run (same day): authored **Unit 2 Lesson 2.1 (Function Fundamentals: Notation, Domain,
and Range, `AFDA.AF.2a, e`)** in full. The unit's first content lesson and the first to teach set
and interval notation; the boxguard pass found no violations.*

*Earlier still (same day): authored **Unit 2 Lesson 2.0 (Unit Opener: Functions as Models)** in full.
This is **the first lesson of the AFDA half** and the course's **first graph-reading lesson**:
seven pre-drawn `pgfplots` figures, no sketching anywhere. The boxguard eyeball pass found **one
real violation invisible to the gate** (a stranded stub atop homework p3) plus two dead-space wins;
all resolved.*

*Earlier still (same day): built **Unit 1's summative layer** — the `unit01/unit_cover/` +
`unit_cover_key/` pair (the course's first unit cover) and all four unit assessments
(`tests/practice_test`, `tests/actual_test`, `test_keys/practice_test_key`,
`test_keys/actual_test_key`). All four are 4 pages blank and key; the cover is 1 pp student /
2 pp key. Every numeric claim in both forms was verified in pure Python before authoring, and a
teachernote/boxguard pass found and fixed two real boxguard violations invisible to any page
count. Unit 1 is complete end to end: 8 lessons + cover + two parallel test forms + two keys.*

## Course-wide rules set by the user (2026-08-04)

1. **No school year on any document.** These materials are reused year over year, so nothing
   printed on a lesson plan, packet, or test carries one. `\SchoolYear` was **deleted** from
   `shared/atda-article.sty`, the `--year` flag was dropped from `new_lesson.py`, and all 59
   scaffolded lesson plans now title on `\CourseName` alone. Do not reintroduce it.
2. **The guided notes' Primary Objective is filled in, not blank.** State the objectives
   outright, worded as on the cover's learning targets, identical in `notes/` and `notes_key/`.
   Only that box changed — vocabulary, hook response, and in-lesson blanks stay fill-in.
   `references/components.md` in the skill was updated to match.

## Current state

- **Structure (user-approved 2026-08-04):** 8 units, Algebra (U1–3) → Data (U4–6) → Trig
  (U7–8). Every unit has a **Lesson X.0 unit opener** (hook + prerequisite diagnostic +
  vocab preview + roadmap, no new content). 59 lessons total. Full lesson maps with standard
  codes live in `spec/algebra_trig_data_analysis.md` ("The lesson maps"). The restructure and
  the scaffolds are merged to `main` (commits `b8addef`, `99a8c19`).
- **Authored (16 of 59): `unit01/lesson00`–`unit01/lesson07` and
  `unit02/lesson00`–`unit02/lesson07`.** Every component written, built, and gated. **Units 1 and 2
  are both complete end to end** — 8 lessons + unit cover pair + two parallel test forms + two keys
  each. **Unit 3 is the next unit to author** and has no lessons yet.
- **`unit02/unit_cover/` + `unit_cover_key/` and `unit02/tests/` + `test_keys/` — Unit 2's summative
  layer. This is the first unit test built for a GRAPH-READING unit, and its shape should be
  reused for every later graph unit.**
  - **The cover follows Unit 1's shape exactly** (banner → overview → 8-row lesson table → five big
    ideas → test-blueprint remindbox; `body.tex` `\input` by both wrappers so page 1 cannot drift).
    Unit 2's five big ideas are the unit's five error streaks made explicit: *say which axis the
    number came from* (2.4), *did the outputs change or the inputs* (2.2), *getting closer is not
    arriving* (2.5), *a rule owns only its own stretch* (2.6), and *a family is chosen by how the
    outputs change, not by shape* (2.7).
  - **Blueprint, 100 pts, four parts** — same as Unit 1 but re-spined for graph reading: A vocabulary
    matching 8×1 (10 definitions, **two distractors**: a *dilation* and a *$y$-intercept*); B multiple
    choice 6×2; C short answer 10×5, **one item per content lesson 2.1–2.7 in lesson order**, then
    three synthesis items (interval notation + a doubly-restricted domain; `AF.1e` answered
    algebraically *and* graphically; the characteristics checklist off an equation); D extended
    response 2×15.
  - **Part B is six items for the unit's six error classes, in lesson order**, so the miss pattern is
    a diagnosis rather than a score: flipped notation (2.1), the backwards horizontal shift (2.2),
    the axis error (2.4 — every option is in dollars, so units cannot settle it), approaches-is-not-
    reaches (2.5), a corner is not a break (2.6), and ``it curves upward'' (2.7).
  - **Part D is the two prompts the unit earned.** D1 reads *one* piecewise-linear profit graph
    completely (domain/range, both zeros, three intervals, the extreme, then a judgement) — and its
    assessed idea is that **the maximum sits on a flat stretch, so its location is an interval**
    ($[7,10]$ P / $[6,9]$ A), which is where students name one endpoint. D2 is choose-justify-use-
    then-know-the-limit: three difference/ratio rows, the model, a prediction, **the student whose
    arithmetic is right and whose conclusion is wrong**, and an extrapolation question.
  - **Parallel forms.** Practice: shares $8,24,72,216$ (ratio 3), $S(d)=8\cdot3^d$, $S(15)=114{,}791{,}256$;
    profit graph $(0,-4),(4,0),(7,6),(10,6),(14,-2)$, zeros $4$ and $13$. Actual: rumor
    $5,20,80,320$ (ratio 4), $N(h)=5\cdot4^h$, $N(12)=83{,}886{,}080$; profit graph
    $(0,-6),(3,0),(6,9),(9,9),(13,-3)$, zeros $3$ and $12$. Vocabulary definitions are reworded and
    relettered **and the multiple-choice options are reordered**, so no answer letter transfers
    (P: 1--B, 2--C, 3--D, 4--B, 5--C, 6--D; A: 1--A, 2--B, 3--A, 4--C, 5--A, 6--B). That is a
    deliberate change from Unit 1, which kept the MC letters identical.
  - **Five pre-drawn `pgfplots` figures (C4, C5, C6, C9, D1) and no sketching anywhere.** That is the
    AFDA guidance's own scope, and it is why this test runs **6 pages** against Unit 1's 4. A shared
    `\pgfplotsset{testaxis/.style={...}}` is defined identically in all four files. Every read lands
    on a gridline; the C4 graphs were designed backwards from integer zeros (check each segment's
    slope divides evenly before drawing).
  - **`\workrowsep` sweep, and the counter-case to Unit 1.** At 6pt the test ran 6 pages with page 6
    holding only D2(c) and D2(d). The sweep gave **6 pages at 5, 4 and 3pt and 5 pages only at 2pt** —
    and 2pt is far too little handwriting room for a Part C of ten computations. **Unit 1's rule
    ("reach for `\workrowsep` before a guard") still holds as a rule, but here it had no acceptable
    setting**, so the room stayed at 6pt and the pagination was fixed with guards instead.
  - **Boxguard findings — three real violations, all invisible to every page count** (parity was a
    perfect 6/6 throughout, because each key stranded exactly what its blank stranded).
    (1) **Part C item 4's stem sat alone at the foot of p2** — the two lines that define what $A(t)$
    *means*, and that $A<0$ is below the platform — with the figure and all four questions opening
    p3. A student reading the context on one page and answering on the next; same class as 2.4 item
    4, 2.5 item 8, 2.6 item 4. Fixed with `\boxguard[16]` (stem + the 5.2cm axis); cost nothing.
    (2) **Part C item 10's stem sat at the foot of p4 with its whole five-row work block opening p5**
    as an unlabelled blank strip above the Part D banner — five answers written on a page showing no
    question. `\boxguard[14]`; cost nothing. **This is a new defect shape worth watching for: in the
    blank the work block is a `\vphantom`, so a split answer space is literally invisible until you
    look at the rendered page.** (3) **Page 6 held only D2(c) and D2(d)**, ~1.5in on an otherwise
    blank page; `\boxguard[26]` sends item 2 over whole, so p5 and p6 now each carry one complete
    extended-response item. All three guards are mirrored byte-identically in the keys, with the
    reason in a comment in each file.
  - **No `teachernote` in any of the four test files** — the practice test is published to
    `sample_test/` and rides in the **student** packet. Both forms' rationale, the three named Part C
    deductions, and the Part D rubrics are on `unit02/unit_cover_key/` page 2 (key packet only).
  - `make -C unit02/tests all` and `make -C unit02/test_keys all` publish
    `unit02/sample_test/main.pdf` and `unit02/sample_test_key/main.pdf`. **Those two PDFs are build
    outputs that must be committed** — `unit.mk` reads them from the source tree.
- **`unit02/lesson07` — Choosing and Comparing Models in Context (`AFDA.AF.1c, e, g`;
  `AFDA.AF.2h`).** Unit 2's **closing lesson**, and the only one whose content is a *decision
  procedure* rather than a reading skill.
  - Spine: **the family is chosen by how the outputs \emph{change}, not by what the graph looks
    like.** The second sentence is **``it curves upward'' rules out linear and nothing else** — that
    single confusion is the hook, the exit ticket's item 3, Tier E item 1, and homework item 3. The
    habit installed is 2.6's ``which piece owns this input?'' generalized: **which family owns this
    situation, and what would have to be true for a different one to fit?**
  - **The hook is a new \emph{mechanism} for the seventh lesson running, and it is about evidence.**
    A school video runs $3, 6, 12, 24$ thousand views over days $0$–$3$. Student A: the jumps are
    $3, 6, 12$, they keep growing, a parabola's jumps grow too, so quadratic. Student B: each day
    doubles, so exponential. **Everything both said about the numbers is literally true** — and A
    checked something that is not \emph{enough}. Resolve on notes box 1 after all three tables are
    filled, never earlier. 2.6's hook turned on \emph{where a rule lives}; this one turns on
    \emph{what counts as evidence}.
  - **The plants from 2.0/2.2/2.6 all land.** 2.0's adding-vs-multiplying test (restated in 2.2's
    notes box 1) is the ratio test with the vocabulary withheld; 2.6's homework item 10 — the four
    stories, and *which two could be confused from part of the graph* — is the warm-up's item 1 and
    the whole lesson in miniature; 2.5's coffee returns twice (Tier A graph (c), and Tier E item 3).
  - Notes = 5 vocab terms (mathematical model, first differences, second differences, common ratio,
    extrapolation) + three boxes + practice. **`mathematical model` is the SOL's own phrase**
    (`AFDA.DA.1d`), which is what licenses the extrapolation caution inside AFDA scope; the term is
    *not* in the AFDA guidance, so it is taught plainly and never assessed for its own sake.
  - **Box 1 is three tables filled before anyone says a family name.** (a) rideshare fare
    $3,5,7,9$; (b) braking distance $20,45,80,125$ at $v=20,30,40,50$; (c) a shared post
    $5,15,45,135$. Each gets a first-difference, second-difference, \emph{and} ratio row, so the
    pattern — exactly one row constant per table, every other row not — is only visible with all
    three on the page. **If you let the class classify (a) as soon as it is filled, the pattern is
    lost.** (b) deliberately steps by $10$: **equal steps, not unit steps**, is the condition that
    gets skipped.
  - **Box 2 is the unit's summary sheet** (`AF.1g` + `AF.2h`): parent, table test, graph shape,
    inc/dec, max/min, asymptote, end behavior, and what the story says, across all three families.
    Every cell is 2.2, 2.4, or 2.5, so it fills fast. Tell students to keep it for the unit test.
  - **Box 3 is `AF.1e` done explicitly both ways** — $V(5)=96$ algebraically, the $50$-thousand
    crossing graphically — with the instruction to *name which method you are using*, because
    students do not notice they have done two different things. It closes on $V(20) \approx 3.1$
    billion views: **the model is not wrong, it is being read outside its window.**
  - **Two ideas that generate the most argument, both worth the time.** (1) *Two points are never
    enough* — Tier A item 5 draws a line and an exponential through $(0,4)$ and $(1,8)$; groups will
    try to pick a model, and the item has no model-picking answer, only a \emph{measurement} answer
    (count day 2: $12$ vs $16$). (2) *Three points never rule out a quadratic* — the homework
    extension gives a tree at $3, 6, 12$ feet with $Q(x)=1.5x^2+1.5x+3$ and $E(x)=3\cdot2^x$ fitting
    **all three exactly**, differing by $3$ feet at year $3$ and $2{,}904$ feet at year $10$.
  - **Tier E item 3 is the sharpest item in the lesson and the honest answer to ``why does the ratio
    test fail on real data.''** 2.5's coffee runs $84, 52, 36, 28, 24, 22, 21$; its ratios are
    $0.62, 0.69, 0.78, \dots$ — not constant. Subtract room temperature and the **gap** is
    $64, 32, 16, 8, 4, 2, 1$, ratio exactly $0.5$. Still exponential: a vertical translation up $20$
    (2.2) that carries the asymptote with it (2.5), and the asymptote *is* room temperature.
  - **Homework items 6–9 are the argument for the lesson.** Two \$24{,}000 trucks: L written down by
    a fixed \$3{,}000/yr (linear), E by a fixed $20\%$/yr (exponential). L is worth more in years
    $1$–$5$, they cross between years $5$ and $6$, and at year $8$ L's model says **\$0** — false of
    any truck that runs — while E approaches \$0 and never arrives. **Item 9's buyer has the numbers
    right and the \emph{question} wrong:** ``holds its value better'' has no answer until a time
    horizon is named. Grade on whether one is named.
  - Exit ticket = a gym at $64, 96, 144, 216, 324$ (ratio $1.5$). **Items 1 and 3 are built on the
    same observation on purpose**, the 2.4/2.5/2.6 pattern used a fourth time: noticing the growing
    jumps is *correct* in item 1 and the *wrong conclusion* in item 3. Item 2 predicts months $5$ and
    $6$ ($486$, $729$) against a building licensed for $500$.
  - Guard sizes: bare on vocab, `[12]` hook, `[30]`$\times$3 on the notesboxes, `[30]` practice,
    `[30]` on all three activity tiers, `[24]`/`[30]`/`[24]`/`[26]` on the homework's boxes, `[18]`
    on the plan's five teachernotes, `[16]` on the plan's Individual Work box, bare on the plan's
    Lesson, Explicit Instruction and Group Work boxes. **2.4's set has now transferred verbatim for
    the fourth lesson running, clean on the plan first pass.**
  - **Boxguard findings — four real violations, and the worst stub the course has produced.**
    (1) **Activity p4 held a single write-line** and nothing else: Tier E overran p3 by one line plus
    the box's closing rule. `\tcbbreak` before Tier E item 3 gives p4 the whole coffee item instead.
    (2) Tier A item 5's stem sat at the foot of p2 with its figure opening p3 — the 2.4/2.5/2.6
    defect class again, fixed with `\tcbbreak`. (3) Homework item 4's stem sat alone at the foot of
    p1 with its whole table on p2 — `\tcbbreak`. (4) Notes box 3 spilled **just its last two lines**
    onto p4; `\tcbbreak` before the day-$20$ paragraph moved a substantial chunk instead. All four
    were invisible to `make check` (each stranded identically in the key, so parity was perfect).
    **The rule this run confirms: a nearly blank page is a boxguard violation, not a page count.**
  - **Key-length finding, and the first time `\ansline` \emph{width} cost a page.** The homework key
    first came out 5 pages against a 4-page blank with **every `\writelines{n}` correctly matched by
    $n$ `\ansline`s** — thirteen of them simply wrapped to two printed lines. Diagnose it by grepping
    `pdftotext -layout` output for answer lines with **no dotted trail** (a wrapped `\ansline` puts
    the trail only on its last line). Two `\ans` table cells were also wider than their `\blank`
    counterparts. The fix is three-part and worth reusing: **trim the long `\ansline`s to one printed
    line, widen the column an `\ans` cell overflows** (in the blank too), and **shorten shared prose
    such as the `remindbox`**, which shrinks the key without costing the blank a page.
  - **Deck defect no check can see, the second in the course.** The comparison-table frame hyphenated
    two cells mid-word (`flat-tens`, `ver-tex`) at projection size. Widening the label column and
    rewording fixed it. `grep Overfull` on the deck log returns **zero** — as it did for 2.6's
    overprint. **Always look at the deck.**
  - Page counts: cover 1, warm-up 1/1, notes 4/4, activity 4/4, exit ticket 1/1, homework 4/4;
    student and key packets **18 pages each**. Plan 6 pp, slides 11 frames (4 pp printed 3-up). No
    overfull box anywhere beyond the structural page banner (6.0pt) and the cover's name row
    (10.77pt), and **none at all in the deck**.
- **`unit02/lesson06` — Piecewise-Defined Functions (`AFDA.AF.2`, esp. `AF.2h`).** The unit's
  **synthesis lesson**: no new characteristic is introduced, the whole `AF.2` checklist is simply run
  once more on a graph that takes more than one rule.
  - Spine: **a piecewise function is one function, not several.** Every question the unit has taught
    gets asked \emph{once}, of the whole thing. The second sentence is **a rule owns only its own
    stretch of the domain** — which is the entire content of the word \emph{piecewise} and the source
    of every wrong answer in the lesson. The habit to install is one question: **which piece owns this
    input?**
  - **The hook is a paycheck, and it is a new \emph{mechanism}, not a new costume.** 2.4's hook was
    settled by naming an axis and 2.5's by \emph{approaches versus reaches}; this one is settled by
    neither. A garden center pays \$12/hr for the first $40$ hours and \$18/hr beyond. For a $45$-hour
    week, student A says $45(12)+5(18)=\$630$ and student B says $40(12)+5(18)=\$570$. **Both used both
    rates and neither made an arithmetic mistake** — A charged the \$12 rate to hours it does not own,
    paying hours $41$–$45$ twice, which is exactly \$60. Resolve on notes box 2 off the graph
    ($P(45)=570$), never earlier.
  - **The two sentences worth the whole lesson.** (1) **A corner is not a break** — a change of
    \emph{rule} is not a hole in the graph, and the guidance's own test settles it (can you draw it
    without lifting your pencil?). (2) **Exactly one filled circle sits above every input, and it has
    to** — the open circles are not a drawing convention, they are 2.1's definition of a function being
    enforced at the seam. Ask ``what is $S(2)$?'' before explaining anything.
  - **Three plants harvested.** 2.5's homework item 10 (the delivery fee, flat \$5 then \$2/mile) is
    reused \emph{unchanged} as notes box 1's opening — the class already answered every part of it in
    plain English, so box 1 supplies only the \emph{name} and the \emph{notation}; 2.1's ``some ranges
    are lists interval notation cannot express'' (the hot dogs) returns as the step function's range
    $\{6,10,16\}$; and 2.1's bracket-versus-parenthesis rule returns as what the dots mean.
  - Notes = 5 vocab terms (piecewise-defined function, piece, boundary point, open/closed circle,
    continuous/discontinuous) + three boxes. In-text blanks: *one*, *domain*, *only that one*, *one*,
    *one*, *one output*, *570*, *B*, *twice*, *owns*, *agree*, *continuous*, *corner*, *break*, *6*,
    *one*, *one output*, *2*, *5*, *discontinuous*, *$\{6,10,16\}$*, *constant*, *no interval*,
    *$0<w\le2$*, *includes*.
  - **Box 3's third surprise is the sharpest idea in the lesson and it generates argument:** the step
    function is **never increasing**. Every piece is constant, and a piece is the only place
    ``increasing'' can be measured; the cost does rise, but it rises \emph{at} the jumps, and a jump
    happens at a single input rather than across an interval. Let the room argue before settling it.
  - **The new wrinkle on `AF.2c` is that an extreme's \emph{location} can be an interval.** 2.4 drilled
    ``a value \emph{and} a location'' and every location so far has been a point. Guided practice's
    drone is at $50$ ft for all of $[5,9]$; Tier R's phone plan sits at its \$30 minimum on all of
    $[0,10]$; the exit ticket's \$40 minimum covers $[0,4]$. Students reliably name one endpoint.
  - **Every context was chosen so the boundary means a different \emph{kind} of thing.** Notes: the
    delivery fee (a mile), the paycheck $P(h)$ (an hour, continuous, corner at $h=40$), shipping
    $S(w)$ (a weight, two jumps, a range that is a list). Guided practice **drone**
    $20t-2t^2 / 50 / 50-10(t-9)$ on $[0,14]$, three pieces, continuous, all reads even. Tier R **phone
    plan** $C(g)$ (\$30 flat then \$5/GB, boundary $g=10$). Tier A **garage** $G(h)=4/7/12$ (steps) and
    a decontextualized $f$: $x^2$ on $[-2,2]$, $-2x+10$ on $(2,6]$. Exit ticket **babysitting**
    $B(h)$ (\$40 flat then \$15/hr). Homework **tiered electricity** $E(k)$ (10¢ then 16¢, boundary
    $500$ kWh) and a **bike-share** in steps.
  - **Tier A item 5 is the item that separates the room, and it pays 2.5 back in a new costume.** The
    open circle at $(2,6)$ means the outputs get as close to $6$ as you like and never reach it, so
    the range is $[-2,6)$ and there is **no absolute maximum** — ``approaches is not reaches'' with a
    *circle* instead of an asymptote. Most groups answer $4$, the biggest filled dot they can point at;
    the prompt that fixes it is ``what is $f(2.1)$?'' Assessed again as homework item 5(a) and 5(d).
  - **Exit ticket items 1 and 3 are the same number on purpose**, the 2.4/2.5 pattern reused a third
    time: naming $h=4$ as the boundary point is the *correct* answer to item 1 and the *wrong*
    conclusion in item 3 (``the graph has a break at $h=4$, because that is where the rule changes'').
    **Item 2 is the second trap** — the minimum's location is the interval $[0,4]$, not a point.
  - **Homework item 9 is the best interpret item in the unit.** A customer doubled usage $500 \to 1000$
    kWh, the bill went \$50 $\to$ \$130, and they are certain they are being overcharged. **The
    arithmetic is right and the \emph{expectation} is wrong**: $500(0.10)=50$ and $500(0.16)=80$, and
    the extra \$30 is exactly $500$ kWh times the six-cent difference. Doubling the input doubles the
    output only when one rate covers the whole range.
  - **Homework item 10 bridges to 2.7** — four stories, one family each (gym → linear, bacteria →
    exponential, thrown ball → quadratic, tiered tax → piecewise) plus the real question: **which two
    could be confused from part of the graph?** The gym and the tax, because below the boundary the tax
    graph *is* a straight line. *Model* is 2.7's word.
  - **The extension introduces $|x|$ honestly** as $-x$ for $x<0$ and $x$ for $x \ge 0$ — a V, continuous
    at $0$, minimum $0$ at the corner, climbing without bound at both ends. It adds no parent to the
    required list and it is the cleanest possible statement of ``a corner is not a break.''
  - Guard sizes: bare on vocab, `[12]` hook, `[30]`$\times$3 on the notesboxes, `[30]` practice,
    `[30]` on all three activity tiers, `[24]`/`[30]`/`[24]`/`[26]` on the homework's boxes, `[18]` on
    the plan's five teachernotes, `[16]` on the plan's Individual Work box, bare on the plan's Lesson,
    Explicit Instruction and Group Work boxes. **2.4's set transferred verbatim for the third lesson
    running, clean on the plan first pass.**
  - **Boxguard finding, and the fourth lesson running where `\tcbbreak` was right on the first build.**
    Homework item 4's stem \emph{and its whole graph} sat at the foot of p1 with the question and all
    four write-line slots opening p2 — a student answering on one page while the figure they must read
    is on the previous one. Same defect class as 2.4's item 4 and 2.5's item 8, and again invisible to
    `make check` (the key stranded the same way, so parity was perfect at 4/4). `\tcbbreak` before
    item 4 **cost nothing**: still 4 pages, and it *filled* p4, which had been ~45% empty. Still no
    `\tcbbreak` authored before a build proved one necessary.
  - **Pagination verdict, measured and recorded in comments in both files.** After the `\tcbbreak`,
    homework p2 ends ~55% full with the electricity box opening p3. Lowering that box's guard `[30]`
    $\to$ `[22]` was tested and **changed nothing at all** — the box's first unbreakable chunk
    (scenario paragraph + the 4.4cm figure, ~2.9in) is larger than p2's free space, so the break is
    natural and the guard is not the lever. Restored per 1.5's test-then-restore rule.
  - **A slide-deck defect that no log reports, and the first of its kind in this course.** On the
    notation frame, a `\vspace{-0.2cm}` between a `\[...\]` display and the paragraph beneath it made
    the paragraph's **first two lines overprint each other** — with `grep Overfull` on the deck log
    returning **zero**. The rule: **never pull text up under a display on a Beamer frame** (the
    display's depth is already absorbed by `\belowdisplayskip`); shrink the figure instead. This is
    also the standing argument for eyeballing the *deck*, not just the components.
  - **Open/closed circles in pgfplots**, the pattern to reuse for every step function from here on:
    filled is `\addplot[royal, only marks, mark=*, mark size=1.9pt]`, open is the same with
    `mark options={fill=white}`. Both belong in the **blank** (they are the data students read), so
    `keyred` marks are added only where the key supplies a *reading*, never on the dots themselves.
  - Page counts: cover 1, warm-up 1/1, notes 5/5, activity 3/3, exit ticket 1/1, homework 4/4;
    student and key packets 20 pages each. Plan 6 pp, slides 11 frames (4 pp printed 3-up). No
    overfull box anywhere beyond the structural page banner (6.0pt, identical in verified 2.5) and the
    cover's name row, and **none at all in the deck**.
- **`unit02/lesson05` — End Behavior and Asymptotes (`AFDA.AF.2f–g`).** The lesson where **four
  lessons' worth of plants get harvested at once**, and the only one in the unit whose whole content
  is a distinction rather than a procedure.
  - Spine: **getting closer and closer is not arriving.** That is the honest answer to the objection
    2.4's log flagged ("but it gets so close"), and it is what makes ``none'' the correct answer to so
    many questions. The second sentence is **an asymptote is a \emph{line}, so it gets an equation** —
    the third member of 2.4's set (an intercept is a point, a zero is a number, an asymptote is a
    line). Drill it out loud every single time; it is the habit the rest of the year runs on.
  - **The hook's design is deliberately \emph{not} 2.4's.** 2.4 was settled by naming an axis; this one
    cannot be settled that way, because both students are talking about degrees. The coffee gap runs
    $64, 32, 16, 8, 4, 2, 1$ and the question is *does it ever reach $20^\circ$C?* Student A: after 12
    hours the gap is $\tfrac{1}{64}$ of a degree and no thermometer can read it. Student B: half of a
    positive number is positive, so it is never zero. **Neither is wrong about a fact** — they answered
    \emph{different questions}, and only B answered the one asked. A is right about \emph{measuring},
    which is a claim about instruments, not about $C$. Students trained for a week to check units will
    want a units answer and there is not one. Resolve it on notes box 2 rule 2, not earlier.
  - **Four plants harvested, and this is the payoff lesson for all of them**: 2.0's homework item 9
    table for $f(x)=\frac{x+1}{x-3}$ ($-39, -399, 401, 41$) is reused \emph{unchanged} as notes box 3's
    opening — the class already made those numbers, box 3 only supplies the picture; 2.1's excluded
    value becomes the vertical asymptote (**the excluded input \emph{is} the answer**); 2.2's
    $(0,\infty)$ range and 2.4's "no zeros" for $2^x$ are both explained by one fact about its left end;
    and 2.4's homework item 10 coffee becomes the hook and notes box 2.
  - Notes = 5 vocab terms (end behavior, horizontal asymptote, vertical asymptote, approaches $\to$,
    without bound) + three boxes. In-text blanks: *right*, *left*, *without bound*, *level off*, *0*,
    *positive*, *never*, *closer and closer*, *reaching*, *end behavior*, *positive*, *20*, *zeros*,
    *minimum*, *$(20,84]$*, *without bound*, *domain*, *except 3*, *no point*, *3*, *0*, *$-1$*,
    *no value at all*, *1*.
  - **Box 1's form of answer matters more than the answers.** Two questions ($x \to -\infty$,
    $x \to \infty$), **three** possible phrases each: climbs without bound, falls without bound, levels
    off toward a number. Panels $x^2$ / $2x-4$ / $2^x$; **panel (c)'s left end is the only new thing in
    the box** and it is what closes the 2.2/2.4 loop.
  - **Box 2's gap row is the definition written in numbers** — fill $64, 32, 16, 8, 4, 2, 1$
    \emph{before} defining anything, and the class will not need the definition read to them. Its best
    five minutes are the **three consequences settled by one line**: no zeros, no absolute minimum, and
    range $(20,84]$ with a parenthesis — all three questions the class already asked about this exact
    graph. Closes on the travelling asymptote ($2^x \to y=0$; $2^x-4 \to y=-4$; $64(0.5)^t+20 \to
    y=20$).
  - **Box 3's sharpest idea — and the best single sentence in the lesson — is that a zero and a
    vertical asymptote are opposites.** Both make you point at a spot on the horizontal axis. At a zero
    the function \emph{has} a value and it is $0$ ($x=-1$ here); at a vertical asymptote it has
    \emph{no value at all} ($x=3$). Ask **"what is $f(3)$?"** before explaining anything — there is no
    such number, and that one fact generates all three rules, including why nothing can cross a
    vertical asymptote (there is no point there to cross with). The same graph carries a horizontal
    asymptote $y=1$, which is why `AF.2g` says "and/or."
  - **Guided practice is the booster club's $A(x)=6+240/x$ — 1.7's and 2.1's own function, harvested a
    third time**, now as the one context where \emph{both} kinds of asymptote mean something: $y=6$ is
    the printing cost with the \$240 setup split ever thinner and never gone, and $x=0$ is "you cannot
    split a setup fee among zero shirts." Reads all integers: $30, 18, 12, 10, 8$ at $x=10,20,40,60,120$.
    Item 4 ("we can get it down to \$5") is the payoff — **\$5 is \emph{below} the asymptote, so it is
    impossible, not merely hard.** Note the vertical asymptote sits on top of the vertical axis; that is
    normal for average cost and worth saying out loud rather than hiding.
  - **Every context was chosen so the asymptote is a different \emph{kind} of thing.** Tier R **drug**
    $D(t)=64(0.5)^t$ (floor at $y=0$; "out of your system in 24 hours" is false as written and still
    good advice — the hook's distinction in a second costume). Tier A **typing speed**
    $S(w)=80-64(0.5)^w$ (ceiling at $y=80$) and **$h(x)=4/(x+2)$** (both kinds, and the parent $4/x$
    moved left 2). Exit ticket **warming soda** $T(t)=72-64(0.5)^t$ (ceiling $y=72$). Homework
    **reservoir** $R(w)=100-64(0.5)^w$ (ceiling $y=100$) and **$h(x)=6/(x-2)$**.
  - **Tier A item 2 is the item that separates the room**: "will they ever type 80? 85?" Both answers
    are no and **the reasons are different** — 80 is approached and never reached; 85 is on the far
    side of the asymptote entirely. Groups reliably give one reason twice.
  - **Tier A item 5 pays 2.2 back and is the cleanest transformation item in the unit.** Sliding
    $4/x$ left 2 moves the \emph{vertical} asymptote ($x=0 \to x=-2$) and leaves the horizontal one at
    $y=0$: a horizontal slide changes inputs, and a vertical asymptote is named by an input. Same rule
    assessed again in homework item 2 ($2^x+3, 2^x-1, 2^{x+4}, -2^x$ → $y=3, y=-1, y=0, y=0$) and
    Tier E item 3.
  - **Exit ticket items 1 and 3 are the same number on purpose**, the 2.4 pattern reused: $72$ and
    $y=72$ are \emph{correct} answers to item 1 and wrong ones in item 3 ("the soda reaches $72^\circ$
    at $t=5$, the graph is on the line"). At $t=5$ the gap is $2^\circ$ and the curve looks welded to
    the line. **Item 2 is the second trap and it flips the period's rhythm** — everything all day has
    answered "no maximum" or "no minimum," and here there is a genuine absolute minimum ($8^\circ$F at
    $t=0$) sitting at the left endpoint. Students answer from rhythm and miss it.
  - **Homework item 5 has a sting in the tail that is worth stealing for later lessons**: after three
    questions about the input that is \emph{missing} from the domain, it asks why the graph has no
    $y$-intercept — and it has one, at $(0,-3)$. **A vertical asymptote deletes one input, not the
    whole axis.** Expect students to answer the question they were primed for.
  - **Homework item 10 bridges to 2.6 and needs no asymptote at all.** A delivery fee, flat \$5 for
    three miles then \$2 a mile ($F(2)=5$, $F(6)=11$), takes **two rules on two stretches with a
    hand-off at $m=3$** — and part (d) checks that outputs climbing without bound rule a horizontal
    asymptote \emph{out}. *Piecewise* is 2.6's word.
  - **The extension is the honest limit of the whole lesson**: $2^x$ against $x^2$ for
    $x=1,\dots,5,10$. They tie at $x=2$ and $x=4$, $x^2$ leads at $x=3$ ($9>8$), and by $x=10$ it is
    $1024$ against $100$. **Same end behavior, wildly different graphs** — end behavior tells you the
    direction, never the rate. That is also Unit 3's opening argument.
  - Guard sizes: bare on vocab, `[12]` hook, `[30]`$\times$3 on the notesboxes, `[30]` practice,
    `[30]` on all three activity tiers, `[24]`/`[30]`/`[24]`/`[26]` on the homework's boxes, `[18]` on
    the plan's five teachernotes, `[16]` on the plan's Individual Work box, bare on the plan's Lesson,
    Explicit Instruction and Group Work boxes. **2.4's set transferred verbatim and clean first pass.**
  - **Boxguard finding, and the third lesson running where `\tcbbreak` was right on the first build.**
    Homework item 8's stem plus **two** of its three write-line slots sat at the foot of p2 with the
    third opening p3 — the same defect class as 2.4's item 4, and again invisible to `make check`
    (the key stranded the same line, so parity was perfect at 4/4). `\tcbbreak` before item 8 **cost
    nothing**: still 4 pages, and p3 now opens with item 8 whole. Note this still does not repeal
    2.0's rule — no `\tcbbreak` was authored until the build proved one necessary.
  - **Two table defects no check and no page count can see, and they are the same family as 2.4's.**
    (1) Notes box 1's label column at `p{1.5cm}` broke "(b) $y=2x-4$" as "(b) $y=$ / $2x-4$" —
    **a label column narrow enough to wrap breaks in the wrong place**; `p{2.3cm}` fixed it. (2) Notes
    box 2's travelling-asymptote header "Horizontal asymptote" at `\small` wrapped **mid-word** as
    "asymp-/tote" in `p{3.2cm}`; the fix is 2.4's rule generalized — **any two-word header near its
    column width needs an explicit `\newline`**, not just a parenthetical one.
  - Pagination: notes pp. 2–5 each run ~55–60% full, and per 2.4's measured verdict that is arithmetic,
    not slack — every box here exceeds half a page, so no two can share one. Activity p3 (Tier E
    complete) and plan p6 (one complete teachernote) are dead space, accepted per 2.3's rule.
  - Page counts: cover 1, warm-up 1/1, notes 5/5, activity 3/3, exit ticket 1/1, homework 4/4;
    student and key packets 20 pages each. Plan 6 pp, slides 12 frames (4 pp printed 3-up). No
    overfull box anywhere over 10.8pt (the standard page banner), and **none at all in the deck**.
- **`unit02/lesson04` — Intercepts, Zeros, and Extrema (`AFDA.AF.2b–d`).** Unit 2's **first pure
  graph-reading lesson** — no equation is needed anywhere in the activity or the exit ticket.
  - Spine: **every mistake in this lesson is an axis mistake, so before you write a number down, say
    which axis it came from.** An interval of *inputs* and a stretch of *outputs* can be the same two
    numbers, in the same units, and mean different things. The second sentence is **2.0's rule
    finally gets its notation: an extreme is a value \emph{and} a location** — which is `AF.2c`'s own
    wording ("the location and value").
  - **The hook is the best one in the unit so far, because the units do not save you.** It reuses
    2.3's homework yearbook curve (profit \$0 at \$0 and \$60, peak \$1800 at \$30) and asks *over
    which prices is profit going up?* Student A answers "from $0$ to $1800$," student B "from $0$ to
    $30$." **Neither made an arithmetic mistake and all four numbers are dollars**, so the only thing
    that distinguishes the answers is which axis they were read from. **Do not resolve it before
    notes box 2** — the interval table makes the resolution obvious instead of asserted, and it is
    rule 1 of that box.
  - **2.3's homework item 10 was the plant and it paid**: the class already answered all three of
    today's questions about that curve in plain English, so 2.4 opens by *naming* what they produced.
    Third consecutive lesson using that move (2.2 named 2.1's translation, 2.3 named 2.2's parentheses).
  - Notes = 5 vocab terms (zero of a function, $x$- and $y$-intercept, increasing/decreasing/constant,
    turning point, absolute max and min) + three boxes. In-text blanks: *vertical*, *0*,
    *horizontal*, *0*, *zero*, *output*, *input*, *input*, *horizontal*, *B*, *strictly*, *strictly*,
    *value*, *location*, *entire domain*.
  - **Box 1's three panels are chosen for two traps, not for variety**: $y=2^x$ has **no zeros at
    all** (most of the room believes every graph crosses the axis — kill it here, and the objection
    "but it gets so close" is the sentence 2.5 is built on), and $y=3-x$ has **$y$-intercept $3$ and
    zero $3$**, the same number meaning nothing alike. Ask what the bare number $3$ tells you.
  - **Box 2's figure is a twelve-hour temperature graph** $(0,2),(2,2),(5,-4),(9,4),(12,1)$ — it
    carries a constant stretch, two decreasing stretches, one increasing, **two zeros ($t=3$, $t=7$)
    that together give an interval of time below freezing**, and an interior max and min. Every read
    is on an integer gridline. **Two zeros producing an interval is what zeros are \emph{for}** and
    is the box's closing line.
  - **Box 3's argument is two panels of the same rule $y=x^2$, on domains all-reals and
    $-1 \le x \le 3$.** Nothing about the curve moves and the restricted version has an absolute
    maximum ($9$ at $x=3$) it did not have. Ask *which point of this curve moved when I cut the
    domain?* before explaining anything. This is the cleanest statement in the unit that **the domain
    is part of the function**.
  - **Every context deliberately puts an extreme somewhere students will not look.** Guided practice
    **cistern** $(0,6),(3,0),(5,4),(6,4),(7,7)$: max $7$ ft at the *last* endpoint, so "the water was
    highest at the start of the week" is false. Tier R **gym** $(0,10),(1,10),(4,40),(6,0)$: zero =
    closing time. Tier A **start-up profit** $-(x-4)^2+9$ on $[0,8]$: zeros $1$ and $7$ are
    *break-even months*, max \$9000 at month 4, and **the minimum $-7$ happens at two locations**
    ($x=0$ and $x=8$) — where groups reliably stop early. Exit ticket **creek** $(0,6),(3,-3),(7,9)$:
    zeros $2$ and $4$, max at an endpoint. Homework **bike share**
    $(0,12),(3,0),(5,8),(8,8),(12,0)$: max at an endpoint *and* the minimum $0$ twice.
  - **Tier A item 4 is four "none" answers in a row** ($2^x+1$: no zeros, no absolute max, no
    absolute min, one interval). Tell groups in advance that "none" is a legitimate answer that needs
    a reason, or they will assume they misread the question.
  - **Tier E item 2 is the share-out**: cut the start-up's domain to months 5–8 and **three things
    change at once** — a zero disappears, the minimum moves to an endpoint, and a maximum appears —
    with the curve untouched. Part (c) ("what would the buyer believe that is false?") is the sentence
    to get on the board before the exit ticket.
  - **Exit ticket items 2 and 3 are the same two numbers on purpose**, the 2.3 pattern reused: item 2
    makes $-3$ and $9$ correct answers (the extremes), item 3 shows them failing "increasing from
    $-3$ to $9$." A student who accepts item 3 because it matches what they just wrote has told you
    exactly what they are doing. **Item 2's maximum sitting at an endpoint is the second trap** —
    students trained on parabolas hunt for the turn and report the minimum as the maximum.
  - **Homework item 10 bridges to 2.5 and produces a genuine "no absolute minimum."** Coffee cooling
    in an insulated flask, $C(t)=64(0.5)^t+20$, giving integer reads $84, 52, 36, 28, 24, 22, 21$.
    Domain is $t \ge 0$ while the graph shows six hours — **that gap is deliberate**, and students who
    answer $21^\circ$ have read the edge of the picture instead of the domain. Then: what number do
    they approach, and does the graph reach it? *Asymptote* and *end behavior* are 2.5's words.
  - Extension: $y=x^2-4$ on all reals, then on $1 \le x \le 4$ (reads $-3, 0, 5, 12$) — one zero
    instead of two, the minimum moved from $-4$ at the turn to $-3$ at an endpoint, and a maximum of
    $12$ appeared. **One domain change, three consequences, and the rule never touched.**
  - Guard sizes: bare on vocab, `[12]` hook, `[30]`$\times$3 on the notesboxes, `[30]` practice,
    `[30]` on all three activity tiers, `[24]`/`[30]`/`[24]`/`[26]` on the homework's boxes, `[18]` on
    the plan's five teachernotes, `[16]` on the plan's Individual Work box, bare on the plan's Lesson,
    Explicit Instruction and Group Work boxes. That is 2.3's set transferred, and it was clean on the
    plan first pass.
  - **Boxguard finding, and the second lesson running where `\tcbbreak` was right on the first
    build.** Homework item 4's stem and its (a)–(d) list sat at the foot of p1 with **one** of its
    four write-line slots, the other three opening p2 — an answer a student starts at the bottom of
    one page and finishes at the top of the next. `\boxguard` is inert inside a breakable
    `tcolorbox`, so `\tcbbreak` is the only lever, and here **it cost nothing**: still 4 pages, and p2
    improved from *two orphan write-lines* to *items 4 and 5 plus the whole bike-share box*. Note
    this still does not repeal 2.0's rule — no `\tcbbreak` was authored until the build proved one
    necessary.
  - **A table defect no check and no page count can see: a multi-word header wrapping
    mid-parenthesis.** Notes box 1's header `\textbf{$y$-intercept (a point)}` at `\small` overran
    `p{3.0cm}` and broke as "$y$-intercept (a / point)". **Break a two-part header explicitly with
    `\newline` and widen the column** rather than letting it wrap: `\textbf{$y$-intercept}\newline
    \textbf{(a point)}` in `p{3.4cm}`. The general rule — **any header carrying a parenthetical
    qualifier needs an explicit break** — belongs with 2.1's `X`-on-the-prose-column finding.
  - **Pagination verdict, measured and recorded in comments in both files.** Notes runs 5 pages with
    pp. 2–5 each about 60% full, and that is the natural break, not slack: **each of the four boxes is
    taller than half a page** (~5.5in, ~6.5in, ~6in, ~5.5in against ~9in of column), so no two can
    share one. Lowering box 2's guard to let it start on p2 was measured and rejected — p2 has ~2.5in
    free and box 2's first unbreakable chunk (intro line + the 5.4cm axis) is ~2.9in, so it would
    strand the intro line alone. **When every box exceeds half a page, a half-empty page is arithmetic,
    not a guard problem** — measure the boxes before reaching for a guard.
  - Homework p4 (extension + remindbox, ~4.5in of real content) and plan p6 (two complete
    teachernotes) are dead space rather than boxguard violations, both accepted per 2.3's rule.
  - Page counts: cover 1, warm-up 1/1, notes 5/5, activity 3/3, exit ticket 1/1, homework 4/4;
    student and key packets 20 pages each. Plan 6 pp, slides 12 frames (4 pp printed 3-up). No
    overfull box anywhere over 10.8pt (the standard page banner), and none at all in the deck.
- **`unit02/lesson03` — Equations and Graphs in Both Directions (`AFDA.AF.1d, f`).** Unit 2's
  first both-directions lesson, and **the course's first technology lesson.**
  - Spine: **2.2 asked students to *describe* a move they were shown; 2.3 asks them to *produce* the
    other representation.** That is why `1d` and `1f` are one lesson — they are the same translation
    run in opposite directions. The second sentence is **"verify" is the standard's own word, and
    verify means check, not decide.**
  - **The best idea in the lesson: a matching picture is not proof.** $y=(x-3)^2$ and
    $y=(x-3)^2+0.5$ differ by half a unit everywhere, which on a screen showing $-10$ to $10$ in
    ~$63$ pixel rows is one or two pixels — the two look identical and are different functions. Only
    a substitution settles it. This is stated in notes box 3, framed on its own deck slide, and
    assessed as Tier E item 3. It is the lesson's answer to "the calculator said so."
  - **Hook is a typing error, and it is 2.2's spine wearing keystrokes.** Two students are told to
    graph $2^x$ moved right $5$; A types `Y1=2^X-5`, B types `Y1=2^(X-5)`. 2.2's outside-or-inside
    question is now literally *did you type the parentheses*. Resolved with one number: right $5$
    means the image at $x=5$ shows the parent's $2^0=1$; A gives $27$, B gives $1$.
    **Deliberately no vote this time** — 2.2's hook spent the vote, and today's point is the
    opposite one (you do not need consensus, you need a number). The plan says so explicitly.
  - **Warm-up item 2 is the hook planted** ($2^x-5$ vs $2^{x-5}$ at $x=5$, giving $27$ and $1$) and
    the teachernote says to score it and stop — resolving it kills the hook. Item 1's table for
    $(x-2)^2$ is not filler: it is the same arithmetic notes box 1 asks for, done once with no
    transformation language attached. Item 3(c) ($-x^2$) is the negative-key trap in advance.
  - **The no-sketching rule was satisfied four times and the pattern is now settled**: a pre-drawn,
    pre-scaled grid with **the parent already plotted**, a table of image points to complete, and
    "plot your five points and join them." Used in notes box 1, activity Tier R, exit ticket item 1,
    and homework item 2. **The key adds the image curve plus `only marks` dots inside the same
    axis** — identical axis dimensions, so parity is free. Reuse this verbatim for 2.4–2.7.
  - **Grids meant for plotting need a gridline at every integer**; grids meant for *reading* need
    sparse tick labels plus `minor x/y tick num` so values land on a visible line without crowding
    the labels. Both forms are in this lesson (box 1 vs box 2) and the distinction is worth keeping.
  - Notes = 5 vocab terms (anchor point, pre-image and image, transformation form, viewing window,
    substitution check) + three boxes: **equation $\to$ graph** (the anchor routine on
    $y=(x-2)^2-3$, anchor $(0,0)\to(2,-3)$, five points carried, then plotted); **graph $\to$
    equation** (three panels, one landmark each) ; and **the calculator** (the four keys, the hook
    resolved on two panels, three traps, and the not-proof rule). In-text blanks: *anchor*,
    *inside*, *right*, *outside*, *down*, *$(2,-3)$*, *shape*, *vertex*, *asymptote*, *two points*,
    *steeper*, *B*, *parentheses*, *window*, *substituting*.
  - **Box 2's three landmarks are the content of `AF.1d`**: quadratic $\to$ the **vertex**;
    exponential $\to$ the **asymptote** plus the point on the $y$-axis; linear $\to$ **two
    points**. The exponential row is the hard one and the reason is structural — students have been
    trained for a week to hunt for a turning point and an exponential has none. The prompt in the
    plan is *where was that dashed line before it moved?*
  - **The line gets its own honest warning, and it is the guidance's own reason.** The AFDA guidance
    says a linear function's equation "can be determined by two points… or by the slope and a
    point" — because for a line the transformations are *not distinguishable*: $2f(x)$ and $f(2x)$
    are both $y=2x$, and a sideways slide looks identical to a vertical one. 2.2's log flagged both
    coincidences; 2.3 states them out loud and tells students to stop asking which move "really"
    happened. Tier A item 4(c) asks them to justify that.
  - **Finding $a$ is taught as three numbers and three checks**: the vertex gives $h$ and $k$, a
    *second* point gives $a$, and a *third* point checks all three. The insistence that matters is
    **write the equation with $a$ in it, then substitute** — students who substitute first get the
    right $a$ by coincidence and cannot repeat it. Guided practice, Tier A item 1, and homework
    items 4 and 7 all run it.
  - **The three calculator traps, all real and all worth teaching**: (1) the **parentheses**
    (`2^X-5` vs `2^(X-5)`); (2) the **two minus keys** — `(-)` negates, `-` subtracts, and
    `-X^2` gives $-x^2$ while `(-X)^2` gives $x^2$, i.e. the parent again (2.2's warm-up item 3 as
    keystrokes); (3) the **window** — $y=(x-20)^2+900$ shows nothing in ZStandard, and the fix is
    read off the anchor point with no graphing. All three are assessed (homework item 5's keystroke
    matching table, Tier E items 1 and 2).
  - **Every context exists because the graph cannot answer the question**, which is the honest
    motive for wanting an equation at all: guided practice **hoodie** $P(x)=-4(x-20)^2+900$
    (vertex $(20,900)$, zeros $5$ and $35$, $a$ from $(5,0)$) asked at $P(23)=864$ — and $23$ and
    $864$ both fall between gridlines; homework **yearbook** $P(x)=-2(x-30)^2+1800$ (vertex
    $(30,1800)$, zeros $0$ and $60$, $a$ from $(60,0)$) asked at $P(35)=1750$, likewise unreadable.
    "You can't tell" with no mention of gridlines earns nothing.
  - Other verified numbers: box 2 panels $(x+3)^2+2$, $2^x-4$ (zero at $x=2$, asymptote $-4$),
    $2x-3$; the $a$ example vertex $(2,1)$ through $(3,3)$ giving $a=2$, checked at $(4,9)$;
    Tier R $(x+1)^2-4$ ($0,-3,-4,-3,0$) and vertex $(4,0)$; Tier A $3(x-3)^2-2$ (from $(4,1)$,
    checked at $(5,10)$), $2^x+2$ (range $(2,\infty)$), gym $C(x)=15x+40$ from $(0,40)$ and
    $(4,100)$, $C(7)=145$; Tier E window $y=(x-15)^2-40$ (anchor $(15,-40)$, $y=60$ at $x=5$ and
    $25$); exit ticket $(x+2)^2-1$ ($3,0,-1,0,3$) and $2^x-3$; homework $(x-3)^2-2$ ($2,-1,-2,-1,2$),
    vertex $(1,2)$ through $(2,5)$ giving $a=3$ checked at $(3,14)$; extension $-2(x-4)^2+8$ (zeros
    $2$, $6$) and the same with $a=-\tfrac12$ (zeros $0$, $8$).
  - **Exit ticket items 2 and 3 are the same expression on purpose, and it is the sharpest
    assessment design in the unit so far.** Item 2's *correct* answer is $y=2^x-3$ (asymptote $-3$,
    through $(0,-2)$); item 3 shows those identical keystrokes *failing* the instruction "moved right
    $3$" ($2^3-3=5$, not $1$). A student cannot pattern-match through both, and one who marks item 3
    correct because it matches what they just wrote has told you exactly what they are doing.
  - **Homework item 10 bridges to 2.4 and deliberately needs no new equation** — it re-asks the
    yearbook graph for its zeros, its absolute maximum *with location*, and the two stretches where
    profit rises and falls, all in plain English. *Zero*, *absolute maximum*, and *increasing
    interval* are 2.4's words. The one thing to insist on is **2.0's rule that an extreme is a value
    \emph{and} a location** — \$1800 alone is half an answer.
  - **The extension's part (c) is the cleanest evidence in the lesson that $a$ controls shape and
    nothing else**: change $-2$ to $-\tfrac12$ and nothing else, and the vertex $(4,8)$ does not
    move while the two zeros spread from $2,6$ to $0,8$. One change, two consequences and one
    non-consequence.
  - Guard sizes: bare on vocab, `[12]` hook, `[30]`/`[30]`/`[30]` on the three notesboxes, `[30]`
    practice, `[30]` on all three activity tiers, `[24]`/`[30]`/`[24]`/`[26]` on the homework's
    boxes, `[18]` on the plan's Reinforcement box and each of the five teachernotes, `[16]` on the
    plan's Individual Work box (2.2's finding, applied pre-emptively and correct first pass).
  - **Boxguard finding — and the first case in this course where `\tcbbreak` was the right answer
    on the first build.** The homework's remindbox landed **alone on p4**, a ~0.75in strip on an
    otherwise blank page, with `make check` clean throughout (the key stranded the same box, so
    parity was perfect at 4/4). **`\workrowsep` was swept 8pt $\to$ 6, 5, 4, 2, 0pt and never bought
    the page back**, so the 4th page is unavoidable — this is the counter-case to Unit 1's tests,
    where 8pt did buy a page. The fix is a `\tcbbreak` before extension part (c), sending it over
    with the remindbox so p4 carries ~2.7in of real content. **Breaking one item earlier (before part
    (b)) was also tested: still 4 pages, but it left half of p3 empty**, so the later placement is
    the better balance. Both the sweep and the placement verdict are recorded in comments in the
    blank and the key. **Note this does not repeal 2.0's rule** — no `\tcbbreak` was authored until
    the build proved one necessary, which is exactly the rule working.
  - **A figure defect that no check and no page count can see: a pgfplots `legend` at
    `at={(0.5,1.02)}, anchor=south` prints on top of the axis `title`.** Notes box 2 panel (a) had
    both, and "parent | image" overprinted "(a) Quadratic." **Never combine `title` with a legend
    placed above the axis.** The fix — and the better pattern for a multi-panel row — is to drop the
    per-panel legend and put one `\scriptsize` caption sentence under the whole row naming the
    dashed/solid convention once. 2.2's log established that legends above the axis beat crowded node
    labels; this is its limit.
  - **Pagination findings, both accepted after the test-then-restore check.** (1) The practice box's
    guard was lowered `[30]` $\to$ `[16]` to try to fill notes p4's lower half; it split the box and
    **stranded only the two-line scenario paragraph** at the foot of p4, with the figure and all four
    items on p5 — worse, and 5 pages either way. Restored, verdict in a comment in both files.
    (2) **The lesson plan runs 6 pages with the Homework teachernote alone on p6.** Plan pp. 3–4 are
    completely full and p5 holds four teachernotes with no slack, so the break is forced. The note is
    a *complete, substantial box*, not a stranded stub, so this is dead space rather than a boxguard
    violation — accepted, and worth knowing that five teachernotes at this length overflow a 5-page
    plan.
  - **A wide Beamer table wants the `X` column on the prose column here too** (2.1's rule, second
    confirmation): the landmark frame at `p{2.3cm} p{4.6cm} X` hyphenated "two points you can read
    ex-actly"; `p{2.1cm} p{5.2cm} X` fixed it with no overfull anywhere in the deck.
  - Page counts: cover 1, warm-up 1/1, notes 5/5, activity 3/3, exit ticket 1/1, homework 4/4;
    student and key packets 20 pages each. Plan 6 pp, slides 11 frames (4 pp printed 3-up).
- **`unit02/lesson02` — Parent Functions and Transformations (`AFDA.AF.1a–b`).** Unit 2's first
  transformation lesson.
  - Spine: **every transformation answers one question — did the *outputs* change or did the
    *inputs* change?** Outside the parentheses touches outputs, inside touches inputs. Everything
    else in the lesson is a consequence, including the "backwards" horizontal rule.
  - **The horizontal rule is taught as substitution, never as "the sign flips."** $f(x-2)$ at
    $x=5$ computes $f(3)$, so the new graph at $5$ shows what the old one showed at $3$. The plan,
    the notes, the deck, and the Active Monitoring box all say to *refuse* the sign-flip phrasing
    and replace it with an evaluation. That is the single most repeated instruction in the lesson.
  - **2.1's homework item 10 already made students describe a vertical translation in their own
    words; 2.2 opens by naming it.** Warm-up item 5 asks for that sentence back, and if it takes
    more than fifteen seconds the class did not do the homework — the plan says so.
  - Hook is **the same firework shell, three seconds later**: 2.0's own exit-ticket function
    $h_A(t)=-16t^2+64t$ (peak $64$ ft at $t=2$, down at $t=4$), fired again at $t=3$. Students
    **vote** on whether shell B's equation says $h_A(t+3)$ or $h_A(t-3)$ before seeing anything;
    most classes vote $+3$. Resolved with one number, not a rule: at $t=5$ shell B has lived
    $5-3=2$ seconds, so it is at $h_A(2)=64$. Domain slid $[0,4] \to [3,7]$; range still $[0,64]$.
    **Reusing a function the class already read makes the shift, not the model, the new thing.**
  - **Warm-up item 2 is the diagnostic of the day**: $f(5)$ versus $f(5-3)$ for $f(x)=x^2$. A
    student who writes $f(5-3)=25-3=22$ substituted *after* applying the rule instead of before,
    and that one habit produces every backwards horizontal shift in the unit. Item 3 ($-x^2$ vs
    $(-x)^2$ at $x=3$, giving $-9$ and $9$) plants the two reflections and is quoted verbatim in
    notes box 3 and again in Tier E — **do not resolve it during the warm-up.**
  - Notes = 5 vocab terms (parent function, function family, translation, reflection, dilation)
    + four boxes: the **three parents** with pre-drawn panels and a domain/range table (the
    exponential's $(0,\infty)$, a parenthesis, is 2.1's bracket rule paying off and previews 2.5);
    **translations** off a three-curve figure, closing on the shells; **reflections and dilations**
    off two figures; and **the card** — the SOL guidance's six notations in one table with an
    outputs/inputs column and a domain/range column. In-text blanks: *adds*, *multiplies*,
    *outside*, *inside*, *opposite*, *range*, *domain*, *$x$*, *$y$*, *stretch*, *compression*.
  - **Box 4 (the card) is the study sheet and is deliberately not a duplicate of boxes 2–3**: boxes
    2 and 3 build the moves with figures, box 4 collects them and adds the *which-one-moved*
    column. It takes three minutes to fill and is what students revise from.
  - **The parabola's own symmetry is the best small idea in the lesson.** $g(-x)=(-x)^2=x^2=g(x)$,
    so reflecting $x^2$ over the $y$-axis really happens and shows nothing. Tier E item 3 asks
    students to defend that, and to name a parent ($x$ or $2^x$) where the same flip is obvious.
  - **Two coincidences to route around, both recorded because they will bite a later author.**
    (1) For the *linear* parent a horizontal shift equals a vertical shift ($5(g-2)=5g-10$), so
    **never demonstrate a horizontal translation on a line.** (2) For linear and quadratic parents
    a horizontal dilation equals a vertical one ($(2x)^2=4x^2$), so $f(kx)$ is demonstrated on the
    **exponential** ($2^{2x}=4^x$) and, in Tier A, on a **restricted-domain context** where the
    domain visibly halves.
  - Context thread, every read on a gridline: hook/shells $-16t^2+64t$; guided practice **robotics
    fundraiser** $P(x)=-x^2+8x$ on $[0,8]$ (max $16$ at $x=4$) with a flat \$400 sponsor gift,
    $Q=P+4$, range $[0,16] \to [4,20]$ and the domain untouched; activity Tier R $x^2$ with
    $x^2-5$ and $(x+3)^2$; Tier A $x^2$ with $-x^2$ and $\tfrac13x^2$ plus a conveyor belt at
    double speed, $C(2t)$, domain $[0,8] \to [0,4]$; exit ticket $(x-3)^2$ and $2^x-5$; homework
    **two irrigation zones**, $F(t)=8t-t^2$ on $[0,8]$ and $G(t)=F(t-4)$ on $[4,12]$
    ($G(6)=F(2)=12$, both flowing on hours $4$–$8$).
  - **The $f(kx)$ item is where groups reliably go wrong** — they answer "the range moved, because
    it is faster." The prompt that fixes it is in the plan: *does the arm reach a different height,
    or the same height sooner?*
  - Activity tiers R/A/E. Tier E is error critique (**$(x+5)^2$ "moves right"** and
    **$-x^2 = (-x)^2$**, both refuted with a number, not a rule), a two-step $(x-3)^2+2$, and the
    symmetric-parabola justification.
  - Homework 10 items (families from equations, families from **three tables** — $A$ adds $3$, $B$
    multiplies by $2$, $C=2x^2$ has constant second differences of $4$; six single transformations;
    three ranges incl. $2^x-3 \to (-3,\infty)$; equations written from words; the four-part
    irrigation read) + an extension. **Item 10 bridges to 2.3**: the parent drawn with $x^2-4$ and
    $(x+2)^2$, both equations written, one checked by substitution, and a prediction of what the
    TI-84 screen will show. Extension closes on **whether order matters** — $-(x^2)+9$ gives $8$ at
    $x=1$ while $-(x^2+9)$ gives $-10$, settled by two numbers and no theory.
  - Guard sizes: bare on vocab, `[12]` hook, `[30]`/`[30]`/`[30]`/`[24]` on notesboxes 1--4, `[30]`
    practice, `[30]` on all three activity tiers, `[24]`/`[30]`/`[30]`/`[30]` on the homework's
    boxes, `[18]` on the plan's Reinforcement box and each of the five teachernotes, plus a **new**
    `[16]` on the plan's Individual Work box.
  - **Two boxguard findings, both invisible to `make check` (which passed clean throughout).**
    (1) The homework's extension box at `[22]` broke, stranding **one write-line plus the remind
    box alone on p4**. `[30]` moves it whole; the page count stayed at 4. Lowering it to `[20]`
    *and* trimming the look-ahead figure was then tested to try to buy the page back — still 4
    pages, so everything was restored per 1.5's test-then-restore rule, with the reason in a
    comment in both files. (2) **The lesson plan's Individual Work \& Assessment box stranded a
    single line atop plan p4** — `\boxguard[16]` moved it whole and the plan held at 5 pages. 1.7
    found this on a teachernote; **it applies to every plan box, not just the trailing ones.**
  - **Pagination finding, consistent with 1.5.** Notes pp. 2–3 each hold one complete box with an
    empty lower half. Lowering notes box 2's guard to `[16]` (to let it split after the
    figure + table) was tested and **still gave 5 pages**, so the break is the natural one;
    restored to `[30]` with the verdict in a comment in both files.
  - **A `\tfrac` in an `\ans` table cell can outgrow the blank's row and break parity.** Tier A
    item 4's $2^{-x}$ row answers with $\tfrac12$ and $\tfrac14$; the fix is a
    `\rule[-0.75em]{0pt}{1.9em}` strut in the row's label cell, authored **in the blank and the
    key both**, so the row height is set identically. This is the general form of 1.7's `\dfrac`
    finding — **any tall answer in a cell whose blank counterpart is short needs a shared strut.**
  - **Multi-curve figures use a pgfplots `legend` placed above the axis**
    (`at={(0.5,1.02)}, anchor=south, legend columns=3`), never node labels crowded against the
    curves. That region is always free and it survives a change of curve. Node labels are used
    only where three curves end at distinct heights (notes box 3).
  - **A wide table on a Beamer frame needs `\small`.** The card frame overflowed by 2.9pt at
    `\arraystretch{1.35}`; `\small` plus `1.25` fixed it. Check `Overfull \vbox` in the deck log,
    not just the components'.
  - Page counts: cover 1, warm-up 1/1, notes 5/5, activity 3/3, exit ticket 1/1, homework 4/4;
    student and key packets 20 pages each. Plan 5 pp, slides 11 frames (4 pp printed 3-up).
- **`unit02/lesson01` — Function Fundamentals: Notation, Domain, and Range (`AFDA.AF.2a, e`).**
  Unit 2's first content lesson.
  - Spine: **``$f(3)=10$'' and ``the point $(3,10)$ is on the graph'' are one sentence in two
    costumes.** That equivalence *is* `AF.2e`, and it is what makes a graph readable. The second
    sentence is **a domain is a decision, not a calculation** — `AF.2a`'s phrase "*including those
    limited by contexts*" is the standard asking for exactly that.
  - **The lesson's organizing move is that a graph gets read in two opposite motions**, and they are
    named out loud: input given $\to$ horizontal axis, up, across; output given $\to$ vertical axis,
    across, down. This is the fix for the input/output stall 2.0's diagnostic found (its warm-up
    item 1: evaluate fine, then freeze on "solve $f(x)=1$").
  - Hook is the **downtown garage**, $C(h)=2h+4$ on $0 \le h \le 8$: \$4 to enter, \$2 an hour,
    billed by the minute (stated, so continuity is honest). Two people ask the same sign two
    different questions --- "what will three hours cost" ($C(3)=10$) and "I have \$16, how long can
    I stay" ($C(6)=16$). Every read lands on a gridline (ticks $1$ in $h$, $4$ in $C$).
  - **The garage's range starting at \$4, not \$0, is the best small idea in the lesson** — the low
    end of a range can be a fact about the *story* (you pay before the clock starts), not about the
    formula. Pair it with "why does the domain stop at $h=8$ when $2(9)+4=22$ computes fine?"
  - Notes = 5 vocab terms (function notation, domain, range, interval notation, restricted domain)
    + four boxes: the notation$\leftrightarrow$point table (4 rows, ending in the **warning that
    the notation does not flip**, $C(3)=10 \ne C(10)=3$); domain/range off the same graph; **the
    three-spellings table**; and what cuts a domain short. In-text blanks: *horizontal*, *vertical*,
    *input*, *output*, *included*, *smaller*, *dots*.
  - **Notes box 3 is the SOL-notation box and its row set comes straight from the AFDA "Understanding
    the Standards" table on p5** (equation/inequality, set notation, interval notation, $\emptyset$).
    Two rows are deliberately **not intervals** — the list $\{2,5\}$ and the empty set — because
    those are the ones students skip. Four rules close it: bracket includes, parenthesis excludes,
    **$\infty$ never takes a bracket**, and **an interval is written smaller-number-first no matter
    which way the graph runs** (the candle case, which Tier E then assesses as an error).
  - Notes box 4's **three reasons a domain gets cut short — the context, the graph, the algebra —
    are worth memorizing as a list**; the third lands on 1.7's $\frac{x+1}{x-3}$, so the excluded
    value the class already found becomes a hole in a domain. The whole-number paragraph under it
    (a field trip cannot take $17.4$ students) is what Tier E item 2 tests.
  - Guided practice is the **drone** $A(t)=-2t^2+16t$ on $[0,8]$ (peak $32$ ft at $t=4$; ytick $8$).
    Its item 2 is the reasoning item of the day: $A(t)=24$ has **two** answers ($t=2$ and $t=6$),
    which is allowed, because a function promises one output per *input* and nothing in reverse.
    Warm-up item 4 plants this on a table first — **do not resolve it during the warm-up.**
  - Context thread is one both-directions read per component, and every asked value lands on a
    gridline: notes/garage $C(h)=2h+4$; practice/drone $-2t^2+16t$; activity Tier R candle
    $L(t)=20-2t$ on $[0,10]$ ($L(6)=8$, $L(t)=4$ at $t=8$); Tier A skate bowl $H(x)=(x-6)^2/3$ on
    $[0,12]$ ($H(3)=H(9)=3$, and $H=0$ at $x=6$ is **the one height with a single input**);
    exit ticket pool $W(t)=2400-300t$ on $[0,8]$ ($W(2)=1800$, $W(t)=600$ at $t=6$); homework arch
    $y=20-x^2/5$ on $[-10,10]$ ($y(\pm5)=15$).
  - **The homework arch is the course's first graph with negative inputs** — expect the domain
    reported as $0 \le x \le 10$ by students who read only the right half. Its item 9 (a 12-ft truck,
    edges at $x=\pm5$, clears by 3 ft) must be justified from a value on the graph.
  - Activity tiers R/A/E. Tier E is error critique (**flipped notation** $L(6)=8 \Rightarrow L(8)=6$,
    and **an interval written backwards** $[20,0]$), a **dot graph** (hot dogs at \$3, at most 8) whose
    domain and range are lists that interval notation cannot express, and a justify item refuting
    "the bowl is not a function because one height happens twice."
  - Homework 10 items (notation both ways, a table read both ways, interval $\leftrightarrow$
    inequality in each direction, a three-part "what restricts this domain?", the four-part arch,
    and the look-ahead) + an extension. **Item 10 bridges to 2.2**: tabulate $f(x)=x^2$ against
    $g(x)=x^2+3$, watch every output rise by 3, and find the **range** moved $[0,\infty) \to
    [3,\infty)$ while the domain did not move at all. Accept plain English; *translation* is 2.2's
    word to introduce.
  - Extension reuses **1.7's own booster-club $A(x)=\frac{6x+240}{x}$**, now asked as a domain
    question: restricted **twice** (algebra forbids $x=0$; context forbids fractions and caps at
    200), so the answer is $\{1,2,\dots,200\}$ and no interval can express it. First time students
    meet a doubly-restricted domain.
  - Guard sizes, all clean first pass: bare on vocab, `[12]` hook, `[30]`/`[22]`/`[26]`/`[20]` on
    notesboxes 1--4, `[30]` practice, `[30]` on all three activity tiers, `[24]`/`[30]`/`[24]`/`[22]`
    on the homework's boxes, `[18]` on the plan's Reinforcement box and each of the five teachernotes.
    That is 2.0's set transferred verbatim. **No `\tcbbreak` was needed** — the sixth lesson
    confirming it must never be authored before a build proves it necessary.
  - **Two pagination findings, both consistent with prior rules.** (1) Notes p4 holds only the
    practice box; lowering its guard to `[16]` was tested and still gave 4 pages, so the break is
    natural — restored to `[30]` per 1.5's "test, then restore." (2) The homework look-ahead box at
    `[24]` again sits alone-ish on p3 while p2 ends at ~63%; measured, the box needs ~24 baselines
    against ~22 free, so `[24]` is correct and lowering it would strand an item — **2.0's finding
    reproduced exactly.**
  - **Two table-width fixes worth carrying.** A `tabularx` whose `X` column is the *last* content
    column pushes all slack there and squeezes the words column into two-line wraps. Put `X` on the
    **prose** column and fix the notation columns (`X p{2.6cm} p{4.0cm} p{2.2cm}` in notes box 3).
    Same fix on the deck's notation frame (`X p{2.4cm} p{3.2cm} p{2.8cm}`), where "not an interval"
    was hyphenating.
  - Page counts: cover 1, warm-up 1/1, notes 4/4, activity 3/3, exit ticket 1/1, homework 3/3;
    student and key packets 18 pages each. Plan 5 pp, slides 10 frames (4 pp printed 3-up).
- **`unit02/lesson00` — Unit 2 opener (no new content). The course's first graph-reading lesson.**
  - Spine: **in Unit 1 you were handed an expression and asked to rewrite it; in Unit 2 you are
    handed a graph and asked what it says.** That is not a teaching preference — the AFDA
    "Understanding the Standards" guidance says outright that in AFDA the characteristics of
    functions are investigated **only from a graph** (analysis from equations is Algebra 2). Say it
    out loud on day one; it is the rule the whole unit runs on.
  - Hook and notes box 1 are **one graph that answers every question the unit asks**: a hiker's
    elevation, $(0,800) \to (2,1600) \to (3,1600) \to (4,2000) \to (6,1000)$, piecewise linear with
    clean integer reads. It yields domain $[0,6]$, the $E$-intercept $800$, a **constant** stretch
    ($t=2$ to $3$), absolute max $2000$ at $t=4$, absolute min $800$ at $t=0$, a rate comparison
    (climb $400$ ft/hr vs. descent $500$ ft/hr) — and, deliberately, **no zeros at all**: the
    hikers never reach sea level. Students arrive believing every graph crosses the $x$-axis; kill
    that here, cheaply.
  - **Two phrases are drilled and both are assessed as errors in Tier E**: an extreme is reported
    as **value \emph{and} location** ("2000 feet" is half an answer), and **"absolute" means over
    the whole domain** (on the battery graph the max is $100\%$ at $t=0$, not the $80\%$ top of the
    charging stretch). The other Tier E critique is domain/range swapped.
  - Notes box 2 previews the three families with pre-drawn parents $f(x)=x$, $g(x)=x^2$,
    $h(x)=2^x$; the discriminating question is **adding vs. multiplying**, since a line and an
    exponential both rise forever. Tier E's three tables make it concrete: $A$ adds $3$ (linear),
    $B$ multiplies by $2$ (exponential), $C=3x^2$ has constant **second** differences of $6$
    (quadratic). Groups that only check first differences stall on $C$ — prompt them to difference
    the differences.
  - Warm-up = the **Unit 2 diagnostic**, five items, figure-free so it holds one page: function
    notation *and solving $f(x)=k$* (2.1), an excluded value (2.1/2.5), rate of change from a table
    (2.2/2.7), intercepts of a line (2.4), evaluate-and-interpret. **Item 1's second half predicts
    the period** — evaluating is automatic, solving requires knowing which slot the number goes in.
  - **The Unit 1 → Unit 2 bridge is carried end to end and is the lesson's best thread**: warm-up
    item 2 is a 1.7 excluded value, notes box 4 names it a *domain restriction*, and homework item 9
    takes 1.7's own $f(x)=\frac{x+1}{x-3}$, tabulates $f$ at $2.9, 2.99, 3.01, 3.1$
    ($-39, -399, 401, 41$), and lets students name the vertical asymptote themselves. Accept any
    description of the graph shooting off; *asymptote* is 2.5's word to introduce, not today's to
    demand.
  - Other verified numbers: guided practice $R(p)=-5p^2+60p$ (zeros $0$ and $12$, max $180$ at
    $p=6$); Tier R $C(m)=2m+3$; Tier A battery $(0,100),(2,70),(3,70),(7,30),(9,80),(10,65)$ — every
    segment slope an integer, min at $t=7$ = 2 p.m.; exit ticket $h(t)=-16t^2+64t$ (max $64$ ft at
    $t=2$, range $[0,64]$); homework views $2^d$ hundreds and the savings-plan extension where
    \$20 doubling passes \$100$+$\$50/month in **month 4** ($320$ vs.\ $300$).
  - **`pgfplots` needs no per-file load in components** (`atda-article` provides it) but **does** in
    the deck — the slides carry `\usepackage{pgfplots}` + `\pgfplotsset{compat=1.18}`, per 1.6's
    finding. The Beamer frames are **light**, so pgfplots axes there use the default (dark) tick
    labels and a `royal` plot line; do not copy dark-background axis styling into them.
  - **Three-panel parent-function figures need explicit column gaps.** `@{}ccc@{}` butts the axis
    boxes together and the quadratic's arms crowd the neighbouring panel. Use
    `@{}c@{\hspace{0.5cm}}c@{\hspace{0.5cm}}c@{}` (0.9cm on a slide) and size each panel to fit.
  - **Boxguard findings, one real.** (1) `\tcbbreak` was authored speculatively at two points in
    the activity and was **wrong both times** — it cost a whole page and left pp. 2–4 roughly 55%
    empty. Removing both took the activity from 4 pages to 3 with every box complete. Fifth lesson
    confirming `\tcbbreak` is a per-lesson judgement: **do not author one until a build proves it is
    needed.** (2) Notes box 2's guard at `[30]` pushed it off a page it could hold; `[22]` (its true
    height) closed a half page of dead space. (3) The homework look-ahead box at `[24]` was lowered
    to `[20]` to reclaim dead space and **broke, stranding item 9(c) alone atop p3** — `make check`
    passed clean throughout, because the key stranded the same lines. Restored to `[24]` with the
    reason in a comment in both files. **The box measures ~23 baselines; a guard must exceed the
    box, not approximate it.**
  - Guard sizes that held: bare on vocab and notesbox 4, `[12]` hook, `[30]`/`[22]`/`[26]` on
    notesboxes 1–3, `[30]` practice (it opens on a pgfplots axis), `[30]` on all three activity
    tiers, `[24]`/`[30]`/`[24]`/`[22]` on the homework's boxes, `[18]` on the plan's Reinforcement
    box **and on each of the five teachernotes** (1.7's finding, applied pre-emptively — the plan
    came out clean first pass).
  - Notes p3–p4 each run ~55% full: the practice box measures ~5.4in against ~4.4in free on p3, so
    the break is the natural one and `[30]` is right-sized. Accepted per 1.5's rule.
  - Page counts: cover 1, warm-up 1/1, notes 4/4, activity 3/3, exit ticket 1/1, homework 3/3;
    student and key packets 18 pages each. Plan 5 pp, slides 10 frames (4 pp printed 3-up).
- **`unit01/unit_cover/` + `unit_cover_key/` — the course's FIRST unit cover pair. Reuse its
  shape for every later unit.**
  - The sheet is `unit_cover/body.tex`; **both** wrappers `\input` it (`unit_cover_key` as
    `../unit_cover/body.tex`), so page 1 cannot drift. Never edit a wrapper.
  - Page 1 (student): banner → one-paragraph overview → an **8-row lesson table** (#, lesson,
    SOL code, "the one idea") → `spiralbox` of the unit's **five big ideas** → `remindbox`
    stating the test blueprint. Both wrapper preambles need `ltablex` + `\keepXColumns`.
  - The five big ideas are the unit's two error streaks made explicit — "an operation does not
    reach inside a sum" (1.1/1.2/1.7) and "completely means largest, not first" (1.3–1.6) —
    plus factoring-recovers-information, zero-is-the-only-useful-product, and the scar.
  - Page 2 (key only, teacher): four `teachernote` blocks — Part A letters for both forms, Part B
    rationale, Part C scoring with **two named deductions**, Part D rubric. This is where the
    test prose lives; see the teachernote note in the tests entry below.
- **`unit01/tests/` + `unit01/test_keys/` — the course's FIRST unit test set. Reuse the
  blueprint.**
  - **Blueprint, 100 pts, four parts:** A vocabulary matching 8×1 (10 definitions, **two are
    distractors** so six known terms cannot yield the last two by elimination); B multiple choice
    6×2; C short answer 10×5, **one item per lesson in lesson order** (1.1 exponent rules →
    1.7 dividing, then an applied area item and a factor-completely item); D extended response
    2×15. Scale the counts, but keep Part C's per-lesson spine — it is what makes it summative.
  - **Part D is the two prompts the unit earned.** D1 = verify an identity by multiplying
    (`A2.EO.3d`), then judge the claim that the simplified quotient equals the original *for
    every $x$* (`A2.EO.1b`) — the algebra is right and the claim is still wrong, which is 1.7's
    "scar" as an assessment item. D2 = a projectile $-16(t-r_1)(t-r_2)$ (`A2.EI.6a–b`): reject
    $t=-1$, but in part (c) **keep both** $t=0$ and the way down — the two-sided interpretation.
  - **Parallel forms.** Practice $-16t^2+64t+80 = -16(t-5)(t+1)$, D1 on $x^3-64$; actual
    $-16t^2+96t+112 = -16(t-7)(t+1)$, D1 on $x^3+27$. Vocabulary terms are reordered and the
    definitions reworded and relettered, so practice answer letters transfer nothing.
  - **Parity mechanism: every computation is a `work` block, byte-identical blank↔key.** No raw
    `\vspace` work room anywhere — the block reserves exactly the answer's height in the blank
    and prints it in the key, so the four documents cannot drift. Prose answers use
    `\writelines{n}` against exactly `n` short `\ansline{…}\\` lines.
  - **`\workrowsep` is the tuning knob, and it is documentwide.** At 10pt the practice test ran
    **5 pages with item D2(d) alone on page 5** — a stub in both files, so page parity was
    perfect and nothing flagged it. 9pt still gave 5; **8pt gave 4**, and 7pt also gave 4. **8pt
    was kept** — the largest value that buys the page back, per 1.5's "test, then restore" rule.
    This is the test-document analogue of the boxguard tuning rule: on a test, reach for
    `\workrowsep` before reaching for a guard, because it moves all four files at once.
  - **`\parthead` carries its own `\boxguard[9]`** so a part strip can never be stranded at a page
    foot. Define it identically in all four files.
  - **Second boxguard finding: a multiple-choice item split across a page.** On the actual test,
    Part B item 4's stem and options (A)–(B) sat at the foot of p1 with (C)–(D) atop p2. **A
    multiple-choice item must never break** — a student cannot compare options they have to turn
    a page to see. `\boxguard[7]` before the `\item` (mirrored in the key) moved it whole; the
    page count held at 4. Note this guard is in an `enumerate`, not a `tcolorbox`, so
    `\Needspace` works normally — the "inert inside a breakable tcolorbox" limit does not apply.
  - **No `teachernote` in any of the four test files** — the practice test is published to
    `sample_test/` and rides in the **student** packet, so its rationale would reach students.
    All of it is on `unit_cover_key/` page 2 instead (key packet only).
  - `make -C unit01/tests all` and `make -C unit01/test_keys all` publish
    `unit01/sample_test/main.pdf` and `unit01/sample_test_key/main.pdf`. **Those two PDFs are
    build outputs that must be committed** — `unit.mk` reads them from the source tree, so a
    fresh clone cannot merge the unit packets without them.
- **`unit01/lesson07` — Simplifying Rational Expressions (`A2.EO.1a–b`).** The last content lesson
  of Unit 1.
  - Spine: **nothing about fractions changed — the letters are the only new thing.** $12/18 = 2/3$
    and $\frac{(x+3)(x-3)}{(x+3)(x+4)} = \frac{x-3}{x+4}$ are one move. The sentence being taught is
    *only factors cancel* — a factor is being multiplied, terms joined by $+$ or $-$ are not.
  - **The unit's error streak changes family here, and that is deliberate.** 1.3–1.6 ran "true but
    incomplete" four times. 1.7's error is a *different* belief with its own three-lesson streak:
    1.1's $(2m+3)^2 \ne 4m^2+9$, 1.2's $\sqrt{9+16} \ne 7$, and now cancelling across a $+$. The
    plan, the slides, and the exit-ticket note all name it as **"an operation does not reach inside
    a sum."** Say the streak out loud — students hear three unrelated mistakes otherwise.
  - **Scope decision, deliberate and recorded.** `EO.1a` (all four operations) is covered in full;
    unlike denominators appear, but only where the common denominator is a **product of binomials
    already in front of the student** — no LCM algorithm. Complex fractions (`EO.1c`) are not in the
    lesson map and are not taught. Every denominator is linear or quadratic, per `EO.1b`.
  - Warm-up **item 3 is the diagnostic and the theorem at once** (1.6's pattern, reused): pure
    arithmetic — $\tfrac{12}{18}$, then $\tfrac{3+4}{3+5}=\tfrac78 \ne \tfrac45$, then
    $\tfrac{3\cdot4}{3\cdot5}=\tfrac45$. Item 4 is the pivot onto letters. **Unlike 1.6, a student
    who cannot factor item 1 genuinely cannot start** — factoring is the only way to see what
    cancels; note those names for Tier R before the notes begin.
  - Hook is the **booster club's T-shirts**, $A(x)=\frac{6x+240}{x}$: the "cancel the $x$'s" claim
    of \$246 is refuted by arithmetic ($A(10)=30$, $A(40)=12$, $A(240)=7$), and $x=0$ is the
    course's first excluded value — one the *story itself* explains. This expression deliberately
    **does not cancel**, which is how "simplify does not mean shorten" gets stated on minute one.
  - Notes = 5 vocab terms (rational expression, excluded value, **factor vs. term**, simplest form,
    equivalent rational expressions) + four boxes: excluded values (5-row table whose **row 5,
    $\frac{3x}{x^2+9}$, has no excluded values at all** — 1.5's prime sum of squares paying a third
    dividend); simplifying, whose two closing paragraphs (**the scar** and **the error of the day**)
    matter more than its table; multiply/divide, where $x \ne -1$ survives into an answer with no
    fraction in it; and add/subtract, like denominators then one unlike pair. The three in-text
    blanks are *zero*, *factors*, *original*.
  - **"The scar" is the lesson's best idea and it is exactly `EO.1b`'s word *justify*.** Excluded
    values are read from the **original** denominator: $\frac{x^2-9}{x^2+7x+12}$ is $\tfrac00$ at
    $x=-3$ while $\tfrac{x-3}{x+4}$ returns $-6$. Cancelling hides a restriction; it never removes
    one. Tier E item 1(b) is a *correct* simplification asserted "for every $x$" — a student being
    wrong while their algebra is right, which most have never had to distinguish.
  - Context thread is one per-unit-rate model per component, and the **interpretation move is
    two-sided** (1.6's rejected-vs-kept, restated): an excluded value may be *meaningful* ($x=0$
    shirts) or *unreachable* ($x=-4$ feet of width). Notes/T-shirts $\frac{6x+240}{x}$ (no cancel);
    guided practice/banner $A=x^2+9x+20$, width $x+4$, length $x+5$, $C/A = \$7$/sq ft
    ($770/110$ at $x=6$); activity/backdrop $A=x^2+3x-28=(x+7)(x-4)$, $5 \times 16 = 80$ sq ft at
    $x=9$, $C/A = \$2$ ($160/80$); homework/garden bed $A=2x^2+14x+20=2(x+5)(x+2)$, length $2x+10$,
    $5 \times 16 = 80$ at $x=3$, $M/A = \$3$ ($240/80$). **Per-unit-cost models with a fixed fee
    never cancel** — only the "bill built as a multiple of the area" ones do, which is why the hook
    and the practice item are deliberately opposite.
  - Activity tiers R/A/E; Tier E is error critique (cancelling terms, and the "for every $x$"
    claim), a division whose $x \ne -1$ vanishes from the answer, and subtract-then-**verify-at-a-
    number** ($x^2/(x-5) - 25/(x-5) = x+5$, checked at $x=7$).
  - Homework 13 items (2 excluded-value, a monomial, 3 binomial simplifications incl. a **PST
    denominator** $x^2-14x+49$ and GCF-first $5x-20$, one of each operation, the garden bed, the
    look-ahead) + an extension adding $\frac{3}{x-2}+\frac{5}{x^2-4}$, where one denominator
    **factors into** the other, verified at $x=3$. **Item 13 bridges to Unit 2**: the excluded value
    of $f(x)=\frac{x+1}{x-3}$ is a **domain** restriction (`AFDA.AF.2a`) and becomes a vertical
    asymptote (`AF.2g`) — accept any description of the graph shooting off; *asymptote* is Unit 2's
    word to introduce.
  - Guard sizes: bare on vocab, `[12]` hook, `[24]`×4 on the notesboxes, `[20]` practice,
    `[16]`/`[16]`/`[30]` on Tiers R/A/E, `[16]`–`[18]` on the homework's trailing boxes, `[18]` on
    the plan's Reinforcement box — the 1.2–1.6 set again, transferred verbatim for the sixth time.
  - **Two boxguard findings, both invisible to `make check` (which passed clean throughout).**
    (1) Notes box 2 split leaving **one line** atop notes p3; `\tcbbreak` before the "why the
    original denominator" paragraph sends both closing paragraphs over together, and the page count
    held at 4 while p4 improved from *practice box alone* to *box 4 + practice*. A `\tcbbreak` that
    costs nothing and fixes two pages at once is rare — this is the fourth lesson confirming it is a
    per-lesson judgement. (2) The **lesson plan's Guided Notes teacher note** stranded three lines
    atop plan p5; `\boxguard[18]` before it moved the note whole and the plan held at 5 pages.
    **A teachernote is a breakable box like any other and needs a guard** — 1.0 found this on the
    Reinforcement box; it applies to the notes too.
  - **A `\frac` inside `\ans{...}` in a table cell renders at script size and is too small to read
    on a teacher key.** The eight fraction cells in notes box 2's table were switched to `\dfrac`;
    because the row height is set by the blank's `\TallMath` strut (identical in both files), this
    changed no page count. Use `\dfrac` in any `\ans` cell whose row is already `\TallMath`-sized.
  - Page counts: cover 1, warm-up 1/1, notes 4/4, activity 3/3, exit ticket 1/1, homework 3/3;
    student and key packets 18 pages each. Plan 5 pp, slides 11 frames (4 pp printed 3-up).
- **`unit01/lesson06` — Solving Polynomial Equations by Factoring (`A2.EI.2b`, `A2.EI.6a–b`).**
  - Spine: **factoring did not change; the question did.** 1.3–1.5 asked "what are the dimensions?"
    1.6 asks "*when*?" The engine is the **zero product property**, and the sentence being taught is
    *zero is the only number that tells you anything* — $ab=12$ says nothing about $a$, $ab=0$ forces
    a factor. 1.5's homework item 13(b) ran the whole method once already (factor $x^2-36$, reason to
    $x=6$, reject $x=-6$), so 1.6 opens by *naming* what the class already did.
  - **Scope decision, deliberate and recorded.** `EI.2b` says "over the set of complex numbers"; the
    course spec caps it at *real solutions by factoring*, so no $i$ and no quadratic formula. `EI.6b`
    ("number and type") is satisfied **without complex arithmetic**: degree gives the count, and a
    factor $x^2+k$ with $k>0$ contributes two imaginary solutions because *a square is never
    negative*. That claim is airtight; **do not generalize it to "any prime quadratic"** — $x^2-2$ is
    prime over the integers and has two real roots.
  - Warm-up **item 3 is the diagnostic and the theorem at once** — pure arithmetic ($ab=0$ vs
    $ab=12$), so every student can answer it, and the sentence they produce *is* the property. Item 4
    is the pivot, same structure as 1.3/1.4/1.5.
  - Notes = 5 vocab terms (zero product property, solution/root, zero of a function, double root,
    **imaginary solution**) + four boxes: the property with an already-factored table (incl. $3x(x-5)$
    where $x=0$ is a real solution and $(x-3)^2$ the **double root**); standard form first, whose
    **row 4 ($2x^2=8x$) is the trap of the day**; degree three and higher, where $x^3+4x$ makes 1.5's
    prime sum of squares finally cost something; and the **backwards** direction (`EI.6a`) — a
    solutions→equation table plus a **pre-drawn cubic graph** ($y=x^3-x^2-6x$, intercepts $-2,0,3$)
    read for its intercepts. The three in-text blanks are *zero*, *degree*, *imaginary*.
  - **"True but incomplete" reaches its fourth lesson**: $5x(4x+6)$ → $(2x+4)(x+6)$ → $(2x+6)(x-3)$ →
    dividing $2x^2=8x$ by $x$ and losing $x=0$. The exit ticket's item 3 is that error; say the streak
    out loud.
  - Context thread is one height model per component, all factoring $-16(t-r_1)(t-r_2)$:
    notes/T-shirt launcher $-16t^2+32t+48 = -16(t-3)(t+1)$, lands at $3$ s; guided practice
    $-16t^2+16t+32=-16(t-2)(t+1)$, plus $h=32$ giving $t=0,1$; activity/model rocket
    $-16t^2+32t+128=-16(t-4)(t+2)$, plus $h=128$ giving $t=0,2$; homework/water balloon
    $-16t^2+80t+96=-16(t-6)(t+1)$, plus $h=96$ giving $t=0,5$.
  - **The interpretation move is deliberately two-sided**, and it is the lesson's best idea: a
    negative time is *rejected*, but $t=0$ is *kept* — it is the launch. Activity Tier A item 4 (a
    ground-launched rocket, $-16t^2+48t$) exists to catch groups treating "throw out the extra one"
    as a rule rather than a judgement.
  - Activity tiers R/A/E; Tier E is error critique ($(x-2)(x+5)=8$ solved factor-by-factor — it
    produces **one correct answer, $x=3$, by luck**, which is why students trust it; and $x^2=9$
    giving only $x=3$), the same-zeros-different-equation item, and $x^3+9x=0$ for the count and type.
  - Homework 13 items (one pre-factored, four quadratics incl. a double root $x^2+8x+16$ and a
    standard-form case $x^2+3x=18$, the divide trap $2x^2=10x$, two cubics, the water balloon, the
    look-ahead) + an extension solving $x^4-16=0$ **from 1.5's own factorization** — four solutions,
    two real, two imaginary, `EI.6b` at degree four. Item 13 bridges to 1.7 by solving $x^2-4=0$ and
    naming those values the **excluded values** of $\frac{x+5}{x^2-4}$.
  - Guard sizes: bare on vocab, `[12]` hook, `[24]`/`[24]`/`[24]`/`[26]` on the four notesboxes,
    `[20]` practice, `[16]`/`[16]`/`[30]` on Tiers R/A/E, `[16]`–`[18]` on the homework's trailing
    boxes, `[18]` on the plan's Reinforcement box — the 1.2–1.5 set again, with `[26]` on the notesbox
    that **opens onto a pgfplots axis** (an axis never splits, so it needs more than the default).
  - **Boxguard finding — the gate passed and the PDF was still wrong.** `make check` reported clean
    while notes p5 held nothing but two write-lines: page parity was perfect because the *key* stranded
    the same two lines. A stub is invisible to every count, which is exactly why the PDF must be
    opened. Fixed with `\tcbbreak` before guided-practice item 3 (mirrored in `notes/` and
    `notes_key/`, with the reason in a comment in both), sending item 3 over whole. **Raising
    `\boxguard` would not have helped** — it is inert inside a breakable `tcolorbox`.
  - Page counts: cover 1, warm-up 1/1, notes 5/5, activity 3/3, exit ticket 1/1, homework 3/3;
    student and key packets 20 pages each. Plan 5 pp, slides 12 frames (4 pp printed 3-up).
  - **`pgfplots` is loaded by `atda-article` but NOT by `atda-beamer`.** The slide deck's graph frame
    needs `\usepackage{pgfplots}` + `\pgfplotsset{compat=1.18}` in the deck's own preamble. Do this in
    the lesson, never in `shared/`.
- **`unit01/lesson05` — Factoring Special Forms (`A2.EO.3b`, `A2.EO.3d`).**
  - Spine: **these are not new rules — they are shortcuts the class already earned.** 1.4's homework
    item 13 factored $x^2-9$ and $x^2+10x+25$ with the product-and-sum search, so 1.5 opens by
    *naming* two patterns the class produced itself. What a pattern buys is **speed and certainty,
    not permission** — and the cubes are the one case the search cannot reach at all.
  - **`3d` is the new code and it reframes the course's oldest habit.** "Check by multiplying back"
    stops being a check and becomes the mathematics: the notes verify $a^3-b^3=(a-b)(a^2+ab+b^2)$
    on the board, Tier E item 3 has students verify it themselves in general letters, and the
    homework extension verifies the two-variable difference of squares. The sentence being taught is
    *one calculation with letters settles every pair of numbers* — the second genuinely deductive
    move of the unit after 1.4's finite-list argument for *prime*.
  - Hook is the **square lobby with a square planter**, $A(x)=x^2-16$: the supplier quotes only
    rectangles, so the L-shaped leftover is cut and slid into $(x+4)(x-4)$ — at $x=10$, $14 \times 6
    = 84$ sq ft. The cut-and-slide is the geometric proof and is stated once, here.
  - Warm-up item 1(a) multiplies $(x+5)(x-5)$ and item 2 factors $x^2-49$; item 4 hands both back and
    asks what happens to the middle terms of $(x+b)(x-b)$ — so the difference of squares is
    *derived*, same pivot structure as 1.3 and 1.4. **Item 3 (perfect squares to $121$, cubes to
    $125$) is the diagnostic that predicts the whole period** — a student who cannot see $121=11^2$
    or $125=5^3$ recognizes no pattern today, and the fix is arithmetic.
  - Notes = 5 vocab terms (perfect square, difference of squares, perfect square trinomial, sum and
    difference of cubes, **polynomial identity**) + **four** boxes: squares
    ($x^2-36$, $x^2-121$, $9x^2-16$, $25x^2-81$, and **$x^2+49$ prime** as row 5, proved by the 1.4
    search); perfect square trinomials ($(x+6)^2$, $(x-8)^2$, $(2x+5)^2$, and **$x^2+8x+25$ prime**
    as row 4 — both ends are squares and $2ab=10x \ne 8x$, the day's most common wrong answer);
    cubes (SOAP, the identity verified, $x^3-8$ on a foam packing block checked at $x=5$ as $117$
    both ways, then $x^3+64$, $27x^3-1$, $8x^3+125$); and the finished factoring order, where
    $x^4-16=(x^2+4)(x+2)(x-2)$ finally gives "check every factor" teeth.
  - The three in-text blanks are *prime*, *twice*, *every*.
  - Context thread is one square-minus-a-square per component: notes/lobby ($x^2-16$, then
    $4x^2-49$ in guided practice, $19 \times 5 = 95$ sq ft at $x=6$); activity/stage platform
    $9x^2-25=(3x+5)(3x-5)$, $17 \times 7 = 119$ sq ft and $48$ ft of edge trim at $x=4$;
    homework/courtyard garden $25x^2-4=(5x+2)(5x-2)$, $17 \times 13 = 221$ sq ft and $60$ ft of
    fencing at $x=3$.
  - Activity tiers R/A/E; Tier E is error critique ($x^2+64=(x+8)(x-8)$ and $x^2-6x+9=(x-3)(x+3)$),
    the double difference of squares $x^4-81$, and the general-letters identity verification.
  - Homework 13 items (4 squares/PSTs, **$x^2+36$ prime**, 3 cubes incl. $8x^3+1$ where *both* $a$
    and $b$ must be read off, GCF-first $3x^3-75x$, the courtyard garden, the look-ahead) + a
    two-variable extension ($4x^2-9y^2$, factored **and verified** — `3b` and `3d` in one item).
    Item 13(b) has students reason from $(x+6)(x-6)$ to $x=6$, rejecting $x=-6$ as a length — the
    zero product property one lesson early, with no new vocabulary.
  - Exit ticket samples PST / cubes / "completely" in order; item 3 critiques $(2x+6)(x-3)$ for
    $2x^2-18$ — **the exact expression 1.4's exit-ticket note predicted**, making this the third
    appearance of one belief in three lessons ($5x(4x+6)$ → $(2x+4)(x+6)$ → $(2x+6)$).
  - Guard sizes: bare on vocab, `[12]` hook, `[24]`/`[22]`/`[24]`/`[20]` on the four notesboxes,
    `[20]` practice, `[16]`/`[16]`/`[30]` on Tiers R/A/E, `[16]`--`[18]` on the homework's trailing
    boxes, `[18]` on the plan's Reinforcement box — the 1.2/1.3/1.4 set again, extended by one
    notesbox. No `\tcbbreak` needed.
  - **Pagination finding — a guard that cannot buy a page back.** Notes run **4 pages**, with p4
    holding only the (complete) practice box. Lowering its guard to `[16]` was tested and still gave
    4 pages, so the break is the natural one, not a missed guard; the same test on the homework's
    extension box (`[18]` → `[12]`) also held at 3 pages. Both guards were restored to their
    box-sized values, since a lower guard that gains nothing only risks a stub when content shifts.
    **Test before accepting dead space, then restore the guard — that is the cheap check.**
  - Page counts: cover 1, warm-up 1/1, notes 4/4, activity 3/3, exit ticket 1/1, homework 3/3;
    student and key packets 18 pages each. Plan 5 pp, slides 13 frames (5 pp printed 3-up).
- **`unit01/lesson04` — Factoring Trinomials (`A2.EO.3b`).**
  - Spine: **nothing new is introduced today.** A trinomial has three terms; splitting the middle
    term gives four; four terms group — 1.3, unedited. The only new move is knowing *which* split
    to make. Hook is the sign shop's banner order listing area only, $A(x)=6x^2+19x+10$: unlike
    1.3's patio it has **no** common factor, so 1.3's method stalls and guessing is deliberately
    unpleasant ($ac=60$, pair $4,15$, giving $(3x+2)(2x+5)$ — at $x=2$, $8 \times 9 = 72$ sq ft).
  - Warm-up item 2 groups $2x^2+6x+5x+15$; item 4 reveals those four terms came from
    $2x^2+11x+15$, so students *derive* the $ac$ rule from their own numbers ($6+5=11$ and
    $6 \cdot 5 = 30 = 2 \cdot 15$). Same pivot structure as 1.3's item 4, one level up. Item 3
    (product/sum pairs) is the arithmetic diagnostic that predicts who stalls on $a \ne 1$.
  - Notes = 5 vocab terms (trinomial, standard form, leading coefficient, splitting the middle
    term, prime) + the $a=1$ table derived from $(x+p)(x+q)=x^2+(p+q)x+pq$
    ($(x+4)(x+5)$, $(x-3)(x-4)$, $(x+5)(x-2)$, $(x-5)(x+3)$, and **$x^2+5x+7$ prime** as row 5) +
    the $ac$ table ($(2x+1)(x+3)$, $(3x-4)(x-2)$, $(2x+5)(2x-3)$ — the third is the mixed-sign
    case) + factor-completely worked on $3x^3+21x^2+30x=3x(x+5)(x+2)$, whose inner trinomial is
    **1.3's homework item 13**. Guided practice is the second banner, $8x^2+22x+15=(4x+5)(2x+3)$,
    $17 \times 9 = 153$ sq ft at $x=3$.
  - The two in-text blanks are *opposite* and *prime*. Row 5 of box 1 is the first genuinely
    **deductive** item of the course — running out of factor pairs is a proof, not a surrender.
  - Context thread is one recovered rectangle per component: notes/sign-shop banners;
    activity/cafeteria mural $6x^2+17x+5=(3x+1)(2x+5)$, $10 \times 11 = 110$ sq ft and $42$ ft of
    border tape at $x=3$; homework/garden bed $6x^2+13x+6=(3x+2)(2x+3)$, $14 \times 11 = 154$ sq ft
    and $50$ ft of edging at $x=4$.
  - Activity tiers R/A/E; Tier R covers all four sign cases plus one $a \ne 1$. Tier E is error
    critique (incomplete $(3x+6)(x+3)$ and the sign slip $(x-4)(x-3)$), a negative-GCF item
    ($-2x^2+2x+24=-2(x-4)(x+3)$), and the finite-list proof that $x^2+4x+6$ is prime.
  - Homework 13 items (5 with $a=1$ incl. a **prime**, 4 with $a \ne 1$ incl. GCF-first
    $4x^3+14x^2+6x=2x(2x+1)(x+3)$, the garden bed, the look-ahead) + a **two-variable** extension
    ($x^2+7xy+12y^2=(x+3y)(x+4y)$ — the standard's two-variable clause). Item 13 factors $x^2-9$
    (rewritten $x^2+0x-9$) and $x^2+10x+25$ with today's search, so 1.5 opens by *naming* two
    patterns the class already produced.
  - Exit ticket samples $a=1$ / $a \ne 1$ / "completely" in order; item 3 critiques
    $(2x+4)(x+6)$ — deliberately the same belief that produced 1.3's $5x(4x+6)$, one method later.
  - Guard sizes: bare on vocab, `[12]` hook, `[24]`/`[24]`/`[20]` on the three notesboxes, `[20]`
    practice, `[16]`/`[16]`/`[30]` on Tiers R/A/E, `[16]`--`[18]` on the homework's trailing boxes,
    `[18]` on the plan's Reinforcement box — i.e. the 1.2/1.3 set, transferred verbatim again.
  - **New pagination finding — when the natural break beats `\tcbbreak`.** Notes box 2 cannot fit
    whole on a page (measured slack on p2 was $\approx 49$pt against the table's $\approx 85$pt),
    and `\boxguard` is inert inside a breakable `tcolorbox`. The natural break carries the
    *complete* fill-in table (header + three rows) to p3 — a substantial chunk, not a stub. Moving
    the split earlier with `\tcbbreak` balanced the halves but pushed notes to **4 pages** and
    stranded a single write-line alone on p4. The natural break was kept and the verdict recorded
    in a comment in both `notes/` and `notes_key/`. This is the third lesson confirming that
    `\tcbbreak` is a per-lesson judgement, never a carried convention.
  - Page counts: cover 1, warm-up 1/1, notes 3/3, activity 3/3, exit ticket 1/1, homework 3/3;
    student and key packets 18 pages each. Plan 5 pp, slides 11 frames (4 pp printed 3-up).
- **`unit01/lesson03` — Factoring: GCF and Grouping (`A2.EO.3b`).**
  - Spine: **multiplying erases the dimensions; factoring puts them back.** Hook is the blueprint
    with the dimensions erased — a patio quoted only as $A(x)=24x^2+36x$, which factors to
    $12x(2x+3)$ ($60$ ft $\times$ $13$ ft $= 780$ sq ft at $x=5$). The trap $6x(4x+6)$ is true and
    incomplete, deliberately the same structure as 1.2's $\sqrt{72}=\sqrt4\cdot\sqrt{18}$ —
    "largest, not first," one lesson later on a different object.
  - Warm-up item 2(b) has students expand $(x+2)(x^2+3)$; item 4 hands that answer back and asks
    them to group it. Grouping therefore arrives as **their own multiplication reversed**, not as a
    procedure. Item 3 (numeric GCF: $12$, $5$, $7$) is the cheap diagnostic for stopping early.
  - Notes = 5 vocab terms + GCF fill-in table ($4$, $5x^2$, $3ab$, $7x$, $-4y^2$ — including the
    two-variable and negative-GCF cases) + grouping table
    ($(x+4)(x^2+3)$, $(2x-3)(3x^2+2)$, $(x-5)(x^2-3)$, the third being the sign case) + the
    factor-completely order, worked on $2x^3+10x^2+6x+30 = 2(x+5)(x^2+3)$; guided practice is the
    deck job, $30x^2+42x=6x(5x+7)$, $24$ ft $\times$ $27$ ft $=648$ sq ft at $x=4$.
  - The two in-text blanks are *complete* and *pairing*.
  - Context thread is one recovered figure per component: notes/patio and deck; activity/two stage
    platforms sharing an edge, $6x^3+9x^2+8x+12=(2x+3)(3x^2+4)$, $7 \times 16 = 112$ sq ft at
    $x=2$; homework/shipping crate $8x^3+12x^2+10x+15=(2x+3)(4x^2+5)$, $9$ ft $\times$ $41$ sq ft
    $=369$ cu ft at $x=3$.
  - Activity tiers R/A/E; Tier E is error critique (incomplete GCF $3x^2(6x-8)$ and the sign slip
    $-2(x-3)$), a rearrange-then-group item ($2x^3-15-5x^2+6x$), and the storage-box justification
    that a factor divides the volume exactly.
  - Homework 13 items (5 GCF, 4 grouping, the crate, the look-ahead) + a binomial-GCF extension
    ($x(x+4)+3(x+4)=(x+4)(x+3)$); item 13 splits $7x$ into $5x+2x$ so $x^2+7x+10$ becomes a
    grouping problem — the engine of 1.4, with no new vocabulary.
  - Exit ticket samples GCF / grouping / "completely" in order; item 3 critiques $5x(4x+6)$, so a
    wrong item names what to reteach.
  - Guard sizes that worked first pass: bare on vocab, `[12]` hook, `[24]`/`[22]`/`[20]` on the
    three notesboxes, `[20]` practice, `[16]`/`[16]`/`[30]` on Tiers R/A/E, `[16]`--`[18]` on the
    homework's trailing boxes, `[18]` on the plan's Reinforcement box. No `\tcbbreak` needed.
  - Page counts: cover 1, warm-up 1/1, notes 3/3, activity 3/3, exit ticket 1/1, homework 2/2;
    student and key packets 16 pages each. Plan 5 pp, slides 10 frames.
- **`unit01/lesson02` — Radicals and Rational Exponents (`A2.EO.2a--c`).**
  - Spine: **a radical is 1.1's machinery run backwards.** Hook is the skid mark,
    $s=\sqrt{30fd}$: on dry asphalt ($f=0.8$) a $60$-ft skid gives $\sqrt{1440}=12\sqrt{10}
    \approx 37.9$ mph and a $240$-ft skid gives $24\sqrt{10}\approx 75.9$ — four times the skid,
    only twice the speed. 1.1 doubled a radius and quadrupled an area; 1.2 inverts it. That
    inversion recurs in the activity (fall time) and Tier E (cube edge).
  - Notes = 5 vocab terms + simplifying (fill-in table: $5\sqrt2$, $3\sqrt[3]2$, $6x^2\sqrt{2x}$,
    $2y^2\sqrt[3]{5y}$, $\tfrac74$) + rational exponents **forced by the product rule**
    ($9^{1/2}\cdot9^{1/2}=9$), conversion table ($x^{5/3}$, $y^{3/4}$, $t^{5/6}$ / $9$, $\tfrac14$,
    $27$) + the four operations incl. rationalizing; guided practice is the accident report,
    $\sqrt{1800}=30\sqrt2\approx 42.4$ mph in a $35$ zone, and $480$ ft (not $240$) to double it.
  - The three in-text blanks are *simplified*, *index*, *radicand*.
  - Context thread is one square-root model per component: notes/skid marks; activity/drop tower
    $t=\sqrt h/4$ ($h=128 \to 2\sqrt2 \approx 2.83$ s; doubling the fall needs $512$ ft, not
    $256$); homework/Kepler $T=a^{3/2}$ ($a=4\to 8$ yr exactly, Jupiter $a=5.2 \to 11.9$ yr).
  - Activity tiers R/A/E; Tier E is error critique ($\sqrt{9+16}=7$, $16^{1/2}=8$), conjugate
    rationalizing $6/(\sqrt5-2)=6\sqrt5+12$, and the $8\times$-volume/$2\times$-edge justification.
  - Homework 13 items + the gate-brace extension ($s\sqrt2$ scales linearly, $\sqrt h$ does not);
    item 13 asks for $12x^3-18x^2=6x^2(2x-3)$, framed as the same "pull out the largest factor"
    habit as simplifying $\sqrt{72}$ — so it bridges to 1.3 without new vocabulary.
  - Exit ticket samples `2a`/`2b`/`2c` in order, so a wrong item names the code to reteach.
  - Page counts: cover 1, warm-up 1/1, notes 3/3, activity 3/3, exit ticket 1/1, homework 2/2;
    student and key packets 16 pages each. Plan 5 pp, slides 10 frames.
- **`unit01/lesson01` — Simplifying Algebraic Expressions and Exponent Rules (`A2.EO.3a`).**
  - Spine: **scaling**. Hook is the Party Size popcorn tub — twice as wide and twice as tall at
    three times the price, so $\pi(2r)^2(2h)=8\pi r^2h$ is eight times the popcorn. The exponent
    on $r$ is what intuition misses; that framing recurs in the activity and homework.
  - Notes = 5 vocab terms + the five exponent rules as a fill-in "Try it" table
    ($x^{13}$, $y^7$, $c^{15}$, $16d^4$, $k^2/9$) + zero/negative exponents **derived from the
    quotient rule** + sums/differences + products; guided practice is the tray
    $V(x)=x(10-2x)(8-2x)=4x^3-36x^2+80x$.
  - The three in-text blanks are *coefficient*, *negative*, *every*; box 4's count is *six*.
  - Context thread is concession/retail profit: notes $P(x)=-10x^2+170x-340$, $P(8)=380$;
    activity (school store) $P(x)=-6x^2+99x-195$, $P(6)=183$, $P(0)=-195$ as a justification
    item; homework (hot dogs) $P(x)=-12x^2+204x-510$, $P(5)=210$. Each verified against its story.
  - Activity tiers R/A/E; Tier E is error critique ($(4x^3)^2$, $(2m+3)^2$), cube scaling
    ($27\times$ volume, $9\times$ surface), and the negative-profit justification.
  - Homework 12 items + a surface-area-to-volume extension ($6s^2/s^3=6/s$); item 12 asks
    students to *check* $7x^3$ by squaring, so it bridges to 1.2 without needing a radical symbol.
  - Page counts: cover 1, warm-up 1/1, notes 4/4, activity 3/3, exit ticket 1/1, homework 3/3;
    student and key packets 18 pages each. Plan 5 pp, slides 10 frames.
- **`unit01/lesson00` — Unit 1 opener (no new content).**
  - Spine: one quadratic model, two equivalent forms —
    $h(t)=-16t^2+48t+64 = -16(t-4)(t+1)$ (fireworks shell off a 64-ft cliff). Expanded form
    shows the launch height, factored form shows the landing time; neither is "better."
  - Warm-up = the **Unit 1 diagnostic**, five items, one per prerequisite skill
    (exponent rules → 1.1, binomial product → 1.1/1.4, GCF → 1.3, linear equation → 1.6,
    evaluate-in-context → everywhere). Miss-rate per item drives the do-now for that lesson.
  - Notes = vocabulary preview (5 terms) + equivalence check + **Unit 1 roadmap table** with a
    Confident/Rusty/New self-assessment column; guided practice is the garden model
    $A(x)=x(40-2x)$.
  - Activity = spirit-wear revenue model $R(x)=x(120-4x)$, tiers R/A/E; Tier E is error
    critique + symmetry to the max ($x=15$, $R=900$).
  - Homework = the three diagnostic skills with new numbers, a softball model
    $-16(t-3)(t+1)$, a first exponential ($A(t)=500(1.04)^t$), number-trick extension.
  - Page counts: cover 1, warm-up 1/1, notes 3/3, activity 2/2, exit ticket 1/1, homework 2/2;
    student and key packets 14 pages each. Plan 4 pp, slides 9 frames.
- **Conventions learned while authoring 1.0 — apply these from lesson 1.1 on:**
  1. **Consecutive `\writeline`s collide.** `\writeline` opens with a no-op `\noindent`, so two
     in a row land on one line and one placed straight after prose fills the rest of that line.
     Use `\writelines{n}`, and put a **blank line before it**. In the key, mirror with
     `\ansline{...}\\` per line (a `work` block or `\termblanklong` already ends the paragraph,
     so a single `\writeline` after one is fine).
  2. **`\boxguard` is inert inside a breakable `tcolorbox`.** The activity's Tier A box broke
     leaving a two-line stub at the top of page 2; `\tcbbreak` at a chosen item fixed it.
     Mirror it in the blank and the key.
  3. The **lesson plan needs guards too** — its Reinforcement box stranded the word
     "properties." atop page 4 until `\boxguard[18]` went in front of it.
  4. Vocab answers are shorter than `\termblanklong`'s two write-lines, so a key can pull a box
     onto an earlier page than the blank. Harmless as long as **total** pages match — that is
     all `make check` measures.
- **Conventions learned while authoring 1.1 — the boxguard tuning rule:**
  1. **Size each guard to its own box, not to a habit.** Guessing high (`[20]`–`[28]`) on boxes
     that are only 10–15 lines tall pushed each one to the next page and left roughly a third of
     notes pp. 1–2 blank. `make check` never sees this — page *parity* held the whole time. The
     working rule: for a box shorter than a page, set the guard to about its own height so it
     moves whole only when it genuinely does not fit; for a long breakable box, use `[16]` so a
     break still leaves a substantial chunk.
  2. **The opposite error is worse, so tune in that order.** Dropping every guard to `[16]` and
     deleting 1.0's `\tcbbreak` closed the dead space but stranded Tier E item 3 alone atop
     activity p3 and the remind box alone atop homework p3. Fix by pushing the *whole* box down
     (`\boxguard[30]` on Tier E, `[24]` on the extension box), not by re-breaking it. A page
     holding one complete box with an empty lower third is correct; a page holding a sliver is not.
  3. `\tcbbreak` is **not** automatically worth carrying between lessons — in 1.0 it saved a stub,
     in 1.1 the same move cost half a page. Re-measure it per lesson.
  4. Guards must be re-measured after *any* content change, and always applied to blank and key
     together (a scripted pass keyed on the guard line plus the following `\begin{...}` line is
     the reliable way; note `tcolorbox` options can push the title onto the *second* line).
- **Conventions confirmed while authoring 1.2 — the guard sizes that worked:**
  1. The 1.1 tuning rule ("size each guard to its own box") produced a clean first pass with no
     re-measuring. Working values for a lesson of this shape: `\boxguard` bare on the vocab box,
     `[12]` on a hook box with two write-lines, `[20]`–`[24]` on a full notesbox carrying a
     fill-in table plus `work` blocks, `[16]` on Tier R/Tier A, `[30]` on Tier E, `[14]`–`[22]`
     on the homework's trailing scenario/extension boxes.
  2. **No `\tcbbreak` was needed** — consistent with the 1.1 finding that it is a per-lesson
     judgement, not a carried convention.
  3. A tall `tabularx` inside a breakable `skillbox` will move the *whole* box, because the table
     itself cannot split. That is why the lesson plan's page 1 ends with roughly a third empty —
     correct behaviour, not a missed guard.
- **Confirmed while authoring 1.3:** the 1.2 guard sizes transferred verbatim to a lesson of the
  same shape (listed in the 1.3 entry above) with no re-measuring and no `\tcbbreak`. Treat that
  set as the default opening bid for an ordinary Unit 1 lesson, then tune per box.
- **Everything else is still scaffold skeletons**: units 03–08 in full, plus every unit's `tests/`,
  `test_keys/`, `sample_test/`, `sample_test_key/` (Unit 1's excepted) and Unit 2's `unit_cover`
  pair.
- **Unit 1 is the only unit with a `unit_cover/` pair or authored tests.** `finals/` has not been
  created.
- Lessons 1.0–1.6 are merged to `main` (PR #4, commit `ca47f7e`; PR #6, commit `248c0c8`; PR #8,
  commit `6a72235`; PR #9, commit `c6b1e1d`; PR #10, commit `5c04bb1`). Lesson 1.7 is merged
  (PR #11, commit `6578d42`); the Unit 1 cover pair and the four test files are merged
  (PR #12, commit `4ba8611`). Lessons 2.0–2.6 are merged to `main` (2.6 via PR #19, commit
  `535a5c3`). **Lesson 2.7 is on worktree branch `claude/lesson-planning-2-7-00ca0b`, built and
  gated, not yet committed.**

## Next steps

1. Commit / PR **Unit 2's summative layer** (user to confirm) — `unit02/unit_cover/`,
   `unit02/unit_cover_key/`, the four test files, **and the two published PDFs
   `unit02/sample_test/main.pdf` and `unit02/sample_test_key/main.pdf`**, which `unit.mk` reads from
   the source tree and which a fresh clone cannot merge the unit packets without. Lesson 2.7 is
   already merged to `main`.
2. **Units 1 and 2 are both complete end to end.** Nothing is outstanding in either.
3. Author **Unit 3 — Exponential and Logarithmic Functions**, opening
   with **Lesson 3.0 (unit opener: growth stories; diagnostic)**. 2.7's plants are already down for
   it: the **common ratio** is named and drilled, the **horizontal asymptote at $y=0$** has now
   decided a real question twice (the truck at year 8, the decay stories in homework item 10), and
   homework item 10 is a growth-or-decay-plus-multiplier table that is literally 3.1's warm-up.
   **The multiplier confusion to fix on day one of Unit 3** — flagged in 2.7's homework note — is
   students writing "$10\%$" where the model needs "$1.10$".
4. **Every Unit 2 lesson is a graph-reading lesson — pre-draw and pre-scale every axis.** 2.0's
   seven `pgfplots` figures are the model for style (`axis lines=left`, `grid=both` at
   `linegray!45`, `\scriptsize` tick/label fonts, `royal` plot, integer-friendly tick marks).
   **2.3 settled the no-sketching pattern for the rest of the unit** and it should be reused
   verbatim: a pre-drawn, pre-scaled grid with **the parent already plotted**, a table of image
   points to complete, and "plot your five points and join them" — with **the key adding the image
   curve plus an `only marks` plot inside the same axis**, so the axis dimensions and therefore the
   page parity are unchanged. Also carry 2.3's grid distinction: **a grid meant for plotting needs a
   gridline at every integer; a grid meant for reading needs sparse tick labels plus
   `minor x/y tick num`** so values land on a visible line without crowding the labels.
5. **Unit 3's cover and tests now have two models, and Unit 2's is the one to copy for any
   graph-heavy unit.** Carry over from `unit02`: the four-part 100-point blueprint,
   Part C's one-item-per-content-lesson spine, `work`-blocks-not-`\vspace` for parity, `\parthead`
   carrying `\boxguard[9]`, the shared `\pgfplotsset{testaxis/.style={...}}` defined identically in
   all four files, and the rationale on `unit_cover_key` page 2. Three lessons specific to a test
   with figures: **design every graph backwards from integer zeros** (check each segment's slope
   divides evenly before drawing); **`\workrowsep` may have no acceptable setting** — Unit 2's swept
   6pt$\to$0pt and only 2pt bought a page, which is unusable writing room, so guards did the work
   instead; and **guard the stem of every figure item and every item whose work block is tall**,
   because in the blank a work block is a `\vphantom`, so an answer space split across a page break
   is literally invisible until you look at the rendered PDF.
6. The model now holds across sixteen lessons. If the parallel-dispatch pattern is used from here on
   (coordinator scaffolds, one subagent per lesson, coordinator builds and gates), give each agent
   the boxguard tuning rule, the 1.2–1.7 guard sizes above, 1.5's "test the guard, then restore it"
   finding, **and 1.6's and 1.7's finding that `make check` passes on a stranded stub** — guard
   placement is the one thing no automated check can catch, so the coordinator must open every PDF.
   Tell them a `teachernote` in the plan needs a guard too (1.7), that `\ans` cells holding
   fractions need `\dfrac` (1.7), and — from 2.0 — that a guard must **exceed** its box, never
   approximate it, and that **no `\tcbbreak` may be authored until a build proves it is needed**.
   From 2.1, add the `tabularx` rule: **put the `X` column on the prose column, not on the last
   notation column**, or all the slack lands in one place and the words wrap. From 2.2, add three:
   **every box in the lesson plan needs a guard, not just the trailing ones** (its Individual Work
   box stranded a line); **a tall `\ans` in a table cell needs a shared strut in the blank** so the
   row height cannot differ; and **check `Overfull \vbox` in the deck's log**, since a wide
   Beamer table silently overruns the frame. From 2.3, add three more: **never combine a pgfplots
   `title` with a legend placed above the axis** (the legend overprints the title, and no check or
   page count can see it — use one caption sentence under a multi-panel row instead); **`\workrowsep`
   does not always buy a page back** (swept 8pt$\to$0pt on 2.3's homework with no change, the
   counter-case to Unit 1's tests), so when a trailing box strands, reach for a `\tcbbreak` that
   sends a *substantial* chunk over rather than shaving row separation; and **five teachernotes at
   full length overflow a 5-page plan** — a complete note alone on a final page is dead space, not a
   boxguard violation, and is worth accepting once pp. 3–5 are measured full. From 2.4, add two:
   **a table header carrying a parenthetical qualifier must be broken explicitly with `\newline`**,
   or at `\small` it overruns its column and wraps mid-parenthesis (no check and no page count sees
   it); and **measure the boxes before reaching for a guard** — when every box in a component is
   taller than half a page, half-empty pages are arithmetic, not a guard problem, and no guard
   setting will reclaim them. From 2.5, generalize 2.4's header rule and add one: **any two-word
   header near its column width needs an explicit `\newline`** (not just a parenthetical one — 2.5's
   "Horizontal asymptote" wrapped mid-word as "asymp-/tote"), and **a table's label column must be
   wide enough to hold its longest entry on one line**, or it breaks in the wrong place (2.5's
   `p{1.5cm}` split "(b) $y=2x-4$" after the equals sign). Both are invisible to `make check` and to
   every page count; only the rendered PDF shows them. From 2.6, add three: **never pull text up
   under a `\[...\]` display on a Beamer frame with a negative `\vspace`** — 2.6's notation frame
   overprinted its paragraph's first two lines while `grep Overfull` on the deck log returned
   **zero**, so shrink the figure instead and *eyeball the deck, not just the components*;
   **a figure and the question that reads it must not straddle a page break** (2.6's homework item 4
   put the stem and graph on p1 and the question plus all four answer lines on p2 — the same defect
   family as 2.4's item 4 and 2.5's item 8, and `\tcbbreak` fixed it free); and **when a guard change
   produces no change at all, the break is natural and the guard is not the lever** — measure the
   box's first unbreakable chunk against the page's free space before touching the number, which is
   2.4's rule in its sharpest form. **From 2.7, add three, and the first is the most general finding
   of the unit:** (a) **a nearly blank page is a boxguard violation** — 2.7's activity p4 held one
   write-line and nothing else because Tier E overran p3 by a single line plus its closing rule, and
   `make check` passed at 4/4 because the key stranded identically; scan every component's *last*
   page, not just its break points. (b) **`\ansline` \emph{width} can cost a page even when every
   `\writelines{n}` is matched by exactly $n$ answer lines** — 2.7's homework key came out 5 against
   4 because thirteen `\ansline`s wrapped to two printed lines each. Diagnose it by grepping
   `pdftotext -layout` output for answer lines carrying **no dotted trail** (a wrapped `\ansline`
   trails only on its last line), then trim to one line each; widening a column an `\ans` cell
   overflows and shortening shared prose such as the `remindbox` both shrink the key **without**
   costing the blank a page, which is the only kind of saving that closes a parity gap. (c) **a
   Beamer table can hyphenate a cell mid-word at projection size** (`flat-tens`, `ver-tex`) with the
   deck log clean — the second deck defect in a row that `grep Overfull` cannot see.
7. **Unit tests and unit covers are outside `make check`** — the gate walks `unitXX/lessonMM/` only.
   For every later unit, check by hand what the gate would have caught: blank/key page parity on
   both test forms, no `teachernote` in any test key, no `\ans` inside math. The Unit 1 run's two
   real findings were *both* boxguard problems that no count could see (a stub page, and a split
   multiple-choice item), so **open all four test PDFs page by page** — that is the only way.
8. Down the road: `finals/` (cumulative final, balanced Algebra/Data/Trig per the blueprint
   guidance in the skill). Unit 1's Part D prompts are the model for the final's synthesis items.

### Open questions

- None pending. The unit-opener component shape is demonstrated by `unit01/lesson00` and
  `unit02/lesson00` (the latter is the model for a **graph-reading** opener), and the
  ordinary-lesson shape by `unit01/lesson01`; reuse them rather than re-deriving.
