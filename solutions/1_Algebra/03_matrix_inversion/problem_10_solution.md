# Exercise 10 – Inverse of a Diagonal Matrix

## Problem Statement

Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5
\end{pmatrix}
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## Solution

### 1. Invertibility Decision Without Gauss–Jordan Elimination

A diagonal matrix is invertible if and only if **all of its diagonal elements are non-zero**.

- **Matrix $D$:** The diagonal entries are $2$, $-3$, and $5$. Since none of these diagonal entries are zero ($\det(D) = 2 \cdot (-3) \cdot 5 = -30 \neq 0$), **matrix $D$ is invertible**.
- **Matrix $E$:** The second diagonal entry is $0$. This creates an entire zero row/column, making the determinant zero ($\det(E) = 2 \cdot 0 \cdot 5 = 0$). Therefore, **matrix $E$ is singular (not invertible)**.

### 2. Inverse of Diagonal Matrix $D$

The inverse of an invertible diagonal matrix is formed simply by replacing each diagonal entry with its reciprocal:

$$
D^{-1} =
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}
$$

### 3. Verification by Matrix Multiplication

We verify the result by computing $D D^{-1}$:

$$
D D^{-1} =
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}
$$

- **Top-left entry $(1,1)$:** $2\left(\frac{1}{2}\right) + 0 + 0 = 1$
- **Middle entry $(2,2)$:** $(-3)\left(-\frac{1}{3}\right) + 0 + 0 = 1$
- **Bottom-right entry $(3,3)$:** $5\left(\frac{1}{5}\right) + 0 + 0 = 1$
- **Off-diagonal entries:** All produce zeros.

$$
D D^{-1} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = I_3
$$

Since $D D^{-1} = I_3$, the inverse matrix $D^{-1}$ is verified to be correct.