

# Discrete Mathematics

### Course Information
**Course:** CSE 2131 (Discrete Mathematics)
**Course Type:** Theory, 3 Credit
**Prerequisite:** None
### Instructor
Mr. Sanjoy Kumar Chakrabarty, Associate Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To develop basics knowledge on Discrete Mathematics

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Mathematical Logic** | Connectives, normal Forms, theory of inference for proposition calculus, predicate calculus, inference theory of predicate calculus, method of proof, mathematical induction, Semantic rules for statements, Syntax and semantics for first order predicate logic (FOPL), Properties of Wffs, Clausal conversion procedure, unification algorithm, resolution in propositional logic, resolution in predicate logic. |
| **Sets** | Basic concept of set theory, operation of sets, ordered pairs and n-tuples. |
| **Relation and Ordering** | Relations, properties of Binary relation in a set, composition of binary relation, relation matrix and graph of a relation, partial ordering, path in relation and di-graph. |
| **Functions** | definition, composition of function, inverse function, binary and array operation. |
| **Graph** | Introduction to graph, graph terminology, representing graph and graph isomorphism, paths, reachability, connectivity, Euler and Hamilton path, shortest path problems, graph coloring, matrix representation of graph. |
| **Trees** | Introduction of trees, application of trees, tree traversal, labelling trees, trees and sorting, spanning trees, minimal spanning tree, undirected trees. |
| **Algebraic Structure** | Algebraic system, general properties, some simple algebraic system. |

## Textbooks

**Primary Texts:**
1. Kenneth H. Rosen — *Discrete Mathematics and Its Applications*, McGraw-Hill.

---

## Table of Contents

1. [Chapter 1 – Logic and Proofs](#chapter-1)
2. [Chapter 2 – Sets](#chapter-2)
3. [Chapter 3 – Relations and Ordering](#chapter-3)
4. [Chapter 4 – Functions](#chapter-4)
5. [Chapter 5 – Graphs](#chapter-5)
6. [Chapter 6 – Trees and Applications](#chapter-6)
7. [Chapter 7 – Algebraic Structure](#chapter-7)
8. [Chapter 8 – Matrices and Bit Operations](#chapter-8)

---

## Chapter 1
## Logic and Proofs

### 1.1 Propositional Logic

- **Definition:** A proposition is a declarative statement that is either true or false, but not both.
- **Logical Operators (Connectives):**
    - **Negation (¬p):** "It is not the case that p".
    - **Conjunction (p ∧ q):** True only if both p and q are true.
    - **Disjunction (p ∨ q):** True if at least one of p or q is true.
    - **Exclusive OR (p ⊕ q):** True if exactly one of p or q is true.
    - **Conditional (p → q):** "If p, then q." It is false only when p is true and q is false.
    - **Biconditional (p ↔ q):** "p if and only if q." True when p and q have the same truth values.
- **Logical Types:**
    - **Tautology:** A statement that is always true (e.g., $p \lor \neg p$).
    - **Contradiction:** A statement that is always false (e.g., $p \land \neg p$).
    - **Contingency:** A statement that can be true or false depending on the situation.
- **Logical Equivalences:** Statements that always have the same truth values (e.g., De Morgan's Laws: $\neg(p \land q) \equiv \neg p \lor \neg q$).
- **Normal Forms:** Standard ways of representing logical formulas (e.g., Conjunctive Normal Form CNF, Disjunctive Normal Form DNF).
- **Theory of inference for proposition calculus:** Rules for deriving valid conclusions from premises.
- **Properties of Wffs (Well-Formed Formulas):** Syntactically correct formulas in propositional or predicate logic.
- **Resolution in propositional logic:** A rule of inference that proves statements by contradiction using clauses.

### 1.2 Predicates and Quantifiers

- **Predicates:** Statements involving variables that become propositions when values are assigned (e.g., $P(x)$ where $x > 3$).
- **Quantifiers:**
    - **Universal ($\forall$):** "For all" elements in the domain.
    - **Existential ($\exists$):** "There exists" at least one element in the domain.
- **Negating Quantifiers:** $\neg\forall x P(x) \equiv \exists x \neg P(x)$ and $\neg\exists x P(x) \equiv \forall x \neg P(x)$.

### 1.3 Predicate Calculus and Inference

- **Predicate calculus:** An extension of propositional logic that includes predicates, quantifiers, and variables.
- **Inference theory of predicate calculus:** Rules for deriving conclusions in predicate logic (e.g., Universal Instantiation, Existential Generalization).
- **Syntax and semantics for first order predicate logic (FOPL):**
    - **Syntax:** The formal structure of well-formed formulas (constants, variables, functions, predicates, connectives, quantifiers).
    - **Semantics:** The meaning assigned to formulas based on interpretations (domain of discourse, assignments to constants and predicates).
- **Semantic rules for statements:** Rules defining when a statement is true or false in a given interpretation.
- **Clausal conversion procedure:** Transforming a predicate logic formula into a set of clauses (universally quantified disjunctions of literals) for resolution.
- **Unification algorithm:** An algorithm that finds a substitution that makes two logical expressions identical; essential for resolution in predicate logic.
- **Resolution in predicate logic:** The generalization of propositional resolution to predicate logic, using unification to resolve complementary literals.

### 1.4 Rules of Inference and Proofs

- **Modus Ponens:** Given $p$ and $p \to q$, conclude $q$.
- **Modus Tollens:** Given $\neg q$ and $p \to q$, conclude $\neg p$.
- **Proof Methods:**
    - **Direct Proof:** Showing that if $p$ is true, then $q$ must be true.
    - **Proof by Contrapositive:** Proving $p \to q$ by showing $\neg q \to \neg p$.
    - **Proof by Contradiction:** Assuming the negation of the statement and finding a logical impossibility.
- **Method of proof (General):** A systematic approach to establishing the truth of a mathematical statement.
- **Mathematical induction:** A proof technique that shows a statement holds for all natural numbers by proving a base case and an inductive step.

---

## Chapter 2
## Sets

**Sets: Basic concept of set theory, operation of sets, ordered pairs and n-tuples.**

### 2.1 Sets

- **Definition:** An unordered collection of unique objects.
- **Cardinality ($|A|$):** The number of elements in a set.
- **Power Set ($P(A)$):** The set of all subsets of $A$, including the empty set ($\emptyset$) and $A$ itself.

### 2.2 Set Operations

- **Operations:** Union ($\cup$), Intersection ($\cap$), Complement ($A^c$), and Symmetric Difference (elements in one but not both).
- **Basic concept of set theory:** Foundations including subsets, proper subsets, universal set, empty set.
- **Ordered pairs and n-tuples:**
    - **Ordered pair ($(a,b)$):** A collection of two elements where order matters ($(a,b) \neq (b,a)$ unless $a=b$).
    - **n-tuple ($(a_1, a_2, \ldots, a_n)$):** An ordered list of $n$ elements.

---

## Chapter 3
## Relations and Ordering

**Relation and ordering: Relations, properties of Binary relation in a set, composition of binary relation, relation matrix and graph of a relation, partial ordering, path in relation and di-graph.**

### 3.1 Binary Relations

- **Definition (Relations):** A collection of ordered pairs $(a, b)$ where $a \in A$ and $b \in B$. A binary relation from $A$ to $B$ is a subset of $A \times B$.
- **Properties of Binary relation in a set:**
    - **Reflexive:** $\forall a (a, a) \in R$.
    - **Symmetric:** If $(a, b) \in R$, then $(b, a) \in R$.
    - **Antisymmetric:** If $(a, b) \in R$ and $(b, a) \in R$, then $a = b$.
    - **Transitive:** If $(a, b) \in R$ and $(b, c) \in R$, then $(a, c) \in R$.
- **Equivalence Relation:** A relation that is reflexive, symmetric, and transitive.
- **Composition of binary relation:** For relations $R \subseteq A \times B$ and $S \subseteq B \times C$, the composition $S \circ R = \{(a,c) \mid \exists b \in B \text{ such that } (a,b) \in R \text{ and } (b,c) \in S\}$.
- **Relation matrix and graph of a relation:**
    - **Relation matrix (Zero-One matrix):** A matrix $M_R$ where $M_{ij} = 1$ if $(a_i, b_j) \in R$, else $0$.
    - **Graph of a relation (Di-graph):** A directed graph where vertices represent elements and directed edges represent ordered pairs in the relation.
- **Path in relation and di-graph:** A sequence of edges $(a_0, a_1), (a_1, a_2), \ldots, (a_{n-1}, a_n)$ in a directed graph representing the relation.

### 3.2 Partial Orderings and Lattices

- **Partial ordering:** A relation that is reflexive, antisymmetric, and transitive.
- **Poset (Partially Ordered Set):** A set combined with a relation that is reflexive, antisymmetric, and transitive. (Partial ordering).
- **Lattice:** A poset in which every pair of elements has a unique **least upper bound (LUB)** and a unique **greatest lower bound (GLB)**.

---

## Chapter 4
## Functions

**Functions: definition, composition of function, inverse function, binary and array operation.**

### 4.1 Functions

- **Definition:** A mapping that assigns each element from a domain to exactly one unique element in a codomain.
- **Types of Functions:**
    - **Injective (One-to-One):** Every element in the codomain has at most one pre-image.
    - **Surjective (Onto):** Every element in the codomain is an image of at least one pre-image.
    - **Bijective:** Both injective and surjective (a one-to-one correspondence).
- **Composition of function:** For functions $f: A \to B$ and $g: B \to C$, the composition $(g \circ f)(x) = g(f(x))$.
- **Inverse function:** A function $f^{-1}: B \to A$ exists if $f$ is bijective, defined by $f^{-1}(y) = x$ iff $f(x) = y$.
- **Binary and array operation:**
    - **Binary operation:** An operation that takes two inputs from a set and produces an output in the same set (e.g., addition, multiplication).
    - **Array operation:** Operations applied to arrays (e.g., matrix addition, element-wise multiplication).

---

## Chapter 5
## Graphs

**Graph: Introduction to graph, graph terminology, representing graph and graph isomorphism, paths, reachability, connectivity, Euler and Hamilton path, shortest path problems, graph coloring, matrix representation of graph.**

### 5.1 Graph Fundamentals

- **Introduction to graph:** A graph consists of a set of vertices (nodes) and edges connecting them.
- **Graph terminology (Components):** Vertices (nodes) and Edges (connections).
- **Handshaking Theorem:** The sum of the degrees of all vertices is equal to twice the number of edges.
- **Types:**
    - **Simple Graph:** Undirected edges, no multiple edges, no loops.
    - **Multigraph:** May have multiple edges between the same vertices.
    - **Pseudograph:** May include both loops and multiple edges.
    - **Bipartite Graph:** Vertices can be divided into two disjoint sets such that every edge connects a vertex in one set to a vertex in the other.
- **Representing graph and graph isomorphism:**
    - **Representing graph:** Using adjacency lists, adjacency matrices, or incidence matrices. (Matrix representation of graph).
    - **Graph isomorphism:** Two graphs $G$ and $H$ are isomorphic if there is a bijection between their vertex sets that preserves adjacency.

### 5.2 Connectivity and Circuits

- **Paths, reachability, connectivity:**
    - **Path:** A sequence of vertices connected by edges.
    - **Reachability:** Vertex $v$ is reachable from $u$ if there exists a path from $u$ to $v$.
    - **Connectivity:** A graph is connected if there is a path between every pair of vertices.
- **Euler and Hamilton path:**
    - **Euler Circuit (Euler path):** A simple circuit that traverses every **edge** in a graph exactly once. An Euler path exists if exactly 0 or 2 vertices have odd degree.
    - **Hamiltonian Circuit (Hamilton path):** A circuit that passes through every **vertex** exactly once (except starting and ending).
- **Shortest path problems:** Finding the path between vertices that minimizes the sum of edge weights (or number of edges).
    - **Dijkstra's Algorithm:** Finds the shortest path from a source node to all other nodes in a weighted graph with non-negative edges.
        - *Application:* Google Maps and routing in telephone networks.
    - **Floyd's Algorithm (Floyd-Warshall):** A dynamic programming approach to find the shortest paths between all pairs of vertices.
- **Graph coloring:** An assignment of colors to vertices such that no two adjacent vertices share the same color; the minimum number of colors needed is the chromatic number.

---

## Chapter 6
## Trees and Applications

**Trees: Introduction of trees, application of trees, tree traversal, labelling trees, trees and sorting, spanning trees, minimal spanning tree, undirected trees.**

### 6.1 Definitions

- **Introduction of trees:** A **Tree** is a connected undirected graph with no simple circuits.
- **Undirected trees:** A tree is a connected acyclic undirected graph.
- **Rooted Tree:** A tree where one vertex is designated as the root, creating parent-child hierarchies.
- **m-ary Tree:** A rooted tree where every internal vertex has no more than $m$ children. A **full m-ary tree** has exactly $m$ children for every internal node.

### 6.2 Tree Traversal and Sorting

- **Tree traversal:** Visiting every node in a tree exactly once (Preorder, Inorder, Postorder, Level-order).
- **Labelling trees:** Assigning labels or weights to tree nodes or edges (e.g., for Huffman coding or search trees).
- **Trees and sorting:** Using tree structures (e.g., binary search trees, heap sort) to sort data efficiently.

### 6.3 Spanning Trees

- **Spanning trees:** A subgraph that includes every vertex of the original graph and is a tree.
- **Minimal spanning tree (Minimum Spanning Tree - MST):** In a weighted graph, a spanning tree with the minimum possible total edge weight.
- **Algorithms:** Kruskal's and Prim's algorithms find MSTs; BFS and DFS construct basic spanning trees.

### 6.4 CSE Applications of Trees

- **Application of trees:**
    - **Binary Search Trees (BST):** Used for efficient data location; elements smaller than the root go left, larger go right.
    - **Huffman Coding:** An algorithm used for efficient character encoding and data compression based on frequencies.
    - **Expression Trees:** Used to represent mathematical expressions (e.g., prefix and postfix notation).
    - **File Systems:** Computer directories and subdirectories are modeled as rooted trees.

---

## Chapter 7
## Algebraic Structure

**Algebraic structure: Algebraic system, general properties, some simple algebraic system.**

### 7.1 Algebraic Systems

- **Algebraic system (Algebraic structure):** A non-empty set $A$ equipped with one or more binary operations (e.g., $(A, *)$).
- **General properties:** Closure, associativity, identity element, inverse element, commutativity, distributivity.
- **Some simple algebraic system:**
    - **Semigroup:** An algebraic system with an associative binary operation $(S, *)$.
    - **Monoid:** A semigroup with an identity element.
    - **Group:** A monoid where every element has an inverse.
    - **Abelian group (Commutative group):** A group where the binary operation is commutative.
    - **Ring:** An algebraic system with two binary operations (addition and multiplication) satisfying ring axioms.
    - **Field:** A commutative ring where every non-zero element has a multiplicative inverse.

---

## Chapter 8
## Matrices and Bit Operations

### 8.1 Matrix Operations

- **Matrix Operations:** Includes sums, products, transposes, and symmetric matrices.
- **Zero-One Matrices (Relation matrix):** Used to represent relations; utilizes **Join** (logical OR) and **Meet** (logical AND) operations.

### 8.2 Bit Operations and Closures

- **Bit Strings:** Series of Boolean values (0 and 1) used to represent sets and perform fast logical operations.
- **Warshall's Algorithm (Closure and Optimization):** An efficient algorithm to find the **transitive closure** of a relation using bit operators.
- **Knapsack Problem:** A dynamic programming problem to find the most valuable subset of items that fit within a capacity.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Logic and Proofs | Proposition, Connectives ($\neg, \land, \lor, \to, \leftrightarrow$), Tautology, Quantifiers ($\forall, \exists$), Modus Ponens/Tollens, Direct/Contrapositive/Contradiction/Induction Proofs |
| 2 | Sets | Cardinality ($|A|$), Power Set ($P(A)$), Union ($\cup$), Intersection ($\cap$), Complement, Ordered Pairs ($(a,b)$) |
| 3 | Relations and Ordering | Reflexive, Symmetric, Antisymmetric, Transitive, Equivalence Relation, Poset, Lattice (LUB/GLB) |
| 4 | Functions | Injective (One-to-One), Surjective (Onto), Bijective, Composition ($(g \circ f)(x)$), Inverse Function ($f^{-1}$) |
| 5 | Graphs | Handshaking Theorem, Bipartite, Isomorphism, Euler/Hamilton Path, Graph Coloring, Dijkstra/Floyd Algorithm |
| 6 | Trees | Tree (connected acyclic), m-ary Tree, Binary Search Tree (BST), Huffman Coding, Spanning Tree, Minimum Spanning Tree (MST) |
| 7 | Algebraic Structure | Semigroup, Monoid, Group, Abelian Group, Ring, Field |
| 8 | Matrices & Bit Operations | Join (OR), Meet (AND), Warshall's Algorithm (Transitive Closure), Knapsack Problem |

---
*CSE 2131 — Discrete Mathematics | Dept. of CSE, University of Rajshahi*






