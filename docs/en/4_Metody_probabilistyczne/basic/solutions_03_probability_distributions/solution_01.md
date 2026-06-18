## Task 1 — Binomial Model: Quality Control Setup

**Experiment:** We check 3 screws one by one. Each screw is independently either good (G) or defective (D). The probability of any individual screw being defective is p, and this stays the same for all three screws.

**Success = defective screw** (we are counting defectives).

### Sample Space

Every possible sequence of three inspection results:

```
Ω = { GGG, GGD, GDG, DGG, GDD, DGD, DDG, DDD }
```

### Probabilities of Each Elementary Outcome

Since the screws are inspected independently, we multiply individual probabilities:

| Outcome | Formula | Probability |
|---|---|---|
| GGG | (1−p)(1−p)(1−p) | (1−p)³ |
| GGD | (1−p)(1−p)(p) | p(1−p)² |
| GDG | (1−p)(p)(1−p) | p(1−p)² |
| DGG | (p)(1−p)(1−p) | p(1−p)² |
| GDD | (1−p)(p)(p) | p²(1−p) |
| DGD | (p)(1−p)(p) | p²(1−p) |
| DDG | (p)(p)(1−p) | p²(1−p) |
| DDD | (p)(p)(p) | p³ |

### Random Variable and PMF

If we define X = the number of defective screws, then X can take values 0, 1, 2, 3.

Grouping outcomes by X:
- X=0: only GGG → P(X=0) = (1−p)³ = C(3,0)p⁰(1−p)³
- X=1: GGD, GDG, DGG (3 outcomes) → P(X=1) = 3p(1−p)² = C(3,1)p¹(1−p)²
- X=2: GDD, DGD, DDG (3 outcomes) → P(X=2) = 3p²(1−p) = C(3,2)p²(1−p)¹
- X=3: only DDD → P(X=3) = p³ = C(3,3)p³(1−p)⁰

This is the **Binomial distribution** B(3, p): **P(X=k) = C(3,k) × pᵏ × (1−p)^(3−k)**
