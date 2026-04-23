## Task 4 — Poisson Model (Arrival of Events)

**1. Describe the random experiment.**
* **Description:** The experiment consists of observing the number of discrete events (error reports) occurring within a continuous, fixed interval of time (one hour). We assume the events occur independently of one another, two events cannot happen at the exact same mathematical instant, and the average rate of occurrence remains constant.

**2. Determine the sample space $\Omega$.**
* **Sample Space:** Let the random variable $X$ be the total number of error reports received in the one-hour interval. The system could receive 0 reports, 1 report, 2 reports, and so on, with no strictly defined upper limit. 
  $$\Omega = \{0, 1, 2, 3, \dots\}$$

**3. Provide the formula of the probability distribution.**
* **Distribution:** This follows a Poisson distribution. Let $k$ be the exact number of reports received. Using the standard formula $P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$, and substituting our specific average rate of 3, the probability of receiving exactly $k$ reports is:
  $$P(X = k) = \frac{3^k e^{-3}}{k!}$$
  *(for $k = 0, 1, 2, 3, \dots$)*

**4. Interpret the parameter $\lambda$.**
* **Interpretation:** The parameter $\lambda$ (lambda) represents the **expected value** or the **average rate of occurrences** within the defined interval. In this specific model, $\lambda = 3$, meaning we expect to receive an average of exactly 3 error reports per hour.