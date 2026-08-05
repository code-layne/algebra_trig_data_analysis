# ATDA Course Planning Log

The running handoff log for the lesson-planning skill. Read at the start of every run,
update at the end. Overwrite stale entries — this is a state file, not a changelog.

## Last updated

**2026-08-04** — Course restructure approved and executed: rewrote
`spec/algebra_trig_data_analysis.md` to the 8-unit bridge-course map and **scaffolded the
entire course** (59 lessons + unit test skeletons for all 8 units). Smoke-tested
`unit01/lesson00`: `make all` and `make check` both pass. Nothing is authored yet — every
component is a scaffold skeleton.

## Current state

- **Structure (user-approved 2026-08-04):** 8 units, Algebra (U1–3) → Data (U4–6) → Trig
  (U7–8). Every unit has a **Lesson X.0 unit opener** (hook + prerequisite diagnostic +
  vocab preview + roadmap, no new content). 59 lessons total. Full lesson maps with standard
  codes live in `spec/algebra_trig_data_analysis.md` ("The lesson maps").
- **Approved decisions:** (1) sinusoidal-graphs survey included as lesson 8.7 (T.GT.1), with
  CT.1a–d merged into 8.1 to fit the 8-lesson cap; (2) Algebra→Data→Trig ordering; (3) A2/PS
  SOL codes cite Units 1, 3, 5 content — the four A2/PS PDFs are now in `spec/`.
- **Scaffolded (all skeletons, zero authored):** unit01–unit08, every lesson dir with the
  full component set (cover, warmup, notes, activity, exit_ticket, homework, slides + keys),
  plus each unit's `tests/`, `test_keys/`, `sample_test/`, `sample_test_key/`. Root and unit
  Makefiles in place. 799 `main.tex` files on disk.
- **Verified:** `make -C unit01/lesson00 all` → all five products; `make -C unit01/lesson00
  check` → passes. Other lessons are identical skeletons and were not individually built.
- **No model lesson exists yet** — nothing is authored. The first authored lesson becomes
  the course model; build and proofread it carefully.
- Work is on worktree branch `claude/atda-course-structure-0e9508`, **not yet committed**.

## Next steps

1. Commit/PR the restructure + scaffolds (user to confirm).
2. Author **Unit 1 Lesson 1.0** (Unit Opener: Why Algebra Fluency Matters) or **1.1** as the
   course's model lesson — read `spec/12AFDAUnderstanding the Standards.pdf` (n/a for U1;
   use the A2 SOL) and the relevant Understanding pages first.
3. Then scale out Unit 1 lessons 1.1–1.7, then the Unit 1 practice/actual tests.
4. Down the road: `finals/` (cumulative final, balanced Algebra/Data/Trig per the blueprint
   guidance in the skill).

### Open questions

- None pending. Unit opener component shape (warmup = diagnostic, notes = vocab preview +
  roadmap, activity = hook scenario) is documented in the spec's "Mapping content into a
  lesson" section.
