# Solution

## Task 1
## Task 1 — Coin Tossing

We are tossing a fair coin, meaning each side (Heads or Tails) is equally likely. The order of outcomes matters.

### Ω₁ — Sample space for one coin toss

A single coin toss can produce exactly two outcomes: Heads (H) or Tails (T). Nothing else is possible.

```
Ω₁ = { H, T }
```

The number of elementary outcomes is **|Ω₁| = 2**.

Each elementary outcome represents: *the single result of one toss of the coin.*

### Ω₂ — Sample space for two coin tosses

For two tosses, we use a tree diagram. At the first stage the coin lands either H or T. From each of those, at the second stage it can again land H or T. Each path from root to leaf is one elementary outcome:

```
START
 ├── H (first toss is Heads)
 │     ├── H  →  outcome: (H, H)
 │     └── T  →  outcome: (H, T)
 └── T (first toss is Tails)
       ├── H  →  outcome: (T, H)
       └── T  →  outcome: (T, T)
```

```
Ω₂ = { (H,H), (H,T), (T,H), (T,T) }
```

The number of elementary outcomes is **|Ω₂| = 4**, which equals 2 × 2 = 2².

Each elementary outcome represents: *an ordered pair recording the result of the first toss and then the second toss.* Notice that (H,T) and (T,H) are different outcomes even though they both contain one H and one T — the order matters.

### Ω₃ — Sample space for three coin tosses

Following the same logic, we extend the tree to a third stage. For each of the 4 outcomes from Ω₂, the third toss can be H or T, giving us 4 × 2 = 8 outcomes:

```
Ω₃ = { HHH, HHT, HTH, HTT, THH, THT, TTH, TTT }
```

The number of elementary outcomes is **|Ω₃| = 8 = 2³**.

Each elementary outcome represents: *an ordered triple recording the results of the first, second, and third tosses in that order.*

**General pattern:** For n independent coin tosses, the sample space has **2ⁿ** elementary outcomes because at each stage we have 2 choices and the stages are independent.
