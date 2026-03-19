## Task 2 — Permutations

**1. In how many ways can 8 different books be arranged on a shelf?**
* **Model:** Permutation
* **Reasoning:** We are arranging all 8 distinct books in a linear sequence, and the order matters. 
* **Calculation:** $8! = 40,320$

**2. In how many ways can 8 people sit in a row if two particular people must sit next to each other?**
* **Model:** Permutation (with a grouped block) and the Product Rule
* **Reasoning:** Treat the two specific people as a single inseparable "block" or "unit". This gives us 7 total units to arrange (the 6 other individuals + the 1 block containing the pair), which can be done in $7!$ ways. However, within that block, the two people can swap seats with each other in $2!$ ways.
* **Calculation:** $7! \times 2! = 5,040 \times 2 = 10,080$

**3. In how many ways can they sit if those two people must not sit next to each other?**
* **Model:** Complementary counting
* **Reasoning:** The easiest way to solve this is to take the total number of unrestricted arrangements for 8 people ($8!$) and subtract the number of arrangements where they *are* sitting together (which we just calculated in question 2).
* **Calculation:** $8! - (7! \times 2!) = 40,320 - 10,080 = 30,240$

**4. In how many ways can 10 questions in a test be ordered if the first question is fixed?**
* **Model:** Permutation
* **Reasoning:** Since the 1st position is locked with a specific question, we only have 9 questions left to arrange in the remaining 9 positions. This is simply a permutation of those remaining 9 elements.
* **Calculation:** $9! = 362,880$
