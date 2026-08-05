# ATDA Course Planning Log

The running handoff log for the lesson-planning skill. Read at the start of every run,
update at the end. Overwrite stale entries — this is a state file, not a changelog.

## Last updated

**2026-08-04** — Authored **Unit 1 Lesson 1.0 (Unit Opener: Why Algebra Fluency Matters)** in
full: lesson plan, cover, warm-up, guided notes, group activity, exit ticket, homework, all
five keys, and the slide deck. `make -C unit01/lesson00 all` and `make -C unit01/lesson00 check`
both pass; PDFs eyeballed for boxguard. **This is now the course's model lesson** — open it
before authoring anything else.

## Current state

- **Structure (user-approved 2026-08-04):** 8 units, Algebra (U1–3) → Data (U4–6) → Trig
  (U7–8). Every unit has a **Lesson X.0 unit opener** (hook + prerequisite diagnostic +
  vocab preview + roadmap, no new content). 59 lessons total. Full lesson maps with standard
  codes live in `spec/algebra_trig_data_analysis.md` ("The lesson maps"). The restructure and
  the scaffolds are merged to `main` (commits `b8addef`, `99a8c19`).
- **Authored (1 of 59): `unit01/lesson00`.** Every component written, built, and gated.
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
- **Everything else is still scaffold skeletons**: unit01 lessons 1.1–1.7, units 02–08 in full,
  plus each unit's `tests/`, `test_keys/`, `sample_test/`, `sample_test_key/`.
- No `unit_cover/` pair exists for any unit yet, and `finals/` has not been created.
- Work is on worktree branch `claude/lesson-planning-generate-12f8bf`, **not yet committed**.

## Next steps

1. Commit / PR Lesson 1.0 (user to confirm).
2. Author **Unit 1 Lesson 1.1 — Simplifying Algebraic Expressions and Exponent Rules**
   (`A2.EO.3a`), mirroring 1.0's structure and voice. Lesson 1.0's homework and slides both
   promise it as the next lesson.
3. Then 1.2–1.7 in order; consider the parallel-dispatch pattern (coordinator scaffolds, one
   subagent per lesson, coordinator builds and gates) once 1.1 confirms the model holds.
4. After the Unit 1 lessons: author `unit01/tests/` (practice + actual) and `unit01/test_keys/`,
   and add the `unit01/unit_cover/` + `unit_cover_key/` pair (the test rationale and Part D
   scoring go on page 2 of the key cover, never in a test key).
5. Down the road: `finals/` (cumulative final, balanced Algebra/Data/Trig per the blueprint
   guidance in the skill).

### Open questions

- None pending. The unit-opener component shape is now demonstrated by `unit01/lesson00`; reuse
  it for lessons 2.0, 3.0, … rather than re-deriving it.
