## Task 9 — Digit Restrictions

### Problem 1: How many 5-digit numbers exist?

A 5-digit number has first digit from {1,...,9} (cannot be 0) and the other four from {0,...,9}:
```
9 × 10 × 10 × 10 × 10 = 90,000
```

This is consistent with knowing that 5-digit numbers go from 10,000 to 99,999, a total of 90,000 numbers.

### Problem 2: How many are even?

An even number ends in {0, 2, 4, 6, 8}.

- First digit: 9 choices (1–9)
- Middle three digits: 10 choices each
- Last digit: 5 choices (even digits)

```
9 × 10 × 10 × 10 × 5 = 45,000
```

### Problem 3: How many contain no repeated digits?

We build the number digit by digit:
- First digit: 9 choices (1–9, not 0)
- Second digit: 9 choices (0–9, excluding the first digit)
- Third digit: 8 choices (excluding the first two)
- Fourth digit: 7 choices
- Fifth digit: 6 choices

```
9 × 9 × 8 × 7 × 6 = 27,216
```

*Why is the second digit 9, not 8?* Because we excluded the first digit but we added back 0, which was not available for the first position. So after the first digit is chosen from {1,...,9}, the second digit can be any of {0,...,9} except the first digit — that is 9 options.

### Problem 4: How many contain at least one repeated digit?

Complementary counting:
```
90,000 − 27,216 = 62,784
```