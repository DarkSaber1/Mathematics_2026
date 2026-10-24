## Exercise 15. Combining Determinant Properties

### Problem Definition
Let $A$ and $B$ be invertible $2 \times 2$ matrices with given determinants:[cite: 1]

$$
\det A = -2, \qquad \det B = 3
$$

1. Without knowing or finding the individual entries of the matrices, compute the determinant of the composite matrix $\det(B^{-1}A^TB)$.[cite: 1]
2. State the specific determinant properties used, in the order they are applied.[cite: 1]
3. Explain mathematically why the factors involving matrix $B$ eventually cancel out.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Applying the Multiplicative Property
The determinant of a product of matrices is equal to the product of their individual determinants. For any matrices $X, Y,$ and $Z$:[cite: 1]

> **Property 1 (Product Rule):** $\det(XYZ) = \det X \cdot \det Y \cdot \det Z$

Applying this to our expression:

$$
\det(B^{-1}A^TB) = \det(B^{-1}) \cdot \det(A^T) \cdot \det(B)
$$

---

#### Step 2: Applying the Inverse Property
The determinant of an inverse matrix is the reciprocal of the determinant of the original matrix.[cite: 1]

> **Property 2 (Inverse Rule):** $\det(M^{-1}) = \frac{1}{\det M}$

Applying this to $\det(B^{-1})$:

$$
\det(B^{-1}) = \frac{1}{\det B}
$$

Substitute this back into our main equation:

$$
\det(B^{-1}A^TB) = \left( \frac{1}{\det B} \right) \cdot \det(A^T) \cdot \det(B)
$$

---

#### Step 3: Applying the Transpose Property
The determinant of a transposed matrix is equal to the determinant of the original matrix.[cite: 1]

> **Property 3 (Transpose Rule):** $\det(M^T) = \det M$

Applying this to $\det(A^T)$:

$$
\det(A^T) = \det A
$$

Substitute this into our ongoing equation:

$$
\det(B^{-1}A^TB) = \left( \frac{1}{\det B} \right) \cdot \det A \cdot \det B
$$

---

#### Step 4: Simplifying and Explaining the Cancellation
Now, look at the scalar expression we have derived:

$$
\left( \frac{1}{\det B} \right) \cdot \det A \cdot \det B
$$

Notice that $\det A$ and $\det B$ are just real numbers (scalars). While matrix multiplication is generally not commutative ($B^{-1} A^T B \neq A^T B^{-1} B$), **multiplication of real numbers is perfectly commutative** ($x \cdot y \cdot z = y \cdot x \cdot z$).[cite: 1]

Because scalar multiplication commutes, we can rearrange the terms:

$$
\det(B^{-1}A^TB) = \det A \cdot \left( \frac{1}{\det B} \cdot \det B \right)
$$

Since $\frac{1}{\det B} \cdot \det B = 1$, the terms involving $B$ cancel each other out entirely:[cite: 1]

$$
\det(B^{-1}A^TB) = \det A \cdot (1) = \det A
$$

---

#### Step 5: Final Calculation
Since we proved that $\det(B^{-1}A^TB) = \det A$, we simply substitute the known value $\det A = -2$:[cite: 1]

$$
\det(B^{-1}A^TB) = -2
$$

---

### Conclusion and Key Takeaways

1. **Calculated Value:**
   $$ \det(B^{-1}A^TB) = -2 $$

2. **Properties Used in Order:**
   * **Product Rule:** Split the product into scalar determinants.[cite: 1]
   * **Inverse Rule:** Converted $\det(B^{-1})$ to $1/\det B$.[cite: 1]
   * **Transpose Rule:** Converted $\det(A^T)$ to $\det A$.[cite: 1]

3. **Why $B$ factors cancel:**
   Matrix multiplication order matters, but once converted into determinants, they become real numbers. Real numbers commute, allowing $(1/\det B)$ and $\det B$ to multiply together to yield $1$, completely eliminating the influence of matrix $B$.[cite: 1]