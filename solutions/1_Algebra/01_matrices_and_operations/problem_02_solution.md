
# Exercise 2 – Addition and Scalar Multiplication

## Problem Statement

Given matrices A and B, calculate A+B, A-B, and 3A-2B.

## Solution

Given:

$$
A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}
\qquad
B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}
$$

### 1. Matrix Addition (A+B)

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

### 2. Matrix Subtraction (A-B)

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

### 3. Scalar Multiplication (3A-2B)

$$
3A = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}
$$

$$
2B = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
$$

Therefore:

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

## Explanation

Matrix addition and subtraction are performed element by element.

Addition is only possible when both matrices have the same dimensions, because every element must have a corresponding element in the other matrix.

Scalar multiplication means multiplying every entry by the given number.

## Verification

Both matrices are 2x2, so addition and subtraction are valid.

We can check the last result using:

$$
3A-2B = A+2(A-B)
$$

$$
= \begin{pmatrix}1&2\\-1&3\end{pmatrix}
+2\begin{pmatrix}-3&4\\-1&-2\end{pmatrix}
= \begin{pmatrix}-5&10\\-3&-1\end{pmatrix}
$$

The result matches.

## Final Answer

$$
\boxed{A+B=\begin{pmatrix}5&0\\-1&8\end{pmatrix}}
$$

$$
\boxed{A-B=\begin{pmatrix}-3&4\\-1&-2\end{pmatrix}}
$$

$$
\boxed{3A-2B=\begin{pmatrix}-5&10\\-3&-1\end{pmatrix}}
$$
