## Exercise 2. Determinant of a 3×3 Matrix

### Problem Definition
Given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}
$$

1. Compute $\det A$ using **Sarrus' Rule**.[cite: 1]
2. Perform a verification check using a chosen **property of the determinant**.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Explanation and Formula for Sarrus' Rule

Sarrus' Rule is a mnemonic device used exclusively for computing the determinant of $3 \times 3$ matrices. 

To perform this calculation:
1. Write down the original $3 \times 3$ matrix.
2. Duplicate the first two columns to the right of the third column.
3. Sum the products of the three **primary diagonals** (top-left to bottom-right).
4. Sum the products of the three **secondary diagonals** (bottom-left to top-right).
5. Subtract the secondary sum from the primary sum:

$$
\det A = \text{Sum}_{\text{primary}} - \text{Sum}_{\text{secondary}}
$$

---

#### Step 2: Step-by-Step Calculation using Sarrus' Rule

##### Augmented Matrix Setup
We write the matrix alongside its first two repeated columns:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5
\end{pmatrix}
\begin{array}{cc}
1 & 2 \\
0 & 3 \\
2 & 1
\end{array}
$$

##### Part A: Primary Diagonals (Top-Left to Bottom-Right)
* **First Primary Diagonal ($P_1$):**
  $$
  P_1 = 1 \cdot 3 \cdot 5 = 15
  $$
* **Second Primary Diagonal ($P_2$):**
  $$
  P_2 = 2 \cdot 4 \cdot 2 = 16
  $$
* **Third Primary Diagonal ($P_3$):**
  $$
  P_3 = (-1) \cdot 0 \cdot 1 = 0
  $$

* **Sum of Primary Diagonals:**
  $$
  \text{Sum}_{\text{primary}} = P_1 + P_2 + P_3 = 15 + 16 + 0 = 31
  $$

##### Part B: Secondary Diagonals (Bottom-Left to Top-Right)
* **First Secondary Diagonal ($S_1$):**
  $$
  S_1 = 2 \cdot 3 \cdot (-1) = -6
  $$
* **Second Secondary Diagonal ($S_2$):**
  $$
  S_2 = 1 \cdot 4 \cdot 1 = 4
  $$
* **Third Secondary Diagonal ($S_3$):**
  $$
  S_3 = 5 \cdot 0 \cdot 2 = 0
  $$

* **Sum of Secondary Diagonals:**
  $$
  \text{Sum}_{\text{secondary}} = S_1 + S_2 + S_3 = -6 + 4 + 0 = -2
  $$

##### Part C: Final Calculation
Subtracting the secondary sum from the primary sum yields:

$$
\det A = \text{Sum}_{\text{primary}} - \text{Sum}_{\text{secondary}} = 31 - (-2) = 31 + 2 = 33
$$

---

#### Step 3: Verification using Determinant Properties

To double-check this result without performing another full Sarrus calculation, we utilize elementary row operations.[cite: 1]

##### Determinant Property (Row Addition Rule)
> *Adding a scalar multiple of one row to another row leaves the value of the determinant completely unchanged.*[cite: 1]

Mathematically, performing $R_i \leftarrow R_i + k R_j$ results in a matrix $A'$ such that:

$$
\det A' = \det A
$$

##### Applying Row Operation $R_3 \leftarrow R_3 - 2 R_1$
We aim to introduce a zero in the first column at row 3 ($a_{31}$):

* Current Row 3: $R_3 = [2, 1, 5]$
* $2 \times$ Row 1: $2 R_1 = [2(1), 2(2), 2(-1)] = [2, 4, -2]$
* New Row 3: $R_3' = R_3 - 2 R_1 = [2 - 2, 1 - 4, 5 - (-2)] = [0, -3, 7]$

The modified matrix is:

$$
A' = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 0 & -3 & 7 \end{pmatrix}
$$

##### Expanding $\det A'$ along Column 1
Because Column 1 now contains two zeros, Laplace cofactor expansion along Column 1 is extremely simple:

$$
\det A' = a'_{11} C_{11} + a'_{21} C_{21} + a'_{31} C_{31}
$$

Since $a'_{21} = 0$ and $a'_{31} = 0$:

$$
\det A' = 1 \cdot (-1)^{1+1} \cdot \det \begin{pmatrix} 3 & 4 \\ -3 & 7 \end{pmatrix}
$$

$$
\det A' = 1 \cdot ((3 \cdot 7) - (4 \cdot (-3))) = 21 - (-12) = 21 + 12 = 33
$$

Since $\det A = \det A'$, this confirms that $\det A = 33$.

---

#### Step 4: Second Verification via Direct Cofactor Expansion (Row 1)

For maximum mathematical thoroughness, we also compute $\det A$ using Laplace expansion along Row 1 ($R_1 = [1, 2, -1]$):

$$
\det A = a_{11} C_{11} + a_{12} C_{12} + a_{13} C_{13}
$$

* **Entry $a_{11} = 1$:**
  $$
  C_{11} = (+1) \cdot \det \begin{pmatrix} 3 & 4 \\ 1 & 5 \end{pmatrix} = (3 \cdot 5) - (4 \cdot 1) = 15 - 4 = 11
  $$

* **Entry $a_{12} = 2$:**
  $$
  C_{12} = (-1) \cdot \det \begin{pmatrix} 0 & 4 \\ 2 & 5 \end{pmatrix} = -1 \cdot ((0 \cdot 5) - (4 \cdot 2)) = -1 \cdot (0 - 8) = 8
  $$

* **Entry $a_{13} = -1$:**
  $$
  C_{13} = (+1) \cdot \det \begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix} = 1 \cdot ((0 \cdot 1) - (3 \cdot 2)) = 1 \cdot (0 - 6) = -6
  $$

Combining the cofactor terms:

$$
\det A = 1 \cdot (11) + 2 \cdot (8) + (-1) \cdot (-6) = 11 + 16 + 6 = 33
$$

---

### Conclusion and Key Takeaways

1. **Calculated Value:**
   $$\det A = 33$$

2. **Verification Summary:**
   All three independent methods (Sarrus' Rule, Row Operations + Column Expansion, and Direct Laplace Expansion) consistently give $\det A = 33$.