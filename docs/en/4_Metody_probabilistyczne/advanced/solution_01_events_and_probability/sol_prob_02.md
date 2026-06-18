## Task 2 — Rolling a Die

We are rolling a standard fair six-sided die. The faces are numbered 1 through 6.

### Ω₁ — Sample space for one roll

Each face is one possible outcome:

```
Ω₁ = { 1, 2, 3, 4, 5, 6 }
```

**|Ω₁| = 6.**

Each elementary outcome represents: *the number showing on top after one roll of the die.*

### Ω₂ — Sample space for two consecutive rolls

For two rolls, the first roll can be any of 6 values and the second roll can independently be any of 6 values. Each elementary outcome is an ordered pair (first result, second result):

```
Ω₂ = { (i, j) : i ∈ {1,2,3,4,5,6} and j ∈ {1,2,3,4,5,6} }
```

For example, (3, 5) means the first die showed 3 and the second showed 5. This is different from (5, 3).

**|Ω₂| = 6 × 6 = 36** ordered pairs.

### Ω₃ — Sample space for three consecutive rolls

```
Ω₃ = { (i, j, k) : i, j, k ∈ {1,2,3,4,5,6} }
```

**|Ω₃| = 6 × 6 × 6 = 216** ordered triples.

Each elementary outcome represents: *an ordered triple recording the face values obtained on the first, second, and third roll, in that order.*

**General pattern:** For n independent rolls, there are **6ⁿ** elementary outcomes.
