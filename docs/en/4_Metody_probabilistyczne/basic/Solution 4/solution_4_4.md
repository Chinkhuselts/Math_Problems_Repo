# Solution: List 4 — Problem 4 (Building complex statements)

## Conceptual Introduction & Set Theory Mapping
This problem serves as a visual playground for formal logic and Boolean algebra. We are given three foundational sets (events) inside our $6 \times 6$ Cartesian sample space $\Omega$:
*   **$A$:** Sum is 7 (The Anti-Diagonal)
*   **$B$:** First die $>$ Second die (The Lower Triangle)
*   **$C$:** At least one 6 (The Edge Cross)

When we build "compound statements" using natural language words like *AND*, *OR*, *NOT*, and *BUT*, we are performing exact mathematical operations on these sets:
*   **OR** translates to **Set Union ($\cup$)**: Combine the marks from both grids.
*   **AND** translates to **Set Intersection ($\cap$)**: Keep only the marks that overlap in both grids.
*   **NOT** translates to **Set Complement ($^c$)**: Invert the grid (swap `X` with `.`).
*   **BUT** translates to **Set Difference ($\setminus$)** or **Intersection with Complement ($\cap \dots^c$)**: Start with the first grid and erase anything that overlaps with the second.

By overlaying these shapes visually, abstract logic becomes concrete geometry.

---

## Part A — Base statements

### Event A: The sum of the two results is equal to 7
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X .
3     . . . X . .
4     . . X . . .
5     . X . . . .
6     X . . . . .

```
*   **Shape:** The main anti-diagonal.

### Event B: The first die shows a greater number than the second
```text
      1 2 3 4 5 6
1     . . . . . .
2     X . . . . .
3     X X . . . .
4     X X X . . .
5     X X X X . .
6     X X X X X .

```
*   **Shape:** The strict lower triangle (excluding the main diagonal).

### Event C: At least one die shows 6
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     X X X X X X

```
*   **Shape:** The 6th row and 6th column (a corner cross).

---

## Part B — Compound statements

### 1. The sum is 7 OR at least one die shows 6 ($A \cup C$)
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X X
3     . . . X . X
4     . . X . . X
5     . X . . . X
6     X X X X X X

```
*   **Reasoning:** We take the anti-diagonal ($A$) and merge it with the corner cross ($C$). Every cell belonging to either set is included.

### 2. The sum is 7 AND at least one die shows 6 ($A \cap C$)
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     X . . . . .

```
*   **Reasoning:** We look strictly for the overlap between the anti-diagonal and the cross. The only points where $i+j=7$ and one of the variables is 6 are the coordinates $(1,6)$ and $(6,1)$. 

### 3. The first die is greater than the second AND at least one die shows 6 ($B \cap C$)
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     X X X X X .

```
*   **Reasoning:** We intersect the lower triangle ($B$) with the 6-cross ($C$). The 6th column ($j=6$) has no elements where $i > j$, so it disappears. The 6th row ($i=6$) contains elements where $6 > j$ for $j \in \{1,2,3,4,5\}$. This gives us a horizontal line segment.

### 4. The sum is 7, BUT the first die is not greater than the second ($A \setminus B$)
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X .
3     . . . X . .
4     . . . . . .
5     . . . . . .
6     . . . . . .

```
*   **Reasoning:** Formally, this is $A \cap B^c$. We start with the anti-diagonal ($A$) and "erase" the portion that dips into the lower triangle ($B$). This leaves only the upper half of the anti-diagonal: $(1,6), (2,5), (3,4)$. (Note: if the sum is 7, they cannot be equal, so the main diagonal is irrelevant here).

### 5. The sum is 7, AND no die shows 6 ($A \cap C^c$)
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . X .
3     . . . X . .
4     . . X . . .
5     . X . . . .
6     . . . . . .

```
*   **Reasoning:** We take the anti-diagonal ($A$) and remove any overlap with $C$. This means we erase the endpoints $(1,6)$ and $(6,1)$, leaving the inner diagonal segment $(2,5), (3,4), (4,3), (5,2)$.

### 6. At least one die shows 6, BUT the sum is not 7 ($C \setminus A$)
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     . X X X X X

```
*   **Reasoning:** Start with the 6-cross ($C$) and punch holes where it intersects the anti-diagonal ($A$). The cells $(1,6)$ and $(6,1)$ are removed from the cross.

### 7. The sum is not 7 AND the first die is greater than the second ($A^c \cap B$)
```text
      1 2 3 4 5 6
1     . . . . . .
2     X . . . . .
3     X X . . . .
4     X X . . . .
5     X . X X . .
6     . X X X X .

```
*   **Reasoning:** We start with the entire lower triangle ($B$). Then we remove the points that sum to 7. This essentially takes a slice out of the triangle, removing $(4,3), (5,2), (6,1)$.

### 8. The first die is not greater than the second AND at least one die shows 6 ($B^c \cap C$)
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     . . . . . X

```
*   **Reasoning:** "Not greater than" means $i \leq j$ (the upper triangle plus the main diagonal). We intersect this with the 6-cross. The 6th row only overlaps at $(6,6)$. The 6th column overlaps completely. Therefore, the resulting set is the entire 6th column.

### 9. It is not true that (the sum is 7 OR at least one die shows 6) ($(A \cup C)^c$)
```text
      1 2 3 4 5 6
1     X X X X X .
2     X X X X . .
3     X X X . X .
4     X X . X X .
5     X . X X X .
6     . . . . . .

```
*   **Reasoning:** By De Morgan's Law, $(A \cup C)^c = A^c \cap C^c$. This reads as: "The sum is not 7 AND no die shows 6." We take the full $6 \times 6$ board and wipe out the entire anti-diagonal and the entire 6-cross.

### 10. It is not true that (the sum is 7 AND at least one die shows 6) ($(A \cap C)^c$)
```text
      1 2 3 4 5 6
1     X X X X X .
2     X X X X X X
3     X X X X X X
4     X X X X X X
5     X X X X X X
6     . X X X X X

```
*   **Reasoning:** Also by De Morgan's Law, $(A \cap C)^c = A^c \cup C^c$. We are negating only the two overlapping intersection points. Therefore, we mark *every single cell* in the grid except for the two excluded points: $(1,6)$ and $(6,1)$.