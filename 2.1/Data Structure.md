

# Data Structure

### Course Information
**Course:** CSE 2121 (Data Structure)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE1121: Structural Programming Language
### Instructor
Md. Touhidul Islam, Associate Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To learn all accumulated expertise in computing and use them in data storage and access so as to write cleaner code that run much faster.

---

## Course Contents

| Area                             | Topics Covered                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Arrays**                       | Maximization, ordered lists, sparse matrices, representation of arrays.                                                                                                                                                                                                                                                                                                                                                                                              |
| **Stacks, Queues and Recursion** | Different types of stacks and queues: Circular, dequeues, etc; evaluation of expressions, multiple stacks and queues; Recursion: Direct and indirect recursion, depth of recursion; Simulation of Recursion, Removal of recursion; Towers of Hanoi.                                                                                                                                                                                                                  |
| **Linked Lists**                 | singly linked lists, linked stacks and queues, the storage pool, polynomial addition, equivalence relations, sparse matrices, doubly linked lists and dynamic storage management, generalized lists, garbage collection and compaction.                                                                                                                                                                                                                              |
| **Trees**                        | Basic terminology, binary trees, binary tree representations, binary tree traversal; Extended binary trees: 2-trees, internal and external path lengths, Huffman codes/algorithms; threaded binary trees, binary tree representation of trees; Application of Trees: Set representation, decision trees, games trees: Counting binary trees, Binary Indexed tree, Segment tree, Trip tree, Suffix tree, Merge Sort tree, Red-black tree, Splay tree, K-d tree, UFDS. |
| **Graphs**                       | Introduction, definitions and terminology, graph representations, traversals, connected components and spanning trees, shortest path and transitive closure, activity networks, topological sort and critical paths enumerating all paths.                                                                                                                                                                                                                           |
| **Symbol Tables**                | static tree tables, dynamic tree tables; Hash Tables: Hashing functions overflow handling: theoretical evaluation of overflow techniques.                                                                                                                                                                                                                                                                                                                            |
| **Files**                        | file, queries and sequential organizations: Indexing Techniques: Cylinder-surface indexing hashed indexes tree indexing-B-trees; Tree indexing.                                                                                                                                                                                                                                                                                                                      |


## Textbooks

**Primary Texts:**
1. Seymour Lipshultz — *Data Structures (Schaum's Outline Series)*, Tata McGraw-Hill.
2. E. Horowitz and S. Sahni — *Fundamentals of Data Structures*, Galgotia.

---

## Table of Contents

1. [Chapter 1 – Data Structure Fundamentals](#chapter-1)
2. [Chapter 2 – Arrays and Sparse Matrices](#chapter-2)
3. [Chapter 3 – Linked Lists](#chapter-3)
4. [Chapter 4 – Stacks, Queues, and Recursion](#chapter-4)
5. [Chapter 5 – Trees and Encoding](#chapter-5)
6. [Chapter 6 – Graphs and Their Algorithms](#chapter-6)
7. [Chapter 7 – Symbol Tables and Hashing Techniques](#chapter-7)
8. [Chapter 8 – Files and Indexing Techniques](#chapter-8)

---

## Chapter 1
## Data Structure Fundamentals

### 1.1 Definition and Necessity

A **data structure** is a logical way of organizing and storing data in a computer so it can be accessed and manipulated efficiently. They are necessary because they:
- Help understand relationships between data elements.
- Allow data to grow or shrink dynamically over time.
- Facilitate efficient data access and storage in logical order.

### 1.2 Linear vs. Non-linear Data Structures

Data structures are broadly categorized into two types:
- **Linear Data Structures:** Data elements are arranged in a sequential or linear order where each element is attached to its previous and next adjacent elements. Examples include **Arrays, Stacks, Queues, and Linked Lists**.
- **Non-linear Data Structures:** Data elements are attached in a hierarchical manner and not in a sequential order. Examples include **Trees and Graphs**.

---

## Chapter 2
## Arrays and Sparse Matrices

**Arrays: Maximization, ordered lists, sparse matrices, representation of arrays.**

### 2.1 Linear Arrays

A **linear array** is a list of a finite number of homogeneous (same type) data elements stored in successive memory locations.
- **Operations:** Common operations include Traversal (processing every element), Searching, Insertion, Deletion, Sorting, and Merging.
- **Memory Representation:** Only the address of the first element (**Base Address**) needs to be stored. The location of any element $LA[k]$ is calculated as:
    $LOC(LA[k]) = Base(LA) + w(k - LB)$
    *(where $w$ is the number of words per memory cell and $LB$ is the lower bound index)*.
- **Ordered lists:** A list where elements are arranged in a specific order (e.g., ascending or descending).

### 2.2 Multi-Dimensional Arrays (2D Arrays)

A 2D array represents data in a grid of rows and columns, such as a matrix. They are stored in memory using two main techniques:
- **Row Major Order (Representation of arrays):** Elements are stored row by row.
    Formula: $loc(A[i, j]) = Base(A) + w[n(i-1) + (j-1)]$.
- **Column Major Order (Representation of arrays):** Elements are stored column by column.
    Formula: $loc(A[i, j]) = Base(A) + w[m(j-1) + (i-1)]$.

### 2.3 Sparse Matrices

A **Sparse Matrix** is a matrix where a high proportion of entries are zero.
- **Triangular Matrix:** All elements above or below the main diagonal are zero.
- **Tridiagonal Matrix:** Non-zero entries only occur on the main diagonal or immediately above or below it.
- **Memory Saving:** Space is saved by storing only non-zero elements in a 1D array. For an $n \times n$ triangular matrix, the number of elements reduces from $n^2$ to $\frac{1}{2}n(n+1)$.

---

## Chapter 3
## Linked Lists

**Links Lists: singly linked lists, linked stacks and queues, the storage pool, polynomial addition, equivalence relations, sparse matrices, doubly linked lists and dynamic storage management, generalized lists, garbage collection and compaction.**

### 3.1 Definition and Advantages

A **linked list** is a linear data structure where elements are not stored in contiguous memory locations; instead, each node contains a data field and a reference (pointer) to the next node.
- **Advantages over Arrays:**
    - **Dynamic Size:** Can grow or shrink at runtime.
    - **Efficient Insertions/Deletions:** Only requires updating pointers rather than shifting elements.
    - **No Wasted Space:** Only uses memory as needed.

### 3.2 Types of Linked Lists

- **Singly linked lists:** Each node contains a pointer only to the next node; traversal is forward only.
- **Two-way (Doubly) Linked Lists (doubly linked lists):** Each node contains pointers to both the next and the previous nodes, allowing traversal in both directions.
- **Header Linked List:** Contains a special "header" node at the beginning of the list.
- **Linked stacks and queues:** Implementing stack and queue data structures using linked lists instead of arrays.
- **Generalized lists:** A list where elements can be atoms or sub-lists; useful for representing hierarchical data.

### 3.3 Key Concepts and Applications

- **The storage pool:** A pre-allocated block of memory from which nodes for linked lists are dynamically allocated.
- **Polynomial addition:** Using linked lists to represent polynomials (each node stores coefficient and exponent) and add them efficiently.
- **Equivalence relations:** Using linked lists to implement union-find algorithms for managing equivalence classes.
- **Sparse matrices (using linked lists):** Representing sparse matrices using linked lists to store only non-zero entries.
- **Dynamic storage management:** The process of allocating and deallocating memory dynamically for data structures.
- **Garbage Collection:** An automatic process that identifies and frees up memory no longer being used by the program to prevent memory leaks.
- **Compaction:** A memory management technique that moves allocated objects together to consolidate free space into a single large block.
- **Overflow:** Occurs when attempting to add data to a structure that is already full.
- **Underflow:** Occurs when attempting to delete data from an empty structure.

---

## Chapter 4
## Stacks, Queues, and Recursion

**Stacks, Queues and Recursion: Different types of stacks and queues: Circular, dequeues, etc; evaluation of expressions, multiple stacks and queues; Recursion: Direct and indirect recursion, depth of recursion; Simulation of Recursion, Removal of recursion; Towers of Hanoi.**

### 4.1 Stacks

A **Stack** is a linear list where elements are inserted and deleted at only one end called the **Top**. It follows the **Last-In, First-Out (LIFO)** principle.
- **Operations:** **Push** (insert) and **Pop** (delete).
- **Applications:** Expression evaluation, function call implementation, and backtracking.
- **Multiple stacks and queues:** Managing several stacks or several queues within a single array.

### 4.2 Queues

A **Queue** is a linear list where elements are inserted at the **Rear** and deleted from the **Front**. It follows the **First-In, First-Out (FIFO)** principle.
- **Circular Queue:** A variation where the last position is connected back to the first position to reuse empty slots. (Different types of stacks and queues: Circular, dequeues, etc).
- **Deque (Double-Ended Queue) (dequeues):** Allows insertion and removal from both ends.
- **Priority Queue:** Elements are processed based on an assigned priority rather than just arrival order.

### 4.3 Polish Notation (Evaluation of Expressions)

This refers to different ways of writing mathematical expressions to eliminate the need for parentheses and reduce ambiguity.
- **Infix:** Operator is between operands (e.g., $A + B$).
- **Prefix (Polish Notation):** Operator is before operands (e.g., $+AB$).
- **Postfix (Reverse Polish Notation):** Operator is after operands (e.g., $AB+$).
- **Evaluation of expressions:** Using stacks to convert infix expressions to postfix and evaluate postfix expressions.

### 4.4 Recursion

**Recursion** is a technique where a function calls itself. A recursive procedure must have a **base case** to terminate and move closer to that base case with each call.
- **Direct and indirect recursion:**
    - **Direct recursion:** A function calls itself directly.
    - **Indirect recursion:** Function A calls function B, and function B calls function A.
- **Depth of recursion:** The maximum number of nested recursive calls active at any one time.
- **Simulation of Recursion:** Using a stack to simulate the behavior of recursive function calls (push arguments and return addresses on call, pop on return).
- **Removal of recursion:** Converting a recursive algorithm into an iterative one (e.g., using explicit stacks) to improve efficiency or avoid stack overflow.
- **Examples:** Factorial calculation, Fibonacci sequence, and the Towers of Hanoi problem.

---

## Chapter 5
## Trees and Encoding

**Trees: Basic terminology, binary trees, binary tree representations, binary tree traversal; Extended binary trees: 2-trees, internal and external path lengths, Huffman codes/algorithms; threaded binary trees, binary tree representation of trees; Application of Trees: Set representation, decision trees, games trees: Counting binary trees, Binary Indexed tree, Segment tree, Trip tree, Suffix tree, Merge Sort tree, Red-black tree, Splay tree, K-d tree, UFDS.**

### 5.1 Binary Trees

A **Binary Tree** is a hierarchical structure where each node has at most two children.
- **Complete Binary Tree:** All levels are filled from left to right.
- **Binary Search Tree (BST):** A binary tree where the left child's value is less than the parent, and the right child's value is greater.
- **Terminology:** **Siblings** (children of same parent), **Ancestor** (nodes higher in the hierarchy), and **Depth** (length of path from root). (Basic terminology).
- **Binary tree representations:** Using arrays (for complete trees) or linked structures (each node contains data, left pointer, right pointer).

### 5.2 Tree Traversal Techniques

Traversing means visiting every node in the tree exactly once (binary tree traversal):
- **Preorder:** Root $\rightarrow$ Left $\rightarrow$ Right.
- **Inorder:** Left $\rightarrow$ Root $\rightarrow$ Right.
- **Postorder:** Left $\rightarrow$ Right $\rightarrow$ Root.

### 5.3 Extended Binary Trees and Path Lengths

- **Extended binary trees (2-trees):** A binary tree where every node has either 0 or 2 children (no nodes with exactly one child). Also known as a 2-tree.
- **Internal and external path lengths:**
    - **Internal path length:** Sum of the depths of all internal nodes.
    - **External path length:** Sum of the depths of all external (leaf) nodes.
- **Binary tree representation of trees:** Representing a general tree (where nodes can have any number of children) using a binary tree (first child/next sibling representation).

### 5.4 Special Binary Trees and Algorithms

- **Threaded binary trees:** A binary tree where null pointers are replaced with threads (pointers to inorder predecessor or successor) to facilitate easier traversal without using a stack.
- **Huffman codes/algorithms:** Huffman coding is a variable-length encoding scheme used for efficient space utilization. It assigns shorter codes to characters that appear more frequently in a message. The Huffman algorithm builds an optimal prefix code tree.
- **Heaps (related to priority queues):** A **Heap** is a complete binary tree used for priority-based operations.
    - **Max Heap:** The value of every node is greater than or equal to its children.
    - **Min Heap:** The value of every node is less than or equal to its children.

### 5.5 Applications of Trees

**Application of Trees:**
- **Set representation:** Using trees (e.g., disjoint-set forests with union by rank) to represent sets efficiently.
- **Decision trees:** A tree where each internal node represents a decision based on an attribute, and leaves represent outcomes; used in machine learning and decision support.
- **Games trees:** A tree representing all possible moves in a game; used for game-playing AI (e.g., minimax algorithm).
- **Counting binary trees:** Determining the number of distinct binary trees with a given number of nodes (Catalan numbers).
- **Binary Indexed tree (Fenwick Tree):** A tree structure that efficiently supports prefix sum queries and point updates.
- **Segment tree:** A tree structure used for answering range queries (sum, min, max) and range updates on an array.
- **Trip tree:** A specialized tree structure.
- **Suffix tree:** A compressed trie containing all suffixes of a given string; used for pattern matching, substring search, and bioinformatics.
- **Merge Sort tree:** A tree where each node stores a sorted list of its children's elements; used for answering range queries with order statistics.
- **Red-black tree:** A self-balancing binary search tree where each node has a color (red or black) to maintain balance; guarantees $O(\log n)$ for insert, delete, and search.
- **Splay tree:** A self-adjusting binary search tree that moves frequently accessed nodes to the root using splay operations.
- **K-d tree (k-dimensional tree):** A space-partitioning tree structure for organizing points in k-dimensional space; used for nearest neighbor search and range search.
- **UFDS (Union-Find Disjoint Sets):** A tree-based data structure that efficiently supports union and find operations on disjoint sets.

---

## Chapter 6
## Graphs and Their Algorithms

**Graphs: Introduction, definitions and terminology, graph representations, traversals, connected components and spanning trees, shortest path and transitive closure, activity networks, topological sort and critical paths enumerating all paths.**

### 6.1 Graph Terminology

A **Graph** consists of a set of vertices (nodes) and edges connecting them. (Introduction, definitions and terminology).
- **Directed Graph (Digraph):** Edges have a specific direction.
- **Weighted Graph:** Edges are assigned numerical values (weights) representing cost or distance.
- **Connectedness:** A graph is **strongly connected** if every pair of nodes has a path in both directions. It is **weakly connected** if there is a path between nodes in the underlying undirected graph.
- **Connected components:** Maximal connected subgraphs of an undirected graph.
- **Spanning trees:** A subgraph that includes all vertices with the minimum number of edges (no cycles) while remaining connected.
- **Activity networks:** A directed graph representing activities and dependencies in a project (e.g., PERT/CPM).
- **Critical paths:** The longest path through an activity network; determines the minimum project completion time.

### 6.2 Graph Representations

- **Adjacency Matrix:** A 2D array where entries (0 or 1, or weights) indicate connections between vertices.
- **Adjacency List:** A collection of linked lists where each node is followed by its list of neighbors.

### 6.3 Key Graph Algorithms

- **Traversals:** **Breadth-First Search (BFS)** uses a queue, while **Depth-First Search (DFS)** uses a stack. (Traversals).
- **Shortest Path and Transitive Closure:**
    - **Dijkstra's Algorithm:** Finds the shortest path from a single source node to all others in a weighted graph with non-negative edges.
    - **Warshall's Algorithm (Transitive Closure):** Efficiently calculates the path matrix (transitive closure) and shortest paths between all pairs of nodes (Floyd-Warshall).
- **Topological sort and critical paths enumerating all paths:**
    - **Topological sort:** A linear ordering of vertices in a DAG (Directed Acyclic Graph) such that for every directed edge $u \to v$, $u$ comes before $v$.
- **Minimum Spanning Trees (MST):** A subgraph that includes all vertices with the minimum total edge weight.
    - **Kruskal's Algorithm:** Build the MST by greedily adding the smallest edges without creating cycles.
    - **Prim's Algorithm:** Builds the tree one vertex at a time by adding the shortest edge connecting the current tree to an external vertex.

---

## Chapter 7
## Symbol Tables and Hashing Techniques

**Symbol Tables: static tree tables, dynamic tree tables; Hash Tables: Hashing functions overflow handling: theoretical evaluation of overflow techniques.**

### 7.1 Symbol Tables

- **Symbol Tables:** A data structure used by compilers to store information about variables, functions, and other identifiers.
- **Static tree tables:** A symbol table implemented as a static (fixed-size) tree; does not change size after creation.
- **Dynamic tree tables:** A symbol table implemented as a dynamic tree (e.g., binary search tree, AVL tree) that can grow and shrink at runtime.

### 7.2 Concept of Hashing

**Hashing** is a technique used to speed up searching by mapping data (keys) to a specific index in a **Hash Table** using a **Hash Function**. Ideally, this provides $O(1)$ constant time complexity for search operations.

### 7.3 Hash Functions

Common methods include:
- **Remainder Method (Division Method):** index = $key \pmod{\text{TableSize}}$.
- **Folding Method:** Dividing the key into pieces and adding them.
- **Mid-Square Method:** Squaring the key and extracting middle digits.

### 7.4 Collision Resolution

A **collision** occurs when two keys hash to the same index.
- **Separate Chaining:** Maintaining a linked list at each index to store colliding values.
- **Open Addressing (Overflow handling):** Searching for another available slot in the table:
    - **Linear Probing:** Sequentially checking the next available slots ($k+1, k+2, \dots$).
    - **Quadratic Probing:** Using a quadratic sequence to find the next slot, which helps reduce clustering.
- **Theoretical evaluation of overflow techniques:** Analysis of the performance (average search time, number of probes) of different collision resolution strategies under various load factors.

### 7.5 Load Factor

The **Load Factor ($\lambda$)** is the ratio of the number of items in the hash table to the total table size. A higher load factor increases the chance of collisions.

---

## Chapter 8
## Files and Indexing Techniques

**Files: file, queries and sequential organizations: Indexing Techniques: Cylinder-surface indexing hashed indexes tree indexing-B-trees; Tree indexing.**

### 8.1 Files and Organizations

- **File:** A collection of records stored on secondary storage (e.g., disk).
- **Queries:** Requests to retrieve specific records from a file based on certain conditions.
- **Sequential organizations:** Records are stored in a sequential order (e.g., by a key field); searching requires scanning sequentially.

### 8.2 Indexing Techniques

**Indexing Techniques:**
- **Cylinder-surface indexing (Cylinder-surface indexing):** An indexing method that organizes data based on the physical cylinder and surface locations on a disk to optimize access time.
- **Hashed indexes (hashed indexes):** Indexes that use a hash function to map keys directly to disk block addresses; provides fast direct access.
- **Tree indexing-B-trees (tree indexing-B-trees):** A balanced tree structure (B-tree and its variant B+ tree) used for indexing in database systems; maintains sorted data and allows efficient insert, delete, and search operations.
- **Tree indexing (Tree indexing):** General index structures based on tree organizations (e.g., B-trees, ISAM) for efficient range queries and sorted access.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Data Structure Fundamentals | Linear (Arrays, Stacks, Queues, Linked Lists), Non-linear (Trees, Graphs) |
| 2 | Arrays and Sparse Matrices | Base Address, Row Major ($n(i-1)+(j-1)$), Column Major, Triangular/Tridiagonal Sparse Matrices |
| 3 | Linked Lists | Singly/Doubly Linked, Garbage Collection, Overflow/Underflow, Dynamic Storage Management |
| 4 | Stacks, Queues, Recursion | LIFO (Push/Pop), FIFO (Enqueue/Dequeue), Circular Queue, Deque, Polish Notation (Prefix/Postfix), Direct/Indirect Recursion, Depth of Recursion, Towers of Hanoi |
| 5 | Trees | Binary Tree, BST, Pre/In/Postorder Traversal, Max/Min Heap, Huffman Codes, Red-black, Splay, Segment, Suffix Tree, K-d tree, UFDS |
| 6 | Graphs | Directed/Weighted, Adjacency Matrix/List, BFS (Queue), DFS (Stack), Dijkstra, Warshall, Kruskal, Prim, Topological Sort |
| 7 | Symbol Tables & Hashing | Static/Dynamic Tree Tables, Hash Function (Remainder/Folding/Mid-Square), Collision, Separate Chaining, Linear/Quadratic Probing, Load Factor ($\lambda$) |
| 8 | Files & Indexing | Sequential Organization, Cylinder-surface Indexing, Hashed Indexes, B-tree Indexing |

---
*CSE 2121 — Data Structure | Dept. of CSE, University of Rajshahi*






