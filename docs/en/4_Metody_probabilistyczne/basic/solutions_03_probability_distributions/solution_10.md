## Task 10 — Multinomial Calculation

**Setup:** 6 selections with replacement from candies:
- Strawberry with probability p₁ = 0.40
- Lemon with probability p₂ = 0.35
- Mint with probability p₃ = 0.25

We want: k₁=3 strawberry, k₂=2 lemon, k₃=1 mint.

### Calculation

```
P(X₁=3, X₂=2, X₃=1) = [6! / (3! × 2! × 1!)] × (0.40)³ × (0.35)² × (0.25)¹
```

Step by step:
- Multinomial coefficient: 6!/(3!×2!×1!) = 720/(6×2×1) = **60**
- (0.40)³ = 0.064
- (0.35)² = 0.1225
- (0.25)¹ = 0.25
- Product of probabilities: 0.064 × 0.1225 × 0.25 = 0.00196

```
P = 60 × 0.00196 = 0.1176   (about 11.8%)
```

**Interpretation:** Among all the ways to pick 6 candies (3 strawberry + 2 lemon + 1 mint), this specific composition occurs about 12% of the time. The multinomial coefficient 60 counts all the different orderings that give this composition (e.g., SSLSMS, SSLSMS, etc. — 60 distinct arrangements).