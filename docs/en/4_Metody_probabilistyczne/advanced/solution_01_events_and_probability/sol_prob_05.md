## Task 5 — Buffon's Needle Experiment

This experiment is fundamentally different from all the previous ones. Instead of a finite list of discrete outcomes, here the outcome of each throw is described by two continuous numerical measurements.

### Setup

A needle of length **L** is thrown randomly onto a floor ruled with parallel lines, where neighboring lines are **d** apart. We assume **L ≤ d**.

### Parameters that determine the outcome

Two quantities completely describe where the needle lands:

1. **x** — the distance from the **center** of the needle to the nearest parallel line. By symmetry, we only need to track x ∈ [0, d/2], since the nearest line is never more than d/2 away from the center.

2. **θ** — the **acute angle** between the needle and the direction of the parallel lines. By symmetry, we only need θ ∈ [0, π/2].

### The sample space

```
Ω = { (x, θ) : x ∈ [0, d/2],  θ ∈ [0, π/2] }
```

This is a rectangle in the (x, θ) plane.

### Why this sample space is continuous

In all previous experiments, the sample space was a finite set — we could list every possible outcome. Here, x can take any real value in [0, d/2], and θ can take any real value in [0, π/2]. Between any two possible values, there are infinitely many others. We say the sample space is **continuous**.

The practical consequence is that we cannot assign positive probability to any single point (x, θ), because there are uncountably many points. Instead, probabilities are computed as **proportions of area** within the sample space rectangle. We use integration (the area under a curve) to compute probabilities, just as in this task list we use counting to compute probabilities for finite sample spaces.