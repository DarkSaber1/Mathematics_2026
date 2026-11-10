# Exercise 6 – A System with a Parameter — Which Cases Actually Occur?

## Problem Statement

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## Solution

### 1. Gaussian Elimination Matrix Analysis

We construct the augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{cc|c} 1 & 1 & 2 \\ a & a & 4 \end{array}\right)
$$

We eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - a R_1$:

$$
R_2 \text{ calculation: } (a, a, 4) - a(1, 1, 2) = (a - a, a - a, 4 - 2a) = (0, 0, 4 - 2a)
$$

The resulting matrix in row echelon form is:

$$
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 4 - 2a \end{array}\right)
$$

The second row translates to the equation:

$$
0x + 0y = 4 - 2a \implies 0 = 4 - 2a
$$

---

### 2. Parameter Case Analysis

We analyze the system based on the right-hand side value $4 - 2a$:

- **Case 1: $4 - 2a \neq 0$ (i.e., $a \neq 2$)**
  - If $a \neq 2$, the equation becomes $0 = 4 - 2a$, where the right-hand side is non-zero.
  - This produces an immediate contradiction ($0 = \text{non-zero constant}$).
  - Therefore, for **$a \neq 2$**, the system has **no solution**.

- **Case 2: $4 - 2a = 0$ (i.e., $a = 2$)**
  - Substituting $a = 2$ gives the second row equation $0x + 0y = 0$, which simplifies to $0 = 0$.
  - The second equation becomes completely redundant, leaving only one independent equation:

$$
x + y = 2 \implies x = 2 - y
$$

  - Choosing $y = t$ (where $t \in \mathbb{R}$) as the free variable yields the parametric solution form:

$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2 \\ 0 \end{pmatrix} + t \begin{pmatrix} -1 \\ 1 \end{pmatrix}
$$

  - Therefore, for **$a = 2$**, the system has **infinitely many solutions**.

---

### 3. Summary of Occurring Cases

1. **No solution:** Occurs for all $a \in \mathbb{R} \setminus \{2\}$.
2. **Infinitely many solutions:** Occurs for $a = 2$.
3. **Exactly one solution:** **Cannot occur** for any value of $a$.

### Explanation of Why "Exactly One Solution" Cannot Occur

The coefficient matrix of the system is:

$$
A = \begin{pmatrix} 1 & 1 \\ a & a \end{pmatrix}
$$

The determinant of $A$ is:

$$
\det(A) = (1)(a) - (1)(a) = a - a = 0
$$

Since $\det(A) = 0$ for **all** values of $a \in \mathbb{R}$, the coefficient matrix $A$ is singular (non-invertible) for every real number $a$. A linear system with a singular square coefficient matrix can never have a unique (exactly one) solution; it can only have either no solution or infinitely many solutions.