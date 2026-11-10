# Exercise 14 – Rotation Matrices

## Problem Statement

The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}
$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that

$$
R(\alpha)R(\beta)=R(\alpha+\beta).
$$

Explain the result geometrically.

## Solution

### 1. Calculation of $R(\alpha)R(\beta)$

Given the rotation matrices for angles $\alpha$ and $\beta$:

$$
R(\alpha) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix}, \qquad R(\beta) = \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix}
$$

Multiplying $R(\alpha)$ by $R(\beta)$:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix}
$$

$$
= \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -\cos\alpha\sin\beta - \sin\alpha\cos\beta \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta \end{pmatrix}
$$

### 2. Applying Trigonometric Angle-Sum Formulas

We use the standard trigonometric sum identities:
- $\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
- $\sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$

Factoring out the negative sign in the top-right entry:
$$
-(\cos\alpha\sin\beta + \sin\alpha\cos\beta) = -\sin(\alpha+\beta)
$$

Substituting these identities back into the matrix yields:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha+\beta)
$$

### 3. Geometric Explanation

The matrix $R(\theta)$ represents a linear transformation that rotates any 2D vector counterclockwise around the origin by an angle $\theta$. 
Applying $R(\beta)$ first rotates a vector by angle $\beta$. Subsequently applying $R(\alpha)$ rotates the resulting vector by an additional angle $\alpha$. Geometrically, performing two successive rotations of angles $\beta$ and $\alpha$ in the same plane is completely equivalent to performing a single combined rotation of total angle $\alpha + \beta$.

### Verification

We test the identity using $\alpha = 90^\circ$ and $\beta = 90^\circ$:

$$
R(90^\circ) = \begin{pmatrix} \cos 90^\circ & -\sin 90^\circ \\ \sin 90^\circ & \cos 90^\circ \end{pmatrix} = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}
$$

- **Left-hand side $R(90^\circ)R(90^\circ)$:**

$$
R(90^\circ)R(90^\circ) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}
$$

- **Right-hand side $R(90^\circ + 90^\circ) = R(180^\circ)$:**

$$
R(180^\circ) = \begin{pmatrix} \cos 180^\circ & -\sin 180^\circ \\ \sin 180^\circ & \cos 180^\circ \end{pmatrix} = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}
$$

Since both evaluations produce $\begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$, the identity $R(\alpha)R(\beta) = R(\alpha+\beta)$ is verified.