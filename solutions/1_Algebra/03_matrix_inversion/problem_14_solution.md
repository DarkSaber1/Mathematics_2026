# Exercise 14 – A Matrix That Is Its Own Inverse

## Problem Statement

Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## Solution

### 1. Proof That $A^{-1} = A$

By definition, a square matrix $B$ is the inverse of a square matrix $A$ (denoted $B = A^{-1}$) if and only if multiplying them in both orders yields the identity matrix $I$:

$$
AB = I \qquad \text{and} \qquad BA = I
$$

We are given the condition that $A^2 = I$. Expanding $A^2$ as the product of $A$ with itself gives:

$$
A \cdot A = I
$$

Comparing this equation directly with the definition of the inverse shows that $A$ itself satisfies the role of $B$ on both the left and the right. Therefore, $A$ is invertible and its inverse is equal to $A$:

$$
A^{-1} = A
$$

---

### 2. Example of a $2 \times 2$ Matrix ($A \neq \pm I$)

Consider the $2 \times 2$ reflection matrix across the line $y = x$:

$$
A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}
$$

This matrix is clearly distinct from both the identity matrix $I_2$ and its negative $-I_2$:

$$
I_2 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \qquad -I_2 = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}
$$

---

### 3. Verification by Matrix Multiplication

We verify that $A$ satisfies $A^2 = I_2$ by computing the product $A \cdot A$:

$$
A^2 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}
$$

$$
A^2 = \begin{pmatrix} 0(0) + 1(1) & 0(1) + 1(0) \\ 1(0) + 0(1) & 1(1) + 0(0) \end{pmatrix}
$$

$$
A^2 = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2
$$

Since $A^2 = I_2$, the condition holds, confirming that $A^{-1} = A$.