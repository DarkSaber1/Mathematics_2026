# Exercise 6 – Angle Between Planes

## Problem Statement

Given

$$
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

## Solution

### 1. Extracting Normal Vectors and Testing for Parallelism

For a plane in general scalar form $ax + by + cz = d$, the coefficients $(a, b, c)$ give a normal vector perpendicular to the plane. Extracting the normal vectors for $\Pi_1$ and $\Pi_2$:

$$
n_1 = (1, 1, 1), \qquad n_2 = (1, -1, 0)
$$

Two planes are parallel if and only if their normal vectors are scalar multiples of one another ($n_1 = k n_2$ for some $k \in \mathbb{R}$). Comparing the third components gives $1 = k \cdot 0 = 0$, which is impossible.

Therefore, $n_1$ and $n_2$ are not parallel, so the planes $\Pi_1$ and $\Pi_2$ are **not parallel** (they intersect along a straight line).

---

### 2. Computing the Angle Between the Planes

The acute angle $\theta \in [0^\circ, 90^\circ]$ between two intersecting planes is equal to the acute angle between their normal vectors $n_1$ and $n_2$, given by:

$$
\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\|\,\|n_2\|}
$$

First, compute the dot product $n_1 \cdot n_2$ and the Euclidean norms $\|n_1\|$ and $\|n_2\|$:

$$
n_1 \cdot n_2 = (1)(1) + (1)(-1) + (1)(0) = 1 - 1 + 0 = 0
$$

$$
\|n_1\| = \sqrt{1^2 + 1^2 + 1^2} = \sqrt{3}
$$

$$
\|n_2\| = \sqrt{1^2 + (-1)^2 + 0^2} = \sqrt{2}
$$

Substituting these into the cosine formula:

$$
\cos\theta = \frac{|0|}{\sqrt{3} \cdot \sqrt{2}} = 0
$$

Taking the inverse cosine for $\theta \in [0^\circ, 90^\circ]$:

$$
\theta = \arccos(0) = 90^\circ \quad \left(\text{or } \frac{\pi}{2}\text{ radians}\right)
$$

Thus, the planes $\Pi_1$ and $\Pi_2$ are **perpendicular (orthogonal)** to each other.

---

### 3. Why Normal Vectors Alone Are Enough for This Calculation

- **Invariance to Translation:** The constant terms $d_1 = 1$ and $d_2 = 2$ only shift the planes parallel to themselves without changing their tilt or orientation in space. Two planes tilted at the same angles will always intersect at the same dihedral angle regardless of where they sit in $\mathbb{R}^3$.
- **Geometric Rigid Rotation:** Because $n_1$ is rigidly fixed at $90^\circ$ to $\Pi_1$ and $n_2$ is rigidly fixed at $90^\circ$ to $\Pi_2$, rotating from $\Pi_1$ to $\Pi_2$ in a cross-section perpendicular to their intersection line rotates $n_1$ to $n_2$ by the **exact same angle** $\theta$. Therefore, finding the angle between two planes reduces completely to finding the angle between their normal vectors.