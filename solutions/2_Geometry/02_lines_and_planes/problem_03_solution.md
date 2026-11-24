# Exercise 3 – Plane Through a Point with a Given Normal Vector

## Problem Statement

Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

## Solution

### 1. Constructing the Equation of the Plane

A plane passing through a known point $P = (x_0, y_0, z_0)$ with a normal vector $n = (a, b, c)$ consists of all points $X = (x, y, z)$ in $\mathbb{R}^3$ such that the displacement vector $\overrightarrow{PX} = X - P$ is perpendicular to $n$:

$$
n \cdot (X - P) = 0 \iff a(x - x_0) + b(y - y_0) + c(z - z_0) = 0
$$

Substituting $P = (1, -2, 3)$ and $n = (2, 1, -1)$:

$$
2(x - 1) + 1(y - (-2)) - 1(z - 3) = 0
$$

$$
2(x - 1) + (y + 2) - (z - 3) = 0
$$

Expanding and simplifying the constants gives the general scalar equation of the plane:

$$
2x - 2 + y + 2 - z + 3 = 0 \implies 2x + y - z + 3 = 0
$$

*(Equivalently, written as $2x + y - z = -3$.)*

---

### 2. Checking the Result by Substituting $P = (1, -2, 3)$

We verify that $P = (1, -2, 3)$ lies on the plane by plugging its coordinates into the left-hand side of $2x + y - z + 3 = 0$:

$$
2(1) + (-2) - (3) + 3 = 2 - 2 - 3 + 3 = 0
$$

Since $0 = 0$, the point $P$ satisfies the equation.

---

### 3. Role of the Normal Vector

- **Fixing the Orientation (Tilt) in Space:**  
  In $\mathbb{R}^3$, a single vector $n = (2, 1, -1)$ uniquely defines a two-dimensional orthogonal complement—the family of all planes perpendicular to $n$. In the general plane equation $ax + by + cz + d = 0$, the coefficients $(a, b, c)$ of $x, y,$ and $z$ are directly the components of the normal vector $n$.
- **Filtering Out Points Not on the Plane:**  
  A point $X$ belongs to the plane if and only if moving from $P$ to $X$ involves zero displacement in the direction of $n$ (i.e., $n \cdot \overrightarrow{PX} = 0$). Choosing the specific point $P = (1, -2, 3)$ fixes the constant term $d = 3$, selecting the unique plane from that parallel family that passes through $P$.