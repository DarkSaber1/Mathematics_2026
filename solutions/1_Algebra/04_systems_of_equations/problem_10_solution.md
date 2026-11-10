# Exercise 10 – A Polynomial Through Three Points

## Problem Statement

Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## Solution

### 1. Reduction to a Linear System

We substitute each given point $(x, y)$ into the general polynomial equation $p(x) = ax^2 + bx + c$:

- **Point $(0,1)$:**

$$
p(0) = a(0)^2 + b(0) + c = 1 \implies c = 1
$$

- **Point $(1,3)$:**

$$
p(1) = a(1)^2 + b(1) + c = 3 \implies a + b + c = 3
$$

- **Point $(2,9)$:**

$$
p(2) = a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9
$$

This yields the linear system of equations:

$$
\begin{cases}
c = 1, \\
a + b + c = 3, \\
4a + 2b + c = 9.
\end{cases}
$$

In matrix form $Ax = b$, reordering variables as $(a, b, c)$:

$$
\begin{pmatrix} 0 & 0 & 1 \\ 1 & 1 & 1 \\ 4 & 2 & 1 \end{pmatrix} \begin{pmatrix} a \\ b \\ c \end{pmatrix} = \begin{pmatrix} 1 \\ 3 \\ 9 \end{pmatrix}
$$

---

### 2. Solving by Gaussian Elimination

We set up the augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{ccc|c} 0 & 0 & 1 & 1 \\ 1 & 1 & 1 & 3 \\ 4 & 2 & 1 & 9 \end{array}\right)
$$

- **Step 1:** Swap row 1 and row 2 ($R_1 \leftrightarrow R_2$) to place a pivot in the top-left position:

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 3 \\ 0 & 0 & 1 & 1 \\ 4 & 2 & 1 & 9 \end{array}\right)
$$

- **Step 2:** Swap row 2 and row 3 ($R_2 \leftrightarrow R_3$):

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 3 \\ 4 & 2 & 1 & 9 \\ 0 & 0 & 1 & 1 \end{array}\right)
$$

- **Step 3:** Eliminate $a$ from row 2 by performing $R_2 \leftarrow R_2 - 4 R_1$:

$$
R_2 \text{ calculation: } (4, 2, 1, 9) - 4(1, 1, 1, 3) = (0, -2, -3, -3)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 3 \\ 0 & -2 & -3 & -3 \\ 0 & 0 & 1 & 1 \end{array}\right)
$$

---

### 3. Back-Substitution and Coefficient Determination

1. **Third equation:**

$$
c = 1
$$

2. **Second equation:**

$$
-2b - 3c = -3 \implies -2b - 3(1) = -3 \implies -2b = 0 \implies b = 0
$$

3. **First equation:**

$$
a + b + c = 3 \implies a + 0 + 1 = 3 \implies a = 2
$$

The coefficient vector is:

$$
\begin{pmatrix} a \\ b \\ c \end{pmatrix} = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}
$$

Thus, the polynomial is:

$$
p(x) = 2x^2 + 1
$$

---

### Verification by Substitution

We test all three original points in the polynomial $p(x) = 2x^2 + 1$:

- **For $x = 0$:**

$$
p(0) = 2(0)^2 + 1 = 1 \quad (\text{Matches point } (0,1))
$$

- **For $x = 1$:**

$$
p(1) = 2(1)^2 + 1 = 2 + 1 = 3 \quad (\text{Matches point } (1,3))
$$

- **For $x = 2$:**

$$
p(2) = 2(2)^2 + 1 = 2(4) + 1 = 9 \quad (\text{Matches point } (2,9))
$$

All three points are satisfied, confirming that $p(x) = 2x^2 + 1$ is the correct polynomial.