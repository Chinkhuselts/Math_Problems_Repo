# Solutions: Task List 1 — Events and Probability

## Task 1 — Coin Tossing

1. **Sample space $\Omega_1$ (one toss):** $\Omega_1 = \{H, T\}$
2. **Sample space $\Omega_2$ (two tosses):** $\Omega_2 = \{(H,H), (H,T), (T,H), (T,T)\}$
3. **Sample space $\Omega_3$ (three tosses):** $\Omega_3 = \{(H,H,H), (H,H,T), (H,T,H), (H,T,T), (T,H,H), (T,H,T), (T,T,H), (T,T,T)\}$
4. **Number of elementary outcomes:**
   * $\Omega_1$: $2^1 = 2$
   * $\Omega_2$: $2^2 = 4$
   * $\Omega_3$: $2^3 = 8$
5. **Elementary outcome representation:** An elementary outcome represents a specific, ordered sequence of results from the coin tosses (e.g., Head on the first toss, Tail on the second, Head on the third).

---

## Task 2 — Rolling a Die

1. **Sample space $\Omega_1$ (one roll):** $\Omega_1 = \{1, 2, 3, 4, 5, 6\}$
2. **Sample space $\Omega_2$ (two rolls):** $\Omega_2 = \{(i, j) \mid i, j \in \{1, 2, 3, 4, 5, 6\}\}$
3. **Sample space $\Omega_3$ (three rolls):** $\Omega_3 = \{(i, j, k) \mid i, j, k \in \{1, 2, 3, 4, 5, 6\}\}$
4. **Number of elementary outcomes:**
   * $\Omega_1$: $6^1 = 6$
   * $\Omega_2$: $6^2 = 36$
   * $\Omega_3$: $6^3 = 216$
5. **Elementary outcome representation:** It represents an exact sequence of numbers rolled on the die in chronological order.

---

## Task 3 — Drawing Cards

Let the deck be denoted as a set $D$ containing 52 unique cards.

1. **Sample space $\Omega_1$ (one card):** $\Omega_1 = \{c \mid c \in D\}$
2. **Sample space $\Omega_2$ (two draws, with replacement):** $\Omega_2 = \{(c_1, c_2) \mid c_1 \in D, c_2 \in D\}$
3. **Sample space $\Omega_2'$ (two draws, without replacement):** $\Omega_2' = \{(c_1, c_2) \mid c_1 \in D, c_2 \in D, c_1 \neq c_2\}$
4. **Number of elementary outcomes:**
   * $\Omega_1$: $52$
   * $\Omega_2$: $52 \times 52 = 2704$
   * $\Omega_2'$: $52 \times 51 = 2652$
5. **Elementary outcome representation:** An ordered pair representing the exact cards drawn, in the order they were drawn.

---

## Task 4 — Weekly Weather Observation

1. **Sample space $\Omega_1$ (one day):** $\Omega_1 = \{S, C, R\}$
2. **Sample space $\Omega_2$ (two days):** $\Omega_2 = \{(w_1, w_2) \mid w_1, w_2 \in \{S, C, R\}\}$
3. **Sample space $\Omega_7$ (seven days):** $\Omega_7 = \{(w_1, w_2, \dots, w_7) \mid w_i \in \{S, C, R\} \text{ for } i=1 \dots 7\}$
4. **Number of elementary outcomes:**
   * $\Omega_1$: $3^1 = 3$
   * $\Omega_2$: $3^2 = 9$
   * $\Omega_7$: $3^7 = 2187$
5. **Elementary outcome representation:** The exact sequence of weather states over the 7 days of the week.

---

## Task 5 — Buffon's Needle Experiment

1. **Sample space $\Omega$:** The set of all possible resting positions of the needle on the ruled floor.
2. **Parameters:**
   * The perpendicular distance from the center of the needle to the nearest line.
   * The acute angle formed between the needle and the parallel lines.
3. **Variables:**
   * Distance $X \in [0, \frac{d}{2}]$
   * Angle $\theta \in [0, \frac{\pi}{2}]$
4. **Sample space as a set:** $\Omega = \{(X, \theta) \mid 0 \le X \le \frac{d}{2}, 0 \le \theta \le \frac{\pi}{2}\}$
5. **Why it is continuous:** Unlike dice or coins which have discrete, countable outcomes, the needle's position and angle can take any real number value within their respective intervals.

---

## Task 6 — Events and Probabilities in Coin Tossing

*(Probabilities assigned to elementary outcomes: $\Omega_1 = \frac{1}{2}$, $\Omega_2 = \frac{1}{4}$, $\Omega_3 = \frac{1}{8}$)*

### One Coin Toss
* $P(A_1) = P(\{H\}) = \frac{1}{2}$
* $P(B_1) = P(\{T\}) = \frac{1}{2}$
* $P(C_1) = P(\{H\}) = \frac{1}{2}$

### Two Coin Tosses
* $P(A_2) = P(\{(H,T), (T,H)\}) = \frac{2}{4} = \frac{1}{2}$
* $P(B_2) = 1 - P(\{(T,T)\}) = 1 - \frac{1}{4} = \frac{3}{4}$
* $P(C_2) = P(\{(H,H), (T,T)\}) = \frac{2}{4} = \frac{1}{2}$

### Three Coin Tosses
* $P(A_3) = P(\{(H,H,T), (H,T,H), (T,H,H)\}) = \frac{3}{8}$
* $P(B_3) = 1 - P(\{(H,H,H)\}) = 1 - \frac{1}{8} = \frac{7}{8}$
* $P(C_3) = P(\{(H,H,H), (T,T,T)\}) = \frac{2}{8} = \frac{1}{4}$

### Additional Event on $\Omega_3$
* **Event $D_3$:** The first toss is tails. 
* $D_3 = \{(T,H,H), (T,H,T), (T,T,H), (T,T,T)\}$
* $P(D_3) = \frac{4}{8} = \frac{1}{2}$

---

## Task 7 — Events and Probabilities in Die Rolling

*(Probabilities assigned: $\Omega_1 = \frac{1}{6}$, $\Omega_2 = \frac{1}{36}$, $\Omega_3 = \frac{1}{216}$)*

### One Die Roll
* $P(A_1) = P(\{2, 4, 6\}) = \frac{3}{6} = \frac{1}{2}$
* $P(B_1) = P(\{5, 6\}) = \frac{2}{6} = \frac{1}{3}$
* $P(C_1) = P(\{1, 2, 3\}) = \frac{3}{6} = \frac{1}{2}$

### Two Die Rolls
* $P(A_2) = P(\{(1,6), (2,5), (3,4), (4,3), (5,2), (6,1)\}) = \frac{6}{36} = \frac{1}{6}$
* $P(B_2) = P(\{(i,i) \mid i \in \{1\dots6\}\}) = \frac{6}{36} = \frac{1}{6}$
* $P(C_2) = P(\{(4,6), (5,5), (6,4), (5,6), (6,5), (6,6)\}) = \frac{6}{36} = \frac{1}{6}$

### Three Die Rolls
* **$A_3$ (Sum is 10):** 27 combinations sum to 10. $P(A_3) = \frac{27}{216} = \frac{1}{8}$
* **$B_3$ (Exactly two same):** Choose duplicated number (6), single number (5), and arrangement (3). $6 \times 5 \times 3 = 90$. $P(B_3) = \frac{90}{216} = \frac{5}{12}$
* **$C_3$ (Two 2s and one 3):** Permutations are $(2,2,3), (2,3,2), (3,2,2)$. $P(C_3) = \frac{3}{216} = \frac{1}{72}$

### Additional Event on $\Omega_3$
* **Event $D_3$:** All three rolls are odd.
* $P(D_3) = \frac{3 \times 3 \times 3}{216} = \frac{27}{216} = \frac{1}{8}$

---

## Task 8 — Events and Probabilities in Card Drawing

### One Card Drawn
* $P(A_1) = \frac{13}{52} = \frac{1}{4}$
* $P(B_1) = \frac{4}{52} = \frac{1}{13}$
* $P(C_1) = \frac{40}{52} = \frac{10}{13}$

### Two Cards Drawn (with replacement)
* $P(A_2) = \frac{13}{52} \times \frac{13}{52} = \frac{1}{16}$
* $P(B_2) = 1 \times \frac{3}{52} = \frac{1}{13}$
* $P(C_2) = 1 - P(\text{No Ace}) = 1 - (\frac{48}{52})^2 = 1 - \frac{144}{169} = \frac{25}{169}$

### Two Cards Drawn (without replacement)
* $P(A_3) = \frac{13}{52} \times \frac{12}{51} = \frac{1}{17}$
* $P(B_3) = 1 \times \frac{3}{51} = \frac{1}{17}$
* $P(C_3) = (\text{King then Queen}) \text{ OR } (\text{Queen then King}) = (\frac{4}{52} \times \frac{4}{51}) + (\frac{4}{52} \times \frac{4}{51}) = \frac{32}{2652} = \frac{8}{663}$

### Additional Event on $\Omega_2'$
* **Event $D_2'$:** Both cards are black. 
* $P(D_2') = \frac{26}{52} \times \frac{25}{51} = \frac{25}{102}$

---

## Task 9 — Events and Probabilities in Weekly Weather

*(Independent events, $P(S) = P(C) = P(R) = \frac{1}{3}$. Total elements: $3^7 = 2187$)*

* $P(A) = P(\text{Sat}=S) \times P(\text{Sun}=S) = \frac{1}{3} \times \frac{1}{3} = \frac{1}{9}$
* $P(B) = P(\text{Wed}=R) \times P(\text{Thu}=R) \times P(\text{Fri}=R) = (\frac{1}{3})^3 = \frac{1}{27}$
* $P(C) = 1 - P(\text{No sunny days}) = 1 - (\frac{2}{3})^7 = 1 - \frac{128}{2187} = \frac{2059}{2187}$
* $P(D) = P(\text{All 7 days are S or C}) = (\frac{2}{3})^7 = \frac{128}{2187}$
* $P(E) = \binom{7}{2} \times (\frac{1}{3})^2 \times (\frac{2}{3})^5 = 21 \times \frac{1}{9} \times \frac{32}{243} = \frac{224}{729}$

### Additional Event on $\Omega_7$
* **Event $F$:** All 7 days have the exact same weather. 
* $P(F) = P(\text{All S}) + P(\text{All C}) + P(\text{All R}) = 3 \times (\frac{1}{3})^7 = \frac{1}{729}$

---

## Task 10 — Buffon's Needle Experiment Probabilities

*(Area of sample space $\Omega = \frac{d}{2} \times \frac{\pi}{2} = \frac{\pi d}{4}$. Intersects if $X \le \frac{L}{2} \sin\theta$)*

* **$P(A)$:** $\text{Area} = \int_{0}^{\pi/2} \frac{L}{2} \sin\theta \, d\theta = \frac{L}{2}$. Then, $P(A) = \frac{L/2}{\pi d / 4} = \frac{2L}{\pi d}$
* **$P(B)$:** $1 - P(A) = 1 - \frac{2L}{\pi d}$
* **$P(C)$:** $\frac{\pi/6}{\pi/2} = \frac{1}{3}$
* **$P(D)$:** $\frac{d/4}{d/2} = \frac{1}{2}$
* **$P(E)$:** $\text{Area} = \int_{\pi/4}^{\pi/2} \frac{L}{2} \sin\theta \, d\theta = \frac{L\sqrt{2}}{4}$. Then, $P(E) = \frac{L\sqrt{2}/4}{\pi d / 4} = \frac{L\sqrt{2}}{\pi d}$

### Additional Event
* **Event $F$:** The needle is perfectly parallel to the lines ($\theta = 0$).
* $P(F) = 0$ (The probability of a single specific value in a continuous distribution is zero).
