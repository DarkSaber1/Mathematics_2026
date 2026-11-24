# Exercise 1 – Recognizing Curves from Canonical Form

## Problem Statement

Recognize the curves

$$
x^2+y^2=9,
$$

$$
\frac{x^2}{16}+\frac{y^2}{9}=1,
$$

$$
y^2=8x,
$$

$$
\frac{x^2}{9}-\frac{y^2}{4}=1.
$$

For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

## Solution

### 1. Curve 1: $x^2 + y^2 = 9$ (Circle)

- **Recognition Mechanism:** Both variables $x$ and $y$ appear squared with equal positive coefficients ($1$ and $1$) on the left-hand side, equal to a positive constant $r^2 = 9$. This matches the canonical circle equation $x^2 + y^2 = r^2$.
- **Key Features:**
  - **Center:** $(0, 0)$
  - **Radius:** $r = \sqrt{9} = 3$
  - **Coordinate Intercepts:** $(-3, 0)$, $(3, 0)$, $(0, -3)$, and $(0, 3)$
  - **Geometric Shape:** A symmetric closed circle of radius $3$ centered at the origin, passing through all four axis intercepts at equal distance $3$ from $(0, 0)$.

---

### 2. Curve 2: $\frac{x^2}{16} + \frac{y^2}{9} = 1$ (Ellipse)

- **Recognition Mechanism:** Both $x^2$ and $y^2$ appear with **positive** signs ($+$), unequal denominators ($16 \neq 9$), and sum to $1$. This matches the canonical ellipse equation $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$.
- **Key Features:**
  - **Center:** $(0, 0)$
  - **Semiaxis Lengths:** $a = \sqrt{16} = 4$ (horizontal major semiaxis) and $b = \sqrt{9} = 3$ (vertical minor semiaxis)
  - **Vertices / Intercepts:** $(-4, 0)$, $(4, 0)$, $(0, -3)$, and $(0, 3)$
  - **Geometric Shape:** A closed oval centered at $(0, 0)$ that is elongated horizontally along the $x$-axis between $x = -4$ and $x = 4$, and bounded vertically between $y = -3$ and $y = 3$.

---

### 3. Curve 3: $y^2 = 8x$ (Parabola)

- **Recognition Mechanism:** Only **one** variable ($y$) is squared while the other variable ($x$) appears linearly to the first power. This matches the canonical parabola equation $y^2 = 2px$ (with $2p = 8 \implies p = 4$).
- **Key Features:**
  - **Vertex:** $(0, 0)$
  - **Axis of Symmetry:** The $x$-axis ($y = 0$), because replacing $y$ with $-y$ leaves the equation unchanged.
  - **Opening Direction:** Opens to the right (along the positive $x$-axis), since $x = \frac{y^2}{8} \ge 0$.
  - **Key Reference Points:** Passes through $(0, 0)$, $(2, 4)$, and $(2, -4)$, widening symmetrically above and below the positive $x$-axis.

---

### 4. Curve 4: $\frac{x^2}{9} - \frac{y^2}{4} = 1$ (Hyperbola)

- **Recognition Mechanism:** Both $x^2$ and $y^2$ are present and equal to $1$, but they have **opposite signs** ($+$ in front of $\frac{x^2}{9}$ and $-$ in front of $\frac{y^2}{4}$). This matches the canonical hyperbola equation $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$.
- **Key Features:**
  - **Center:** $(0, 0)$
  - **Semiaxis Parameters:** $a = \sqrt{9} = 3$ (transverse semiaxis) and $b = \sqrt{4} = 2$ (conjugate semiaxis)
  - **Vertices ($x$-intercepts):** Setting $y = 0$ gives $x^2 = 9 \implies (-3, 0)$ and $(3, 0)$ (no $y$-intercepts, since $x = 0$ yields $-\frac{y^2}{4} = 1$, which has no real solutions).
  - **Asymptotes:** $y = \pm \frac{b}{a}x = \pm \frac{2}{3}x$
  - **Geometric Shape:** Two symmetric open branches facing left (for $x \le -3$) and right (for $x \ge 3$), approaching the two intersecting asymptote lines $y = \frac{2}{3}x$ and $y = -\frac{2}{3}x$ as $|x| \to \infty$.