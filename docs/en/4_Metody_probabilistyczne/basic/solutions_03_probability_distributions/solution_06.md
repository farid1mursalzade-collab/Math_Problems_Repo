## Task 6 — Binomial Calculation

**Setup:** n=10 parts inspected. p=0.04 (probability of defective). X ~ B(10, 0.04).

### P(exactly 2 defective)

```
P(X = 2) = C(10, 2) × (0.04)² × (0.96)⁸
```

Computing step by step:
- C(10, 2) = (10 × 9)/(2 × 1) = **45**
- (0.04)² = **0.0016**
- (0.96)⁸: compute step by step:
  - 0.96² = 0.9216
  - 0.96⁴ = 0.9216² = 0.84934656
  - 0.96⁸ = 0.84934656² ≈ **0.72138959**

```
P(X = 2) = 45 × 0.0016 × 0.72138959
           = 45 × 0.00115422...
           ≈ 0.0519   (about 5.2%)
```

### P(at least one defective)

"At least one" is complementary to "zero defective."

```
P(X = 0) = C(10,0) × (0.04)⁰ × (0.96)¹⁰ = 1 × 1 × (0.96)¹⁰
```

(0.96)¹⁰ = (0.96)⁸ × (0.96)² = 0.72138959 × 0.9216 ≈ **0.66483263**

```
P(X ≥ 1) = 1 − P(X = 0) = 1 − 0.66483263 ≈ 0.3352   (about 33.5%)
```

**Interpretation:** Despite each part having only a 4% defect rate, there is more than a 1-in-3 chance of finding at least one defective part in a batch of 10. This highlights how individual rare events can be common in aggregate.
