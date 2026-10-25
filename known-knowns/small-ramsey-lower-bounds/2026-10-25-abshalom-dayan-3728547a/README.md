# A 3-colouring of K_251 proving R(3,5,7) >= 252 (small-ramsey-lower-bounds, partial win p1)

## What
The circulant 3-colouring of K_251 in object/R_3_5_7.txt (sha256 3728547a...351976) has, by two independent exact checks, no monochromatic K3 in colour 1, K5 in colour 2 or K7 in colour 3, so R(3,5,7) >= 252, strictly above the bound 241 in DS1 revision #18 (April 24, 2026, Table XIb) and above every lower bound for R(3,5,7) found in arXiv titles and abstracts up to 2026-10-21.

## Check it yourself
```sh
sh verify-it-yourself/run_checks.sh
```
Expected last three lines: `proves R(3,5,7) >= 252`, `PASS`, `PASS` (the checker and the script each print PASS). Python 3 standard library only; under a second on a laptop.

## Compared to
| source | cell | value | URL | fetched (UTC) |
|---|---|---|---|---|
| DS1, Radziszowski, Small Ramsey Numbers (revision of April 24, 2026), Table XIb | R(3,5,7) | 241 (reference 6.2.g) | https://www.combinatorics.org/ojs/index.php/eljc/article/download/DS1/pdf | 2026-10-25T06:19:34Z and 07:44:20Z |

252 > 241. Fetch records, hashes and the extracted table are in the-record-we-beat/; the panel's own searches for anything newer are in panel/novelty.md and panel/criterion.md.

## Not claimed
- Only a lower bound: nothing about upper bounds or the exact value of R(3,5,7).
- One cell only. Other cells built in the same runs are separate claims with their own panels.
- Not a new method: the construction is the splitting method of Exoo and Tatarevic applied to a published two-colour circulant (see Credits).
- "Nothing at 252 or above was published" rests on the searches listed in panel/novelty.md and panel/criterion.md (DS1, arXiv, the authors' repositories, this repository).

## Notes on the panel files
- The panel files mention the run's REPORT.md (its "Needs you" section). That report is not part of this package; everything it says about this claim is in panel/gate.md.

## Credits
- Geoffrey Exoo and Milos Tatarevic, "New Lower Bounds for 28 Classical Ramsey Numbers", Electron. J. Combin. 22(3) (2015) #P3.11, https://www.combinatorics.org/ojs/index.php/eljc/article/view/v22i3p11 (arXiv:1504.02403, https://arxiv.org/abs/1504.02403): the splitting method used here (split one colour graph of a two-colour colouring into two colour graphs with smaller forbidden cliques).
- Eugene Kuznetsov, "Computational lower limits on small Ramsey numbers", arXiv:1505.07186v5 (2016), https://arxiv.org/abs/1505.07186, Table 2: the (7,9) circulant on Z_251 whose two colour classes this object starts from.
- Xu Xiaodong, Xie Zheng, Geoffrey Exoo and Stanislaw Radziszowski, "Constructive Lower Bounds on Classical Multicolor Ramsey Numbers", Electron. J. Combin. 11 (2004) #R35, https://www.combinatorics.org/ojs/index.php/eljc/article/view/v11i1r35: the general construction (DS1 item 6.2.g; eq. (15) there, R(k1, 2k2-1, k3) >= 4R(k1-1, k2, k3) - 3) behind the current DS1 entry R(3,5,7) >= 241.
- Stanislaw Radziszowski, "Small Ramsey Numbers", Electron. J. Combin. Dynamic Survey DS1 (revision of April 24, 2026), https://www.combinatorics.org/ojs/index.php/eljc/article/view/DS1: the table compared against.
- Found and packaged by Abshalom Dayan with the V3R1T4S kit (https://github.com/elder-plinius/V3R1T4S).
