# fmm-catalogue-small-format-rank: partial win p1, <18,19,19> rank 3424 over Q

## What
The files in claim/object/ define a bilinear scheme over Q for <18,19,19> (A 18x19 times B 19x19) with 3424 rank-one terms, each with three nonzero factors, satisfying all 42224004 Brent equations in exact arithmetic, and 3424 is strictly below the rank 3633 for (18,19,19) in the live fmm_sota.json and the rank 3816 on the live Lille page 18x19x19.html (both fetched for the claim at 2026-10-24T17:37:57Z and re-fetched unchanged at 2026-10-24T18:18:21Z) and below the 3633 of the only listed Lille construction Proj([[19, 0], [0]], <19x19x19:3633>) (index fetched 2026-10-24T15:58:56Z), so it meets partial win p1 of fmm-catalogue-small-format-rank and not the main criterion.

Status: CONFIRMED_PARTIAL (p1), three-skeptic panel (panel/). The scheme comes from Khoruzhii, Serafin, Gelss and
Pokutta's published LITA 19x19x19 rank-3633 scheme by one exact one-slice restriction (208 terms vanish) and one
exact 2-reduction; the rebuild is deterministic and byte-identical (how-we-built-it/COMMANDS.md).

## Check it yourself
    sh verify-it-yourself/run_checks.sh
Expected last line: `PASS`. Needs only python3 (standard library), no network; about 45 seconds on a laptop. It
joins object/u.part1.txt and object/u.part2.txt into u.txt (the 1 MB per-file limit), prints the three sha256 values
(u.txt 47419363...298a, the file the panel checked), checks all 42,224,004 Brent equations exactly, and runs three
exact random evaluations. RUN_IT_YOURSELF.md has the full expected output.

## Compared to
| table | cell | value | URL | fetched (UTC) |
|---|---|---|---|---|
| fmm_sota.json (Lille catalogue digest) | [18, 19, 19] | 3633 | https://raw.githubusercontent.com/sedoglavic/fmm_digest/master/fmm_sota.json | 2026-10-24T17:37:57Z (unchanged at 18:05:47Z and 18:18:21Z) |
| Lille per-format page | <18x19x19> | 3816 | https://fmm.univ-lille.fr/18x19x19.html | 2026-10-24T17:37:57Z (unchanged at 18:05:47Z and 18:18:21Z) |
| Lille catalogue index | row 18x19x19 | 3633, construction Proj([[19, 0], [0]], <19x19x19:3633>) | https://fmm.univ-lille.fr/ | 2026-10-24T18:05:46Z |
| matmulcatalog docs/catalog.json (lowest other public value) | [18, 19, 19] | 3595 | https://raw.githubusercontent.com/solven-eu/matmulcatalog/master/docs/catalog.json | 2026-10-24T18:06:50Z |

Snapshots with sha256 and headers: the-record-we-beat/RECORD.md.

## Not claimed
- Not the main criterion: max(18,19,19) = 19 > 16. Partial win p1 only.
- Not the tensor rank of <18,19,19>: 3424 is an upper bound (a scheme with 3424 multiplications), not a proof that
  fewer are impossible.
- Not a ring upgrade: the coefficients are rationals (denominators up to 1200); nothing is claimed over Z or GF(2).
- Not a new method: the slice-and-reduce step uses the published LITA scheme; the record is the value 3424 for this
  format, which no table, catalogue, pull request or paper we could read lists (lowest found: 3595).
- The run also built <18,18,19> at 3225 (fmm_sota.json 3355); it is not part of this package (one cell per package).

## Credits
- Kirill Khoruzhii, Luzian Serafin, Patrick Gelss and Sebastian Pokutta, Local Improvements to Trilinear Aggregation
  (LITA), https://github.com/khoruzhii/lita: the 19x19x19 rank-3633 scheme this one is restricted from.
- Alexandre Sedoglavic, the Lille fast matrix multiplication catalogue, https://fmm.univ-lille.fr/, and its digest
  https://github.com/sedoglavic/fmm_digest.
- Chatain Lacelle, matmulcatalog (arXiv 2606.13408), https://github.com/solven-eu/matmulcatalog.
- Perminov (dronperminov), FastMatrixMultiplication, https://github.com/dronperminov/FastMatrixMultiplication, and
  MerlijnW70/fmm-schemes, https://github.com/MerlijnW70/fmm-schemes (checked; neither covers max dimension 19).
- Contributor: Abshalom Dayan (V3R1T4S run).
