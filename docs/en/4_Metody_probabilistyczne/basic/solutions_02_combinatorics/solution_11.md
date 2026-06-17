## Task 11 — Modeling Outcomes

### 1. Distinguishable vs. Indistinguishable

Box: 4 red (R), 4 blue (B), 3 green (G) balls = 11 balls total.

**(a) Indistinguishable balls of same color — how many linear arrangements?**

We are arranging 11 items in a line where 4 are identical red, 4 are identical blue, 3 are identical green. Swapping two red balls changes nothing visually.

```
11! / (4! × 4! × 3!) = 39,916,800 / (24 × 24 × 6) = 39,916,800 / 3,456 = 11,550
```

**(b) All balls individually labeled (R₁, R₂, R₃, R₄, B₁, ..., G₃) — how many arrangements?**

Now every ball is distinct. Any rearrangement creates a new outcome:
```
11! = 39,916,800
```

**(c) Why are the answers different?**

In case (a), swapping R₁ and R₂ gives the exact same visible arrangement — we cannot tell them apart. So the 39,916,800 arrangements of labeled balls collapse into groups of duplicates. The denominator 4!×4!×3! divides out exactly those duplicates, giving the true number of distinguishable arrangements.

In case (b), every ball has a unique identity, so every permutation is genuinely new. There is no collapsing.

### 2. Recording Order vs. Ignoring Order

Drawing 3 balls from the same box (4R, 4B, 3G) without replacement:

**(a) Only the SET of colors is recorded (order ignored)**

We describe each outcome as a multiset of colors drawn. Since we draw only 3 balls and the maximum available of any color exceeds 3 (for R and B) and equals 3 (for G), all color multisets of size 3 are possible:

{R,R,R}, {R,R,B}, {R,R,G}, {R,B,B}, {R,B,G}, {R,G,G}, {B,B,B}, {B,B,G}, {B,G,G}, {G,G,G}

This gives **10 possible color outcomes** (note: these are not equally likely).

**(b) The SEQUENCE of colors is recorded (order matters)**

Now (R,B,G) is different from (B,R,G). With 3 colors and 3 draws, we have 3³ = **27 possible ordered color sequences**, all of which are feasible (no color requires more than 3 balls, and we have at least 3 of each).

**(c) Why does recording order change the count?**

When order matters, (R,B,G), (R,G,B), (B,R,G), (B,G,R), (G,R,B), and (G,B,R) are all different outcomes. When only the set is recorded, these 6 sequences collapse into the single set {R,B,G}. Tracking order multiplies the number of distinct outcomes.

### 3. PIN Code vs. 4-Digit Number

**(a) 4-digit PINs:**
```
10⁴ = 10,000 (from 0000 to 9999)
```

**(b) 4-digit numbers:**
```
9 × 10³ = 9,000 (from 1000 to 9999)
```

**(c) Why different?**
A PIN code like "0042" is perfectly valid — it has leading zeros. But "0042" as a number is simply 42, a 2-digit number, not a 4-digit number. The rules are different for each context.

**(d) Why are 1234 and 4321 different PINs?**
A PIN code is an ordered sequence. Position matters: the first digit triggers one action, the second another. The code 1234 is not the same code as 4321 even though they contain the same four digits. This is why PINs are sequences, not sets.
