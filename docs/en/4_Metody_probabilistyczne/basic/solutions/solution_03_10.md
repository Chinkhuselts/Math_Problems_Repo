## Task 10 — Multinomial Model

A box contains candies with the following probability distribution for each independent draw: 
* Strawberry ($p_1$) = 0.40
* Lemon ($p_2$) = 0.35
* Mint ($p_3$) = 0.25

We randomly select $n = 6$ candies independently. Let $X_1, X_2,$ and $X_3$ represent the number of strawberry, lemon, and mint candies obtained, respectively. This follows a Multinomial distribution.

**Calculate the probability that we obtain exactly 3 strawberry, 2 lemon, and 1 mint:**
* **Formula:** $P(X_1 = k_1, X_2 = k_2, X_3 = k_3) = \frac{n!}{k_1! k_2! k_3!} (p_1)^{k_1} (p_2)^{k_2} (p_3)^{k_3}$
* **Calculation:** $$P(X_1 = 3, X_2 = 2, X_3 = 1) = \frac{6!}{3! 2! 1!} (0.40)^3 (0.35)^2 (0.25)^1$$
  
  First, calculate the factorial coefficient:
  $$\frac{720}{6 \times 2 \times 1} = \frac{720}{12} = 60$$
  
  Next, calculate the probability products:
  $$(0.40)^3 = 0.064$$
  $$(0.35)^2 = 0.1225$$
  $$(0.25)^1 = 0.25$$
  
  Multiply everything together:
  $$P(3, 2, 1) = 60 \times 0.064 \times 0.1225 \times 0.25 = 0.1176$$
  *(There is an 11.76% chance of drawing exactly this combination of candies).*