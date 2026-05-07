# Solution: List 4 — Problem 4 (Building complex statements)

## Conceptual Introduction & Set Theory Mapping

We are given three foundational sets inside a $6 \times 6$ Cartesian sample space $\Omega$ (rows = first die, columns = second die):

- **$A$:** Sum is 7 — the anti-diagonal
- **$B$:** First die $>$ Second die — the strict lower triangle
- **$C$:** At least one 6 — the 6th row and 6th column

Operations on sets:
- **OR** → Union ($\cup$): include cells from *either* grid
- **AND** → Intersection ($\cap$): keep only cells in *both* grids
- **NOT** → Complement ($^c$): flip every cell
- **BUT** → Set Difference ($\setminus$): start with one grid, erase the overlap with the other

---

## Part A — Base Events

<table>
<tr>
<th align="center">Event A &nbsp;—&nbsp; Sum = 7</th>
<th align="center">Event B &nbsp;—&nbsp; First die &gt; Second die</th>
<th align="center">Event C &nbsp;—&nbsp; At least one die shows 6</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 X . . . . .
3 X X . . . .
4 X X X . . .
5 X X X X . .
6 X X X X X .
</pre></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
</tr>
</table>

---

## Part B — Compound Events

### 1. The sum is 7 OR at least one die shows 6 &nbsp; ($A \cup C$)

<table>
<tr>
<th align="center">Event A &nbsp;(Sum = 7)</th>
<th align="center">∪</th>
<th align="center">Event C &nbsp;(At least one 6)</th>
<th align="center">=</th>
<th align="center">Result: $A \cup C$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td align="center"><b>∪</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X X
3 . . . X . X
4 . . X . . X
5 . X . . . X
6 X X X X X X
</pre></td>
</tr>
</table>

> Merge the anti-diagonal with the 6-cross. Every cell belonging to either set is included.

---

### 2. The sum is 7 AND at least one die shows 6 &nbsp; ($A \cap C$)

<table>
<tr>
<th align="center">Event A &nbsp;(Sum = 7)</th>
<th align="center">∩</th>
<th align="center">Event C &nbsp;(At least one 6)</th>
<th align="center">=</th>
<th align="center">Result: $A \cap C$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td align="center"><b>∩</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . .
3 . . . . . .
4 . . . . . .
5 . . . . . .
6 X . . . . .
</pre></td>
</tr>
</table>

> Only cells where $i+j=7$ **and** one die is 6: $(1,6)$ and $(6,1)$.

---

### 3. The first die is greater than the second AND at least one die shows 6 &nbsp; ($B \cap C$)

<table>
<tr>
<th align="center">Event B &nbsp;(First &gt; Second)</th>
<th align="center">∩</th>
<th align="center">Event C &nbsp;(At least one 6)</th>
<th align="center">=</th>
<th align="center">Result: $B \cap C$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 X . . . . .
3 X X . . . .
4 X X X . . .
5 X X X X . .
6 X X X X X .
</pre></td>
<td align="center"><b>∩</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 . . . . . .
3 . . . . . .
4 . . . . . .
5 . . . . . .
6 X X X X X .
</pre></td>
</tr>
</table>

> Column 6 ($j=6$) has no cells where $i>j$, so it drops out. Row 6 ($i=6$) gives $6>j$ for $j \in \{1,2,3,4,5\}$ — a horizontal strip.

---

### 4. The sum is 7, BUT the first die is not greater than the second &nbsp; ($A \setminus B$)

<table>
<tr>
<th align="center">Event A &nbsp;(Sum = 7)</th>
<th align="center">∖</th>
<th align="center">Event B &nbsp;(First &gt; Second)</th>
<th align="center">=</th>
<th align="center">Result: $A \setminus B$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td align="center"><b>∖</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 X . . . . .
3 X X . . . .
4 X X X . . .
5 X X X X . .
6 X X X X X .
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . . . . .
5 . . . . . .
6 . . . . . .
</pre></td>
</tr>
</table>

> Formally $A \cap B^c$. Remove the lower-triangle portion of the anti-diagonal. Leaves the upper half: $(1,6), (2,5), (3,4)$.

---

### 5. The sum is 7 AND no die shows 6 &nbsp; ($A \cap C^c$)

<table>
<tr>
<th align="center">Event A &nbsp;(Sum = 7)</th>
<th align="center">∩</th>
<th align="center">Event C<sup>c</sup> &nbsp;(No 6)</th>
<th align="center">=</th>
<th align="center">Result: $A \cap C^c$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td align="center"><b>∩</b></td>
<td><pre>
  1 2 3 4 5 6
1 X X X X X .
2 X X X X X .
3 X X X X X .
4 X X X X X .
5 X X X X X .
6 . . . . . .
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 . . . . . .
</pre></td>
</tr>
</table>

> Remove the two endpoints of the anti-diagonal that touch the 6-cross: $(1,6)$ and $(6,1)$. Leaves the inner segment $(2,5),(3,4),(4,3),(5,2)$.

---

### 6. At least one die shows 6, BUT the sum is not 7 &nbsp; ($C \setminus A$)

<table>
<tr>
<th align="center">Event C &nbsp;(At least one 6)</th>
<th align="center">∖</th>
<th align="center">Event A &nbsp;(Sum = 7)</th>
<th align="center">=</th>
<th align="center">Result: $C \setminus A$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
<td align="center"><b>∖</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 . X X X X X
</pre></td>
</tr>
</table>

> Start with the 6-cross and punch out the two intersection points $(1,6)$ and $(6,1)$.

---

### 7. The sum is not 7 AND the first die is greater than the second &nbsp; ($A^c \cap B$)

<table>
<tr>
<th align="center">Event A<sup>c</sup> &nbsp;(Sum ≠ 7)</th>
<th align="center">∩</th>
<th align="center">Event B &nbsp;(First &gt; Second)</th>
<th align="center">=</th>
<th align="center">Result: $A^c \cap B$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 X X X X X .
2 X X X X . X
3 X X X . X X
4 X X . X X X
5 X . X X X X
6 . X X X X X
</pre></td>
<td align="center"><b>∩</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 X . . . . .
3 X X . . . .
4 X X X . . .
5 X X X X . .
6 X X X X X .
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . .
2 X . . . . .
3 X X . . . .
4 X X . . . .
5 X . X X . .
6 . X X X X .
</pre></td>
</tr>
</table>

> Take the lower triangle ($B$) and remove the three anti-diagonal cells that fall inside it: $(4,3),(5,2),(6,1)$.

---

### 8. The first die is NOT greater than the second AND at least one die shows 6 &nbsp; ($B^c \cap C$)

<table>
<tr>
<th align="center">Event B<sup>c</sup> &nbsp;(First ≤ Second)</th>
<th align="center">∩</th>
<th align="center">Event C &nbsp;(At least one 6)</th>
<th align="center">=</th>
<th align="center">Result: $B^c \cap C$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 X X X X X X
2 . X X X X X
3 . . X X X X
4 . . . X X X
5 . . . . X X
6 . . . . . X
</pre></td>
<td align="center"><b>∩</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
<td align="center"><b>=</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 . . . . . X
</pre></td>
</tr>
</table>

> "$i \leq j$" (upper triangle + diagonal) intersected with the 6-cross. Row 6 loses all but $(6,6)$; column 6 survives entirely — the result is the full 6th column.

---

### 9. NOT (sum is 7 OR at least one die shows 6) &nbsp; ($(A \cup C)^c$)

<table>
<tr>
<th align="center">Event A &nbsp;(Sum = 7)</th>
<th align="center">∪</th>
<th align="center">Event C &nbsp;(At least one 6)</th>
<th align="center">=</th>
<th align="center">Result: $(A \cup C)^c$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td align="center"><b>∪</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
<td align="center"><b>complement →</b></td>
<td><pre>
  1 2 3 4 5 6
1 X X X X X .
2 X X X X . .
3 X X X . X .
4 X X . X X .
5 X . X X X .
6 . . . . . .
</pre></td>
</tr>
</table>

> By De Morgan: $(A \cup C)^c = A^c \cap C^c$ — "sum ≠ 7 AND no 6." The entire anti-diagonal and 6-cross are wiped from the board.

---

### 10. NOT (sum is 7 AND at least one die shows 6) &nbsp; ($(A \cap C)^c$)

<table>
<tr>
<th align="center">Event A &nbsp;(Sum = 7)</th>
<th align="center">∩</th>
<th align="center">Event C &nbsp;(At least one 6)</th>
<th align="center">=</th>
<th align="center">Result: $(A \cap C)^c$</th>
</tr>
<tr>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .
</pre></td>
<td align="center"><b>∩</b></td>
<td><pre>
  1 2 3 4 5 6
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X
</pre></td>
<td align="center"><b>complement →</b></td>
<td><pre>
  1 2 3 4 5 6
1 X X X X X .
2 X X X X X X
3 X X X X X X
4 X X X X X X
5 X X X X X X
6 . X X X X X
</pre></td>
</tr>
</table>

> By De Morgan: $(A \cap C)^c = A^c \cup C^c$. Since $A \cap C$ contains only $(1,6)$ and $(6,1)$, we negate just those two — marking every other cell in the grid.
