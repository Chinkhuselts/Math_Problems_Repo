## Task 9 — Digit Restrictions

**1. How many 5-digit numbers exist?**
* **Model:** Product Rule (Sequence with repetition and a restriction)
* **Reasoning:** A 5-digit number cannot start with the digit 0 (otherwise it would be a 4-digit number). Therefore, the 1st digit has 9 options (1–9). The remaining 4 digits can be anything from 0–9, giving them 10 options each. Repetition is allowed.
* **Calculation:** $9 \times 10 \times 10 \times 10 \times 10 = 90,000$

**2. How many of them are even?**
* **Model:** Product Rule with restrictions
* **Reasoning:** For a number to be even, its last digit must be 0, 2, 4, 6, or 8 (5 options). The first digit still cannot be 0 (9 options). The middle three digits can be anything (10 options each).
* **Calculation:** $9 \times 10 \times 10 \times 10 \times 5 = 45,000$ *(Alternatively, exactly half of all possible 5-digit numbers are even: $90,000 / 2 = 45,000$)*

**3. How many contain no repeated digits?**
* **Model:** Product Rule without repetition (modified k-permutation)
* **Reasoning:** We build the number digit by digit. 
  - 1st digit: 9 options (1–9, cannot be 0).
  - 2nd digit: 9 options (0–9, but must exclude the digit chosen for the 1st spot).
  - 3rd digit: 8 options (must exclude the 2 digits already used).
  - 4th digit: 7 options.
  - 5th digit: 6 options.
* **Calculation:** $9 \times 9 \times 8 \times 7 \times 6 = 27,216$

**4. How many contain at least one repeated digit?**
* **Model:** Complementary counting
* **Reasoning:** Similar to the PIN code problem, "at least one" is best solved by taking the total number of valid outcomes and subtracting the outcomes we don't want (the ones with completely distinct digits).
* **Calculation:** Total 5-digit numbers = $90,000$
  Numbers with NO repeated digits = $27,216$
  Numbers with AT LEAST ONE repeat = $90,000 - 27,216 = 62,784$