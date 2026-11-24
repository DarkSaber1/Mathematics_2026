# Exercise 2 – A Line in Space

## Problem Statement

Given

$$
L:(x,y,z)=(2,-1,3)+t(1,2,-2).
$$

State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

## Solution

### 1. Identifying a Point on the Line and Its Direction Vector

The parametric vector equation of a line in $\mathbb{R}^3$ has the form $(x, y, z) = P_0 + tv$, where $P_0$ is a fixed initial point on the line (corresponding to $t = 0$) and $v$ is a direction vector parallel to the line.

Comparing directly with $L : (x, y, z) = (2, -1, 3) + t(1, 2, -2)$:

- **A point on the line:**

$$
P_0 = (2, -1, 3)
$$

- **Direction vector:**

$$
v = (1, 2, -2)
$$

---

### 2. Checking Whether $P = (4, 3, -1)$ Lies on $L$

A point $P = (4, 3, -1)$ lies on $L$ if and only if there exists a single real parameter value $t \in \mathbb{R}$ that simultaneously satisfies all three scalar parametric equations:

$$
\begin{cases}
4 = 2 + 1t \\
3 = -1 + 2t \\
-1 = 3 - 2t
\end{cases}
$$

We solve each equation independently for $t$:

- From the $x$-coordinate:

$$
4 = 2 + t \implies t = 4 - 2 = 2
$$

- From the $y$-coordinate:

$$
3 = -1 + 2t \implies 2t = 4 \implies t = 2
$$

- From the $z$-coordinate:

$$
-1 = 3 - 2t \implies -2t = -4 \implies t = 2
$$

Since all three coordinate equations yield the **exact same** parameter value $t = 2$, the point $P = (4, 3, -1)$ **does lie** on the line $L$.

---

### 3. Finding the Point Corresponding to $t = -1$

To find the point $Q$ on $L$ corresponding to $t = -1$, substitute $t = -1$ into the line equation:

$$
Q = (2, -1, 3) + (-1)(1, 2, -2)
$$

$$
Q = (2, -1, 3) + (-1, -2, 2) = (2 - 1,\, -1 - 2,\, 3 + 2) = (1, -3, 5)
$$

Thus, the point on $L$ corresponding to $t = -1$ is:

$$
Q = (1, -3, 5)
$$