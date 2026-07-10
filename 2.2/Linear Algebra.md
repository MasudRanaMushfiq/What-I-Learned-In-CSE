

# Linear Algebra

### Course Information
**Course:** MATH 2241 (Linear Algebra)
**Course Type:** Theory, 3 Credit
**Prerequisite:** MATH 1121 Differential and Integral Calculus, MATH1221 Co-ordinate Geometry, Vector analysis and Complex Variable, MATH 2131 Differential Equations and Optimization

### Instructor
Dr. Shiuly Akhter, Professor, Dept. of Mathematics, University of Rajshahi 

### Course Motivation
> To develop a mathematical base for signal processing, machine learning and mathematical modeling.

---

## Course Contents

| Area | Topics Covered |
| ---- | -------------- |
| **Matrices** | Definition of Matrices: Equality of two Matrices, Addition, Subtraction and Multiplication of Matrices, Equivalence of Matrices, Positive and Negative Matrices, Adjoint of Matrices, Transpose and Inverse of Matrices, Rank and Normal form of Matrices |
| **System of Linear Equations** | Solution of Homogeneous and Non-Homogeneous Systems, Determination of Eigen Values and Eigen Vectors, Solutions of Matrix Differential Equations |
| **Linear Algebra** | Vector Space, Subspace, Sum and Direct Sum, Basis and Dimension, Hilbert Space, Normed Linear Space Branch Space |
| **Linear Transformation** | Range, Kernel, Nullity, Singular and Non-Singular Transformation |
| **Linear Operations** | Matrix Representation of a Linear Operator, Change of Basis, Similarity and Linear Mapping. Norms and Inner products, Orthogonal complements, orthonormal sets, Gram-schmidt orthogonalization process |
| **Diagonalization** | Properties of Eigenvalues and Eigenvectors, Positive definite Matrices, Matrix Decomposition |


## Textbooks

**Primary Texts:**
1. David C. Lay — *Linear Algebra and Its Application*, Pearson
2. M. L. Khanna — *Matrices*, Jai Prakash Nath and Co.

---

## Table of Contents

1. [Chapter 1 – Matrices](#chapter-1)
2. [Chapter 2 – System of Linear Equations](#chapter-2)
3. [Chapter 3 – Vector Spaces and Subspaces](#chapter-3)
4. [Chapter 4 – Linear Combinations, Basis and Dimension](#chapter-4)
5. [Chapter 5 – Linear Mappings (Transformations)](#chapter-5)
6. [Chapter 6 – Matrices and Linear Operations](#chapter-6)
7. [Chapter 7 – Inner Product Spaces](#chapter-7)
8. [Chapter 8 – Eigenvalues, Eigenvectors and Diagonalization](#chapter-8)

---

## Chapter 1
## Matrices

### 1.1 Definition of Matrices

- **Definition of Matrices:** A matrix is a rectangular array of numbers arranged in rows and columns. The size or dimension of a matrix is given by $m \times n$, where $m$ is the number of rows and $n$ is the number of columns.

### 1.2 Equality of Two Matrices

- **Equality of two Matrices:** Two matrices $A$ and $B$ are equal if and only if they have the same dimension and their corresponding entries are equal.

### 1.3 Addition, Subtraction and Multiplication of Matrices

- **Addition:** Matrices of the same dimension can be added by adding corresponding entries: $(A + B)_{ij} = A_{ij} + B_{ij}$.
- **Subtraction:** Matrices of the same dimension can be subtracted by subtracting corresponding entries: $(A - B)_{ij} = A_{ij} - B_{ij}$.
- **Multiplication of Matrices:** The product $AB$ is defined only when the number of columns of $A$ equals the number of rows of $B$. The $(i,j)$-entry of $AB$ is the dot product of the $i$-th row of $A$ and the $j$-th column of $B$.

### 1.4 Equivalence of Matrices

- **Equivalence of Matrices:** Two matrices $A$ and $B$ are said to be equivalent if one can be obtained from the other by a sequence of elementary row and column operations.

### 1.5 Positive and Negative Matrices

- **Positive and Negative Matrices:** A matrix is called a positive matrix if all its entries are positive. A matrix is called a negative matrix if all its entries are negative.

### 1.6 Adjoint of Matrices

- **Adjoint of Matrices:** The adjoint (or adjugate) of a square matrix $A$ is the transpose of its cofactor matrix, denoted by $\text{adj}(A)$. It satisfies $A \cdot \text{adj}(A) = \text{adj}(A) \cdot A = \det(A) I$.

### 1.7 Transpose and Inverse of Matrices

- **Transpose:** The transpose of a matrix $A$, denoted $A^T$, is obtained by interchanging its rows and columns.
- **Inverse of Matrices:** A square matrix $A$ is invertible if there exists a matrix $A^{-1}$ such that $A A^{-1} = A^{-1} A = I$. The inverse exists if and only if $\det(A) \neq 0$.

### 1.8 Rank and Normal Form of Matrices

- **Rank:** The rank of a matrix is the dimension of the row space or column space of a matrix. It equals the number of non-zero rows in its echelon form.
- **Normal form of Matrices:** A matrix is said to be in normal form (or canonical form) if it can be written as $\begin{bmatrix} I_r & 0 \\ 0 & 0 \end{bmatrix}$, where $r$ is the rank of the matrix.

---

## Chapter 2
## System of Linear Equations

### 2.1 Solution of Homogeneous and Non-Homogeneous Systems

- **Homogeneous System:** A system of linear equations of the form $Ax = 0$ always has the trivial solution $x = 0$. Non-trivial solutions exist if and only if the rank of $A$ is less than the number of variables.
- **Non-Homogeneous System:** A system of the form $Ax = b$. Solutions exist if and only if $\text{rank}(A) = \text{rank}([A|b])$.

### 2.2 Determination of Eigen Values and Eigen Vectors

- **Determination of Eigen Values and Eigen Vectors:** For a square matrix $A$, a scalar $\lambda$ is an eigenvalue if there exists a non-zero vector $v$ such that $Av = \lambda v$. The vector $v$ is called an eigenvector.

### 2.3 Solutions of Matrix Differential Equations

- **Solutions of Matrix Differential Equations:** A matrix differential equation of the form $\frac{dX}{dt} = AX$ has a solution $X(t) = e^{At} X(0)$, where $e^{At}$ is the matrix exponential.

---

## Chapter 3
## Vector Spaces and Subspaces

### 3.1 Vector Space Definition

- **Vector Space Definition:** A non-empty set $V$ over a field $K$ is a vector space if it satisfies eight axioms regarding vector addition and scalar multiplication. These include associativity, commutativity, the existence of a zero vector, and distributive properties.
- **Hilbert Space:** A Hilbert space is an inner product space that is complete with respect to the norm induced by the inner product (every Cauchy sequence converges).
- **Normed Linear Space Branch Space:** A normed linear space is a vector space equipped with a norm (a function that assigns a length to each vector). A Banach space is a complete normed linear space.

### 3.2 Subspaces

- **Subspaces:** A subset $W$ of $V$ is a subspace if $W$ is itself a vector space over $K$ under the same operations.
- **Criteria:** $W$ is a subspace if it is non-empty, closed under addition ($u, v \in W \implies u+v \in W$), and closed under scalar multiplication ($v \in W, k \in K \implies kv \in W$).

### 3.3 Sum and Direct Sum

- **Sum:** The sum of two subspaces $U$ and $W$ of $V$ is defined as $U + W = \{u + w : u \in U, w \in W\}$.
- **Direct Sum:** A vector space $V$ is the direct sum of subspaces $U$ and $W$ ($V = U \oplus W$) if every vector $v \in V$ can be written uniquely as $v = u + w$, where $u \in U$ and $w \in W$.
- **Theorem:** $V = U \oplus W$ if and only if $V = U + W$ and $U \cap W = \{0\}$.

---

## Chapter 4
## Linear Combinations, Basis and Dimension

### 4.1 Linear Combination

- **Linear Combination:** A vector $v$ is a linear combination of vectors $v_1, \dots, v_n$ if $v = a_1v_1 + a_2v_2 + \dots + a_nv_n$ for some scalars $a_i$.

### 4.2 Linear Span

- **Linear Span:** The set of all linear combinations of a set of vectors $S$ is called the span of $S$, denoted $L(S)$ or $\text{span}(S)$.

### 4.3 Linear Independence

- **Linear Independence:** A set of vectors $\{v_1, \dots, v_n\}$ is linearly independent if the equation $a_1v_1 + \dots + a_nv_n = 0$ implies all scalars $a_i = 0$. If any non-zero solution exists, the set is **linearly dependent**.
- **CSE Example:** In data science, linearly dependent features represent redundant information. Linear independence ensures each feature provides unique data for training models.

### 4.4 Basis

- **Basis:** A set $S$ is a basis for $V$ if it is linearly independent and spans $V$. Every vector in $V$ is uniquely expressed as a linear combination of basis vectors.

### 4.5 Dimension

- **Dimension:** The number of vectors in a basis of $V$ is called its dimension, $\dim(V)$.
- **Example ($R^3$):** The standard basis is $\{(1,0,0), (0,1,0), (0,0,1)\}$, so $\dim(R^3) = 3$.

---

## Chapter 5
## Linear Mappings (Transformations)

### 5.1 Definition

- **Definition:** A mapping $F: V \to U$ is linear if it preserves addition and scalar multiplication: $F(v+w) = F(v) + F(w)$ and $F(kv) = kF(v)$.

### 5.2 Range and Kernel

- **Kernel ($\text{Ker } F$):** The set of all $v \in V$ such that $F(v) = 0$.
- **Image ($\text{Im } F$):** The set of all points in $U$ that are images of vectors in $V$.

### 5.3 Nullity

- **Nullity:** The nullity of a linear transformation $F$ is the dimension of its kernel: $\text{nullity}(F) = \dim(\text{Ker } F)$.

### 5.4 Rank-Nullity Theorem

- **Rank-Nullity Theorem:** $\dim(V) = \text{rank}(F) + \text{nullity}(F)$, where $\text{rank}(F) = \dim(\text{Im } F)$ and $\text{nullity}(F) = \dim(\text{Ker } F)$.

### 5.5 Singular and Non-Singular Transformation

- **Singular and Non-Singular Transformation:** A linear transformation is singular if its kernel contains non-zero vectors (i.e., it is not one-to-one). It is non-singular if it is one-to-one (or equivalently, if its kernel is $\{0\}$).

### 5.6 Isomorphism

- **Isomorphism:** A bijective (one-to-one and onto) linear mapping. Isomorphic spaces have the same dimension.

---

## Chapter 6
## Matrices and Linear Operations

### 6.1 Matrix Representation of a Linear Operator

- **Matrix Representation:** A linear operator $T$ on $V$ can be represented by a matrix $[T]_e$ relative to a basis $\{e_i\}$. The $j$-th column of this matrix consists of the coordinates of $T(e_j)$.

### 6.2 Change of Basis

- **Change of Basis:** If $P$ is the transition matrix from basis $e$ to $f$, then for any vector $v$, $[v]_e = P[v]_f$.

### 6.3 Similarity and Linear Mapping

- **Similarity:** Matrices $A$ and $B$ are similar if $B = P^{-1}AP$ for some invertible matrix $P$. Similar matrices represent the same linear operator under different bases.
- **CSE Application:** Computer graphics use matrix transformations (rotation, scaling, translation) to manipulate 3D objects on a 2D screen.

### 6.4 Norms and Inner Products

- **Norms and Inner products:** An inner product is a function $\langle u, v \rangle$ assigning a scalar to vector pairs, satisfying linearity, symmetry (or conjugate symmetry for complex spaces), and positive definiteness. A norm is derived from an inner product as $\|v\| = \sqrt{\langle v, v \rangle}$.

### 6.5 Orthogonal Complements

- **Orthogonal complements:** For a subspace $W$ of an inner product space $V$, the orthogonal complement $W^\perp$ is the set of all vectors in $V$ that are orthogonal to every vector in $W$.

### 6.6 Orthonormal Sets

- **orthonormal sets:** A set of vectors is orthonormal if each vector has norm 1 and distinct vectors are orthogonal to each other.

### 6.7 Gram-Schmidt Orthogonalization Process

- **Gram-Schmidt Process:** An algorithm to convert any basis into an orthogonal or orthonormal basis.

---

## Chapter 7
## Inner Product Spaces

### 7.1 Inner Product

- **Inner Product:** A function $\langle u, v \rangle$ assigning a scalar to vector pairs, satisfying linearity, symmetry (or conjugate symmetry for complex spaces), and positive definiteness.

### 7.2 Norm and Distance

- **Norm and Distance:** The norm (length) of $v$ is $\|v\| = \sqrt{\langle v, v \rangle}$. The distance between $u$ and $v$ is $d(u,v) = \|u-v\|$.

### 7.3 Orthogonality

- **Orthogonality:** $u$ and $v$ are orthogonal if $\langle u, v \rangle = 0$.

### 7.4 Orthonormal Sets

- **Orthonormal Sets:** A set of vectors is orthonormal if each vector has norm 1 and distinct vectors are orthogonal to each other.

### 7.5 Gram-Schmidt Process

- **Gram-Schmidt Process:** An algorithm to convert any basis into an orthogonal or orthonormal basis.

---

## Chapter 8
## Eigenvalues, Eigenvectors and Diagonalization

### 8.1 Definitions

- **Definitions:** For a square matrix $A$, a scalar $\lambda$ is an **eigenvalue** if there exists a non-zero vector $v$ (**eigenvector**) such that $Av = \lambda v$.

### 8.2 Characteristic Equation

- **Characteristic Equation:** Eigenvalues are the roots of the polynomial $\det(A - \lambda I) = 0$.

### 8.3 Diagonalization

- **Diagonalization:** A matrix $A$ is diagonalizable if it is similar to a diagonal matrix $D$ ($A = PDP^{-1}$). This is possible if and only if $A$ has $n$ linearly independent eigenvectors.

### 8.4 Properties of Eigenvalues and Eigenvectors

- **Properties of Eigenvalues and Eigenvectors:**
    - The sum of eigenvalues equals the trace of the matrix.
    - The product of eigenvalues equals the determinant of the matrix.
    - Eigenvectors corresponding to distinct eigenvalues are linearly independent.

### 8.5 Positive Definite Matrices

- **Positive definite Matrices:** A symmetric matrix $A$ is positive definite if $x^T A x > 0$ for all non-zero vectors $x$. All eigenvalues of a positive definite matrix are positive.

### 8.6 Matrix Decomposition

- **Matrix Decomposition:** Matrix decomposition (or factorization) involves expressing a matrix as a product of simpler matrices (e.g., LU decomposition, QR decomposition, Cholesky decomposition, SVD).

- **CSE Example:** Eigenvalues are used in **PageRank algorithms** (Google Search) to determine the importance of web pages and in **Principal Component Analysis (PCA)** for image compression and noise reduction.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Matrices | Equality, Addition, Subtraction, Multiplication, Equivalence, Positive/Negative Matrices, Adjoint, Transpose, Inverse, Rank, Normal Form |
| 2 | System of Linear Equations | Homogeneous System, Non-Homogeneous System, Eigenvalues, Eigenvectors, Matrix Differential Equations |
| 3 | Vector Spaces and Subspaces | Vector Space, Subspace, Sum, Direct Sum, Hilbert Space, Normed Linear Space, Banach Space |
| 4 | Linear Combinations, Basis and Dimension | Linear Combination, Span, Linear Independence, Basis, Dimension, Rank |
| 5 | Linear Transformations | Linear Mapping, Kernel, Image, Nullity, Rank-Nullity Theorem, Singular/Non-Singular, Isomorphism |
| 6 | Matrices and Linear Operations | Matrix Representation, Change of Basis, Similarity, Norms, Inner Products, Orthogonal Complements, Orthonormal Sets, Gram-Schmidt Process |
| 7 | Inner Product Spaces | Inner Product, Norm, Distance, Orthogonality, Orthonormal Sets, Gram-Schmidt |
| 8 | Eigenvalues, Eigenvectors and Diagonalization | Eigenvalue, Eigenvector, Characteristic Equation, Diagonalization, Positive Definite Matrices, Matrix Decomposition, PageRank, PCA |

---
*MATH 2241 — Linear Algebra | Dept. of CSE, University of Rajshahi*





