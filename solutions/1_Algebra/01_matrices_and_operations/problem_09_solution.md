
# Exercise 9 – Composing Transformations

## Problem Statement

Calculate $RSx$ and $SRx$. Compare the results and explain why the order of transformations matters.

## Solution

Given:

$$
S = \begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix},
\quad
R = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix},
\quad
x = \begin{pmatrix}1\\2\end{pmatrix}
$$

### 1. Calculate RSx

First, apply scaling:

$$
Sx =
\begin{pmatrix}
2(1)+0(2)\\
0(1)+1(2)
\end{pmatrix}
=
\begin{pmatrix}2\\2\end{pmatrix}
$$

Then apply rotation:

$$
RSx =
R\begin{pmatrix}2\\2\end{pmatrix}
=
\begin{pmatrix}
0(2)-1(2)\\
1(2)+0(2)
\end{pmatrix}
=
\begin{pmatrix}-2\\2\end{pmatrix}
$$

### 2. Calculate SRx

First, apply rotation:

$$
Rx =
\begin{pmatrix}
0(1)-1(2)\\
1(1)+0(2)
\end{pmatrix}
=
\begin{pmatrix}-2\\1\end{pmatrix}
$$

Then apply scaling:

$$
SRx =
S\begin{pmatrix}-2\\1\end{pmatrix}
=
\begin{pmatrix}
2(-2)+0(1)\\
0(-2)+1(1)
\end{pmatrix}
=
\begin{pmatrix}-4\\1\end{pmatrix}
$$

## Explanation

Matrix S doubles the horizontal coordinate, while matrix R rotates a vector 90 degrees counterclockwise.

In RSx, scaling is applied before rotation.

In SRx, rotation is applied before scaling.

The order matters because the horizontal direction changes after rotation.

## Verification

The results are:

$$
RSx = \begin{pmatrix}-2\\2\end{pmatrix}
$$

$$
SRx = \begin{pmatrix}-4\\1\end{pmatrix}
$$

Since the results are different:

$$
RSx \neq SRx
$$

## Final Answer

$$
\boxed{RSx = \begin{pmatrix}-2\\2\end{pmatrix}}
$$

$$
\boxed{SRx = \begin{pmatrix}-4\\1\end{pmatrix}}
$$

Therefore, the order of transformations affects the final result.
