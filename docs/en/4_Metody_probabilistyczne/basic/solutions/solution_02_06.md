## Task 6 — Combinations in Card Problems

A standard deck contains 52 cards. There are 13 hearts and 39 non-hearts. There are 12 face cards (J, Q, K) and 40 non-face cards.

**1. In how many ways can 5 cards be drawn so that the hand contains exactly 2 hearts?**
* **Model:** Combinations with the Product Rule
* **Reasoning:** To get exactly 2 hearts, we must choose 2 hearts from the 13 available hearts, AND we must choose the remaining 3 cards from the 39 available non-heart cards. The order of drawing doesn't matter.
* **Calculation:** $\binom{13}{2} \times \binom{39}{3} = \left(\frac{13 \times 12}{2}\right) \times \left(\frac{39 \times 38 \times 37}{3 \times 2 \times 1}\right) = 78 \times 9,139 = 712,842$

**2. In how many ways can a 5-card hand contain at least one heart?**
* **Model:** Complementary counting with Combinations
* **Reasoning:** Calculating "at least one" directly requires summing multiple cases (1 heart, 2 hearts, 3 hearts...). It is much easier to take the total number of possible 5-card hands and subtract the number of hands that contain ZERO hearts (which means all 5 cards are drawn from the 39 non-hearts).
* **Calculation:** Total hands = $\binom{52}{5} = 2,598,960$
  Hands with NO hearts = $\binom{39}{5} = 575,757$
  Hands with AT LEAST ONE heart = $2,598,960 - 575,757 = 2,023,203$

**3. In how many ways can a 5-card hand contain no face cards (J, Q, K)?**
* **Model:** Combination
* **Reasoning:** We want to completely exclude the 12 face cards from our selection pool. We only choose our 5 cards from the remaining 40 non-face cards.
* **Calculation:** $\binom{40}{5} = \frac{40 \times 39 \times 38 \times 37 \times 36}{5 \times 4 \times 3 \times 2 \times 1} = 658,008$