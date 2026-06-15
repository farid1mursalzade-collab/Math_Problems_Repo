## Task 1 — Coin Tossing
 
### Setup
 
A fair coin is tossed one or more times. The possible outcome of each single toss is either **H** (Heads) or **T** (Tails). The order of outcomes matters.
 
---
 
### Ω₁ — One Coin Toss
 
```
Ω₁ = { H, T }
```
 
**Number of outcomes:** |Ω₁| = **2**
 
**What is an elementary outcome?**  
It is the result of a single coin toss — either Heads (H) or Tails (T).
 
---
 
### Ω₂ — Two Coin Tosses
 
**Tree Diagram:**
 
```
START
 ├── H (1st toss = Heads)
 │    ├── H  →  HH
 │    └── T  →  HT
 └── T (1st toss = Tails)
      ├── H  →  TH
      └── T  →  TT
```
 
```
Ω₂ = { HH, HT, TH, TT }
```
 
**Number of outcomes:** |Ω₂| = 2² = **4**
 
**What is an elementary outcome?**  
An ordered pair recording the result of the **first** and **second** toss. For example, HT means "first toss was Heads, second toss was Tails." Note that HT ≠ TH — order matters.
 
---
 
### Ω₃ — Three Coin Tosses
 
**Tree Diagram:**
 
```
START
 ├── H
 │    ├── H
 │    │    ├── H  →  HHH
 │    │    └── T  →  HHT
 │    └── T
 │         ├── H  →  HTH
 │         └── T  →  HTT
 └── T
      ├── H
      │    ├── H  →  THH
      │    └── T  →  THT
      └── T
           ├── H  →  TTH
           └── T  →  TTT
```
 
```
Ω₃ = { HHH, HHT, HTH, HTT, THH, THT, TTH, TTT }
```
 
**Number of outcomes:** |Ω₃| = 2³ = **8**
 
**What is an elementary outcome?**  
An ordered triple recording the results of three consecutive tosses, e.g., HTH = "Heads, then Tails, then Heads."
 
---
 
### General Rule
 
| Experiment | Sample space | Number of outcomes |
|------------|-------------|-------------------|
| 1 toss | Ω₁ | 2¹ = 2 |
| 2 tosses | Ω₂ | 2² = 4 |
| 3 tosses | Ω₃ | 2³ = 8 |
| n tosses | Ωₙ | 2ⁿ |
 
The number grows exponentially because at each toss we have 2 choices, and the choices are independent.
