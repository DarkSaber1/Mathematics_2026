# Exercise 15 – Two Methods for Solving the Same System

## Problem Statement

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Solution

### 1. Method 1: Solving via $x = A^{-1}b$

- **Step 1: Compute the determinant of $A$:**

$$
\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5
$$

- **Step 2: Find $A^{-1}$ using the $2 \times 2$ inverse formula:**

$$
A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}
$$

- **Step 3: Multiply $A^{-1}b$ to find $x$:**

$$
x = A^{-1}b = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 7 \\ 8 \end{pmatrix}
$$

$$
x = \frac{1}{5} \begin{pmatrix} 3(7) + (-1)(8) \\ -1(7) + 2(8) \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 21 - 8 \\ -7 + 16 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 13 \\ 9 \end{pmatrix} = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}
$$

---

### 2. Method 2: Solving via Gaussian Elimination

- **Step 1: Form the augmented matrix $[A \mid b]$:**

$$
[A \mid b] = \left(\begin{array}{cc|c} 2 & 1 & 7 \\ 1 & 3 & 8 \end{array}\right)
$$

- **Step 2: Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$) to obtain a leading pivot of $1$:**

$$
\left(\begin{array}{cc|c} 1 & 3 & 8 \\ 2 & 1 & 7 \end{array}\right)
$$

- **Step 3: Eliminate the first entry in Row 2 by performing $R_2 \leftarrow R_2 - 2R_1$:**

$$
R_2 \text{ calculation: } (2, 1, 7) - 2(1, 3, 8) = (0, -5, -9)
$$

$$
\left(\begin{array}{cc|c} 1 & 3 & 8 \\ 0 & -5 & -9 \end{array}\right)
$$

- **Step 4: Solve via back-substitution:**
  - From Row 2:

$$
-5y = -9 \implies y = \frac{9}{5}
$$

  - From Row 1:

$$
x + 3y = 8 \implies x + 3\left(\frac{9}{5}\right) = 8 \implies x + \frac{27}{5} = \frac{40}{5} \implies x = \frac{13}{5}
$$

Thus, the solution vector is:

$$
x = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}
$$

---

### 3. Comparison of Methods

- **Agreement of Solutions:**  
  Both methods yield the exact same unique solution vector:

$$
x = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}
$$

- **Number of Essential Steps:**
  - **Method 1 ($A^{-1}b$):** Requires 3 main stages—computing $\det(A)$, constructing $A^{-1}$, and performing the matrix-vector multiplication $A^{-1}b$.
  - **Method 2 (Gaussian Elimination):** Requires 3 main stages—setting up the augmented matrix $[A \mid b]$, performing one row elimination step to reach row echelon form, and executing back-substitution.

- **Which Method Was Simpler:**  
  **Gaussian elimination** was simpler and more efficient in this example. Because the system only involves a **single** right-hand side vector $b$, computing the full inverse matrix $A^{-1}$ does extra unnecessary work (finding $A^{-1}$ is equivalent to solving two systems simultaneously for the columns of $I_2$). Gaussian elimination reaches the solution directly with fewer multiplications and avoids introducing fractions until the final back-substitution step.