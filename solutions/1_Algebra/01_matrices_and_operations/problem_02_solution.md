# Exercise 2 – Addition and Scalar Multiplication

## Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

## Solution

### 1. Calculation of $A+B$

Matrix addition is performed entry-by-entry:

$$
A+B =
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5
\end{pmatrix}
=
\begin{pmatrix}
5 & 0 \\
-1 & 8
\end{pmatrix}
$$

### 2. Calculation of $A-B$

Matrix subtraction is performed entry-by-entry:

$$
A-B =
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5
\end{pmatrix}
=
\begin{pmatrix}
-3 & 4 \\
-1 & -2
\end{pmatrix}
$$

### 3. Calculation of $3A-2B$

First, multiply matrix $A$ by the scalar 3 and matrix $B$ by the scalar 2:

$$
3A =
\begin{pmatrix}
3(1) & 3(2) \\
3(-1) & 3(3)
\end{pmatrix}
=
\begin{pmatrix}
3 & 6 \\
-3 & 9
\end{pmatrix}
$$

$$
2B =
\begin{pmatrix}
2(4) & 2(-2) \\
2(0) & 2(5)
\end{pmatrix}
=
\begin{pmatrix}
8 & -4 \\
0 & 10
\end{pmatrix}
$$

Now subtract $2B$ from $3A$:

$$
3A-2B =
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10
\end{pmatrix}
=
\begin{pmatrix}
-5 & 10 \\
-3 & -1
\end{pmatrix}
$$

### 4. Explanation: Compatibility of Dimensions

Matrix addition and subtraction are defined element-wise, meaning the entry at position $(i, j)$ in the resulting matrix is computed as $a_{ij} + b_{ij}$. If two matrices have different dimensions, at least one entry will not have a corresponding entry in the other matrix, making element-wise addition impossible.

### Verification

Since both $A$ and $B$ have dimensions $2 \times 2$, addition and scalar multiplication are fully defined. We can algebraically verify $3A-2B$ using the identity $3A-2B = A + 2(A-B)$:

$$
A + 2(A-B) =
\begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}
+ 2
\begin{pmatrix}
-3 & 4 \\
-1 & -2
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}
+
\begin{pmatrix}
-6 & 8 \\
-2 & -4
\end{pmatrix}
=
\begin{pmatrix}
-5 & 10 \\
-3 & -1
\end{pmatrix}
$$

The verification confirms that the calculation for $3A-2B$ is correct.