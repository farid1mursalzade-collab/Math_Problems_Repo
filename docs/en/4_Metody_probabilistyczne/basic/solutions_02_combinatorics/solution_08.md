## Task 8 — Sequences with Repetition

A sequence of length k from n symbols (repetition allowed): nᵏ

### Problem 1: 5-digit PIN (digits 0–9, repetition allowed)

Each of 5 positions has 10 possible digits:
```
10⁵ = 100,000
```

### Problem 2: PINs with at least one repeated digit

Total PINs − PINs with all different digits:
```
All different: 10 × 9 × 8 × 7 × 6 = P(10,5) = 30,240

At least one repeat: 100,000 − 30,240 = 69,760
```

### Problem 3: PINs with all digits different

As computed above:
```
P(10, 5) = 30,240
```
