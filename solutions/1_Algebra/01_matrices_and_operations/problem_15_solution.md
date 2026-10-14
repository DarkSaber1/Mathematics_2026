
# Exercise 15 – Associativity of Multiplication

## Problem Statement

Calculate $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain the associativity of matrix multiplication.

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
1 & 0 \\
2 & 1 \\
-1 & 3
\end{pmatrix}
$$

$$
C =
\begin{pmatrix}
2 & 1 \\
0 & -1
\end{pmatrix}
$$

### 1. Calculate (AB)C

First, calculate AB:

$$
AB =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
5 & 2 \\
1 & 4
\end{pmatrix}
$$

Now multiply AB by C:

$$
(AB)C =
\begin{pmatrix}
5 & 2 \\
1 & 4
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1
\end{pmatrix}
$$

$$
(AB)C =
\begin{pmatrix}
10 & 3 \\
2 & -3
\end{pmatrix}
$$

### 2. Calculate A(BC)

First, calculate BC:

$$
BC =
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1
\end{pmatrix}
$$

$$
BC =
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4
\end{pmatrix}
$$

Now multiply A by BC:

$$
A(BC) =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4
\end{pmatrix}
$$

$$
A(BC) =
\begin{pmatrix}
10 & 3 \\
2 & -3
\end{pmatrix}
$$

### 3. Compare Calculation Paths

Both methods give the same result.

Counting scalar multiplications:

- (AB)C requires 12 + 8 = 20 multiplications.
- A(BC) requires 12 + 12 = 24 multiplications.

Therefore, (AB)C requires fewer scalar multiplications.

## Explanation

Matrix multiplication is associative. This means that changing the grouping of matrices does not change the final result.

However, different calculation paths may require different numbers of operations.

## Verification

Both methods produce the same matrix:

$$
(AB)C =
\begin{pmatrix}
10 & 3 \\
2 & -3
\end{pmatrix}
$$

$$
A(BC) =
\begin{pmatrix}
10 & 3 \\
2 & -3
\end{pmatrix}
$$

Therefore:

$$
(AB)C = A(BC)
$$

## Final Answer

$$
\boxed{
(AB)C = A(BC) =
\begin{pmatrix}
10 & 3 \\
2 & -3
\end{pmatrix}
}
$$

Matrix multiplication is associative, and (AB)C is more efficient for these matrices.
