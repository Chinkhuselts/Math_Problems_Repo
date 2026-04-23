## Task 6 — Binomial Model

An inspector checks $n = 10$ parts. The probability of a part being defective is $p = 0.04$. Therefore, the probability of a part being functional is $1 - p = 0.96$. Let $X$ be the random variable representing the number of defective parts found. $X$ follows a Binomial distribution: $X \sim B(10, 0.04)$.

**1. Calculate the probability that exactly 2 parts are defective:**
* **Formula:** $P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$
* **Calculation:** $$P(X = 2) = \binom{10}{2} (0.04)^2 (0.96)^8$$
  $$P(X = 2) = 45 \times 0.0016 \times (0.96)^8$$
  $$P(X = 2) \approx 0.072 \times 0.7214 \approx 0.0519$$
  *(There is an approximately 5.19% chance that exactly 2 parts are defective).*

**2. Calculate the probability that at least one part is defective:**
* **Formula:** It is much easier to use the complementary event. "At least one" is the opposite of "exactly zero".
  $$P(X \ge 1) = 1 - P(X = 0)$$
* **Calculation:**
  $$P(X = 0) = \binom{10}{0} (0.04)^0 (0.96)^{10} = 1 \times 1 \times (0.96)^{10} \approx 0.6648$$
  $$P(X \ge 1) = 1 - 0.6648 = 0.3352$$
  *(There is an approximately 33.52% chance of finding at least one defective part).*