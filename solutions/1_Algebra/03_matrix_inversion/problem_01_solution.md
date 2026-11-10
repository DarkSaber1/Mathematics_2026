# Exercise 1 – Definition of the Inverse

## Problem Statement

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Solution

### 1. Calculation of $AB$

We compute the product $AB$:

$$
AB = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}
$$

$$
AB = \begin{pmatrix} 2(1) + 1(-1) & 2(-1) + 1(2) \\ 1(1) + 1(-1) & 1(-1) + 1(2) \end{pmatrix}
$$

$$
AB = \begin{pmatrix} 2 - 1 & -2 + 2 \\ 1 - 1 & -1 + 2 \end{pmatrix}
$$

$$
AB = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I
$$

### 2. Calculation of $BA$

We compute the product $BA$:

$$
BA = \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
$$

$$
BA = \begin{pmatrix} 1(2) + (-1)(1) & 1(1) + (-1)(1) \\ -1(2) + 2(1) & -1(1) + 2(1) \end{pmatrix}
$$

$$
BA = \begin{pmatrix} 2 - 1 & 1 - 1 \\ -2 + 2 & -1 + 2 \end{pmatrix}
$$

$$
BA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I
$$

### 3. Relation to the Definition of the Inverse

By definition, a matrix $B$ is the inverse of a square matrix $A$ (denoted $B = A^{-1}$) if and only if:

$$
AB = I \quad \text{and} \quad BA = I
$$

Since both matrix products $AB$ and $BA$ equal the identity matrix $I$, matrix $B$ is indeed the inverse of matrix $A$ ($B = A^{-1}$).

### Verification

We verify the results by confirming that both diagonal entries are 1 and both off-diagonal entries are 0:

- For $AB$: $(1,1)$ entry is $2-1=1$, $(1,2)$ entry is $-2+2=0$, $(2,1)$ entry is $1-1=0$, $(2,2)$ entry is $-1+2=1$.
- For $BA$: $(1,1)$ entry is $2-1=1$, $(1,2)$ entry is $1-1=0$, $(2,1)$ entry is $-2+2=0$, $(2,2)$ entry is $-1+2=1$.

Both products yield the identity matrix $I$, verifying that $B = A^{-1}$.