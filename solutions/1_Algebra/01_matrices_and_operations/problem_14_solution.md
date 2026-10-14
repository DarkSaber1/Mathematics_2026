
# Exercise 14 – Rotation Matrices

## Problem Statement

Calculate R(α)R(β) and show that it equals R(α+β) using the angle-sum formulas for sine and cosine. Explain the result geometrically.

## Solution

Given the rotation matrix:

$$
R(\theta) =
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{pmatrix}
$$

### 1. Multiply the Rotation Matrices

$$
R(\alpha) =
\begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{pmatrix}
$$

$$
R(\beta) =
\begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta
\end{pmatrix}
$$

Now multiply the matrices:

$$
R(\alpha)R(\beta) =
\begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta
\end{pmatrix}
$$

Multiplying rows by columns gives:

$$
R(\alpha)R(\beta) =
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta &
-\cos\alpha\sin\beta-\sin\alpha\cos\beta \\
\sin\alpha\cos\beta+\cos\alpha\sin\beta &
-\sin\alpha\sin\beta+\cos\alpha\cos\beta
\end{pmatrix}
$$

### 2. Apply the Angle-Sum Formulas

Using the trigonometric identities:

$$
\cos(\alpha+\beta) =
\cos\alpha\cos\beta-\sin\alpha\sin\beta
$$

$$
\sin(\alpha+\beta) =
\sin\alpha\cos\beta+\cos\alpha\sin\beta
$$

Substituting these identities:

$$
R(\alpha)R(\beta) =
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta)
\end{pmatrix}
$$

This is exactly the rotation matrix for the angle α+β.

Therefore:

$$
\boxed{R(\alpha)R(\beta)=R(\alpha+\beta)}
$$

## Explanation

A rotation matrix rotates a vector counterclockwise by a given angle.

Applying a rotation of β followed by a rotation of α is equivalent to rotating once by the sum of the two angles.

Geometrically, the total rotation angle is α+β.

## Verification

Consider:

$$
\alpha=90^\circ,\qquad \beta=90^\circ
$$

The rotation matrix is:

$$
R(90^\circ) =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

Multiplying two rotations:

$$
R(90^\circ)R(90^\circ) =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
-1 & 0 \\
0 & -1
\end{pmatrix}
$$

Now calculate the combined rotation:

$$
R(180^\circ) =
\begin{pmatrix}
-1 & 0 \\
0 & -1
\end{pmatrix}
$$

Both results are equal, so the property is verified for this example.

## Final Answer

$$
\boxed{
R(\alpha)R(\beta)=R(\alpha+\beta)
}
$$

Two consecutive rotations are equivalent to one rotation by the sum of their angles.
