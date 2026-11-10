# Exercise 7 – Inverse of a Product

## Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## Solution

### 1. Calculation of $(AB)^{-1}$

First, we compute the product matrix $AB$:

$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} 1(2)+1(0) & 1(0)+1(3) \\ 0(2)+1(0) & 0(0)+1(3) \end{pmatrix} = \begin{pmatrix} 2 & 3 \\ 0 & 3 \end{pmatrix}
$$

Next, we find the inverse of $AB$. The determinant of $AB$ is:

$$
\det(AB) = (2)(3) - (3)(0) = 6
$$

Using the $2 \times 2$ inverse formula:

$$
(AB)^{-1} = \frac{1}{6} \begin{pmatrix} 3 & -3 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}
$$

### 2. Calculation of $B^{-1}A^{-1}$

First, we find the individual inverses $A^{-1}$ and $B^{-1}$:

- For $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$, $\det(A) = 1$:

$$
A^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}
$$

- For $B = \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix}$, $\det(B) = 6$:

$$
B^{-1} = \frac{1}{6} \begin{pmatrix} 3 & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{3} \end{pmatrix}
$$

Now, we multiply $B^{-1}$ by $A^{-1}$:

$$
B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{3} \end{pmatrix} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(1)+0(0) & \frac{1}{2}(-1)+0(1) \\ 0(1)+\frac{1}{3}(0) & 0(-1)+\frac{1}{3}(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}
$$

### 3. Comparison and Explanation of Reversed Order

Comparing both results:

$$
(AB)^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix} = B^{-1}A^{-1}
$$

- **Meaning of the reversed order:**  
  When transformations are applied sequentially as $AB$, matrix $B$ acts first, followed by matrix $A$. To undo this combined transformation, we must reverse the steps: first undo the last transformation $A$ (by applying $A^{-1}$), and then undo the first transformation $B$ (by applying $B^{-1}$). Algebraically:

$$
(AB)(B^{-1}A^{-1}) = A(B B^{-1})A^{-1} = A I A^{-1} = A A^{-1} = I
$$

### Verification

We verify that multiplying $(AB)$ by $(B^{-1}A^{-1})$ yields the identity matrix $I$:

$$
(AB) (B^{-1}A^{-1}) = \begin{pmatrix} 2 & 3 \\ 0 & 3 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}
$$

- Top-left entry: $2\left(\frac{1}{2}\right) + 3(0) = 1 + 0 = 1$
- Top-right entry: $2\left(-\frac{1}{2}\right) + 3\left(\frac{1}{3}\right) = -1 + 1 = 0$
- Bottom-left entry: $0\left(\frac{1}{2}\right) + 3(0) = 0 + 0 = 0$
- Bottom-right entry: $0\left(-\frac{1}{2}\right) + 3\left(\frac{1}{3}\right) = 0 + 1 = 1$

$$
(AB)(B^{-1}A^{-1}) = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I
$$

Since the product is $I$, the identity $(AB)^{-1} = B^{-1}A^{-1}$ is verified.