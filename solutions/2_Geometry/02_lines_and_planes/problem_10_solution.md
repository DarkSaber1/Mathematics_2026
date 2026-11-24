# Exercise 10 – Projection of a Point onto a Plane

## Problem Statement

Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

## Solution

### 1. Finding the Orthogonal Projection $P'$ of $P$ onto the Plane

From the plane equation $\Pi : x + y + z = 3$, we extract the normal vector:

$$
n = (1, 1, 1)
$$

The orthogonal projection $P'$ of $P = (2, 1, 3)$ onto $\Pi$ is the intersection of the plane $\Pi$ with the line $L$ passing through $P$ in the direction of $n$. The parametric equation of this normal line $L$ is:

$$
L : (x, y, z) = (2, 1, 3) + t(1, 1, 1) \implies \begin{cases} x = 2 + t \\ y = 1 + t \\ z = 3 + t \end{cases}
$$

Substitute these parametric coordinates into the plane equation $x + y + z = 3$:

$$
(2 + t) + (1 + t) + (3 + t) = 3
$$

$$
6 + 3t = 3 \implies 3t = -3 \implies t = -1
$$

Substituting $t = -1$ back into the line equation gives the orthogonal projection $P'$:

$$
P' = (2 + (-1),\, 1 + (-1),\, 3 + (-1)) = (1, 0, 2)
$$

---

### 2. Finding the Reflection $P''$ of $P$ Across the Plane

Geometrically, the orthogonal projection $P'$ is the exact midpoint between the original point $P$ and its reflection $P''$ across the plane. Moving from $P$ to $P'$ required a displacement corresponding to $t = -1$ along $n$; continuing an equal distance past the plane corresponds to $t = -2$ (or equivalently, $P'' = 2P' - P$):

$$
P'' = 2(1, 0, 2) - (2, 1, 3) = (2 - 2,\, 0 - 1,\, 4 - 3) = (0, -1, 1)
$$

*(Equivalently, using $t = -2$ in $L$: $(2 - 2,\, 1 - 2,\, 3 - 2) = (0, -1, 1)$.)*

Thus, the reflection of $P$ across the plane is:

$$
P'' = (0, -1, 1)
$$

---

### 3. Checking That the Midpoint Lies on the Plane

First, compute the midpoint $M$ of the segment joining $P = (2, 1, 3)$ and its reflection $P'' = (0, -1, 1)$:

$$
M = \left( \frac{2 + 0}{2},\, \frac{1 + (-1)}{2},\, \frac{3 + 1}{2} \right) = (1, 0, 2)
$$

Notice that $M = (1, 0, 2)$ equals our projection point $P'$. Substituting $M = (1, 0, 2)$ into the plane equation $x + y + z = 3$:

$$
1 + 0 + 2 = 3 \quad (\text{True})
$$

Since $M$ satisfies the plane equation, the midpoint of the segment $PP''$ is verified to lie directly on the plane.