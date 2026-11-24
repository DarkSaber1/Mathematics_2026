# Exercise 5 – Hyperbola and Asymptotes

## Problem Statement

For

$$
\frac{x^2}{16}-\frac{y^2}{9}=1,
$$

find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

## Solution

### 1. Finding the Intercepts with the $x$-Axis

To find where the hyperbola crosses the $x$-axis, set $y = 0$ in the equation:

$$
\frac{x^2}{16} - \frac{0^2}{9} = 1 \implies \frac{x^2}{16} = 1 \implies x^2 = 16 \implies x = \pm 4
$$

This gives the two vertices ($x$-intercepts) of the hyperbola:

- **Left Vertex:** $(-4, 0)$
- **Right Vertex:** $(4, 0)$

*(Note: Setting $x = 0$ yields $-\frac{y^2}{9} = 1$, which has no real solutions, confirming there are no $y$-intercepts and no points on the curve for $-4 < x < 4$.)*

---

### 2. Finding the Asymptotes

Comparing $\frac{x^2}{16} - \frac{y^2}{9} = 1$ with the canonical hyperbola form $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$, we identify:

$$
a = \sqrt{16} = 4, \qquad b = \sqrt{9} = 3
$$

Replacing the constant $1$ on the right-hand side with $0$ gives the combined equation of the asymptotes:

$$
\frac{x^2}{16} - \frac{y^2}{9} = 0 \implies \frac{y^2}{9} = \frac{x^2}{16} \implies y = \pm \frac{3}{4}x
$$

Thus, the two asymptote lines are:

- **Positive-slope asymptote:** $y = \frac{3}{4}x$
- **Negative-slope asymptote:** $y = -\frac{3}{4}x$

---

### 3. Geometric Description of the Sketch

- **Central Reference Rectangle:** Draw the guide rectangle centered at $(0, 0)$ bounded by $x = \pm 4$ and $y = \pm 3$. The diagonals of this rectangle extend infinitely to form the asymptotes $y = \pm \frac{3}{4}x$.
- **Two Open Branches:**
  - The **right branch** starts at the vertex $(4, 0)$ with a vertical tangent, opens to the right in the region $x \ge 4$, and approaches $y = \frac{3}{4}x$ from below (in the first quadrant) and $y = -\frac{3}{4}x$ from above (in the fourth quadrant).
  - The **left branch** starts at the vertex $(-4, 0)$ with a vertical tangent, opens to the left in the region $x \le -4$, and approaches the same two asymptote lines symmetrically.

---

### 4. Why the Asymptotes Describe Behavior Far from the Center

Solving the hyperbola equation explicitly for $y$ in terms of $x$ gives:

$$
\frac{y^2}{9} = \frac{x^2}{16} - 1 = \frac{x^2}{16}\left(1 - \frac{16}{x^2}\right) \implies y = \pm \frac{3}{4}|x|\sqrt{1 - \frac{16}{x^2}}
$$

Far from the center $(0, 0)$, when $|x|$ becomes very large ($|x| \gg 4$), the correction term $\frac{16}{x^2}$ approaches $0$:

$$
\lim_{|x| \to \infty} \frac{16}{x^2} = 0 \implies \sqrt{1 - \frac{16}{x^2}} \approx 1
$$

Consequently, for large $|x|$, the curve satisfies $y \approx \pm \frac{3}{4}x$ (specifically, the vertical gap between the hyperbola and its asymptotes shrinks toward zero as $|x| \to \infty$). Geometrically, the constant $1$ becomes negligible compared to $\frac{x^2}{16}$ and $\frac{y^2}{9}$, so the hyperbola hugs the lines $\frac{x^2}{16} - \frac{y^2}{9} = 0$ arbitrarily closely at large distances from the origin.