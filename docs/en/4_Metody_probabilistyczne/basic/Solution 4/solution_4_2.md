# Solution: List 4 — Problem 2 (Die × Die)

## Conceptual Introduction & The Mathematical Space
We are now moving to a slightly more complex discrete probability space. The experiment is rolling two standard six-sided dice. 
* Let $\Omega_1 = \{1, 2, 3, 4, 5, 6\}$ be the sample space for the first die.
* The total sample space is the Cartesian product: $\Omega = \Omega_1 	imes \Omega_1$, which contains $6 	imes 6 = 36$ elementary outcomes.
* We represent this space as a 6x6 grid. The row index ($i$) represents the outcome of the first die, and the column index ($j$) represents the outcome of the second die. 

In this space, arithmetic and algebraic relations map directly to geometric shapes:
* **Equations** (like $i + j = k$ or $i = j$) form "lines" or "diagonals".
* **Inequalities** (like $i > j$) form bounded regions like triangles.
* **Logical operations** (AND, OR, XOR) correspond directly to set intersections, unions, and symmetric differences.

---

## Part A — Marking events

### 1. The sum is equal to 8
**Graphical Representation:**
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . X
3     . . . . X .
4     . . . X . .
5     . . X . . .
6     . X . . . .
```
* **Reasoning:** The algebraic constraint is $i + j = 8$. We find all pairs satisfying this: $(2,6), (3,5), (4,4), (5,3), (6,2)$. Because the sum is constant, as the row index increases by 1, the column index must decrease by 1. 
* **Conceptual Example / Logical Link:** In continuous geometry, $x + y = 8$ forms a straight line with a slope of $-1$. In our discrete grid, it forms an upward-sloping diagonal.

### 2. The first die is greater than the second
**Graphical Representation:**
```text
      1 2 3 4 5 6
1     . . . . . .
2     X . . . . .
3     X X . . . .
4     X X X . . .
5     X X X X . .
6     X X X X X .
```
* **Reasoning:** The condition is the strict inequality $i > j$. This means we mark cells where the row number is strictly larger than the column number. 
* **Conceptual Example / Logical Link:** An inequality $y < x$ divides a plane into two half-spaces. Here, the grid is divided into a "lower triangle" and an "upper triangle". Because the inequality is *strict* ($>$ rather than $\geq$), the boundary itself—the main diagonal where $i = j$—is completely excluded.

### 3. Both dice show even numbers
**Graphical Representation:**
```text
      1 2 3 4 5 6
1     . . . . . .
2     . X . X . X
3     . . . . . .
4     . X . X . X
5     . . . . . .
6     . X . X . X
```
* **Reasoning:** Let $A$ be the event "first die is even" (rows 2, 4, 6) and $B$ be "second die is even" (columns 2, 4, 6). The word "both" implies the logical AND operation, which maps to set intersection: $A \cap B$. We only mark cells where an even row crosses an even column.
* **Conceptual Example / Logical Link:** This shows how conditions placed independently on each dimension combine to create a sub-grid. It is the Cartesian product of the subset of evens with itself: $\{2, 4, 6\} 	imes \{2, 4, 6\}$.

### 4. At least one die shows 6
**Graphical Representation:**
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     X X X X X X
```
* **Reasoning:** Let $A$ be the event "first die is 6" (row 6) and $B$ be the event "second die is 6" (column 6). "At least one" is the logical OR operator, which means set union: $A \cup B$. We mark all cells in row 6 and all cells in column 6. The intersection cell $(6,6)$ is included because $(6=6) \lor (6=6)$ evaluates to True.
* **Conceptual Example / Logical Link:** This is a classic Inclusive OR. It forms a characteristic "cross" shape (or in this case, an L-shape hugging the edge). 

### 5. Exactly one die shows 1
**Graphical Representation:**
```text
      1 2 3 4 5 6
1     . X X X X X
2     X . . . . .
3     X . . . . .
4     X . . . . .
5     X . . . . .
6     X . . . . .
```
* **Reasoning:** We want the outcomes where either the first die is 1 OR the second die is 1, *but strictly not both*. We take the union of the 1st row and 1st column, and then we remove their intersection, which is the cell $(1,1)$.
* **Conceptual Example / Logical Link:** This represents the **Exclusive OR (XOR)** operation. In set theory, this is known as the **Symmetric Difference**, written as $A \oplus B$ or $A \Delta B$. Formulaically: $(A \cup B) \setminus (A \cap B)$.

---

## Part B — Interpretation

### Case 1
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . X X X X
4     . . X X X X
5     . . X X X X
6     . . X X X X
```
* **Analysis of the Set:** We have a solid 4x4 block of marked cells. Looking at the rows, the `X`s only appear in rows 3, 4, 5, and 6 (which means $i \geq 3$). Looking at the columns, the `X`s only appear in columns 3, 4, 5, and 6 (which means $j \geq 3$). 
* **Reasoning:** Because it's a perfect solid rectangle, the condition on the first die and the second die are independent of each other and joined by an AND. Formally, it's the Cartesian product $\{3,4,5,6\} 	imes \{3,4,5,6\}$.
* **Interpretation:** Both dice rolled a number 3 or greater.
* **Final Statement:** **"Both dice show a number that is at least 3."**

### Case 2
```text
      1 2 3 4 5 6
1     X . . . . .
2     . X . . . .
3     . . X . . .
4     . . . X . .
5     . . . . X .
6     . . . . . X
```
* **Analysis of the Set:** The marked cells form a perfect diagonal going down and to the right. 
* **Reasoning:** If we look at the coordinates of the marked cells, we get $(1,1), (2,2), (3,3), (4,4), (5,5), (6,6)$. The invariant rule connecting all these points is the algebraic equation $i = j$.
* **Interpretation:** The number on the first die is exactly equal to the number on the second die. 
* **Final Statement:** **"Both dice show the same number,"** or commonly, **"A double is rolled."**