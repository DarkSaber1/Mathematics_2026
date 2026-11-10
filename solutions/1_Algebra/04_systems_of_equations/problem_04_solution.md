# Exercise 4 – Infinitely Many Solutions

## Problem Statement

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## Solution

### 1. Step-by-Step Gaussian Elimination

We set up the augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 2 & 2 & 2 & 4 \\ 1 & -1 & 1 & 0 \end{array}\right)
$$

- **Step 1:** Eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ calculation: } (2, 2, 2, 4) - 2(1, 1, 1, 2) = (0, 0, 0, 0)
$$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 0 & 0 & 0 \\ 1 & -1 & 1 & 0 \end{array}\right)
$$

- **Step 2:** Swap row 2 and row 3 ($R_2 \leftrightarrow R_3$) to move the zero row to the bottom:

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 1 & -1 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right)
$$

- **Step 3:** Eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - R_1$:

$$
R_2 \text{ calculation: } (1, -1, 1, 0) - (1, 1, 1, 2) = (0, -2, 0, -2)
$$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & -2 & 0 & -2 \\ 0 & 0 & 0 & 0 \end{array}\right)
$$

- **Step 4:** Scale row 2 by $-\frac{1}{2}$ ($R_2 \leftarrow -\frac{1}{2} R_2$):

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{array}\right)
$$

---

### 2. Parametric Solution Form

Converting the row echelon form matrix back to linear equations:

1. **Second equation:**

$$
y = 1
$$

2. **First equation:**

$$
x + y + z = 2 \implies x + 1 + z = 2 \implies x + z = 1 \implies x = 1 - z
$$

Since $z$ does not correspond to a pivot column, $z$ is chosen as the **free variable**. Let $z = t$ (where $t \in \mathbb{R}$). 

The parametric solution set is:

$$
\begin{cases}
x = 1 - t, \\
y = 1, \\
z = t
\end{cases} \qquad (t \in \mathbb{R})
$$

In vector parametric form:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}
$$

---

### 3. Verification with a Chosen Parameter Value

Let us choose the parameter value $t = 2$.

- **Resulting point:**

$$
x = 1 - 2 = -1, \quad y = 1, \quad z = 2
$$

Written as a vector:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} -1 \\ 1 \\ 2 \end{pmatrix}
$$

- **Substituting into the original system:**
  - **Equation 1:** $(-1) + 1 + 2 = 2 \quad (\text{Correct})$
  - **Equation 2:** $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4 \quad (\text{Correct})$
  - **Equation 3:** $(-1) - 1 + 2 = -2 + 2 = 0 \quad (\text{Correct})$

Since all equations are satisfied, the parametric solution form is verified to be correct.