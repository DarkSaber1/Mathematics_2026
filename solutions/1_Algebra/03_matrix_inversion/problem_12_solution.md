# Exercise 12 – Finding Inverses Without Starting from Scratch

## Problem Statement

It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## Solution

### 1. Computing $(3A)^{-1}$

- **Property Used:**  
  For any invertible matrix $A$ and non-zero scalar $c \neq 0$, the inverse of a scalar multiple is given by:

$$
(cA)^{-1} = \frac{1}{c} A^{-1}
$$

  **Justification:** Multiplying $(cA)$ by $\left(\frac{1}{c} A^{-1}\right)$ yields:

$$
(cA)\left(\frac{1}{c}A^{-1}\right) = \left(c \cdot \frac{1}{c}\right)(AA^{-1}) = 1 \cdot I = I
$$

- **Calculation:**  
  Substituting $c = 3$ and the given $A^{-1}$:

$$
(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3} \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{3} \\ -1 & \frac{2}{3} \end{pmatrix}
$$

---

### 2. Computing $(A^T)^{-1}$

- **Property Used:**  
  For any invertible matrix $A$, the inverse of its transpose is equal to the transpose of its inverse:

$$
(A^T)^{-1} = (A^{-1})^T
$$

  **Justification:** Taking the transpose of both sides of $A A^{-1} = I$ gives:

$$
(A A^{-1})^T = I^T \implies (A^{-1})^T A^T = I
$$

- **Calculation:**  
  Transposing $A^{-1}$ (swapping its rows and columns):

$$
(A^T)^{-1} = (A^{-1})^T = \begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix}
$$

---

### 3. Computing $(A^2)^{-1}$

- **Property Used:**  
  For any invertible matrix $A$ and positive integer $k$, the inverse of a matrix power equals the power of its inverse:

$$
(A^k)^{-1} = (A^{-1})^k
$$

  **Justification:** For $k = 2$, $A^2 = A \cdot A$. Using the inverse-of-a-product rule $(AB)^{-1} = B^{-1}A^{-1}$ with $B = A$:

$$
(A^2)^{-1} = (A \cdot A)^{-1} = A^{-1} A^{-1} = (A^{-1})^2
$$

- **Calculation:**  
  Multiplying $A^{-1}$ by itself:

$$
(A^2)^{-1} = (A^{-1})^2 = \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}
$$

$$
(A^2)^{-1} = \begin{pmatrix} 2(2) + (-1)(-3) & 2(-1) + (-1)(2) \\ (-3)(2) + 2(-3) & (-3)(-1) + 2(2) \end{pmatrix}
$$

$$
(A^2)^{-1} = \begin{pmatrix} 4 + 3 & -2 - 2 \\ -6 - 6 & 3 + 4 \end{pmatrix} = \begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}
$$