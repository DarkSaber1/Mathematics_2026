# Exercise 5 – Row Echelon Form and Number of Solutions

## Problem Statement

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Solution

### 1. Analysis of Pivots and Solution Existence

We analyze the matrix in row echelon form:

- **Row 1:** Pivot in column 1 (corresponding to variable $x$).
- **Row 2:** Pivot in column 2 (corresponding to variable $y$).
- **Row 3:** Entire zero row ($0 = 0$), which provides no constraint and confirms system consistency.

Since there is no row of the form $(0 \quad 0 \quad 0 \mid b)$ with $b \neq 0$, the system is **consistent**.

To determine the number of free variables:
- **Total number of variables ($n$):** $3$ ($x, y, z$).
- **Number of pivot columns / rank ($r$):** $2$ (columns 1 and 2).
- **Number of free variables ($n - r$):** $3 - 2 = 1$.

Since column 3 contains no pivot, $z$ is the **free variable**. Because there is $1$ free variable that can take any real value, the system has **infinitely many solutions**.

---

### 2. Parametric Solution Form

Converting the non-zero rows back to linear equations:

1. **Second equation:**

$$
y + 2z = 1 \implies y = 1 - 2z
$$

2. **First equation:**

$$
x + 2y - z = 3
$$

Substituting $y = 1 - 2z$ into the first equation:

$$
x + 2(1 - 2z) - z = 3 \implies x + 2 - 4z - z = 3 \implies x - 5z = 1 \implies x = 1 + 5z
$$

Setting the free variable $z = t$ (where $t \in \mathbb{R}$), the solution in parametric scalar form is:

$$
\begin{cases}
x = 1 + 5t, \\
y = 1 - 2t, \\
z = t
\end{cases} \qquad (t \in \mathbb{R})
$$

In vector parametric form:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} 5 \\ -2 \\ 1 \end{pmatrix}
$$

---

### Verification

We verify by substituting the parametric vector into the augmented matrix equations:

- **Row 1 equation ($x + 2y - z$):**

$$
(1 + 5t) + 2(1 - 2t) - t = 1 + 5t + 2 - 4t - t = 3 \quad (\text{Matches right-hand side } 3)
$$

- **Row 2 equation ($y + 2z$):**

$$
(1 - 2t) + 2(t) = 1 - 2t + 2t = 1 \quad (\text{Matches right-hand side } 1)
$$

The parametric solution form is verified to be correct.