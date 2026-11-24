# Exercise 6 – Shifted Ellipse

## Problem Statement

Reduce

$$
4x^2+9y^2-16x+18y-11=0
$$

to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

## Solution

### 1. Reducing to Canonical Form by Completing the Square

Start with the given general second-degree equation[cite: 1]:

$$
4x^2 + 9y^2 - 16x + 18y - 11 = 0
$$

Group the $x$-terms and $y$-terms together, move the constant $-11$ to the right-hand side, and factor out the leading coefficients $4$ and $9$:

$$
4(x^2 - 4x) + 9(y^2 + 2y) = 11
$$

Complete the square inside each set of parentheses:
- For $x^2 - 4x$: add $(-2)^2 = 4$ inside the parentheses, which adds $4 \cdot 4 = 16$ to the left-hand side.
- For $y^2 + 2y$: add $(1)^2 = 1$ inside the parentheses, which adds $9 \cdot 1 = 9$ to the left-hand side.

Balance the equation by adding $16 + 9$ to the right-hand side:

$$
4(x^2 - 4x + 4) + 9(y^2 + 2y + 1) = 11 + 16 + 9
$$

Rewrite the squared binomials and simplify the right-hand side:

$$
4(x - 2)^2 + 9(y + 1)^2 = 36
$$

Divide every term by $36$ so that the right-hand side equals $1$:

$$
\frac{4(x - 2)^2}{36} + \frac{9(y + 1)^2}{36} = 1 \implies \frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1
$$

This is the **canonical form** of the shifted ellipse[cite: 1].

---

### 2. Center and Semiaxis Lengths

Comparing $\frac{(x - 2)^2}{3^2} + \frac{(y - (-1))^2}{2^2} = 1$ with the canonical shifted ellipse equation $\frac{(x - x_0)^2}{a^2} + \frac{(y - y_0)^2}{b^2} = 1$:

- **Center:** $(x_0, y_0) = (2, -1)$
- **Horizontal Semiaxis Length:** $a = \sqrt{9} = 3$
- **Vertical Semiaxis Length:** $b = \sqrt{4} = 2$

---

### 3. Consistency Check at the Center $(2, -1)$

In the completed-square form $4(x - 2)^2 + 9(y + 1)^2 - 36 = 0$, evaluating the expression at the center $(x, y) = (2, -1)$ gives:

$$
4(2 - 2)^2 + 9(-1 + 1)^2 - 36 = 0 + 0 - 36 = -36
$$

Now substitute $(x, y) = (2, -1)$ directly into the original left-hand side $4x^2 + 9y^2 - 16x + 18y - 11$[cite: 1]:

$$
4(2)^2 + 9(-1)^2 - 16(2) + 18(-1) - 11 = 16 + 9 - 32 - 18 - 11 = 25 - 61 = -36
$$

Both forms evaluate to $-36$ at the center $(2, -1)$, confirming that the algebraic reduction is completely consistent.