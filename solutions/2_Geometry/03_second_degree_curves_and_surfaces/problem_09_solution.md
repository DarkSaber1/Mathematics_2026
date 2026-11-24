# Exercise 9 – Ellipsoid and Its Cross-Sections

## Problem Statement

Consider

$$
\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.
$$

Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

## Solution

### 1. Finding the Semiaxis Lengths

The canonical equation of an ellipsoid centered at the origin $(0, 0, 0)$ is:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1
$$

Comparing $\frac{x^2}{9} + \frac{y^2}{4} + \frac{z^2}{16} = 1$[cite: 1] directly with the canonical form:

- **Semiaxis along the $x$-axis:** $a = \sqrt{9} = 3$
- **Semiaxis along the $y$-axis:** $b = \sqrt{4} = 2$
- **Semiaxis along the $z$-axis:** $c_{\text{axis}} = \sqrt{16} = 4$

---

### 2. Describing the Cross-Section $z = 0$

Setting $z = 0$ intersects the ellipsoid with the horizontal $xy$-plane[cite: 1]:

$$
\frac{x^2}{9} + \frac{y^2}{4} + \frac{0^2}{16} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1
$$

- **Geometric Description:** This cross-section is an **ellipse** in the plane $z = 0$ centered at $(0, 0, 0)$ with horizontal semiaxes $a = 3$ (along $x$) and $b = 2$ (along $y$). This is the widest horizontal slice ("equator") of the ellipsoid.

---

### 3. How the Cross-Sections $z = c$ Change for $|c| < 4$

Intersecting the ellipsoid with a horizontal plane $z = c$ (where $|c| < 4$, i.e., $-4 < c < 4$) gives[cite: 1]:

$$
\frac{x^2}{9} + \frac{y^2}{4} = 1 - \frac{c^2}{16}
$$

Since $|c| < 4$, we have $\frac{c^2}{16} < 1$, so the right-hand side $k(c) = 1 - \frac{c^2}{16}$ is strictly positive ($0 < k(c) \le 1$). Dividing both sides by $k(c)$ brings the slice into canonical ellipse form:

$$
\frac{x^2}{9\left(1 - \frac{c^2}{16}\right)} + \frac{y^2}{4\left(1 - \frac{c^2}{16}\right)} = 1
$$

From this family of equations, the cross-sections evolve as follows:

- **Constant Shape and Aspect Ratio:** For every $c \in (-4, 4)$, the slice is an **ellipse** centered at $(0, 0, c)$ whose semiaxes scale by the exact same factor $\sqrt{1 - \frac{c^2}{16}}$:

$$
a(c) = 3\sqrt{1 - \frac{c^2}{16}}, \qquad b(c) = 2\sqrt{1 - \frac{c^2}{16}}
$$

  Because $\frac{a(c)}{b(c)} = \frac{3}{2}$ for all $c$, every horizontal slice is geometrically similar to the equatorial ellipse at $z = 0$.
- **Behavior as $|c|$ Increases from $0$ toward $4$:**
  - At $c = 0$, the ellipse reaches its maximum size ($a(0) = 3$, $b(0) = 2$).
  - As $|c|$ increases toward $4$ (moving either upward toward $z = 4$ or downward toward $z = -4$), the scaling factor $\sqrt{1 - \frac{c^2}{16}}$ decreases smoothly toward $0$, so the ellipses shrink continuously while remaining concentric around the $z$-axis.
  - At the boundary values $c = \pm 4$, $1 - \frac{c^2}{16} = 0$, and the ellipse degenerates into a single tangent pole point: $(0, 0, 4)$ at the top and $(0, 0, -4)$ at the bottom. (For $|c| > 4$, $1 - \frac{c^2}{16} < 0$, so the plane misses the ellipsoid completely.)