
# Exercise 9 – Composing Transformations

## Problem Statement

Calculate $RSx$ and $SRx$. Compare the results and explain geometrically why the order of transformations matters.

## Solution

Given:

$$
S =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
$$

$$
R =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

$$
x =
\begin{pmatrix}
1 \\
2
\end{pmatrix}
$$

### 1. Calculate RSx

First, apply scaling:

$$
Sx =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix}
$$

$$
Sx =
\begin{pmatrix}
2(1)+0(2) \\
0(1)+1(2)
\end{pmatrix}
$$

$$
Sx =
\begin{pmatrix}
2 \\
2
\end{pmatrix}
$$

Then apply rotation:

$$
RSx =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
2 \\
2
\end{pmatrix}
$$

$$
RSx =
\begin{pmatrix}
0(2)-1(2) \\
1(2)+0(2)
\end{pmatrix}
$$

$$
RSx =
\begin{pmatrix}
-2 \\
2
\end{pmatrix}
$$

### 2. Calculate SRx

First, apply rotation:

$$
Rx =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1 \\
2
\end{pmatrix}
$$

$$
Rx =
\begin{pmatrix}
0(1)-1(2) \\
1(1)+0(2)
\end{pmatrix}
$$

$$
Rx =
\begin{pmatrix}
-2 \\
1
\end{pmatrix}
$$

Then apply scaling:

$$
SRx =
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-2 \\
1
\end{pmatrix}
$$

$$
SRx =
\begin{pmatrix}
2(-2)+0(1) \\
0(-2)+1(1)
\end{pmatrix}
$$

$$
SRx =
\begin{pmatrix}
-4 \\
1
\end{pmatrix}
$$

## Explanation

Matrix S doubles the horizontal coordinate while keeping the vertical coordinate unchanged.

Matrix R rotates a vector 90 degrees counterclockwise.

In RSx, scaling is applied before rotation.

In SRx, rotation is applied before scaling.

The order matters because rotation changes the direction in which scaling is applied.

## Verification

The two results are:

$$
RSx =
\begin{pmatrix}
-2 \\
2
\end{pmatrix}
$$

$$
SRx =
\begin{pmatrix}
-4 \\
1
\end{pmatrix}
$$

Since the results are different:

$$
RSx \neq SRx
$$

## Final Answer

$$
\boxed{
RSx =
\begin{pmatrix}
-2 \\
2
\end{pmatrix}
}
$$

$$
\boxed{
SRx =
\begin{pmatrix}
-4 \\
1
\end{pmatrix}
}
$$

Therefore, the order of transformations affects the final result.
