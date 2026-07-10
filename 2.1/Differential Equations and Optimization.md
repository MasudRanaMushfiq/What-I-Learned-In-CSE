

# Differential Equations and Optimization

### Course Information
**Course:** MATH 2131 (Differential Equations and Optimization)
**Course Type:** Theory, 3 Credit
**Prerequisite:** MATH 1121 Differential and Integral, MATH1221 Co-ordinate Geometry, Vector analysis and Complex Variable
### Instructor
Dr. Mahammed Harunor Rashid, Professor, Dept. of Mathematics, University of Rajshahi

### Course Motivation
> To understand the formation, solution and applications of differential equations.

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Differential Equations** | Solutions of first order and first degree and first-order and higher degree equations with variable coefficients, Solution of Higher-Order linear differential equations, Series solution of linear differential equation, Series solution of second order equation with variable coefficients, Solutions of partial differential equation, Laplace's equation and transformation, Poisson's equation, Helmholtz's equation, Diffusion equation, Green's function solution, Integral equation. |
| **Basics of Multivariable Calculus** | Multivariable functions, Limit and continuity, Partial Derivatives, Total Derivative, Vector Functions, Gradient, Physical interpretation of Gradient, Existence of Minimum and a Maximum, Continuity of Functions, Taylor's Theorem, Convex Functions. |
| **Optimization Problem Formulation** | Statement of an Optimization problem, Historical development, Classification of Optimization problems and techniques, Single variable optimization problem, Iterative algorithmic approach. |
| **Unconstrained Optimization** | Necessary and Sufficient conditions for optimality, Convexity, Steepest Descent Method. |
| **Constrained Optimization** | Necessary conditions for optimality, sufficient conditions for optimality, sensitivity of solution, Sequential Quadratic Programming. |

## Textbooks

**Primary Texts:**
1. W. G. Kelley, A. C. Peterson — *Differential Equations, An Introduction with Applications*, Harcourt Academic Press.
2. A. D. Belegundu, T. R. Chandrupatla — *Optimization Concepts and Applications in Engineering*, Cambridge University Press.

---

## Table of Contents

1. [Chapter 1 – Linear Algebra & Matrix Theory](#chapter-1)
2. [Chapter 2 – Differential Equations (DE)](#chapter-2)
3. [Chapter 3 – Basics of Multivariable Calculus](#chapter-3)
4. [Chapter 4 – Optimization Theory](#chapter-4)
5. [Chapter 5 – Optimization Problem Formulation](#chapter-5)
6. [Chapter 6 – Unconstrained Optimization](#chapter-6)
7. [Chapter 7 – Constrained Optimization](#chapter-7)
8. [Chapter 8 – Course Applications (CSE Examples)](#chapter-8)

---

## Chapter 1
## Linear Algebra & Matrix Theory

Matrices form the mathematical foundation for solving systems of differential equations and multivariate optimization problems.

### 1.1 Fundamental Matrix Concepts

- **Matrix Definition:** A rectangular array of $mn$ numbers arranged in $m$ rows and $n$ columns.
- **Key Matrix Types:**
    - **Square Matrix:** Rows equal columns ($m=n$).
    - **Identity Matrix ($I_n$):** A square matrix with ones on the main diagonal and zeros elsewhere.
    - **Diagonal Matrix:** All elements outside the main diagonal are zero.
    - **Trace:** The sum of the diagonal elements of a square matrix.
- **Inverse of a Matrix:** A matrix $B$ such that $AB = BA = I$. $A$ is invertible if its determinant $|A| \neq 0$ (non-singular).
- **System of Linear Equations:** Represented as $AX = B$. A system is **consistent** if it has at least one solution, which occurs when the rank of the coefficient matrix $A$ equals the rank of the augmented matrix $[A, B]$.
- **Eigenvalues & Eigenvectors:** Scalar $\lambda$ and non-zero vector $x$ such that $Ax = \lambda x$. These are found using the **Characteristic Equation** $|A - \lambda I| = 0$.
    - **Cayley-Hamilton Theorem:** Every square matrix satisfies its own characteristic equation.

---

## Chapter 2
## Differential Equations (DE)

Differential equations describe systems where the rate of change of a variable depends on the variable itself.

### 2.1 Fundamental Definitions

- **Ordinary Differential Equation (ODE):** Involves derivatives with respect to a single independent variable.
- **Order:** The highest derivative present in the equation.
- **Degree:** The power of the highest-order derivative (after clearing fractions/radicals).
- **Types of Solutions:**
    - **General Solution (GS):** Contains arbitrary constants equal to the order of the DE.
    - **Particular Solution (PS):** Obtained by assigning specific values to the constants.
    - **Singular Solution (SS):** A solution that cannot be derived from the general solution.

### 2.2 First-Order Differential Equations

**Solutions of first order and first degree and first-order and higher degree equations with variable coefficients:**

- **Separable Equations:** Variables can be separated into the form $F(x)dx + G(y)dy = 0$. Solve by integrating both sides.
- **Homogeneous Equations:** A DE where the function is of the same degree in $x$ and $y$. Solve using the substitution $y = vx$.
- **Exact Differential Equations:** A DE $M(x,y)dx + N(x,y)dy = 0$ is exact if $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$.
    - **Integrating Factor (I.F.):** If an equation is not exact, it can be made exact by multiplying by an I.F..
- **Linear & Bernoulli Equations:**
    - **Linear:** $\frac{dy}{dx} + Py = Q$ (where $P, Q$ are functions of $x$). $I.F. = e^{\int P dx}$.
    - **Bernoulli:** $\frac{dy}{dx} + Py = Qy^n$. Solve by substituting $v = y^{1-n}$ to reduce it to a linear form.

### 2.3 Higher-Order Linear DEs with Constant Coefficients

**Solution of Higher-Order linear differential equations:**

These take the form $F(D)y = f(x)$, where $D = \frac{d}{dx}$.
- **Complementary Function (C.F.):** The solution to the homogeneous part $F(D)y = 0$. It depends on the roots of the **Auxiliary Equation (A.E.)**:
    - **Distinct Real Roots:** $y_c = c_1e^{m_1x} + c_2e^{m_2x}$.
    - **Repeated Roots:** $y_c = (c_1 + c_2x)e^{mx}$.
    - **Imaginary Roots ($\alpha \pm i\beta$):** $y_c = e^{\alpha x}(c_1 \cos\beta x + c_2 \sin\beta x)$.
- **Particular Integral (P.I.):** The solution to the non-homogeneous part $f(x)$.
    - **Operator Method:** Uses specific rules for $f(x) = e^{ax}$, $\sin(ax)$, or polynomials.
    - **Method of Undetermined Coefficients:** Assumes a trial solution based on the form of $f(x)$ (e.g., if $f(x) = e^x$, try $y_p = Ae^x$).
    - **Variation of Parameters:** A general method to find $y_p = u(x)y_1 + v(x)y_2$ when the C.F. is known.

### 2.4 Series Solutions and Partial Differential Equations

**Series solution of linear differential equation, Series solution of second order equation with variable coefficients:**

- Series solutions are used to solve linear differential equations with variable coefficients when standard methods fail, typically assuming a solution of the form $y = \sum_{n=0}^{\infty} a_n x^n$.

**Solutions of partial differential equation, Laplace's equation and transformation, Poisson's equation, Helmholtz's equation, Diffusion equation, Green's function solution, Integral equation:**

- **Partial Differential Equation (PDE):** An equation involving partial derivatives of a function of two or more independent variables.
- **Laplace's equation:** $\nabla^2 u = 0$ (elliptic, describes steady-state phenomena).
- **Laplace's transformation:** An integral transform used to convert PDEs into ordinary differential equations.
- **Poisson's equation:** $\nabla^2 u = f$ (elliptic, describes potential with a source term).
- **Helmholtz's equation:** $\nabla^2 u + k^2 u = 0$ (arises in wave propagation problems).
- **Diffusion equation (Heat equation):** $\frac{\partial u}{\partial t} = \alpha \nabla^2 u$ (parabolic, describes heat flow or diffusion).
- **Green's function solution:** A method for solving inhomogeneous PDEs by constructing a Green's function that represents the response to a point source.
- **Integral equation:** An equation in which an unknown function appears under an integral sign.

---

## Chapter 3
## Basics of Multivariable Calculus

### 3.1 Fundamental Concepts

**Basic of Multivariable Calculus:**
- **Multivariable functions:** Functions of two or more independent variables (e.g., $f(x,y)$).
- **Limit and continuity:** The concept of a function approaching a value as the input approaches a point; continuity requires the limit equals the function value.
- **Partial Derivatives:** Derivatives with respect to one variable while holding others constant.
- **Total Derivative:** The derivative of a function with respect to an independent variable, accounting for indirect dependencies through intermediate variables.
- **Vector Functions:** Functions that output vectors, typically $f: \mathbb{R}^n \to \mathbb{R}^m$.
- **Gradient:** $\nabla f = \left( \frac{\partial f}{\partial x_1}, \ldots, \frac{\partial f}{\partial x_n} \right)$ (a vector pointing in the direction of the greatest rate of increase).
- **Physical interpretation of Gradient:** The gradient points in the direction of steepest ascent of a function, and its magnitude is the rate of change in that direction.
- **Existence of Minimum and a Maximum:** Continuous functions on closed and bounded sets attain both a minimum and a maximum (Extreme Value Theorem).
- **Continuity of Functions:** A function is continuous if small changes in input produce small changes in output.
- **Taylor's Theorem:** Expresses a function as an infinite sum of terms calculated from its derivatives at a single point; used for approximation.
- **Convex Functions:** A function where the line segment between any two points on the graph lies above or on the graph ($f(tx + (1-t)y) \leq tf(x) + (1-t)f(y)$).

---

## Chapter 4
## Optimization Theory

Optimization involves finding the "best" solution (maximum or minimum) from a set of feasible options.

### 4.1 Basic Concepts

- **Objective Function ($f(x)$):** The real-valued function to be minimized or maximized.
- **Decision Variables:** The independent variables $x = [x_1, x_2, ..., x_n]^T$.
- **Constraints:** Restrictions on variables (Equality $h(x)=0$ or Inequality $g(x) \leq 0$).
    - **Feasible Region ($\Omega$):** The set of all points satisfying the constraints.
- **Minimizers:**
    - **Local Minimizer:** Smallest value in a local neighborhood.
    - **Global Minimizer:** Smallest value over the entire feasible region.

### 4.2 Optimality Conditions

- **First-Order Necessary Condition (FONC):** If $x^*$ is a local minimizer, then for any feasible direction $d$, $d^T \nabla f(x^*) \geq 0$. For interior points (unconstrained), $\nabla f(x^*) = 0$.
- **Second-Order Necessary Condition (SONC):** If $x^*$ is a local minimizer, the Hessian matrix $F(x^*)$ must be positive semi-definite.
- **Lagrange Conditions:** Used for equality constraints. $L(x, \lambda) = f(x) + \lambda^T h(x)$. At a minimizer, $\nabla_x L = 0$ and $\nabla_\lambda L = 0$.
- **KKT Conditions:** Generalization of Lagrange for inequality constraints.

### 4.3 Search Algorithms

- **Unconstrained Algorithms:**
    - **Line Search:** One-dimensional search to find step size $\alpha$.
        - **Golden Section Method:** Iteratively reduces the uncertainty interval of a unimodal function by a factor of $\approx 0.618$.
    - **Steepest Descent:** Moves in the direction of the negative gradient $-\nabla f(x_k)$.
    - **Newton's Method:** Uses the Hessian to find the direction $d = -[F(x_k)]^{-1} \nabla f(x_k)$. It has fast quadratic convergence but is computationally expensive.
- **Constrained Algorithms:**
    - **Penalty Function Methods:** Convert constrained problems into unconstrained ones by adding a penalty term for constraint violations.
    - **Feasible Direction Methods:** Move from one feasible point to another while decreasing the objective function.

---

## Chapter 5
## Optimization Problem Formulation

**Optimization Problem Formulation:**

- **Statement of an Optimization problem:** The process of defining the objective function, decision variables, and constraints that mathematically describe the problem.
- **Historical development:** The evolution of optimization from calculus (Fermat, Newton) to linear programming (Dantzig, 1947) and modern computational methods.
- **Classification of Optimization problems and techniques:**
    - By presence of constraints: Unconstrained vs. Constrained.
    - By nature of variables: Continuous, Integer, or Mixed-integer.
    - By form of functions: Linear, Nonlinear, Quadratic, Convex.
    - By determinism: Deterministic vs. Stochastic.
- **Single variable optimization problem:** A problem with only one decision variable $x$; optimality condition is $f'(x)=0$.
- **Iterative algorithmic approach:** Optimization algorithms generate a sequence of points $\{x_k\}$ converging to an optimal solution, using a direction $d_k$ and step size $\alpha_k$: $x_{k+1} = x_k + \alpha_k d_k$.

---

## Chapter 6
## Unconstrained Optimization

**Unconstrained Optimization:**

- **Necessary and Sufficient conditions for optimality:**
    - **Necessary:** $\nabla f(x^*) = 0$ (FONC) and $\nabla^2 f(x^*)$ is positive semi-definite (SONC).
    - **Sufficient:** $\nabla f(x^*) = 0$ and $\nabla^2 f(x^*)$ is positive definite (then $x^*$ is a strict local minimizer).
- **Convexity:** If $f$ is convex and $\nabla f(x^*) = 0$, then $x^*$ is a global minimizer.
- **Steepest Descent Method:** An iterative algorithm using $d_k = -\nabla f(x_k)$ as the search direction; converges linearly but can be slow near the optimum due to zigzagging.

---

## Chapter 7
## Constrained Optimization

**Constrained Optimization:**

- **Necessary conditions for optimality:** For a point $x^*$ to be a local minimizer subject to $h(x)=0$ and $g(x) \leq 0$, there must exist Lagrange multipliers $\lambda$ and $\mu \geq 0$ such that $\nabla f(x^*) + \sum \lambda_i \nabla h_i(x^*) + \sum \mu_j \nabla g_j(x^*) = 0$ and $\mu_j g_j(x^*) = 0$ (complementary slackness). These are the KKT conditions.
- **Sufficient conditions for optimality:** If KKT conditions hold and appropriate second-order conditions (positive definiteness of the Hessian of the Lagrangian in the tangent space of active constraints) are satisfied, then $x^*$ is a strict local minimizer.
- **Sensitivity of solution:** Analysis of how the optimal objective value changes with respect to changes in constraint right-hand sides (given by the Lagrange multipliers $\lambda$).
- **Sequential Quadratic Programming (SQP):** An iterative method for constrained optimization that solves a sequence of Quadratic Programming (QP) subproblems, each approximating the original problem with a quadratic objective and linearized constraints.

---

## Chapter 8
## Course Applications (CSE Examples)

Optimization is an indispensable tool in Computer Science and Engineering:

- **Machine Learning:** Training neural networks involves minimizing a "loss function" using **Gradient Descent**.
- **Big Data Analysis:** Processing large-scale data requires **Sparse Optimization** to identify key features efficiently.
- **Network Flow:** Optimizing water, electricity, or data packet delivery across pipelines/networks.
- **Image Processing:** Used in speech and image detection to improve accuracy and reduce noise.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Linear Algebra & Matrix Theory | Identity Matrix, Determinant, Eigenvalues, Characteristic Equation, Cayley-Hamilton Theorem |
| 2 | Differential Equations (DE) | ODE, Order/Degree, GS/PS/SS, Separable, Exact, Linear, Bernoulli, C.F./P.I., Laplace/Poisson/Helmholtz/Diffusion Equations |
| 3 | Basics of Multivariable Calculus | Partial Derivatives, Gradient ($\nabla f$), Taylor's Theorem, Convex Functions |
| 4 | Optimization Theory | Objective Function, Constraints, Feasible Region, FONC, SONC, Lagrange, KKT |
| 5 | Optimization Problem Formulation | Statement, Classification, Single variable, Iterative approach ($x_{k+1} = x_k + \alpha_k d_k$) |
| 6 | Unconstrained Optimization | $\nabla f(x^*)=0$, Positive definite Hessian, Steepest Descent |
| 7 | Constrained Optimization | KKT Conditions, Lagrange Multipliers ($\lambda$), Complementary Slackness, SQP |
| 8 | Applications | Gradient Descent (ML), Sparse Optimization (Big Data), Network Flow, Image Processing |

---
*MATH 2131 — Differential Equations and Optimization | Dept. of CSE, University of Rajshahi*





