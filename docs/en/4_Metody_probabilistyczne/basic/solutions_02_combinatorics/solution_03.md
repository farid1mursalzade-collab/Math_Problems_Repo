## Task 3 — Permutations with Repeated Elements

The formula for arranging n objects where group 1 has n₁ identical items, group 2 has n₂ identical items, etc., is:

```
n! / (n₁! × n₂! × ... × nₖ!)
```

This corrects for the fact that swapping two identical items within a group does not create a new arrangement.

### MISSISSIPPI

Count the letters: M(1), I(4), S(4), P(2). Total: 11 letters.

```
11! / (1! × 4! × 4! × 2!)
= 39,916,800 / (1 × 24 × 24 × 2)
= 39,916,800 / 1,152
= 34,650
```

### STATISTICS

Count the letters: S(3), T(3), A(1), I(2), C(1). Total: 10 letters.

```
10! / (3! × 3! × 1! × 2! × 1!)
= 3,628,800 / (6 × 6 × 1 × 2 × 1)
= 3,628,800 / 72
= 50,400
```

### Arrangements of STATISTICS beginning with S

We fix one S in the first position. The remaining 9 letters are: S(2), T(3), A(1), I(2), C(1).

```
9! / (2! × 3! × 1! × 2! × 1!)
= 362,880 / (2 × 6 × 1 × 2 × 1)
= 362,880 / 24
= 15,120
```