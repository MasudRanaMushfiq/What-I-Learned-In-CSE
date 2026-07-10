

# Object Oriented Programming

### Course Information
**Course:** CSE 1221 (Object Oriented Programming)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE1121 Structural Programming Language
### Instructor
Mr. Md. Omar Faruqe, Associate Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> Introduce how to design a computer program by making them out of objects that interact with one another.

---

## Course Contents

| Area                                  | Topics Covered                                                                                                                                                                                                                                                   |
| ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Introduction**                      | Object Oriented Programming Concepts and features, Java as OOP language, Typical Java Development Environment. Java's Primitive Data Types, Operator (arithmetic and logical) and Control Structures                                                             |
| **Classes and Objects (Basic)**       | Java Classes, Objects, Methods and instance variables, Program Modules in Java, static Methods, static Fields, Methods with Multiple Parameters, Java API Packages                                                                                               |
| **Arrays**                            | Arrays, Enhanced for Statement, Passing Arrays to Methods, Variable-Length Argument Lists, Using Command-Line Arguments                                                                                                                                          |
| **Classes and Objects (Deeper Look)** | Encapsulation and data hiding, the notions of data abstraction and abstract data types (ADTs), use of keyword this, use of static variables and methods, to import static members of a class, Controlling Access to Members, Inheritance, Polymorphism, Packages |
| **Exception Handling**                | How exception and error handling works, to use try, throw and catch to detect, indicate and handle exceptions respectively, to use the finally block to release resources, to declare new exception classes                                                      |
| **Files and Streams**                 | To create, read, write and update files, to retrieve information about files and directories, Java input/output stream class hierarchy, differences between text files and binary files, Sequential-access and random-access file processing                     |


## Textbooks

**Primary Texts:**
1. Herbert Schildt — *Java: The Complete Reference, Ninth Edition 9th Edition*, Oracle Press

---

## Table of Contents

1. [Chapter 1 – Introduction to Computer Science and Java](#chapter-1)
2. [Chapter 2 – Fundamental Data Types and Input/Output](#chapter-2)
3. [Chapter 3 – Objects and Classes](#chapter-3)
4. [Chapter 4 – Designing Classes](#chapter-4)
5. [Chapter 5 – Inheritance and Polymorphism](#chapter-5)
6. [Chapter 6 – Interfaces](#chapter-6)
7. [Chapter 7 – Exception Handling and File I/O](#chapter-7)
8. [Chapter 8 – Generics and Data Structures](#chapter-8)
9. [Chapter 9 – Object-Oriented Design (OOD)](#chapter-9)

---

## Chapter 1
## Introduction to Computer Science and Java

### 1.1 Computer Program and Programming

- **Computer Program:** A sequence of instructions and decisions that a computer executes to perform tasks.
- **Programming:** The act of designing and implementing these computer programs.
- **Algorithm:** A step-by-step description of how to solve a problem. A valid algorithm must be **unambiguous** (precise steps), **executable** (can be carried out), and **terminating** (eventually ends).

### 1.2 Java Attributes and Object Oriented Programming Concepts

- **Java Attributes:** Designed for the internet, Java is notable for **safety** (terminates unsafe programs) and **portability** (runs on a virtual machine, making it platform-independent).
- **Object Oriented Programming Concepts and features:** Object-oriented programming organizes code around objects that contain data and methods that operate on that data.
- **Java as OOP language:** Java is an object-oriented programming language that supports classes, objects, inheritance, polymorphism, encapsulation, and abstraction.
- **Typical Java Development Environment:** The typical Java development environment includes a text editor (or IDE), Java compiler (javac), Java Virtual Machine (JVM), and Java class libraries.

---

## Chapter 2
## Fundamental Data Types and Input/Output

### 2.1 Data Types

- **Variables:** A named storage location in a program.
- **Java's Primitive Data Types:** Java has eight primitive types, including four integer types (e.g., `int`) and two floating-point types (e.g., `double` for numbers with fractional parts).
- **Strings:** A sequence of characters. They are **immutable**, meaning they cannot be changed once constructed.
    - *Example:* `String sub = greeting.substring(0, 5);` extracts characters from index 0 to 4.

### 2.2 Operators and Control Structures

- **Operators (arithmetic and logical):** Standard arithmetic includes `+`, `-`, `*`, `/`. The `%` operator computes the remainder of integer division. Logical operators include `&&` (AND), `||` (OR), and `!` (NOT).
- **Control Structures:** Control structures include if-else statements, switch statements, while loops, do-while loops, and for loops that control the flow of program execution.

### 2.3 Formatted Output

- **Printf:** Used to produce formatted output, such as lining up columns or specifying decimal places.
    - *Example:* `System.out.printf("%.2f", price);` displays a price with two digits after the decimal point.

### 2.4 Input

- **Scanner Class:** Used to read keyboard input from the console.
    - *Example:* `Scanner in = new Scanner(System.in); int value = in.nextInt();`

---

## Chapter 3
## Objects and Classes

### 3.1 Definitions

- **Class:** A blueprint or template that defines the structure (data) and behavior (methods) of a set of objects.
- **Java Classes:** A Java class is a user-defined data type that serves as a blueprint for creating objects.
- **Object:** An instance of a class and a real-world entity (e.g., a specific "bank account" or "pen").
- **Object Variable:** Does not actually hold the object, but holds an **object reference** (the memory location of the object).
- **Program Modules in Java:** Program modules in Java are methods that break complex computations into smaller, manageable pieces.

### 3.2 Methods and Instance Variables

- **Methods:** Methods define the behavior of an object and specify what operations can be performed on that object.
- **Instance Variables:** Instance variables store the data (state) of a specific object.
- **Methods with Multiple Parameters:** Java methods can accept multiple parameters, separated by commas in the method declaration.
- **Public Interface:** The set of methods through which a programmer interacts with a class; it specifies what the class can do without revealing how.
- **Accessor Method:** Asks an object for information without changing its internal state.
- **Mutator Method:** Changes the internal data of an object.

### 3.3 Construction

- **Constructor:** A special method that sets the initial values for an object. It must have the same name as the class and does **not** have a return type (not even `void`).
- **New Operator:** Used to construct new objects.
    - *Example:* `Rectangle box = new Rectangle(5, 10, 20, 30);`

### 3.4 Static Methods and Static Fields

- **Static Methods:** A method that is not invoked on an object (e.g., `Math.sqrt(x)`). Static methods belong to the class rather than any instance.
- **Static Fields:** A static variable belongs to the class itself, not to any individual object. All objects of the class share the same copy.

### 3.5 Java API Packages

- **Java API Packages:** The Java Application Programming Interface (API) provides a collection of pre-written classes and interfaces organized into packages (e.g., `java.lang`, `java.util`, `java.io`).

---

## Chapter 4
## Designing Classes

### 4.1 Key Principles

- **Single Responsibility Principle (SRP):** A class should have only one reason to change, meaning it should focus on a single responsibility or function.
- **Encapsulation and Data Hiding:** The process of hiding implementation details (by making instance variables **private**) and providing public methods for data access.
- **The Notions of Data Abstraction and Abstract Data Types (ADTs):** Data abstraction is the concept of hiding implementation details and exposing only essential features. An Abstract Data Type (ADT) is a data type defined by its behavior (operations) rather than its implementation.
- **Cohesion:** A class is cohesive if all of its interface features are closely related to the single concept the class represents.

### 4.2 The `this` Keyword

- **Use of keyword `this`:** The `this` keyword refers to the current object within a method or constructor. It is used to distinguish between instance variables and parameters with the same name.

### 4.3 Static Members

- **Use of static variables and methods:** Static variables and methods belong to the class rather than instances. Static methods cannot access instance variables directly because they are not associated with any specific object.
- **To import static members of a class:** Java allows importing static members using `import static` so that they can be referenced without class qualification (e.g., `import static java.lang.Math.sqrt;`).

### 4.4 Controlling Access to Members

- **Controlling Access to Members:** Java provides access modifiers — `private`, `protected`, `public`, and package-private (default) — to control which classes can access a member.

### 4.5 Arrays

- **Arrays:** An array is a data structure that holds a fixed number of values of the same type.
- **Enhanced for Statement:** The enhanced for loop (for-each loop) iterates through all elements of an array or collection without using an index counter.
- **Passing Arrays to Methods:** Arrays are objects in Java; when passed to a method, the method receives a reference to the array, allowing it to modify the original array elements.
- **Variable-Length Argument Lists:** Variable-length argument lists (varargs) allow methods to accept an arbitrary number of arguments of the same type, denoted by an ellipsis (`...`).
- **Using Command-Line Arguments:** Command-line arguments are passed to the `main` method as a `String` array named `args`, allowing programs to receive input when launched.

### 4.6 Inheritance

- **Subclass and Superclass:** A subclass inherits data and behavior from a more general superclass using the `extends` keyword.
- **Overriding:** When a subclass provides a new implementation for a method inherited from the superclass.
- **Super Keyword:** Used to call a superclass constructor or method.
    - *Example:* `super.withdraw(amount);` calls the superclass's version of the withdraw method.

### 4.7 Polymorphism

- **Polymorphism:** The ability to treat objects of different subclasses in a uniform way.
- **Dynamic Method Lookup:** Method calls are determined by the type of the actual object at runtime, not the type of the variable reference.
- **Abstract Class:** A class that cannot be instantiated and may contain **abstract methods** (methods without implementation).

### 4.8 Packages

- **Packages:** Packages are namespaces that organize classes and interfaces, preventing naming conflicts and controlling access visibility.

---

## Chapter 5
## Inheritance and Polymorphism

### 5.1 Inheritance

- **Subclass and Superclass:** A subclass inherits data and behavior from a more general superclass using the `extends` keyword.
- **Overriding:** When a subclass provides a new implementation for a method inherited from the superclass.
- **Super Keyword:** Used to call a superclass constructor or method.
    - *Example:* `super.withdraw(amount);` calls the superclass's version of the withdraw method.

### 5.2 Polymorphism

- **Polymorphism:** The ability to treat objects of different subclasses in a uniform way.
- **Dynamic Method Lookup:** Method calls are determined by the type of the actual object at runtime, not the type of the variable reference.
- **Abstract Class:** A class that cannot be instantiated and may contain **abstract methods** (methods without implementation).

---

## Chapter 6
## Interfaces

- **Definition:** A "contract" that specifies required operations without implementing them. Unlike classes, interfaces have no instance variables and no constructors.
- **Implementation:** A class uses the `implements` keyword to indicate it provides the required method bodies.
- **Callbacks:** A mechanism for bundling code (often as an object) to be executed at a later time.
- **Lambda Expressions:** A compact notation for specifying a block of code for a functional interface (an interface with a single abstract method).

---

## Chapter 7
## Exception Handling and File I/O

### 7.1 Exception Handling

- **How exception and error handling works:** Exception handling allows a program to detect and respond to runtime errors without crashing.
- **Throwing:** Use the `throw` statement to signal an exceptional condition (e.g., `throw new IllegalArgumentException();`).
- **To use try, throw and catch to detect, indicate and handle exceptions respectively:**
    - `try` block encloses code that might throw an exception.
    - `throw` statement signals that an exception has occurred.
    - `catch` block handles the thrown exception.
- **To use the finally block to release resources:** The `finally` block executes regardless of whether an exception is thrown or caught, making it ideal for releasing resources (closing files, database connections).
- **To declare new exception classes:** New exception classes can be created by extending the `Exception` class (for checked exceptions) or `RuntimeException` (for unchecked exceptions).
- **Checked vs. Unchecked:** Checked exceptions (like `IOException`) must be handled or declared in the method header with a `throws` clause. Unchecked exceptions (like `ArithmeticException`) represent logic errors and do not require explicit handling.

### 7.2 File I/O

- **To create, read, write and update files:** Java provides classes for file operations including creating, reading, writing, and updating files.
- **Reading:** Use `Scanner` combined with a `File` object.
- **Writing:** Use the `PrintWriter` class.
- **Closing Files:** Always close `Scanner` and `PrintWriter` objects to ensure all data is written to the disk.
- **To retrieve information about files and directories:** The `File` class provides methods to retrieve information about files and directories (name, size, existence, whether it is a file or directory).
- **Java input/output stream class hierarchy:** The Java I/O stream hierarchy includes `InputStream`, `OutputStream`, `Reader`, `Writer` as abstract base classes, with concrete subclasses like `FileInputStream`, `FileOutputStream`, `BufferedReader`, `PrintWriter`.
- **Differences between text files and binary files:** Text files store data as human-readable characters; binary files store data in the same format as in memory (more compact but not human-readable).
- **Sequential-access and random-access file processing:** Sequential-access files are read/written in order from beginning to end. Random-access files allow direct access to any byte position using `RandomAccessFile`.

---

## Chapter 8
## Generics and Data Structures

- **Generic Class:** A class parameterized with one or more **type parameters** (e.g., `ArrayList<E>`), allowing it to work safely with different data types.
- **Type Erasure:** The process where the Java virtual machine replaces type parameters with their bounds (or `Object`) because it does not recognize generic types at execution.
- **Collections Framework:** A hierarchy of interfaces (List, Set, Map) and classes for grouping objects.
    - **List:** Ordered collection (e.g., `ArrayList`, `LinkedList`).
    - **Set:** Unordered collection of unique elements.
    - **Map:** Stores associations between key and value objects.

---

## Chapter 9
## Object-Oriented Design (OOD) and Design Patterns

### 9.1 Design Process

- **Design Process:**
    1.  **Gather Requirements:** Define what the program must do.
    2.  **CRC Cards:** Identify Classes, Responsibilities, and Collaborators by looking for nouns and verbs in the requirements.
    3.  **UML Diagrams:** Use standard notation to record relationships like **Inheritance** (is-a) and **Aggregation** (has-a).
    4.  **Documentation:** Use **javadoc** to describe classes and methods before implementation.
    5.  **Implementation:** Write the actual code.

### 9.2 Design Patterns

- **Overview:** Design patterns are reusable solutions to common software design problems that capture best practices and proven design approaches.
- **Common Design patterns:**

| Pattern | Category | Description |
| --- | --- | --- |
| **Singleton** | Creational | Ensures a class has only one instance and provides a global access point to it |
| **Factory** | Creational | Defines an interface for creating an object but lets subclasses decide which class to instantiate |
| **Abstract Factory** | Creational | Provides an interface for creating families of related or dependent objects without specifying their concrete classes |
| **Builder** | Creational | Separates the construction of a complex object from its representation, allowing the same construction process to create different representations |
| **Adapter** | Structural | Allows incompatible interfaces to work together by wrapping an existing class with a new interface |
| **Iterator** | Behavioral | Provides a way to access elements of a collection sequentially without exposing its underlying representation |
| **Observer** | Behavioral | Defines a one-to-many dependency so that when one object changes state, all its dependents are notified and updated automatically |
| **Strategy** | Behavioral | Defines a family of algorithms, encapsulates each one, and makes them interchangeable at runtime |

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Introduction to Computer Science and Java | Program, Programming, Algorithm, Unambiguous, Executable, Terminating, Java Attributes (Safety, Portability) |
| 2 | Fundamental Data Types and I/O | Variables, Primitive Types (int, double), Strings (Immutable), Operators (+, -, *, /, %), Printf, Scanner |
| 3 | Objects and Classes | Class, Object, Object Reference, Constructor, New Operator, Instance Variables, Methods, Accessor, Mutator, Public Interface, Static Methods, Static Fields, Java API Packages |
| 4 | Designing Classes | SRP, Encapsulation, Data Hiding, Data Abstraction, ADT, Cohesion, this keyword, Static Members, Access Modifiers, Arrays, Enhanced for Statement, Varargs, Command-Line Arguments, Inheritance, Overriding, super, Polymorphism, Dynamic Method Lookup, Abstract Class, Packages |
| 5 | Inheritance and Polymorphism | Subclass, Superclass, extends, Overriding, super, Polymorphism, Dynamic Method Lookup, Abstract Class |
| 6 | Interfaces | Interface, Contract, implements, Callbacks, Lambda Expressions, Functional Interface |
| 7 | Exception Handling and File I/O | try, throw, catch, finally, Checked Exceptions, Unchecked Exceptions, Scanner (File), PrintWriter, File Class, I/O Hierarchy, Text vs Binary Files, Sequential vs Random Access |
| 8 | Generics and Data Structures | Generic Class, Type Parameters, Type Erasure, Collections Framework, List, Set, Map |
| 9 | OOD and Design Patterns | Requirements, CRC Cards, UML, javadoc, GUI Design, Layout Managers, Singleton, Factory, Abstract Factory, Builder, Adapter, Iterator, Observer, Strategy |

---
*CSE 1221 — Object Oriented Programming | Dept. of CSE, University of Rajshahi*





