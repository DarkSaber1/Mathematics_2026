# Exercise 9 – Composing Transformations

## Problem Statement

Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

### 1. Calculation of $RSx$ (Scale First, Then Rotate)

- **Step 1:** Apply scaling $S$ to vector $x$:

$$
Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2(1)+0(2) \\ 0(1)+1(2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}
$$

- **Step 2:** Apply rotation $R$ to the resulting vector $Sx$:

$$
RSx = R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(2)-1(2) \\ 1(2)+0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

### 2. Calculation of $SRx$ (Rotate First, Then Scale)

- **Step 1:** Apply rotation $R$ to vector $x$:

$$
Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(1)-1(2) \\ 1(1)+0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix}
$$

- **Step 2:** Apply scaling $S$ to the resulting vector $Rx$:

$$
SRx = S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} 2(-2)+0(1) \\ 0(-2)+1(1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

### 3. Comparison and Geometric Explanation

Comparing the two resulting vectors:

$$
RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix} \neq \begin{pmatrix} -4 \\ 1 \end{pmatrix} = SRx
$$

- **Geometric interpretation of $RSx$:**  
  Vector $x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ is first stretched by a factor of 2 strictly along the horizontal $x$-axis, becoming $\begin{pmatrix} 2 \\ 2 \end{pmatrix}$. Rotating this vector by $90^\circ$ counterclockwise maps the positive $x$-axis to the positive $y$-axis, placing the stretched component on the $y$-axis: $\begin{pmatrix} -2 \\ 2 \end{pmatrix}$.

- **Geometric interpretation of $SRx$:**  
  Vector $x$ is first rotated $90^\circ$ counterclockwise, moving its original $y$-component ($2$) onto the negative $x$-axis as $-2$, giving $\begin{pmatrix} -2 \\ 1 \end{pmatrix}$. When scaling $S$ is applied second, it stretches whatever component currently resides on the $x$-axis. Thus, the original $y$-component gets doubled instead, yielding $\begin{pmatrix} -4 \\ 1 \end{pmatrix}$.

Because non-uniform scaling acts exclusively along fixed coordinate axes, rotating a vector prior to scaling changes which of its components gets stretched.

### Verification

We verify by matrix multiplication of the combined operators:

- Combined matrix $RS$:

$$
RS = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix}
\implies RSx = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

- Combined matrix $SR$:

$$
SR = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0 & -2 \\ 1 & 0 \end{pmatrix}
\implies SRx = \begin{pmatrix} 0 & -2 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

Both composite matrix evaluations match our step-by-step results, verifying that $RSx \neq SRx$.