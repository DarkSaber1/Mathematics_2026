
# Exercise 10 – Columns of a Matrix Product

## Problem Statement

Calculate $Ab_1$, $Ab_2$, and $AB$. Explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

Given:

$$
A =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix}
$$

$$
B =
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1
\end{pmatrix}
$$

The columns of B are:

$$
b_1 =
\begin{pmatrix}
1 \\
-1 \\
3
\end{pmatrix}
$$

$$
b_2 =
\begin{pmatrix}
2 \\
0 \\
1
\end{pmatrix}
$$

### 1. Calculate Ab₁

$$
Ab_1 =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3
\end{pmatrix}
$$

$$
Ab_1 =
\begin{pmatrix}
1(1)+2(-1)+0(3) \\
0(1)+1(-1)+1(3)
\end{pmatrix}
$$

$$
Ab_1 =
\begin{pmatrix}
-1 \\
2
\end{pmatrix}
$$

### 2. Calculate Ab₂

$$
Ab_2 =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1
\end{pmatrix}
$$

$$
Ab_2 =
\begin{pmatrix}
1(2)+2(0)+0(1) \\
0(2)+1(0)+1(1)
\end{pmatrix}
$$

$$
Ab_2 =
\begin{pmatrix}
2 \\
1
\end{pmatrix}
$$

### 3. Calculate AB

$$
AB =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
1(1)+2(-1)+0(3) & 1(2)+2(0)+0(1) \\
0(1)+1(-1)+1(3) & 0(2)+1(0)+1(1)
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
-1 & 2 \\
2 & 1
\end{pmatrix}
$$

## Explanation

Matrix multiplication can be performed by multiplying matrix A by each column of matrix B separately.

The resulting vectors become the columns of the product AB.

Therefore:

$$
AB =
\begin{pmatrix}
Ab_1 & Ab_2
\end{pmatrix}
$$

## Verification

We calculated:

$$
Ab_1 =
\begin{pmatrix}
-1 \\
2
\end{pmatrix}
$$

$$
Ab_2 =
\begin{pmatrix}
2 \\
1
\end{pmatrix}
$$

Combining these vectors as columns gives:

$$
AB =
\begin{pmatrix}
-1 & 2 \\
2 & 1
\end{pmatrix}
$$

This matches the result obtained by direct matrix multiplication.

## Final Answer

$$
\boxed{
Ab_1 =
\begin{pmatrix}
-1 \\
2
\end{pmatrix}
}
$$

$$
\boxed{
Ab_2 =
\begin{pmatrix}
2 \\
1
\end{pmatrix}
}
$$

$$
\boxed{
AB =
\begin{pmatrix}
-1 & 2 \\
2 & 1
\end{pmatrix}
}
$$
