## Task 6 — Events and Probabilities in Coin Tossing

For a fair coin, every elementary outcome in each sample space is equally likely. This means:

- In Ω₁: each outcome has probability 1/2
- In Ω₂: each outcome has probability 1/4
- In Ω₃: each outcome has probability 1/8

An **event** is any subset of the sample space. The probability of an event is the number of favorable outcomes divided by the total number of outcomes (when all outcomes are equally likely).

### One Coin Toss — Events

**A₁ — the result is Heads:**  
A₁ = { H }  
P(A₁) = 1/2

**B₁ — the result is Tails:**  
B₁ = { T }  
P(B₁) = 1/2

**C₁ — the result is NOT Tails:**  
C₁ = { H } (the complement of B₁)  
P(C₁) = 1/2

Notice that A₁ = C₁: getting Heads is the same as not getting Tails.

### Two Coin Tosses — Events

Working from Ω₂ = { (H,H), (H,T), (T,H), (T,T) }, each with probability 1/4.

**A₂ — exactly one head occurs:**  
We need sequences with exactly one H: (H,T) and (T,H).  
A₂ = { (H,T), (T,H) }  
P(A₂) = 2/4 = **1/2**

**B₂ — at least one head occurs:**  
"At least one" means one or more. The only outcome with no heads is (T,T).  
B₂ = { (H,H), (H,T), (T,H) }  
P(B₂) = 3/4

*Shortcut:* P(at least one head) = 1 − P(no heads) = 1 − P({ (T,T) }) = 1 − 1/4 = 3/4.

**C₂ — both tosses give the same result:**  
C₂ = { (H,H), (T,T) }  
P(C₂) = 2/4 = **1/2**

### Three Coin Tosses — Events

Working from Ω₃, each of the 8 outcomes has probability 1/8.

**A₃ — exactly two heads occur:**  
Outcomes with exactly 2 H's: HHT, HTH, THH.  
A₃ = { HHT, HTH, THH }  
P(A₃) = 3/8

**B₃ — at least one tail occurs:**  
The complement is "no tails at all," which is only HHH.  
P(B₃) = 1 − P({ HHH }) = 1 − 1/8 = **7/8**

**C₃ — all three tosses give the same result:**  
Either all Heads or all Tails.  
C₃ = { HHH, TTT }  
P(C₃) = 2/8 = **1/4**

**Additional event — D₃ — the first and last toss differ:**  
We need sequences where the 1st and 3rd positions are different:
- HTH: 1st=H, 3rd=H → same, not in event
- HHT: 1st=H, 3rd=T → different ✓
- HTT: 1st=H, 3rd=T → different ✓
- THH: 1st=T, 3rd=H → different ✓
- TTH: 1st=T, 3rd=H → different ✓
- HHH: same, not in event
- TTT: same, not in event
- THT: 1st=T, 3rd=T → same, not in event

D₃ = { HHT, HTT, THH, TTH }  
P(D₃) = 4/8 = **1/2**
