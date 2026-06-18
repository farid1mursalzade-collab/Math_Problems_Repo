## Task 5 — Multinomial Model: Categories of Outcomes

**Experiment:** A die is rolled 5 times. Each outcome is classified into one of three categories:
- Small: {1, 2} with probability p₁ = 1/3
- Medium: {3, 4} with probability p₂ = 1/3
- Large: {5, 6} with probability p₃ = 1/3

### Sample Space

The detailed sample space consists of all ordered 5-tuples of die results, but for the multinomial model we work with the counts in each category. If X₁, X₂, X₃ are the counts of small, medium, large results respectively, then X₁ + X₂ + X₃ = 5.

### Multinomial Distribution

```
P(X₁=k₁, X₂=k₂, X₃=k₃) = [5! / (k₁! × k₂! × k₃!)] × (1/3)^k₁ × (1/3)^k₂ × (1/3)^k₃
```

where k₁ + k₂ + k₃ = 5 and each kᵢ ≥ 0.

### Parameter Interpretation

- The multinomial coefficient **5!/(k₁!k₂!k₃!)** counts the number of ordered arrangements of k₁ smalls, k₂ mediums, and k₃ larges (similar to permutations with repeated elements).
- The probabilities **p₁^k₁ × p₂^k₂ × p₃^k₃** give the probability that a specific sequence has k₁ smalls, k₂ mediums, and k₃ larges.
- Together, the formula counts all sequences with the right category counts and sums their probabilities.

**Example:** P(X₁=2, X₂=2, X₃=1):
```
= [5!/(2!×2!×1!)] × (1/3)² × (1/3)² × (1/3)¹
= 30 × (1/9) × (1/9) × (1/3)
= 30 / 243
≈ 0.1235
```