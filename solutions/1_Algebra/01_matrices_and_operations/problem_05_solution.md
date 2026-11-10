# Exercise 5 – Matrix Times Vector

## Problem Statement

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2
\end{pmatrix}
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Solution

### 1. Calculation of $Ax$ (Row-by-Vector Dot Product)

We compute $Ax$ by taking the dot product of each row of $A$ with the vector $x$:

$$
Ax = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 4 \\ 2 \end{pmatrix}
$$

$$
Ax = \begin{pmatrix} 2(4) + (-1)(2) \\ 1(4) + 3(2) \end{pmatrix}
$$

$$
Ax = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix}
$$

$$
Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

### 2. $Ax$ as a Linear Combination of Columns

The columns of matrix $A$ are $a_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$ and $a_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}$. Using the components of vector $x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$ as scalar coefficients:

$$
Ax = 4 a_1 + 2 a_2
$$

$$
Ax = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

$$
Ax = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix}
$$

$$
Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

### Explanation

Matrix-vector multiplication can be interpreted in two equivalent ways:
1. Entry-by-entry via row dot products.
2. A linear combination of the column vectors of $A$ weighted by the scalar entries of $x$.

### Verification

We compare the results obtained from both calculation methods:

- **Row dot product method:**

$$
Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

- **Column linear combination method:**

$$
4 a_1 + 2 a_2 = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

Both methods yield identical vectors, verifying that the calculation is correct.