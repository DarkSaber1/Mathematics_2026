# Exercise 7 – A Line Relative to a Plane

## Problem Statement

For

$$
L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,
$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

## Solution

### 1. Extracting the Direction Vector and Normal Vector

From the parametric equation of the line $L : (x, y, z) = (1, 1, 0) + t(1, -1, 0)$, we identify a base point $P_0$ on the line and its direction vector $v$:

$$
P_0 = (1, 1, 0), \qquad v = (1, -1, 0)
$$

From the scalar equation of the plane $\Pi : x + y + z = 2$, the coefficients of $x, y, z$ give a normal vector $n$ perpendicular to $\Pi$:

$$
n = (1, 1, 1)
$$

---

### 2. Testing Parallelism Using $v \cdot n$

We compute the dot product of the line's direction vector $v = (1, -1, 0)$ and the plane's normal vector $n = (1, 1, 1)$:

$$
v \cdot n = (1)(1) + (-1)(1) + (0)(1) = 1 - 1 + 0 = 0
$$

Since $v \cdot n = 0$, the direction vector $v$ is perpendicular (orthogonal) to the normal vector $n$. Because $n$ is perpendicular to the plane $\Pi$, this means the line $L$ runs parallel to the plane $\Pi$. Therefore, $L$ **cannot intersect $\Pi$ at a single point**; it must either be **strictly parallel to $\Pi$ (no common points)** or **lie entirely inside $\Pi$**.

---

### 3. Testing Whether the Line Lies in the Plane

To distinguish between the two parallel cases, we test whether the base point $P_0 = (1, 1, 0)$ of $L$ satisfies the equation of the plane $\Pi : x + y + z = 2$:

$$
1 + 1 + 0 = 2 \quad (\text{True})
$$

Since $P_0 = (1, 1, 0)$ lies on $\Pi$ and the line moves exclusively in a direction parallel to $\Pi$, every point $(1 + t,\, 1 - t,\, 0)$ on $L$ satisfies $(1 + t) + (1 - t) + 0 = 2$.

Thus, the line $L$ **lies entirely in the plane $\Pi$**.

---

### 4. Role of the Dot Product $v \cdot n$

The dot product $v \cdot n$ serves as the fundamental orientation test between a line and a plane:

- **When $v \cdot n \neq 0$:** The direction vector $v$ is not perpendicular to the normal $n$, meaning the line approaches the plane at a non-zero angle and must pierce it at **one unique intersection point**.
- **When $v \cdot n = 0$:** The direction vector $v$ is perpendicular to the normal $n$, which means the line maintains a constant signed distance from the plane and is **parallel** to it. In this case, checking a single point $P_0 \in L$ determines whether that constant distance is zero (line contained in the plane) or non-zero (strictly parallel, zero intersection points).