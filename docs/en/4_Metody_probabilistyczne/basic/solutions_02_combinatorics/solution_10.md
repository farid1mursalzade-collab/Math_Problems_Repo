## Task 10 — Urn Models

The urn contains 5 red (R), 4 blue (B), and 3 green (G) balls, for a total of 12.

### Problem 1: 3 balls drawn, order ignored, without replacement

We choose 3 balls from 12 regardless of which color or what order:
```
C(12, 3) = 12! / (3! × 9!) = (12 × 11 × 10) / 6 = 220
```

### Problem 2: Exactly 2 red balls in the sample (order ignored)

We choose 2 red balls from the 5 available, and 1 non-red ball from the 7 non-red balls:
```
C(5, 2) × C(7, 1) = 10 × 7 = 70
```

### Problem 3: 3 balls drawn, order recorded

Now the sequence matters: drawing R₁, B₂, G₁ is different from B₂, R₁, G₁. We are choosing an ordered sequence of 3 from 12 distinct balls:
```
P(12, 3) = 12 × 11 × 10 = 1,320
```

### Problem 4: Exactly 2 red balls, order recorded

We have 3 positions. Two must be red and one must be non-red.

- Choose which 2 positions are red: C(3,2) = 3 ways
- Fill the red positions in order (from 5 red balls, no replacement): 5 × 4 = 20 ways
- Fill the remaining position with a non-red ball: 7 choices

```
3 × 5 × 4 × 7 = 420
```
