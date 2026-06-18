## Task 7 — Hypergeometric Calculation

**Setup:** 15 light bulbs total: 12 working, 3 defective. Draw 5 without replacement.
X = number of defective bulbs in the sample.

### P(exactly 2 defective)

```
P(X = 2) = C(3, 2) × C(12, 3) / C(15, 5)
```

Computing each term:
- C(3, 2) = 3 (choose 2 defectives from 3)
- C(12, 3) = (12×11×10)/(3×2×1) = 1320/6 = **220** (choose 3 working from 12)
- C(15, 5) = (15×14×13×12×11)/(5×4×3×2×1) = 360360/120 = **3003** (total ways to choose 5 from 15)

```
P(X = 2) = (3 × 220) / 3003 = 660 / 3003 = 220/1001 ≈ 0.2198   (about 22%)
```

**Interpretation:** With 3 defective bulbs out of 15, drawing a sample of 5 has about a 22% chance of containing exactly 2 of those defectives.