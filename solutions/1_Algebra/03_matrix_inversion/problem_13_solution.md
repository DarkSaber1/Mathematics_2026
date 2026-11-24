# Exercise 13 – Undoing a Composite Transformation

## Problem Statement

The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

## Solution

### 1. Method 1: Compute $T = HS$ First, Then Its Inverse

First, we compute the product matrix $T = HS$:

$$
T = HS = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(2) + 1(0) & 1(0) + 1(1) \\ 0(2) + 1(0) & 0(0) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}
$$

Next, we find $T^{-1}$ using the $2 \times 2$ inverse formula. The determinant of $T$ is:

$$
\det(T) = (2)(1) - (1)(0) = 2
$$

Applying the $2 \times 2$ inverse formula:

$$
T^{-1} = \frac{1}{2} \begin{pmatrix} 1 & -1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}
$$

---

### 2. Method 2: Using $(HS)^{-1} = S^{-1}H^{-1}$

First, we compute the individual inverses $S^{-1}$ and $H^{-1}$:

- **For $S$:** $\det(S) = (2)(1) - (0)(0) = 2$, so:

$$
S^{-1} = \frac{1}{2} \begin{pmatrix} 1 & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix}
$$

- **For $H$:** $\det(H) = (1)(1) - (1)(0) = 1$, so:

$$
H^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}
$$

Now, we multiply $S^{-1}$ by $H^{-1}$:

$$
S^{-1}H^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(1) + 0(0) & \frac{1}{2}(-1) + 0(1) \\ 0(1) + 1(0) & 0(-1) + 1(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}
$$

---

### 3. Comparison and Verification of the Incorrect Order ($H^{-1}S^{-1}$)

Comparing the results of Method 1 and Method 2 confirms they are identical:

$$
T^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix} = S^{-1}H^{-1}
$$

Now, we compute the product in the incorrect order $H^{-1}S^{-1}$:

$$
H^{-1}S^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1\left(\frac{1}{2}\right) + (-1)(0) & 1(0) + (-1)(1) \\ 0\left(\frac{1}{2}\right) + 1(0) & 0(0) + 1(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -1 \\ 0 & 1 \end{pmatrix}
$$

Comparing the $(1,2)$ entries ($-\frac{1}{2} \neq -1$) shows that the incorrect order yields a different matrix:

$$
H^{-1}S^{-1} \neq (HS)^{-1}
$$

---

### 4. Explanation of the Rule: Undoing Operations from the End

When the composite transformation $T = HS$ acts on an input vector $v$, matrix multiplication is evaluated from right to left:

$$
Tv = (HS)v = H(Sv)
$$

This means that **scaling ($S$) is applied first**, and **shear ($H$) is applied second (at the end)**. 

To reverse this process and restore the original vector $v$, we must undo the operations in reverse chronological order—starting from the last operation applied:
1. First, undo the shear $H$ by applying $H^{-1}$.
2. Second, undo the scaling $S$ by applying $S^{-1}$.

Algebraically, this corresponds to multiplying by $S^{-1}H^{-1}$:

$$
(S^{-1}H^{-1})(HS)v = S^{-1}(H^{-1}H)Sv = S^{-1}ISv = S^{-1}Sv = v
$$

Using $H^{-1}S^{-1}$ attempts to undo the scaling before undoing the shear, which fails to reverse the transformation properly.