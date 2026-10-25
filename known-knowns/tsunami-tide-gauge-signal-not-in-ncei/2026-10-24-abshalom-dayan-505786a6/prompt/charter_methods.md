# Research charter (methods only; thesis, quarries and self-critique not published)

## Lenses

1. **key:** constructor · **title:** Build from structure · **skeptic:** no
   Choose a structured family (restrictions of larger schemes, group orbits, lattices from codes, symmetric seeds) where the objective has a fast exact evaluator, reason about which parameters could beat the record, then search only that family. Dead when the family's best provably cannot reach the record.

2. **key:** optimizer · **title:** Warm-start from the record · **skeptic:** no
   Start from the current record object, perturb and polish with an exact objective (flip-graph walks, active-set or SLSQP polishing followed by exact certification). Dead when long runs plateau at the record across three seeds.

3. **key:** solver · **title:** Let a solver argue · **skeptic:** no
   Encode the cell as SAT, ILP or a polynomial system with symmetry breaking you can justify, and keep every certificate. Dead when encodings time out at sizes below what a record needs.

4. **key:** object-as-data · **title:** Read the record holder · **skeptic:** no
   Treat the current best object as data: invariants, symmetries, near-misses and slack; find regularities its authors did not use. Dead when local moves around the record all lose.

5. **key:** evaluator-first · **title:** Exact, fast, twice · **skeptic:** no
   Spend the first hour on a fast exact evaluator and a second independent one; test both on the record holder and on seeded flawed objects. Floats only for search.

6. **key:** already-settled · **title:** Prove it is not new · **skeptic:** yes
   Assume the cell is already beaten: read the live table, its pending submissions, the public repositories the bank names, arXiv for the last 6 months, this repo's TROPHY_CASE.md, known-knowns and open pull requests. Dead (for the cell) when it is listed or claimed.

## Scout voice

Read the live record table first and copy the exact current value, its source and fetch time; then every secondary source the bank names. Treat cells this repo's contributors improved, or that open pull requests claim, as taken.

## Attacker voice

Reason first about which structure could win and why, then let code do the counting. One certified record beats ten near misses; move on fast from a plateau and say exactly what was searched.

## Heuristics

1. Exact arithmetic or an interval certificate decides; floats only search.
2. Two independent exact checkers before believing any object.
3. Seed from the record holder.
4. Prefer cells where the checker runs in seconds.
5. A tie is not a record; one cell per claim.
6. Re-read the live cell right before claiming.
7. Compare against the sorted or canonical form of the cell (permutations, transposes, rotations).
8. Pick cells the active record-chasers are not working this week.

## Kill criteria

1. The two exact checkers disagree and it cannot be resolved.
2. The live cell or a public repository already equals or beats the object.
3. The cell is improved in this repo, an open pull request or the literature.
4. Search plateaus at the record across three distinct seeds.
5. The exact check cannot run at the cell's size on one laptop.
6. A claimed exhaustive search turns out capped.

## Method cards used

construct-space · structured-family · object-as-data · solver (chosen for a reasoning-heavy weekend push aimed at widely recognised problems, not drawn at random)
