## Task 9 — Events and Probabilities in Weekly Weather

We model the seven days as independent, each with P(S) = P(C) = P(R) = 1/3. The sample space Ω₇ has 3⁷ = 2187 equally likely outcomes, each with probability (1/3)⁷.

**Note on day labeling:** Days are Mon(1), Tue(2), Wed(3), Thu(4), Fri(5), Sat(6), Sun(7).

**Event A — entire weekend is sunny (Sat = S and Sun = S):**  
Only days 6 and 7 are constrained. The other 5 days are free to be anything. Since the days are independent:  
P(A) = P(Sat=S) × P(Sun=S) = (1/3) × (1/3) = **1/9**

**Event B — Wednesday, Thursday, and Friday are all rainy:**  
P(B) = P(Wed=R) × P(Thu=R) × P(Fri=R) = (1/3)³ = **1/27**

**Event C — at least one day during the week is sunny:**  
The complement of C is "no day is sunny," meaning every day is either Cloudy or Rainy (2 options per day).  
P(no sunny day) = (2/3)⁷ = 128/2187  
P(C) = 1 − 128/2187 = **2059/2187 ≈ 0.941**

This makes intuitive sense: it is very unlikely to have an entire week with no sunshine at all.

**Event D — no rainy day during the entire week:**  
Each day must be either S or C (probability 2/3 each, independently).  
P(D) = (2/3)⁷ = **128/2187 ≈ 0.059**

**Event E — exactly two days are sunny:**  
This follows the binomial distribution with n=7 trials and success probability p=1/3 (where "success" = sunny).  
P(E) = C(7,2) × (1/3)² × (2/3)⁵  
= 21 × (1/9) × (32/243)  
= 21 × 32 / 2187  
= **672/2187 ≈ 0.307**

**Additional event — F — exactly one day is rainy:**  
P(F) = C(7,1) × (1/3)¹ × (2/3)⁶  
= 7 × (1/3) × (64/729)  
= 448/2187 ≈ **0.205**