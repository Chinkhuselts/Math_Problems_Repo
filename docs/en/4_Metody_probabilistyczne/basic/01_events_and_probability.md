# Solutions: Task List 1 — Events and Probability

## Task 1 — Coin Tossing

1. **Sample space Omega_1 (one toss):** Omega_1 = {H, T}
2. **Sample space Omega_2 (two tosses):**
   Omega_2 = {(H,H), (H,T), (T,H), (T,T)}
3. **Sample space Omega_3 (three tosses):**
   Omega_3 = {(H,H,H), (H,H,T), (H,T,H), (H,T,T), (T,H,H), (T,H,T), (T,T,H), (T,T,T)}
4. **Number of elementary outcomes:**
   * Omega_1: 2^1 = 2
   * Omega_2: 2^2 = 4
   * Omega_3: 2^3 = 8
5. **Elementary outcome representation:**
   An elementary outcome represents a specific, ordered sequence of results from the coin tosses (e.g., Head on the first toss, Tail on the second, Head on the third).

---

## Task 2 — Rolling a Die

1. **Sample space Omega_1 (one roll):**
   Omega_1 = {1, 2, 3, 4, 5, 6}
2. **Sample space Omega_2 (two rolls):**
   Omega_2 = {(i, j) | i, j in {1, 2, 3, 4, 5, 6}}
3. **Sample space Omega_3 (three rolls):**
   Omega_3 = {(i, j, k) | i, j, k in {1, 2, 3, 4, 5, 6}}
4. **Number of elementary outcomes:**
   * Omega_1: 6^1 = 6
   * Omega_2: 6^2 = 36
   * Omega_3: 6^3 = 216
5. **Elementary outcome representation:**
   It represents an exact sequence of numbers rolled on the die in chronological order.

---

## Task 3 — Drawing Cards

Let the deck be denoted as a set D containing 52 unique cards.
1. **Sample space Omega_1 (one card):**
   Omega_1 = {c | c in D}
2. **Sample space Omega_2 (two draws, with replacement):**
   Omega_2 = {(c_1, c_2) | c_1 in D, c_2 in D}
3. **Sample space Omega_2' (two draws, without replacement):**
   Omega_2' = {(c_1, c_2) | c_1 in D, c_2 in D, c_1 != c_2}
4. **Number of elementary outcomes:**
   * Omega_1: 52
   * Omega_2: 52 * 52 = 2704
   * Omega_2': 52 * 51 = 2652
5. **Elementary outcome representation:**
   An ordered pair (or single value) representing the exact cards drawn, in the order they were drawn.

---

## Task 4 — Weekly Weather Observation

1. **Sample space Omega_1 (one day):**
   Omega_1 = {S, C, R}
2. **Sample space Omega_2 (two days):**
   Omega_2 = {(w_1, w_2) | w_1, w_2 in {S, C, R}}
3. **Sample space Omega_7 (seven days):**
   Omega_7 = {(w_1, w_2, ..., w_7) | w_i in {S, C, R} for i=1...7}
4. **Number of elementary outcomes:**
   * Omega_1: 3^1 = 3
   * Omega_2: 3^2 = 9
   * Omega_7: 3^7 = 2187
5. **Elementary outcome representation:**
   The exact sequence of weather states over the 7 days of the week (e.g., S-C-R-R-S-C-S).

---

## Task 5 — Buffon's Needle Experiment

1. **Sample space Omega:** The set of all possible resting positions of the needle on the ruled floor.
2. **Parameters:** * The perpendicular distance from the center of the needle to the nearest line.
   * The acute angle formed between the needle and the parallel lines.
3. **Variables:**
   * Distance X in [0, d/2]
   * Angle theta in [0, pi/2]
4. **Sample space as a set:**
   Omega = {(X, theta) | 0 <= X <= d/2, 0 <= theta <= pi/2}
5. **Why it is continuous:**
   Unlike dice or coins which have discrete, countable outcomes, the needle's position and angle can take any real number value within their respective intervals. 

---

## Task 6 — Events and Probabilities in Coin Tossing

(Probabilities assigned to elementary outcomes: Omega_1 = 1/2, Omega_2 = 1/4, Omega_3 = 1/8)

**One Coin Toss:**
* P(A_1) = P({H}) = 1/2
* P(B_1) = P({T}) = 1/2
* P(C_1) = P({H}) = 1/2

**Two Coin Tosses:**
* P(A_2) = P({(H,T), (T,H)}) = 2/4 = 1/2
* P(B_2) = 1 - P({(T,T)}) = 1 - 1/4 = 3/4
* P(C_2) = P({(H,H), (T,T)}) = 2/4 = 1/2

**Three Coin Tosses:**
* P(A_3) = P({(H,H,T), (H,T,H), (T,H,H)}) = 3/8
* P(B_3) = 1 - P({(H,H,H)}) = 1 - 1/8 = 7/8
* P(C_3) = P({(H,H,H), (T,T,T)}) = 2/8 = 1/4

**Additional Event on Omega_3:**
* D_3 — The first toss is tails. 
* D_3 = {(T,H,H), (T,H,T), (T,T,H), (T,T,T)}
* P(D_3) = 4/8 = 1/2

---

## Task 7 — Events and Probabilities in Die Rolling

(Probabilities assigned: Omega_1 = 1/6, Omega_2 = 1/36, Omega_3 = 1/216)

**One Die Roll:**
* P(A_1) = P({2, 4, 6}) = 3/6 = 1/2
* P(B_1) = P({5, 6}) = 2/6 = 1/3
* P(C_1) = P({1, 2, 3}) = 3/6 = 1/2

**Two Die Rolls:**
* P(A_2) = P({(1,6), (2,5), (3,4), (4,3), (5,2), (6,1)}) = 6/36 = 1/6
* P(B_2) = P({(i,i) | i in {1...6}}) = 6/36 = 1/6
* P(C_2) = P({(4,6), (5,5), (6,4), (5,6), (6,5), (6,6)}) = 6/36 = 1/6

**Three Die Rolls:**
* A_3 (Sum is 10): 27 combinations sum to 10. P(A_3) = 27/216 = 1/8
* B_3 (Exactly two same): Choose duplicated number (6), single number (5), and arrangement (3). 6 * 5 * 3 = 90. P(B_3) = 90/216 = 5/12
* C_3 (Two 2s and one 3): Permutations are (2,2,3), (2,3,2), (3,2,2). P(C_3) = 3/216 = 1/72

**Additional Event on Omega_3:**
* D_3 — All three rolls are odd.
* P(D_3) = (3 * 3 * 3) / 216 = 27/216 = 1/8

---

## Task 8 — Events and Probabilities in Card Drawing

**One Card Drawn:**
* P(A_1) = 13/52 = 1/4
* P(B_1) = 4/52 = 1/13
* P(C_1) = 40/52 = 10/13

**Two Cards Drawn (with replacement):**
* P(A_2) = (13/52) * (13/52) = 1/16
* P(B_2) = 1 * (3/52) = 1/13
* P(C_2) = 1 - P(No Ace) = 1 - (48/52)^2 = 1 - 144/169 = 25/169

**Two Cards Drawn (without replacement):**
* P(A_3) = (13/52) * (12/51) = 1/17
* P(B_3) = 1 * (3/51) = 1/17
* P(C_3) = (King then Queen) OR (Queen then King) = (4/52 * 4/51) + (4/52 * 4/51) = 32/2652 = 8/663

**Additional Event on Omega_2':**
* D_2' — Both cards are black. 
* P(D_2') = (26/52) * (25/51) = 25/102

---

## Task 9 — Events and Probabilities in Weekly Weather

(Independent events, P(S) = P(C) = P(R) = 1/3. Total elements: 3^7 = 2187)

* P(A) = P(Sat=S) * P(Sun=S) = (1/3) * (1/3) = 1/9
* P(B) = P(Wed=R) * P(Thu=R) * P(Fri=R) = (1/3)^3 = 1/27
* P(C) = 1 - P(No sunny days) = 1 - (2/3)^7 = 1 - 128/2187 = 2059/2187
* P(D) = P(All 7 days are S or C) = (2/3)^7 = 128/2187
* P(E) = (7 choose 2) * (1/3)^2 * (2/3)^5 = 21 * (1/9) * (32/243) = 224/729

**Additional Event on Omega_7:**
* F — All 7 days have the exact same weather. 
* P(F) = P(All S) + P(All C) + P(All R) = 3 * (1/3)^7 = 1/729

---

## Task 10 — Buffon's Needle Experiment Probabilities

(Area of sample space Omega = d/2 * pi/2 = pi*d/4. Intersects if X <= (L/2)*sin(theta))

* P(A): Area = Integral from 0 to pi/2 of (L/2)*sin(theta) d(theta) = L/2. 
  P(A) = (L/2) / (pi*d/4) = 2L / (pi*d)
* P(B) = 1 - P(A) = 1 - (2L) / (pi*d)
* P(C) = (pi/6) / (pi/2) = 1/3
* P(D) = (d/4) / (d/2) = 1/2
* P(E): Area = Integral from pi/4 to pi/2 of (L/2)*sin(theta) d(theta) = L*sqrt(2)/4. 
  P(E) = (L*sqrt(2)/4) / (pi*d/4) = L*sqrt(2) / (pi*d)

**Additional Event:**
* F — The needle is perfectly parallel to the lines (theta = 0).
* P(F) = 0 (Probability of a single specific value in a continuous distribution is zero).
