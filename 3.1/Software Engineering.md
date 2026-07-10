

# Software Engineering

### Course Information
**Course:** CSE 3111 (Software Engineering)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE1221: Object Oriented Programming, CSE2121: Data Structure, CSE2221: Design and Analysis of Algorithms
### Instructor
Mr. Kazi Jahidur Rahman, Assistant Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To show the skills and processes needed to complement technical understanding of software products in order to make you a more effective software developer in an engineering team.

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Introduction** | Introduction to software engineering, Importance of software, The Software evolution, Software characteristics, Software components, Software applications, Crisis-Problem and causes |
| **Software development life-cycle** | Requirement Engineering, Design, Coding, Testing, Deployment and Maintenance etc. |
| **Software Process Model** | Waterfall Process, Spiral Process, Evolutionary Prototyping Process, Rational Unified Process, Agile Process, Unified Software Process, Choosing a Model, Lifecycle Documents |
| **Requirement Engineering** | General Definition, Software Intensive Systems, Functional and Nonfunctional Requirements, User and System Requirements, Problem analysis, requirement specification, validation, matrices, monitoring and control, Gathering Requirements: The agile way, User Stories: The currency of agile development, Characteristics of good user stories, Generating User Stories, Modeling Requirements, Analyzing Requirements, Requirements Prioritization, Requirements Engineering Process, Agile Estimation and Planning, Estimation Styles and Process, Velocity, Release Planning, Release Tracking |
| **System Design** | Problem partitioning, abstraction, Cohesiveness, coupling, structured approach, functional versus object-oriented approach, UML Structural Diagrams: Class Diagrams, Component Diagram, Deployment Diagram, UML Behavioral Diagram: Use Case, Sequence, and State Transition Diagram, Software Architecture, Prescriptive vs. Descriptive Architecture, Architectural Evolution, Architectural Degradation, Architectural Recovery, Architectural Elements, Components, Connectors, and Configuration, Deployment Architectural Perspective, Analyzing Requirements, Refining Classes and Attributes, Adding Attributes, Identifying Operations, Refining the Class Diagram |
| **Coding** | TOP-DOWN and BOTTOM-UP structure programming, information hiding, programming style, and internal documentation, verification, metrics, monitoring and control, Software Refactoring: Reasons to Refactor, Refactoring Risks, Cost of Refactoring, When Not to Refactor |
| **Software Testing** | Failure, Fault and Error, Verification Approaches, Pros and Cons of Approaches, Testing Granularity Levels, Alpha and Beta Testing, Black and White Box Testing Introduction, Black-Box Testing: Systematic Functional Testing Approach, Test Data Selection, Category Partition Method, Produce and Evaluate Test Case Specifications, Generate Test Cases from Test Case Specifications, Model Based Testing, Finite State Machines, White-Box Testing: Coverage Criteria, Statement Coverage, Control Flow Graphs, Test Criteria Sub-Sumption, MC/DC Coverage, test plan, test case specification, Software testing strategies, Verification and validation, Unit and Integration Testing, Alpha and Beta testing, System testing and debugging |
| **Deployment and maintenance** | What is deployment? Is deployment the problem? Key issues around deployment, Deployment itself, Continuous Integration and Deployment, Maintenance, Maintenance challenges, Software evolution and release management, Re-engineering |


## Textbooks

**Primary Texts:**
1. Roger S. Pressman — *Software Engineering, A practitioner's Approach*, McGraw-Hill
2. Ian Sommerville — *Software Engineering*, Pearson Education

---

## Table of Contents

1. [Chapter 1 – Introduction to Software Engineering](#chapter-1)
2. [Chapter 2 – Software Development Life Cycle and Process Models](#chapter-2)
3. [Chapter 3 – Requirement Engineering](#chapter-3)
4. [Chapter 4 – System Design](#chapter-4)
5. [Chapter 5 – Coding](#chapter-5)
6. [Chapter 6 – Software Testing](#chapter-6)
7. [Chapter 7 – Deployment and Maintenance](#chapter-7)

---

## Chapter 1
## Introduction to Software Engineering

### 1.1 Fundamental Concepts

**Introduction to software engineering:** Software engineering is the systematic, disciplined, and measurable approach to the development, operation, and maintenance of software.

**Importance of software:** Software is important because it controls, manages, and enhances almost every aspect of modern life, from business and healthcare to transportation and entertainment.

**The Software evolution:** Software evolution refers to the process of initially developing a software product and then repeatedly updating it for reasons such as changing requirements, fixing bugs, adapting to new environments, and adding new features.

**Software characteristics:** Software has the following characteristics:
- It is developed or engineered, not manufactured in a classical sense.
- It does not wear out over time like hardware, but it can deteriorate due to changes (maintenance) that introduce errors.
- It is mostly custom-built rather than assembled from existing components.

**Software components:** Software components are the building blocks of a software system; they include source code modules, libraries, data structures, configuration files, and documentation.

**Software applications:** Software applications include system software (operating systems, compilers), application software (word processors, spreadsheets), embedded software (firmware in devices), scientific software, web applications, artificial intelligence software, and more.

### 1.2 The Software Crisis

**Crisis-Problem and causes:** The software crisis refers to the difficulty of writing bug-free, on-time, within-budget software that meets user requirements.

**Causes of the software crisis:**
- Increasing complexity of software systems
- Poor project planning and estimation
- Lack of disciplined development processes
- Inadequate documentation
- Unclear or constantly changing requirements
- Difficulty in software maintenance and evolution

---

## Chapter 2
## Software Development Life Cycle and Process Models

### 2.1 Software Development Life Cycle (SDLC)

**Software development life-cycle:** The software development life cycle (SDLC) is a framework that defines the stages involved in developing a software system, from initial feasibility study to final deployment and maintenance.

**Requirement Engineering:** The first phase where requirements are gathered, analyzed, documented, and validated.

**Design:** The phase where the software architecture and detailed design are created based on requirements.

**Coding:** The phase where the design is translated into executable source code.

**Testing:** The phase where the software is executed with test cases to find faults and ensure it meets requirements.

**Deployment:** The phase where the software is delivered to the customer and installed in the target environment.

**Maintenance:** The phase where the software is modified after deployment to fix bugs, adapt to new environments, or add new features.

**etc.:** Other activities in the life cycle include project management, configuration management, and quality assurance.

---

### 2.2 Software Process Models

**Software Process Model:** A software process model is an abstract representation of a software development process, describing the sequence of phases, activities, and their relationships.

**Waterfall Process:** The waterfall process is a sequential, non-iterative process model where each phase (requirements, design, coding, testing, deployment, maintenance) is completed fully before the next phase begins.

**Spiral Process:** The spiral process is an iterative, risk-driven model that combines elements of prototyping and waterfall. Each loop in the spiral consists of: objective setting, risk assessment, development and validation, and planning for the next iteration.

**Evolutionary Prototyping Process:** In the evolutionary prototyping process, an initial prototype is built, then refined through multiple iterations based on user feedback, gradually evolving into the final system.

**Rational Unified Process (RUP):** The Rational Unified Process is a phased, iterative process framework that divides the project into four phases: Inception, Elaboration, Construction, and Transition, each ending with a milestone.

**Agile Process:** Agile processes focus on short iterations (sprints), small releases, continuous customer involvement, and responding to change over following a rigid plan.

**Unified Software Process (UP):** The Unified Software Process is a generic, use-case-driven, architecture-centric, iterative and incremental software process framework, of which RUP is a specific instance.

**Choosing a Model:** Choosing a model depends on project size, complexity, risk level, requirement stability, customer involvement, and team experience. Waterfall works for stable requirements, spiral for high-risk projects, agile for rapidly changing needs.

**Lifecycle Documents:** Lifecycle documents include the Software Requirements Specification (SRS), Software Design Document (SDD), test plan, test cases, user manual, deployment guide, and maintenance records.

---

## Chapter 3
## Requirement Engineering

### 3.1 Fundamentals of Requirements

**General Definition:** A requirement is a condition or capability that a software system must have to solve a user problem or achieve a contract standard.

**Software Intensive Systems:** Systems where software contributes essential influence on the design, construction, deployment, and evolution of the overall system (e.g., avionics, medical devices, telecommunications).

**Functional and Nonfunctional Requirements:**
- **Functional requirements** describe what the system should do (e.g., "The system shall allow a user to log in").
- **Nonfunctional requirements** describe constraints or qualities of the system (e.g., performance, security, usability, maintainability).

**User and System Requirements:**
- **User requirements** are high-level statements in natural language, often with diagrams, about what the system should do for users.
- **System requirements** are detailed, structured specifications of the system's functions, services, and operational constraints.

**Problem analysis:** The process of understanding the customer's underlying needs, business processes, and constraints before writing requirements.

**Requirement specification:** The activity of writing the Software Requirements Specification (SRS) document that organizes functional and non-functional requirements.

**Validation:** The process of checking that the documented requirements accurately reflect the customer's true needs and are feasible, consistent, and testable.

**Matrices:** Requirements traceability matrices are tables that link requirements to their origin (stakeholder needs) and to subsequent artifacts (design, code, tests) to track coverage and impact.

**Monitoring and control:** Continuously tracking requirement status, changes, and ensuring that implementation stays aligned with approved requirements.

---

### 3.2 Agile Requirements

**Gathering Requirements: The agile way:** In agile development, requirements are gathered incrementally through direct user collaboration, user stories, and frequent feedback loops rather than a massive upfront specification.

**User Stories: The currency of agile development:** A user story is a short, simple description of a feature told from the perspective of the user who wants the new capability. It follows the format: "As a [type of user], I want [some goal] so that [some reason]."

**Characteristics of good user stories:** Good user stories are **INVEST**: Independent, Negotiable, Valuable, Estimatable, Small, and Testable.

**Generating User Stories:** User stories are generated through user interviews, workshops, brainstorming, personas, and story-writing sessions with the product owner and development team.

**Modeling Requirements:** Modeling requirements means creating visual representations (use case diagrams, activity diagrams, state machines) to clarify and analyze functional and nonfunctional needs.

**Analyzing Requirements:** Requirements analysis involves checking for conflicts, ambiguities, missing information, feasibility, and prioritizing different stakeholder requests.

**Requirements Prioritization:** Prioritization uses methods like MoSCoW (Must-have, Should-have, Could-have, Won't-have) or ranking to decide which requirements are implemented in which release.

**Requirements Engineering Process:** The requirements engineering process includes: feasibility study, elicitation, analysis, specification, validation, and management.

**Agile Estimation and Planning:** Agile teams estimate the size and effort of user stories using relative units (story points) rather than hours.

**Estimation Styles and Process:** Estimation styles include planning poker, affinity estimation, and the bucket system; the process involves the whole team discussing each story and reaching consensus on its size.

**Velocity:** Velocity is the average number of story points (or hours) a team completes per sprint; it is used to forecast how many sprints are needed for future work.

**Release Planning:** Release planning in agile means selecting a set of user stories for an upcoming release, ordering them by priority, and using velocity to predict the release date.

**Release Tracking:** Release tracking involves monitoring progress against the release plan using burndown charts, burnup charts, and iteration backlog tracking.

---

## Chapter 4
## System Design

### 4.1 Design Principles

**Problem partitioning:** Problem partitioning is the technique of dividing a large, complex software problem into smaller, more manageable pieces (modules or components).

**Abstraction:** Abstraction focuses on the essential characteristics of a software element while ignoring irrelevant details; it reduces complexity by providing a simplified model.

**Cohesiveness:** Cohesion is the degree to which the elements inside a single module belong together. High cohesion (functional cohesion) is desirable; low cohesion means the module does many unrelated things.

**Coupling:** Coupling is the degree of interdependence between software modules. Low coupling (data coupling) is desirable; high coupling (content coupling) makes the system hard to change.

**Structured approach:** The structured approach uses top-down design, flowcharts, and function-oriented decomposition (e.g., Data Flow Diagrams and Structure Charts).

**Functional versus object-oriented approach:**
- **Functional approach** focuses on functions (processes) that transform input to output; data is passive.
- **Object-oriented approach** focuses on objects that combine data and behaviour (methods); functions are encapsulated within objects.

---

### 4.2 UML Diagrams (Unified Modeling Language)

**UML Structural Diagrams: Class Diagrams:** A class diagram shows the static structure of a system: classes, their attributes, methods, and the relationships (inheritance, association, aggregation, composition) between classes.

**UML Structural Diagrams: Component Diagram:** A component diagram shows how the system's physical components (JAR files, DLLs, executables, source files) are organized and depend on each other.

**UML Structural Diagrams: Deployment Diagram:** A deployment diagram shows the physical hardware nodes (servers, workstations, devices) and where software components are placed on those nodes.

**UML Behavioral Diagram: Use Case:** A use case diagram shows actors (users or external systems) and the use cases (functionalities) they interact with, illustrating system boundaries and high-level requirements.

**UML Behavioral Diagram: Sequence:** A sequence diagram shows the interaction between objects over time, using lifelines, messages, and activation boxes to represent a specific scenario.

**UML Behavioral Diagram: State Transition Diagram:** A state transition diagram shows the finite states an object can be in, the events that cause transitions, and the actions that occur during state changes.

---

### 4.3 Software Architecture

**Software Architecture:** Software architecture is the fundamental organization of a system, embodied in its components, their relationships to each other and to the environment, and the principles guiding its design and evolution.

**Prescriptive vs. Descriptive Architecture:**
- **Prescriptive architecture** is the architecture as planned and documented (the ideal).
- **Descriptive architecture** is the architecture as actually implemented (the reality). The gap between them is called architectural drift.

**Architectural Evolution:** The gradual, planned change of a software system's architecture over time in response to new requirements, technology, or business goals.

**Architectural Degradation:** The unplanned, undesirable deterioration of architecture when developers make shortcuts, bypass intended structures, or add features without following the design.

**Architectural Recovery:** The process of reverse-engineering the existing source code to produce a representation (usually diagrams) of the current "as-built" architecture.

**Architectural Elements:**
- **Components:** The core functional units that encapsulate processing and data.
- **Connectors:** The communication mechanisms (procedure calls, events, pipes, message queues) that link components.
- **Configuration:** The topology of components and connectors that shows how they are arranged and interact.

**Deployment Architectural Perspective:** The deployment perspective describes how the architecturally significant components are assigned to nodes (hardware, cloud instances, containers) in the physical runtime environment.

**Analyzing Requirements:** During design, requirements are analyzed again to ensure the proposed architecture satisfies functional and nonfunctional needs (e.g., performance, security).

**Refining Classes and Attributes:** In OO design, initial analysis classes are refined by adding more detail, splitting large classes, and clarifying responsibilities.

**Adding Attributes:** Attributes (data members) that were missing in analysis are added to classes to support the required functionality.

**Identifying Operations:** Operations (methods) are identified from interaction diagrams, use case descriptions, and state models, specifying their parameters, return types, and visibility.

**Refining the Class Diagram:** The class diagram is refined by adding more relationships, multiplicities, constraints, navigation directions, and design patterns.

---

## Chapter 5
## Coding

### 5.1 Coding Fundamentals

**TOP-DOWN and BOTTOM-UP structure programming:**
- **TOP-DOWN programming** starts with the main routine and decomposes it into lower-level subroutines; it focuses on high-level logic first.
- **BOTTOM-UP programming** starts with low-level utility functions and components, then assembles them into higher-level routines.

**Information hiding:** Information hiding is the principle of hiding the internal details of a module behind a public interface, so that changes inside the module do not affect other modules.

**Programming style:** Programming style includes consistent indentation, meaningful variable names, avoidance of overly complex expressions, and following language-specific conventions.

**Internal documentation:** Internal documentation consists of comments within the source code that explain why a piece of code does something, preconditions/postconditions, and any non-obvious logic.

**Verification:** In coding, verification means checking that the code correctly implements the design and meets its requirements, often through code reviews, walkthroughs, or static analysis.

**Metrics:** Coding metrics include lines of code (LOC), cyclomatic complexity, comment density, and defect density, used to measure size, complexity, and quality.

**Monitoring and control:** Monitoring involves tracking code completeness, bug counts, and schedule adherence; control means taking actions (e.g., adding resources, adjusting scope) if targets are not met.

---

### 5.2 Software Refactoring

**Software Refactoring: Reasons to Refactor:** Reasons to refactor include: to remove duplicate code, to simplify complex methods, to improve naming, to make adding new features easier, and to pay down technical debt.

**Refactoring Risks:** Refactoring risks include: introducing new bugs, breaking existing functionality, time spent on refactoring instead of new features, and potential mismatch with external interfaces.

**Cost of Refactoring:** The cost includes developer time, potential regression testing, documentation updates, and possible delays to release schedules.

**When Not to Refactor:** Do not refactor when the code is extremely close to a deadline, when the module is about to be replaced, when the cost of testing outweighs the benefit, or when the system is too unstable.

---

## Chapter 6
## Software Testing

### 6.1 Testing Fundamentals

**Failure, Fault and Error:**
- **Error:** A human mistake made in understanding requirements, designing, or coding.
- **Fault (Bug):** The manifestation of an error in the software artifact (e.g., a wrong line of code).
- **Failure:** The observable incorrect behavior of the software when a fault is executed.

**Verification Approaches:** Verification asks "Are we building the product right?" Approaches include reviews, walkthroughs, inspections, and static analysis (without executing code).

**Validation Approaches:** Validation asks "Are we building the right product?" Approaches include all forms of testing (dynamic execution with test cases).

**Pros and Cons of Approaches:**
- **Static (Reviews):** Pros: finds faults early, improves understanding, low cost. Cons: cannot find all runtime errors, heavy documentation, human fatigue.
- **Dynamic (Testing):** Pros: finds actual execution failures, gives confidence, scalable. Cons: can only show presence of bugs, not absence; requires test harness.

**Testing Granularity Levels:**
- **Unit testing:** Tests individual modules (smallest part).
- **Integration testing:** Tests interactions between modules.
- **System testing:** Tests the entire integrated system.
- **Acceptance testing:** Tests from end-user perspective, often by customer.

**Alpha and Beta Testing:**
- **Alpha testing** is performed by internal developers or testers in a controlled environment, often at the developer's site.
- **Beta testing** involves releasing the software to a limited external audience (real users) in their own environment to get feedback before full release.

**Black and White Box Testing Introduction:**
- **Black-box testing** designs test cases based only on the specification (inputs and expected outputs) without looking at internal code.
- **White-box testing** designs test cases based on the internal structure, logic, and code paths.

---

### 6.2 Black-Box Testing Techniques

**Black-Box Testing: Systematic Functional Testing Approach:** Start from requirements and specifications, partition input and output domains, select representative test cases, and design test procedures.

**Test Data Selection:** Test data is selected using equivalence partitioning (divide input domain into classes where all values behave the same) and boundary value analysis (test edges of equivalence classes).

**Category Partition Method:** The category-partition method is a systematic functional testing approach where you identify categories of input conditions, partition each category into choices, and then combine choices into test case specifications.

**Produce and Evaluate Test Case Specifications:** Write a test case specification that includes: test case ID, objective, input data, execution steps, expected outputs, and pass/fail criteria. Evaluate specifications for completeness and feasibility.

**Generate Test Cases from Test Case Specifications:** Transform the textual specifications into concrete test cases with actual values, scripts, and environment setup instructions.

**Model Based Testing:** Model-based testing creates a formal model (state machine, activity diagram) of the system's behaviour, then automatically generates test cases to cover transitions, states, or paths in that model.

**Finite State Machines (FSM):** An FSM is a model consisting of states, transitions, events, and actions; it is used in model-based testing to generate test cases that cover all states or transitions.

---

### 6.3 White-Box Testing Techniques

**White-Box Testing: Coverage Criteria:** Coverage criteria are measurable rules that define how much of the code's structure must be exercised by the test suite (e.g., statements, branches, paths).

**Statement Coverage:** Statement coverage requires that every executable statement in the code is executed at least once by some test case.

**Control Flow Graphs (CFG):** A CFG is a graphical representation of a program's control flow using nodes (basic blocks or statements) and edges (possible transfers of control between nodes).

**Test Criteria Sub-Sumption:** A test criterion C1 subsumes C2 if every test set that satisfies C1 also satisfies C2. For example, branch coverage subsumes statement coverage.

**MC/DC Coverage (Modified Condition/Decision Coverage):** MC/DC is a coverage criterion used in safety-critical systems that requires: each condition independently affects the decision outcome; each condition has taken both true and false; and the decision has taken both true and false.

**Test plan:** A test plan is a document describing the scope, approach, resources, schedule, and deliverables of testing activities. It includes objectives, test items, features to be tested, features not to be tested, pass/fail criteria, and staffing.

**Test case specification:** A test case specification is a detailed document for a specific test case, containing: identifier, test item, input specifications, output specifications, environmental needs, and procedural steps.

**Software testing strategies:** Strategies include: big-bang integration (test everything together), top-down integration (test from main downwards), bottom-up integration (test low-level units first), and regression testing (re-run old tests after changes).

**Verification and validation:** Verification (static, reviews) ensures correctness of artifacts relative to previous stage; validation (dynamic, testing) ensures the system meets customer requirements.

**Unit and Integration Testing:**
- **Unit testing** tests individual components in isolation, often using stubs and drivers.
- **Integration testing** tests combined components incrementally to find interface faults.

**System testing and debugging:**
- **System testing** tests the fully integrated system against the SRS; includes functional, performance, security, usability, and stress testing.
- **Debugging** is the process of locating and fixing a detected fault (bug) after a test case causes a failure.

---

## Chapter 7
## Deployment and Maintenance

### 7.1 Deployment

**What is deployment?** Deployment is the process of delivering, installing, configuring, and making a software system operational in its target environment (production).

**Is deployment the problem?** Deployment is often a problem because of environment differences (development vs. production), configuration complexity, data migration needs, and coordination with external systems.

**Key issues around deployment:** Key issues include: environment consistency (containerization helps), rollback plans, downtime management, data migration, version compatibility, user training, and release coordination.

**Deployment itself:** Deployment includes activities: packaging the software (build artifacts), setting up infrastructure (servers, databases), transferring artifacts to production, running installation scripts, configuring the runtime parameters, and smoke testing.

**Continuous Integration and Deployment (CI/CD):**
- **Continuous Integration (CI):** Developers frequently merge code into a shared repository; each merge triggers automated build and test.
- **Continuous Deployment (CD):** Every successful build that passes all tests is automatically deployed to production (or staging) without manual intervention.

---

### 7.2 Maintenance

**Maintenance:** Software maintenance is the modification of a software product after delivery to correct faults, improve performance or other attributes, or adapt to a changed environment.

**Maintenance challenges:** Challenges include: lack of up-to-date documentation, intrusion of the original developers, aging code (legacy systems), regression risk, and maintaining backward compatibility.

**Software evolution and release management:** Software evolution covers the entire lifecycle of continuous change. Release management plans, schedules, builds, tests, and deploys new versions (releases) that incorporate both bug fixes and new features.

**Re-engineering:** Software re-engineering is the process of examining, understanding, and restructuring an existing system to improve its maintainability, reusability, or quality without changing its external behaviour. It often includes reverse engineering, restructuring, and forward engineering.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Introduction to Software Engineering | Software evolution, crisis, characteristics, components, applications |
| 2 | SDLC and Process Models | Waterfall, Spiral, Prototyping, RUP, Agile, UP, Lifecycle Documents |
| 3 | Requirement Engineering | Functional/Nonfunctional, User/System, Validation, User Stories, INVEST, Velocity, Release Tracking |
| 4 | System Design | Cohesion, Coupling, UML (Class, Component, Deployment, Use Case, Sequence, State), Architectural degradation, Connectors |
| 5 | Coding | TOP-DOWN, BOTTOM-UP, information hiding, Refactoring reasons and risks |
| 6 | Software Testing | Failure/Fault/Error, Alpha/Beta, Black-box (Category partition, FSM), White-box (MC/DC, CFG), Test plan |
| 7 | Deployment and Maintenance | CI/CD, Maintenance challenges, Re-engineering, Release management |

---
*CSE 3111 — Software Engineering | Dept. of CSE, University of Rajshahi*




