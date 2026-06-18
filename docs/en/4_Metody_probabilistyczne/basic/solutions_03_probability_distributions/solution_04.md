## Task 4 — Poisson Model: Arrival of Events

**Experiment:** A web service receives error reports at an average rate of 3 per hour. We count how many reports arrive in one hour.

### Sample Space

In principle, any non-negative integer number of reports could arrive:

```
Ω = { 0, 1, 2, 3, 4, ... }
```

The sample space is infinite (even though very large numbers are extremely unlikely).

### Probability Distribution

The **Poisson distribution** with parameter λ:

```
P(X = k) = e^(−λ) × λᵏ / k!    for k = 0, 1, 2, ...
```

where e ≈ 2.71828 (Euler's number).

**For this problem:** λ = 3 (average reports per hour).

```
P(X = k) = e^(−3) × 3ᵏ / k!
```

### What λ Represents

The parameter λ is both the **mean** and the **variance** of the Poisson distribution (a key property: E[X] = Var[X] = λ).

For one hour: λ = 3 means on average 3 reports arrive per hour.

For two hours: λ = 6 (the rate scales linearly with the time interval).

For 30 minutes: λ = 1.5.

**The Poisson model assumes:**
1. Events occur independently of each other
2. The rate is constant over time (stationary)
3. Two events cannot occur at exactly the same instant
