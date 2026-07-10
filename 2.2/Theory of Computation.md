

# Theory of Computation

### Course Information
**Course:** CSE 2211 (Theory of Computation)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE2131 Discrete Mathematics

### Instructor
Dr. Md. Saiful Islam, Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> Mathematical study of computing machines and their capabilities.

---

## Course Contents

| Area | Topics Covered |
| ---- | -------------- |
| **Fundamentals** | Strings, Alphabet, Language, Operations, Finite state machine, definitions, finite automaton model, acceptance of strings, and languages, deterministic finite automaton and nondeterministic finite automaton, transition diagrams and Language recognizers |
| **Finite Automata** | NFA with null transitions - Significance, acceptance of languages. Conversions and Equivalence: Equivalence between NFA with and without null transitions, NFA to DFA conversion, minimization of FSM, equivalence between two FSM's, Finite Automata with output- Moore and Mealy machines |
| **Regular Languages** | Regular sets, regular expressions, identity rules, Constructing finite Automata for a given regular expressions, Conversion of Finite Automata to Regular expressions. Pumping lemma of regular sets, closure properties of regular sets |
| **Grammar Formalism** | Regular grammars-right linear and left linear grammars, equivalence between regular linear grammar and FA, inter conversion, Context free grammar, derivation trees, and sentential forms, Rightmost and leftmost derivation of strings |
| **Context Free Grammars** | Ambiguity in context free grammars. Minimization of Context Free Grammars, Chomsky normal form, Greibach normal form, Pumping Lemma for Context Free Languages. Enumeration of properties of CFL |
| **Push Down Automata** | Push down automata, definition, model, acceptance of CFL, Acceptance by final state and acceptance by empty state and its equivalence. Equivalence of CFL and PDA, interconversion. Introduction to DCFL and DPDA |
| **Turing Machine** | Turing Machine, definition, model, design of TM, Computable functions, recursively enumerable languages. Church's hypothesis, counter machine, types of Turing machines., linear bounded automata and context sensitive language |
| **Computability Theory** | Chomsky hierarchy of languages, decidability of problems, Universal Turing machine, undecidability of posts correspondence problem, Turing reducibility, Definition of P and NP Problems, NP complete and NP hard problems |


## Textbooks

**Primary Texts:**
1. Joha E. Hopcroft, Jeffery Ullman — *Introduction to Automata theory, Languages & Computation*, Narosa Publishers
2. K.L.P. Mishra & N. Chandrasekaran — *Theory of Computer Science*, PHI Learning
3. Michael Sipser — *Theory of Computation*, Cenage Learning

---

## Table of Contents

1. [Chapter 1 – Introduction to the Theory of Computation](#chapter-1)
2. [Chapter 2 – Finite Automata](#chapter-2)
3. [Chapter 3 – Regular Languages and Regular Expressions](#chapter-3)
4. [Chapter 4 – Grammar Formalism and Context Free Grammars](#chapter-4)
5. [Chapter 5 – Push Down Automata](#chapter-5)
6. [Chapter 6 – Turing Machines and Computability Theory](#chapter-6)
7. [Chapter 7 – Complexity Theory (P, NP, NP-Complete, NP-Hard)](#chapter-7)

---

## Chapter 1
## Introduction to the Theory of Computation

### 1.1 What is Theory of Computation?

The theory of computation comprises the fundamental mathematical properties of computer hardware, software, and their applications. It seeks to determine what can and cannot be computed, the resources required (time/memory), and the computational models used for these tasks.

- **Main Areas of Study:**
    1.  **Automata Theory:** Deals with the definitions and properties of mathematical models of computation used in text processing, compilers, and hardware design.
    2.  **Computability Theory:** Focuses on classifying problems as solvable or unsolvable.
    3.  **Complexity Theory:** Focuses on classifying problems as "easy" or "hard" based on the time or space resources required.

### 1.2 Basic Mathematical Notions (Strings, Alphabet, Language, Operations)

- **Basic Mathematical Notions:**
    - **Symbol:** The basic building block of computation (e.g., 0, 1, a, b).
    - **Alphabet ($\Sigma$):** A finite, non-empty set of symbols (e.g., $\Sigma = \{0, 1\}$).
    - **String:** A finite sequence of symbols from an alphabet.
    - **Language:** A set of strings chosen from some $\Sigma^*$.
    - **Computation:** Any type of calculation that follows a well-defined algorithm to find an answer.

### 1.3 Finite State Machine, Finite Automaton Model

- **Finite State Machine, definitions, finite automaton model, acceptance of strings, and languages, deterministic finite automaton and nondeterministic finite automaton, transition diagrams and Language recognizers:** Finite automata are the simplest computational models, used for devices with a small or limited amount of memory. A finite automaton model consists of a finite set of states, an input alphabet, a transition function, a start state, and a set of accept states. The acceptance of strings and languages is determined by whether the automaton ends in an accept state after processing the entire input. Transition diagrams visually represent the states and transitions of an automaton. Language recognizers are automata that accept or reject strings based on whether they belong to a specific language.

---

## Chapter 2
## Finite Automata

### 2.1 Deterministic Finite Automata (DFA)

**Finite Automata (FA)** are the simplest computational models, used for devices with a small or limited amount of memory.

A **DFA** is a model where there is exactly one transition exiting every state for each possible input symbol.

- **Formal Definition (5-tuple):** $M = (Q, \Sigma, \delta, q_0, F)$.
    1.  $Q$: Finite set of **states**.
    2.  $\Sigma$: Finite set called the **alphabet**.
    3.  $\delta: Q \times \Sigma \to Q$: **Transition function**.
    4.  $q_0 \in Q$: **Start/initial state**.
    5.  $F \subseteq Q$: Set of **accept states** (or final states).

### 2.2 Nondeterministic Finite Automata (NFA)

An **NFA** allows multiple next states or no state for a single input symbol, and can transition on the empty string ($\epsilon$).

### 2.3 NFA with Null Transitions - Significance, Acceptance of Languages

- **NFA with null transitions - Significance, acceptance of languages:** An NFA with null transitions (also called $\epsilon$-NFA) allows transitions on the empty string $\epsilon$, meaning the automaton can change state without consuming any input symbol. The significance is that it provides more flexibility in modeling certain systems. The acceptance of languages by an NFA with null transitions is defined by the existence of at least one path from the start state to an accept state that consumes all input symbols (with $\epsilon$-transitions allowed at any point).

### 2.4 Conversions and Equivalence

- **Equivalence:** DFAs and NFAs are equivalent in power; any NFA can be converted into a DFA that recognizes the same language.

- **Equivalence between NFA with and without null transitions:** NFAs with null transitions and NFAs without null transitions are equivalent. Any NFA with $\epsilon$-transitions can be converted to an equivalent NFA without $\epsilon$-transitions.

- **NFA to DFA conversion:** The conversion from NFA to DFA uses the subset construction method, where each state in the DFA represents a set of states from the NFA.

- **minimization of FSM:** Minimization of a Finite State Machine (FSM) is the process of reducing the number of states in a DFA to obtain an equivalent DFA with the minimum number of states.

- **equivalence between two FSM's:** Two FSMs are equivalent if they recognize the same language. This can be determined using table-filling algorithms or by minimizing both machines and comparing their structures.

### 2.5 Finite Automata with Output - Moore and Mealy Machines

- **Finite Automata with output- Moore and Mealy machines:**
    - **Moore Machine:** The output is determined solely by the current state.
    - **Mealy Machine:** The output is determined by the current state and the current input.

---

## Chapter 3
## Regular Languages and Regular Expressions

### 3.1 Regular Languages and Finite Automata

**Regular Languages** are languages that can be recognized by finite automata.

### 3.2 Regular Expressions (RE)

**Regular expressions** are a formal way to describe the patterns of strings in a regular language.

- **Regular sets, regular expressions, identity rules:** Regular sets are the sets of strings recognized by finite automata (regular languages). Regular expressions are algebraic descriptions of regular sets. Identity rules specify equivalences between different regular expressions (e.g., $R \cup \emptyset = R$, $R \epsilon = R$).

- **Identity:** A language is regular if and only if some regular expression describes it.

- **Example:** $(0 \cup 1)0^*$ describes all strings starting with 0 or 1 followed by any number of 0s.

### 3.3 Constructing Finite Automata for a Given Regular Expressions

- **Constructing finite Automata for a given regular expressions:** For any regular expression, a finite automaton (NFA with $\epsilon$-transitions) can be constructed recursively using Thompson's construction.

### 3.4 Conversion of Finite Automata to Regular Expressions

- **Conversion of Finite Automata to Regular expressions:** A finite automaton can be converted to a regular expression using state elimination methods or by solving a system of linear equations derived from the automaton's transition graph.

### 3.5 Non-Regular Languages and the Pumping Lemma

Not all languages are regular (e.g., $\{0^n1^n | n \ge 0\}$).

- **Pumping Lemma of regular sets, closure properties of regular sets:**
    - **Pumping Lemma:** A tool used to prove a language is **not regular** by showing it cannot be "pumped" while remaining in the language.
    - **Closure properties of regular sets:** Regular languages are closed under union, concatenation, Kleene star, intersection, complementation, and reversal.

---

## Chapter 4
## Grammar Formalism and Context Free Grammars

### 4.1 Regular Grammars (Right Linear and Left Linear Grammars)

- **Regular grammars-right linear and left linear grammars, equivalence between regular linear grammar and FA, inter conversion:**
    - **Right Linear Grammar:** Productions of the form $A \to aB$ or $A \to a$ (where $A, B$ are non-terminals, $a$ is a terminal).
    - **Left Linear Grammar:** Productions of the form $A \to Ba$ or $A \to a$.
    - **Equivalence between regular linear grammar and FA:** Regular grammars (right linear or left linear) generate exactly the same class of languages as finite automata (regular languages). There exists an interconversion procedure between regular grammars and finite automata.

### 4.2 Context Free Grammars (CFG)

**Context-Free Languages (CFL)** have a recursive structure and are more powerful than regular languages. They are used to specify the syntax of programming languages.

A **CFG** generates strings using substitution rules.

- **Formal Definition (4-tuple):** $G = (V, \Sigma, R, S)$.
    1.  $V$: Finite set of **variables** (non-terminals).
    2.  $\Sigma$: Finite set of **terminals** (disjoint from $V$).
    3.  $R$: Finite set of **substitution rules** (productions).
    4.  $S \in V$: The **start variable**.

- **derivation trees, and sentential forms, Rightmost and leftmost derivation of strings:**
    - **Derivation Tree (Parse Tree):** A graphical representation of the derivation of a string in a CFG.
    - **Sentential Forms:** The intermediate strings generated during a derivation.
    - **Leftmost Derivation:** At each step, the leftmost non-terminal is replaced.
    - **Rightmost Derivation:** At each step, the rightmost non-terminal is replaced.

### 4.3 Ambiguity in Context Free Grammars

- **Ambiguity in context free grammars:** A CFG is ambiguous if there exists a string that can be generated by two different leftmost derivations (or two distinct parse trees).

### 4.4 Minimization of Context Free Grammars

- **Minimization of Context Free Grammars:** CFG minimization involves eliminating useless symbols (non-generating and unreachable symbols), removing $\epsilon$-productions (except possibly from the start symbol), and removing unit productions.

### 4.5 Chomsky Normal Form (CNF) and Greibach Normal Form (GNF)

- **Chomsky Normal Form (CNF):** A simplified CFG where all rules are $A \to BC$ or $A \to a$ (where $A, B, C$ are non-terminals, and $a$ is a terminal). Additionally, $S \to \epsilon$ may be allowed if $\epsilon$ is in the language.

- **Greibach Normal Form (GNF):** A simplified CFG where all rules are of the form $A \to a\alpha$, where $A$ is a non-terminal, $a$ is a terminal, and $\alpha$ is a string of non-terminals (possibly empty).

### 4.6 Pumping Lemma for Context Free Languages

- **Pumping Lemma for Context Free Languages:** A tool used to prove that a language is **not context-free**. It states that for any infinite CFL, there exists a constant $p$ such that any string of length at least $p$ can be "pumped" in a specific way while remaining in the language.

### 4.7 Enumeration of Properties of CFL

- **Enumeration of properties of CFL:** Context-free languages are closed under union, concatenation, and Kleene star. They are not closed under intersection or complementation.

---

## Chapter 5
## Push Down Automata

### 5.1 Pushdown Automata (PDA) Definition and Model

**Context-Free Languages (CFL)** have a recursive structure and are more powerful than regular languages. They are used to specify the syntax of programming languages.

A **PDA** is essentially a finite automaton with an additional infinite memory component called a **stack**.

- **Push down automata, definition, model, acceptance of CFL, Acceptance by final state and acceptance by empty state and its equivalence:**
    - **Mechanism:** It uses **LIFO** (Last In, First Out) stack operations: **push** (add to top) and **pop** (remove from top).
    - **Acceptance by final state:** A PDA accepts a string if, after processing the entire input, it is in an accept state (regardless of the stack content).
    - **Acceptance by empty state:** A PDA accepts a string if, after processing the entire input, its stack is empty.
    - **Equivalence:** Acceptance by final state and acceptance by empty state are equivalent; any PDA of one type can be converted to a PDA of the other type.

### 5.2 Equivalence of CFL and PDA

- **Equivalence:** CFLs are precisely the languages accepted by (nondeterministic) PDAs.

- **Equivalence of CFL and PDA, interconversion:** For every context-free grammar, there exists an equivalent PDA that accepts the same language, and vice versa. Algorithms exist for interconversion between CFGs and PDAs.

### 5.3 Introduction to DCFL and DPDA

- **Introduction to DCFL and DPDA:** Deterministic Context-Free Languages (DCFLs) are languages accepted by Deterministic Pushdown Automata (DPDAs), where the automaton has at most one legal move from any configuration. DCFLs are a proper subset of CFLs.

---

## Chapter 6
## Turing Machines and Computability Theory

### 6.1 Turing Machines (TM)

**Turing Machine (TM)** is the most powerful computational model, capable of performing any algorithm. It uses an infinite tape as memory and a read-write head that can move in both directions.

- **Turing Machine, definition, model, design of TM, Computable functions, recursively enumerable languages.**
    - **Formal Definition (7-tuple):** $M = (Q, \Sigma, \Gamma, \delta, q_0, q_{accept}, q_{reject})$, where $\Gamma$ is the tape alphabet (contains $\Sigma$ and blank symbol $\sqcup$), and $\delta$ is the transition function that maps (state, tape symbol) to (new state, write symbol, direction {L,R}).
    - **Deciders:** A TM that halts on all inputs (never loops) is called a **decider**.
    - **Computable functions:** A function $f$ is computable if there exists a Turing machine that, given input $x$, halts with $f(x)$ written on its tape.
    - **Recursively enumerable languages:** Languages accepted by a Turing machine (if a string is in the language, the TM eventually accepts; if not, the TM may reject or loop forever).

### 6.2 Church's Hypothesis

- **Church's hypothesis (Church-Turing Thesis):** Asserts that any algorithm can be executed by a Turing machine. (i.e., anything that is computable is computable by a Turing machine).

### 6.3 Types of Turing Machines

- **counter machine:** A counter machine is a model of computation similar to a Turing machine but uses a finite number of counters (each storing a non-negative integer) instead of a tape.

- **types of Turing machines:** Types of Turing machines include multi-tape TMs, nondeterministic TMs, and multi-head TMs. These variations are all equivalent in power to the basic deterministic single-tape Turing machine.

### 6.4 Linear Bounded Automata and Context Sensitive Language

- **linear bounded automata and context sensitive language:** A Linear Bounded Automaton (LBA) is a Turing machine with a restricted tape size that is a linear function of the input length. LBAs recognize Context-Sensitive Languages (Type 1 in the Chomsky hierarchy).

---

## Chapter 7
## Computability Theory and Complexity Theory

### 7.1 Chomsky Hierarchy of Languages

The **Chomsky Hierarchy** classifies grammars into four types, each corresponding to a specific machine model.

| Type | Language Name | Grammar Name | Machine Model |
| :--- | :--- | :--- | :--- |
| **Type 0** | Recursively Enumerable | Unrestricted Grammar | Turing Machine |
| **Type 1** | Context-Sensitive | Context-Sensitive Grammar | Linear Bounded Automaton |
| **Type 2** | Context-Free | Context-Free Grammar | Pushdown Automaton |
| **Type 3** | Regular | Regular Grammar | Finite Automaton |

### 7.2 Decidability and Undecidability

This section explores the limits of what can be solved by computers.

- **decidability of problems, Universal Turing machine, undecidability of posts correspondence problem, Turing reducibility:**
    - **Decidable Language:** A language for which a TM exists that accepts every string in the language and rejects every string not in it.
    - **Undecidability:** Problems that cannot be solved by any algorithm.
    - **The Halting Problem ($A_{TM}$):** The most famous undecidable problem; it is impossible to write a program that can determine if an arbitrary program will eventually stop or loop forever.
    - **Universal Turing machine:** A Turing machine that can simulate any other Turing machine. It takes as input a description of a Turing machine and its input, and simulates its behavior.
    - **Undecidability of Post's Correspondence Problem (PCP):** Post's Correspondence Problem is a classic undecidable problem involving matching sequences of strings.
    - **Turing reducibility:** A problem $A$ is Turing-reducible to problem $B$ if there exists an algorithm that solves $A$ using a hypothetical algorithm that solves $B$ as a subroutine.

### 7.3 Complexity Theory (P, NP, NP-Complete, NP-Hard)

Complexity theory investigates the **resources** (time and space) required to solve decidable problems.

- **Definition of P and NP Problems, NP complete and NP hard problems:**
    - **Measuring Time:** The **time complexity** of a TM is the maximum number of steps it takes to solve a problem for an input of length $n$.
    - **The Class P:** Languages decidable in **polynomial time** on a deterministic TM (problems solvable in practice).
    - **The Class NP:** Languages where a solution can be **verified** in polynomial time.
    - **NP-Completeness:** A problem is **NP-complete** if it is in NP and every other problem in NP can be reduced to it. Solving one NP-complete problem in polynomial time would prove $P = NP$.
    - **NP-Hard:** A problem is NP-hard if every problem in NP can be reduced to it (but it may not be in NP itself).

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Introduction | Symbol, Alphabet ($\Sigma$), String, Language, Computation, Automata Theory, Computability Theory, Complexity Theory |
| 2 | Finite Automata | DFA (5-tuple: Q, $\Sigma$, $\delta$, $q_0$, F), NFA, $\epsilon$-NFA, Subset Construction, Moore Machine, Mealy Machine, FSM Minimization |
| 3 | Regular Languages | Regular Expression, Identity Rules, Pumping Lemma (for regular languages), Closure Properties (union, concatenation, Kleene star, intersection, complement) |
| 4 | Context Free Grammars | CFG (4-tuple: V, $\Sigma$, R, S), Derivation Tree, Leftmost/Rightmost Derivation, Ambiguity, CNF ($A \to BC$ or $A \to a$), GNF ($A \to a\alpha$), Pumping Lemma (for CFL) |
| 5 | Push Down Automata | PDA, Stack (LIFO, push, pop), Acceptance by Final State, Acceptance by Empty State, DCFL, DPDA |
| 6 | Turing Machines | TM (7-tuple), Church-Turing Thesis, Decider, Recursively Enumerable Languages, LBA, Context-Sensitive Language |
| 7 | Computability and Complexity | Chomsky Hierarchy (Type 0-3), Decidable, Undecidable, Halting Problem, Universal TM, PCP, P, NP, NP-Complete, NP-Hard, Turing Reducibility |

---
*CSE 2211 — Theory of Computation | Dept. of CSE, University of Rajshahi*





