

# Structural Programming Language

### Course Information
**Course:** CSE 1121 (Structural Programming Language)
**Course Type:** Theory, 3 Credit
**Prerequisite:** None
### Instructor
Dr. Md. Iqbal Aziz Khan, Professor, Dept. of CSE, University of Rajshahi 

### Course Motivation
> This course is offered to introduce students with the algorithmic way of thinking and problem solving by programming language.

---

## Course Contents

| Area | Topics Covered |
| ---- | -------------- |
| **Structured Programming Language fundamentals** | C overviews, History and Features, Basic Structure of C Program and Hello World Program, C Program Development Environment |
| **Variables, Constants, Data Types, Operators & Expression** | Declaring variables and assigning values, input from keyboard, add comments, Arithmetic Operators, Relational Operators, Logical Operators, Assignment Operators, Increment and Decrement Operators, Conditional Operators, Bitwise Operators, Special Operators, Arithmetic Expressions, Evaluation of Expressions, Type Conversions in Expressions, Operator Precedence and Associativity |
| **Program control statements** | Decision Making Statements; if-else statement, switch statement; Looping Statements: for loop, while loop, nested if, do while loop, nested loop; Jump Statements: continue, break |
| **Functions** | Function prototype, recursion, parameters, arguments, scope rules and storage classes |
| **Arrays and Pointer** | One and Multi-dimensional arrays, Character Arrays and Strings, Basic of Pointer, pointer expression, pointer arrays |
| **User defined data types and Input/Output** | Structures, Unions, Enumerations, Standard input and output, Formatted input and output, File access; Variable length argument list; Command line parameters; Error Handling; Graphics; Linking; Library functions |
| **Memory manipulation and Preprocessor** | Dynamic Memory Allocation and Linked List, Macro substitution, File inclusion, Compiler Control Directives |

---

## Textbooks

**Primary Texts:**
1. Steven Prata — *C Primer Plus*, Addison-Wesley Professional
2. Herbert Schildt — *C: The Complete Reference*, McGraw-Hill Osborne Media

---

## Table of Contents

1. [Chapter 1 – Structured Programming Language Fundamentals](#chapter-1)
2. [Chapter 2 – Variables, Constants, Data Types, Operators & Expression](#chapter-2)
3. [Chapter 3 – Program Control Statements](#chapter-3)
4. [Chapter 4 – Functions](#chapter-4)
5. [Chapter 5 – Arrays and Pointer](#chapter-5)
6. [Chapter 6 – User Defined Data Types and Input/Output](#chapter-6)
7. [Chapter 7 – Memory Manipulation and Preprocessor](#chapter-7)

---

## Chapter 1
## Structured Programming Language Fundamentals

### 1.1 C Overviews, History and Features

- **C Overviews:** C is a general-purpose, structured programming language widely used for system programming and application development.
- **History:** C was developed by Dennis Ritchie at Bell Laboratories in 1972.
- **Features:** C is efficient, portable, flexible, and provides low-level memory access with high-level language constructs.

### 1.2 Basic Structure of C Program and Hello World Program

- **Basic Structure of C Program:** A C program consists of preprocessor directives, global declarations, a main function, and user-defined functions.
- **Hello World Program:**
```c
#include <stdio.h>
int main() {
    printf("Hello, World!");
    return 0;
}
```


### 1.3 C Program Development Environment

- **C Program Development Environment:** The development environment includes an editor (to write code), preprocessor (to handle directives), compiler (to convert to object code), linker (to combine object files), and loader (to load into memory for execution).

---

## Chapter 2
## Variables, Constants, Data Types, Operators & Expression

### 2.1 Variables, Constants and Data Types

- **Declaring variables and assigning values:** Variables are declared with a data type followed by an identifier (e.g., `int num;`), and values are assigned using the assignment operator (`num = 10;`).
- **Constants:** Constants are fixed values that cannot be changed during program execution (e.g., `const int MAX = 100;` or `#define MAX 100`).
- **Data Types:** C provides basic data types including `int` (integer), `float` (floating-point), `char` (character), and `double` (double-precision floating-point).

### 2.2 Input from Keyboard

- **Input from keyboard:** The `scanf()` function is used to read input from the keyboard (e.g., `scanf("%d", &num);`).

### 2.3 Add Comments

- **Add comments:** Comments are ignored by the compiler and used for documentation. Single-line comments use `//`, and multi-line comments use `/* ... */`.

### 2.4 Operators

- **Arithmetic Operators:** `+` (addition), `-` (subtraction), `*` (multiplication), `/` (division), `%` (modulus/remainder).
- **Relational Operators:** `==` (equal to), `!=` (not equal to), `<` (less than), `>` (greater than), `<=` (less than or equal to), `>=` (greater than or equal to).
- **Logical Operators:** `&&` (logical AND), `||` (logical OR), `!` (logical NOT).
- **Assignment Operators:** `=` (simple assignment), `+=`, `-=`, `*=`, `/=`, `%=` (compound assignment).
- **Increment and Decrement Operators:** `++` (increment by 1), `--` (decrement by 1). Both have prefix (`++x`) and postfix (`x++`) forms.
- **Conditional Operators:** `? :` (ternary operator) – `condition ? expression_if_true : expression_if_false`.
- **Bitwise Operators:** `&` (bitwise AND), `|` (bitwise OR), `^` (bitwise XOR), `~` (bitwise complement), `<<` (left shift), `>>` (right shift).
- **Special Operators:** `sizeof` (returns size of operand), `&` (address of), `*` (dereference/pointer), `->` (structure pointer).

### 2.5 Expressions

- **Arithmetic Expressions:** Combinations of variables, constants, and operators that evaluate to a numeric value.
- **Evaluation of Expressions:** Expressions are evaluated according to operator precedence and associativity rules.
- **Type Conversions in Expressions:** C automatically converts operands to a common type (implicit conversion) when different types appear in an expression.
- **Operator Precedence and Associativity:** Operator precedence determines the order of evaluation (e.g., `*` and `/` before `+` and `-`). Associativity determines the order when operators have the same precedence (left-to-right or right-to-left).

---

## Chapter 3
## Program Control Statements

### 3.1 Decision Making Statements

- **if-else statement:** Executes a block of code if a condition is true, and optionally another block if false.
```c
if (condition) {
    // executes if condition is true
} else {
    // executes if condition is false
}

- **switch statement:** Allows multi-way branching based on the value of an integer expression.
```c
switch(expression) {
    case constant1: // code; break;
    case constant2: // code; break;
    default: // code;
}
```

### 3.2 Looping Statements

- **for loop:** Repeats a block of code a specified number of times.
```c
for (initialization; condition; increment) {
    // loop body
}
```
- **while loop:** Repeats a block of code while a condition is true (entry-controlled).
```c
while (condition) {
    // loop body
}
```
- **do while loop:** Repeats a block of code while a condition is true (exit-controlled, executes at least once).
```c
do {
    // loop body
} while (condition);
```
- **nested if:** An if statement inside another if statement.
- **nested loop:** A loop inside another loop.

### 3.3 Jump Statements

- **continue:** Skips the remaining code in the current loop iteration and jumps to the next iteration.
- **break:** Terminates the current loop or switch statement and transfers control to the statement following the loop/switch.

---

## Chapter 4
## Functions

### 4.1 Function Prototype

- **Function prototype:** A declaration that specifies the function's name, return type, and parameter types before the function is defined (e.g., `int add(int a, int b);`).

### 4.2 Recursion

- **Recursion:** A function that calls itself. Recursive functions must have a base case to terminate the recursion.

### 4.3 Parameters and Arguments

- **Parameters:** Variables listed in the function definition that receive values passed to the function.
- **Arguments:** Actual values passed to the function when it is called.

### 4.4 Scope Rules and Storage Classes

- **Scope Rules:** Determine where a variable is accessible (block scope, function scope, file scope).
- **Storage Classes:**
    - **auto:** Default storage class for local variables.
    - **register:** Suggests storing the variable in a CPU register for faster access.
    - **static:** Retains variable value between function calls (local static) or limits visibility to the file (global static).
    - **extern:** Declares a variable defined in another file.

---

## Chapter 5
## Arrays and Pointer

### 5.1 One and Multi-dimensional Arrays

- **One-dimensional array:** A linear collection of elements of the same type (e.g., `int arr[10];`).
- **Multi-dimensional arrays:** Arrays with more than one dimension (e.g., `int matrix[3][4];`).

### 5.2 Character Arrays and Strings

- **Character Arrays:** Arrays of type `char` used to store strings.
- **Strings:** Null-terminated (`\0`) character sequences. String functions are found in `<string.h>` (e.g., `strlen()`, `strcpy()`, `strcmp()`).

### 5.3 Basic of Pointer

- **Basic of Pointer:** A pointer is a variable that stores the memory address of another variable. Declared with an asterisk (e.g., `int *ptr;`).

### 5.4 Pointer Expression

- **pointer expression:** Expressions involving pointers, including pointer arithmetic (addition/subtraction of integers moves the pointer by the size of the pointed-to type).

### 5.5 Pointer Arrays

- **pointer arrays:** Arrays where each element is a pointer (e.g., `int *ptr_arr[10];`).

---

## Chapter 6
## User Defined Data Types and Input/Output

### 6.1 Structures, Unions, Enumerations

- **Structures:** A user-defined data type that groups related variables of different types under a single name (keyword `struct`).
- **Unions:** Similar to structures but all members share the same memory location (keyword `union`). Only one member can hold a value at a time.
- **Enumerations:** A user-defined type consisting of named integer constants (keyword `enum`).

### 6.2 Standard Input and Output

- **Standard input and output:** `stdin` (standard input, usually keyboard) and `stdout` (standard output, usually screen). Functions include `printf()`, `scanf()`, `getchar()`, `putchar()`.

### 6.3 Formatted Input and Output

- **Formatted input and output:** `printf()` and `scanf()` with format specifiers (`%d` for int, `%f` for float, `%c` for char, `%s` for string, etc.) control the formatting of data.

### 6.4 File Access

- **File access:** Files are opened using `fopen()`, read/written using `fprintf()`, `fscanf()`, `fgetc()`, `fputc()`, `fread()`, `fwrite()`, and closed using `fclose()`.

### 6.5 Variable Length Argument List

- **Variable length argument list:** Functions like `printf()` can accept a variable number of arguments using the `<stdarg.h>` header and macros `va_list`, `va_start`, `va_arg`, `va_end`.

### 6.6 Command Line Parameters

- **Command line parameters:** Arguments passed to the program at execution time, accessed through the `main` function parameters `int argc` (argument count) and `char *argv[]` (argument vector).

### 6.7 Error Handling

- **Error Handling:** The global variable `errno` (in `<errno.h>`) stores error codes. The `perror()` function prints a descriptive error message.

### 6.8 Graphics

- **Graphics:** Graphics programming in C uses libraries like `graphics.h` (Turbo C) or OpenGL/SDL for more advanced graphics.

### 6.9 Linking

- **Linking:** The process of combining object files and libraries into a single executable file. The linker resolves references to external functions and variables.

### 6.10 Library Functions

- **Library functions:** Pre-written functions provided in standard libraries (e.g., `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<math.h>`).

---

## Chapter 7
## Memory Manipulation and Preprocessor

### 7.1 Dynamic Memory Allocation and Linked List

- **Dynamic Memory Allocation and Linked List:** Dynamic memory allocation uses functions `malloc()`, `calloc()`, `realloc()`, and `free()` (in `<stdlib.h>`) to allocate memory at runtime. Linked lists are data structures built using dynamically allocated nodes.

### 7.2 Macro Substitution

- **Macro substitution:** The `#define` directive creates macros (symbolic constants or function-like macros). The preprocessor replaces macro names with their definitions before compilation.

### 7.3 File Inclusion

- **File inclusion:** The `#include` directive inserts the contents of a specified file into the source code. Angle brackets (`< >`) are used for system headers, double quotes (`" "`) for user-defined headers.

### 7.4 Compiler Control Directives

- **Compiler Control Directives:** Directives such as `#if`, `#ifdef`, `#ifndef`, `#else`, `#elif`, and `#endif` conditionally compile portions of code.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | C Fundamentals | History, Features, Basic Structure, Hello World, Development Environment (Editor, Preprocessor, Compiler, Linker, Loader) |
| 2 | Variables, Constants, Data Types, Operators | Declaring variables, Constants, Data Types (int, float, char, double), Arithmetic/Relational/Logical/Bitwise Operators, Increment/Decrement, Conditional Operator, Expression Evaluation, Type Conversion, Precedence, Associativity |
| 3 | Control Statements | if-else, switch, for loop, while loop, do while loop, nested if, nested loop, continue, break |
| 4 | Functions | Function prototype, Recursion, Parameters, Arguments, Scope Rules, Storage Classes (auto, register, static, extern) |
| 5 | Arrays and Pointer | One-dimensional array, Multi-dimensional array, Character Array, String, Pointer, Pointer Expression, Pointer Array |
| 6 | User Defined Types and I/O | Structure, Union, Enumeration, Standard I/O, Formatted I/O, File Access (fopen, fclose, fprintf, fscanf), Variable Length Argument List, Command Line Parameters (argc, argv), Error Handling (errno, perror), Graphics, Linking, Library Functions |
| 7 | Memory Manipulation and Preprocessor | Dynamic Memory Allocation (malloc, calloc, realloc, free), Linked List, Macro Substitution (#define), File Inclusion (#include), Compiler Control Directives (#if, #ifdef, #ifndef, #endif) |

---
*CSE 1121 — Structural Programming Language | Dept. of CSE, University of Rajshahi*





