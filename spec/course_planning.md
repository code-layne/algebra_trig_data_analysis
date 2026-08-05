# ATDA Course Planning Log

The running handoff log for the lesson-planning skill. Read at the start of every run,
update at the end. Overwrite stale entries — this is a state file, not a changelog.

## Last updated

**2026-08-04** — Authored **Unit 1 Lesson 1.4 (Factoring Trinomials, `A2.EO.3b`)** in full:
lesson plan, cover, warm-up, guided notes, group activity, exit ticket, homework, all five keys,
and the slide deck. `make -C unit01/lesson04 all` and `make -C unit01/lesson04 check` both pass
(`✓ check passed — 1 lesson, no convention violations`); every page of both packets and the plan
eyeballed for boxguard. All 45 factorizations verified in pure Python (random rational evaluation)
before authoring, including that every $ac$-pair used in the lesson is **unique**. The structural
model set by 1.0--1.3 held, with one new pagination finding recorded under 1.4 below.

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
- **Authored (5 of 59): `unit01/lesson00`, `unit01/lesson01`, `unit01/lesson02`,
  `unit01/lesson03`, `unit01/lesson04`.** Every component written, built, and gated.
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
- **Everything else is still scaffold skeletons**: unit01 lessons 1.5–1.7, units 02–08 in full,
  plus each unit's `tests/`, `test_keys/`, `sample_test/`, `sample_test_key/`.
- No `unit_cover/` pair exists for any unit yet, and `finals/` has not been created.
- Lessons 1.0–1.3 are merged to `main` (PR #4, commit `ca47f7e`, PR #6, commit `248c0c8`). Lesson
  1.4 is on worktree branch `claude/lesson-1-4-generation-76a895`, **not yet committed**.

## Next steps

1. Commit / PR Lesson 1.4 (user to confirm).
2. Author **Unit 1 Lesson 1.5 — Special Forms** (`A2.EO.3b, d`): difference of squares, sum and
   difference of cubes, perfect square trinomials. Lesson 1.4's homework item 13, its remind box,
   and its closing slide all promise it — item 13 already has students factor $x^2-9$ (rewritten
   $x^2+0x-9$) into $(x+3)(x-3)$ and $x^2+10x+25$ into $(x+5)^2$ with the product-and-sum search,
   so 1.5 opens by *naming* two patterns the class has already produced, then adds the cubes.
3. Then 1.6–1.7 in order. The model now holds across five lessons, so the parallel-dispatch
   pattern (coordinator scaffolds, one subagent per lesson, coordinator builds and gates) is
   reasonable to try — but give each agent the boxguard tuning rule and the 1.2/1.3 guard sizes
   above, since guard sizing is the one thing `make check` cannot catch.
4. After the Unit 1 lessons: author `unit01/tests/` (practice + actual) and `unit01/test_keys/`,
   and add the `unit01/unit_cover/` + `unit_cover_key/` pair (the test rationale and Part D
   scoring go on page 2 of the key cover, never in a test key).
5. Down the road: `finals/` (cumulative final, balanced Algebra/Data/Trig per the blueprint
   guidance in the skill).

### Open questions

- None pending. The unit-opener component shape is demonstrated by `unit01/lesson00` and the
  ordinary-lesson shape by `unit01/lesson01`; reuse them rather than re-deriving.
