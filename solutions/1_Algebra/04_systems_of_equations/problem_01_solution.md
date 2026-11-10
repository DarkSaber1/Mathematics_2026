# Exercise 1 – From a System to a Matrix

## Problem Statement

Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Solution

### 1. Matrix Representation

We rewrite the system in the matrix form $Ax=b$:

$$
\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$

### 2. Component Identification

- **Coefficient Matrix ($A$):**

$$
A = \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}
$$

- **Vector of Unknowns ($x$):**

$$
x = \begin{pmatrix} x \\ y \\ z \end{pmatrix}
$$

- **Right-Hand Side Vector ($b$):**

$$
b = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$

### 3. Row-to-Equation Correspondence Explanation

Each row of matrix $A$ represents the coefficients of the variables $x$, $y$, and $z$ from a single linear equation in the system:

- **Row 1:** The entries $(2, -1, 1)$ are the coefficients of $x$, $y$, and $z$ in the first equation $2x - y + z = 4$.
- **Row 2:** The entries $(1, 3, -2)$ are the coefficients in the second equation $x + 3y - 2z = 1$.
- **Row 3:** The entries $(3, 1, 1)$ are the coefficients in the third equation $3x + y + z = 7$.

By matrix-vector multiplication rules, taking the dot product of the $i$-th row of $A$ with the unknown vector $x$ yields the left-hand side of the $i$-th linear equation, which equals the $i$-th entry of the right-hand side vector $b$.