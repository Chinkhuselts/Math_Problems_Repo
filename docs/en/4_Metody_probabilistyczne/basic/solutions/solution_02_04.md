## Task 4 — Circular Permutations

**1. In how many ways can 7 people sit around a round table?**
* **Model:** Circular permutation
* **Reasoning:** We are arranging all 7 people in a circle. Because there is no fixed starting point, we use the formula $(n-1)!$.
* **Calculation:** $(7-1)! = 6! = 720$

**2. In how many ways can they sit if two particular people must sit next to each other?**
* **Model:** Circular permutation (with a grouped block) and the Product Rule
* **Reasoning:** Treat the two specific people as a single "block". Now we have 6 total units (5 single people + 1 block) to arrange in a circle. The circular arrangement of these 6 units is $(6-1)! = 5!$. Within the block itself, the two people can swap places with each other in $2!$ ways.
* **Calculation:** $5! \times 2! = 120 \times 2 = 240$

**3. In how many ways can they sit if those two people must sit opposite each other?**
* **Model:** Circular permutation (with fixed relative positions)
* **Reasoning:** First, seat one of the two specific people anywhere at the table. Since the table is circular and empty, placing the first person simply establishes the reference point (1 way). The second person *must* sit in the single chair exactly opposite them (1 way). Now, there are 5 remaining distinct seats (distinct because they are now defined by their distance from the two seated people) for the remaining 5 people. These 5 people can be arranged in these distinct seats in standard linear fashion, which is $5!$.
* **Calculation:** $1 \times 1 \times 5! = 120$
