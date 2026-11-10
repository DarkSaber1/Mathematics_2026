# Exercise 1 – Matrix Size and Entries

## Problem Statement

Given

$$
A = \begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5
\end{pmatrix},\qquad B = \begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1
\end{pmatrix}
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Solution

### 1. Matrix Dimensions

Matrix dimensions are given in the format $\text{rows} \times \text{columns}$:

- Matrix $A$ has 2 rows and 3 columns, so its size is $2 \times 3$.
- Matrix $B$ has 3 rows and 2 columns, so its size is $3 \times 2$.

### 2. Matrix Entries

The notation $a_{ij}$ identifies the entry in row $i$ and column $j$:

- $a_{12} = -1$ (row 1, column 2 of $A$)
- $a_{23} = 5$ (row 2, column 3 of $A$)
- $b_{21} = -2$ (row 2, column 1 of $B$)
- $b_{32} = 1$ (row 3, column 2 of $B$)

### 3. Row and Column Vectors

Extracting the requested row and column from the matrices:

- The second row of $A$ written as a row vector:

$$
\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}
$$

- The first column of $B$ written as a column vector:

$$
\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}
$$

### Verification

We verify the dimensions and index extraction directly from the definitions:

- $A$ has 2 rows and 3 columns ($2 \times 3$). $B$ has 3 rows and 2 columns ($3 \times 2$).
- Checking entries by indices: $A_{1,2} = -1$, $A_{2,3} = 5$, $B_{2,1} = -2$, and $B_{3,2} = 1$.
- Row 2 of $A$ corresponds to entries $(a_{21}, a_{22}, a_{23}) = (0, 4, 5)$.
- Column 1 of $B$ corresponds to entries $(b_{11}, b_{21}, b_{31})^T = (1, -2, 4)^T$. All values match the original matrices.