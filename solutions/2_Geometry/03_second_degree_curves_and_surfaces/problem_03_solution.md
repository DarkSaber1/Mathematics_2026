# Exercise 3 – Ellipse

## Problem Statement

For

$$
\frac{x^2}{25}+\frac{y^2}{9}=1,
$$

find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

## Solution

### 1. Finding the Semiaxis Lengths

The canonical equation of an ellipse centered at the origin $(0, 0)$ is:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

Comparing $\frac{x^2}{25} + \frac{y^2}{9} = 1$ directly with the canonical form:

- **Horizontal Semiaxis Length ($a$):**

$$
a^2 = 25 \implies a = \sqrt{25} = 5
$$

- **Vertical Semiaxis Length ($b$):**

$$
b^2 = 9 \implies b = \sqrt{9} = 3
$$

---

### 2. Finding the Intercepts with the Coordinate Axes

- **Intercepts with the $x$-axis (Vertices):**  
  Set $y = 0$ in the equation:

$$
\frac{x^2}{25} + \frac{0^2}{9} = 1 \implies \frac{x^2}{25} = 1 \implies x^2 = 25 \implies x = \pm 5
$$

  This gives the two $x$-intercepts: $(-5, 0)$ and $(5, 0)$.

- **Intercepts with the $y$-axis (Co-vertices):**  
  Set $x = 0$ in the equation:

$$
\frac{0^2}{25} + \frac{y^2}{9} = 1 \implies \frac{y^2}{9} = 1 \implies y^2 = 9 \implies y = \pm 3
$$

  This gives the two $y$-intercepts: $(0, -3)$ and $(0, 3)$.

---

### 3. Geometric Description of the Sketch

- **Center and Symmetry:** The ellipse is centered at $(0, 0)$ and symmetric across both the $x$-axis and $y$-axis (replacing $x \to -x$ or $y \to -y$ leaves the equation unchanged).
- **Bounding Box:** The curve lies completely inside the rectangle $[-5, 5] \times [-3, 3]$, smoothly connecting the four axis intercepts $(-5, 0) \to (0, 3) \to (5, 0) \to (0, -3) \to (-5, 0)$ with horizontal tangents at $(0, \pm 3)$ and vertical tangents at $(\pm 5, 0)$.

---

### 4. Direction of Greater Stretch and How It Appears in the Equation

- **Direction of Stretch:** The ellipse is more stretched **horizontally along the $x$-axis**, spanning a total width of $2a = 10$ units compared to a total vertical height of $2b = 6$ units.
- **How This Is Visible in the Equation:**  
  In $\frac{x^2}{25} + \frac{y^2}{9} = 1$, the denominator under $x^2$ ($25$) is larger than the denominator under $y^2$ ($9$). Because $x^2$ is divided by a larger number, $x$ must reach a larger magnitude ($|x| = 5$) before $\frac{x^2}{25}$ reaches $1$, whereas $y$ only needs to reach $|y| = 3$ for $\frac{y^2}{9}$ to reach $1$. Thus, the larger denominator immediately identifies the major axis of the ellipse.