## Exercise 10. Detecting Dependence

### Problem Definition
Given the $3 \times 3$ matrix:[cite: 1]

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix}
$$

1. Without performing a full determinant computation (such as Sarrus' Rule or cofactor expansion), explain why $\det A = 0$.[cite: 1]
2. Identify the specific linear dependence relationship between the rows of matrix $A$.[cite: 1]
3. Connect this linear dependence to the non-invertibility of the matrix.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Identifying Linear Dependence Among Rows

Let us write down the three rows of matrix $A$ as row vectors:[cite: 1]

$$
R_1 = \begin{pmatrix} 1 & 2 & 3 \end{pmatrix}
$$

$$
R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}
$$

$$
R_3 = \begin{pmatrix} 0 & 1 & 5 \end{pmatrix}
$$

By inspecting Row 1 ($R_1$) and Row 2 ($R_2$), we observe an immediate proportional relationship:

$$
R_2 = 2 \cdot R_1 = 2 \cdot \begin{pmatrix} 1 & 2 & 3 \end{pmatrix} = \begin{pmatrix} 2 \cdot 1 & 2 \cdot 2 & 2 \cdot 3 \end{pmatrix} = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}
$$

Row 2 is an exact scalar multiple of Row 1 (with scalar factor $c = 2$).[cite: 1]

---

#### Step 2: Determinant Property of Proportional / Linearly Dependent Rows

##### Theoretical Property
> *If a square matrix has two rows (or two columns) that are scalar multiples of each other—or if one row can be expressed as a linear combination of the other rows—the determinant of the matrix is identically equal to zero.*

##### Algebraic Explanation via Row Operations
Recall the fundamental row operation property:
* Performing $R_2 \leftarrow R_2 - 2 R_1$ does **not change** the value of the determinant ($\det A' = \det A$).

Let us apply this single row operation to matrix $A$:

$$
R_2 - 2 R_1 = \begin{pmatrix} 2 - 2(1) & 4 - 2(2) & 6 - 2(3) \end{pmatrix} = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix}
$$

The resulting matrix $A'$ is:

$$
A' = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{pmatrix}
$$

Because matrix $A'$ contains an entire row consisting strictly of zeros ($R_2 = [0, 0, 0]$), expanding along this zero row yields:

$$
\det A = \det A' = 0 \cdot C_{21} + 0 \cdot C_{22} + 0 \cdot C_{23} = 0
$$

Thus, without computing a full determinant expansion, the existence of linearly dependent rows guarantees that $\det A = 0$.[cite: 1]

---

#### Step 3: Connecting Linear Dependence to Non-Invertibility

##### 1. Loss of Matrix Rank
* An $n \times n$ matrix is invertible if and only if its rows (and columns) span an $n$-dimensional space, meaning all $n$ rows are linearly independent ($\text{rank}(A) = n$).
* In matrix $A$, because $R_2 = 2 R_1$, Row 2 contributes no new spatial direction. The set $\{R_1, R_2, R_3\}$ spans only a 2D plane in $\mathbb{R}^3$ rather than full $3\text{D}$ space.
* Therefore, $\text{rank}(A) = 2 < 3$, meaning $A$ is rank-deficient (singular).

##### 2. The Invertible Matrix Theorem
By the **Invertible Matrix Theorem**, the following statements are logically equivalent for any square matrix $A$:
1. Matrix $A$ is invertible ($A^{-1}$ exists).
2. The determinant of $A$ is non-zero ($\det A \neq 0$).
3. The rows of $A$ are linearly independent.
4. The linear system $A x = 0$ has only the trivial solution $x = 0$.

Since the rows of $A$ are linearly dependent, Statement 3 is false, which implies that Statement 2 ($\det A \neq 0$) and Statement 1 ($A$ is invertible) are also false.

Hence, matrix $A$ is **not invertible** (singular).[cite: 1]

---

### Conclusion and Key Takeaways

1. **Specific Dependence Identified:**
   $$R_2 = 2 R_1$$
   Row 2 is twice Row 1.[cite: 1]

2. **Determinant Verdict:**
   $$\det A = 0$$
   (Guaranteed because proportional rows produce a row of zeros under elementary row operations).[cite: 1]

3. **Invertibility Status:**
   Matrix $A$ is **not invertible** because linear dependence reduces its rank below full rank ($\text{rank}(A) = 2 < 3$), resulting in a zero determinant.[cite: 1]