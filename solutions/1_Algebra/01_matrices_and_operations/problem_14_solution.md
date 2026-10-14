
# Exercise 14 – Rotation Matrices

## Problem Statement

Calculate R(α)R(β) and prove that it equals R(α+β) using the angle-sum formulas for sine and cosine. Explain the result geometrically.

## Solution

Given the rotation matrix:

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta\\
\sin\theta & \cos\theta
\end{pmatrix}
$$

### 1. Multiply the Rotation Matrices

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha\\
\sin\alpha & \cos\alpha
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta\\
\sin\beta & \cos\beta
\end{pmatrix}
$$

Multiplying rows by columns:

$$
=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta &
-\cos\alpha\sin\beta-\sin\alpha\cos\beta\\
\sin\alpha\cos\beta+\cos\alpha\sin\beta &
-\sin\alpha\sin\beta+\cos\alpha\cos\beta
\end{pmatrix}
$$

### 2. Apply the Angle-Sum Formulas

Using the identities:

$$
\cos(\alpha+\beta)=
\cos\alpha\cos\beta-\sin\alpha\sin\beta
$$

$$
\sin(\alpha+\beta)=
\sin\alpha\cos\beta+\cos\alpha\sin\beta
$$

We obtain:

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta)\\
\sin(\alpha+\beta) & \cos(\alpha+\beta)
\end{pmatrix}
$$

Therefore:

$$
\boxed{R(\alpha)R(\beta)=R(\alpha+\beta)}
$$

## Explanation

A rotation matrix rotates a vector counterclockwise by a given angle.

Applying a rotation of β followed by a rotation of α is equivalent to rotating once by α+β.

Therefore, the angles are added when two rotation matrices are multiplied.

## Verification

For α = 90° and β = 90°:

$$
R(90^\circ)=
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
$$

Multiplying:

$$
R(90^\circ)R(90^\circ)=
\begin{pmatrix}
-1 & 0\\
0 & -1
\end{pmatrix}
$$

This equals:

$$
R(180^\circ)=
\begin{pmatrix}
-1 & 0\\
0 & -1
\end{pmatrix}
$$

The property is verified.

## Final Answer

$$
\boxed{R(\alpha)R(\beta)=R(\alpha+\beta)}
$$

Two consecutive rotations are equivalent to one rotation by the sum of their angles.
