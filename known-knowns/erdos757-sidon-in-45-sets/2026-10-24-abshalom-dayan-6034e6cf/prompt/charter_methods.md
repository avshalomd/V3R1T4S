# Research charter (methods only; thesis, quarries and self-critique not published)

## Lenses

1. **key:** constructor · **title:** Build from structure · **skeptic:** no
   Choose a structured family (Cayley-type sets, digit masks, products, orbits under a group) where the objective has a closed form or a fast exact evaluator, reason about which parameters could beat the record, then search only that family. Dead when the family's best provably cannot reach the record.

2. **key:** small-cases · **title:** Solve tiny cases exactly, then lift · **skeptic:** no
   Settle the smallest instances exhaustively with a certificate, tabulate optima, and look for the pattern a product or recursion could lift. Dead when the small optima already sit below what lifting needs.

3. **key:** solver · **title:** Let a solver argue · **skeptic:** no
   Encode the question as SAT, ILP or CP with symmetry breaking you can justify, and keep every UNSAT proof (DRAT/LRAT) and every SAT witness. Dead when encodings time out at sizes below what a record needs.

4. **key:** object-as-data · **title:** Read the record holder · **skeptic:** no
   Treat the current best object as data: compute its invariants, automorphisms and near-misses, and find regularities its authors did not use; perturb from there. Dead when local moves around the record all lose.

5. **key:** evaluator-first · **title:** Exact, fast, twice · **skeptic:** no
   Spend the first hour on a fast exact evaluator and a second independent one; test both on the record holder and on seeded flawed objects. Search speed and checker trust are the edge.

6. **key:** already-settled · **title:** Prove it is not new · **skeptic:** yes
   Assume the quarry is answered: read the live page, the forum thread and proof-claims, arXiv for the last 24 months, and this repo's TROPHY_CASE.md, known-knowns and open pull requests. Dead (for the quarry) when the record has moved past reach or the question is settled.

## Scout voice

Read the live record page first and copy the exact current value and its source; then the forum thread from the newest post backwards. Note any value with an asterisk or an unverified formalisation as provisional.

## Attacker voice

Reason first about which structure could possibly win and why, then let code do the counting. Prefer one certified object over many near misses, and say exactly what part of a space was searched.

## Heuristics

1. A record in exact arithmetic or nothing; floats only for search.
2. Two independent exact checkers before believing any object.
3. Seed the search with the record holder.
4. Products and tensor powers turn small dense seeds into rates.
5. Symmetry shrinks search; break it on purpose before claiming exhaustiveness.
6. A tie is not a record.
7. Write the record's exact value as a Fraction before comparing.
8. One object per claim.

## Kill criteria

1. The best object in the chosen family provably falls short.
2. The two exact checkers disagree and the disagreement cannot be resolved.
3. The live record has moved past what the family can reach.
4. The question is settled on the forum or in print.
5. Search sizes needed exceed one laptop in a week of nights.
6. A claimed exhaustive search turns out capped.

## Method cards used

construct-space · structured-family · object-as-data · solver (chosen for the weekend push, not drawn at random)
