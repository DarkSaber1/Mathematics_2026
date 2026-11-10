# Exercise 13 – Does Every Equation Add New Information?

## Problem Statement

Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Solution

### 1. Gaussian Elimination

We set up the augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{ccc|c} 1 & 1 & 0 & 10 \\ 0 & 1 & 1 & 8 \\ 1 & 0 & -1 & 2 \end{array}\right)
$$

- **Step 1:** Eliminate $x_1$ from row 3 by performing $R_3 \leftarrow R_3 - R_1$:

$$
R_3 \text{ calculation: } (1, 0, -1, 2) - (1, 1, 0, 10) = (0, -1, -1, -8)
$$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 0 & 10 \\ 0 & 1 & 1 & 8 \\ 0 & -1 & -1 & -8 \end{array}\right)
$$

- **Step 2:** Eliminate $x_2$ from row 3 by performing $R_3 \leftarrow R_3 + R_2$:

$$
R_3 \text{ calculation: } (0, -1, -1, -8) + (0, 1, 1, 8) = (0, 0, 0, 0)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{ccc|c} 1 & 1 & 0 & 10 \\ 0 & 1 & 1 & 8 \\ 0 & 0 & 0 & 0 \end{array}\right)
$$

---

### 2. Analysis of Equation Redundancy

The appearance of the row $(0 \quad 0 \quad 0 \mid 0)$ in the third row proves that **the third equation does not add any new information** to the system. It is linearly dependent on (a linear combination of) the first two equations.

#### Direct Algebraic Calculation Showing Dependence

Let $E_1$, $E_2$, and $E_3$ represent the three original linear equations:
- $E_1: x_1 + x_2 = 10$
- $E_2: x_2 + x_3 = 8$
- $E_3: x_1 - x_3 = 2$

If we subtract Equation 2 from Equation 1 ($E_1 - E_2$):

$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8
$$

$$
x_1 - x_3 = 2
$$

This produces Equation 3 ($E_3$) exactly. Because $E_3 = E_1 - E_2$, Equation 3 is redundant and provides no independent geometric constraint.

---

### 3. Parametric Solution Form

Converting the non-zero rows of the row echelon form matrix back to linear equations:

1. **Second equation:**

$$
x_2 + x_3 = 8 \implies x_2 = 8 - x_3
$$

2. **First equation:**

$$
x_1 + x_2 = 10 \implies x_1 + (8 - x_3) = 10 \implies x_1 - x_3 = 2 \implies x_1 = 2 + x_3
$$

Since column 3 contains no pivot, $x_3$ is the **free variable**. Setting $x_3 = t$ (where $t \in \mathbb{R}$), the solution set in scalar parametric form is:

$$
\begin{cases}
x_1 = 2 + t, \\
x_2 = 8 - t, \\
x_3 = t
\end{cases} \qquad (t \in \mathbb{R})
$$

In vector parametric form:

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 2 \\ 8 \\ 0 \end{pmatrix} + t \begin{pmatrix} 1 \\ -1 \\ 1 \end{pmatrix}
$$

---

### Verification

We test the solution vector by substituting it into all three original equations:

- **Equation 1 ($x_1 + x_2$):**

$$
(2 + t) + (8 - t) = 10 \quad (\text{Matches } 10)
$$

- **Equation 2 ($x_2 + x_3$):**

$$
(8 - t) + t = 8 \quad (\text{Matches } 8)
$$

- **Equation 3 ($x_1 - x_3$):**

$$
(2 + t) - t = 2 \quad (\text{Matches } 2)
$$

The solution is verified to be correct.