## Task 2 — Hypergeometric Model: Sampling a Batch

**Experiment:** A warehouse has 20 components: 5 defective and 15 functional. We randomly select 4 components WITHOUT replacement.

**Success = drawing a defective component.**

The key difference from the Binomial is that we are sampling WITHOUT replacement from a FINITE population. After drawing one defective item, the composition of the remaining pool changes — the trials are no longer independent.

**Random variable:** X = number of defective items in the sample of 4.

**Possible values:** X can be 0, 1, 2, 3, or 4 (but not more, since there are only 5 defectives and only 4 items drawn).

### Formula

The hypergeometric PMF is:

```
P(X = k) = C(5, k) × C(15, 4−k) / C(20, 4)
```

Explanation:
- C(5, k): choose k defective items from the 5 defective ones
- C(15, 4−k): choose the remaining (4−k) items from the 15 functional ones
- C(20, 4): total number of ways to choose any 4 items from 20

**Total combinations:** C(20, 4) = (20×19×18×17)/(4×3×2×1) = 4,845

### Full Probability Distribution

| k | C(5,k) | C(15, 4−k) | P(X=k) | Approximate |
|---|---|---|---|---|
| 0 | 1 | C(15,4)=1365 | 1365/4845 | 0.2817 |
| 1 | 5 | C(15,3)=455 | 2275/4845 | 0.4696 |
| 2 | 10 | C(15,2)=105 | 1050/4845 | 0.2167 |
| 3 | 10 | C(15,1)=15 | 150/4845 | 0.0310 |
| 4 | 5 | C(15,0)=1 | 5/4845 | 0.0010 |

**Verification:** 1365+2275+1050+150+5 = 4845, so all probabilities sum to 1. ✓

**Interpretation:** The most likely result is drawing exactly 1 defective item (46.96%), which reflects the fact that defectives make up 25% of the population.