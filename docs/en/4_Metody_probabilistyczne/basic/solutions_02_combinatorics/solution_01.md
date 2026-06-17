## Task 1 — Recognizing Counting Models

Let us go through each situation carefully.

**1. Arranging 7 students in a line.**
- Are we using all objects? YES (all 7 students).
- Are any identical? NO (each student is a distinct person).
- Are they in a circle? NO (a line has a first and last position).
- Model: **Permutation** → 7!

**2. Choosing 4 members of a committee from 12 people.**
- Are we using all? NO (only 4 out of 12).
- Does order matter? NO (a committee {Alice, Bob, Carol, Dan} is the same regardless of who was chosen first).
- Repetition? NO (a person cannot be on the committee twice).
- Model: **Combination** → C(12, 4)

**3. Assigning gold, silver, and bronze medals among 15 athletes.**
- Are we using all? NO (only 3 out of 15).
- Does order matter? YES (gold ≠ silver ≠ bronze — the rank of each medal matters).
- Repetition? NO (one person cannot win two medals).
- Model: **k-Permutation (ordered selection without repetition)** → P(15, 3)

**4. Forming a 6-digit PIN code.**
- Are we using all available symbols? Not necessarily — the same digit can appear more than once.
- Does order matter? YES (the PIN 123456 is different from 654321).
- Repetition allowed? YES (e.g., PIN 112233 is valid).
- Model: **Sequence with repetition** → 10⁶

**5. Arranging the letters of the word BANANA.**
- Letters: B(1), A(3), N(2) → total 6 letters, some identical.
- Are we using all? YES (all 6 letters are arranged).
- Are some identical? YES (A repeats 3 times, N repeats 2 times).
- Model: **Permutation with repeated elements** → 6! / (3! × 2! × 1!)

**6. Seating 6 people around a round table.**
- Are we using all? YES.
- Are they in a circle? YES (rotations of the same arrangement are considered identical — if everyone shifts one seat clockwise, it is the same seating).
- Model: **Circular permutation** → (6−1)! = 5!