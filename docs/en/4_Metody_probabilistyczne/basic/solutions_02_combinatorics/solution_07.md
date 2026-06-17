## Task 7 — k-Permutations (Ordered Selections Without Repetition)

Formula: P(n, k) = n! / (n−k)! = n × (n−1) × ... × (n−k+1)

This counts ordered selections of k items from n distinct items, without replacement.

### Problem 1: First 3 places among 12 runners

Gold can be any of 12, silver any of remaining 11, bronze any of remaining 10:
```
P(12, 3) = 12 × 11 × 10 = 1,320
```

### Problem 2: 4-digit numbers with distinct digits from {1, 2, ..., 9}

We choose 4 of the 9 available digits and arrange them in order (since it is a number, position matters):
```
P(9, 4) = 9 × 8 × 7 × 6 = 3,024
```

### Problem 3: How many of the above are divisible by 5?

A number is divisible by 5 only if its last digit is 0 or 5. Since our digits come from {1,...,9}, only 5 is available. So we fix the last digit as 5.

Now choose and arrange the first 3 digits from the 8 remaining digits {1,2,3,4,6,7,8,9}:
```
P(8, 3) = 8 × 7 × 6 = 336
```

Check: 336 / 3024 = 1/9, which makes sense by symmetry — each of the 9 digits is equally likely to appear in any given position.
