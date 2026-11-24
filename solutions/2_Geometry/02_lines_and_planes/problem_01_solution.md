# Exercise 1 – Line Through Two Points

## Problem Statement

Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## Solution

### 1. Finding a Direction Vector and the Parametric Form

Given two distinct points $A = (1, 2)$ and $B = (4, -1)$ in $\mathbb{R}^2$, a direction vector $v$ pointing along the line from $A$ to $B$ is obtained by subtracting the coordinates of $A$ from $B$:

$$
v = \overrightarrow{AB} = B - A = (4 - 1,\, -1 - 2) = (3, -3)
$$

(Note: Any non-zero scalar multiple of $(3, -3)$, such as $(1, -1)$, is also a valid direction vector.)

Using $A = (1, 2)$ as the initial point and $v = (3, -3)$ as the direction vector, the vector parametric equation of the line is $(x, y) = A + tv$, or in scalar component form:

$$
\begin{cases}
x = 1 + 3t \\
y = 2 - 3t
\end{cases}
\qquad (t \in \mathbb{R})
$$

---

### 2. Finding a Normal Vector and the General Form

In $\mathbb{R}^2$, a normal vector $n = (n_1, n_2)$ is perpendicular to the direction vector $v = (3, -3)$, meaning $n \cdot v = 0$. Swapping the components of $v$ and negating one gives:

$$
n = (3, 3) \quad \text{or simplified by dividing by } 3: \quad n = (1, 1)
$$

We verify orthogonality: $n \cdot v = (1)(3) + (1)(-3) = 3 - 3 = 0$.

Using the point-normal form $n \cdot \bigl((x, y) - A\bigr) = 0$ with $n = (1, 1)$ and $A = (1, 2)$:

$$
1(x - 1) + 1(y - 2) = 0
$$

$$
x - 1 + y - 2 = 0 \implies x + y - 3 = 0
$$

*(Alternatively, eliminating $t$ from the parametric equations by adding $x = 1 + 3t$ and $y = 2 - 3t$ yields $x + y = 3$, i.e., $x + y - 3 = 0$.)*

Thus, the **general form** of the line is:

$$
x + y - 3 = 0
$$

---

### 3. Summary of Key Vectors

- **Direction Vector:** $v = (3, -3)$ (or $v = (1, -1)$)
- **Normal Vector:** $n = (1, 1)$ (or $n = (3, 3)$)

---

### 4. Checking That Both Points Satisfy the Equations

- **Verification in the General Form ($x + y - 3 = 0$):**
  - For $A = (1, 2)$:

$$
1 + 2 - 3 = 0 \quad (\text{True})
$$

  - For $B = (4, -1)$:

$$
4 + (-1) - 3 = 0 \quad (\text{True})
$$

- **Verification in the Parametric Form ($x = 1 + 3t,\, y = 2 - 3t$):**
  - Setting $t = 0$ gives $(x, y) = (1 + 0,\, 2 - 0) = (1, 2) = A$.
  - Setting $t = 1$ gives $(x, y) = (1 + 3,\, 2 - 3) = (4, -1) = B$.

Both points $A$ and $B$ satisfy both forms of the line equation.