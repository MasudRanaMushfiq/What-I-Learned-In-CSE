

# Co-ordinate Geometry

### Course Information
**Course:** MATH-1221 (Co-ordinate Geometry, Vector Analysis, and Complex Variable)
**Course Type:** Theory, 3 Credit
**Prerequisite:** None
### Instructor
Dr. Mohd. Altab Hossain, Professor, Dept. of Mathematics, University of Rajshahi

### Course Motivation
> To know basics of co-ordinate geometry, vector analysis, complex variable, calculus, and counting principles.

---

## Course Contents

| Area                                               | Topics Covered                                                                                                                                                                                                                                                                                                                                            |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Coordinate Geometry**                               | Coordinate Systems (2D & 3D), Lines and Angles in Space, The Plane and Straight Line, Shortest Distance, Pairs of Lines |
| **Vector Analysis**            | Vector Algebra, Dot (Scalar) Product, Cross (Vector) Product, Vector Differentiation and Operators, Gradient, Divergence, Curl, Integral Theorems (Divergence Theorem of Gauss, Stokes' Theorem)                                                                                                             |
| **Complex Variables** | Complex Numbers and Functions, Analytic Functions, Cauchy-Riemann Equations, Complex Integration, Cauchy’s Theorem, Cauchy’s Integral Formula, Laurent Series, Residue Theorem                                                                                                                |
| **Permutations and Combinations**                               | Permutations ($^n P_r$), Combinations ($^n C_r$), Word Formation |
| **Differential and Integral Calculus**                               | Continuity and Differentiability, Mean Value Theorem, Integration Techniques |

---

## Textbooks

**Primary Texts:**
1. No specific textbook listed in the provided curriculum text.

---

## Table of Contents

1. [Module I – Coordinate Geometry](#module-i)
2. [Module II – Vector Analysis](#module-ii)
3. [Module III – Complex Variables](#module-iii)
4. [Module IV – Permutations and Combinations](#module-iv)
5. [Module V – Differential and Integral Calculus](#module-v)

---

## Module I
## Coordinate Geometry

### 1. Coordinate Systems (2D & 3D)

- **Rectangular System:** Axes are inclined at 90°.
- **Oblique System:** Axes are inclined at an angle $\omega$.
- **Transformation Relations:** The relation between rectangular coordinates $(x, y)$ and oblique coordinates $(x_1, y_1)$ is given by $x = x_1 + y_1 \cos \omega$ and $y = y_1 \sin \omega$.

### 2. Lines and Angles in Space

- **Direction Cosines (d.c.'s):** Denoted by $l, m, n$, where $l = \cos \alpha$, $m = \cos \beta$, and $n = \cos \gamma$ for the angles a line makes with the axes. A fundamental property is $l^2 + m^2 + n^2 = 1$.
- **Direction Ratios (d.r.'s):** Any three numbers $a, b, c$ proportional to the direction cosines.
- **Projection:** The projection of a line segment on another line is the "shadow" it casts, helping to understand where a segment hits another line if extended. The projection of the join of two points $(x_1, y_1, z_1)$ and $(x_2, y_2, z_2)$ on a line with d.c.'s $l, m, n$ is $(x_2 - x_1)l + (y_2 - y_1)m + (z_2 - z_1)n$.
- **Angle between lines:** If two lines have d.c.'s $(l_1, m_1, n_1)$ and $(l_2, m_2, n_2)$, the angle $\theta$ between them is $\cos \theta = l_1l_2 + m_1m_2 + n_1n_2$.

### 3. The Plane and Straight Line

- **General Equation of a Plane:** Every first-degree equation in $x, y, z$ represents a plane: $ax + by + cz + d = 0$.
- **Shortest Distance (S.D.):** The S.D. between two skew lines is the projection of the join of any two points on the lines onto the line perpendicular to both.
- **Pairs of Lines:** A homogeneous quadratic equation $ax^2 + 2hxy + by^2 = 0$ represents two straight lines passing through the origin. These lines are real if $h^2 > ab$.

---

## Module II
## Vector Analysis

### 1. Vector Algebra

- **Definitions:** **Scalars** have magnitude only (e.g., mass, temperature); **Vectors** have both magnitude and direction (e.g., force, velocity).
- **Dot (Scalar) Product:** $A \cdot B = |A||B| \cos \theta$. It is commutative ($A \cdot B = B \cdot A$).
    - **CSE Application:** In **Computer Graphics**, the dot product is used for back-face culling and lighting calculations (Lambertian reflectance) to determine how much light hits a surface based on the angle between the light source and the surface normal.
- **Cross (Vector) Product:** $A \times B = |A||B| \sin \theta \mathbf{n}$. The magnitude represents the area of a parallelogram with sides $A$ and $B$.

### 2. Vector Differentiation and Operators

- **Frenet-Serret Formulas:** Describe the kinematic properties of a particle moving along a continuous, differentiable curve in 3D space using the **Tangent ($T$)**, **Normal ($N$)**, and **Binormal ($B$)** vectors.
- **Gradient ($\nabla \phi$):** Represents the rate of change of a scalar field $\phi$. It is always perpendicular to the surface $\phi(x, y, z) = c$.
- **Divergence ($\nabla \cdot A$):** A scalar measure of a vector field's "source" or "sink" at a given point.
- **Curl ($\nabla \times A$):** A vector measure of the rotation of a vector field.

### 3. Integral Theorems

- **Divergence Theorem of Gauss:** Relates the surface integral of the normal component of a vector $A$ to the volume integral of its divergence: $\iiint_V \nabla \cdot A \, dV = \iint_S A \cdot \mathbf{n} \, dS$.
- **Stokes' Theorem:** Relates a line integral around a closed curve to a surface integral of the curl of the vector field.

---

## Module III
## Complex Variables

### 1. Complex Numbers and Functions

- **Definition:** $z = a + bi$, where $i^2 = -1$.
- **Analytic Functions:** A function $f(z) = u + iv$ is analytic if it is differentiable and satisfies the **Cauchy-Riemann Equations**: $\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}$ and $\frac{\partial v}{\partial x} = -\frac{\partial u}{\partial y}$.
- **CSE Application:** **Signal Processing (FFT)**. Complex numbers allow the representation of signals in the frequency domain. The Fast Fourier Transform (FFT) uses these properties to efficiently compress audio (MP3) and images (JPEG).

### 2. Complex Integration

- **Cauchy’s Theorem:** If $f(z)$ is analytic within and on a simple closed curve $C$, then $\oint_C f(z) \, dz = 0$.
- **Cauchy’s Integral Formula:** Allows the value of an analytic function at a point inside a contour to be determined by the values on the contour: $f(a) = \frac{1}{2\pi i} \oint_C \frac{f(z)}{z-a} \, dz$.

### 3. Residues and Series

- **Laurent Series:** An expansion of a complex function in a region where it may have singularities, containing both positive and negative powers: $f(z) = \sum a_n(z-a)^n$.
- **Residue Theorem:** The integral of $f(z)$ around a closed curve $C$ is $2\pi i$ times the sum of the residues at its singularities within $C$. This is a powerful tool for evaluating real definite integrals that are otherwise difficult.

---

## Module IV
## Permutations and Combinations

- **Permutations ($^n P_r$):** Arrangements where order matters: $^n P_r = \frac{n!}{(n-r)!}$.
- **Combinations ($^n C_r$):** Selections where order does not matter: $^n C_r = \frac{n!}{r!(n-r)!}$.
- **Word Formation:** If some items are identical, the number of permutations is $\frac{n!}{p!q!r!}$ where $p, q, r$ are the counts of identical items.
- **CSE Application:** **Cryptography and Security**. These principles are used to calculate the complexity of "brute-force" attacks. For instance, the number of possible $k$-length passwords from a set of $n$ characters is a variation of permutation with repetition ($n^k$).

---

## Module V
## Differential and Integral Calculus

- **Continuity and Differentiability:** A function $f(x)$ is continuous at $x=c$ if the limit equals the function value; it is differentiable if the derivative exists at that point.
- **Mean Value Theorem:** Provides a relationship between the average rate of change and the instantaneous rate of change.
- **Integration Techniques:** Includes reduction formulas for powers of trigonometric functions (e.g., $\int \sin^n x \, dx$) and methods for evaluating definite integrals as the limit of a sum.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
|---|---|---|
| Module I | Coordinate Geometry | Rectangular System, Oblique System, d.c.'s, d.r.'s, Projection, Plane, Shortest Distance, Pairs of Lines |
| Module II | Vector Analysis | Scalars, Vectors, Dot Product, Cross Product, Frenet-Serret Formulas, Gradient, Divergence, Curl, Divergence Theorem, Stokes' Theorem |
| Module III | Complex Variables | $z = a+bi$, Analytic Functions, Cauchy-Riemann Equations, Cauchy’s Theorem, Cauchy’s Integral Formula, Laurent Series, Residue Theorem |
| Module IV | Permutations and Combinations | $^n P_r$, $^n C_r$, Word Formation, Identical Items |
| Module V | Differential and Integral Calculus | Continuity, Differentiability, Mean Value Theorem, Reduction Formulas, Limit of a Sum |

---
*MATH-1221 — Co-ordinate Geometry, Vector Analysis, and Complex Variable | Dept. of CSE*






