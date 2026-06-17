## Task 12 — Mixed Counting Problem

### 1. Student ID Codes (2 letters from {A,B,C,D,E} + 3 digits from 0–9)

**(a) Letters and digits may repeat:**
- 2 letters from 5, with repetition: 5² = 25 ways (sequence with repetition)
- 3 digits from 10, with repetition: 10³ = 1,000 ways
- Total: 25 × 1,000 = **25,000**

**(b) Letters may not repeat, digits may:**
- 2 letters from 5, without repetition, ordered: P(5,2) = 5 × 4 = 20 ways
- 3 digits from 10, with repetition: 10³ = 1,000 ways
- Total: 20 × 1,000 = **20,000**

**(c) Neither letters nor digits may repeat:**
- 2 letters from 5, ordered, no repeat: P(5,2) = 20 ways
- 3 digits from 10, ordered, no repeat: P(10,3) = 10 × 9 × 8 = 720 ways
- Total: 20 × 720 = **14,400**

### 2. Medal Assignment (12 runners, gold/silver/bronze)

**(a) How many ways to assign medals?**
An ordered selection of 3 from 12 — each medal is distinct:
```
P(12, 3) = 12 × 11 × 10 = 1,320
```

**(b) Two specific runners (A and B) must BOTH receive medals:**
Both A and B must get a medal, along with one other runner.

Step 1: Which medal does A get? 3 choices.  
Step 2: Which of the 2 remaining medals does B get? 2 choices.  
Step 3: Which of the 10 other runners gets the last medal? 10 choices.

```
3 × 2 × 10 = 60
```

### 3. Committee of 4 from 10 (6 men, 4 women)

**(a) Any committee:**
```
C(10, 4) = 210
```

**(b) Exactly 2 women:**
```
C(4, 2) × C(6, 2) = 6 × 15 = 90
```

**(c) At least one woman:**
Total − all men:
```
C(10, 4) − C(6, 4) = 210 − 15 = 195
```

### 4. Circular Seating (7 people at a round table)

**(a) Any arrangement:**
```
(7−1)! = 6! = 720
```

**(b) Two specific people must sit next to each other:**
Treat them as one unit → 6 units in a circle: (6−1)! = 5! = 120. Internal arrangements of the pair: ×2.
```
5! × 2 = 120 × 2 = 240
```

### 5. Passwords (5 characters from 10 digits + 26 letters = 36 symbols)

**(a) Repetition allowed:**
Each of the 5 positions can independently be any of the 36 symbols:
```
36⁵ = 60,466,176
```
Model used: **Sequence with repetition**.

**(b) No character may repeat:**
Each position uses a distinct symbol from the 36 available:
```
P(36, 5) = 36 × 35 × 34 × 33 × 32 = 45,239,040
```
Model used: **k-Permutation (ordered selection without repetition)**.

---
