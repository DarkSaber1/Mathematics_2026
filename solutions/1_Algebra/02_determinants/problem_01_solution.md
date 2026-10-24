## Exercise 1. Determinant of a 2×2 Matrix

### Problem Definition
Given the two $2 \times 2$ matrices:[cite: 1]

$$
A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}
$$

1. Compute the determinant of matrix $A$: $\det A$.[cite: 1]
2. Compute the determinant of matrix $B$: $\det B$.[cite: 1]
3. Determine which of the two matrices is invertible and provide a rigorous mathematical justification for your answer.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: General Formula for a $2 \times 2$ Determinant

For any arbitrary $2 \times 2$ square matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, its determinant is defined as the product of the entries on the main diagonal minus the product of the entries on the anti-diagonal:

$$
\det M = \begin{vmatrix} a & b \\ c & d \end{vmatrix} = (a \cdot d) - (b \cdot c)
$$

---

#### Step 2: Computing $\det A$

Given matrix $A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$:[cite: 1]

* Identify the components:
  * $a = 3$
  * $b = -2$
  * $c = 5$
  * $d = 4$

* Apply the $2 \times 2$ determinant formula step-by-step:

$$
\det A = (3 \cdot 4) - ((-2) \cdot 5)
$$

* Calculate individual products:
  * Main diagonal product: $3 \cdot 4 = 12$
  * Anti-diagonal product: $(-2) \cdot 5 = -10$

* Subtract the anti-diagonal product from the main diagonal product:

$$
\det A = 12 - (-10) = 12 + 10 = 22
$$

Thus:

$$
\det A = 22
$$

---

#### Step 3: Computing $\det B$

Given matrix $B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$:[cite: 1]

* Identify the components:
  * $a = 1$
  * $b = 7$
  * $c = 2$
  * $d = 14$

* Apply the $2 \times 2$ determinant formula step-by-step:

$$
\det B = (1 \cdot 14) - (7 \cdot 2)
$$

* Calculate individual products:
  * Main diagonal product: $1 \cdot 14 = 14$
  * Anti-diagonal product: $7 \cdot 2 = 14$

* Subtract the anti-diagonal product from the main diagonal product:

$$
\det B = 14 - 14 = 0
$$

Thus:

$$
\det B = 0
$$

---

#### Step 4: Invertibility Analysis and Justification

##### Theoretical Criterion for Invertibility
According to the **Invertibility Criterion** (a fundamental consequence of the Invertible Matrix Theorem), an $n \times n$ square matrix $M$ is invertible (non-singular) if and only if its determinant is non-zero:[cite: 1]

$$
M \text{ is invertible} \iff \det M \neq 0
$$

If $\det M = 0$, the matrix is singular (non-invertible), meaning its inverse matrix $M^{-1}$ does not exist.[cite: 1]

##### Application to Matrix $A$
* Calculated determinant: $\det A = 22$.
* Since $\det A = 22 \neq 0$, matrix $A$ is **invertible**.[cite: 1]
* Its inverse $A^{-1}$ can be explicitly computed using the formula $A^{-1} = \frac{1}{\det A} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$:

$$
A^{-1} = \frac{1}{22} \begin{pmatrix} 4 & 2 \\ -5 & 3 \end{pmatrix} = \begin{pmatrix} \frac{2}{11} & \frac{1}{11} \\ -\frac{5}{22} & \frac{3}{22} \end{pmatrix}
$$

##### Application to Matrix $B$
* Calculated determinant: $\det B = 0$.
* Since $\det B = 0$, matrix $B$ is **not invertible** (singular).[cite: 1]
* Notice that Row 2 ($R_2 = [2, 14]$) is exactly twice Row 1 ($R_1 = [1, 7]$): $R_2 = 2 R_1$. This linear dependence between the rows guarantees that $\det B = 0$ and confirms that $B$ cannot be inverted.[cite: 1]

---

### Conclusion and Key Takeaways

1. **Calculated Determinants:**
   * $\det A = 22$
   * $\det B = 0$

2. **Invertibility Verdict:**
   * **Matrix $A$** is **invertible** because $\det A = 22 \neq 0$.[cite: 1]
   * **Matrix $B$** is **not invertible** because $\det B = 0$.[cite: 1]