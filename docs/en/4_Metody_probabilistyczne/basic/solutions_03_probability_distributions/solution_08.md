## Task 8 — Geometric Calculation

**Setup:** Each compilation has probability p=0.1 of error. X = trial number of the first error. X ~ Geom(0.1).

### P(first error on the 4th compilation)

The first 3 compilations are error-free, and the 4th has an error:

```
P(X = 4) = (1 − 0.1)³ × 0.1 = (0.9)³ × 0.1 = 0.729 × 0.1 = 0.0729
```

### P(first error no later than the 3rd compilation)

This is P(X ≤ 3) = P(X=1) + P(X=2) + P(X=3):
- P(X=1) = 0.1
- P(X=2) = 0.9 × 0.1 = 0.09
- P(X=3) = 0.9² × 0.1 = 0.081

Total: 0.1 + 0.09 + 0.081 = **0.271**

**Shortcut using complement:**

P(X > 3) = P(no error in first 3 compilations) = (0.9)³ = 0.729

P(X ≤ 3) = 1 − 0.729 = **0.271** ✓

**Interpretation:** There is about a 27% chance of encountering the first compilation error within the first three attempts.
