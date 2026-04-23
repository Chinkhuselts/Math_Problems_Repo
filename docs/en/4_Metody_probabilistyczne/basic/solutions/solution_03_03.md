## Task 3 — Geometric Model (Waiting for the First Event)

**1. Describe the random experiment.**
* **Description:** The experiment involves examining printed pages one by one sequentially until a page with a printing error is found. Because each page's outcome is independent and the probability of an error remains constant, this is a sequence of independent Bernoulli trials that specifically stops after the first "success".

**2. Determine the sample space $\Omega$.**
* **Sample Space:** Let the random variable $X$ be the number of the page on which the first error is found. The error could appear on the very first page, the second, the third, and so on, theoretically out to infinity. Therefore, the sample space is the set of all positive integers:
  $$\Omega = \{1, 2, 3, \dots\}$$

**3. Provide the probability distribution.**
* **Distribution:** This follows a Geometric distribution. For the first error to occur exactly on the $k$-th page, the preceding $k-1$ pages must be perfectly printed (each with probability $1-p$), and the $k$-th page must have an error (with probability $p$). 
  $$P(X = k) = (1-p)^{k-1}p$$
  *(for $k = 1, 2, 3, \dots$)*

**4. Specify what is considered a success.**
* **Definition:** In the context of this geometric model, a "success" is finding a page with a **printing error**. The experiment immediately terminates as soon as this "success" is achieved.