
# Exercise 5 – Matrix Times Vector

## Problem Statement

Compute Ax and express the result as a linear combination of the columns of A, using the entries of x as coefficients.

## Solution

Given:

$$
A =
\begin{pmatrix}
2 & -1 \\
1 & 3
\end{pmatrix}
$$

$$
x =
\begin{pmatrix}
4 \\
2
\end{pmatrix}
$$

### 1. Calculate Ax

Multiply each row of A by the vector x:

$$
Ax =
\begin{pmatrix}
2 & -1 \\
1 & 3
\end{pmatrix}
\begin{pmatrix}
4 \\
2
\end{pmatrix}
$$

$$
Ax =
\begin{pmatrix}
2(4)+(-1)(2) \\
1(4)+3(2)
\end{pmatrix}
$$

$$
Ax =
\begin{pmatrix}
8-2 \\
4+6
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10
\end{pmatrix}
$$

### 2. Linear Combination

The columns of A are:

$$
a_1 =
\begin{pmatrix}
2 \\
1
\end{pmatrix}
$$

$$
a_2 =
\begin{pmatrix}
-1 \\
3
\end{pmatrix}
$$

Using the entries of x as coefficients:

$$
Ax = 4a_1 + 2a_2
$$

$$
Ax =
4\begin{pmatrix}
2 \\
1
\end{pmatrix}
+
2\begin{pmatrix}
-1 \\
3
\end{pmatrix}
$$

$$
Ax =
\begin{pmatrix}
8 \\
4
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6
\end{pmatrix}
$$

$$
Ax =
\begin{pmatrix}
6 \\
10
\end{pmatrix}
$$

## Explanation

Matrix-vector multiplication is performed by multiplying each row of the matrix by the vector.

It can also be expressed as a linear combination of the columns of the matrix, using the vector entries as coefficients.

## Verification

Both methods give the same result:

$$
Ax =
\begin{pmatrix}
6 \\
10
\end{pmatrix}
$$

$$
4a_1+2a_2 =
\begin{pmatrix}
6 \\
10
\end{pmatrix}
$$

Therefore, the result is correct.

## Final Answer

$$
\boxed{
Ax =
\begin{pmatrix}
6 \\
10
\end{pmatrix}
}
$$

$$
\boxed{Ax = 4a_1 + 2a_2}
$$
