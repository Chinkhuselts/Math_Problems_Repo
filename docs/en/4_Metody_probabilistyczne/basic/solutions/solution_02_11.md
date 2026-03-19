## Task 11 — Modeling Outcomes

### 1. Distinguishable vs Indistinguishable Objects

A box contains 11 balls: 4 red, 4 blue, 3 green.

**1. How many linear arrangements of all 11 balls are possible if balls of the same color are treated as indistinguishable?**
* **Model:** Permutations with repeated elements
* **Calculation:** Total balls = 11. We divide by the factorials of the repeated colors.
  $$\frac{11!}{4! \times 4! \times 3!} = 11,550$$

**2. How many arrangements are possible if every ball is individually labeled ($R_1, R_2, \dots$)?**
* **Model:** Permutation
* **Calculation:** Because every ball has a unique label, they are all distinct objects. We simply arrange 11 unique items.
  $$11! = 39,916,800$$

**3. Explain why the answers in parts (1) and (2) are different.**
* **Explanation:** When objects are indistinguishable, swapping two red balls (e.g., $R_1$ and $R_2$) creates the exact same visual sequence. We divide by $4!$, $4!$, and $3!$ in part (1) to remove these identical, duplicated arrangements. In part (2), every swap creates a mathematically unique sequence because of the distinct labels.

---

### 2. Recording Order vs Ignoring Order

Three balls are drawn without replacement from the same box.

**1. How many outcomes are possible if only the set of colors is recorded (order ignored)?**
* **Model:** Combinations with repetition (or simple enumeration)
* **Calculation:** Since we only draw 3 balls, and we have at least 3 of every color in the box, we can use the "stars and bars" formula to choose 3 items from 3 color categories: $\binom{n+k-1}{k} = \binom{3+3-1}{3} = \binom{5}{3} = 10$. 
  *(Alternatively, list them: 3 of same color [3 ways], 2 of one color & 1 of another [6 ways], 1 of each color [1 way]. $3 + 6 + 1 = 10$.)*

**2. How many outcomes are possible if the sequence of colors is recorded?**
* **Model:** Sequence with repetition
* **Calculation:** Since we are recording the order, and we have enough of each color to draw the same color 3 times, each of the 3 draws can be any of the 3 colors (Red, Blue, or Green).
  $$3 \times 3 \times 3 = 3^3 = 27$$

**3. Explain why recording the order changes the counting model.**
* **Explanation:** When order is ignored, drawing (Red, Blue, Green) is identical to drawing (Green, Blue, Red) — they form the same subset of colors. When order is recorded, these become two distinct events, shifting the model from subsets (combinations) to sequences.

---

### 3. PIN Code vs Number

**1. How many different 4-digit PIN codes are possible if repetition is allowed?**
* **Model:** Sequence with repetition
* **Calculation:** $10 \times 10 \times 10 \times 10 = 10^4 = 10,000$

**2. Consider 4-digit numbers, where the first digit cannot be zero. How many such numbers exist?**
* **Model:** Product rule with a restriction
* **Calculation:** $9 \times 10 \times 10 \times 10 = 9 \times 10^3 = 9,000$

**3. Explain why a PIN code and a 4-digit number are counted using different rules.**
* **Explanation:** A PIN is a string of characters where a leading zero is perfectly valid (e.g., `0451` is a 4-character PIN). A number is a mathematical magnitude; a "4-digit number" mathematically cannot start with `0` because `0451` simplifies to `451`, making it a 3-digit number. 

**4. Explain why the codes 1234 and 4321 must be treated as different outcomes.**
* **Explanation:** A PIN code is a specific sequence of keystrokes. Order is an inherent property of a sequence. Entering the digits in a different order fails the security check, making them distinct outcomes.