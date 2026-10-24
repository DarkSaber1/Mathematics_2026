## Exercise 7. Using Properties Instead of Recomputing

### Problem Definition
Suppose that $A$ is a $3 \times 3$ matrix with determinant $\det A = -4$.[cite: 1] 

Without knowing the individual entries of matrix $A$, compute the following determinants:[cite: 1]
1. $\det(2A)$[cite: 1]
2. $\det(A^T)$[cite: 1]
3. $\det(A^2)$[cite: 1]
4. $\det(-A)$[cite: 1]

For each calculation, state and justify the determinant property used.[cite: 1]

---

### Detailed Mathematical Solution

#### 1. Computation of $\det(2A)$

##### Relevant Property: Scalar Multiplication Rule
> For any $n \times n$ square matrix $M$ and scalar $c \in \mathbb{R}$, multiplying the entire matrix by $c$ scales every row by $c$. Since factoring a scalar out of each of the $n$ rows pulls out a factor of $c$, the determinant relationship is:
>
> $$ \det(c M) = c^n \cdot \det M $$

##### Step-by-Step Calculation
* Matrix $A$ is a $3 \times 3$ matrix, so $n = 3$.
* The scalar multiplier is $c = 2$.
* Applying the formula:

$$ \det(2A) = 2^3 \cdot \det A $$

* Compute $2^3 = 8$.
* Substitute $\det A = -4$:

$$ \det(2A) = 8 \cdot (-4) = -32 $$

---

#### 2. Computation of $\det(A^T)$

##### Relevant Property: Transpose Property
> The determinant of a matrix is equal to the determinant of its transpose:
>
> $$ \det(M^T) = \det M $$
>
> This holds because row operations on $M^T$ correspond directly to column operations on $M$, and transpose operations preserve the algebraic expansion of the determinant.

##### Step-by-Step Calculation
* Apply the property directly to matrix $A$:

$$ \det(A^T) = \det A $$

* Substitute $\det A = -4$:

$$ \det(A^T) = -4 $$

---

#### 3. Computation of $\det(A^2)$

##### Relevant Property: Power / Product Property
> For any $n \times n$ matrix $M$ and integer $k \ge 1$, the determinant of a matrix power equals the power of the determinant:
>
> $$ \det(M^k) = (\det M)^k $$
>
> This follows directly from the multiplicative property of determinants: $\det(M \cdot M) = \det M \cdot \det M = (\det M)^2$.

##### Step-by-Step Calculation
* Apply the power rule for $k = 2$:

$$ \det(A^2) = (\det A)^2 $$

* Substitute $\det A = -4$:

$$ \det(A^2) = (-4)^2 = 16 $$

---

#### 4. Computation of $\det(-A)$

##### Relevant Property: Negation / Scalar Rule for $-1$
> Negating a matrix is equivalent to scalar multiplication by $c = -1$, i.e., $-A = (-1)A$. For an $n \times n$ matrix:
>
> $$ \det(-M) = \det((-1)M) = (-1)^n \cdot \det M $$
>
> * If dimension $n$ is **even**, $(-1)^n = +1 \implies \det(-M) = \det M$.
> * If dimension $n$ is **odd**, $(-1)^n = -1 \implies \det(-M) = -\det M$.

##### Step-by-Step Calculation
* Since $A$ is a $3 \times 3$ matrix, dimension $n = 3$ (odd).
* Apply the scalar formula with $c = -1$ and $n = 3$:

$$ \det(-A) = (-1)^3 \cdot \det A = -1 \cdot \det A $$

* Substitute $\det A = -4$:

$$ \det(-A) = -1 \cdot (-4) = 4 $$

---

### Summary of Results for Exercise 7

| Target Expression | Applied Property / Formula | Intermediate Substitution | Final Value |
| :--- | :--- | :--- | :--- |
| $\det(2A)$ | $c^n \cdot \det A \quad (n=3, c=2)$ | $2^3 \cdot (-4) = 8 \cdot (-4)$ | **$-32$** |
| $\det(A^T)$ | $\det(A^T) = \det A$ | $-4$ | **$-4$** |
| $\det(A^2)$ | $(\det A)^2$ | $(-4)^2$ | **$16$** |
| $\det(-A)$ | $(-1)^n \cdot \det A \quad (n=3)$ | $(-1)^3 \cdot (-4) = -1 \cdot (-4)$ | **$4$** |