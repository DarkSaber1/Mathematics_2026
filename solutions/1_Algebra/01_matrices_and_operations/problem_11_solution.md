# Exercise 11 – When Do Matrices Commute?

## Problem Statement

Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

## Solution

### 1. Calculation of Matrix Products $AB$ and $BA$

- **Product $AB$:**

$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} 1(a)+1(c) & 1(b)+1(d) \\ 0(a)+1(c) & 0(b)+1(d) \end{pmatrix} = \begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix}
$$

- **Product $BA$:**

$$
BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a(1)+b(0) & a(1)+b(1) \\ c(1)+d(0) & c(1)+d(1) \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}
$$

### 2. Deriving Conditions for Commutativity ($AB = BA$)

For $AB = BA$ to hold, their corresponding entries must be equal element-by-element:

1. **Top-left entry $(1,1)$:** $a + c = a \implies c = 0$
2. **Top-right entry $(1,2)$:** $b + d = a + b \implies d = a$
3. **Bottom-left entry $(2,1)$:** $c = c$ (holds automatically)
4. **Bottom-right entry $(2,2)$:** $d = c + d \implies c = 0$

Thus, the required necessary and sufficient conditions for commutativity are:

$$
c = 0 \quad \text{and} \quad d = a
$$

### 3. General Form of Matrix $B$

Substituting $c = 0$ and $d = a$ into matrix $B$ yields the general form for all commuting matrices:

$$
B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix} \quad \text{where } a, b \in \mathbb{R}
$$

### Explanation

Although matrix multiplication is generally noncommutative, specific matrices can commute if their algebraic structure aligns. In this case, any matrix $B$ that commutes with $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$ must be an upper triangular matrix with equal diagonal elements.

### Verification

We multiply $A$ by the generalized commuting matrix $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$ in both orders:

- **$AB$:**

$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ 0 & a \end{pmatrix} = \begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}
$$

- **$BA$:**

$$
BA = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}
$$

Since $AB = BA = \begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}$, the conditions and general form are fully verified.