## Exercise 8. Determinant of a Product

### Problem Definition
Let $A$ and $B$ be $n \times n$ square matrices such that:[cite: 1]

$$ \det A = 3, \qquad \det B = -5 $$

1. Compute $\det(AB)$.[cite: 1]
2. Compute $\det(BA)$.[cite: 1]
3. Determine whether $\det(A^{-1}B)$ exists, and if so, compute its value.[cite: 1]
4. Explain why $\det(AB) = \det(BA)$ even though matrix multiplication is generally non-commutative ($AB \neq BA$).[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Computation of $\det(AB)$

##### Multiplicative Property of Determinants
> For any two $n \times n$ square matrices $M$ and $N$, the determinant of their product is the product of their individual determinants:
>
> $$ \det(M N) = \det M \cdot \det N $$

##### Calculation
Substituting the given values $\det A = 3$ and $\det B = -5$:[cite: 1]

$$ \det(AB) = \det A \cdot \det B = (3) \cdot (-5) = -15 $$

---

#### Step 2: Computation of $\det(BA)$

##### Calculation
Applying the multiplicative property to $BA$:

$$ \det(BA) = \det B \cdot \det A = (-5) \cdot (3) = -15 $$

---

#### Step 3: Computation of $\det(A^{-1}B)$

##### 1. Existence Check for $A^{-1}$
A square matrix $A$ is invertible if and only if $\det A \neq 0$.[cite: 1]
Since $\det A = 3 \neq 0$, matrix $A$ is non-singular and its inverse $A^{-1}$ **is guaranteed to exist**.[cite: 1]

##### 2. Inverse Determinant Property
> For an invertible matrix $M$, the determinant of its inverse is the reciprocal of its determinant:
>
> $$ \det(M^{-1}) = \frac{1}{\det M} $$

##### 3. Calculation
Using the product property and inverse property combined:

$$ \det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \left( \frac{1}{\det A} \right) \cdot \det B $$

Substituting $\det A = 3$ and $\det B = -5$:

$$ \det(A^{-1}B) = \left( \frac{1}{3} \right) \cdot (-5) = -\frac{5}{3} $$

---

#### Step 4: Explanation of Why $\det(AB) = \det(BA)$

##### Matrix Non-Commutativity vs. Real Number Commutativity

1. **Matrix Level (Non-Commutative):**
   In matrix algebra, matrix multiplication is generally non-commutative ($AB \neq BA$). The resulting product matrices $AB$ and $BA$ are distinct matrices with different individual entries.

2. **Scalar Level (Commutative):**
   The determinant function $\det: \mathbb{R}^{n \times n} \to \mathbb{R}$ maps a matrix to a single real number (scalar).

3. **Algebraic Proof:**
   * $\det(AB) = \det A \cdot \det B$
   * $\det(BA) = \det B \cdot \det A$

   Since $\det A$ and $\det B$ are real numbers in $\mathbb{R}$, and multiplication of real numbers is commutative ($x \cdot y = y \cdot x$ for all $x, y \in \mathbb{R}$):

   $$ \det A \cdot \det B = \det B \cdot \det A \implies \det(AB) = \det(BA) $$

Thus, even though $AB$ and $BA$ are completely different matrices, their determinants are identical because scalar multiplication in $\mathbb{R}$ is commutative.

---

### Summary of Results for Exercise 8

* **$\det(AB) = -15$**
* **$\det(BA) = -15$**
* **$\det(A^{-1}B) = -\frac{5}{3}$** (Exists because $\det A = 3 \neq 0$)
* **Commutativity Explanation:** Matrix multiplication $AB \neq BA$ is non-commutative, but scalar product $\det A \cdot \det B = \det B \cdot \det A$ is commutative.