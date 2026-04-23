## Task 1 — Binomial Model (Quality Control)

**1. Describe the random experiment.**
* **Description:** The experiment consists of inspecting 3 consecutive screws independently to determine their quality state. Since there are only two possible outcomes for each screw (good or defective) and the probability remains constant, this is a sequence of 3 independent Bernoulli trials.

**2. Determine the sample space $\Omega$.**
* **Sample Space:** Let $G$ represent a good screw and $D$ represent a defective screw. The sample space consists of all possible ordered sequences of length 3:
  $$\Omega = \{(G,G,G), (G,G,D), (G,D,G), (D,G,G), (G,D,D), (D,G,D), (D,D,G), (D,D,D)\}$$

**3. Specify the probabilities of the elements of the sample space.**
* **Probabilities:** Let the probability of finding a defective screw be $P(D) = p$, and the probability of a good screw be $P(G) = 1 - p$. Assuming independence, we multiply the probabilities of individual outcomes:
  * $P(G,G,G) = (1-p)^3$
  * $P(G,G,D) = P(G,D,G) = P(D,G,G) = p(1-p)^2$
  * $P(G,D,D) = P(D,G,D) = P(D,D,G) = p^2(1-p)$
  * $P(D,D,D) = p^3$

**4. Define what is considered a "success" in this model.**
* **Definition:** In probability models, "success" is simply the event we are choosing to count, regardless of whether it is a positive or negative thing in real life. If we are tracking the number of defective parts for quality control, finding a **defective screw** is considered a "success" (with probability $p$).