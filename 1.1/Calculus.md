

# Differential and Integral Calculus

### Course Information
**Course:** MATH 1121 (Differential and Integral Calculus)
**Course Type:** Theory, 3 Credit
**Prerequisite:** None

### Instructor
Dr. Md. Masum Murshed, Associate Professor, Dept. of Mathematics, University of Rajshahi 

---
### Course Motivation
> Familiarize students with introductory calculus.

## Course Contents

|Area|Topics Covered|
|---|---|
|**Functions**|Domain, range, inverse function, composition of functions, limits, continuity and differentiability|
|**Ordinary Differentiation**|Successive differentiation, Leibnitz theorem, Rolle's theorem, Lagrange's and Cauchy's mean value theorem, Taylor's and Maclaurin's formulae, tangents and normals|
|**Application of Derivative**|Maximum and minimum values, second derivative test, tangents and normals|
|**Indefinite Integrals**|Substitution, integration by parts|
|**Definite Integrals**|Reduction formulas, definite integral as limit of a sum|
|**Application of the Definite Integral**|Area between curves, arc length|
|**Special Functions**|Beta and Gamma functions, recurrence relation, Gamma-Beta relationship|


## Textbooks
**Primary Texts:**
1. Gilbert Strang — *Calculus*, Wellesley-Cambridge Press
2. B. C. Das and B. N. Mukherjee — *Differential Calculus*, U. N. Dhur & Sons
3. B. C. Das and B. N. Mukherjee — *Integral Calculus*, U. N. Dhur & Sons

## Table of Contents
1. [Module I – Functions, Limits, and Continuity](#module-i)
2. [Module II – Ordinary Differentiation](#module-ii)
3. [Module III – Expansions of Functions](#module-iii)
4. [Module IV – Applications of the Derivative](#module-iv)
5. [Module V – Indefinite and Definite Integrals](#module-v)
6. [Module VI – Special Functions](#module-vi)

---

## Module I
## Functions, Limits, and Continuity

### 1.1 Functions and Graphs

#### Definition
A **function** $f: X \to Y$ is a rule such that for **each** $x \in X$, there exists a **unique** $y \in Y$ where $y = f(x)$.

#### Domain, Co-domain, and Range

| Term | Definition |
|---|---|
| **Domain** | The set $X$ of **all possible inputs** |
| **Co-domain** | The set $Y$ containing **all potential outputs** |
| **Range** | The **actual** set of outputs: $\{f(x) : x \in X\}$ |

> 📌 **Note:** Range ⊆ Co-domain. They are equal only when the function is **onto (surjective)**.


#### Classification of Functions

| Type | Definition | Condition |
|---|---|---|
| **One-one (Injective)** | Every input maps to a **unique** output | $f(x_1) = f(x_2) \Rightarrow x_1 = x_2$ |
| **Onto (Surjective)** | Every element in the **co-domain** is mapped to by at least one input | Range = Co-domain |
| **Bijective** | Both one-one AND onto | Necessary for inverse to exist |

#### Inverse Functions
$g$ is the **inverse** of $f$ if:
$$g \circ f = \text{Identity on } X \quad \text{and} \quad f \circ g = \text{Identity on } Y$$

> 💡 **CSE Connection:** A **Primary Key** in a database is a real-world example of a **one-one (injective) function** — every unique ID (domain) maps to exactly one specific record (range). No two records share the same primary key.


#### Transcendental Functions
Functions that are **not algebraic** — cannot be expressed as a finite polynomial. Includes:
- **Trigonometric:** $\sin x,\ \cos x,\ \tan x, \ldots$
- **Exponential:** $e^x,\ a^x$
- **Logarithmic:** $\ln x,\ \log_a x$


### 1.2 Limit of a Function

#### Formal ($\varepsilon$-$\delta$) Definition
$$\lim_{x \to a} f(x) = L$$

if for every $\varepsilon > 0$, there exists a $\delta > 0$ such that:
$$|f(x) - L| < \varepsilon \quad \text{whenever} \quad 0 < |x - a| < \delta$$

> 📌 This means: we can make $f(x)$ **as close to $L$ as we want**, just by making $x$ close enough to $a$ — without actually reaching $a$.


#### One-Sided Limits

| Limit Type | Notation | Description |
|---|---|---|
| **Right-Hand Limit (RHL)** | $\lim_{x \to a^+} f(x)$ | $x$ approaches $a$ from **above** $(a < x < a + \delta)$ |
| **Left-Hand Limit (LHL)** | $\lim_{x \to a^-} f(x)$ | $x$ approaches $a$ from **below** $(a - \delta < x < a)$ |

#### Existence of a Limit

$$\lim_{x \to a} f(x) \text{ exists} \iff \text{LHL} = \text{RHL} = L$$

If $\text{LHL} \neq \text{RHL}$, the limit **does not exist** at that point.

---

### 1.3 Continuity and Discontinuity

#### Three Conditions for Continuity at $x = a$

A function $f(x)$ is **continuous at $x = a$** if and only if **all three** hold:

1. $f(a)$ is **defined**
2. $\lim_{x \to a} f(x)$ **exists**
3. $\lim_{x \to a} f(x) = f(a)$

> 💡 Breaking **any** one of these three conditions creates a discontinuity.


#### Types of Discontinuity

| Type | Condition | Description |
|---|---|---|
| **Discontinuity of the First Kind** | LHL and RHL exist but $\neq f(a)$ | Limit exists but doesn't match function value |
| **Jump Discontinuity** | $\text{LHL} \neq \text{RHL}$ | Left and right limits exist but differ |
| **Discontinuity of the Second Kind** | At least one of LHL or RHL **does not exist** | e.g., the Dirichlet function |

#### Uniform Continuity

A function is **uniformly continuous** on an interval if:
- The same $\delta$ works for **all points** in the interval for a given $\varepsilon$
- (Unlike ordinary continuity, where $\delta$ may depend on the specific point $a$)

---

## Module II
## Ordinary Differentiation

### 2.1 Successive Differentiation

**Successive differentiation** means finding **higher-order derivatives** of a function repeatedly.

For a function $y = f(x)$:

$$y' = \frac{dy}{dx}, \quad y'' = \frac{d^2y}{dx^2}, \quad \ldots, \quad y_n = \frac{d^ny}{dx^n}$$

**Common results used:**

| Function | $n$-th Derivative |
|---|---|
| $y = x^n$ | $y_n = n!$ (constant) |
| $y = \sin(ax)$ | $y_n = a^n \sin\!\left(ax + \frac{n\pi}{2}\right)$ |
| $y = e^{ax}$ | $y_n = a^n e^{ax}$ |

---

### 2.2 Leibnitz's Theorem

Used to find the **$n$-th derivative of a product** of two functions $u$ and $v$:

$$(uv)_n = \sum_{k=0}^{n} \binom{n}{k} u_k \cdot v_{n-k}$$

where $u_k$ denotes the $k$-th derivative of $u$, and $v_{n-k}$ the $(n-k)$-th derivative of $v$.

> 💡 **CSE Connection:** **Algorithm Complexity.** Successive differentiation underlies **Taylor series approximations**, which are used to analyse the **convergence rates** of numerical algorithms and iterative methods.

---

## Module III
## Expansions of Functions

### 3.1 Mean Value Theorems

These theorems guarantee the **existence** of special points on differentiable curves.

---

#### Rolle's Theorem

**Conditions:**
1. $f(x)$ is **continuous** on $[a, b]$
2. $f(x)$ is **differentiable** on $(a, b)$
3. $f(a) = f(b)$

**Conclusion:**
$$\exists\ c \in (a, b) \text{ such that } f'(c) = 0$$

> 📌 Geometrically: if a smooth curve starts and ends at the same height, there must be at least one **horizontal tangent** in between.

---

#### Lagrange's Mean Value Theorem (First MVT)

**Conditions:** $f$ continuous on $[a,b]$, differentiable on $(a,b)$.

**Conclusion:**
$$\exists\ c \in (a, b) \text{ such that } f'(c) = \frac{f(b) - f(a)}{b - a}$$

> 📌 Geometrically: there is at least one point where the **tangent slope** equals the **average slope** (secant) over the interval.

---

#### Cauchy's Mean Value Theorem (Generalized MVT)

A generalization involving **two functions** $f$ and $g$:

$$\exists\ c \in (a, b) \text{ such that } \frac{f'(c)}{g'(c)} = \frac{f(b) - f(a)}{g(b) - g(a)}$$

Reduces to Lagrange's MVT when $g(x) = x$.

---

### 3.2 Series Expansions

#### Taylor's Theorem

Expands a function $f(x + h)$ in **powers of $h$**:

$$f(x+h) = f(x) + hf'(x) + \frac{h^2}{2!}f''(x) + \cdots + \frac{h^n}{n!}f^{(n)}(x) + R_n$$

where $R_n$ is the **remainder term** (error of truncation).

---

#### Maclaurin's Series

A **special case** of Taylor's theorem centered at $x = 0$ (i.e., $x = 0$, expand in powers of $x$):

$$f(x) = f(0) + xf'(0) + \frac{x^2}{2!}f''(0) + \frac{x^3}{3!}f'''(0) + \cdots$$

**Common Maclaurin Expansions:**

| Function | Series |
|---|---|
| $e^x$ | $1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$ |
| $\sin x$ | $x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots$ |
| $\cos x$ | $1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots$ |
| $\ln(1+x)$ | $x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots$ |

**Remainder Forms:** The finite Maclaurin/Taylor series includes a **remainder term** to account for truncation error. The **Lagrange form** of the remainder is:
$$R_n = \frac{f^{(n+1)}(c)}{(n+1)!} x^{n+1} \quad \text{for some } c \in (0, x)$$

> 💡 **CSE Connection:** **Floating-Point Arithmetic.** Computers cannot compute $\sin(x)$ or $e^x$ directly — they use **Taylor series truncated to a finite number of terms**, working within specific **precision limits** (e.g., IEEE 754 double precision).

---

## Module IV
## Applications of the Derivative

### 4.1 Maxima and Minima

#### Definitions

- **Local Maximum at $c$:** $f(x) < f(c)$ for all $x$ in a neighbourhood of $c$
- **Local Minimum at $c$:** $f(x) > f(c)$ for all $x$ in a neighbourhood of $c$

#### Necessary Condition (Critical Points)

$$f'(c) = 0$$

> ⚠️ This is a **necessary** but **not sufficient** condition. $f'(c) = 0$ gives **critical points** — which may be maxima, minima, or **saddle/inflection points**.

#### Second Derivative Test (Sufficient Condition)

| Condition | Conclusion |
|---|---|
| $f'(c) = 0$ and $f''(c) < 0$ | **Local Maximum** |
| $f'(c) = 0$ and $f''(c) > 0$ | **Local Minimum** |
| $f'(c) = 0$ and $f''(c) = 0$ | **Inconclusive** — use higher derivatives |

> 💡 **CSE Connection:** **Optimization in Machine Learning.** The **Gradient Descent** algorithm uses derivatives to find the **minimum of a loss function** — iteratively moving in the direction of steepest descent ($-\nabla f$) to improve model accuracy.

---

### 4.2 Tangents and Normals

For a curve $y = f(x)$ at a point $(x_0, y_0)$:

| Line | Slope | Equation |
|---|---|---|
| **Tangent** | $m = f'(x_0)$ | $y - y_0 = f'(x_0)(x - x_0)$ |
| **Normal** | $m = -\frac{1}{f'(x_0)}$ | $y - y_0 = -\frac{1}{f'(x_0)}(x - x_0)$ |

> 📌 The normal is **perpendicular** to the tangent at the point of contact.

---

## Module V
## Indefinite and Definite Integrals

### 5.1 Indefinite Integration Techniques

**Two major techniques for complex integrals:**

| Technique | When to Use | Example Form |
|---|---|---|
| **Substitution** | Function contains a composite expression | $\int \frac{dx}{\sqrt{ax^2 + bx + c}}$ |
| **Integration by Parts** | Product of two functions | $\int e^{ax} \cos bx\ dx$ |

**Integration by Parts formula:**
$$\int u\ dv = uv - \int v\ du$$

> 📌 **ILATE Rule** for choosing $u$: **I**nverse trig → **L**ogarithmic → **A**lgebraic → **T**rigonometric → **E**xponential

---

### 5.2 Definite Integrals

#### Reduction Formulas

Systematic formulas to evaluate **integrals of powers** — reduce the power by 2 at each step.

| Integral | Reduction Formula |
|---|---|
| $\int_0^{\pi/2} \sin^n x\ dx$ | $\frac{n-1}{n} \int_0^{\pi/2} \sin^{n-2} x\ dx$ |
| $\int_0^{\pi/2} \sin^m x \cos^n x\ dx$ | Reduction using both indices $m$ and $n$ |

---

#### Definite Integral as a Limit of a Sum

$$\int_a^b f(x)\ dx = \lim_{n \to \infty} \frac{b-a}{n} \sum_{k=0}^{n-1} f\!\left(a + k \cdot \frac{b-a}{n}\right)$$

The interval $[a, b]$ is partitioned into $n$ equal parts; the sum of rectangular areas approaches the exact area as $n \to \infty$.

---

### 5.3 Geometric Applications

#### Area Between Curves

$$A = \int_a^b \left[ f(x) - g(x) \right] dx \quad \text{where } f(x) \geq g(x) \text{ on } [a, b]$$

**Example:** Area between the circle $x^2 + y^2 = 1$ and parabola $y^2 = 1 - x$.

---

#### Arc Length

The **length of a curve** $y = f(x)$ from $x = a$ to $x = b$:

$$L = \int_a^b \sqrt{1 + \left[\frac{dy}{dx}\right]^2}\ dx$$

**Applications include:**
- Perimeter of a circle
- Length of an intercepted arc of a parabola

---

## Module VI
## Special Functions

### 6.1 Beta and Gamma Functions

These are **improper integrals** that generalize the factorial and appear throughout advanced mathematics and physics.

---

#### Gamma Function — $\Gamma(n)$

$$\Gamma(n) = \int_0^{\infty} x^{n-1} e^{-x}\ dx \quad (n > 0)$$

**Key Properties:**

| Property | Statement |
|---|---|
| **Recurrence Relation** | $\Gamma(n+1) = n\,\Gamma(n)$ |
| **Factorial Connection** | $\Gamma(n+1) = n!$ for positive integers |
| **Special Value** | $\Gamma\!\left(\tfrac{1}{2}\right) = \sqrt{\pi}$ |

---

#### Beta Function — $\beta(m, n)$

$$\beta(m, n) = \int_0^{1} x^{m-1}(1-x)^{n-1}\ dx \quad (m, n > 0)$$

**Key Properties:**

| Property | Statement |
|---|---|
| **Symmetry** | $\beta(m, n) = \beta(n, m)$ |
| **Relation to Gamma** | $\beta(m, n) = \dfrac{\Gamma(m)\,\Gamma(n)}{\Gamma(m+n)}$ |

> 📌 The **Gamma–Beta relationship** is one of the most powerful tools for evaluating complex definite integrals — it converts them into standard Gamma function forms.

---

## Quick Reference Summary

| Module | Core Topic | Key Results / Tools |
|---|---|---|
| I | Functions, Limits, Continuity | $\varepsilon$-$\delta$ definition, LHL = RHL, 3 conditions for continuity |
| II | Differentiation | Successive derivatives, Leibnitz's Theorem |
| III | Expansions | Rolle's, Lagrange's, Cauchy's MVT; Taylor & Maclaurin Series |
| IV | Applications | Maxima/Minima, Second Derivative Test, Tangent & Normal |
| V | Integration | Substitution, Parts, Reduction Formulas, Area, Arc Length |
| VI | Special Functions | $\Gamma(n+1)=n\Gamma(n)$, $\Gamma(\frac{1}{2})=\sqrt{\pi}$, $\beta(m,n)=\frac{\Gamma(m)\Gamma(n)}{\Gamma(m+n)}$ |

---
*MATH 1121 | Differential and Integral Calculus  | Dept. of CSE, University of Rajshahi* 







