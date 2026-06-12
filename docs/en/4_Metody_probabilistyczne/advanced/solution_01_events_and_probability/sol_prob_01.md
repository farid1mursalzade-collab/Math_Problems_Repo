# Solution

## Task 1
# Task 1 — Coin Tossing

## 🎯 Objective
Construct the sample spaces for one, two, and three tosses of a **fair coin**, and identify what an elementary outcome represents in each case.

---

## 🛠️ Setup
* Every **fair coin** has two possible results per toss:
  * `"H"` = Heads
  * `"T"` = Tails
* The **order of outcomes matters** — each toss is a separate stage of the experiment.

---

## 🌿 Tree Diagrams

### One Toss
START
├── H
└── T


### Two Tosses
START
├── H ── H  -> (H, H)
│     └── T  -> (H, T)
└── T ── H  -> (T, H)
└── T  -> (T, T)


### Three Tosses
START
├── H ── H ── H  -> (H, H, H)
│     │     └── T  -> (H, H, T)
│     └── T ── H  -> (H, T, H)
│           └── T  -> (H, T, T)
└── T ── H ── H  -> (T, H, H)
│     └── T  -> (T, H, T)
└── T ── H  -> (T, T, H)
└── T  -> (T, T, T)


---

## 📝 Solutions

### 1. Sample Space for One Toss — $\Omega_1$
$$\Omega_1 = \{ H, T \}$$

* **Number of elementary outcomes:**
$$|\Omega_1| = 2$$

### 2. Sample Space for Two Tosses — $\Omega_2$
$$\Omega_2 = \{ (H, H), (H, T), (T, H), (T, T) \}$$

* **Number of elementary outcomes:**
$$|\Omega_2| = 2 \times 2 = 4$$

### 3. Sample Space for Three Tosses — $\Omega_3$
$$\Omega_3 = \{ (H,H,H), (H,H,T), (H,T,H), (H,T,T), (T,H,H), (T,H,T), (T,T,H), (T,T,T) \}$$

* **Number of elementary outcomes:**
$$|\Omega_3| = 2 \times 2 \times 2 = 8$$

---

## 🔢 4. General Formula

For $n$ coin tosses, the number of elementary outcomes is:
$$|\Omega_n| = 2^n$$

| Experiment | Sample Space Size |
| :--- | :--- |
| $\Omega_1$ (1 toss) | $2^1 = 2$ |
| $\Omega_2$ (2 tosses) | $2^2 = 4$ |
| $\Omega_3$ (3 tosses) | $2^3 = 8$ |

---

## 🔍 5. What Does an Elementary Outcome Represent?

| Sample Space | Elementary Outcome | Meaning |
| :---: | :---: | :--- |
| $\Omega_1$ | $H$ or $T$ | The single result of one coin toss. |
| $\Omega_2$ | $(x_1, x_2)$ where $x_i \in \{H, T\}$ | An ordered pair recording the result of toss 1 and toss 2. |
| $\Omega_3$ | $(x_1, x_2, x_3)$ where $x_i \in \{H, T\}$ | An ordered triple recording the result of each of the three tosses in sequence. |

> ⚠️ **Note:** The order matters — the outcome $(H, T)$ is different from $(T, H)$, because the first toss gave a different result in each case.

---

## 💡 Key Insights

* **Exponential Growth:** Every time we add another coin toss, the size of the sample space doubles ($2^n$). This happens because each existing branch splits into two new possibilities (Heads or Tails).
* **Order and Distinction:** Tracking outcomes as ordered sequences (tuples) ensures we do not compress distinct experimental realities. For example, flipping a Head then a Tail is physically a different sequence than flipping a Tail then a Head.
* **Foundation for Probability:** Knowing the exact size of these symmetric, equally likely sample spaces allows us to easily calculate classical probabilities using the formula:
$$P(A) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}$$
