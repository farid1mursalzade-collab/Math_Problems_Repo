## Task 5 — Combinations

A combination selects k items from n without regard to order.

### Problem 1: Committee of 4 from 12

```
C(12, 4) = 12! / (4! × 8!) = (12 × 11 × 10 × 9) / (4 × 3 × 2 × 1) = 11,880 / 24 = 495
```

### Problem 2: Committee must contain one particular student (call them Alice)

Fix Alice's spot. We need to choose the remaining 3 members from the other 11 students:
```
C(11, 3) = 11! / (3! × 8!) = (11 × 10 × 9) / 6 = 165
```

### Problem 3: Committee must contain at least one of two particular students (Alice or Bob)

**Method — complementary counting:**
- Total committees: C(12, 4) = 495
- Committees with NEITHER Alice NOR Bob (chosen from the 10 others): C(10, 4) = 210
- Committees with at least one of them: 495 − 210 = **285**

### Problem 4: Exactly two women, from a group of 7 men and 5 women

Choose 2 women from 5: C(5, 2) = 10  
Choose 2 men from 7: C(7, 2) = 21  
By the multiplication principle:
```
C(5, 2) × C(7, 2) = 10 × 21 = 210