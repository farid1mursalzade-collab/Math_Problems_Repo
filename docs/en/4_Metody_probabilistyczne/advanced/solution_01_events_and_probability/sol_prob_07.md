## Task 7 — Events and Probabilities in Die Rolling

Every elementary outcome in Ω₁ has probability 1/6. In Ω₂, each of 36 outcomes has probability 1/36. In Ω₃, each of 216 outcomes has probability 1/216.

### One Roll

**A₁ — even result:**  
Even faces: {2, 4, 6}  
P(A₁) = 3/6 = **1/2**

**B₁ — result greater than 4:**  
{5, 6}  
P(B₁) = 2/6 = **1/3**

**C₁ — result at most 3:**  
{1, 2, 3}  
P(C₁) = 3/6 = **1/2**

### Two Rolls

**A₂ — sum equals 7:**  
We list all ordered pairs (i, j) with i + j = 7:  
(1,6), (2,5), (3,4), (4,3), (5,2), (6,1) → 6 outcomes  
P(A₂) = 6/36 = **1/6**

This is a well-known result: 7 is the most likely sum when rolling two dice.

**B₂ — both results are the same:**  
(1,1), (2,2), (3,3), (4,4), (5,5), (6,6) → 6 outcomes  
P(B₂) = 6/36 = **1/6**

**C₂ — sum is at least 10:**  
We count outcomes by sum:
- Sum = 10: (4,6), (5,5), (6,4) → 3 outcomes
- Sum = 11: (5,6), (6,5) → 2 outcomes
- Sum = 12: (6,6) → 1 outcome
- Total: 3 + 2 + 1 = 6 outcomes

P(C₂) = 6/36 = **1/6**

### Three Rolls

**A₃ — sum equals 10:**  
We first find unordered combinations of three faces summing to 10, then count how many ordered arrangements each gives:

| Combination | Arrangements | Count |
|---|---|---|
| {1, 3, 6} | 3! = 6 | 6 |
| {1, 4, 5} | 3! = 6 | 6 |
| {2, 2, 6} | 3!/2! = 3 | 3 |
| {2, 3, 5} | 3! = 6 | 6 |
| {2, 4, 4} | 3!/2! = 3 | 3 |
| {3, 3, 4} | 3!/2! = 3 | 3 |

Total favorable outcomes = 6+6+3+6+3+3 = **27**  
P(A₃) = 27/216 = **1/8**

**B₃ — exactly two rolls give the same number:**  
We choose the value that appears twice: 6 options.  
We choose which two of the three positions hold this value: C(3,2) = 3 ways.  
The remaining position must show a different value: 5 choices.  
Total = 6 × 3 × 5 = **90** outcomes  
P(B₃) = 90/216 = **5/12**

**C₃ — outcomes contain two 2s and one 3:**  
The sequence has one die showing 3 and the other two showing 2. The die showing 3 can be in position 1, 2, or 3 → 3 arrangements.  
C₃ = { (2,2,3), (2,3,2), (3,2,2) } → 3 outcomes  
P(C₃) = 3/216 = **1/72**

**Additional event — D₃ — all three dice show different numbers:**  
First die: 6 choices. Second die: must differ → 5 choices. Third die: must differ from both → 4 choices.  
Favorable = 6 × 5 × 4 = 120  
P(D₃) = 120/216 = **5/9**
