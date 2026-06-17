## Task 4 — Weekly Weather Observation

The weather on each day is classified into exactly one of three states: Sunny (S), Cloudy (C), or Rainy (R). We observe weather for seven consecutive days.

### Ω₁ — Weather on one day

```
Ω₁ = { S, C, R }
```

**|Ω₁| = 3**

### Ω₂ — Weather on two consecutive days

Each ordered pair of daily weather states is one outcome:

```
Ω₂ = { (w₁, w₂) : w₁, w₂ ∈ {S, C, R} }
```

This gives us **|Ω₂| = 3 × 3 = 9** ordered pairs: (S,S), (S,C), (S,R), (C,S), (C,C), (C,R), (R,S), (R,C), (R,R).

### Ω₇ — Weather over seven days

An elementary outcome is a sequence of seven weather states, one for each day of the week:

```
Ω₇ = { (w₁, w₂, w₃, w₄, w₅, w₆, w₇) : each wᵢ ∈ {S, C, R} }
```

**|Ω₇| = 3⁷ = 2187** ordered 7-tuples.

A typical elementary outcome might look like: **(S, C, R, S, R, C, S)**, which would mean Monday is Sunny, Tuesday is Cloudy, Wednesday is Rainy, Thursday is Sunny, Friday is Rainy, Saturday is Cloudy, Sunday is Sunny.

Each elementary outcome represents: *the complete description of the weather across all seven days of the week, day by day in order.* Two outcomes are different if even a single day has a different weather state.
