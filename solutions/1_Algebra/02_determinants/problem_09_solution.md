## Exercise 9. Area and the Determinant

### Problem Definition
Given the vectors in $\mathbb{R}^2$:[cite: 1]

$$
u = \begin{pmatrix} 3 \\ 1 \end{pmatrix}, \qquad v = \begin{pmatrix} 1 \\ 4 \end{pmatrix}
$$

1. Compute the area of the parallelogram spanned by vectors $u$ and $v$ using a determinant.[cite: 1]
2. Reverse the order of the vectors (forming a matrix with $v$ first, then $u$) and compute the new determinant.[cite: 1]
3. Explain what changes in the determinant value and what remains unchanged regarding the geometric area.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Geometric Relationship Between Determinants and Area

In 2D space ($\mathbb{R}^2$), two vectors $u = \begin{pmatrix} u_1 \\ u_2 \end{pmatrix}$ and $v = \begin{pmatrix} v_1 \\ v_2 \end{pmatrix}$ define a parallelogram.

The determinant of the matrix $M = \begin{pmatrix} u & v \end{pmatrix} = \begin{pmatrix} u_1 & v_1 \\ u_2 & v_2 \end{pmatrix}$ represents the **signed area** of this parallelogram:

* **Signed Area (Determinant):**
  $$ \det M = \det \begin{pmatrix} u_1 & v_1 \\ u_2 & v_2 \end{pmatrix} = u_1 v_2 - u_2 v_1 $$

* **Geometric Area (Absolute Value):**
  Since physical area must always be non-negative ($\text{Area} \ge 0$), the geometric area of the parallelogram is given by the absolute value of the determinant:
  $$ \text{Area} = |\det M| = \left| \det \begin{pmatrix} u_1 & v_1 \\ u_2 & v_2 \end{pmatrix} \right| $$

---

#### Step 2: Computing the Determinant and Parallelogram Area for Order $(u, v)$

Form the $2 \times 2$ matrix $M$ using $u$ as the first column and $v$ as the second column:[cite: 1]

$$
M = \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}
$$

##### Determinant Calculation
Applying the $2 \times 2$ determinant formula:

$$
\det M = (3 \cdot 4) - (1 \cdot 1) = 12 - 1 = 11
$$

##### Parallelogram Area
Taking the absolute value of the determinant:

$$
\text{Area} = |\det M| = |11| = 11 \text{ square units}
$$

---

#### Step 3: Reversing the Order of Vectors to $(v, u)$

Now, swap the order of the vectors to form a new matrix $M' = \begin{pmatrix} v & u \end{pmatrix}$:[cite: 1]

$$
M' = \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix}
$$

##### Determinant Calculation
Applying the $2 \times 2$ determinant formula:

$$
\det M' = (1 \cdot 1) - (3 \cdot 4) = 1 - 12 = -11
$$

##### Parallelogram Area
Taking the absolute value of the new determinant:

$$
\text{Area}' = |\det M'| = |-11| = 11 \text{ square units}
$$

---

#### Step 4: Geometric and Algebraic Explanation

##### 1. What Changes: The Sign of the Determinant (Orientation)
* When the vector order is reversed, the columns of the matrix are swapped ($C_1 \leftrightarrow C_2$).
* According to the **Column Swap Property** of determinants (identical to the row swap property), swapping two columns flips the sign of the determinant:
  $$ \det \begin{pmatrix} v & u \end{pmatrix} = -\det \begin{pmatrix} u & v \end{pmatrix} $$
* **Geometric Orientation:** The sign of the determinant reflects the **orientation** (handedness) of the vector pair:
  * $\det M = +11 > 0$: Going counterclockwise from $u$ to $v$ follows a standard **positive (right-handed)** orientation.
  * $\det M' = -11 < 0$: Going counterclockwise from $v$ to $u$ follows a **negative (left-handed)** orientation.

##### 2. What Does Not Change: The Geometric Area
* The physical shape and dimensions of the parallelogram defined by $u$ and $v$ are completely unchanged regardless of which vector is named first.
* Because geometric area is calculated as the magnitude (absolute value) of the signed determinant, taking the absolute value removes the orientation sign:
  $$ \text{Area} = |\det M| = |11| = 11 = |-11| = |\det M'| $$

---

### Conclusion and Key Takeaways

1. **Calculated Determinants:**
   * For matrix $\begin{pmatrix} u & v \end{pmatrix}$: $\det M = 11$[cite: 1]
   * For matrix $\begin{pmatrix} v & u \end{pmatrix}$: $\det M' = -11$[cite: 1]

2. **Parallelogram Area:**
   * $\text{Area} = 11$ square units (unchanged in both cases).[cite: 1]

3. **Core Insight:**
   * The **determinant** measures *signed* scale with orientation (+ vs -).[cite: 1]
   * The **area** measures *absolute* geometric size, requiring the absolute value $|\det M|$.[cite: 1]