## Task 2 — Permutations

### Problem 1: 8 books on a shelf

All 8 distinct books are arranged in a line. The first position can be any of the 8 books, the second any of the remaining 7, and so on. By the multiplication principle:

```
8 × 7 × 6 × 5 × 4 × 3 × 2 × 1 = 8! = 40,320
```

### Problem 2: 8 people in a row, two particular people MUST sit next to each other

Let us call these two people A and B. The key idea is to treat A and B as a single "super-person" (a unit). This unit can be arranged internally in 2 ways (AB or BA).

Now we have 7 entities to arrange (the super-unit + the other 6 people):
```
7! × 2 = 5,040 × 2 = 10,080
```

### Problem 3: 8 people in a row, two people must NOT sit next to each other

The easiest approach uses complementary counting:
- Total arrangements: 8! = 40,320
- Arrangements where A and B ARE together: 10,080 (from above)
- Arrangements where A and B are NOT together: 40,320 − 10,080 = **30,240**

### Problem 4: 10 questions in a test, first question is fixed

Since the first question cannot be moved, we only arrange the remaining 9 questions in the remaining 9 positions:
```
9! = 362,880
```
