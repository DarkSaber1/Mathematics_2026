# Exercise 9 – A System from a Sum Condition

## Problem Statement

Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

## Solution

### 1. Matrix Formulation and Elimination

We write the system as an augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{cc|c} 1 & 1 & 10 \\ 2 & 5 & 32 \end{array}\right)
$$

We eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ calculation: } (2, 5, 32) - 2(1, 1, 10) = (2, 5, 32) - (2, 2, 20) = (0, 3, 12)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c} 1 & 1 & 10 \\ 0 & 3 & 12 \end{array}\right)
$$

---

### 2. Back-Substitution

Converting back to linear equations:

1. **Second equation:**

$$
3y = 12 \implies y = 4
$$

2. **First equation:**

$$
x + y = 10 \implies x + 4 = 10 \implies x = 6
$$

The unique solution vector is:

$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 6 \\ 4 \end{pmatrix}
$$

---

### 3. Geometric Explanation of Uniqueness

Each equation in the system represents a line in $\mathbb{R}^2$:

- **Line 1 ($L_1$):** $x + y = 10 \implies y = -x + 10$ (Slope $m_1 = -1$)
- **Line 2 ($L_2$):** $2x + 5y = 32 \implies y = -\frac{2}{5}x + \frac{32}{5}$ (Slope $m_2 = -\frac{2}{5}$)

Because the slopes are different ($m_1 \neq m_2$), the two lines are **not parallel**. Non-parallel lines in a 2D plane must intersect at **exactly one unique point**. 

Algebraically, this is reflected in the determinant of the coefficient matrix $A$:

$$
A = \begin{pmatrix} 1 & 1 \\ 2 & 5 \end{pmatrix}
$$

$$
\det(A) = (1)(5) - (1)(2) = 5 - 2 = 3 \neq 0
$$

Since $\det(A) \neq 0$, matrix $A$ is invertible, guaranteeing a unique solution vector.

---

### Verification

Substituting $x = 6$ and $y = 4$ back into both equations:

- **Equation 1:** $6 + 4 = 10 \quad (\text{Correct})$
- **Equation 2:** $2(6) + 5(4) = 12 + 20 = 32 \quad (\text{Correct})$

The solution is verified to be correct.