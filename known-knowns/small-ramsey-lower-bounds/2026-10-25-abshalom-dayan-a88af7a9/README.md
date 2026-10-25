# A 3-colouring of K_132 proving R(3,3,9) >= 133 (small-ramsey-lower-bounds, partial win p1)

## What
The circulant 3-colouring of K_132 in object/R_3_3_9.txt (sha256 a88af7a9fb8fc8eb0ddf226628db6f59df6c1fb8504ed3ec80d2eeaf972a64cd) has no monochromatic K_3 in colours 1 and 2 and no K_9 in colour 3 (checked exhaustively by three independent methods), so R(3,3,9) >= 133, which is strictly above the 129 in DS1 revision #18 (April 24, 2026) Table XIb and above every bound I found in arXiv papers posted or updated after that revision.

## Check it yourself
```sh
sh verify-it-yourself/run_checks.sh
```
Expected last three lines: `proves R(3,3,9) >= 133`, `PASS`, `PASS` (the checker and the script each print PASS). Python 3 standard library only; under a second on a laptop.

## Compared to
| source | cell | value | URL | fetched (UTC) |
|---|---|---|---|---|
| DS1, Radziszowski, Small Ramsey Numbers (revision of April 24, 2026), Table XIb | R(3,3,9) | 129 (reference Ex18) | https://www.combinatorics.org/ojs/index.php/eljc/article/download/DS1/pdf | 2026-10-25T06:19:34Z and 07:44:20Z |

133 > 129. Fetch records, hashes and the extracted table are in the-record-we-beat/; the panel's own searches for anything newer are in panel/novelty.md and panel/criterion.md.

## Not claimed
- Only a lower bound: nothing about upper bounds or the exact value of R(3,3,9).
- One cell only. Other cells built in the same runs are separate claims with their own panels.
- Not a new method: the construction is the splitting method of Exoo and Tatarevic applied to a published two-colour circulant (see Credits).
- "Nothing at 133 or above was published" rests on the searches listed in panel/novelty.md and panel/criterion.md (DS1, arXiv, the authors' repositories, this repository).

## Notes on the panel files
- The panel files mention run files that are not part of this package: the run's REPORT.md (its "Needs you" section), CLAIM.md, table_record.md and literature_record.md; PREREG.md and code/alpha.c also name paths in the run's workspace. These are private workspace files. Everything they say about this claim is in panel/gate.md and the panel files.
- One source could not be read: Exoo's construction folder http://cs.indstate.edu/ge/RAMSEY/ExTa/ returned HTTP 403 and was not retried. It may hold Exoo's constructions behind the DS1 entry 129 [Ex18]; DS1 itself lists nothing above 129 for this cell.

## Credits
- Geoffrey Exoo and Milos Tatarevic, "New Lower Bounds for 28 Classical Ramsey Numbers", Electron. J. Combin. 22(3) (2015) #P3.11, https://www.combinatorics.org/ojs/index.php/eljc/article/view/v22i3p11 (arXiv:1504.02403, https://arxiv.org/abs/1504.02403): the splitting method used here (take a (5,k)-colouring and split its K5-free colour graph into two K3-free colour graphs).
- Geoffrey Exoo: the current DS1 entry R(3,3,9) >= 129 (DS1 reference [Ex18], personal communication 2012-2013, constructions at http://cs.indstate.edu/ge/RAMSEY).
- Eugene Kuznetsov, "Computational lower limits on small Ramsey numbers", arXiv:1505.07186v5 (2016), https://arxiv.org/abs/1505.07186, Table 2: the (5,9) circulant on Z_132 whose two colour classes this object starts from.
- Stanislaw Radziszowski, "Small Ramsey Numbers", Electron. J. Combin. Dynamic Survey DS1 (revision of April 24, 2026), https://www.combinatorics.org/ojs/index.php/eljc/article/view/DS1: the table compared against.
- PySAT (https://pysathq.github.io) with the CaDiCaL solver (https://github.com/arminbiere/cadical): the SAT search that found the split, and the run's second exact check.
- Found and packaged by Abshalom Dayan with the V3R1T4S kit (https://github.com/elder-plinius/V3R1T4S).
