# A 3-colouring of K_271 proving R(3,3,15) >= 272 (small-ramsey-lower-bounds, partial win p1)

## What
The 3-colouring of K_271 in object/R_3_3_15.txt has no colour-1 triangle, no colour-2 triangle and no colour-3 K_15 (checked exhaustively), so R(3,3,15) >= 272, which exceeds the R(3,3,15) >= 269 of DS1 (revision of April 24, 2026, Table XIb) and every bound I found in newer arXiv papers or implied by DS1's Section 6.2 constructions; it is a corollary of the same object's 266-vertex R(3,3,14) colouring via the folklore colour-3 join.

## Check it yourself
```sh
sh verify-it-yourself/run_checks.sh
```
Expected last three lines: `proves R(3,3,15) >= 272`, `PASS`, `PASS`. Python 3 standard library only; about 5 seconds on a laptop.

## Compared to
| source | cell | value | URL | fetched (UTC) |
|---|---|---|---|---|
| DS1, Radziszowski, Small Ramsey Numbers (revision of April 24, 2026), Table XIb | R(3,3,15) | 269 (reference ExT) | https://www.combinatorics.org/ojs/index.php/eljc/article/download/DS1/pdf | 2026-10-25T06:19:34Z, 07:44:20Z and 11:04:12Z |

272 > 269. Fetch records, hashes and the extracted table are in the-record-we-beat/; the panel's own searches for anything newer are in panel/novelty.md and panel/criterion.md.

The panel files refer to workspace files that are not shipped here (CLAIM.md, work/, table_record.md, literature_record.md, panel/.work/, runs/, REPORT.md); the panel ran on the full run workspace, and everything needed to check the claim is in this package.

## Not claimed
- Only a lower bound: nothing about upper bounds or the exact value of R(3,3,15).
- One cell only. Other cells built in the same runs are separate claims with their own panels.
- Not a new method: the construction is the folklore colour-3 join of the R(3,3,14) >= 267 colouring of the same weekend (filed separately as PR #733; itself the splitting method of Exoo and Tatarevic applied to a published circulant) with a 5-vertex block (see Credits). With DS1's own R(3,3,14) value the join gives only 247.
- "Nothing at 272 or above was published" rests on the searches listed in panel/novelty.md and panel/criterion.md (DS1, arXiv, the authors' repositories, this repository).

## Credits
- Geoffrey Exoo and Milos Tatarevic, "New Lower Bounds for 28 Classical Ramsey Numbers", Electron. J. Combin. 22(3) (2015) #P3.11, https://www.combinatorics.org/ojs/index.php/eljc/article/view/v22i3p11 , arXiv:1504.02403 (https://arxiv.org/abs/1504.02403): the splitting method behind the R(3,3,14) colouring used for vertices 0..265, and the current DS1 entry R(3,3,15) >= 269.
- Eugene Kuznetsov, "Computational lower limits on small Ramsey numbers", arXiv:1505.07186v5 (2016), https://arxiv.org/abs/1505.07186v5 , Table 2: the (5,14) circulant on Z_266 whose two colour classes the R(3,3,14) colouring starts from.
- Stanislaw Radziszowski, "Small Ramsey Numbers", Electron. J. Combin. Dynamic Survey DS1 (revision of April 24, 2026), https://www.combinatorics.org/ojs/index.php/eljc/article/view/DS1 : the table compared against, and section 6.2's general constructions.
- PySAT (python-sat 1.9.dev17), https://github.com/pysathq/pysat , with Armin Biere's CaDiCaL solver, https://github.com/arminbiere/cadical : the SAT searches in the run's checkers (how-we-built-it/code/) and the panel's checks.
- The colour-3 join with a block is a folklore construction for multicolour Ramsey lower bounds; it is not the author's.
- Found and packaged by Abshalom Dayan with the V3R1T4S kit (https://github.com/elder-plinius/V3R1T4S).
