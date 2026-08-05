# ATDA Course Planning Log

The running handoff log for the lesson-planning skill. Read at the start of every run,
update at the end. Overwrite stale entries — this is a state file, not a changelog.

## Last updated

**2026-08-04** — Authored **Unit 1 Lesson 1.1 (Simplifying Algebraic Expressions and Exponent
Rules, `A2.EO.3a`)** in full: lesson plan, cover, warm-up, guided notes, group activity, exit
ticket, homework, all five keys, and the slide deck. `make -C unit01/lesson01 all` and
`make -C unit01/lesson01 check` both pass; every page of every blank, plus key spot-checks,
eyeballed for boxguard. All arithmetic verified in Python before authoring. Lesson 1.0 remains
the structural model; 1.1 confirms it holds.

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
- **Authored (2 of 59): `unit01/lesson00`, `unit01/lesson01`.** Every component written, built,
  and gated.
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
- **Everything else is still scaffold skeletons**: unit01 lessons 1.2–1.7, units 02–08 in full,
  plus each unit's `tests/`, `test_keys/`, `sample_test/`, `sample_test_key/`.
- No `unit_cover/` pair exists for any unit yet, and `finals/` has not been created.
- Lesson 1.0 is merged to `main` (PR #4). Lesson 1.1 is on worktree branch
  `claude/lesson-1-1-generation-460932`, **not yet committed**.

## Next steps

1. Commit / PR Lesson 1.1 (user to confirm).
2. Author **Unit 1 Lesson 1.2 — Radicals and Rational Exponents** (`A2.EO.2a–c`). Lesson 1.1's
   homework item 12, its remind box, and its closing slide all promise it as the next lesson,
   and its notes explicitly set up "the same exponent rules survive fractional exponents."
3. Then 1.3–1.7 in order. The model now holds across two lessons, so the parallel-dispatch
   pattern (coordinator scaffolds, one subagent per lesson, coordinator builds and gates) is
   reasonable to try — but give each agent the boxguard tuning rule above, since guard sizing is
   the one thing `make check` cannot catch and it cost the most iteration on 1.1.
4. After the Unit 1 lessons: author `unit01/tests/` (practice + actual) and `unit01/test_keys/`,
   and add the `unit01/unit_cover/` + `unit_cover_key/` pair (the test rationale and Part D
   scoring go on page 2 of the key cover, never in a test key).
5. Down the road: `finals/` (cumulative final, balanced Algebra/Data/Trig per the blueprint
   guidance in the skill).

### Open questions

- None pending. The unit-opener component shape is demonstrated by `unit01/lesson00` and the
  ordinary-lesson shape by `unit01/lesson01`; reuse them rather than re-deriving.
