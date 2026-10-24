## Exercise 3. Swapping Two Rows

### Problem Definition
Given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}
$$

1. Compute $\det A$ using a direct calculation method.[cite: 1]
2. Form a new matrix $B$ by swapping the first row ($R_1$) and the second row ($R_2$) of matrix $A$.[cite: 1]
3. Predict the value of $\det B$ using a fundamental property of determinants.[cite: 1]
4. Explicitly calculate $\det B$ to verify your prediction step-by-step.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Computing $\det A$

To ensure maximum accuracy, we compute $\det A$ using two distinct methods: **Cofactor Expansion (Laplace Expansion)** and **Sarrus' Rule**.

##### Method A: Cofactor Expansion along Row 1 ($R_1$)

The general formula for Laplace expansion along the first row of a $3 \times 3$ matrix is:

$$
\det A = a_{11} C_{11} + a_{12} C_{12} + a_{13} C_{13}
$$

where each cofactor $C_{ij} = (-1)^{i+j} \det(M_{ij})$, and $M_{ij}$ is the $2 \times 2$ submatrix remaining after deleting row $i$ and column $j$.

* **First Term ($a_{11} = 1$):**
  $$
  C_{11} = (-1)^{1+1} \cdot \det \begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} = +1 \cdot ((3 \cdot 1) - (1 \cdot 1)) = 1 \cdot (3 - 1) = 2
  $$

* **Second Term ($a_{12} = 2$):**
  $$
  C_{12} = (-1)^{1+2} \cdot \det \begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} = -1 \cdot ((0 \cdot 1) - (1 \cdot 2)) = -1 \cdot (0 - 2) = 2
  $$

* **Third Term ($a_{13} = 0$):**
  $$
  C_{13} = (-1)^{1+3} \cdot \det \begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix} = +1 \cdot ((0 \cdot 1) - (3 \cdot 2)) = 1 \cdot (0 - 6) = -6
  $$

Combining the terms into the expansion formula:

$$
\det A = 1 \cdot (2) + 2 \cdot (2) + 0 \cdot (-6) = 2 + 4 + 0 = 6
$$

##### Method B: Double-Check via Sarrus' Rule

Augment matrix $A$ by copying its first two columns to the right:

$$
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1
\end{pmatrix}
\begin{array}{cc}
1 & 2 \\
0 & 3 \\
2 & 1
\end{array}
$$

* **Primary Diagonals (Top-Left to Bottom-Right):**
  * $P_1 = 1 \cdot 3 \cdot 1 = 3$[cite: 1]
  * $P_2 = 2 \cdot 1 \cdot 2 = 4$[cite: 1]
  * $P_3 = 0 \cdot 0 \cdot 1 = 0$[cite: 1]
  
  $$\text{Sum}_{\text{primary}} = 3 + 4 + 0 = 7$$

* **Secondary Diagonals (Bottom-Left to Top-Right):**
  * $S_1 = 2 \cdot 3 \cdot 0 = 0$[cite: 1]
  * $S_2 = 1 \cdot 1 \cdot 1 = 1$[cite: 1]
  * $S_3 = 1 \cdot 0 \cdot 2 = 0$[cite: 1]
  
  $$\text{Sum}_{\text{secondary}} = 0 + 1 + 0 = 1$$

* **Final Calculation:**
  $$
  \det A = \text{Sum}_{\text{primary}} - \text{Sum}_{\text{secondary}} = 7 - 1 = 6
  $$

Both techniques give $\det A = 6$.

---

#### Step 2: Constructing Matrix $B$

Swapping the first row ($R_1 = [1, 2, 0]$) and the second row ($R_2 = [0, 3, 1]$) of matrix $A$ yields:[cite: 1]

$$
B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}
$$

---

#### Step 3: Theoretical Prediction of $\det B$

**Determinant Property (Row Swap Rule):**
> *Swapping any two rows (or columns) of a square matrix multiplies its determinant by $-1$.*[cite: 1]

Mathematically:

$$
\det(\text{swapped matrix}) = -\det(\text{original matrix})
$$

Since $\det A = 6$, our prediction for matrix $B$ is:

$$
\det B = -\det A = -6
$$

---

#### Step 4: Verification by Direct Calculation of $\det B$

We expand $\det B$ along its first row ($R_1 = [0, 3, 1]$) to verify the prediction:

$$
\det B = b_{11} C_{11} + b_{12} C_{12} + b_{13} C_{13}
$$

* **Term 1 ($b_{11} = 0$):**
  $$
  0 \cdot \det \begin{pmatrix} 2 & 0 \\ 1 & 1 \end{pmatrix} = 0
  $$

* **Term 2 ($b_{12} = 3$):**
  $$
  (-1)^{1+2} \cdot 3 \cdot \det \begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} = -3 \cdot ((1 \cdot 1) - (0 \cdot 2)) = -3 \cdot (1 - 0) = -3
  $$

* **Term 3 ($b_{13} = 1$):**
  $$
  (-1)^{1+3} \cdot 1 \cdot \det \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix} = +1 \cdot ((1 \cdot 1) - (2 \cdot 2)) = +1 \cdot (1 - 4) = -3
  $$

Combining all three terms:

$$
\det B = 0 + (-3) + (-3) = -6
$$

The direct calculation yields $\det B = -6$, which matches the theoretical prediction.

---

### Conclusion and Key Takeaways

1. **Determinant Values:**
   * $\det A = 6$
   * $\det B = -6$

2. **Core Property Verified:**
   Interchanging two rows flips the sign of the determinant while maintaining its absolute value ($|-6| = |6| = 6$).