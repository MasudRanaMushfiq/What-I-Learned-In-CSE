

# Design and Analysis of Algorithms

### Course Information
**Course:** CSE 2221 (Design and Analysis of Algorithms)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE1121: Structural Programming Language, CSE2121: Data Structure

### Instructor
Dr. Md. Iqbal Aziz Khan, Professor, Dept. of CSE, University of Rajshahi 

### Course Motivation
> This course is offered to provide an introduction to mathematical modeling of computational problems.

---

## Course Contents

| Area | Topics Covered |
| ---- | -------------- |
| **Analysis of algorithm** | Time complexity, Space complexity |
| **Sorting** | Insertion sort, Bubble sort, Counting sort, Merge sort, Quick sort |
| **Searching** | Linear search, Binary search (on discrete domain and on continuous domain) |
| **Uninformed search** | DFS, BFS, Dijkstra, IDDFS, Meet-in-the-middle, Informed search, A* search, IDA* |
| **Local search** | Random restart hill climb, Simulated annealing, Local beam search, Genetic algorithm |
| **Game theoretic search** | Minimax search, Alpha-beta pruning |
| **Constraint satisfaction problem** | Backtrack, Algorithm x |
| **Data structure** | BST, Heap (priority queue), Merge sort tree (interval based sorted array), Treap (array merge, split and accumulation), UFDS (solving connectivity problem) |
| **Dynamic programming** | Subset sum / 0-1 knapsack, Interval DP |
| **Greedy** | Activity selection |
| **String** | KMP, Rabin Karp, Suffix array |
| **Geometry** | Line sweep, Jarvis march, Graham scan |

---

## Textbooks

**Primary Texts:**
1. Thomas H. Cormen, Clifford Stein, Ronald L. Rivest, Charles E. Leiserson — *Introduction to Algorithms*, The MIT Press

**Books Recommended:**
1. Antti Laaksonen — *Competitive Programmer's Handbook*, Springer
2. Antti Laaksonen — *Guide to Competitive Programming: Learning and Improving Algorithms Through Contests*, Springer

---

## Table of Contents

1. [Chapter 1 – Introduction to Algorithms](#chapter-1)
2. [Chapter 2 – Analysis of Complexity](#chapter-2)
3. [Chapter 3 – Sorting Algorithms](#chapter-3)
4. [Chapter 4 – Searching & Optimization Techniques](#chapter-4)
5. [Chapter 5 – Graph Algorithms (Uninformed and Informed Search)](#chapter-5)
6. [Chapter 6 – Local Search and Game Theoretic Search](#chapter-6)
7. [Chapter 7 – Constraint Satisfaction Problem](#chapter-7)
8. [Chapter 8 – Advanced Data Structures](#chapter-8)
9. [Chapter 9 – Dynamic Programming](#chapter-9)
10. [Chapter 10 – Greedy Algorithms](#chapter-10)
11. [Chapter 11 – String Matching Algorithms](#chapter-11)
12. [Chapter 12 – Computational Geometry](#chapter-12)

---

## Chapter 1
## Introduction to Algorithms

- **Definition:** An algorithm is a finite sequence of well-defined instructions to solve a computational problem. It takes an **input** and transforms it into a specific **output** through a series of computational steps.
- **Relation to Data Structures:** An algorithm is the method used to manipulate data, while a data structure is the storage system (e.g., array, list, tree) where that data resides. The choice of data structure significantly impacts the efficiency of an algorithm.
- **Steps in Algorithm Design:**
    1.  **Problem Definition:** Clearly define inputs, outputs, and constraints.
    2.  **Analysis of Requirements:** Identify time, space, and hardware limitations.
    3.  **Data Structure Selection:** Choose a structure that optimizes access and manipulation (e.g., using a heap for Dijkstra's).
    4.  **Design Strategy:** Select a paradigm (e.g., Divide and Conquer, Greedy, or Dynamic Programming).
    5.  **Complexity Analysis:** Use asymptotic analysis to determine performance bounds.
    6.  **Implementation & Testing:** Code the algorithm and validate it with various test cases, including edge cases.

---

## Chapter 2
## Analysis of Complexity

Algorithm efficiency is measured by resource utilization:

- **Time Complexity:** Measures the number of basic operations as a function of input size $n$.
- **Space Complexity:** The total memory required, including input storage, variables, and the recursive function call stack.
- **Asymptotic Notations:**
    - **Big-O ($O$):** Asymptotic **upper bound** (worst-case scenario).
    - **Omega ($\Omega$):** Asymptotic **lower bound** (best-case scenario).
    - **Theta ($\Theta$):** Asymptotic **tight bound** (average-case or exact growth rate).
- **Performance Cases:**
    - **Best Case:** Minimum time taken for ideal input (e.g., Linear Search on the first element is $\Omega(1)$).
    - **Worst Case:** Maximum time taken for the least favorable scenario (e.g., Quick Sort on a sorted array is $O(n^2)$).
    - **Average Case:** Expected time over random inputs.

---

## Chapter 3
## Sorting Algorithms

Sorting refers to the rearrangement of elements according to a comparison operator.

### 3.1 Comparison-Based Sorts

- **Insertion Sort:** Iteratively builds the sorted array by taking one element at a time and placing it in its correct position. Time: $O(n^2)$ (worst), $O(n)$ (best); Space: $O(1)$.
- **Bubble Sort:** Swaps adjacent elements if they are in the wrong order. Time: $O(n^2)$; Space: $O(1)$.
- **Selection Sort:** Repeatedly finds the smallest element from the unsorted portion and swaps it with the first unsorted element. Time: $O(n^2)$; Space: $O(1)$.
- **Merge Sort:** A **Divide and Conquer** algorithm. It divides the array into two halves, sorts them recursively, and merges them back. Time: $O(n \log n)$ for all cases; Space: $O(n)$.
- **Quick Sort:** Uses a **pivot** to partition the array into subarrays of smaller and larger elements.
    - **Best Case:** $\Omega(n \log n)$ (balanced partitions).
    - **Worst Case:** $O(n^2)$ (occurs if the array is already sorted or all elements are equal).
- **Heap Sort:** Converts an array into a **Max-Heap** and repeatedly extracts the maximum element. Time: $O(n \log n)$ for all cases; Space: $O(1)$ (in-place).

### 3.2 Non-Comparison Sorts

- **Counting Sort:** Sorts based on the frequency of distinct key values within a specific range $k$. Time: $O(n + k)$; Space: $O(n + k)$.

---

## Chapter 4
## Searching & Optimization Techniques

- **Linear search:** Linear search traverses the array sequentially to find a target element. Time complexity: $O(n)$.
- **Binary Search (on discrete domain and on continuous domain):** Binary search efficiently finds a target in a **sorted** array by repeatedly halving the search interval. Time: $O(\log n)$. On continuous domains, binary search is used to find the root of a function or optimize a unimodal function to a desired precision.
- **Ternary Search:** Divides the sorted array into three parts instead of two. Time: $O(\log_3 n)$.
- **Two-Pointer Algorithm:** Uses two indices to traverse data linearly. Used for finding pairs with specific sums or "Trapping Rain Water" problems.

---

## Chapter 5
## Graph Algorithms (Uninformed and Informed Search)

### 5.1 Graph Representations

- **Representations:**
    - **Adjacency List:** Array of lists; space-efficient for sparse graphs.
    - **Adjacency Matrix:** 2D array; good for dense graphs.

### 5.2 Uninformed Search

- **Breadth-First Search (BFS):** Explores nodes level-by-level using a **queue**. Used for finding the shortest path in unweighted graphs. Time: $O(V + E)$.
- **Depth-First Search (DFS):** Explores as far as possible along a branch before backtracking using a **stack** or recursion. Time: $O(V + E)$.
- **Dijkstra's Algorithm:** A **Greedy** approach to find the shortest path from a single source in a weighted graph with non-negative weights. Time: $O(E + V \log V)$.
- **IDDFS (Iterative Deepening Depth-First Search):** Combines the space-efficiency of DFS with the level-order exploration of BFS. It repeatedly runs depth-limited DFS with increasing depth limits.
- **Meet-in-the-Middle:** A technique for large problem sizes where the search space is split into two, solved separately, and merged. Time: $O(2^{n/2} \cdot \log 2^{n/2})$.

### 5.3 Informed Search

- **Informed search, A* search, IDA*:**
    - **Informed Search:** Uses heuristics (domain-specific knowledge) to guide the search toward the goal more efficiently than uninformed search.
    - **A* Search:** Combines the actual cost from the start ($g(n)$) with a heuristic estimate to the goal ($h(n)$) using $f(n) = g(n) + h(n)$. A* is optimal if the heuristic is admissible (never overestimates).
    - **IDA* (Iterative Deepening A*):** A memory-efficient version of A* that uses iterative deepening with an $f$-cost limit instead of maintaining a frontier set.

### 5.4 Minimum Spanning Tree (MST)

- **Kruskal's:** Greedy; adds the smallest weight edges that don't form a cycle. Uses **Disjoint Set Union (DSU)**.
- **Prim's:** Greedy; grows the tree from a starting vertex by adding the smallest edge connecting the tree to a new vertex.

---

## Chapter 6
## Local Search and Game Theoretic Search

### 6.1 Local Search

- **Local search: Random restart hill climb, Simulated annealing, Local beam search, Genetic algorithm:**
    - **Random restart hill climb:** Runs hill climbing multiple times from different random starting points to avoid getting stuck in local optima.
    - **Simulated annealing:** A probabilistic local search that sometimes accepts worse solutions to escape local optima, with the probability decreasing over time (annealing schedule).
    - **Local beam search:** Keeps $k$ states at each step, generating all successors and selecting the best $k$ to continue.
    - **Genetic algorithm:** A population-based search inspired by natural selection, using crossover, mutation, and selection operators.

### 6.2 Game Theoretic Search

- **Game theoretic search: Minimax search, Alpha-beta pruning:**
    - **Minimax search:** A recursive algorithm for two-player zero-sum games (e.g., chess). It assumes both players play optimally: the maximizing player chooses moves that maximize the minimum possible outcome.
    - **Alpha-beta pruning:** An optimization of minimax that prunes branches that cannot possibly influence the final decision, allowing deeper search with the same resources.

---

## Chapter 7
## Constraint Satisfaction Problem

- **Constraint satisfaction problem: Backtrack, Algorithm x:**
    - **Constraint Satisfaction Problem (CSP):** A problem where variables must be assigned values from domains subject to constraints.
    - **Backtrack:** A depth-first search algorithm for CSPs that assigns variables one at a time and backtracks when a constraint is violated.
    - **Algorithm X:** A recursive, nondeterministic, depth-first backtracking algorithm for solving the exact cover problem (e.g., solving Sudoku).

---

## Chapter 8
## Advanced Data Structures

- **BST (Binary Search Tree):** A tree data structure where each node has at most two children, with left child $\leq$ parent $\leq$ right child. Supports search, insert, delete in $O(\log n)$ average time.

- **Heap (priority queue):** A complete binary tree satisfying the heap property (parent $\geq$ children for max-heap). Supports insert and extract-min/max in $O(\log n)$.

- **Merge sort tree (interval based sorted array):** A segment tree where each node stores a sorted array of its interval's elements. Used for range queries like "number of elements $\leq k$ in $[l, r]$" in $O(\log^2 n)$.

- **Treap (array merge, split and accumulation):** A randomized binary search tree that is also a heap (tree + heap). Supports merge, split, and associative accumulation operations in $O(\log n)$ expected time.

- **UFDS (Union-Find Disjoint Set) solving connectivity problem:** Supports `Union` and `Find` operations. Optimized with **path compression** and **union by rank** to run in nearly $O(1)$ amortized time. Used for solving connectivity problems (e.g., finding connected components, cycle detection in Kruskal's).

- **Binary Indexed Tree (BIT) / Fenwick Tree:** Efficiently handles prefix sums and point updates. Update and Query: $O(\log n)$.

- **Segment Tree:** Used for range queries (sum, min, max). With **Lazy Propagation**, range updates also take $O(\log n)$.

- **Sqrt Decomposition:** Divides an array into blocks of size $\sqrt{N}$. Range queries and updates take $O(\sqrt{N})$.

- **Trie (Prefix Tree):** Tree-like structure used for fast string retrieval and prefix matching.

---

## Chapter 9
## Dynamic Programming (DP)

DP solves problems by breaking them into **overlapping subproblems** and storing results to avoid redundant calculations (**memoization**).

- **Requirements:** Optimal Substructure and Overlapping Subproblems.
- **Approaches:**
    - **Top-Down:** Recursive with memoization.
    - **Bottom-Up:** Iterative using a table (tabulation).
- **Examples:** Fibonacci series ($O(n)$ with DP), Longest Common Subsequence (LCS), Matrix Chain Multiplication.
- **Subset sum / 0-1 knapsack, Interval DP:**
    - **Subset sum / 0-1 knapsack:** Given weights and values, determine the maximum value that can be placed in a knapsack of capacity $W$ (or whether a subset sums to a target). DP state: $dp[i][w]$.
    - **Interval DP:** DP on intervals where the solution for an interval $[i, j]$ is built from smaller intervals. Used for problems like Matrix Chain Multiplication and Palindrome partitioning.
    - **Meet-in-the-Middle:** A technique for large problem sizes where the search space is split into two, solved separately, and merged. Time: $O(2^{n/2} \cdot \log 2^{n/2})$.

---

## Chapter 10
## Greedy Algorithms

A greedy algorithm makes the **locally optimal choice** at each step with the hope of finding a global optimum.

- **Activity Selection:** Choosing the maximum number of compatible tasks based on finish times.
- **Huffman Coding:** A greedy technique for data compression that assigns shorter codes to more frequent characters.

---

## Chapter 11
## String Matching Algorithms

- **String: KMP, Rabin Karp, Suffix array:**
    - **Knuth-Morris-Pratt (KMP):** Preprocesses the pattern to create an **LPS (Longest Proper Prefix which is also a Suffix)** array to avoid redundant comparisons. Time: $O(n + m)$.
    - **Rabin-Karp:** Uses **hashing** to find pattern occurrences in text. Time: $O(n + m)$ average case.
    - **Suffix array:** An array of all suffixes of a string sorted lexicographically. Used for efficient substring search, longest repeated substring, and other string processing tasks.

---

## Chapter 12
## Computational Geometry

- **Geometry: Line sweep, Jarvis march, Graham scan:**
    - **Convex Hull:** The smallest convex polygon enclosing all points.
        - **Graham Scan:** Uses sorting by polar angle; $O(n \log n)$.
        - **Jarvis March (Gift Wrapping):** Repeatedly finds the point with the smallest polar angle relative to the current point; $O(nh)$ where $h$ is the number of points on the hull.
    - **Line sweep:** A technique for solving geometric problems by sweeping a vertical (or horizontal) line across the plane and maintaining state at event points. Used for line segment intersection, closest pair of points, and rectangle union area.
    - **Line Segment Intersection:** Uses **orientation tests** (via cross product) to check if two segments intersect.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms / Complexity |
| --- | --- | --- |
| 1 | Introduction to Algorithms | Definition, Input, Output, Data Structure, Algorithm Design Steps |
| 2 | Complexity Analysis | Time Complexity, Space Complexity, Big-O ($O$), Omega ($\Omega$), Theta ($\Theta$), Best/Worst/Average Case |
| 3 | Sorting Algorithms | Insertion Sort ($O(n^2)$), Bubble Sort ($O(n^2)$), Selection Sort ($O(n^2)$), Merge Sort ($O(n \log n)$), Quick Sort ($O(n^2)$ worst, $O(n \log n)$ avg), Heap Sort ($O(n \log n)$), Counting Sort ($O(n+k)$) |
| 4 | Searching | Linear Search ($O(n)$), Binary Search ($O(\log n)$), Ternary Search, Two-Pointer |
| 5 | Graph Algorithms | BFS ($O(V+E)$), DFS ($O(V+E)$), Dijkstra ($O(E + V \log V)$), IDDFS, Meet-in-the-Middle, A*, IDA*, Kruskal's, Prim's |
| 6 | Local and Game Theoretic Search | Random Restart Hill Climb, Simulated Annealing, Local Beam Search, Genetic Algorithm, Minimax, Alpha-Beta Pruning |
| 7 | Constraint Satisfaction | CSP, Backtrack, Algorithm X, Exact Cover |
| 8 | Advanced Data Structures | BST ($O(\log n)$), Heap ($O(\log n)$), Merge Sort Tree, Treap, UFDS (nearly $O(1)$), BIT ($O(\log n)$), Segment Tree ($O(\log n)$), Sqrt Decomposition ($O(\sqrt{N})$), Trie |
| 9 | Dynamic Programming | Optimal Substructure, Overlapping Subproblems, Memoization, Tabulation, Subset Sum / 0-1 Knapsack, Interval DP |
| 10 | Greedy Algorithms | Locally Optimal Choice, Activity Selection, Huffman Coding |
| 11 | String Matching | KMP ($O(n+m)$), Rabin-Karp ($O(n+m)$ avg), Suffix Array |
| 12 | Computational Geometry | Convex Hull, Graham Scan ($O(n \log n)$), Jarvis March ($O(nh)$), Line Sweep, Orientation Test |

---
*CSE 2221 — Design and Analysis of Algorithms | Dept. of CSE, University of Rajshahi*




