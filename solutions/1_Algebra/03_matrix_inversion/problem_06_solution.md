# Exercise 6 – Solving a System Using the Inverse

## Problem Statement

Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

## Solution

### 1. Calculation of the Inverse Matrix $A^{-1}$

For a $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is:

$$
\det(A) = ad - bc = (2)(3) - (1)(1) = 6 - 1 = 5
$$

Since $\det(A) = 5 \neq 0$, the matrix is invertible. Using the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{\det(A)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}
$$

### 2. Computing the Solution Vector $x = A^{-1}b$

Multiplying $A^{-1}$ by vector $b$:

$$
x = A^{-1}b = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 5 \\ 7 \end{pmatrix}
$$

$$
x = \frac{1}{5} \begin{pmatrix} 3(5) + (-1)(7) \\ -1(5) + 2(7) \end{pmatrix}
$$

$$
x = \frac{1}{5} \begin{pmatrix} 15 - 7 \\ -5 + 14 \end{pmatrix}
$$

$$
x = \frac{1}{5} \begin{pmatrix} 8 \\ 9 \end{pmatrix} = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}
$$

### Explanation

Multiplying both sides of the matrix equation $Ax = b$ from the left by $A^{-1}$ isolates the unknown vector $x$:

$$
A^{-1}(Ax) = A^{-1}b \implies (A^{-1}A)x = A^{-1}b \implies Ix = A^{-1}b \implies x = A^{-1}b
$$

This approach allows direct computation of the solution vector using the inverse matrix.

### Verification by Substitution

We substitute the calculated vector $x = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}$ back into $Ax$:

$$
Ax = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}
$$

- **First entry:**

$$
2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) = \frac{16}{5} + \frac{9}{5} = \frac{25}{5} = 5
$$

- **Second entry:**

$$
1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) = \frac{8}{5} + \frac{27}{5} = \frac{35}{5} = 7
$$

Combining the entries gives:

$$
Ax = \begin{pmatrix} 5 \\ 7 \end{pmatrix} = b
$$

Since $Ax = b$, the solution $x = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}$ is verified to be correct.