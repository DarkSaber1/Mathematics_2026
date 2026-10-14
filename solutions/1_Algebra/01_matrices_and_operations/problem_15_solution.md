
# Exercise 15 – Associativity of Multiplication

## Problem Statement

Calculate (AB)C and A(BC). Compare the results and the number of intermediate operations. Explain associativity.

## Solution

Given:

$$
A = \begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix},
\quad
B = \begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix},
\quad
C = \begin{pmatrix}
2 & 1\\
0 & -1
\end{pmatrix}
$$

### 1. Calculate (AB)C

First, calculate AB:

$$
AB =
\begin{pmatrix}
1 & 2 & 0\\
0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 0\\
2 & 1\\
-1 & 3
\end{pmatrix}
=
\begin{pmatrix}
5 & 2\\
1 & 4
\end{pmatrix}
$$

Then multiply by C:

$$
(AB)C =
\begin{pmatrix}
5 & 2\\
1 & 4
\end{pmatrix}
\begin{pmatrix}
2 & 1\\
0 & -1
\end{pmatrix}
$$

$$
(AB)C =
\begin{pmatrix}
10 & 3\\
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

Then multiply by A:

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

- (AB)C: 12 + 8 = 20 multiplications.
- A(BC): 12 + 12 = 24 multiplications.

Therefore, calculating (AB)C requires fewer scalar multiplications.

## Explanation

Matrix multiplication is associative, meaning that changing the grouping of matrices does not change the final result.

However, different groupings can require different numbers of calculations.

## Verification

Both calculations produce:

$$
(AB)C =
\begin{pmatrix}
10 & 3\\
2 & -3
\end{pmatrix}
$$

$$
A(BC) =
\begin{pmatrix}
10 & 3\\
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
10 & 3\\
2 & -3
\end{pmatrix}
}
$$

Matrix multiplication is associative, and (AB)C is more efficient in this example.
