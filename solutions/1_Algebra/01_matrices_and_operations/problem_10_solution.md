
# Exercise 10 – Columns of a Matrix Product

## Problem Statement

Calculate Ab₁, Ab₂, and AB. Explain why the columns of AB are equal to Ab₁ and Ab₂.

## Solution

Given:

$$
A = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix},
\quad
B = \begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1
\end{pmatrix}
$$

The columns of B are:

$$
b_1 = \begin{pmatrix}1\\-1\\3\end{pmatrix},
\quad
b_2 = \begin{pmatrix}2\\0\\1\end{pmatrix}
$$

### 1. Calculate Ab₁

$$
Ab_1 =
\begin{pmatrix}
1(1)+2(-1)+0(3)\\
0(1)+1(-1)+1(3)
\end{pmatrix}
=
\begin{pmatrix}-1\\2\end{pmatrix}
$$

### 2. Calculate Ab₂

$$
Ab_2 =
\begin{pmatrix}
1(2)+2(0)+0(1)\\
0(2)+1(0)+1(1)
\end{pmatrix}
=
\begin{pmatrix}2\\1\end{pmatrix}
$$

### 3. Calculate AB

$$
AB =
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 2\\
-1 & 0\\
3 & 1
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
-1 & 2\\
2 & 1
\end{pmatrix}
$$

## Explanation

When multiplying matrices A and B, each column of B is multiplied separately by A.

Therefore, the columns of AB are exactly the vectors Ab₁ and Ab₂.

## Verification

We obtained:

$$
Ab_1 = \begin{pmatrix}-1\\2\end{pmatrix},
\quad
Ab_2 = \begin{pmatrix}2\\1\end{pmatrix}
$$

Combining these vectors as columns:

$$
AB = \begin{pmatrix}-1&2\\2&1\end{pmatrix}
$$

This matches the matrix multiplication result.

## Final Answer

$$
\boxed{Ab_1 = \begin{pmatrix}-1\\2\end{pmatrix}}
$$

$$
\boxed{Ab_2 = \begin{pmatrix}2\\1\end{pmatrix}}
$$

$$
\boxed{AB = \begin{pmatrix}-1&2\\2&1\end{pmatrix}}
$$
