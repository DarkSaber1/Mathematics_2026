## Exercise 5. Row Operations

### Problem Definition
Given the $3 \times 3$ matrix:[cite: 1]

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}
$$

1. Find $\det A$ by systematically simplifying matrix $A$ into an upper triangular matrix using elementary row operations.[cite: 1]
2. At every individual operation step, state explicitly whether and how the determinant value changes.[cite: 1]
3. Verify the final result using an independent calculation (such as Sarrus' Rule or cofactor expansion).

---

### Key Theoretical Rules: Row Operations and Determinants

When performing Gaussian elimination on a square matrix $M$, the three elementary row operations affect the determinant as follows:

1. **Row Addition ($R_i \leftarrow R_i + k R_j$):**
   Adding a scalar multiple of row $j$ to row $i$ **does not change** the determinant:
   $$
   \det(M') = \det(M)
   $$

2. **Row Scaling ($R_i \leftarrow k R_i$ or factoring out $k$):**
   Multiplying a single row by a non-zero scalar $k$ (or factoring $k$ out of a row) **scales the determinant by $k$**:
   $$
   \det(M) = k \cdot \det(M')
   $$

3. **Row Swap ($R_i \leftrightarrow R_j$):**
   Interchanging two rows **flips the sign** of the determinant:
   $$
   \det(M') = -\det(M)
   $$

---

### Detailed Step-by-Step Solution

#### Step 1: Creating Zeros in Column 1 Below the Main Diagonal

We start with matrix $A$:

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}
$$

##### Operation 1A: $R_2 \leftarrow R_2 - 2 R_1$
* **Goal:** Eliminate entry $a_{21} = 2$.
* **Calculation:**
  $$
  R_2 - 2 R_1 = [2 - 2(1),\; 1 - 2(2),\; 0 - 2(3)] = [0,\; -3,\; -6]
  $$
* **Effect on Determinant:** Row addition operation—**Determinant remains unchanged.**

$$
\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}
$$

##### Operation 1B: $R_3 \leftarrow R_3 + R_1$
* **Goal:** Eliminate entry $a_{31} = -1$.
* **Calculation:**
  $$
  R_3 + R_1 = [-1 + 1,\; 4 + 2,\; 2 + 3] = [0,\; 6,\; 5]
  $$
* **Effect on Determinant:** Row addition operation—**Determinant remains unchanged.**

Let $A_1$ be the matrix after these two row additions:

$$
A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix} \implies \det A = \det A_1
$$

---

#### Step 2: Simplifying Row 2 by Factoring Out a Scalar

Notice that all elements in Row 2 of $A_1$ ($[0, -3, -6]$) share a common scalar factor of $-3$.

##### Operation 2: Factor out $-3$ from Row 2
* **Goal:** Make the pivot element in position $(2,2)$ equal to $1$.
* **Effect on Determinant:** Factoring out a scalar $k = -3$ from a single row scales the determinant expression by $-3$.

$$
\det A_1 = -3 \cdot \det A_2
$$

where matrix $A_2$ is:

$$
A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 2 \\ 0 & 6 & 5 \end{pmatrix}
$$

---

#### Step 3: Creating Zero in Column 2 Below the Pivot

We now eliminate entry $a_{32} = 6$ in matrix $A_2$.

##### Operation 3: $R_3 \leftarrow R_3 - 6 R_2$
* **Goal:** Eliminate the entry below the main diagonal in Column 2.
* **Calculation:**
  $$
  R_3 - 6 R_2 = [0 - 6(0),\; 6 - 6(1),\; 5 - 6(2)] = [0,\; 0,\; -7]
  $$
* **Effect on Determinant:** Row addition operation—**Determinant remains unchanged** ($\det A_3 = \det A_2$).

The resulting matrix $A_3$ is:

$$
A_3 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 2 \\ 0 & 0 & -7 \end{pmatrix}
$$

---

#### Step 4: Computing the Determinant of Upper Triangular Matrix $A_3$

Matrix $A_3$ is now in **upper triangular form** (all entries below the main diagonal are $0$).

According to the triangular matrix rule:

$$
\det A_3 = \text{product of main diagonal entries} = (1) \cdot (1) \cdot (-7) = -7
$$

---

#### Step 5: Back-Substituting to Find $\det A$

Reassembling our tracked determinant factor equation from Step 2:

$$
\det A = -3 \cdot \det A_3
$$

Substituting $\det A_3 = -7$:

$$
\det A = (-3) \cdot (-7) = 21
$$

---

### Step 6: Verification via Sarrus' Rule

To rigorously confirm our result, we evaluate $\det A$ directly using Sarrus' Rule on the original matrix $A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}$:

$$
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2
\end{pmatrix}
\begin{array}{cc}
1 & 2 \\
2 & 1 \\
-1 & 4
\end{array}
$$

* **Primary Diagonals (Top-Left to Bottom-Right):**
  * $P_1 = 1 \cdot 1 \cdot 2 = 2$
  * $P_2 = 2 \cdot 0 \cdot (-1) = 0$
  * $P_3 = 3 \cdot 2 \cdot 4 = 24$
  
  $$\text{Sum}_{\text{primary}} = 2 + 0 + 24 = 26$$

* **Secondary Diagonals (Bottom-Left to Top-Right):**
  * $S_1 = (-1) \cdot 1 \cdot 3 = -3$
  * $S_2 = 4 \cdot 0 \cdot 1 = 0$
  * $S_3 = 2 \cdot 2 \cdot 2 = 8$
  
  $$\text{Sum}_{\text{secondary}} = (-3) + 0 + 8 = 5$$

* **Final Computation:**
  $$
  \det A = \text{Sum}_{\text{primary}} - \text{Sum}_{\text{secondary}} = 26 - 5 = 21
  $$

Both methods yield the exact same result: $\det A = 21$.

---

### Summary of Row Operations & Determinant Effects

| Step | Operation Applied | Determinant Tracking Equation | Effect / Reason |
| :--- | :--- | :--- | :--- |
| **Start** | Original Matrix $A$ | $\det A$ | Base value |
| **Step 1A** | $R_2 \leftarrow R_2 - 2 R_1$ | $\det A = \det A_1$ | No change (Row Addition) |
| **Step 1B** | $R_3 \leftarrow R_3 + R_1$ | $\det A = \det A_1$ | No change (Row Addition) |
| **Step 2** | Factor $-3$ out of $R_2$ | $\det A = -3 \cdot \det A_2$ | Multiplied by scalar factor $-3$ |
| **Step 3** | $R_3 \leftarrow R_3 - 6 R_2$ | $\det A = -3 \cdot \det A_3$ | No change (Row Addition) |
| **Step 4** | Compute $\det A_3$ | $\det A_3 = 1 \cdot 1 \cdot (-7) = -7$ | Diagonal product of upper triangular matrix |
| **Final** | Combine Factors | $\det A = (-3)(-7) = 21$ | Final result verified |