# Solution: List 4 — Problem 5 (From Frequencies to Probability)

## Conceptual Introduction: Bridging the Empirical and Theoretical
This problem is arguably the most important in the list because it demonstrates the birth of probability theory. We transition from tracking physical, messy reality (rolling a die 1000 times) to defining pristine mathematical rules. 
*   **Empirical World:** We deal with counts ($n$) and observed frequencies ($f = n/N$). These are real data points derived from physical action.
*   **Theoretical World:** We abstract these observations into a pure mathematical function ($P$, Probability). 

By manipulating observed frequencies, we organically discover the rules that *any* theoretical model of probability must obey to remain faithful to physical reality.

---

## Part A — From elementary outcomes to events

We are given total throws $N = 1000$ and individual counts:
*   $n(\{1\})=168, n(\{2\})=154, n(\{3\})=181$
*   $n(\{4\})=167, n(\{5\})=160, n(\{6\})=170$

The formula for observed frequency is $f(A) = \frac{n(A)}{1000}$.

### 1. Event A: Even numbers $\{2, 4, 6\}$
*   **Count:** $n(A) = n(\{2\}) + n(\{4\}) + n(\{6\}) = 154 + 167 + 170 = 491$
*   **Frequency:** $f(A) = \frac{491}{1000} = 0.491$

### 2. Event B: $\{1, 2, 3\}$
*   **Count:** $n(B) = n(\{1\}) + n(\{2\}) + n(\{3\}) = 168 + 154 + 181 = 503$
*   **Frequency:** $f(B) = \frac{503}{1000} = 0.503$

### 3. Event C: $\{5, 6\}$
*   **Count:** $n(C) = n(\{5\}) + n(\{6\}) = 160 + 170 = 330$
*   **Frequency:** $f(C) = \frac{330}{1000} = 0.330$

### 4. Event D: Odd numbers $\{1, 3, 5\}$
*   **Count:** $n(D) = n(\{1\}) + n(\{3\}) + n(\{5\}) = 168 + 181 + 160 = 509$
*   **Frequency:** $f(D) = \frac{509}{1000} = 0.509$

### 5. Event E: $\{1, 2, 3, 4\}$
*   **Count:** $n(E) = 168 + 154 + 181 + 167 = 670$
*   **Frequency:** $f(E) = \frac{670}{1000} = 0.670$

---

## Part B — How frequencies combine

Here we verify the foundational property of additivity.

### 1. Verify $f(\{2,4,6\}) = f(\{2\}) + f(\{4\}) + f(\{6\})$
*   **Check:** $0.491 = 0.154 + 0.167 + 0.170$. The equality holds.
*   **Explanation:** The elementary outcomes are mutually exclusive (a die cannot land on 2 and 4 simultaneously). Therefore, to count how many times "an even number" occurred, we simply sum the occurrences of 2, 4, and 6. Because frequency is just count divided by a constant ($N=1000$), the addition holds true for frequencies as well.

### 2. Verify $f(\{1,2,3,4\}) = f(\{1,2\}) + f(\{3,4\})$
*   **Check:** $f(\{1,2\}) = 0.322$. $f(\{3,4\}) = 0.348$. $0.322 + 0.348 = 0.670$. This matches $f(\{1,2,3,4\})$ calculated in Part A.
*   **Explanation:** The sets $\{1,2\}$ and $\{3,4\}$ are disjoint ($A \cap B = \emptyset$). There is no overlap, so summing their individual frequencies gives the exact frequency of their union.

### 3. Verify $f(\{1,3,5\}) + f(\{2,4,6\}) = 1$
*   **Check:** $0.509 + 0.491 = 1.000$. The equality holds.
*   **Explanation:** These two sets represent the Odd numbers and Even numbers. They form a complete *partition* of the sample space $\Omega$. Since every roll must be either odd or even, the sum of their counts is exactly 1000. Thus, their total frequency is $1000/1000 = 1$.

### 4. Verify $f(\{5,6\}) = 1 - f(\{1,2,3,4\})$
*   **Check:** $0.330 = 1 - 0.670$. The equality holds.
*   **Explanation:** This is the empirical basis for the Complement Rule. The set $\{5,6\}$ is the complement of $\{1,2,3,4\}$. The sum of their frequencies must be 1 (as established in point 3), so algebraically, $f(A^c) = 1 - f(A)$.

---

## Part C — When simple addition works and when it fails

### 1. Disjoint events: $f(\{1,2\} \cup \{5,6\}) = f(\{1,2\}) + f(\{5,6\})$
*   **Check:** The union is $\{1,2,5,6\}$. $f(\{1,2,5,6\}) = \frac{168+154+160+170}{1000} = 0.652$. The sum is $0.322 + 0.330 = 0.652$. Equality holds because the sets are disjoint.

### 2 & 3 & 4. Overlapping events: $M=\{1,2,3\}, N=\{3,4,5\}$
*   **Calculate:** 
    *   $f(M) = 0.503$
    *   $f(N) = \frac{181+167+160}{1000} = 0.508$
    *   $M \cup N = \{1,2,3,4,5\}$. $f(M \cup N) = \frac{1000-170}{1000} = 0.830$
    *   Sum: $f(M) + f(N) = 0.503 + 0.508 = 1.011$
*   **Explanation of Failure:** $f(M \cup N) \neq f(M) + f(N)$. The simple addition overshoots the true frequency (it even goes above 100%!). This fails because the events $M$ and $N$ are not mutually exclusive.
*   **The Double-Count:** The elementary outcome **`{3}`** exists in both set $M$ and set $N$. In the physical count, the 181 times the die landed on '3' were counted in $f(M)$ and then counted *again* in $f(N)$. 

---

## Part D — Covering the whole sample space

### 1 & 2. Sum of all elementary frequencies
*   **Calculation:** $0.168 + 0.154 + 0.181 + 0.167 + 0.160 + 0.170 = 1.000$
*   **Explanation:** Every single trial produced exactly one outcome from the sample space. Therefore, the sum of all individual occurrences equals the total number of trials $N$. The sum of the fractions is $N/N = 1$.

### 3 & 4. Splitting into disjoint triplets
*   **Sets:** $\{1,2\}, \{3,4\}, \{5,6\}$
*   **Calculation:** $0.322 + 0.348 + 0.330 = 1.000$
*   **Explanation:** Just as with individual outcomes, these three sets are mutually disjoint and their union is $\Omega$. No roll is counted twice, and no roll is missed.

### 5. General Statement
For any sample space $\Omega$ partitioned into mutually exclusive and exhaustive events $A_1, A_2, \dots, A_k$ (meaning $A_i \cap A_j = \emptyset$ and $\bigcup A_i = \Omega$), the sum of their observed frequencies is exactly 1. 

$$\sum_{i=1}^{k} f(A_i) = 1$$

---

## Part E — From observed frequency to probability

If we invent a theoretical function $P(A)$ to predict how likely events are (rather than measuring how often they *did* happen), it must follow the arithmetic laws we just observed:

1.  **Numbers between 0 and 1:** Empirical counts cannot be less than 0, nor can they be greater than the total number of trials $N$. Thus $0 \leq n(A) \leq N$. Dividing by $N$ mandates that $0 \leq P(A) \leq 1$.
2.  **Assigns 0 to the impossible event:** If a set is empty ($\emptyset$), its count across any number of trials is perpetually zero. $P(\emptyset) = 0$.
3.  **Assigns 1 to the whole sample space:** The event $\Omega$ encompasses every possible outcome. Therefore, it happens on every trial. $n(\Omega) = N$, leading to $P(\Omega) = 1$.
4.  **Disjoint additivity:** As seen in Part C, adding probabilities of disjoint sets works flawlessly because there is no double-counting. $P(A \cup B) = P(A) + P(B)$ if $A \cap B = \emptyset$.
5.  **Complementary events:** Because an event $A$ and its complement $A^c$ are disjoint and perfectly form $\Omega$, their probabilities must sum to $P(\Omega) = 1$.

---

## Part F — Conclusion: The Three Levels of Abstraction

1.  **Elementary outcomes and events (The Logical Level):** This is pure set theory. We define the universe $\Omega$ and identify subsets. No numbers or probabilities exist here yet, only boolean logic (AND, OR, NOT translated to $\cap, \cup, ^c$).
2.  **Observed frequencies (The Empirical Level):** This is the physical world. We perform experiments, tally results, and calculate fractions. The numbers here are "messy" and change slightly every time we run the 1000 trials.
3.  **Probability (The Mathematical Abstraction):** This is the theoretical bridge. We observe the unbreakable arithmetic rules governing the messy empirical frequencies (boundedness, additivity to 1) and define a pristine mathematical function $P$ that acts exactly the same way, but without needing physical dice. It is a formalized model of reality.