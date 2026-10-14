
# Exercise 2 – Addition and Scalar Multiplication

## Problem Statement

Given matrices A and B, calculate A+B, A-B, and 3A-2B. Explain why matrix addition requires matrices of the same size.

## Solution

Given:

$$
A =
\begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}
$$

$$
B =
\begin{pmatrix}
4 & -2 \\
0 & 5
\end{pmatrix}
$$

### 1. Calculate A+B

Add the corresponding entries:

$$
A+B =
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5
\end{pmatrix}
$$

$$
A+B =
\begin{pmatrix}
5 & 0 \\
-1 & 8
\end{pmatrix}
$$

### 2. Calculate A-B

Subtract the corresponding entries:

$$
A-B =
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5
\end{pmatrix}
$$

$$
A-B =
\begin{pmatrix}
-3 & 4 \\
-1 & -2
\end{pmatrix}
$$

### 3. Calculate 3A-2B

First, multiply A by 3:

$$
3A =
\begin{pmatrix}
3 & 6 \\
-3 & 9
\end{pmatrix}
$$

Then multiply B by 2:

$$
2B =
\begin{pmatrix}
8 & -4 \\
0 & 10
\end{pmatrix}
$$

Subtract the matrices:

$$
3A-2B =
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10
\end{pmatrix}
$$

$$
3A-2B =
\begin{pmatrix}
-5 & 10 \\
-3 & -1
\end{pmatrix}
$$

## Explanation

Matrix addition and subtraction are performed element by element.

Both matrices must have the same dimensions because each entry needs a corresponding entry in the other matrix.

Scalar multiplication means multiplying every entry of a matrix by the given number.

## Verification

Both A and B are 2x2 matrices, so addition and subtraction are possible.

We can verify the last result using:

$$
3A-2B = A+2(A-B)
$$

$$
A+2(A-B) =
\begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}
+
\begin{pmatrix}
-6 & 8 \\
-2 & -4
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
-5 & 10 \\
-3 & -1
\end{pmatrix}
$$

The result matches the original calculation.

## Final Answer

$$
\boxed{
A+B =
\begin{pmatrix}
5 & 0 \\
-1 & 8
\end{pmatrix}
}
$$

$$
\boxed{
A-B =
\begin{pmatrix}
-3 & 4 \\
-1 & -2
\end{pmatrix}
}
$$

$$
\boxed{
3A-2B =
\begin{pmatrix}
-5 & 10 \\
-3 & -1
\end{pmatrix}
}
$$
