# A 3-colouring of K_266 proving R(3,3,14) >= 267 (small-ramsey-lower-bounds, partial win p1)

## What
The circulant 3-colouring of K_266 in object/R_3_3_14.txt (sha256 d46e9b16…34ba) has no monochromatic K_3 in colours 1 and 2 and no K_14 in colour 3, verified exhaustively by a SAT/UNSAT search and by the author's branch and bound, so R(3,3,14) ≥ 267, which is strictly above DS1's (April 24, 2026) bound of 242 and above every bound for this cell that I found on arXiv up to 2026-10-21 (titles and abstracts only).

## Check it yourself
```sh
sh verify-it-yourself/run_checks.sh
```
Expected last line: `PASS` (the line before it: `proves R(3,3,14) >= 267`). Python 3 standard library only; about 4 seconds on a laptop.

## Compared to
| source | cell | value | URL | fetched (UTC) |
|---|---|---|---|---|
| DS1, Radziszowski, Small Ramsey Numbers (revision of April 24, 2026), Table XIb | R(3,3,14) | 242 (reference ExT) | https://www.combinatorics.org/ojs/index.php/eljc/article/download/DS1/pdf | 2026-10-25T06:19:34Z and 07:44:20Z |

267 > 242. Fetch records, hashes and the extracted table are in the-record-we-beat/; the panel's own searches for anything newer are in panel/novelty.md and panel/criterion.md.

## Not claimed
- Only a lower bound: nothing about upper bounds or the exact value of R(3,3,14).
- One cell only. Other cells built in the same runs are separate claims with their own panels.
- Not a new method: the construction is the splitting method of Exoo and Tatarevic applied to a published two-colour circulant (see Credits).
- "Nothing at 267 or above was published" rests on the searches listed in panel/novelty.md and panel/criterion.md (DS1, arXiv, the authors' repositories, this repository).

## Notes on the panel files
- The panel files mention the run's REPORT.md (its "Needs you" section). That report is not part of this package; everything it says about this claim is in panel/gate.md.
- The CRITERION skeptic ran twice. The first session (panel/criterion_attempt1.md, kept unchanged) found the object correct by two exact methods but returned pass: false because it had no web access to check the p1 clause "any newer arXiv paper for that multicolour cell" and claim/ held no search record for it. The run then added claim/literature_record.md and allowed that skeptic honest web access; a new fresh session (panel/criterion.md) passed. NOVELTY, which had web access from the start, passed the same clause on its own. panel/gate.md records both sessions and every change.

## Credits
- Geoffrey Exoo and Milos Tatarevic, "New Lower Bounds for 28 Classical Ramsey Numbers", Electron. J. Combin. 22(3)
  (2015) #P3.11, https://www.combinatorics.org/ojs/index.php/eljc/article/view/v22i3p11 (arXiv:1504.02403,
  https://arxiv.org/abs/1504.02403): the splitting method used here (take a (5,k)-colouring and split its K5-free colour
  graph into two K3-free colour graphs) and the current DS1 entry R(3,3,14) >= 242.
- Eugene Kuznetsov, "Computational lower limits on small Ramsey numbers", arXiv:1505.07186v5 (2016), https://arxiv.org/abs/1505.07186, Table 2: the
  (5,14) circulant on Z_266 whose two colour classes this object starts from.
- Stanislaw Radziszowski, "Small Ramsey Numbers", Electron. J. Combin. Dynamic Survey DS1 (revision of April 24, 2026),
  https://www.combinatorics.org/ojs/index.php/eljc/article/view/DS1: the table compared against.
- Found and packaged by Abshalom Dayan with the V3R1T4S kit (https://github.com/elder-plinius/V3R1T4S).
