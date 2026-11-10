# Exercise 2 – Gaussian Elimination — One Solution

## Problem Statement

Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

## Solution

### 1. Step-by-Step Gaussian Elimination

We construct the augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 2 & -1 & 1 & 3 \\ 1 & 2 & -1 & 2 \end{array}\right)
$$

- **Step 1:** Eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ calculation: } (2, -1, 1, 3) - 2(1, 1, 1, 6) = (0, -3, -1, -9)
$$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 1 & 2 & -1 & 2 \end{array}\right)
$$

- **Step 2:** Eliminate $x$ from row 3 by performing $R_3 \leftarrow R_3 - R_1$:

$$
R_3 \text{ calculation: } (1, 2, -1, 2) - (1, 1, 1, 6) = (0, 1, -2, -4)
$$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 0 & 1 & -2 & -4 \end{array}\right)
$$

- **Step 3:** Swap row 2 and row 3 ($R_2 \leftrightarrow R_3$) to obtain a simpler pivot:

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & -3 & -1 & -9 \end{array}\right)
$$

- **Step 4:** Eliminate $y$ from row 3 by performing $R_3 \leftarrow R_3 + 3 R_2$:

$$
R_3 \text{ calculation: } (0, -3, -1, -9) + 3(0, 1, -2, -4) = (0, 0, -7, -21)
$$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & 0 & -7 & -21 \end{array}\right)
$$

---

### 2. Back-Substitution

From the row echelon form, we convert back to linear equations:

1. **Third equation:**

$$
-7z = -21 \implies z = 3
$$

2. **Second equation:**

$$
y - 2z = -4 \implies y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2
$$

3. **First equation:**

$$
x + y + z = 6 \implies x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1
$$

Thus, the unique solution vector is:

$$
x = \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}
$$

---

### 3. Verification by Substitution

We substitute $x=1$, $y=2$, $z=3$ back into the original system:

- **Equation 1:**

$$
1 + 2 + 3 = 6 \quad (\text{Correct})
$$

- **Equation 2:**

$$
2(1) - 2 + 3 = 2 - 2 + 3 = 3 \quad (\text{Correct})
$$

- **Equation 3:**

$$
1 + 2(2) - 3 = 1 + 4 - 3 = 2 \quad (\text{Correct})
$$

All three equations are satisfied, confirming the solution vector:

$$
x = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}
$$