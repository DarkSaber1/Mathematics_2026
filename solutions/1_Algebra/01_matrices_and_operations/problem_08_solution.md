# Exercise 8 – Row Operations and Their Reversibility

## Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

### 1. Sequential Elementary Row Operations

Starting with the initial matrix:

$$
A = \begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3
\end{pmatrix}
$$

- **Step 1:** $R_2 \leftarrow R_2 - 2R_1$  
  Computing the new row 2: $(2, 4, 1) - 2(1, 2, -1) = (0, 0, 3)$.

$$
A_1 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3
\end{pmatrix}
$$

- **Step 2:** $R_3 \leftarrow R_3 + R_1$  
  Computing the new row 3: $(-1, 1, 3) + (1, 2, -1) = (0, 3, 2)$.

$$
A_2 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2
\end{pmatrix}
$$

- **Step 3:** Interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$)

$$
A_3 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3
\end{pmatrix}
$$

### 2. Reversing the Operations

Each elementary row operation can be undone using an inverse operation:

1. The inverse of $R_2 \leftarrow R_2 - 2R_1$ is **$R_2 \leftarrow R_2 + 2R_1$**.
2. The inverse of $R_3 \leftarrow R_3 + R_1$ is **$R_3 \leftarrow R_3 - R_1$**.
3. The inverse of interchanging $R_2$ and $R_3$ is **interchanging $R_2$ and $R_3$ again** ($R_2 \leftrightarrow R_3$).

### Explanation

Elementary row operations preserve the row space of a matrix. Because every elementary row operation is reversible, applying the inverse operations in reverse chronological order restores the original matrix.

### Verification

We apply the inverse operations to $A_3$ in reverse order (Step 3 $\rightarrow$ Step 2 $\rightarrow$ Step 1):

1. Interchange $R_2$ and $R_3$ on $A_3$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2
\end{pmatrix}
$$

2. Apply $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
(0-1) & (3-2) & (2-(-1))
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3
\end{pmatrix}
$$

3. Apply $R_2 \leftarrow R_2 + 2R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 \\
(0+2(1)) & (0+2(2)) & (3+2(-1)) \\
-1 & 1 & 3
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3
\end{pmatrix}
= A
$$

Since the original matrix $A$ is completely recovered, all operations and their inverses are correct.