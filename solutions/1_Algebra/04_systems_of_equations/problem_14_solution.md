# Exercise 14 – A Small Change in the Right-Hand Side

## Problem Statement

Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Solution

### 1. Analysis of System 1

We construct the augmented matrix $[A \mid b_1]$ for System 1:

$$
[A \mid b_1] = \left(\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 3 & 0 & 3 \end{array}\right)
$$

- **Step 1:** Eliminate $x$ from row 2 ($R_2 \leftarrow R_2 - 2 R_1$) and row 3 ($R_3 \leftarrow R_3 - 3 R_1$):

$$
R_2 \text{ calculation: } (2, -1, 1) - 2(1, 1, 2) = (0, -3, -3)
$$

$$
R_3 \text{ calculation: } (3, 0, 3) - 3(1, 1, 2) = (0, -3, -3)
$$

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -3 & -3 \\ 0 & -3 & -3 \end{array}\right)
$$

- **Step 2:** Scale row 2 by $-\frac{1}{3}$ ($R_2 \leftarrow -\frac{1}{3} R_2$):

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 1 & 1 \\ 0 & -3 & -3 \end{array}\right)
$$

- **Step 3:** Eliminate $y$ from row 3 ($R_3 \leftarrow R_3 + 3 R_2$):

$$
R_3 \text{ calculation: } (0, -3, -3) + 3(0, 1, 1) = (0, 0, 0)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array}\right)
$$

- **Solving System 1:**
  1. $y = 1$
  2. $x + y = 2 \implies x + 1 = 2 \implies x = 1$

The solution vector is:

$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

Since row 3 yields $0 = 0$, **System 1 is consistent** and has **exactly one unique solution**.

---

### 2. Analysis of System 2

We construct the augmented matrix $[A \mid b_2]$ for System 2:

$$
[A \mid b_2] = \left(\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 3 & 0 & 3.1 \end{array}\right)
$$

- **Step 1:** Eliminate $x$ from row 2 ($R_2 \leftarrow R_2 - 2 R_1$) and row 3 ($R_3 \leftarrow R_3 - 3 R_1$):

$$
R_2 \text{ calculation: } (2, -1, 1) - 2(1, 1, 2) = (0, -3, -3)
$$

$$
R_3 \text{ calculation: } (3, 0, 3.1) - 3(1, 1, 2) = (0, -3, -2.9)
$$

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -3 & -3 \\ 0 & -3 & -2.9 \end{array}\right)
$$

- **Step 2:** Scale row 2 by $-\frac{1}{3}$ ($R_2 \leftarrow -\frac{1}{3} R_2$):

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 1 & 1 \\ 0 & -3 & -2.9 \end{array}\right)
$$

- **Step 3:** Eliminate $y$ from row 3 ($R_3 \leftarrow R_3 + 3 R_2$):

$$
R_3 \text{ calculation: } (0, -3, -2.9) + 3(0, 1, 1) = (0, 0, 0.1)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 1 & 1 \\ 0 & 0 & 0.1 \end{array}\right)
$$

Row 3 translates back to the equation:

$$
0x + 0y = 0.1 \implies 0 = 0.1
$$

Since $0 = 0.1$ is a mathematical contradiction, **System 2 is inconsistent** and has **no solution**.

---

### 3. Explanation of the Structural Change

- **Overdetermined System Geometry:** Both systems are *overdetermined* (containing $3$ equations for only $2$ unknowns). Geometrically, each equation represents a line in $\mathbb{R}^2$.
- **Intersection in System 1:** The first two equations intersect at the unique point $(1, 1)$. The third line ($3x = 3 \implies x = 1$) also passes exactly through $(1, 1)$. Thus, all three lines share a common point of intersection.
- **Disruption in System 2:** Changing the third equation slightly to $3x = 3.1 \implies x = 1.0333...$ shifts the third line parallelly to the right. The third line no longer passes through $(1, 1)$. 

Because an overdetermined system requires **all** equations to hold simultaneously, a small alteration in a redundant boundary condition breaks the common point of intersection, instantly changing the system type from consistent to inconsistent.