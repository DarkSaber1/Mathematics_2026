
# Exercise 12 – Formula for a Matrix Power

## Problem Statement

Calculate A², A³, and A⁴. Find a general formula for Aⁿ and prove it using mathematical induction.

## Solution

Given:

$$
A = \begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
$$

### 1. Calculate Matrix Powers

$$
A^2 = A \cdot A
= \begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix}
$$

$$
A^3 = A^2 \cdot A
= \begin{pmatrix}
1 & 3\\
0 & 1
\end{pmatrix}
$$

$$
A^4 = A^3 \cdot A
= \begin{pmatrix}
1 & 4\\
0 & 1
\end{pmatrix}
$$

### 2. Find the General Formula

We observe that the upper-right entry increases by 1 with each multiplication.

Therefore, we predict:

$$
\boxed{
A^n = \begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix}
}
$$

for every positive integer n.

### 3. Proof by Mathematical Induction

**Base Case (n = 1):**

$$
A^1 = \begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
$$

The formula is correct for n = 1.

**Inductive Step:**

Assume the formula holds for n:

$$
A^n = \begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix}
$$

Multiply both sides by A:

$$
A^{n+1} = A^n A
$$

$$
= \begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
$$

$$
= \begin{pmatrix}
1 & n+1\\
0 & 1
\end{pmatrix}
$$

This is exactly the formula for n+1.

Therefore, the formula holds for all positive integers n.

## Explanation

The diagonal entries remain equal to 1, while the upper-right entry increases by 1 each time A is multiplied.

Mathematical induction proves that this pattern continues for every positive integer n.

## Verification

For n = 4, the general formula gives:

$$
A^4 = \begin{pmatrix}
1 & 4\\
0 & 1
\end{pmatrix}
$$

This matches the result calculated directly.

## Final Answer

$$
\boxed{
A^n = \begin{pmatrix}
1 & n\\
0 & 1
\end{pmatrix}
}
$$

The formula is valid for every positive integer n.
