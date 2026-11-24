# Exercise 10 – Triangle Area from Vectors

## Problem Statement

The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

## Solution

### 1. Constructing the Side Vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$

Starting from vertex $A = (0, 0, 0)$, we construct the two adjacent edge vectors of the triangle:

$$
\overrightarrow{AB} = B - A = (2 - 0,\, 1 - 0,\, 0 - 0) = (2, 1, 0)
$$

$$
\overrightarrow{AC} = C - A = (1 - 0,\, 3 - 0,\, 2 - 0) = (1, 3, 2)
$$

---

### 2. Computing the Area of the Parallelogram Using the Cross Product

The area of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$ is equal to the Euclidean norm (magnitude) of their cross product:

$$
\text{Area}_{\text{parallelogram}} = \|\overrightarrow{AB} \times \overrightarrow{AC}\|
$$

First, compute the cross product $\overrightarrow{AB} \times \overrightarrow{AC}$:

$$
\overrightarrow{AB} \times \overrightarrow{AC} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & 0 \\ 1 & 3 & 2 \end{vmatrix}
$$

Expanding by minors:

$$
\overrightarrow{AB} \times \overrightarrow{AC} = \mathbf{i} \begin{vmatrix} 1 & 0 \\ 3 & 2 \end{vmatrix} - \mathbf{j} \begin{vmatrix} 2 & 0 \\ 1 & 2 \end{vmatrix} + \mathbf{k} \begin{vmatrix} 2 & 1 \\ 1 & 3 \end{vmatrix}
$$

$$
\overrightarrow{AB} \times \overrightarrow{AC} = ((1)(2) - (0)(3))\mathbf{i} - ((2)(2) - (0)(1))\mathbf{j} + ((2)(3) - (1)(1))\mathbf{k}
$$

$$
\overrightarrow{AB} \times \overrightarrow{AC} = 2\mathbf{i} - 4\mathbf{j} + 5\mathbf{k} = (2, -4, 5)
$$

Next, compute the magnitude of this cross product vector:

$$
\text{Area}_{\text{parallelogram}} = \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5}
$$

---

### 3. Finding the Area of the Triangle $\triangle ABC$

The area of triangle $\triangle ABC$ is half the area of the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$:

$$
\text{Area}_{\triangle ABC} = \frac{1}{2} \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \frac{1}{2} (3\sqrt{5}) = \frac{3\sqrt{5}}{2}
$$

---

### 4. Explanation of the Factor $\frac{1}{2}$

Geometrically, the two vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ define two adjacent sides of a parallelogram $ABDC$ (where $D$ is the fourth vertex $B + C - A$). 

Drawing the diagonal segment $BC$ divides this parallelogram into **two congruent triangles** ($\triangle ABC$ and $\triangle DCB$) that have identical base lengths and identical perpendicular heights. Because the two triangles have equal area and together compose the entire parallelogram, each triangle occupies exactly **half** ($\frac{1}{2}$) of the parallelogram's total area.