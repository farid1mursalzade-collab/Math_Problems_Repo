## Task 3 — Drawing Cards

We have a standard deck of 52 cards. Each card is unique (a specific combination of rank and suit). The order of draws is recorded.

### Ω₁ — Drawing one card

There are 52 distinct cards, each one a possible outcome.

**|Ω₁| = 52**

Each elementary outcome represents: *the specific card drawn* (for example, the King of Hearts, or the 7 of Clubs).

### Ω₂ — Two draws **with replacement**

After drawing the first card, we record it and place it back into the deck. The deck is then shuffled and we draw again. Because the first card is returned, the second draw is independent of the first — the same card could theoretically be drawn twice.

The number of ordered pairs is:

```
|Ω₂| = 52 × 52 = 2704
```

Each elementary outcome represents: *an ordered pair (first card drawn, second card drawn), where both draws come from the full 52-card deck.*

### Ω₂' — Two draws **without replacement**

Now after drawing the first card, we do not return it. The second draw comes from only 51 remaining cards. The first card cannot appear again.

```
|Ω₂'| = 52 × 51 = 2652
```

Each elementary outcome represents: *an ordered pair (first card drawn, second card drawn), where the two cards are necessarily different.*

**Key difference:** With replacement, we have 2704 outcomes because repetitions are allowed. Without replacement, we have 2652 outcomes because the first card is no longer available for the second draw. This difference in structure leads to different probabilities.

---
