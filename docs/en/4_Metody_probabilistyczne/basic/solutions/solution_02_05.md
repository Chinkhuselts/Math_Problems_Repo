## Task 5 — Combinations

**1. A committee of 4 people is chosen from 12 students. How many committees are possible?**
* **Model:** Combination
* **Reasoning:** We are choosing a subset of 4 people from a total of 12. The order in which the committee members are selected does not matter, and repetition is not allowed (you can't pick the same person twice).
* **Calculation:** $\binom{12}{4} = \frac{12!}{4!(12-4)!} = \frac{12 \times 11 \times 10 \times 9}{4 \times 3 \times 2 \times 1} = 495$

**2. How many committees contain a particular student?**
* **Model:** Combination (with fixed inclusion)
* **Reasoning:** One spot on the 4-person committee is guaranteed to this specific student (1 way to choose them). We now only need to fill the remaining 3 spots from the remaining 11 students. 
* **Calculation:** $\binom{1}{1} \times \binom{11}{3} = 1 \times \frac{11!}{3!(11-3)!} = \frac{11 \times 10 \times 9}{3 \times 2 \times 1} = 165$

**3. How many committees contain at least one of two particular students?**
* **Model:** Complementary counting with Combinations
* **Reasoning:** It is much easier to calculate the *total* number of possible committees and subtract the number of committees that contain *neither* of the two particular students. If we exclude both students, we are choosing 4 members from the remaining 10 students. 
* **Calculation:** Total committees = $\binom{12}{4} = 495$
  Committees with neither student = $\binom{10}{4} = \frac{10 \times 9 \times 8 \times 7}{4 \times 3 \times 2 \times 1} = 210$
  Committees with at least one = $495 - 210 = 285$

**4. How many committees contain exactly two women if the group consists of 7 men and 5 women?**
* **Model:** Combinations with the Product Rule
* **Reasoning:** We must construct the committee by completing two independent sub-tasks: choosing exactly 2 women from the 5 available women, AND choosing exactly 2 men from the 7 available men to complete the 4-person committee.
* **Calculation:** $\binom{5}{2} \times \binom{7}{2} = \left(\frac{5 \times 4}{2}\right) \times \left(\frac{7 \times 6}{2}\right) = 10 \times 21 = 210$