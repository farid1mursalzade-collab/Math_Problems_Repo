## Task 3 — Geometric Model: Waiting for the First Event

**Experiment:** Each printed page independently has a printing error with probability p. We keep examining pages until we find the first error.

**Success = a page has a printing error.**

### Sample Space

The experiment can end on the 1st page, 2nd page, 3rd page, ..., or in principle any page. The sample space is infinite:

```
Ω = { 1, 2, 3, 4, ... }
```

where outcome k means the first error appears on the k-th page.

### Probability Distribution

For the first error to appear on page k:
- Pages 1, 2, ..., k−1 must all be error-free (probability (1−p) each)
- Page k must have an error (probability p)

Since pages are independent:

```
P(X = k) = (1−p)^(k−1) × p    for k = 1, 2, 3, ...
```

This is the **Geometric distribution** Geom(p).

**Verification:** The probabilities sum to 1:
∑ₖ₌₁^∞ (1−p)^(k−1) × p = p × ∑ₙ₌₀^∞ (1−p)^n = p × 1/(1−(1−p)) = p × 1/p = 1 ✓

(This uses the formula for the sum of a geometric series.)

**Success in this model = finding a page with an error.** The parameter p is the probability of success on any single trial.