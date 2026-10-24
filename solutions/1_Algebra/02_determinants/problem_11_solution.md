## Exercise 11. Shortening the Calculation with Row Operations

### Problem Definition
Given the $3 \times 3$ matrix:[cite: 1]

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}
$$

1. Compute $\det A$ by first performing elementary row operations that create as many zeros as possible.[cite: 1]
2. State explicitly which row operations do not change the determinant.[cite: 1]
3. Explain how strategic planning simplifies the computation compared to a mechanical full expansion.[cite: 1]

---

### Key Determinant Property: Row Addition Rule

> **Property:** Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + k R_j$) does **not change** the value of the determinant:[cite: 1]
>
> $$ \det(A') = \det(A) $$

By using row addition/subtraction exclusively, we can transform matrix $A$ into an upper triangular matrix without introducing any scaling factors or sign changes, making the final determinant calculation immediate.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Strategic Planning

Looking at the first column of matrix $A$:

$$
A = \begin{pmatrix} 
1 & 2 & 3 \\ 
1 & 3 & 4 \\ 
1 & 4 & 6 
\end{pmatrix}
$$

Notice that all entries in Column 1 are equal to $1$ ($a_{11} = 1, a_{21} = 1, a_{31} = 1$). 

By using Row 1 ($R_1$) as a pivot row and subtracting $R_1$ from Row 2 ($R_2$) and Row 3 ($R_3$), we can instantly eliminate the non-zero entries in Column 1 below the top-left entry.[cite: 1]

---

#### Step 2: Step-by-Step Row Elimination

##### Operation 1: $R_2 \leftarrow R_2 - R_1$
* **Goal:** Create a zero at position $(2,1)$.
* **Calculation:**
  $$
  R_2 - R_1 = [1 - 1,\; 3 - 2,\; 4 - 3] = [0,\; 1,\; 1]
  $$
* **Determinant Impact:** Row addition ($k = -1$). **Determinant remains unchanged.**

The matrix becomes:

$$
A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 4 & 6 \end{pmatrix} \implies \det A = \det A_1
$$

##### Operation 2: $R_3 \leftarrow R_3 - R_1$
* **Goal:** Create a zero at position $(3,1)$.
* **Calculation:**
  $$
  R_3 - R_1 = [1 - 1,\; 4 - 2,\; 6 - 3] = [0,\; 2,\; 3]
  $$
* **Determinant Impact:** Row addition ($k = -1$). **Determinant remains unchanged.**

The matrix becomes:

$$
A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix} \implies \det A = \det A_2
$$

---

#### Step 3: Eliminating Entry Below the Main Diagonal in Column 2

Now inspect $A_2$:

$$
A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}
$$

Row 2 now has pivot entry $1$ at $(2,2)$, and Row 3 has entry $2$ at $(3,2)$. We eliminate position $(3,2)$ using Row 2.

##### Operation 3: $R_3 \leftarrow R_3 - 2 R_2$
* **Goal:** Create a zero at position $(3,2)$.
* **Calculation:**
  $$
  R_3 - 2 R_2 = [0 - 2(0),\; 2 - 2(1),\; 3 - 2(1)] = [0,\; 0,\; 1]
  $$
* **Determinant Impact:** Row addition ($k = -2$). **Determinant remains unchanged.**

The resulting upper triangular matrix $A_3$ is:

$$
A_3 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix} \implies \det A = \det A_3
$$

---

#### Step 4: Computing the Final Determinant Value

Matrix $A_3$ is now in **upper triangular form** (all entries strictly below the main diagonal are zeros).

The determinant of any upper triangular matrix is the product of its main diagonal entries:[cite: 1]

$$
\det A_3 = a_{11} \cdot a_{22} \cdot a_{33} = 1 \cdot 1 \cdot 1 = 1
$$

Since none of the three row operations modified the determinant value:

$$
\det A = \det A_3 = 1
$$

---

#### Step 5: Verification via Cofactor Expansion along Column 1

To confirm our solution, we expand $\det A_2$ along Column 1 (which contains two zeros):

$$
A_2 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}
$$

$$
\det A = 1 \cdot (-1)^{1+1} \cdot \det \begin{pmatrix} 1 & 1 \\ 2 & 3 \end{pmatrix} = 1 \cdot ((1 \cdot 3) - (1 \cdot 2)) = 3 - 2 = 1
$$

Both approaches give $\det A = 1$.

---

### Summary of Row Operations Used

| Step | Row Operation | New Row Result | Impact on $\det A$ |
| :--- | :--- | :--- | :--- |
| **1** | $R_2 \leftarrow R_2 - R_1$ | $[0,\; 1,\; 1]$ | **No change** (Row Addition) |
| **2** | $R_3 \leftarrow R_3 - R_1$ | $[0,\; 2,\; 3]$ | **No change** (Row Addition) |
| **3** | $R_3 \leftarrow R_3 - 2 R_2$ | $[0,\; 0,\; 1]$ | **No change** (Row Addition) |

---

### Conclusion and Key Takeaways

1. **Calculated Value:**
   $$\det A = 1$$

2. **Operations that do not change the determinant:**
   All operations of the form $R_i \leftarrow R_i + k R_j$ (such as $R_2 - R_1$, $R_3 - R_1$, and $R_3 - 2 R_2$) leave the determinant completely unchanged.[cite: 1]

3. **Strategic Advantage:**
   Creating zeros systematically turns a multi-term multiplication into a simple product of diagonal elements ($1 \cdot 1 \cdot 1 = 1$), eliminating computational errors.[cite: 1]