## Task 5 — Multinomial Model (Categories of Outcomes)

**1. Describe the random experiment.**
* **Description:** The experiment consists of rolling a fair six-sided die 5 times independently. Unlike the binomial model which only has two outcomes (success/failure), each trial here falls into one of three mutually exclusive categories (Small, Medium, or Large). Because there are multiple categories and a fixed number of independent trials, this is modeled by a multinomial distribution.

**2. Define the sample space.**
* **Sample Space:** Let $X_1, X_2,$ and $X_3$ represent the number of times the die lands on Small, Medium, and Large, respectively. Since we roll the die exactly 5 times, the sample space consists of all possible combinations of these counts that add up to 5:
  $$\Omega = \{(k_1, k_2, k_3) \mid k_1 + k_2 + k_3 = 5 \text{ and } k_i \in \{0, 1, 2, 3, 4, 5\}\}$$

**3. Specify the multinomial distribution.**
* **Distribution:** First, identify the probabilities for a single roll. Since each category covers 2 out of the 6 faces of a fair die, $p_1 = p_2 = p_3 = \frac{2}{6} = \frac{1}{3}$. For $n = 5$ trials, the probability of getting exactly $k_1$ Small, $k_2$ Medium, and $k_3$ Large outcomes is given by the multinomial formula:
  $$P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{5!}{k_1! k_2! k_3!} \left(\frac{1}{3}\right)^{k_1} \left(\frac{1}{3}\right)^{k_2} \left(\frac{1}{3}\right)^{k_3}$$

**4. Explain the interpretation of the parameters.**
* **Interpretation:** * $n = 5$: The total number of independent trials (die rolls).
  * $p_1, p_2, p_3$: The underlying probabilities of each category occurring on any single trial (each is $\frac{1}{3}$).
  * $k_1, k_2, k_3$: The specific number of times each respective category occurs during the 5 trials.