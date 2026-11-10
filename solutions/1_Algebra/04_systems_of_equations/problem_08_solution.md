# Exercise 8 – Two Systems with the Same Coefficient Matrix

## Problem Statement

Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Solution

### 1. Simultaneous Gaussian Elimination

Since both systems share the exact same coefficient matrix $A$, we can form a combined augmented matrix $[A \mid b_1 \mid b_2]$ to execute the elimination steps for both right-hand side vectors simultaneously:

$$
[A \mid b_1 \mid b_2] = \left(\begin{array}{cc|c|c} 2 & 1 & 5 & 1 \\ 1 & -1 & 1 & 4 \end{array}\right)
$$

- **Step 1:** Swap row 1 and row 2 ($R_1 \leftrightarrow R_2$) to establish a pivot of $1$:

$$
\left(\begin{array}{cc|c|c} 1 & -1 & 1 & 4 \\ 2 & 1 & 5 & 1 \end{array}\right)
$$

- **Step 2:** Eliminate $x$ from row 2 by performing $R_2 \leftarrow R_2 - 2 R_1$:

$$
R_2 \text{ row operations on } A: (2, 1) - 2(1, -1) = (0, 3)
$$

$$
R_2 \text{ row operations on } b_1: 5 - 2(1) = 3
$$

$$
R_2 \text{ row operations on } b_2: 1 - 2(4) = -7
$$

The resulting row echelon form matrix is:

$$
\left(\begin{array}{cc|c|c} 1 & -1 & 1 & 4 \\ 0 & 3 & 3 & -7 \end{array}\right)
$$

---

### 2. Solving System 1 ($Ax = b_1$)

Using the third column ($b_1$):

1. **Second equation:**

$$
3y = 3 \implies y = 1
$$

2. **First equation:**

$$
x - y = 1 \implies x - 1 = 1 \implies x = 2
$$

The solution vector for System 1 is:

$$
x_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}
$$

---

### 3. Solving System 2 ($Ax = b_2$)

Using the fourth column ($b_2$):

1. **Second equation:**

$$
3y = -7 \implies y = -\frac{7}{3}
$$

2. **First equation:**

$$
x - y = 4 \implies x - \left(-\frac{7}{3}\right) = 4 \implies x + \frac{7}{3} = 4 \implies x = \frac{5}{3}
$$

The solution vector for System 2 is:

$$
x_2 = \begin{pmatrix} \frac{5}{3} \\ -\frac{7}{3} \end{pmatrix}
$$

---

### 4. Comparison and Explanation

- **Identical Computation Part:**  
  All elementary row operations performed on the coefficient matrix $A$ (left side of the vertical line) are identical in both cases. Specifically, swapping rows and subtracting $2 \times R_1$ from $R_2$ depends solely on the entries of $A$.

- **Why this occurs:**  
  Row operations are linear transformations applied to equations to eliminate unknowns. The sequence of operations needed to achieve row echelon form is dictated entirely by the structure of $A$, independently of the constants in the right-hand side vectors $b_1$ and $b_2$.