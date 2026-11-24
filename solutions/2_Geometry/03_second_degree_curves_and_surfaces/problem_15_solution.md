# Exercise 15 – Recognition and Sketch Without a Given Name

## Problem Statement

Consider the two equations:

$$
4x^2+9y^2-8x+36y+4=0,
$$

$$
4x^2+y^2=z^2.
$$

For the first equation, reduce it to canonical form, recognize the curve, give its most important features, and make a sketch.

For the second equation, do not begin by using a ready-made name for the surface. First describe the cross-sections $z=c$ and the cross-sections by the planes $x=0$ and $y=0$, paying attention to the different scales along the axes. Only then identify the surface and make a sketch.

## Solution

### Part 1: First Equation — $4x^2 + 9y^2 - 8x + 36y + 4 = 0$

#### 1. Reducing to Canonical Form by Completing the Square
Group the $x$- and $y$-terms separately, move the constant $4$ to the right-hand side, and factor out the leading coefficients $4$ and $9$:

$$
4(x^2 - 2x) + 9(y^2 + 4y) = -4
$$

Complete the square inside each set of parentheses:
- For $x^2 - 2x$: add $(-1)^2 = 1$ inside the parentheses, which adds $4 \cdot 1 = 4$ to the left-hand side.
- For $y^2 + 4y$: add $(2)^2 = 4$ inside the parentheses, which adds $9 \cdot 4 = 36$ to the left-hand side.

Balance the equation by adding $4 + 36 = 40$ to the right-hand side:

$$
4(x^2 - 2x + 1) + 9(y^2 + 4y + 4) = -4 + 4 + 36
$$

Rewrite the squared binomials and simplify the right-hand side:

$$
4(x - 1)^2 + 9(y + 2)^2 = 36
$$

Divide both sides by $36$ to bring the equation to **canonical form**[cite: 1]:

$$
\frac{4(x - 1)^2}{36} + \frac{9(y + 2)^2}{36} = 1 \implies \frac{(x - 1)^2}{9} + \frac{(y + 2)^2}{4} = 1
$$

#### 2. Curve Recognition and Key Features
- **Curve Type:** **Shifted Ellipse** (both squared terms are positive with distinct denominators and sum to $1$).
- **Center:** $(x_0, y_0) = (1, -2)$
- **Semiaxis Lengths:**
  - Horizontal major semiaxis: $a = \sqrt{9} = 3$
  - Vertical minor semiaxis: $b = \sqrt{4} = 2$
- **Vertices (Endpoints of Major Axis):** $(1 - 3, -2) = (-2, -2)$ and $(1 + 3, -2) = (4, -2)$
- **Co-vertices (Endpoints of Minor Axis):** $(1, -2 - 2) = (1, -4)$ and $(1, -2 + 2) = (1, 0)$ (notice $(1, 0)$ is tangent to the $x$-axis).

#### 3. Geometric Description of the Sketch
The curve is a horizontally elongated oval centered at $(1, -2)$ in the fourth quadrant, enclosed inside the bounding rectangle $[-2, 4] \times [-4, 0]$. It smoothly connects $(-2, -2) \to (1, 0) \to (4, -2) \to (1, -4) \to (-2, -2)$, touching the $x$-axis tangentially at $(1, 0)$ and crossing the $y$-axis twice near $y = -2 \pm \frac{4\sqrt{2}}{3} \approx -2 \pm 1.89$.

---

### Part 2: Second Equation — $4x^2 + y^2 = z^2$

#### 1. Analyzing Cross-Sections Before Naming the Surface
1. **Horizontal Cross-Sections $z = c$ (planes parallel to the $xy$-plane):**  
   Substituting $z = c$ yields[cite: 1]:

$$
4x^2 + y^2 = c^2
$$

   - **For $c = 0$:** $4x^2 + y^2 = 0$, which has only the single real solution $(x, y, z) = (0, 0, 0)$ (a **single point** at the origin).
   - **For $c \neq 0$:** Dividing both sides by $c^2 > 0$ puts the slice into canonical ellipse form:

$$
\frac{x^2}{\left(\frac{|c|}{2}\right)^2} + \frac{y^2}{|c|^2} = 1
$$

     Every horizontal slice at height $z = c \neq 0$ is an **ellipse** centered on the $z$-axis at $(0, 0, c)$ whose semiaxes scale linearly with $|c|$:
     - **Semiaxis along the $x$-direction:** $a(c) = \frac{|c|}{2}$
     - **Semiaxis along the $y$-direction:** $b(c) = |c|$
     - **Scale Comparison:** Because $b(c) = 2\,a(c)$, every horizontal cross-section is stretched **twice as wide along the $y$-axis as along the $x$-axis** (a $1 : 2$ aspect ratio between the $x$- and $y$-directions).

2. **Vertical Cross-Section by the Plane $x = 0$ (in the $yz$-plane):**  
   Setting $x = 0$ gives[cite: 1]:

$$
y^2 = z^2 \implies z = \pm y
$$

   This consists of **two intersecting straight lines** ($z = y$ and $z = -y$) crossing at $(0, 0, 0)$ at a $45^\circ$ angle to the $y$- and $z$-axes (slope $\left|\frac{\Delta z}{\Delta y}\right| = 1$).

3. **Vertical Cross-Section by the Plane $y = 0$ (in the $xz$-plane):**  
   Setting $y = 0$ gives[cite: 1]:

$$
4x^2 = z^2 \implies z = \pm 2x
$$

   This consists of **two steeper intersecting straight lines** ($z = 2x$ and $z = -2x$) crossing at $(0, 0, 0)$ with slope $\left|\frac{\Delta z}{\Delta x}\right| = 2$, reflecting the compressed scale along the $x$-axis compared to the $y$-axis.

#### 2. Identification and Geometric Description of the Sketch
- **Surface Identification:** **Elliptic Double Cone** centered at the origin $(0, 0, 0)$ and symmetric about the $z$-axis[cite: 1].
- **Qualitative Sketch Description:**  
  Two infinite conical nappes meet at their shared apex $(0, 0, 0)$ and flare linearly upward ($z > 0$) and downward ($z < 0$). Unlike a circular cone, its horizontal cross-sections are **ellipses** elongated by a factor of $2$ in the $y$-direction relative to the $x$-direction (at $z = \pm 2$, for example, the ellipse spans $x \in [-1, 1]$ and $y \in [-2, 2]$). Consequently, the cone rises steeply along the $xz$-profile ($z = \pm 2x$) and opens twice as broadly along the $yz$-profile ($z = \pm y$).