## Task 8 — Events and Probabilities in Card Drawing

### One Card Drawn (from 52, equally likely)

**A₁ — the card is a heart:**  
There are 13 hearts in a 52-card deck.  
P(A₁) = 13/52 = **1/4**

**B₁ — the card is a king:**  
There are 4 kings (one per suit).  
P(B₁) = 4/52 = **1/13**

**C₁ — the card is not a face card:**  
Face cards are Jacks, Queens, and Kings → 3 per suit × 4 suits = 12 face cards.  
Non-face cards: 52 − 12 = 40.  
P(C₁) = 40/52 = **10/13**

### Two Cards With Replacement (from Ω₂, each pair has probability 1/2704)

**A₂ — both cards are hearts:**  
P(first is heart) = 13/52 = 1/4.  
Because the card is returned, P(second is heart) = 13/52 = 1/4 independently.  
P(A₂) = (1/4) × (1/4) = **1/16**

**B₂ — both cards have the same rank:**  
There are 13 possible ranks. For each rank, P(first card is that rank) = 4/52 = 1/13, and P(second card is same rank) = 4/52 (with replacement).  
P(B₂) = 13 × (4/52) × (4/52) = 13 × (1/13) × (1/13) = 1/13

Alternatively: P(second matches first) = 4/52 = **1/13** (whatever the first card, there are 4 cards of its rank in the full deck).

**C₂ — at least one card is an ace:**  
Complementary approach: P(no aces) = P(first not ace) × P(second not ace) = (48/52) × (48/52) = (12/13)² = 144/169.  
P(C₂) = 1 − 144/169 = **25/169**

### Two Cards Without Replacement (from Ω₂', each pair has probability 1/2652)

**A₃ — both cards are hearts:**  
P(first is heart) = 13/52. Given the first is a heart, only 12 hearts remain among 51 cards.  
P(A₃) = (13/52) × (12/51) = 156/2652 = **1/17**

**B₃ — both cards have the same rank:**  
Whatever the first card is, we need the second to match its rank. Since one card of that rank is already drawn, there are 3 remaining cards of that rank among 51 remaining cards.  
P(B₃) = 3/51 = **1/17**

**C₃ — one card is a king and the other is a queen (any order):**  
Case 1 — King first, Queen second: P = (4/52) × (4/51)  
Case 2 — Queen first, King second: P = (4/52) × (4/51)  
These cases are mutually exclusive, so we add:  
P(C₃) = 2 × (4/52)(4/51) = 2 × 16/2652 = 32/2652 = **8/663**

**Additional event — D₃ — both cards are aces (without replacement):**  
P(first is ace) = 4/52. Given that, P(second is also ace) = 3/51.  
P(D₃) = (4/52)(3/51) = 12/2652 = **1/221**
