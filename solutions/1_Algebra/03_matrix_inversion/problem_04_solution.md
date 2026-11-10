# Exercise 4 – Gauss–Jordan

## Problem Statement

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5
\end{pmatrix}
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## Solution

### 1. Step-by-Step Gauss–Jordan Elimination

We set up the augmented matrix $[A \mid I]$:

$$
[A \mid I] = \left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 3 & 5 & 0 & 1 \end{array}\right)
$$

- **Step 1:** Eliminate the entry below the pivot in row 1 by performing $R_2 \leftarrow R_2 - 3R_1$:

$$
R_2 \text{ calculation: } (3, 5, 0, 1) - 3(1, 2, 1, 0) = (0, -1, -3, 1)
$$

$$
\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & -1 & -3 & 1 \end{array}\right)
$$

- **Step 2:** Scale row 2 by $-1$ ($R_2 \leftarrow -1 \cdot R_2$) to make the second pivot $+1$:

$$
\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & 1 & 3 & -1 \end{array}\right)
$$

- **Step 3:** Eliminate the entry above the pivot in row 2 by performing $R_1 \leftarrow R_1 - 2R_2$:

$$
R_1 \text{ calculation: } (1, 2, 1, 0) - 2(0, 1, 3, -1) = (1, 0, -5, 2)
$$

$$
\left(\begin{array}{cc|cc} 1 & 0 & -5 & 2 \\ 0 & 1 & 3 & -1 \end{array}\right)
$$

Since the left side has been transformed into the identity matrix $I$, the right side is the inverse matrix $A^{-1}$:

$$
A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}
$$

### 2. Explanation of the Gauss–Jordan Principle

Performing elementary row operations on $[A \mid I]$ corresponds to multiplying both sides from the left by a sequence of elementary matrices $E_1, E_2, \ldots, E_k$. 

When the sequence of operations reduces $A$ to the identity matrix $I$:

$$
(E_k \cdots E_2 E_1) A = I \implies E_k \cdots E_2 E_1 = A^{-1}
$$

Applying the exact same operations simultaneously to $I$ yields:

$$
(E_k \cdots E_2 E_1) I = A^{-1} I = A^{-1}
$$

Thus, obtaining $I$ on the left guarantees that the right side becomes $A^{-1}$.

### Verification

We verify the result by computing the product $A A^{-1}$:

$$
A A^{-1} = \begin{pmatrix} 1 & 2 \\ 3 & 5 \end{pmatrix} \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}
$$

- Top-left entry: $1(-5) + 2(3) = -5 + 6 = 1$
- Top-right entry: $1(2) + 2(-1) = 2 - 2 = 0$
- Bottom-left entry: $3(-5) + 5(3) = -15 + 15 = 0$
- Bottom-right entry: $3(2) + 5(-1) = 6 - 5 = 1$

$$
A A^{-1} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I
$$

The product equals $I$, confirming that $A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}$ is correct.