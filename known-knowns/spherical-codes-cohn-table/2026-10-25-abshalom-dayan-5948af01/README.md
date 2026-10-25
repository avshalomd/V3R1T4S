# (6, 575) spherical code: a 575-point code in R^6 with a larger minimal angle than the table's

## What

The 575 vectors in object/code_6_575.txt (26 significant digits per coordinate), each normalised in mpmath at 50 digits, have maximum pairwise cosine c* = 0.7926798356844868804983 (22 significant digits), which is 0.00010040110051 (at least 1e-10, confirmed with exact rationals) below the cosine 0.792780236785 of the (6, 575) row in the /plain and HTML index pages saved in claim/ (logged as fetched at 2026-10-25T00:04:42Z and 00:04:44Z, 3 to 5 seconds before the claim files were written at 00:04:47Z), a row that in those saved pages has no '&ast;' and no 'needs more optimization', is the lowest of all listed rows with d' <= 6 and N' >= 575, and is not matched at or below c* by arXiv:2610.19988's three tables or by any paper in the saved arXiv keyword feeds; not confirmed are the row's live state after that fetch, the fetch times beyond their agreement with file times and sha256, and arXiv papers outside those keyword feeds.

Notes on the sentence above (quoted verbatim from panel/gate.md): "claim/" is the run's claim folder; the hashes of the
pages saved there are in the-record-we-beat/RECORD.md. The mpmath normalisation is the panel's check; the shipped
checker uses exact rational arithmetic.

## Check it yourself

From this folder, with Python 3 (standard library only):

```sh
sh verify-it-yourself/run_checks.sh
```

Expected last line: `PASS` (under a second on a laptop; full expected output in RUN_IT_YOURSELF.md and
verify-it-yourself/RECEIPTS.md). The check is exact: it reads the coordinates as decimals and compares every one
of the 165,025 pairs with the bar 0.792780236785 - 1e-10 in integer arithmetic.

## Compared to

| table | cell | value | URL | fetched (UTC) |
|---|---|---|---|---|
| Henry Cohn's Table of Spherical Codes | d = 6, N = 575 (no `&ast;`, not labelled "needs more optimization"; Pavlos Moros, 2026) | 0.792780236785 | https://spherical-codes.org/ and https://spherical-codes.org/plain | 2026-10-25T00:04:42Z and 00:04:44Z (re-read 00:14:17Z, same row) |

This code: c* = 0.7926798356844868804983 (22 significant digits), which is 1.004011e-4 lower (a minimal angle of
37.5633437° against 37.5539067° for the table's code). No listed code with d' <= 6 and N' >= 575 (which would give
a (6, 575) code by deleting points or padding with zeros) reaches c*, in the table or in the three data tables of
arXiv:2610.19988. Snapshot and extracted cell: the-record-we-beat/RECORD.md.

## Not claimed

- Not 26-digit precision: digits beyond the 17th of each coordinate are the exact decimal expansion of a
  double-precision value (printed with %.25e); c* is computed from the file exactly as written.
- Not optimality: the code is a numerical local optimum (2,801 pairs within 1e-14 of the maximum cosine, 12 points
  free of contacts), not a proof that (6, 575) cannot do better.
- Not an exact (algebraic) angle: the table lists no minimal polynomial for this row, and none is claimed here.
- Not a new construction: the code is a local polish of the posted code. That code was far from converged (1 pair
  at its maximum cosine, 3 within 1e-6), though the table row carried no "needs more optimization" label; an earlier
  (6, 575) row (Henry Cohn, 2026) carried that label in the 2026-09-23 snapshot recorded by arXiv:2610.19988.
- Not uploaded to the table: an upload to spherical-codes.org/upload-code is left to the contributor.
- The table row's state after 2026-10-25T00:14:19Z, and arXiv papers outside the saved 'spherical code' / 'Tammes'
  / 575 metadata searches, are not checked.

## Credits

- **Pavlos Moros**: the (6, 575) code posted on the table (2026), https://spherical-codes.org/data/6/575. This
  object is a local refinement of that code (points moved by a chord distance of 0.018 median, 0.079 at most), so the seed is Pavlos
  Moros's work.
- **Henry Cohn**: the Table of Spherical Codes, https://spherical-codes.org/ (archived data set
  https://hdl.handle.net/1721.1/153543).
- **Antoine Jay, M. Poberznik, M. Brut, A. Hemeryck, L.-H. Hoang, M. Gunde, N. Salles, G. Cruchon, M. Roux**:
  "Equidistribution of points on the hypersphere including symmetries", SSRN preprint 2026,
  doi:10.2139/ssrn.6427919 (not read: SSRN returns a bot check). Their program produced 645 of the 1,752 rows with
  d' <= 6 and N' >= 575 compared against, including every neighbouring row (6, 570)-(6, 574) and (6, 576)-(6, 588).
- **Joseph Farland** (8 of those rows), **R. H. Hardin, N. J. A. Sloane, W. D. Smith** (2 rows) and
  **T. Ericson, V. Zinoviev** (1 row): other rows compared against.
- **Ilmari Vahteristo**: "New spherical codes by tuning an annealing solver", https://arxiv.org/abs/2610.19988,
  data at https://zenodo.org/records/23270586 (compared against).
- **Alexey Kravatskiy, Valentin Khrulkov, Ivan Oseledets**: "ImprovEvolve", https://arxiv.org/abs/2602.10233
  (compared against; no d = 6 cell).
- Also checked: Chengdong Ma et al. (PackingStar, https://arxiv.org/abs/2511.13391), S. V. Borodachov,
  P. G. Boyvalenkov, P. D. Dragnev, D. P. Hardin, E. B. Saff, M. M. Stoyanova (https://arxiv.org/abs/2512.25037),
  Rustem Takhanov, Zhenisbek Assylbekov, Stanislav Yun (https://arxiv.org/abs/2606.18984), Yanlu Lian, Qun Mo,
  Yu Xia (https://arxiv.org/abs/2411.16038).
- HiGHS (via SciPy's linprog) solves the linear programs of the polish.
- Contributed by Abshalom Dayan. Found and checked by an AI agent run using the V3R1T4S kit (method:
  how-we-built-it/ and HOW_WE_FOUND_IT.md; panel: panel/).
