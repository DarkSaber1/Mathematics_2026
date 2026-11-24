# Exercise 11 – Decomposition into Parallel and Perpendicular Components

## Problem Statement

Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check

$$
u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.
$$

Explain why these are two independent checks of correctness.

## Solution

### 1. Computing the Parallel Component ($u_{\parallel}$)

The component of $u = (3, 4)$ parallel to $v = (1, 2)$ is given by the orthogonal projection of $u$ onto $v$:

$$
u_{\parallel} = \mathrm{proj}_v\,u = \frac{u \cdot v}{v \cdot v} v
$$

First, compute the required dot products:

$$
u \cdot v = (3)(1) + (4)(2) = 3 + 8 = 11
$$

$$
v \cdot v = (1)(1) + (2)(2) = 1 + 4 = 5
$$

Substituting these values into the projection formula:

$$
u_{\parallel} = \frac{11}{5} (1, 2) = \left( \frac{11}{5},\, \frac{22}{5} \right)
$$

---

### 2. Computing the Perpendicular Component ($u_{\perp}$)

Once $u_{\parallel}$ is known, the perpendicular (orthogonal) component $u_{\perp}$ is obtained by subtracting $u_{\parallel}$ from $u$:

$$
u_{\perp} = u - u_{\parallel} = (3, 4) - \left( \frac{11}{5},\, \frac{22}{5} \right)
$$

Writing $(3, 4)$ with denominator $5$ as $\left( \frac{15}{5}, \frac{20}{5} \right)$:

$$
u_{\perp} = \left( \frac{15}{5} - \frac{11}{5},\, \frac{20}{5} - \frac{22}{5} \right) = \left( \frac{4}{5},\, -\frac{2}{5} \right)
$$

Thus, the orthogonal decomposition of $u$ with respect to $v$ is:

$$
u_{\parallel} = \left( \frac{11}{5},\, \frac{22}{5} \right), \qquad u_{\perp} = \left( \frac{4}{5},\, -\frac{2}{5} \right)
$$

---

### 3. Verifying Both Conditions

- **Check 1: Reconstruction ($u = u_{\parallel} + u_{\perp}$):**

$$
u_{\parallel} + u_{\perp} = \left( \frac{11}{5},\, \frac{22}{5} \right) + \left( \frac{4}{5},\, -\frac{2}{5} \right) = \left( \frac{15}{5},\, \frac{20}{5} \right) = (3, 4) = u
$$

- **Check 2: Orthogonality ($u_{\perp} \cdot v = 0$):**

$$
u_{\perp} \cdot v = \left(\frac{4}{5}\right)(1) + \left(-\frac{2}{5}\right)(2) = \frac{4}{5} - \frac{4}{5} = 0
$$

Both conditions are satisfied.

---

### 4. Why These Are Two Independent Checks of Correctness

An orthogonal decomposition requires two distinct properties to hold simultaneously, and neither condition guarantees the other on its own:

- **What $u = u_{\parallel} + u_{\perp}$ Tests (Completeness / No Lost Part):**  
  This verifies that the two pieces sum back to the exact original vector $u$ without any arithmetic sign or addition errors. However, infinitely many pairs of vectors sum to $u$ (for example, $(1, 1) + (2, 3) = (3, 4)$) without being aligned with or perpendicular to $v$.

- **What $u_{\perp} \cdot v = 0$ Tests (True Orthogonality / Correct Projection Scale):**  
  This verifies that the scalar factor $\frac{u \cdot v}{v \cdot v} = \frac{11}{5}$ used in $u_{\parallel}$ was calculated accurately—if the scalar multiple of $v$ were slightly off, $u - u_{\parallel}$ would still contain a component along $v$ and its dot product with $v$ would be non-zero. Conversely, a vector satisfying $u_{\perp} \cdot v = 0$ could be scaled improperly (e.g., $(8, -4)$) and fail to sum back to $u$.

Together, the two checks confirm both **geometric alignment** and **exact vector reconstruction**.