# Exercise 10 – Paraboloids

## Problem Statement

Compare

$$
z=x^2+y^2
$$

and

$$
z=x^2-y^2.
$$

For each surface, describe the cross-sections $x=0$, $y=0$, and $z=c$, then make a qualitative sketch.

## Solution

### 1. First Surface: $z = x^2 + y^2$ (Elliptic / Circular Paraboloid)

#### Cross-Sections
- **Cross-section $x = 0$ (in the $yz$-plane):**
  Substituting $x = 0$ gives:

$$
z = y^2
$$

  This is an **upward-opening parabola** with vertex at $(0, 0, 0)$ lying in the $yz$-plane.
- **Cross-section $y = 0$ (in the $xz$-plane):**
  Substituting $y = 0$ gives:

$$
z = x^2
$$

  This is an identical **upward-opening parabola** with vertex at $(0, 0, 0)$ lying in the $xz$-plane.
- **Horizontal Cross-sections $z = c$ (planes parallel to the $xy$-plane):**
  Setting $z = c$ gives:

$$
x^2 + y^2 = c
$$

  - For $c > 0$: a **circle** centered on the $z$-axis at $(0, 0, c)$ with radius $r = \sqrt{c}$, widening smoothly as $c$ increases.
  - For $c = 0$: a **single point** at the origin $(0, 0, 0)$ (the minimum point / vertex of the surface).
  - For $c < 0$: **empty set ($\emptyset$)** — no real points exist below the $xy$-plane because $x^2 + y^2 \ge 0$.

#### Qualitative Sketch Description
The surface is a symmetric, smooth **bowl (cup) opening upward** along the positive $z$-axis with its lowest point at $(0, 0, 0)$. Every vertical slice through the $z$-axis is an upward parabola, while every horizontal slice above $z = 0$ is a concentric circle whose radius grows like $\sqrt{z}$.

---

### 2. Second Surface: $z = x^2 - y^2$ (Hyperbolic Paraboloid)

#### Cross-Sections
- **Cross-section $x = 0$ (in the $yz$-plane):**
  Substituting $x = 0$ gives:

$$
z = -y^2
$$

  This is a **downward-opening parabola** with vertex at $(0, 0, 0)$ lying in the $yz$-plane.
- **Cross-section $y = 0$ (in the $xz$-plane):**
  Substituting $y = 0$ gives:

$$
z = x^2
$$

  This is an **upward-opening parabola** with vertex at $(0, 0, 0)$ lying in the $xz$-plane.
- **Horizontal Cross-sections $z = c$ (planes parallel to the $xy$-plane):**
  Setting $z = c$ gives:

$$
x^2 - y^2 = c
$$

  - For $c > 0$: a **hyperbola** opening along the $x$-direction (vertices at $(\pm\sqrt{c}, 0, c)$).
  - For $c = 0$: $x^2 - y^2 = 0 \implies y = \pm x$, which is a pair of **two intersecting straight lines** crossing at the origin $(0, 0, 0)$.
  - For $c < 0$: rewriting as $y^2 - x^2 = -c$ (with $-c > 0$) gives a **hyperbola** opening along the $y$-direction (vertices at $(0, \pm\sqrt{-c}, c)$).

#### Qualitative Sketch Description
The surface has a characteristic **saddle shape** centered at the saddle point $(0, 0, 0)$:
- Moving along the $x$-axis curves **upward** like a valley ($z = x^2$), whereas moving along the $y$-axis curves **downward** like a mountain ridge ($z = -y^2$).
- Horizontal contour lines switch orientation across $z = 0$: hyperbolas opening left/right above the origin ($z > 0$), two crossing straight lines $y = \pm x$ directly at $z = 0$, and hyperbolas opening front/back below the origin ($z < 0$).

---

### 3. Summary Comparison

| Feature | $z = x^2 + y^2$ (Circular Paraboloid) | $z = x^2 - y^2$ (Hyperbolic Paraboloid) |
| :--- | :--- | :--- |
| **$x = 0$ slice** | Upward parabola ($z = y^2$) | Downward parabola ($z = -y^2$) |
| **$y = 0$ slice** | Upward parabola ($z = x^2$) | Upward parabola ($z = x^2$) |
| **$z = c$ ($c > 0$)** | Circles of radius $\sqrt{c}$ | Hyperbolas opening along $x$ |
| **$z = 0$ slice** | Single point $(0, 0, 0)$ | Two intersecting lines $y = \pm x$ |
| **$z = c$ ($c < 0$)** | Empty (no points) | Hyperbolas opening along $y$ |
| **Overall geometry** | Upward bowl with global minimum at $(0,0,0)$ | Saddle surface with saddle point at $(0,0,0)$ |