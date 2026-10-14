
# Exercise 8 – Row Operations and Their Reversibility

## Problem Statement

Perform the three given row operations in order, write the matrix after each step, and identify the inverse of each operation.

## Solution

Given:

$$
A = \begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3
\end{pmatrix}
$$

### 1. First Row Operation

Apply $R_2 \leftarrow R_2 - 2R_1$.

$$
R_2 = (2,4,1)-2(1,2,-1)=(0,0,3)
$$

The new matrix is:

$$
A_1 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3
\end{pmatrix}
$$

### 2. Second Row Operation

Apply $R_3 \leftarrow R_3 + R_1$.

$$
R_3 = (-1,1,3)+(1,2,-1)=(0,3,2)
$$

The new matrix is:

$$
A_2 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2
\end{pmatrix}
$$

### 3. Third Row Operation

Interchange $R_2$ and $R_3$.

The final matrix is:

$$
A_3 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3
\end{pmatrix}
$$

## Explanation

Elementary row operations change the rows of a matrix without losing information.

Each operation can be reversed:

1. $R_2 \leftarrow R_2 - 2R_1$

   Inverse: $R_2 \leftarrow R_2 + 2R_1$

2. $R_3 \leftarrow R_3 + R_1$

   Inverse: $R_3 \leftarrow R_3 - R_1$

3. Swap $R_2$ and $R_3$.

   Inverse: Swap $R_2$ and $R_3$ again.

## Verification

Starting from $A_3$, reverse the operations in the opposite order.

First, swap rows 2 and 3:

$$
\begin{pmatrix}
1&2&-1\\
0&0&3\\
0&3&2
\end{pmatrix}
$$

Then subtract row 1 from row 3:

$$
\begin{pmatrix}
1&2&-1\\
0&0&3\\
-1&1&3
\end{pmatrix}
$$

Finally, add twice row 1 to row 2:

$$
\begin{pmatrix}
1&2&-1\\
2&4&1\\
-1&1&3
\end{pmatrix}
=A
$$

The original matrix is recovered.

## Final Answer

$$
\boxed{
A_3 =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3
\end{pmatrix}
}
$$

All three row operations are reversible.
