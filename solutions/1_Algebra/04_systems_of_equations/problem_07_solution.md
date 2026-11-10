# Exercise 7 – Choosing a Method Deliberately

## Problem Statement

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Solution

### 1. Case 1: System with a Triangular Matrix

#### Method Choice
**Back-substitution**. Since the coefficient matrix is upper triangular, Gaussian elimination is already complete. Performing full elimination or computing a matrix inverse would introduce unnecessary arithmetic steps.

#### Complete Execution

We solve the system directly using back-substitution:

1. **Solve for $y$ from the second equation:**

$$
4y = 8 \implies y = 2
$$

2. **Substitute $y = 2$ into the first equation to solve for $x$:**

$$
2x - y = 3 \implies 2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2}
$$

The unique solution vector is:

$$
x = \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} \frac{5}{2} \\ 2 \end{pmatrix}
$$

---

### 2. Case 2: Three Systems $Ax=b_i$ with Known Invertible Matrix $A$ and Known $A^{-1}$

#### Method Choice
**Direct Matrix-Vector Multiplication ($x_i = A^{-1}b_i$)**.

#### Plan & Reusability Analysis
- **Plan:** Multiply the pre-calculated inverse matrix $A^{-1}$ separately by each right-hand side vector:

$$
x_1 = A^{-1}b_1, \qquad x_2 = A^{-1}b_2, \qquad x_3 = A^{-1}b_3
$$

- **Reusable Part:** The matrix $A^{-1}$ is computed only once (or in this case, already provided) and reused across all three vector multiplications.
- **Unnecessary Computations:** Re-running Gaussian elimination three separate times from scratch would duplicate row operations on $A$. Using $A^{-1}$ reduces the problem to three simple matrix-vector products.

---

### 3. Case 3: One $3\times3$ System with Unknown Inverse Matrix

#### Method Choice
**Gaussian Elimination (LU Decomposition or Augmented Matrix Elimination $[A \mid b]$)**.

#### Plan & Reusability Analysis
- **Plan:** Form the augmented matrix $[A \mid b]$ and apply row operations to reduce it to row echelon form, then solve for the unknowns using back-substitution.
- **Unnecessary Computations:** Computing the inverse matrix $A^{-1}$ explicitly requires solving three separate systems (one for each column of the identity matrix $I_3$), taking roughly three times the computational effort of a single Gaussian elimination. Since we only need to solve for **one** specific right-hand side vector $b$, calculating $A^{-1}$ is inefficient and unnecessary.