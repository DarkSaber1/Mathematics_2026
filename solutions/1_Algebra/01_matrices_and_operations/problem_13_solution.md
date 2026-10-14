
# Exercise 13 – A Recurrence Written in Matrix Form

## Problem Statement

Calculate F², F³, F⁴, and F⁵. Compare the results with the Fibonacci sequence and explain how matrix multiplication represents a recurrence step.

## Solution

Given:

$$
F = \begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
$$

### 1. Calculate Matrix Powers

$$
F^2 = F \cdot F =
\begin{pmatrix}
2 & 1\\
1 & 1
\end{pmatrix}
$$

$$
F^3 = F^2 \cdot F =
\begin{pmatrix}
3 & 2\\
2 & 1
\end{pmatrix}
$$

$$
F^4 = F^3 \cdot F =
\begin{pmatrix}
5 & 3\\
3 & 2
\end{pmatrix}
$$

$$
F^5 = F^4 \cdot F =
\begin{pmatrix}
8 & 5\\
5 & 3
\end{pmatrix}
$$

### 2. Connection to the Fibonacci Sequence

The Fibonacci sequence is:

$$
0,\ 1,\ 1,\ 2,\ 3,\ 5,\ 8,\ldots
$$

Each term is the sum of the previous two terms.

The matrix powers contain consecutive Fibonacci numbers.

The general pattern is:

$$
F^n =
\begin{pmatrix}
f_{n+1} & f_n\\
f_n & f_{n-1}
\end{pmatrix}
$$

where $f_n$ is the nth Fibonacci number.

### 3. Matrix-Vector Multiplication

For a vector:

$$
v = \begin{pmatrix}a\\b\end{pmatrix}
$$

Multiplying by F gives:

$$
Fv =
\begin{pmatrix}
1 & 1\\
1 & 0
\end{pmatrix}
\begin{pmatrix}a\\b\end{pmatrix}
$$

$$
Fv =
\begin{pmatrix}
a+b\\
a
\end{pmatrix}
$$

## Explanation

The matrix F generates Fibonacci numbers through repeated multiplication.

If a and b are two consecutive terms, multiplying by F produces their sum and keeps a for the next step.

This follows the Fibonacci recurrence:

$$
f_{n+1} = f_n + f_{n-1}
$$

## Verification

Using two consecutive Fibonacci numbers, a = 3 and b = 2:

$$
F\begin{pmatrix}3\\2\end{pmatrix}
=
\begin{pmatrix}5\\3\end{pmatrix}
$$

The next Fibonacci number is 5, so the recurrence works correctly.

Also, F⁵ contains the consecutive Fibonacci numbers 8, 5, and 3.

## Final Answer

$$
\boxed{
F^5 = \begin{pmatrix}
8 & 5\\
5 & 3
\end{pmatrix}
}
$$

$$
\boxed{
F\begin{pmatrix}a\\b\end{pmatrix}
=
\begin{pmatrix}a+b\\a\end{pmatrix}
}
$$

Matrix powers of F follow the Fibonacci sequence.
