## Task 8 — Sequences with Repetition

**1. How many 5-digit PIN codes are possible if digits may repeat?**
* **Model:** Sequence with repetition
* **Reasoning:** We are forming a sequence of 5 digits. For each of the 5 positions, we can choose any of the 10 available digits (0–9). Since repetitions are allowed and each position is chosen independently, we multiply the possibilities.
* **Calculation:** $10^5 = 10 \times 10 \times 10 \times 10 \times 10 = 100,000$

**2. How many such codes contain at least one repeated digit?**
* **Model:** Complementary counting
* **Reasoning:** Calculating "at least one repeated digit" directly is very complicated because it involves many cases (exactly one pair, two pairs, three of a kind, etc.). It is much easier to take the **total** number of possible PINs (calculated in question 1) and subtract the number of PINs where **all digits are different**. 
* **Calculation:** Total PINs = $100,000$
  PINs with all distinct digits = $P(10, 5) = 10 \times 9 \times 8 \times 7 \times 6 = 30,240$
  PINs with at least one repeat = $100,000 - 30,240 = 69,760$

**3. How many such codes have all digits different?**
* **Model:** k-permutation (ordered selection without repetition)
* **Reasoning:** As calculated in the intermediate step for question 2, if all digits must be different, we are simply selecting and arranging 5 distinct digits from the pool of 10.
* **Calculation:** $P(10, 5) = \frac{10!}{(10-5)!} = 10 \times 9 \times 8 \times 7 \times 6 = 30,240$