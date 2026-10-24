## Exercise 4. Triangular Matrix

### Problem Definition
Given the $3 \times 3$ matrix:[cite: 1]

$$
T = \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}
$$

1. Without performing full expansion (such as Sarrus' Rule or general cofactor expansion), compute $\det T$.[cite: 1]
2. State the general rule for computing the determinant of an arbitrary triangular matrix.[cite: 1]
3. Provide a clear mathematical explanation of why this rule holds, using this specific example.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Identifying the Matrix Structure

Observe the structure of the given matrix:

$$
T = \begin{pmatrix} 
2 & 4 & 1 \\ 
0 & -3 & 5 \\ 
0 & 0 & 7 
\end{pmatrix}
$$

* The entries strictly below the main diagonal (namely $t_{21} = 0$, $t_{31} = 0$, and $t_{32} = 0$) are all equal to zero.
* Therefore, $T$ is an **upper triangular matrix**.

---

#### Step 2: Direct Computation using the Triangular Matrix Property

**Property of Triangular Matrices:**
> The determinant of any upper triangular, lower triangular, or diagonal matrix is simply the product of the entries located on its main diagonal.[cite: 1]

Identifying the main diagonal entries of $T$:
* $t_{11} = 2$
* $t_{22} = -3$
* $t_{33} = 7$

Applying the product rule directly:[cite: 1]

$$
\det T = t_{11} \cdot t_{22} \cdot t_{33} = (2) \cdot (-3) \cdot (7)
$$

Calculating the product step-by-step:
1. First product: $2 \cdot (-3) = -6$
2. Second product: $(-6) \cdot 7 = -42$

Thus:

$$
\det T = -42
$$

---

#### Step 3: General Rule for an Arbitrary Triangular Matrix

##### General Formulation
Let $A = (a_{ij})$ be an $n \times n$ square matrix that is either **upper triangular** ($a_{ij} = 0$ for $i > j$), **lower triangular** ($a_{ij} = 0$ for $i < j$), or **diagonal** ($a_{ij} = 0$ for $i \neq j$). 

The determinant of $A$ is given by:

$$
\det A = \prod_{i=1}^{n} a_{ii} = a_{11} \cdot a_{22} \cdot a_{33} \cdots a_{nn}
$$

##### Types of Triangular Matrices
* **Upper Triangular Matrix:** All entries below the main diagonal are zero.
  $$
  \det \begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ 0 & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & a_{nn} \end{pmatrix} = a_{11} \cdot a_{22} \cdots a_{nn}
  $$

* **Lower Triangular Matrix:** All entries above the main diagonal are zero.
  $$
  \det \begin{pmatrix} a_{11} & 0 & \cdots & 0 \\ a_{21} & a_{22} & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nn} \end{pmatrix} = a_{11} \cdot a_{22} \cdots a_{nn}
  $$

* **Diagonal Matrix:** All non-diagonal entries are zero.
  $$
  \det \begin{pmatrix} a_{11} & 0 & \cdots & 0 \\ 0 & a_{22} & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & a_{nn} \end{pmatrix} = a_{11} \cdot a_{22} \cdots a_{nn}
  $$

---

#### Step 4: Mathematical Explanation / Proof Using the Example

To understand **why** this rule works, we perform Laplace cofactor expansion on our $3 \times 3$ matrix $T$ step-by-step along the first column ($C_1$), where all elements below $t_{11}$ are zero.

##### Step A: Expand along Column 1 ($C_1$)

The expansion formula along $C_1 = \begin{pmatrix} 2 \\ 0 \\ 0 \end{pmatrix}$ is:

$$
\det T = t_{11} C_{11} + t_{21} C_{21} + t_{31} C_{31}
$$

Since $t_{21} = 0$ and $t_{31} = 0$, the second and third terms vanish completely:

$$
\det T = 2 \cdot C_{11} + 0 + 0 = 2 \cdot (-1)^{1+1} \cdot \det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}
$$

$$
\det T = 2 \cdot 1 \cdot \det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}
$$

Notice that the remaining $2 \times 2$ submatrix $\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}$ is also upper triangular!

##### Step B: Compute the $2 \times 2$ Determinant

Using the standard formula for a $2 \times 2$ determinant:

$$
\det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} = ((-3) \cdot 7) - (5 \cdot 0) = -21 - 0 = -21
$$

Notice that the term $5 \cdot 0$ vanishes because $t_{32} = 0$. This leaves only the product of the diagonal entries of the $2 \times 2$ submatrix: $(-3) \cdot 7$.

##### Step C: Combine the Factors

Substituting this back into our expression for $\det T$:

$$
\det T = 2 \cdot [(-3) \cdot 7] = 2 \cdot (-3) \cdot 7 = -42
$$

This inductive process demonstrates why all non-diagonal off-axis terms drop out, leaving strictly the product of the main diagonal elements.

---

### Conclusion and Key Takeaways

1. **Calculated Determinant:**
   $$\det T = -42$$

2. **Core Takeaway:**
   For any triangular matrix (upper or lower), you never need to perform a full expansion—simply multiply the diagonal elements together.