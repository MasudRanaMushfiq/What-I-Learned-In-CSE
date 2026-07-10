

# Database Management Systems

### Course Information
**Course:** CSE 3121 (Database Management Systems)
**Course Type:** Theory, 3 Credits | Contact Hours: 39 | Year: Third | Semester: Odd
**Prerequisite:** CSE2131 Discrete Mathematics
### Instructor
Mr. Md. Morshedul Arefin, Associate Professor, Dept. of CSE, University of Rajshahi


### Course Motivation
> To know basic of database design and implementation, database security, integrity and concurrency.

---

## Course Contents

| Area                                       | Topics Covered                                                                                                                                                                                                                                                                   |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Introduction**                           | Database system concept; Purpose of database system; View of data; Data models; Conventional file processing; Transaction management; Storage management; Database administrator.                                                                                                |
| **Database Model**                         | Entity-relationship model; Relational model, Network model; Hierarchical model, Database languages, Relational algebra, Integrity constraint, Generalization and Specialization, Developing an ER Diagram.                                                                       |
| **Structured Query Language**              | Basic Structure of SQL, String operations, Different set operations, Aggregate functions, Handling NULL values, Nested Subqueries, View definition, Modification of the Database: Deletion, Insertion and Update operations, Domain Types in SQL, Alteration of Table Structure. |
| **Database Design**                        | Functional dependencies and normal forms; Object-oriented databases; Distributed database; multimedia database, object-relational database, Intelligent database.                                                                                                                |
| **Transactions**                           | Introduction to transaction, ACID Properties, Transaction State, Schedule, Conflict Serializability and View Serializability.                                                                                                                                                    |


---

## Textbooks

**Primary Texts:**
1. A. Silberschatz — *Database System Concepts*, McGraw-Hill.
2. James Martin — *Principles of Database Management*, Prentice-hall Of India Pvt Ltd.

---

## Table of Contents

1. [Chapter 1 – Course Overview and Introduction](#chapter-1)
2. [Chapter 2 – View of Data and Abstraction](#chapter-2)
3. [Chapter 3 – The Relational Model](#chapter-3)
4. [Chapter 4 – Relational Algebra](#chapter-4)
5. [Chapter 5 – SQL (Structured Query Language)](#chapter-5)
6. [Chapter 6 – Database Design and the E-R Model](#chapter-6)
7. [Chapter 7 – Relational Database Design and Normalization](#chapter-7)
8. [Chapter 8 – Physical Storage and RAID](#chapter-8)
9. [Chapter 9 – Transaction Management](#chapter-9)

---

## Chapter 1
## Course Overview and Introduction

### 1.1 Course Overview
This comprehensive course note is synthesized from all provided sources, including textbooks, lecture notes, and assessment materials, to provide a detailed guide for Database Management Systems (DBMS).

A **Database-Management System (DBMS)** is a collection of interrelated data and a set of programs designed to access and manipulate that data. The primary objective of a DBMS is to provide a way to store and retrieve information that is both **convenient and efficient**. Databases are used to manage large bodies of highly valuable information, ensuring its safety despite system crashes or unauthorized access attempts.

### 1.2 Data vs. Information
- **Data:** Simply a value of real-world things or objects (concrete or abstract), such as a person's name or an account number.
- **Information:** The processed form of data that is meaningful and useful to users (e.g., a student's result sheet or CGPA).

### 1.3 Disadvantages of Traditional File-Processing Systems
Before DBMS, organizations stored records in conventional file systems, which led to several major drawbacks:
- **Data Redundancy and Inconsistency:** Different programmers creating files over time lead to duplicated data in several places, increasing storage costs and causing inconsistencies where various copies no longer agree.
- **Difficulty in Accessing Data:** Retrieving specific data requires writing new application programs for every new task.
- **Data Isolation:** Data is scattered in various files and formats.
- **Integrity Problems:** Enforcing consistency constraints (e.g., a bank balance not dropping below zero) is difficult.
- **Atomicity Problem:** A system failure may leave data in an inconsistent state (e.g., money deducted from one account but not credited to another).
- **Concurrent-Access Anomalies:** Multiple users modifying the same data simultaneously without control lead to inconsistent data.
- **Security Problems:** Difficulty in enforcing different access levels for different users.

### 1.4 Database Administrator (DBA)
The DBA is a person responsible for central control of the system.
- **Functions:** Schema definition, storage structure and access method definition, granting authorization for data access, and routine maintenance.

---

## Chapter 2
## View of Data and Abstraction

### 2.1 Three Levels of Data Abstraction
A major purpose of a DBMS is to provide users with an **abstract view** of data, hiding details of how it is stored.

| Level | Description |
|---|---|
| **Physical Level** | The lowest level describing how data is actually stored in physical memory (e.g., blocks of bytes). |
| **Logical Level (Conceptual Level)** | Describes what data is stored and what relationships exist among them. This level is used by programmers and DBAs. |
| **View Level** | The highest level describing only part of the entire database relevant to a specific user, removing complexity for common users. |

### 2.2 Schema and Instance
- **Schema:** The overall design of the database (similar to a variable declaration in programming).
- **Instance:** The actual collection of information stored in the database at a particular moment.

---

## Chapter 3
## The Relational Model

### 3.1 Structure of Relational Databases
The **Relational Model** is a table-based model where data is organized in rows and columns.
- **Attributes:** The column headers (e.g., *ID, name, salary*).
- **Tuples:** The rows representing individual records.
- **Relation:** A collection of tables.

### 3.2 Database Keys
Keys uniquely identify records in a table.

| Key Type | Definition |
|---|---|
| **Super Key** | A set of one or more attributes that collectively allow us to identify a tuple uniquely. |
| **Candidate Key** | A minimal super key (no proper subset is also a super key). |
| **Primary Key** | A candidate key chosen by the database designer to identify tuples within a relation. |
| **Foreign Key** | An attribute in one table that references the primary key of another table to maintain referential integrity. |

---

## Chapter 4
## Relational Algebra

**Relational Algebra** is a procedural query language consisting of a set of operations that take one or two relations as input and produce a new relation as a result.

### 4.1 Basic Operations

| Operation | Symbol | Description |
|---|---|---|
| **Select** | $\sigma$ | Selects tuples that satisfy a given predicate (row-wise operation). |
| **Project** | $\pi$ | Selects specific attributes (columns) from a relation. |
| **Union** | $\cup$ | Combines tuples from two relations. Relations must have the same arity and compatible domains. |
| **Set Difference** | $-$ | Finds tuples in one relation that are not in another. |
| **Cartesian Product** | $\times$ | Combines every tuple of one relation with every tuple of another. |
| **Rename** | $\rho$ | Assigns a name to the results of relational-algebra expressions. |

### 4.2 Additional/Derived Operations

| Operation | Symbol | Description |
|---|---|---|
| **Natural Join** | $\bowtie$ | A Cartesian product followed by a selection on common fields. |
| **Left Outer Join** | $\leftouterjoin$ | Natural join + remaining tuples from the left relation. |
| **Right Outer Join** | $\rightouterjoin$ | Natural join + remaining tuples from the right relation. |
| **Full Outer Join** | $\fullouterjoin$ | Natural join + all unmatched tuples from both relations. |
| **Division** | $\div$ | Used for queries involving the word "all" or "every". |

---

## Chapter 5
## SQL (Structured Query Language)

SQL is the most widely used commercial relational database language.

### 5.1 SQL Language Categories

| Category | Purpose | Commands |
|---|---|---|
| **Data Definition Language (DDL)** | Defines the schema and structure of tables | `CREATE, ALTER, DROP, TRUNCATE` |
| **Data Manipulation Language (DML)** | Enables users to access or manipulate data | `SELECT, INSERT, UPDATE, DELETE` |
| **Data Control Language (DCL)** | Manages user access and permissions | `GRANT, REVOKE` |
| **Transaction Control Language (TCL)** | Manages database transactions | `COMMIT, ROLLBACK, SAVEPOINT` |

### 5.2 Aggregate Functions
These functions take a collection of values and return a single summarized value.
- `avg`, `min`, `max`, `sum`, `count`.
- **Group By:** Used to group tuples with the same values on specified attributes.
- **Having:** Applies conditions to groups created by the `group by` clause.

---

## Chapter 6
## Database Design and the E-R Model

The **Entity-Relationship (E-R) Model** is a conceptual data modeling technique used to provide a visual representation of entities and their relationships.

### 6.1 Entity and Attributes
- **Entity:** A "thing" or "object" distinguishable from others (e.g., a specific student).
- **Attributes:** Descriptive properties of an entity (e.g., student name, roll).

| Attribute Type | Description | Example |
|---|---|---|
| **Composite Attribute** | Can be divided into subparts | Name into First, Middle, Last |
| **Multivalued Attribute** | Can have a set of values | phone numbers |
| **Derived Attribute** | Value calculated from other attributes | Age derived from Date of Birth |

### 6.2 Relationship Sets
An association among several entities.
- **Mapping Cardinality:** Expresses the number of entities to which another entity can be associated via a relationship.
    - One-to-one (1:1), One-to-many (1:M), Many-to-one (M:1), Many-to-many (M:M).

### 6.3 Weak Entity Sets
An entity set that does not have a primary key and depends on an **identifying entity set** for its identification. It is represented by a double rectangle in E-R diagrams.

### 6.4 Extended E-R Features

| Feature | Description |
|---|---|
| **Specialization** | A top-down approach where a general entity is divided into specific entities based on characteristics (Inheritance). |
| **Generalization** | A bottom-up approach where specific entities are combined into a more general entity to reduce redundancy. |
| **Aggregation** | An abstraction that treats a relationship between entities as a higher-level entity. |

---

## Chapter 7
## Relational Database Design and Normalization

Normalization is the process of decomposing larger tables into smaller ones to minimize redundancy and avoid anomalies (Insertion, Update, and Deletion).

### 7.1 Functional Dependency (FD)
A relationship between attributes where the value of one attribute (the determinant) determines the value of another.
- **Armstrong’s Axioms:** Primary rules for FD inference: Reflexivity, Augmentation, and Transitivity.

### 7.2 Normal Forms

| Normal Form | Key Requirement |
|---|---|
| **First Normal Form (1NF)** | All attributes must contain only atomic (single) values. |
| **Second Normal Form (2NF)** | Must be in 1NF and have no **partial dependency** (non-prime attributes must depend on the whole candidate key). |
| **Third Normal Form (3NF)** | Must be in 2NF and have no **transitive dependency**. |
| **Boyce-Codd Normal Form (BCNF)** | A stronger version of 3NF where for every non-trivial FD $X \to Y$, $X$ must be a super key. |
| **Fourth Normal Form (4NF)** | Deals with **multivalued dependencies**. |

---

## Decomposition

**Decomposition** is the process of breaking down a single, large, poorly designed table (relation) into two or more smaller, well-structured tables. The goal is to eliminate redundancy, avoid data anomalies (insertion, update, deletion anomalies), and achieve higher normal forms (like 2NF, 3NF, or BCNF).

> 📌 **Key Insight:** Decomposition is the practical implementation of normalization. When a table fails to meet the requirements of a normal form, you decompose it to fix the problem.

---

## Properties of a Good Decomposition

For a decomposition to be acceptable, it must satisfy two critical properties:

|Property|Meaning|
|---|---|
|**Lossless Join Decomposition**|When you join the decomposed tables back together, you must get back the **exact original table** — no extra rows and no missing rows.|
|**Dependency Preservation**|All functional dependencies (constraints) that existed in the original table must still be enforceable without joining the decomposed tables.|

> 💡 If a decomposition loses information upon rejoining, it is called a **lossy decomposition** (or lossy join), and it is never acceptable in database design.

---


## Chapter 8
## Physical Storage and RAID

Ultimately, data must be stored on physical devices like magnetic disks or flash-based SSDs.

### 8.1 RAID (Redundant Arrays of Independent Disks)
RAID provides increased performance and reliability by using multiple disks.

| RAID Level | Technique | Primary Benefit |
|---|---|---|
| **RAID 0** | Striping for performance | No redundancy; highest performance |
| **RAID 1** | Mirroring (duplicating data) | High reliability |
| **RAID 4** | Block-level striping with a dedicated parity disk | Efficient use of space with parity |
| **RAID 5** | Block-level striping with distributed parity | No single parity disk bottleneck |
| **RAID 10** | Combination of RAID 1 and RAID 0 (Mirroring then Striping) | Both performance and reliability |

---

## Chapter 9
## Transaction Management

A **Transaction** is a set of operations that perform a single logical unit of work.

### 9.1 ACID Properties
To ensure database integrity, transactions must follow ACID properties:

| Property | Description |
|---|---|
| **Atomicity** | "All or none" – every operation must succeed or the whole transaction fails. |
| **Consistency** | The database remains in a consistent state before and after the transaction. |
| **Isolation** | Transactions occur independently without interference. |
| **Durability** | Once committed, changes are permanent even in case of system failure. |

### 9.2 Transaction States
Active $\to$ Partially Committed $\to$ Committed (Success) OR Active $\to$ Failed $\to$ Aborted (Failure).

---

## Important Concepts & Definitions

- **Metadata:** Data about data (e.g., the structure of a table).
- **Trigger:** A statement that the system executes automatically as a side effect of a modification (Insert, Update, Delete) to the database.
- **View:** A virtual table based on a stored query; it does not exist physically.
- **Data Mining:** The process of discovering hidden patterns and knowledge from large datasets.
- **Big Data:** Extremely large datasets characterized by high Volume, Velocity, and Variety.

---

## Key Examples

### Technical Example: SQL Table Creation
```sql
CREATE TABLE student (
    Roll INT PRIMARY KEY,
    Name VARCHAR(20) NOT NULL,
    GPA FLOAT(3,2)
);
```


### Technical Example: Triggers

A trigger to move deleted employee records to a recycle bin:

```sql
CREATE TRIGGER move_to_bin BEFORE DELETE ON employee
FOR EACH ROW
BEGIN
    INSERT INTO recycle_bin VALUES (OLD.id, OLD.name, OLD.email);
END;
```

### Technical Example: Normalization (2NF)

If a relation R(A,B,C,D)R(A,B,C,D) has FD={AB→CD,C→A,D→B}FD={AB→CD,C→A,D→B}, and ABAB is the candidate key, there is no partial dependency because non-prime attributes C,DC,D depend on the whole key ABAB. Thus, it is in 2NF.

---

## Quick Reference Summary

|Topic|Key Takeaways|
|---|---|
|**DBMS Goals**|Convenience, efficiency, security, and data integrity.|
|**Database Design Flow**|Real-world requirements →→ E-R Diagram →→ Relational Schema →→ Normalization →→ Physical Implementation.|
|**Normalization Rules**|1NF (Atomic), 2NF (No partial dependency), 3NF (No transitive dependency), BCNF (LHS must be Superkey).|
|**Transaction Checklist**|ACID properties must always be maintained.|
|**RAID Quick Guide**|Use RAID 0 for speed, RAID 1 for safety, RAID 5/6 for a balance of both.|

---
_CSE 3121 — Database Management Systems | Dept. of CSE, University of Rajshahi_





