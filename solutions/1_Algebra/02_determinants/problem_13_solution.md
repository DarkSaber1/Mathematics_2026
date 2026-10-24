## Exercise 13. Determinant by Elimination

### Problem Definition
Given the $3 \times 3$ matrix:[cite: 1]

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}
$$

1. Compute $\det A$ using Gaussian elimination (row reduction to upper triangular form).[cite: 1]
2. Record the exact effect of every single row operation used on the value of the determinant.[cite: 1]
3. Verify the final result using an independent calculation method (such as Laplace expansion or Sarrus' Rule).

---

### Key Theoretical Framework: Row Operations & Determinants

During elimination, the effect of elementary row operations on the determinant of a square matrix is governed by three fundamental rules:

1. **Row Addition ($R_i \leftarrow R_i + k R_j$):**
   Adding a scalar multiple of one row to another **does not change** the determinant:
   $$ \det(A_{\text{new}}) = \det(A_{\text{old}}) $$

2. **Row Swap ($R_i \leftrightarrow R_j$):**
   Interchanging two rows **multiplies the determinant by $-1$**:
   $$ \det(A_{\text{new}}) = -\det(A_{\text{old}}) $$

3. **Row Scaling ($R_i \leftarrow k R_i$):**
   Multiplying a row by a non-zero scalar $k$ **scales the determinant by $k$**:
   $$ \det(A_{\text{new}}) = k \cdot \det(A_{\text{old}}) \implies \det(A_{\text{old}}) = \frac{1}{k} \det(A_{\text{new}}) $$

---

### Detailed Mathematical Solution via Elimination

#### Step 1: Initial Matrix State
We begin with the original matrix $A$:[cite: 1]

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}
$$

Our objective is to use the pivot element $a_{11} = 1$ in Row 1 to eliminate the entries below it in Column 1 ($a_{21} = 2$ and $a_{31} = 1$).

---

#### Step 2: Creating Zeros in Column 1

##### Operation 1: $R_2 \leftarrow R_2 - 2 R_1$
* **Goal:** Eliminate entry $a_{21} = 2$.
* **Vector Arithmetic:**
  $$
  R_2 - 2 R_1 = [2,\; 5,\; 7] - 2 \cdot [1,\; 2,\; 3] = [2 - 2,\; 5 - 4,\; 7 - 6] = [0,\; 1,\; 1]
  $$
* **Effect on Determinant:** Row addition type operation ($k = -2$). **Determinant value remains unchanged.**

The matrix becomes:

$$
A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \end{pmatrix} \implies \det A = \det A_1
$$

##### Operation 2: $R_3 \leftarrow R_3 - R_1$
* **Goal:** Eliminate entry $a_{31} = 1$.
* **Vector Arithmetic:**
  $$
  R_3 - R_1 = [1,\; 0,\; 2] - [1,\; 2,\; 3] = [1 - 1,\; 0 - 2,\; 2 - 3] = [0,\; -2,\; -1]
  $$
* **Effect on Determinant:** Row addition type operation ($k = -1$). **Determinant value remains unchanged.**

The matrix becomes:

$$
A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \end{pmatrix} \implies \det A = \det A_2
$$

---

#### Step 3: Creating Zero in Column 2 Below the Main Diagonal

Inspect matrix $A_2$:

$$
A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \end{pmatrix}
$$

The pivot entry in Row 2 is $a_{22} = 1$. We use Row 2 to eliminate entry $a_{32} = -2$ in Row 3.

##### Operation 3: $R_3 \leftarrow R_3 + 2 R_2$
* **Goal:** Eliminate entry $a_{32} = -2$.
* **Vector Arithmetic:**
  $$
  R_3 + 2 R_2 = [0,\; -2,\; -1] + 2 \cdot [0,\; 1,\; 1] = [0 + 0,\; -2 + 2,\; -1 + 2] = [0,\; 0,\; 1]
  $$
* **Effect on Determinant:** Row addition type operation ($k = 2$). **Determinant value remains unchanged.**

The matrix reaches upper triangular form $U$:

$$
U = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix} \implies \det A = \det U
$$

---

#### Step 4: Computing Determinant of Upper Triangular Matrix $U$

Since matrix $U$ is upper triangular (all entries below the main diagonal are strictly zero), its determinant is the product of its main diagonal entries:[cite: 1]

$$
\det U = u_{11} \cdot u_{22} \cdot u_{33} = 1 \cdot 1 \cdot 1 = 1
$$

Because every single row operation performed was a row addition ($R_i \leftarrow R_i + k R_j$), none of the operations altered the determinant value at any point:

$$
\det A = \det A_1 = \det A_2 = \det U = 1
$$

---

#### Step 5: Verification via Sarrus' Rule

To rigorously double-check the elimination result, compute $\det A$ using Sarrus' Rule on the original matrix $A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}$:

$$
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2
\end{pmatrix}
\begin{array}{cc}
1 & 2 \\
2 & 5 \\
1 & 0
\end{array}
$$

* **Primary Diagonals (Top-Left to Bottom-Right):**
  * $P_1 = 1 \cdot 5 \cdot 2 = 10$
  * $P_2 = 2 \cdot 7 \cdot 1 = 14$
  * $P_3 = 3 \cdot 2 \cdot 0 = 0$
  
  $$\text{Sum}_{\text{primary}} = 10 + 14 + 0 = 24$$

* **Secondary Diagonals (Bottom-Left to Top-Right):**
  * $S_1 = 1 \cdot 5 \cdot 3 = 15$
  * $S_2 = 0 \cdot 7 \cdot 1 = 0$
  * $S_3 = 2 \cdot 2 \cdot 2 = 8$
  
  $$\text{Sum}_{\text{secondary}} = 15 + 0 + 8 = 23$$

* **Final Calculation:**
  $$
  \det A = \text{Sum}_{\text{primary}} - \text{Sum}_{\text{secondary}} = 24 - 23 = 1
  $$

Both elimination and Sarrus' Rule yield $\det A = 1$.

---

### Step-by-Step Row Operation Tracking Summary

| Step | Operation Applied | Resulting Row | Effect on Determinant Value | Determinant Relation |
| :---: | :--- | :--- | :--- | :---: |
| **0** | Initial Matrix $A$ | - | Base matrix | $\det A$ |
| **1** | $R_2 \leftarrow R_2 - 2 R_1$ | $[0,\; 1,\; 1]$ | No change (Row Addition) | $\det A_1 = \det A$ |
| **2** | $R_3 \leftarrow R_3 - R_1$ | $[0,\; -2,\; -1]$ | No change (Row Addition) | $\det A_2 = \det A$ |
| **3** | $R_3 \leftarrow R_3 + 2 R_2$ | $[0,\; 0,\; 1]$ | No change (Row Addition) | $\det U = \det A$ |
| **4** | Diagonal Product | - | $1 \cdot 1 \cdot 1 = 1$ | $\det A = 1$ |

---

### Conclusion and Key Takeaways

1. **Calculated Determinant:**
   $$\det A = 1$$

2. **Core Elimination Insight:**
   Using row addition operations exclusively ($R_i \leftarrow R_i + k R_j$) allows reducing any matrix to upper triangular form while keeping the determinant completely invariant, making computation straightforward.[cite: 1]