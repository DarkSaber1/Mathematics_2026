# Exercise 13 – Intersection of a Sphere and a Plane

## Problem Statement

Given the sphere

$$
x^2+y^2+z^2=25
$$

and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

## Solution

### 1. Equation and Radius of the Intersection Curve for $z = 3$

Substitute $z = 3$ into the sphere equation $x^2 + y^2 + z^2 = 25$:

$$
x^2 + y^2 + 3^2 = 25 \implies x^2 + y^2 + 9 = 25 \implies x^2 + y^2 = 16
$$

- **Equation of the Intersection Curve:**  
  In three-dimensional space $\mathbb{R}^3$, the intersection is defined by the system:

$$
\begin{cases}
x^2 + y^2 = 16, \\
z = 3
\end{cases}
$$

- **Geometric Description and Radius:**  
  This is a **circle** lying in the horizontal plane $z = 3$, centered at $(0, 0, 3)$, with radius:

$$
r = \sqrt{16} = 4
$$

---

### 2. General Behavior of the Intersection with $z = c$ Depending on $c$

The sphere $x^2 + y^2 + z^2 = 25$ is centered at $(0, 0, 0)$ with radius $R = 5$. Intersecting it with an arbitrary horizontal plane $z = c$ yields:

$$
x^2 + y^2 = 25 - c^2
$$

Depending on the value of $c$ relative to the sphere's vertical bounds $[-5, 5]$, there are four distinct cases:

1. **Case 1: $c = 0$ (Equatorial Great Circle)**  
  - Equation: $x^2 + y^2 = 25$ in the plane $z = 0$.
  - The plane passes directly through the center of the sphere, producing the largest possible circular cross-section ("great circle") with maximum radius $r(0) = 5$.

2. **Case 2: $0 < |c| < 5$ (Smaller Circles of Latitude)**  
- Equation: $x^2 + y^2 = 25 - c^2$ in the plane $z = c$.
  - Since $25 - c^2 > 0$, the intersection is a **circle** centered at $(0, 0, c)$ with radius:

$$
r(c) = \sqrt{25 - c^2}
$$

- As $|c|$ increases from $0$ toward $5$, the circle shrinks smoothly in radius.

3. **Case 3: $|c| = 5$ (i.e., $c = 5$ or $c = -5$ — Single Tangent Points)**  
- Equation: $x^2 + y^2 = 0$ in the plane $z = \pm 5$.
  - The plane is tangent to the sphere at its poles, so the intersection degenerates into a **single point** (a circle of radius $r = 0$): the North Pole $(0, 0, 5)$ when $c = 5$, and the South Pole $(0, 0, -5)$ when $c = -5$.

4. **Case 4: $|c| > 5$ (i.e., $c > 5$ or $c < -5$ — Empty Intersection)**  
- Equation: $x^2 + y^2 = 25 - c^2 < 0$.
  - Because $x^2 + y^2 \ge 0$ for all real $(x, y)$, there are **no real solutions** ($\emptyset$). The plane lies completely above or below the sphere and does not intersect it.