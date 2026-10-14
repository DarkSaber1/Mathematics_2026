
# Exercise 7 – Identity Matrix, Zero Matrix, and Powers

## Problem Statement

Given matrix A, calculate AI, IA, A+0, A², and A³. Explain the roles of the identity and zero matrices and describe the pattern in the powers of A.

## Solution

Given:

$$
A = \begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

### 1. Identity and Zero Matrices

The identity and zero matrices are:

$$
I = \begin{pmatrix}1&0\\0&1\end{pmatrix},
\qquad
0 = \begin{pmatrix}0&0\\0&0\end{pmatrix}
$$

Multiplying by the identity matrix:

$$
AI = IA =
\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

Adding the zero matrix:

$$
A+0 =
\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

### 2. Calculate A²

$$
A^2 = A \cdot A
$$

$$
A^2 =
\begin{pmatrix}
2(2)+1(0) & 2(1)+1(2) \\
0(2)+2(0) & 0(1)+2(2)
\end{pmatrix}
$$

$$
A^2 = \begin{pmatrix}4&4\\0&4\end{pmatrix}
$$

### 3. Calculate A³

$$
A^3 = A^2 \cdot A
$$

$$
A^3 =
\begin{pmatrix}
4(2)+4(0) & 4(1)+4(2) \\
0(2)+4(0) & 0(1)+4(2)
\end{pmatrix}
$$

$$
A^3 = \begin{pmatrix}8&12\\0&8\end{pmatrix}
$$

## Explanation

The identity matrix does not change a matrix when multiplied by it.

The zero matrix does not change a matrix when added to it.

The powers of A follow a pattern:

$$
A^n =
\begin{pmatrix}
2^n & n2^{n-1} \\
0 & 2^n
\end{pmatrix}
$$

The diagonal entries are powers of 2, while the upper-right entry follows the pattern $n2^{n-1}$.

## Verification

For n = 2:

$$
A^2 = \begin{pmatrix}4&4\\0&4\end{pmatrix}
$$

For n = 3:

$$
A^3 = \begin{pmatrix}8&12\\0&8\end{pmatrix}
$$

Both results match the formula.

## Final Answer

$$
\boxed{AI=IA=A+0=A}
$$

$$
\boxed{A^2=\begin{pmatrix}4&4\\0&4\end{pmatrix}}
$$

$$
\boxed{A^3=\begin{pmatrix}8&12\\0&8\end{pmatrix}}
$$
