
# Exercise 6 – Transpose

## Problem Statement

Calculate $A^T$, $B^T$, and $AB$. Verify that $(AB)^T = B^TA^T$.

## Solution

Given:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
\qquad
B = \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3
\end{pmatrix}
$$

### 1. Calculate the Transposes

Swap the rows and columns of each matrix.

$$
A^T = \begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}
$$

$$
B^T = \begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3
\end{pmatrix}
$$

### 2. Calculate AB

$$
AB =
\begin{pmatrix}
1(1)+2(2)+3(-1) & 1(0)+2(1)+3(3) \\
4(1)+5(2)+6(-1) & 4(0)+5(1)+6(3)
\end{pmatrix}
$$

$$
AB = \begin{pmatrix}
2 & 11 \\
8 & 23
\end{pmatrix}
$$

### 3. Verify the Transpose Property

First, calculate the transpose of AB:

$$
(AB)^T = \begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
$$

Now calculate $B^TA^T$:

$$
B^TA^T =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}
$$

$$
B^TA^T =
\begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
$$

## Explanation

The transpose of a matrix is obtained by exchanging its rows and columns.

When taking the transpose of a matrix product, the order of multiplication is reversed:

$$
(AB)^T = B^TA^T
$$

## Verification

Both calculations produce the same matrix:

$$
(AB)^T = B^TA^T =
\begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
$$

Therefore, the property is verified.

## Final Answer

$$
\boxed{
A^T = \begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}
}
$$

$$
\boxed{
B^T = \begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3
\end{pmatrix}
}
$$

$$
\boxed{
AB = \begin{pmatrix}
2 & 11 \\
8 & 23
\end{pmatrix}
}
$$

$$
\boxed{(AB)^T = B^TA^T}
$$
