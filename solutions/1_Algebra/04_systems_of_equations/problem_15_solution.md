# Exercise 15 – Classifying Three Systems

## Problem Statement

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## Solution

### 1. Analysis of System 1

We construct the augmented matrix $[A \mid b_1]$:

$$
[A \mid b_1] = \left(\begin{array}{cc|c} 1 & 1 & 2 \\ 1 & -1 & 0 \end{array}\right)
$$

We eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - R_1$:

$$
R_2 \text{ calculation: } (1, -1, 0) - (1, 1, 2) = (0, -2, -2)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -2 & -2 \end{array}\right)
$$

- **Pivots:** There are 2 non-zero pivots (column 1 for $x$, column 2 for $y$).
- **Classification:** **Exactly one solution (Unique Solution)**.
- **Justification:** The rank of the matrix equals the number of variables ($r = n = 2$). Back-substitution yields $y = 1$ and $x = 1$. The unique solution vector is:

$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

---

### 2. Analysis of System 2

We construct the augmented matrix $[A \mid b_2]$:

$$
[A \mid b_2] = \left(\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & 2 & 4 \end{array}\right)
$$

We eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ calculation: } (2, 2, 4) - 2(1, 1, 2) = (0, 0, 0)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 0 \end{array}\right)
$$

- **Pivots:** There is only 1 pivot (column 1 for $x$). Column 2 ($y$) contains no pivot.
- **Classification:** **Infinitely many solutions**.
- **Justification:** The second row yields $0 = 0$, making it completely redundant. Variable $y$ is a free variable ($y = t$). The system reduces to $x = 2 - t$. The parametric solution set is:

$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2 \\ 0 \end{pmatrix} + t \begin{pmatrix} -1 \\ 1 \end{pmatrix} \qquad (t \in \mathbb{R})
$$

---

### 3. Analysis of System 3

We construct the augmented matrix $[A \mid b_3]$:

$$
[A \mid b_3] = \left(\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & 2 & 5 \end{array}\right)
$$

We eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ calculation: } (2, 2, 5) - 2(1, 1, 2) = (0, 0, 1)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 1 \end{array}\right)
$$

- **Pivots:** A pivot appears in the augmented right-hand side column.
- **Classification:** **No solution (Inconsistent System)**.
- **Justification:** Row 2 translates to the linear equation:

$$
0x + 0y = 1
$$

Simplifying gives:

$$
0 = 1
$$

This is a logical contradiction.

---

### 4. Summary Table of Classifications

| System | Row Echelon Form (Rows) | Pivot Positions | Solution Type |
| :--- | :--- | :--- | :--- |
| **System 1** | Row 1: [1, 1 \| 2]<br>Row 2: [0, -2 \| -2] | Columns 1 and 2 | **Exactly one solution** |
| **System 2** | Row 1: [1, 1 \| 2]<br>Row 2: [0, 0 \| 0] | Column 1 (1 free variable) | **Infinitely many solutions** |
| **System 3** | Row 1: [1, 1 \| 2]<br>Row 2: [0, 0 \| 1] | Column 1 and Augmented column | **No solution** |