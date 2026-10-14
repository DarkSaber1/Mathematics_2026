
# Exercise 4 – Matrix Multiplication and Noncommutativity

## Problem Statement

Calculate AB and BA, then determine whether AB = BA.

## Solution

Given:

$$
A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
\qquad
B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
$$

### 1. Calculate AB

$$
AB =
\begin{pmatrix}
1(2)+2(3) & 1(0)+2(1) \\
0(2)+1(3) & 0(0)+1(1)
\end{pmatrix}
$$

$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
$$

### 2. Calculate BA

$$
BA =
\begin{pmatrix}
2(1)+0(0) & 2(2)+0(1) \\
3(1)+1(0) & 3(2)+1(1)
\end{pmatrix}
$$

$$
BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

## Explanation

Matrix multiplication is performed by multiplying rows of the first matrix by columns of the second matrix.

Unlike ordinary number multiplication, changing the order of matrices can change the result.

This property is called noncommutativity.

## Verification

Comparing both results:

$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
$$

$$
BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

Since the corresponding entries are different:

$$
AB \neq BA
$$

## Final Answer

$$
\boxed{AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}}
$$

$$
\boxed{BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}}
$$

Therefore, matrix multiplication is not commutative in general.
