## Task 2 — Hypergeometric Model (Sampling from a Batch)

**1. Describe the random experiment.**
* **Description:** The experiment consists of randomly drawing a sample of 4 components from a finite population of 20 components **without replacement**. Because the population is small and elements are not replaced, the result of each draw affects the probabilities of the subsequent draws (the trials are dependent).

**2. Define the sample space $\Omega$ as the number of defective elements in the sample.**
* **Sample Space:** Let the random variable $X$ represent the number of defective components in our drawn sample. Since we are drawing 4 components, and there are 5 defective ones available in total, we could draw anywhere from 0 to 4 defective components.
  $$\Omega = \{0, 1, 2, 3, 4\}$$

**3. Determine the possible values of the random variable.**
* **Values:** The random variable $X$ (number of defective components drawn) can take the exact values: 
  $$X \in \{0, 1, 2, 3, 4\}$$

**4. Provide the probability distribution.**
* **Distribution:** This follows a Hypergeometric distribution. We use the formula $P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}}$, where $N=20$ (total population), $K=5$ (total successes/defective available), and $n=4$ (sample size). The probability of drawing exactly $k$ defective components is:
  $$P(X = k) = \frac{\binom{5}{k} \binom{15}{4-k}}{\binom{20}{4}}$$
  *(for $k = 0, 1, 2, 3, 4$)*

**5. Explain what a "success" means in this model.**
* **Definition:** A "success" in this specific model means drawing a **defective component**. In probability, a success isn't necessarily a good thing; it is simply the specific characteristic or event that our random variable is counting.