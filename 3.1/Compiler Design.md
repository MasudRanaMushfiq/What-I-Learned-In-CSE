

# Compiler Design

### Course Information
**Course:** CSE 3141 (Compiler Design)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE2211 Theory of Computation, CSE2221 Design and Analysis of Algorithms, CSE2121 Data Structure
### Instructor
Dr. Md. Saiful Islam, Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To know basic structure of compiler and design of phases of compiler such as lexical analyzer, parser etc.

---

## Course Contents

| Area                  | Topics Covered                                                                                                                                                                                                       |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Fundamentals**      | Strings, Alphabet, Language, Operations, Finite state machine, definitions, finite automaton model, Introduction: Introduction to compiler, compiler and translator, the structure of a compiler                     |
| **Grammars**          | Notation and concepts for languages and Grammars, sets and string, Discussion and classification of Grammars, Scanner regular expression, regular definition, finite automata, LL and LR Grammars, ambiguous grammar |
| **Parsing**           | Basic parsing technique, parsers, shift reduce parsing, operator-procedure parsing, top-down parsing, bottom up parsing, predictive parsing                                                                          |
| **Syntax**            | Syntax directed translation, intermediate code generation, polish notation, parse tree and syntax trees, quadruples, triples, Boolean expression                                                                     |
| **Symbol Table**      | Perspective and motivation of symbol table. Symbol table content, operation on symbol table, organization of symbol table                                                                                            |


---

## Textbooks

**Primary Texts:**
1. Alfred V. Aho and Jeffrey D. Ullman — *Principles of Compiler Design*, Addison-Wesley Publication
2. A.J. Holub — *Compiler design in C*, Prentice-Hall of India

---

## Table of Contents

1. [Chapter 1 – Introduction to Language Processing and Compiler Structure](#chapter-1)
2. [Chapter 2 – Grammars and Fundamentals](#chapter-2)
3. [Chapter 3 – Lexical Analysis (Scanning)](#chapter-3)
4. [Chapter 4 – Parsing (Syntax Analysis)](#chapter-4)
5. [Chapter 5 – Syntax Directed Translation and Intermediate Code Generation](#chapter-5)
6. [Chapter 6 – Symbol Table](#chapter-6)

---

## Chapter 1
## Introduction to Language Processing and Compiler Structure

### 1.1 Fundamentals of Language Processing

**Strings, Alphabet, Language, Operations:**
- **Alphabet:** A finite set of symbols, typically denoted by $\Sigma$.
- **String:** A finite sequence of symbols drawn from an alphabet.
- **Language:** A set of strings over a fixed alphabet.
- **Operations on strings:** Concatenation, repetition (Kleene star), and reversal.

**Finite state machine, definitions:** A finite state machine (finite automaton) is a computational model with a finite number of states, transitions between states based on input symbols, a start state, and one or more accepting states.

**Finite automaton model:** The finite automaton model consists of: a finite set of states, a finite input alphabet, a transition function mapping (state, input) to next state, a start state, and a set of final/accepting states.

---

### 1.2 Introduction to Compilers

**Introduction to compiler:** The study of compiler design focuses on the principles, techniques, and tools used to translate a program written in a high-level language (HLL) into an equivalent target language, typically machine code. A compiler acts as a bridge between human-readable source code and the sequence of instructions a processor can understand.

**Compiler and translator:** A translator is a software system that converts source code into object code. A compiler translates the entire source program at once, leading to faster execution but platform-dependent object code. An interpreter translates and executes code step-by-step; it is platform-independent but slower. An assembler converts assembly language into machine code. A pre-processor handles macros and file inclusions before actual compilation.

**The structure of a compiler:** The compiler is organized into a sequence of phases. The compilation process is generally divided into two main parts: Analysis, which breaks the source program into constituent pieces and imposes a grammatical structure, and Synthesis, which constructs the desired target program from the intermediate representation.

**Front-End vs. Back-End:**
- **Front-End:** Consists of analysis phases (lexical, syntax, semantic) and intermediate code generation; it is largely machine-independent.
- **Back-End:** Focuses on synthesis phases (optimization, code generation) that are machine-dependent.

**Bootstrapping:** The process of writing a compiler for a language in that same language itself. It allows a compiler to self-compile once a basic version exists.

**The Six Phases of a Compiler:** Lexical → Syntax → Semantic → Intermediate Code Generation → Optimization → Code Generation.

---

## Chapter 2
## Grammars and Fundamentals

### 2.1 Notation and Concepts for Languages and Grammars

**Notation and concepts for languages and Grammars:** Grammars are formal systems used to describe the syntax of languages. They consist of a set of production rules that generate all valid strings of the language.

**Sets and string:** A set is a collection of elements. A string is a finite sequence of symbols from an alphabet. The empty string (denoted $\epsilon$) has length zero.

**Discussion and classification of Grammars:** Grammars are classified according to the Chomsky hierarchy:
- **Type 0 (Unrestricted Grammars):** No restrictions on production rules.
- **Type 1 (Context-Sensitive Grammars):** Productions have the form $\alpha A \beta \rightarrow \alpha \gamma \beta$ where $\gamma$ is non-empty.
- **Type 2 (Context-Free Grammars):** Productions have the form $A \rightarrow \gamma$, where $A$ is a non-terminal.
- **Type 3 (Regular Grammars):** Productions are right-linear or left-linear; they generate regular languages.

**Context-Free Grammar (CFG):** A formal system $(V, \Sigma, R, S)$ used to define language syntax, where $V$ is non-terminals, $\Sigma$ is terminals, $R$ is production rules, and $S$ is the start symbol.

---

### 2.2 Scanner and Regular Expressions

**Scanner regular expression:** A scanner (lexical analyzer) uses regular expressions to define patterns for tokens. Regular expressions use operators: concatenation, alternation (|), and Kleene star (*).

**Regular definition:** A regular definition is a sequence of regular expressions with associated names, allowing complex patterns to be built from simpler ones.

**Finite automata:** Finite automata are computational models used to implement regular expressions. They can be:
- **Deterministic Finite Automata (DFA):** Has exactly one transition for every state and input symbol.
- **Non-deterministic Finite Automata (NFA):** Can have multiple transitions for the same input or $\epsilon$-transitions.

---

### 2.3 LL and LR Grammars

**LL and LR Grammars:**
- **LL Grammar:** A grammar that can be parsed by a top-down parser scanning input from Left to right and producing a Leftmost derivation. LL(1) means one lookahead symbol.
- **LR Grammar:** A grammar that can be parsed by a bottom-up parser scanning input from Left to right and producing a Rightmost derivation in reverse.

**Ambiguous grammar:** An ambiguous grammar is a grammar that can generate the same string using two or more distinct parse trees. Ambiguity is generally undesirable for programming languages.

**Grammar Transformations:**
- **Elimination of Left Recursion:** Necessary for top-down parsers to prevent infinite loops.
- **Left Factoring:** Rewriting a grammar to delay decisions until enough of the input has been seen.
- **First and Follow Sets:** Used to construct predictive parsing tables.

---

## Chapter 3
## Lexical Analysis (Scanning)

### 3.1 Role and Definitions

**Role (Lexical Analysis):** This is the first phase, which reads characters and groups them into meaningful sequences called lexemes.

**Definitions:**
- **Token:** An abstract symbol representing a lexical unit (e.g., identifier, keyword).
- **Lexeme:** The actual character sequence in the source code matching a token pattern (e.g., `x`, `123`).
- **Pattern:** A rule, often defined by Regular Expressions, describing the form a lexeme must take.

**Implementation:** Lexical analyzers can be implemented using Finite Automata (DFA or NFA).

---

## Chapter 4
## Parsing (Syntax Analysis)

### 4.1 Basic Parsing Techniques

**Basic parsing technique:** Parsing is the process of determining whether a string of tokens can be generated by a grammar. It imposes a hierarchical structure on the token stream, typically expressed as a Parse Tree.

**Parsers:** A parser is a software component that performs syntax analysis. Parsers are classified as top-down or bottom-up.

**Shift reduce parsing:** Shift-reduce parsing is a bottom-up parsing technique that uses a stack and two actions: shift (push input symbol onto stack) and reduce (replace a handle on the stack with a non-terminal).

**Operator-procedure parsing:** Operator-precedence parsing is a simple bottom-up parsing method for operator grammars (grammars where no production has two consecutive non-terminals). It uses precedence relations between terminals.

**Top-down parsing:** Top-down parsing starts from the root (start symbol) and moves toward leaves; examples include Recursive Descent and LL(1) parsing.

**Bottom up parsing:** Bottom-up parsing starts from leaves (input tokens) and reduces toward the root (start symbol); examples include Shift-Reduce and the LR family (LR(0), SLR, LALR, CLR).

**Predictive parsing:** Predictive parsing is a top-down parsing technique that uses a parsing table (constructed from First and Follow sets) to decide which production to apply without backtracking.

> 📌 **Parsing Rule of Thumb:** Top-down is easier to write by hand; bottom-up is more powerful and usually automated.

---

### 4.2 LR Parsing Family

**LR (Left-to-right, Rightmost derivation in reverse) parsing** is the most prevalent type of bottom-up parsing used in modern compilers. It uses a **shift-reduce** strategy with an explicit stack to recognize the handle of a right-sentential form.

The four main types of LR parsers—LR(0), SLR, LR(1), and LALR—differ primarily in their parsing table construction and the amount of lookahead information they use to resolve conflicts.

#### 4.2.1 LR(0) Parsing
LR(0) is the simplest form of LR parsing and serves as the foundation for the others.
- **LR(0) Items:** An item is a grammar production with a **dot** ($\cdot$) at some position on the right side (e.g., $A \rightarrow X\cdot YZ$). The dot indicates how much of a production has been seen so far.
- **Automaton Construction:** States are formed by the **CLOSURE** of items and transitions are defined by the **GOTO** function.
- **Parsing Decisions:** Shift-reduce decisions are made without looking ahead at the input. In an LR(0) parsing table, if a state contains a final item (dot at the end), the reduction is placed across the entire row for all input symbols.
- **Limitation:** It often fails because many states will have **shift/reduce conflicts** (the parser doesn't know whether to shift a new symbol or reduce what is already on the stack).

#### 4.2.2 SLR (Simple LR) Parsing
SLR is an improvement over LR(0) that uses **FOLLOW sets** to resolve parsing conflicts.
- **Table Construction:** It uses the same canonical collection of LR(0) items as LR(0). However, it only places a **reduce action** for $A \rightarrow \alpha$ in the row of state $i$ for input symbols that are actually in **FOLLOW(A)**.
- **Power:** It is more powerful than LR(0) because it uses context to decide when a reduction is valid.
- **Limitation:** It cannot handle all unambiguous grammars because the FOLLOW set may be too broad a context to resolve some conflicts.

#### 4.2.3 LR(1) / Canonical LR Parsing
LR(1) is the most general and powerful non-backtracking shift-reduce parsing method.
- **LR(1) Items:** Unlike LR(0), items here include a **lookahead symbol** $[A \rightarrow \alpha \cdot \beta, a]$, where '$a$' is a terminal that can follow the production.
- **Logic:** A reduction is only called for if the next input symbol matches the specific lookahead terminal associated with that item in that specific state.
- **Pros/Cons:** It can recognize virtually all programming language constructs. However, it generates a very **large number of states** (thousands for a language like C), making it memory-intensive and slower to construct.

#### 4.2.4 LALR (Lookahead LR) Parsing
LALR is a compromise between the simplicity of SLR and the power of LR(1).
- **Core Idea:** It identifies sets of LR(1) items that have the same **"core"** (the same LR(0) part, ignoring lookaheads) and **merges** them into a single state.
- **Table Size:** The number of states is exactly the same as an SLR/LR(0) table, making it much smaller and more efficient than Canonical LR.
- **Power:** It is more powerful than SLR because it tracks specific lookaheads during state construction rather than relying on the general FOLLOW set.
- **Use Case:** LALR is the method of choice for most automated parser generators, such as **Yacc** and **Bison**.

#### 4.2.5 Comparison Summary

| Feature | LR(0) | SLR | LALR | LR(1) |
| :--- | :--- | :--- | :--- | :--- |
| **Lookahead** | None | Uses FOLLOW set | Merged LR(1) lookaheads | Full 1-symbol lookahead |
| **States** | Fewest | Same as LR(0) | Same as LR(0) | Most (thousands) |
| **Power** | Weakest | Medium | High (standard for tools) | Strongest |
| **Conflicts** | Many | Reduced by FOLLOW | Rare | Fewest |

---

## Chapter 5
## Syntax Directed Translation and Intermediate Code Generation

### 5.1 Syntax Directed Translation

**Syntax directed translation (SDT):** Attaches semantic actions to the productions of a CFG to perform translation tasks.

**Attributes:**
- **Synthesized Attributes:** Values computed from the attributes of children in the parse tree.
- **Inherited Attributes:** Values computed from the attributes of parents or siblings.

**Syntax-Directed Definition (SDD):** A high-level specification using attributes and rules.

**Syntax-Directed Translation Scheme (SDT):** An SDD with program fragments (actions) embedded within production bodies.

---

### 5.2 Intermediate Code Generation

**Intermediate code generation (ICG):** Translates the source program into a machine-independent internal representation.

**Polish notation:** Polish notation (prefix notation) places the operator before its operands (e.g., `+ a b`); Reverse Polish Notation (postfix notation) places the operator after its operands (e.g., `a b +`). Postfix notation does not require parentheses.

**Parse tree and syntax trees:**
- **Parse tree:** A concrete representation of the grammatical structure of a source program, where every leaf is a terminal and every internal node is a non-terminal.
- **Syntax tree (Abstract Syntax Tree, AST):** A condensed version of the parse tree that omits non-essential punctuation and production rules.

**Three-Address Code (3AC):** Instructions have at most one operator and three addresses (e.g., $x = y + z$).

**Quadruples:** A 3AC implementation using four fields: (op, arg1, arg2, result).

**Triples:** A 3AC implementation using three fields: (op, arg1, arg2). Results are referenced by their position in the triple list.

**Boolean expression:** Boolean expressions are expressions that evaluate to true or false; they are often translated using control-flow (short-circuit) or value-based methods.

> 💡 **Phases of Translation — For the statement `position = initial + rate * 60`:**
> - **Lexical:** Produces tokens like `id1 = id2 + id3 * 60`.
> - **Syntax:** Builds a parse tree where `*` has higher precedence than `+`.
> - **Semantic:** Might perform type conversion (e.g., `int-to-float(60)`).
> - **ICG:** Generates 3AC like `t1 = id3 * 60.0; id1 = id2 + t1`.

> 💡 **3AC Implementation — For $x = a + b * c$, a Quadruple representation would look like:**
> 1. `(*, b, c, t1)`
> 2. `(+, a, t1, x)`

---

## Chapter 6
## Symbol Table

### 6.1 Symbol Table Fundamentals

**Perspective and motivation of symbol table:** A symbol table is a data structure used to store information about identifiers, such as their type, scope, and memory location. It is motivated by the need to track attributes of names as they appear in the source program.

**Symbol table content:** The symbol table typically contains for each identifier: name, type, scope, memory location (address), size, and any other attributes (e.g., const/volatile qualifiers, parameter list for functions).

**Operation on symbol table:** Basic operations on a symbol table include: insertion (adding a new symbol), lookup (finding a symbol by name), deletion (removing a symbol when scope exits), and update (modifying attributes of an existing symbol).

**Organization of symbol table:** Symbol tables can be organized using linear lists, binary search trees, hash tables, or nested scope structures (e.g., a stack of symbol tables for block-structured languages).

---

## Quick Reference Summary

| Chapter | Core Topic        | Key Terms                                                                                                  |
| ------- | ----------------- | ---------------------------------------------------------------------------------------------------------- |
| 1       | Introduction      | Translator, Compiler vs. Interpreter, Front-End/Back-End, Bootstrapping, Six Phases                        |
| 2       | Grammars          | Chomsky hierarchy, CFG, Regular Expression, DFA/NFA, LL/LR, Ambiguous grammar                              |
| 3       | Lexical Analysis  | Token, Lexeme, Pattern, Finite Automata implementation                                                     |
| 4       | Parsing           | Shift-reduce, Top-down, Bottom-up, Predictive parsing, Parse Tree, LR(0), SLR, LALR, LR(1)                |
| 5       | Syntax & ICG      | SDT, Synthesized/Inherited attributes, Polish notation, 3AC, Quadruples, Triples                           |
| 6       | Symbol Table      | Insert, Lookup, Delete, Hash tables, Scope stack                                                           |

---
*CSE 3141 — Compiler Design | Dept. of CSE, University of Rajshahi*





