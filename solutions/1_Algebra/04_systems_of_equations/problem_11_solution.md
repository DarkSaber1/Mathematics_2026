# Exercise 11 – A Parameter in a System of Three Equations

## Problem Statement

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Solution

### 1. Gaussian Elimination

We set up the augmented matrix $[A \mid b]$:

$$
[A \mid b] = \left(\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 1 & t & 1 & 2 \\ 1 & 1 & t & 3 \end{array}\right)
$$

- **Step 1:** Eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - R_1$:

$$
R_2 \text{ calculation: } (1, t, 1, 2) - (1, 1, 1, 1) = (0, t-1, 0, 1)
$$

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & t-1 & 0 & 1 \\ 1 & 1 & t & 3 \end{array}\right)
$$

- **Step 2:** Eliminate $x$ from row 3 by performing $R_3 \leftarrow R_3 - R_1$:

$$
R_3 \text{ calculation: } (1, 1, t, 3) - (1, 1, 1, 1) = (0, 0, t-1, 2)
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & t-1 & 0 & 1 \\ 0 & 0 & t-1 & 2 \end{array}\right)
$$

---

### 2. Parameter Case Analysis

We analyze the system equations derived from the row echelon form:

1. **Third row equation:**

$$
(t - 1)z = 2
$$

2. **Second row equation:**

$$
(t - 1)y = 1
$$

3. **First row equation:**

$$
x + y + z = 1
$$

#### Case 1: $t = 1$
When $t = 1$, the second and third row equations yield immediate contradictions:
- Second row: $(1 - 1)y = 1 \implies 0y = 1 \implies 0 = 1$
- Third row: $(1 - 1)z = 2 \implies 0z = 2 \implies 0 = 2$

Since $0 = 1$ and $0 = 2$ are logical impossibilities, for **$t = 1$**, the system has **no solution**.

#### Case 2: $t \neq 1$
When $t \neq 1$, the coefficient $(t - 1)$ is non-zero, allowing valid division by $(t - 1)$:

1. **Solve for $z$:**

$$
z = \frac{2}{t - 1}
$$

2. **Solve for $y$:**

$$
y = \frac{1}{t - 1}
$$

3. **Solve for $x$:**

$$
x = 1 - y - z = 1 - \frac{1}{t - 1} - \frac{2}{t - 1} = 1 - \frac{3}{t - 1} = \frac{t - 1 - 3}{t - 1} = \frac{t - 4}{t - 1}
$$

Thus, for any $t \neq 1$, there exists a unique solution vector:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} \frac{t - 4}{t - 1} \\ \frac{1}{t - 1} \\ \frac{2}{t - 1} \end{pmatrix}
$$

Therefore, for **$t \neq 1$**, the system has **exactly one solution**.

---

### 3. Summary of Solution Cases

1. **No solution:** Occurs if and only if $t = 1$.
2. **Exactly one solution:** Occurs for all $t \in \mathbb{R} \setminus \{1\}$.
3. **Infinitely many solutions:** **Cannot occur** for any real value of $t$.