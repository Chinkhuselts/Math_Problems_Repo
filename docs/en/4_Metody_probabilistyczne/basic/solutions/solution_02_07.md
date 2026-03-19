## Task 7 — k-Permutations (Ordered Selections Without Repetition)

**1. In how many ways can the first three places be assigned among 12 runners?**
* **Model:** k-permutation (ordered selection without repetition)
* **Reasoning:** We are selecting a subset of 3 runners from the 12 available. Order absolutely matters because 1st, 2nd, and 3rd places are distinct. A runner cannot win more than one place, so repetition is not allowed.
* **Calculation:** $P(12, 3) = \frac{12!}{(12-3)!} = 12 \times 11 \times 10 = 1,320$

**2. How many 4-digit numbers with distinct digits can be formed from the digits 1–9?**
* **Model:** k-permutation
* **Reasoning:** We are choosing 4 digits from a pool of 9 possible digits (1 through 9, excluding 0). The order of digits matters to form different numbers (e.g., 1234 is different from 4321), and the problem explicitly states the digits must be "distinct" (no repetition).
* **Calculation:** $P(9, 4) = \frac{9!}{(9-4)!} = 9 \times 8 \times 7 \times 6 = 3,024$

**3. How many of these numbers are divisible by 5?**
* **Model:** k-permutation with a fixed condition (Product Rule)
* **Reasoning:** For a number formed from the digits 1–9 to be divisible by 5, it *must* end in the digit 5 (since 0 is not in our allowed set). Therefore, the 4th digit is fixed (1 option). We must now select and arrange the remaining 3 digits from the 8 remaining available digits.
* **Calculation:** $1 \times P(8, 3) = 1 \times (8 \times 7 \times 6) = 336$