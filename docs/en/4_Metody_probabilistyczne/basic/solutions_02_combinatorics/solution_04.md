## Task 4 — Circular Permutations

In a circular arrangement, only the relative position of people matters — rotating everyone one seat does not change the arrangement. We fix one person to eliminate equivalent rotations, and arrange the rest.

For n distinct people in a circle: **(n−1)!** arrangements.

### Problem 1: 8 people around a round table

Fix one person. Arrange the other 7:
```
(8−1)! = 7! = 5,040
```

### Problem 2: 8 people, two particular people (A and B) MUST be adjacent

Treat A and B as one unit. Now we have 7 "people" in a circle:
```
(7−1)! × 2 = 6! × 2 = 720 × 2 = 1,440
```

The factor of 2 accounts for the two internal arrangements of A and B within their unit (A on the left of B, or B on the left of A).

### Problem 3: 8 people, A and B must sit directly OPPOSITE each other

In a circular table with 8 seats, each seat has exactly one seat directly across the table.

Fix A in one seat (this is our standard circular-arrangement fix). The seat directly opposite A is uniquely determined — B must sit there. There is only 1 way to place B.

Now the remaining 6 people fill the 6 remaining seats in any order:
```
6! = 720
```