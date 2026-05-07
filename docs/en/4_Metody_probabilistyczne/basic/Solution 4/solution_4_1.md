# Solution: List 4 — Problem 1 (Coin × Coin)

## Conceptual Introduction & The Mathematical Space
Before diving into the specific questions, it is crucial to understand the formal structure we are working with. The experiment consists of tossing two coins. 
* We define the sample space of a single toss as $\Omega_1 = \{H, T\}$. 
* Because we toss two coins, our total sample space is the Cartesian product: $\Omega = \Omega_1 	imes \Omega_1 = \{(H,H), (H,T), (T,H), (T,T)\}$.
* Every subset of $\Omega$ is an "event". 

The 2x2 grid provided in the problem is a direct geometric representation of this Cartesian plane. The rows represent the first variable (the first toss), and the columns represent the second variable (the second toss). Marking a cell with an `X` is mathematically equivalent to including that ordered pair in our event set. This visual tool helps us translate natural language conditions into set theory and formal logic.

---

## Part A — Marking events

### 1. Exactly one head
**Graphical Representation:**
```text
      H   T
H     .   X
T     X   .
```
* **Reasoning:** We are looking for outcomes where the number of heads is strictly equal to 1. Looking at our universal set $\Omega$, $(H,H)$ has two heads, and $(T,T)$ has zero. The only outcomes that satisfy the condition are $(H,T)$ and $(T,H)$. On the grid, these correspond to the anti-diagonal.
* **Conceptual Example / Logical Link:** In formal logic, this statement corresponds to the **Exclusive OR (XOR)** operation: "The first coin is heads XOR the second coin is heads." It means one condition is true, but strictly not both.

### 2. Both tosses are the same
**Graphical Representation:**
```text
      H   T
H     X   .
T     .   X
```
* **Reasoning:** The formal condition here is an equality constraint between the two variables: $x_1 = x_2$. The pairs that satisfy this are $(H,H)$ and $(T,T)$. On the grid, this forms the main diagonal. 
* **Conceptual Example / Logical Link:** This represents an equivalence relation. Think of it like drawing the line $y = x$ on a standard Cartesian coordinate system; we are picking the points where the "x-coordinate" matches the "y-coordinate".

### 3. At least one head
**Graphical Representation:**
```text
      H   T
H     X   X
T     X   .
```
* **Reasoning:** "At least one" translates to $\geq 1$. The only outcome that fails this test is $(T,T)$, where there are zero heads. Therefore, the event set is $\{(H,H), (H,T), (T,H)\}$. 
* **Conceptual Example / Logical Link:** This is the standard **Logical OR (Inclusive OR)**: $A \cup B$. Let $A$ be "first toss is heads" (the entire first row) and $B$ be "second toss is heads" (the entire first column). The union of these two sets gives us the L-shaped block of three `X`s.

### 4. The first toss is tails
**Graphical Representation:**
```text
      H   T
H     .   .
T     X   X
```
* **Reasoning:** Here, the condition is placed *only* on the first toss (the row). We are given the constraint $x_1 = T$. Notice that there is absolutely no constraint placed on the second toss ($x_2$). Therefore, $x_2$ is "free" to be either $H$ or $T$. The resulting set is $\{(T,H), (T,T)\}$, which visually occupies the entire second row.
* **Conceptual Example / Logical Link:** This highlights the concept of a **marginal event**. When a dimension is unconstrained in a multidimensional space, the event extends across the entirety of that dimension. Formally, this is the Cartesian product $\{T\} 	imes \{H, T\}$.

### 5. The second toss is heads
**Graphical Representation:**
```text
      H   T
H     X   .
T     X   .
```
* **Reasoning:** Symmetrically to the previous problem, the constraint is now strictly on the second variable (the column): $x_2 = H$. The first toss is free to be anything. The outcomes are $\{(H,H), (T,H)\}$. This marks the entire first column.
* **Conceptual Example / Logical Link:** Just like the previous example, this is $\{H, T\} 	imes \{H\}$. Seeing these rows and columns independently is vital for understanding independent events later in probability theory.

---

## Part B — Interpretation

In this section, we practice the reverse operation: looking at a geometric subset of the sample space and finding the most concise natural language statement (logical proposition) that defines it.

### Case 1
```text
      H   T
H     X   X
T     .   .
```
* **Analysis of the Set:** The marked outcomes are $(H,H)$ and $(H,T)$. 
* **Reasoning:** Let's look for the invariant (what stays the same) and the variant (what changes). In both pairs, the first element is strictly $H$. The second element takes on all possible values ($H$ and $T$). Because the second coordinate spans the entire $\Omega_1$ space without restriction, the defining rule only applies to the first coordinate.
* **Interpretation:** The event is simply defined by the first outcome being heads. 
* **Final Statement:** **"The first toss is heads."**

### Case 2
```text
      H   T
H     .   X
T     X   .
```
* **Analysis of the Set:** The marked outcomes are $(H,T)$ and $(T,H)$.
* **Reasoning:** We check the relationship between the row and column for the marked cells. In neither case does the row value equal the column value. This is the exact complement (the logical NOT) of the main diagonal we saw in Part A.2 (where both tosses are the same). 
* **Interpretation:** Since $(H,T)$ and $(T,H)$ are the only two ways to get a mixed result, this subset represents the state where the coins show opposing faces.
* **Final Statement:** **"The two tosses yield different results,"** or equivalently, **"Exactly one head and exactly one tail."**