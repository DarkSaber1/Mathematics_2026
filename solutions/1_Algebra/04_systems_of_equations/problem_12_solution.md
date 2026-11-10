# Exercise 12 – Homogeneous System

## Problem Statement

Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

## Solution

### 1. Gaussian Elimination

We set up the augmented matrix $[A \mid 0]$:

$$
[A \mid 0] = \left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 2 & 4 & -2 & 0 \\ 1 & -1 & 2 & 0 \end{array}\right)
$$

- **Step 1:** Eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ calculation: } (2, 4, -2, 0) - 2(1, 2, -1, 0) = (0, 0, 0, 0)
$$

$$
\left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 0 & 0 & 0 \\ 1 & -1 & 2 & 0 \end{array}\right)
$$

- **Step 2:** Swap row 2 and row 3 ($R_2 \leftrightarrow R_3$) to place the zero row at the bottom:

$$
\left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 1 & -1 & 2 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right)
$$

- **Step 3:** Eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - R_1$:

$$
R_2 \text{ calculation: } (1, -1, 2, 0) - (1, 2, -1, 0) = (0, -3, 3, 0)
$$

$$
\left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & -3 & 3 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right)
$$

- **Step 4:** Scale row 2 by $-\frac{1}{3}$ ($R_2 \leftarrow -\frac{1}{3} R_2$):

$$
\left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right)
$$

---

### 2. Parametric Solution Form

Converting the row echelon form matrix back to linear equations:

1. **Second equation:**

$$
y - z = 0 \implies y = z
$$

2. **First equation:**

$$
x + 2y - z = 0 \implies x + 2(z) - z = 0 \implies x + z = 0 \implies x = -z
$$

Since column 3 contains no pivot, $z$ is the **free variable**. Setting $z = t$ (where $t \in \mathbb{R}$), the solution set in parametric scalar form is:

$$
\begin{cases}
x = -t, \\
y = t, \\
z = t
\end{cases} \qquad (t \in \mathbb{R})
$$

In vector parametric form:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = t \begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix}
$$

---

### 3. Explanation of the Trivial Solution $(0,0,0)$

A homogeneous system of linear equations is represented in matrix form as:

$$
Ax = 0
$$

where $A$ is an $m \times n$ coefficient matrix, $x$ is the $n \times 1$ vector of unknowns, and $0$ is the $m \times 1$ zero vector.

- **Algebraic Explanation:**  
  When the zero vector $x = 0$ is substituted into $Ax$, every entry in each equation is multiplied by zero:

$$
A \cdot 0 = \begin{pmatrix} a_{11}(0) + a_{12}(0) + \dots + a_{1n}(0) \\ a_{21}(0) + a_{22}(0) + \dots + a_{2n}(0) \\ \vdots \\ a_{m1}(0) + a_{m2}(0) + \dots + a_{mn}(0) \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ \vdots \\ 0 \end{pmatrix} = 0
$$

  Because $0 = 0$ holds identically regardless of the specific coefficient values in $A$, the zero vector (trivial solution) is guaranteed to satisfy **every** homogeneous system.

- **In our parametric solution:**  
  Setting the parameter $t = 0$ immediately yields the trivial solution:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = 0 \begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
$$