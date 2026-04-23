## Task 8 — Geometric Model

A programmer performs compilations until the first error occurs. The probability of an error (a "success" in this model) is $p = 0.1$. The probability of a successful, error-free compilation is $1 - p = 0.9$. Let $X$ be the number of the compilation on which the first error occurs. $X$ follows a Geometric distribution.

**1. Calculate the probability that the first error appears on the 4th compilation:**
* **Formula:** $P(X = k) = (1-p)^{k-1}p$
  *(This means exactly $k-1$ error-free compilations followed by 1 error).*
* **Calculation:** $$P(X = 4) = (0.9)^{4-1}(0.1)$$
  $$P(X = 4) = (0.9)^3(0.1)$$
  $$P(X = 4) = 0.729 \times 0.1 = 0.0729$$
  *(There is a 7.29% chance the first error happens exactly on the 4th try).*

**2. Calculate the probability that it appears no later than the 3rd compilation:**
* **Formula:** "No later than the 3rd" means the error happens on the 1st, 2nd, OR 3rd compilation. We must find $P(X \le 3) = P(X = 1) + P(X = 2) + P(X = 3)$.
* **Calculation:** * $P(X = 1) = (0.9)^0(0.1) = 0.1$
  * $P(X = 2) = (0.9)^1(0.1) = 0.09$
  * $P(X = 3) = (0.9)^2(0.1) = 0.81 \times 0.1 = 0.081$
  
  Now, add them together:
  $$P(X \le 3) = 0.1 + 0.09 + 0.081 = 0.271$$
  *(There is a 27.1% chance the first error appears within the first three attempts).*