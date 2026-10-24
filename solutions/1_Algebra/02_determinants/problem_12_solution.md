## Exercise 12. A Parameter Revealed by a Row Operation

### Problem Definition
Given the $3 \times 3$ matrix depending on parameter $t$:[cite: 1]

$$
A(t) = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & t \\ 0 & 1 & 1 \end{pmatrix}
$$

1. Before computing the full determinant, perform the row operation $R_2 \leftarrow R_2 - 2 R_1$ and analyze the resulting matrix structure.[cite: 1]
2. Compute $\det A(t)$ using the simplified matrix structure.[cite: 1]
3. Find all values of $t$ for which matrix $A(t)$ is **not invertible**.[cite: 1]
4. Explain what special relationship occurs among the rows of $A(t)$ for the parameter value you found.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Performing the Prescribed Row Operation

We begin with matrix $A(t)$:[cite: 1]

$$
A(t) = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & t \\ 0 & 1 & 1 \end{pmatrix}
$$

##### Applying $R_2 \leftarrow R_2 - 2 R_1$
* **Row 2:** $[2,\; 4,\; t]$
* **$2 \times$ Row 1:** $2 \cdot [1,\; 2,\; 3] = [2,\; 4,\; 6]$
* **Subtracting:**
  $$
  R_2 - 2 R_1 = [2 - 2,\; 4 - 4,\; t - 6] = [0,\; 0,\; t - 6]
  $$

The transformed matrix $A'(t)$ is:[cite: 1]

$$
A'(t) = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & t - 6 \\ 0 & 1 & 1 \end{pmatrix}
$$

##### Effect on the Determinant
Because adding a scalar multiple of one row to another row does not change the value of the determinant, we have:[cite: 1]

$$
\det A(t) = \det A'(t)
$$

---

#### Step 2: Computing $\det A(t)$ from the Simplified Matrix Structure

Notice the structure of $A'(t)$:
* Row 2 now has two zeros: $[0,\; 0,\; t - 6]$.
* Column 1 also has two zeros: $\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$.

We can easily compute $\det A'(t)$ using two alternative, simple methods:

##### Method A: Laplace Expansion along Column 1
Expanding along Column 1 of matrix $A'(t)$:

$$
\det A'(t) = 1 \cdot (-1)^{1+1} \cdot \det \begin{pmatrix} 0 & t - 6 \\ 1 & 1 \end{pmatrix} + 0 + 0
$$

Calculate the $2 \times 2$ determinant:

$$
\det \begin{pmatrix} 0 & t - 6 \\ 1 & 1 \end{pmatrix} = (0 \cdot 1) - ((t - 6) \cdot 1) = 0 - (t - 6) = 6 - t
$$

Thus:

$$
\det A(t) = 6 - t
$$

##### Method B: Laplace Expansion along Row 2
Expanding along Row 2 of matrix $A'(t)$:

$$
\det A'(t) = (t - 6) \cdot C_{23} = (t - 6) \cdot (-1)^{2+3} \cdot \det \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
$$

$$
\det A'(t) = (t - 6) \cdot (-1) \cdot ((1 \cdot 1) - (2 \cdot 0)) = (t - 6) \cdot (-1) \cdot (1) = -(t - 6) = 6 - t
$$

Both expansion methods give:

$$
\det A(t) = 6 - t
$$

---

#### Step 3: Finding Parameter Values for Non-Invertibility

##### Invertibility Criterion
A square matrix $A(t)$ is **not invertible** (singular) if and only if its determinant is zero:[cite: 1]

$$
A(t) \text{ is not invertible} \iff \det A(t) = 0
$$

##### Solving for $t$
Set $\det A(t) = 0$:[cite: 1]

$$
6 - t = 0 \implies t = 6
$$

Thus, matrix $A(t)$ is **not invertible** if and only if $t = 6$.[cite: 1]

---

#### Step 4: Explanation of the Special Row Structure at $t = 6$

Substitute $t = 6$ back into the original matrix $A(t)$:[cite: 1]

$$
A(6) = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 1 \end{pmatrix}
$$

Let us inspect the rows of $A(6)$:
* $R_1 = [1,\; 2,\; 3]$
* $R_2 = [2,\; 4,\; 6]$
* $R_3 = [0,\; 1,\; 1]$

##### What happens special to the rows:
1. **Direct Proportionality:** Row 2 is an exact scalar multiple of Row 1:
   $$
   R_2 = 2 \cdot R_1 \implies [2,\; 4,\; 6] = 2 \cdot [1,\; 2,\; 3]
   $$
2. **Creation of a Zero Row:** When performing the operation $R_2 \leftarrow R_2 - 2 R_1$ on $A(6)$, Row 2 becomes entirely zero:[cite: 1]
   $$
   R_2 - 2 R_1 = [2 - 2,\; 4 - 4,\; 6 - 6] = [0,\; 0,\; 0]
   $$
3. **Linear Dependence:** The set of row vectors $\{R_1, R_2, R_3\}$ is linearly dependent because $R_2 - 2 R_1 + 0 R_3 = 0$. This linear dependency reduces the matrix rank ($\text{rank}(A(6)) = 2 < 3$), making it impossible to invert matrix $A(6)$.[cite: 1]

---

### Conclusion and Key Takeaways

1. **Determinant Formula:**
   $$\det A(t) = 6 - t$$

2. **Non-Invertibility Condition:**
   Matrix $A(t)$ is not invertible when **$t = 6$**.[cite: 1]

3. **Special Row Property at $t = 6$:**
   When $t = 6$, Row 2 is exactly twice Row 1 ($R_2 = 2 R_1$), causing the row operation $R_2 \leftarrow R_2 - 2 R_1$ to generate a row of zeros and proving linear dependence.[cite: 1]