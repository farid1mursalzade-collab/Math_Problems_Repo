## Task 2 — Rolling a Die
 
### Setup
 
A fair six-sided die is rolled one or more times. The faces show values 1 through 6. Order matters.
 
---
 
### Ω₁ — One Roll
 
```
Ω₁ = { 1, 2, 3, 4, 5, 6 }
```
 
**Number of outcomes:** |Ω₁| = **6**
 
**What is an elementary outcome?**  
The number showing on the top face after a single roll.
 
---
 
### Ω₂ — Two Consecutive Rolls
 
```
Ω₂ = { (i, j) : i, j ∈ {1, 2, 3, 4, 5, 6} }
```
 
This is the set of all **ordered pairs** where the first element is the result of roll 1 and the second is the result of roll 2. For example, (3, 5) means "3 on the first roll, 5 on the second roll."
 
**Number of outcomes:** |Ω₂| = 6 × 6 = 6² = **36**
 
---
 
### Ω₃ — Three Consecutive Rolls
 
```
Ω₃ = { (i, j, k) : i, j, k ∈ {1, 2, 3, 4, 5, 6} }
```
 
**Number of outcomes:** |Ω₃| = 6³ = **216**
 
**What is an elementary outcome?**  
An ordered triple (i, j, k) giving the results of the first, second, and third roll respectively. For example, (2, 6, 1) is a different outcome from (1, 6, 2) because order matters.
 
---
 
### General Rule
 
| Experiment | Number of outcomes |
|------------|-------------------|
| 1 roll | 6¹ = 6 |
| 2 rolls | 6² = 36 |
| 3 rolls | 6³ = 216 |
