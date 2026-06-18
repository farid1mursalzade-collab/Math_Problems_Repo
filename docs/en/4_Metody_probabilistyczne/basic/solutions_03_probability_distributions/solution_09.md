## Task 9 — Poisson Calculation

**Setup:** λ = 5 requests per hour. X ~ Poisson(5).

Recall: e⁻⁵ ≈ 0.006738

### P(exactly 3 requests)

```
P(X = 3) = e^(−5) × 5³ / 3!
           = 0.006738 × 125 / 6
           = 0.006738 × 20.8333...
           ≈ 0.1404   (about 14%)
```

### P(at least one request)

The complement is "zero requests":

```
P(X = 0) = e^(−5) × 5⁰ / 0! = e^(−5) × 1 = e^(−5) ≈ 0.006738

P(X ≥ 1) = 1 − e^(−5) ≈ 1 − 0.006738 ≈ 0.9933   (about 99.3%)
```

**Interpretation:** With an average of 5 requests per hour, it is extremely unlikely (less than 0.7% chance) for the service to receive no requests at all in an entire hour.
