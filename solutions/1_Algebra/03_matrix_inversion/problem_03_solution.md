# Exercise 3 – When Does the Inverse Not Exist?

## Problem Statement

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## Solution

### 1. Explanation Using the Determinant

For a $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is given by:

$$
\det(A) = ad - bc
$$

Calculating the determinant of matrix $A$:

$$
\det(A) = (2)(2) - (4)(1)
$$

$$
\det(A) = 4 - 4 = 0
$$

A matrix is invertible if and only if its determinant is non-zero ($\det(A) \neq 0$). Since $\det(A) = 0$, matrix $A$ is singular and its inverse $A^{-1}$ does not exist.

### 2. Explanation Using Linear Dependence of Rows

Let the rows of matrix $A$ be represented as row vectors:

$$
r_1 = \begin{pmatrix} 2 & 4 \end{pmatrix}
$$

$$
r_2 = \begin{pmatrix} 1 & 2 \end{pmatrix}
$$

We observe that row 1 is an exact scalar multiple of row 2:

$$
r_1 = 2 r_2
$$

Since one row can be expressed as a linear combination of the other, the rows of matrix $A$ are linearly dependent. Linear dependence means the matrix collapses dimensions and does not have full rank ($\text{rank}(A) = 1 < 2$), which guarantees that $A^{-1}$ cannot exist.

### Verification

We verify non-invertibility by attempting to solve $A x = 0$ for a non-zero vector $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$:

$$
\begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}
$$

This system yields the single linear equation $x_1 + 2x_2 = 0$. Setting $x_2 = 1$ gives $x_1 = -2$, producing a non-zero solution vector:

$$
x = \begin{pmatrix} -2 \\ 1 \end{pmatrix} \neq \begin{pmatrix} 0 \\ 0 \end{pmatrix}
$$

Since the null space contains non-trivial solutions ($\ker(A) \neq \{0\}$), matrix $A$ cannot be inverted.