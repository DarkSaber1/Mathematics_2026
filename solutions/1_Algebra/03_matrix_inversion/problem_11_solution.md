# Exercise 11 – Inverse of Triangular Matrices and LU Decomposition

## Problem Statement

Let

$$
L=
\begin{pmatrix}
1 & 0 \\
2 & 1
\end{pmatrix},\qquad U=
\begin{pmatrix}
3 & 1 \\
0 & 2
\end{pmatrix}
$$

1. Compute $L^{-1}$ and $U^{-1}$.
2. Compute $A = LU$ and find $A^{-1}$ directly using the inverse formula.
3. Verify that $(LU)^{-1} = U^{-1}L^{-1}$.

## Solution

### 1. Calculation of $L^{-1}$ and $U^{-1}$

- **For matrix $L$:**

$$
\det(L) = (1)(1) - (0)(2) = 1
$$

Using the $2 \times 2$ inverse formula:

$$
L^{-1} = \frac{1}{1} \begin{pmatrix} 1 & 0 \\ -2 & 1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ -2 & 1 \end{pmatrix}
$$

- **For matrix $U$:**

$$
\det(U) = (3)(2) - (1)(0) = 6
$$

Using the $2 \times 2$ inverse formula:

$$
U^{-1} = \frac{1}{6} \begin{pmatrix} 2 & -1 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} \frac{1}{3} & -\frac{1}{6} \\ 0 & \frac{1}{2} \end{pmatrix}
$$

### 2. Computation of $A = LU$ and Direct Inverse $A^{-1}$

First, we calculate the product matrix $A$:

$$
A = LU = \begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 0 & 2 \end{pmatrix}
$$

$$
A = \begin{pmatrix} 1(3) + 0(0) & 1(1) + 0(2) \\ 2(3) + 1(0) & 2(1) + 1(2) \end{pmatrix} = \begin{pmatrix} 3 & 1 \\ 6 & 4 \end{pmatrix}
$$

Next, we find $A^{-1}$ directly. The determinant of $A$ is:

$$
\det(A) = (3)(4) - (1)(6) = 12 - 6 = 6
$$

Using the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{6} \begin{pmatrix} 4 & -1 \\ -6 & 3 \end{pmatrix} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{6} \\ -1 & \frac{1}{2} \end{pmatrix}
$$

### 3. Verification of $(LU)^{-1} = U^{-1}L^{-1}$

We compute $U^{-1}L^{-1}$:

$$
U^{-1}L^{-1} = \begin{pmatrix} \frac{1}{3} & -\frac{1}{6} \\ 0 & \frac{1}{2} \end{pmatrix} \begin{pmatrix} 1 & 0 \\ -2 & 1 \end{pmatrix}
$$

$$
U^{-1}L^{-1} = \begin{pmatrix} \frac{1}{3}(1) + \left(-\frac{1}{6}\right)(-2) & \frac{1}{3}(0) + \left(-\frac{1}{6}\right)(1) \\ 0(1) + \frac{1}{2}(-2) & 0(0) + \frac{1}{2}(1) \end{pmatrix}
$$

$$
U^{-1}L^{-1} = \begin{pmatrix} \frac{1}{3} + \frac{1}{3} & -\frac{1}{6} \\ 0 - 1 & \frac{1}{2} \end{pmatrix} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{6} \\ -1 & \frac{1}{2} \end{pmatrix}
$$

### Verification

Comparing the results:

$$
A^{-1} = (LU)^{-1} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{6} \\ -1 & \frac{1}{2} \end{pmatrix} = U^{-1}L^{-1}
$$

Both methods produce the identical inverse matrix, confirming that $(LU)^{-1} = U^{-1}L^{-1}$.