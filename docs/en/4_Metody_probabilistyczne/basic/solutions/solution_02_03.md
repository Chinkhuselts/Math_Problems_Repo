## Task 3 — Permutations with Repeated Elements

**1. How many distinct arrangements of the word MISSISSIPPI are possible?**
* **Model:** Permutation with repeated elements
* **Reasoning:** We are arranging all 11 letters, but several letters repeat (four 'I's, four 'S's, and two 'P's). We must divide the total permutations by the factorials of the repeated counts to avoid overcounting identical arrangements.
* **Calculation:** Total letters ($n$) = 11
  Frequencies: M=1, I=4, S=4, P=2
  $$\frac{11!}{4! \times 4! \times 2!} = \frac{39,916,800}{24 \times 24 \times 2} = 34,650$$

**2. How many distinct arrangements of STATISTICS are possible?**
* **Model:** Permutation with repeated elements
* **Reasoning:** Similar to the previous problem, we are arranging all 10 letters, but we have repeating characters (three 'S's, three 'T's, and two 'I's).
* **Calculation:**
  Total letters ($n$) = 10
  Frequencies: S=3, T=3, A=1, I=2, C=1
  $$\frac{10!}{3! \times 3! \times 2!} = \frac{3,628,800}{6 \times 6 \times 2} = 50,400$$

**3. How many of the arrangements of STATISTICS start with the letter S?**
* **Model:** Permutation with repeated elements (with a fixed condition)
* **Reasoning:** Since the first letter is fixed as 'S', we only need to arrange the remaining 9 letters. We must also update our frequency counts because one 'S' has already been used.
* **Calculation:**
  Remaining letters ($n$) = 9
  Remaining frequencies: S=2, T=3, A=1, I=2, C=1
  $$\frac{9!}{2! \times 3! \times 2!} = \frac{362,880}{2 \times 6 \times 2} = 15,120$$
