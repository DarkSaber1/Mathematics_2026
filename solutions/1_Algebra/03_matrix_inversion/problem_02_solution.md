# Exercise 2 – Formula for a 2×2 Matrix

## Problem Statement

Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

## Solution

### 1. Determinant Calculation

For a $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is calculated as:

$$
\det(A) = ad - bc
$$

Substituting the entries of matrix $A$:

$$
\det(A) = (3)(4) - (2)(5)
$$

$$
\det(A) = 12 - 10 = 2
$$

Since $\det(A) = 2 \neq 0$, the inverse matrix $A^{-1}$ exists.

### 2. Applying the $2 \times 2$ Inverse Formula

The explicit formula for the inverse of a $2 \times 2$ matrix is:

$$
A^{-1} = \frac{1}{\det(A)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}
$$

Substituting $\det(A) = 2$ and swapping/negating the entries:

$$
A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix}
$$

$$
A^{-1} = \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
$$

### 3. Verification by Matrix Product

We verify the result by computing the product $A A^{-1}$:

$$
A A^{-1} = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
$$

- **Top-left entry $(1,1)$:**

$$
3(2) + 2\left(-\frac{5}{2}\right) = 6 - 5 = 1
$$

- **Top-right entry $(1,2)$:**

$$
3(-1) + 2\left(\frac{3}{2}\right) = -3 + 3 = 0
$$

- **Bottom-left entry $(2,1)$:**

$$
5(2) + 4\left(-\frac{5}{2}\right) = 10 - 10 = 0
$$

- **Bottom-right entry $(2,2)$:**

$$
5(-1) + 4\left(\frac{3}{2}\right) = -5 + 6 = 1
$$

Combining the entries gives:

$$
A A^{-1} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I
$$

Since $A A^{-1} = I$, the calculated inverse $A^{-1}$ is verified to be correct.