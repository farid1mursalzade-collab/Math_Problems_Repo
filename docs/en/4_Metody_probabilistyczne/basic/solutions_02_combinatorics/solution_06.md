## Task 6 — Combinations in Card Problems

A standard 52-card deck has 4 suits (hearts, diamonds, clubs, spades) of 13 cards each. Face cards are J, Q, K (3 per suit × 4 suits = 12 face cards total).

### Problem 1: 5-card hand with exactly 2 hearts

We must choose 2 hearts from the 13 hearts, and 3 non-hearts from the 39 non-hearts:
```
C(13, 2) × C(39, 3) = 78 × 9,139 = 712,842
```

### Problem 2: 5-card hand with at least one heart

**Complementary approach** (easier than counting directly):
- Total 5-card hands: C(52, 5) = 2,598,960
- Hands with NO hearts (all 5 from the 39 non-hearts): C(39, 5) = 575,757
- Hands with at least one heart: 2,598,960 − 575,757 = **2,023,203**

### Problem 3: 5-card hand with no face cards

Remove the 12 face cards; only 40 non-face cards remain. Choose 5:
```
C(40, 5) = 40! / (5! × 35!) = (40×39×38×37×36) / 120 = 658,008
```