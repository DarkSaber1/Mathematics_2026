# Exercise 3 – Inconsistent System

## Problem Statement

Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Solution

### 1. Gaussian Elimination

We set up the augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{cc|c} 1 & 2 & 3 \\ 2 & 4 & 7 \end{array}\right)
$$

We eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ calculation: } (2, 4, 7) - 2(1, 2, 3) = (2, 4, 7) - (2, 4, 6) = (0, 0, 1)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c} 1 & 2 & 3 \\ 0 & 0 & 1 \end{array}\right)
$$

---

### 2. Contradiction Analysis and Geometric Interpretation

- **Matrix Contradiction:**  
  The second row of the augmented matrix translates directly back to the equation:

$$
0x + 0y = 1 \implies 0 = 1
$$

  Since $0 = 1$ is a logical impossibility, the system has **no solution** (it is inconsistent).

- **Geometric Interpretation:**  
  Each equation in the system represents a line in $\mathbb{R}^2$:
  - Line 1: $x + 2y = 3 \implies y = -\frac{1}{2}x + \frac{3}{2}$
  - Line 2: $2x + 4y = 7 \implies y = -\frac{1}{2}x + \frac{7}{4}$

  Both lines have the exact same slope ($m = -\frac{1}{2}$) but different $y$-intercepts ($\frac{3}{2} \neq \frac{7}{4}$). Therefore, the two lines are **parallel** and will never intersect, meaning there is no point $(x,y)$ that satisfies both equations simultaneously.