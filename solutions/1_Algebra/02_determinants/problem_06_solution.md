## Exercise 6. Parameter and Invertibility

### Problem Definition
Given the $2 \times 2$ parameterized matrix:[cite: 1]

$$
A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}
$$

1. Compute the determinant of $A(t)$ as a function of the parameter $t$.[cite: 1]
2. Find all real values of $t$ for which matrix $A(t)$ is **not invertible** (singular).[cite: 1]
3. Explain in detail how your answer relates to the determinant being zero and the geometric/algebraic meaning of matrix invertibility.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Computing $\det A(t)$

Using the standard formula for the determinant of a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$:

$$
\det \begin{pmatrix} a & b \\ c & d \end{pmatrix} = (a \cdot d) - (b \cdot c)
$$

For $A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}$:[cite: 1]

* Main diagonal product: $t \cdot t = t^2$
* Anti-diagonal product: $1 \cdot 2 = 2$

Subtracting the anti-diagonal product from the main diagonal product yields the polynomial expression:[cite: 1]

$$
\det A(t) = t^2 - 2
$$

---

#### Step 2: Finding Values of $t$ for Non-Invertibility

##### The Invertibility Criterion
By the **Invertible Matrix Theorem**, a square matrix $M$ is **not invertible** (also called **singular**) if and only if its determinant equals zero:[cite: 1]

$$
A(t) \text{ is not invertible} \iff \det A(t) = 0
$$

##### Solving the Equation
Set the determinant polynomial equal to zero:

$$
t^2 - 2 = 0
$$

Isolate $t^2$:

$$
t^2 = 2
$$

Taking the square root on both sides gives two real solutions:

$$
t = \sqrt{2} \quad \text{or} \quad t = -\sqrt{2}
$$

Thus, the matrix $A(t)$ is **not invertible** if and only if $t = \sqrt{2}$ or $t = -\sqrt{2}$.

---

#### Step 3: Explanation of the Connection Between $\det A(t) = 0$ and Invertibility

##### 1. Algebraic Explanation (Linear Dependence)
The determinant measures whether the rows (or columns) of a matrix are linearly independent.

* **Case 1: $t = \sqrt{2}$**
  The matrix becomes:
  $$
  A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \end{pmatrix}
  $$
  Notice that Row 2 is a exact scalar multiple of Row 1:
  $$
  R_2 = \sqrt{2} \cdot R_1 \implies (2, \sqrt{2}) = \sqrt{2} \cdot (\sqrt{2}, 1)
  $$
  Because the rows are linearly dependent, the matrix loses full rank ($\text{rank} = 1 < 2$), which means it cannot be inverted.

* **Case 2: $t = -\sqrt{2}$**
  The matrix becomes:
  $$
  A(-\sqrt{2}) = \begin{pmatrix} -\sqrt{2} & 1 \\ 2 & -\sqrt{2} \end{pmatrix}
  $$
  Similarly, Row 2 is a scalar multiple of Row 1:
  $$
  R_2 = -\sqrt{2} \cdot R_1 \implies (2, -\sqrt{2}) = -\sqrt{2} \cdot (-\sqrt{2}, 1)
  $$
  Again, linear dependence forces the determinant to zero, rendering the matrix non-invertible.

##### 2. Explicit Inverse Formula Perspective
The inverse of a general $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ is given by:

$$
M^{-1} = \frac{1}{\det M} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}
$$

For matrix $A(t)$:

$$
A(t)^{-1} = \frac{1}{t^2 - 2} \begin{pmatrix} t & -1 \\ -2 & t \end{pmatrix}
$$

If $t = \pm\sqrt{2}$, the denominator $t^2 - 2$ becomes $0$, leading to division by zero ($\frac{1}{0}$), which is mathematically undefined. Therefore, no inverse matrix exists for these parameter values.

##### 3. Geometric Transformation Perspective
Geometrically, a $2 \times 2$ matrix maps the $2\text{D}$ plane onto another space, and $|\det A(t)|$ represents the **area scaling factor** of this transformation.

* When $t \neq \pm\sqrt{2}$, the matrix maps a unit square into a parallelogram of area $|t^2 - 2| > 0$, making the mapping reversible (invertible).
* When $t = \pm\sqrt{2}$, $\det A(t) = 0$, meaning the 2D plane is squashed/compressed down onto a 1D line (area = 0). Since information is collapsed into a lower dimension, the transformation cannot be undone, making $A(t)$ non-invertible.

---

### Conclusion and Key Takeaways

1. **Determinant Expression:**
   $$\det A(t) = t^2 - 2$$

2. **Parameter Values for Non-Invertibility:**
   $$t = \sqrt{2} \quad \text{and} \quad t = -\sqrt{2}$$

3. **Core Rule:**
   A matrix is singular (non-invertible) if and only if its determinant is zero, which corresponds precisely to linear dependence among its rows/columns.