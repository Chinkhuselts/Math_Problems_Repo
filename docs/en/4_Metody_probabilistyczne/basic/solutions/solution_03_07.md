## Task 7 — Hypergeometric Model

A box contains $N = 15$ total light bulbs (12 working + 3 defective). We draw a sample of $n = 5$ bulbs without replacement. Let $X$ be the random variable representing the number of defective bulbs in the sample. $X$ follows a Hypergeometric distribution.

**Calculate the probability that the sample contains exactly 2 defective bulbs:**
* **Formula:** $P(X = k) = \frac{\binom{K}{k} \binom{N-K}{n-k}}{\binom{N}{n}}$
  *(where $K$ is the total number of defective bulbs available, and $N-K$ is the total number of working bulbs).*
* **Calculation:** $$P(X = 2) = \frac{\binom{3}{2} \binom{12}{3}}{\binom{15}{5}}$$
  
  First, calculate the individual combinations:
  * $\binom{3}{2} = \frac{3!}{2!(3-2)!} = 3$
  * $\binom{12}{3} = \frac{12 \times 11 \times 10}{3 \times 2 \times 1} = 220$
  * $\binom{15}{5} = \frac{15 \times 14 \times 13 \times 12 \times 11}{5 \times 4 \times 3 \times 2 \times 1} = 3003$

  Now plug the values back into the probability fraction:
  $$P(X = 2) = \frac{3 \times 220}{3003} = \frac{660}{3003} \approx 0.2198$$
  *(There is an approximately 21.98% chance that the sample contains exactly 2 defective bulbs).*