# Exercise 4 – Parabola

## Problem Statement

For

$$
y^2=12x,
$$

identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x=3$ and use them to make a sketch.

## Solution

### 1. Identifying the Basic Geometric Features

Comparing $y^2 = 12x$ with the canonical horizontal parabola equation $y^2 = 2px$ (where $2p = 12 \implies p = 6$):

- **Vertex:** $(0, 0)$, because there are no linear shift terms in $x$ or $y$ (both $x = 0$ and $y = 0$ satisfy $0^2 = 12(0)$).
- **Axis of Symmetry:** The **$x$-axis** (given by the line $y = 0$), since replacing $y$ with $-y$ yields $(-y)^2 = y^2 = 12x$, leaving the equation completely unchanged.
- **Opening Direction:** The parabola opens **to the right** (in the positive $x$-direction). Rearranging for $x$ gives:

$$
x = \frac{y^2}{12}
$$

  Since $y^2 \ge 0$ for all real $y$, every point on the curve must satisfy $x \ge 0$, with $x$ growing unboundedly as $|y|$ increases.

---

### 2. Finding Points on the Parabola for $x = 3$

Substitute $x = 3$ into $y^2 = 12x$:

$$
y^2 = 12(3) = 36 \implies y = \pm\sqrt{36} = \pm 6
$$

This produces two symmetric points on the parabola:

- **Upper point:** $P_1 = (3, 6)$
- **Lower point:** $P_2 = (3, -6)$

---

### 3. Geometric Description of the Sketch

- **Anchor Points:** The curve starts at its vertex $(0, 0)$ with a vertical tangent line ($x = 0$), passes smoothly through $(3, 6)$ in the first quadrant and $(3, -6)$ in the fourth quadrant, and continues opening wider to the right.
- **Symmetry:** The upper branch ($y = \sqrt{12x}$) and lower branch ($y = -\sqrt{12x}$) are exact mirror images across the $x$-axis ($y = 0$), and no part of the curve exists in the left half-plane ($x < 0$).