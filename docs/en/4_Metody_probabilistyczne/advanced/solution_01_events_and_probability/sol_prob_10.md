## Task 10 — Events and Probabilities in Buffon's Needle

### Setup

- x is uniform on [0, d/2]; θ is uniform on [0, π/2]; x and θ are independent.  
- Joint probability density: f(x, θ) = 4/(πd) (the normalizing constant ensures total probability = 1).  
- The needle intersects a line exactly when the half-length projected perpendicular to the lines exceeds x, i.e., when **x ≤ (L/2)sinθ**.

### Event A — the needle intersects one of the lines

We integrate the joint density over the region where x ≤ (L/2)sinθ:

```
P(A) = ∫₀^(π/2) ∫₀^{(L/2)sinθ}  4/(πd)  dx dθ

     = [4/(πd)] × (L/2) × ∫₀^(π/2) sinθ dθ

     = [4/(πd)] × (L/2) × [-cosθ]₀^(π/2)

     = [4/(πd)] × (L/2) × [0 - (-1)]

     = [4/(πd)] × (L/2) × 1

     = 2L/(πd)
```

**P(A) = 2L/(πd)**

This famous result is one of the earliest uses of probability to estimate π: if we observe many throws and count how many times the needle crosses a line, we can estimate π from the crossing frequency.

### Event B — the needle does not intersect any line

B is the complement of A:  
**P(B) = 1 − 2L/(πd)**

### Event C — the angle is less than π/6

Since θ is uniformly distributed on [0, π/2], all sub-intervals of the same length are equally likely:  
P(C) = P(θ < π/6) = (π/6) / (π/2) = **1/3**

### Event D — the center is less than d/4 from the nearest line

Since x is uniformly distributed on [0, d/2]:  
P(D) = P(x < d/4) = (d/4) / (d/2) = **1/2**

### Event E — intersects a line AND angle > π/4

We integrate only over the portion of A where θ > π/4:

```
P(E) = [4/(πd)] × (L/2) × ∫_{π/4}^{π/2} sinθ dθ

     = [4/(πd)] × (L/2) × [-cosθ]_{π/4}^{π/2}

     = [4/(πd)] × (L/2) × [0 − (−√2/2)]

     = [4/(πd)] × (L/2) × (√2/2)

     = [4/(πd)] × (L√2/4)

     = L√2/(πd)
```

**P(E) = L√2/(πd)**

### Additional event — F — the angle is between π/3 and π/2

Since θ is uniform on [0, π/2]:  
P(F) = (π/2 − π/3) / (π/2) = (π/6) / (π/2) = **1/3**

This event describes needles that are nearly perpendicular to the lines (steep angle), and it has the same probability as Event C (angle less than π/6) by symmetry of the uniform distribution about π/4.
