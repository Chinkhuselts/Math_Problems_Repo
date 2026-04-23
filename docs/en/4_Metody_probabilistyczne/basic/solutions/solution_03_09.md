## Task 9 — Poisson Model

A customer service center receives an average of $\lambda = 5$ requests per hour. Let $X$ be the random variable representing the number of requests received in a one-hour interval. $X$ follows a Poisson distribution: $X \sim \text{Poisson}(5)$.

**1. Calculate the probability that during one hour there will be exactly 3 requests:**
* **Formula:** $P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$
* **Calculation:** $$P(X = 3) = \frac{5^3 e^{-5}}{3!}$$
  $$P(X = 3) = \frac{125 \times e^{-5}}{3 \times 2 \times 1} = \frac{125 \times 0.006738}{6}$$
  $$P(X = 3) \approx \frac{0.84225}{6} \approx 0.1404$$
  *(There is an approximately 14.04% chance of receiving exactly 3 requests in an hour).*

**2. Calculate the probability of receiving at least one request:**
* **Formula:** "At least one" is best calculated using the complementary event (1 minus the probability of receiving exactly zero requests).
  $$P(X \ge 1) = 1 - P(X = 0)$$
* **Calculation:** First, find $P(X = 0)$:
  $$P(X = 0) = \frac{5^0 e^{-5}}{0!} = \frac{1 \times e^{-5}}{1} \approx 0.0067$$
  
  Now subtract from 1:
  $$P(X \ge 1) = 1 - 0.0067 = 0.9933$$
  *(There is a 99.33% chance of receiving at least one request during the hour).*