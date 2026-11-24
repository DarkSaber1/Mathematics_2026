# Exercise 9 – Distances

## Problem Statement

Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

## Solution

### 1. Distance from $P = (2, 3)$ to the Line $3x + 4y - 10 = 0$

In $\mathbb{R}^2$, the perpendicular distance $d(P, L)$ from a point $P = (x_0, y_0)$ to a line $ax + by + c = 0$ is given by:

$$
d(P, L) = \frac{|ax_0 + by_0 + c|}{\sqrt{a^2 + b^2}}
$$

Substituting $P = (2, 3)$ and the line coefficients $a = 3$, $b = 4$, $c = -10$:

$$
d(P, L) = \frac{|3(2) + 4(3) - 10|}{\sqrt{3^2 + 4^2}} = \frac{|6 + 12 - 10|}{\sqrt{9 + 16}} = \frac{|8|}{\sqrt{25}} = \frac{8}{5} = 1.6
$$

---

### 2. Distance from $Q = (2, -1, 3)$ to the Plane $2x - 2y + z - 4 = 0$

In $\mathbb{R}^3$, the perpendicular distance $d(Q, \Pi)$ from a point $Q = (x_0, y_0, z_0)$ to a plane $ax + by + cz + d = 0$ is given by:

$$
d(Q, \Pi) = \frac{|ax_0 + by_0 + cz_0 + d|}{\sqrt{a^2 + b^2 + c^2}}
$$

Substituting $Q = (2, -1, 3)$ and the plane coefficients $a = 2$, $b = -2$, $c = 1$, $d = -4$:

$$
d(Q, \Pi) = \frac{|2(2) - 2(-1) + 1(3) - 4|}{\sqrt{2^2 + (-2)^2 + 1^2}} = \frac{|4 + 2 + 3 - 4|}{\sqrt{4 + 4 + 1}} = \frac{|5|}{\sqrt{9}} = \frac{5}{3}
$$

---

### 3. Comparison of the Formulas and Connection with the Normal Direction

Comparing the two formulas reveals that they are the **exact same geometric formula** written in 2D and 3D:

- **Numerator (Scaled Normal Offset):** Evaluating the linear equation at the given point produces $n \cdot (P - P_0)$, where $P_0$ is any reference point on the line/plane (since $n \cdot P_0 + c = 0$ in 2D, and $n \cdot P_0 + d = 0$ in 3D).
- **Denominator (Length of the Normal Vector):** The square root term in both cases is simply the Euclidean norm $\|n\|$ of the normal vector—specifically $\|n\| = \sqrt{a^2 + b^2}$ for $n = (a, b)$ in $\mathbb{R}^2$, and $\|n\| = \sqrt{a^2 + b^2 + c^2}$ for $n = (a, b, c)$ in $\mathbb{R}^3$.

**Geometric Meaning:**  
Both formulas compute the length of the **orthogonal projection** of the displacement vector $\overrightarrow{P_0 P}$ onto the unit normal vector $\hat{n} = \frac{n}{\|n\|}$:

$$
\text{Distance} = \left| \overrightarrow{P_0 P} \cdot \frac{n}{\|n\|} \right| = \frac{|n \cdot (P - P_0)|}{\|n\|}
$$

Because the shortest path from a point to a hyperplane (a line in 2D or a plane in 3D) always travels strictly along the perpendicular normal direction, projecting onto $\hat{n}$ isolates that perpendicular distance directly.