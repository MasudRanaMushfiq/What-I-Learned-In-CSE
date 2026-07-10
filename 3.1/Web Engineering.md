

# Web Engineering

### Course Information
**Course:** CSE 3131 (Web Engineering)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE2252 (Web Application Development Lab)
### Instructor
Mr. A. F. M. Mahbubur Rahman, Associate Professor, Dept. of CSE, University of Rajshahi

### Course Motivation
> To provide students with conceptual and practical knowledge, and skills required to develop web applications and web services.

---

## Course Contents

| Area                                | Topics Covered                                                                                                                                                                                                                                                          |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Web Engineering Fundamentals**    | Attributes of Web based system and Application, Web App Engineering Layers, Web Engineering Process                                                                                                                                                                     |
| **Web App Project Management**      | Formulation Web based Systems, Planning for Web Engineering Project, Building Web Engineering Team, Web App Project Management, Metrics for web engineering and Apps                                                                                                    |
| **Web Apps Analysis**               | Requirement Analysis, Analysis Model, Web Apps Estimation, Content Model                                                                                                                                                                                                |
| **Web Apps Design**                 | Design issues of Web Apps, Interface Design, Typography, Layout design, Aesthetic Design, Content Design, Architecture Design, Navigation Design, Object Oriented Hypermedia Design, Design Metrics for web Apps                                                        |
| **Web Apps Implementation**         | Client side scripting: Java Script, AJAX, PHP; Framework: PHP MVC frameworks                                                                                                                                                                                            |
| **Web Apps Security**               | Encryption techniques (digital signatures, certificates), Security threats, Securing client/server interactions, Vulnerabilities at the client (desktop security, phishing, etc.) and the server (cross-site scripting, SQL injections, etc.), Building Secure Web Apps |
| **Maintenance of Web Applications** | Web Server and Database server load balancing, web apps performance assessment, Application usage monitoring and report generation                                                                                                                                      |

## Textbooks

**Primary Texts:**
1. Roger Pressman and David Lowe — *Web Engineering*, Tata McGraw Hill Edition, 2008
2. Web Security for Developers: Real Threats, Practical Defense — Malcolm McDonald

---

## Table of Contents

1. [Chapter 1 – Introduction to Web-Based Systems and Web Engineering](#chapter-1)
2. [Chapter 2 – Web App Project Management](#chapter-2)
3. [Chapter 3 – Web Apps Analysis](#chapter-3)
4. [Chapter 4 – Web Apps Design](#chapter-4)
5. [Chapter 5 – Web Apps Implementation](#chapter-5)
6. [Chapter 6 – Web Apps Security](#chapter-6)
7. [Chapter 7 – Maintenance of Web Applications](#chapter-8)

---

## Chapter 1
## Introduction to Web-Based Systems and Web Engineering

### 1.1 Web Engineering Fundamentals

**Web Engineering (WebE):** Web Engineering is a systematic and disciplined approach to the development, deployment, and maintenance of high-quality Web Applications (WebApps). Unlike traditional software engineering, WebE emphasizes agility, rapid development cycles, and the unique characteristics of the web, such as network-intensiveness and content-driven architecture. Students will progress through the entire System Development Life Cycle (SDLC)—from project initiation and requirements gathering to modeling, construction using modern tools like PHP and Laravel, and finally testing, security, and deployment.

**Attributes of Web based system and Application:** WebApps are a category of computer software that evolved from simple informational websites into complex systems providing significant functionality and customized content.

**WebApp Categories:**
- **Document-Centric:** Static HTML documents; predecessors of modern apps.
- **Interactive:** Use CGI and forms to generate dynamic pages based on user input.
- **Transactional:** Highly data-driven; allow users to update databases (e.g., e-commerce, banking).
- **Workflow-Based:** Automate internal or B2B processes (e.g., e-government portals).
- **Semantic Web:** Presents data in machine-readable forms (RDF, OWL) to support intelligent search and knowledge management.

**Product-Related Characteristics:**
- **Hyper-text:** Basis for non-linear information structuring using Nodes (info units), Links (paths), and Anchors.
- **Presentation Elements:** Success often depends on Aesthetics (look-and-feel) and Self-explanation (usability without documentation).

### 1.2 The Web Engineering Process

**Web App Engineering Layers:** The engineering layers for WebApps include the process framework (communication, planning, modeling, construction, deployment) supported by foundational technologies and methodologies.

**Web Engineering Process:** The Web Engineering process is comprised of five core activities: Communication, Planning, Modeling, Construction, and Deployment.

**Incremental Process Flow:** Because requirements evolve frequently and timelines are short, WebApps are delivered in increments. Each increment goes through the full framework and delivers a specific set of features.

**Agility Principles:** WebE teams adopt Agile Manifestos, prioritizing customer satisfaction, frequent delivery of working software, and face-to-face communication over lengthy documentation.

---

## Chapter 2
## Web App Project Management

### 2.1 Project Formulation and Planning

**Formulation Web based Systems:** Formulation is the entry point of the process where stakeholders and developers build a shared understanding of purpose and scope for the web-based system.

**Planning for Web Engineering Project:** Planning involves creating a task table that matches framework tasks to specific content objects and functions, followed by macroscopic scheduling.

**Building Web Engineering Team:** Building a Web Engineering team requires identifying roles such as project manager, content developer, web designer, front-end developer, back-end developer, tester, and security specialist.

**Web App Project Management:** Web App Project Management encompasses project planning, change control, risk management, schedule tracking, and quality assurance specifically for web-based projects.

**Metrics for web engineering and Apps:** Metrics for web engineering include size metrics (number of pages, number of use cases), complexity metrics (fan-in/fan-out for web components), and quality metrics (page load time, defect density).

---

### 2.2 Task Tables and Scheduling

**Task Tables:** Planning involves creating a matrix that matches framework tasks to specific content objects and functions.

**Macroscopic Schedule:** An ordered list of increments (e.g., Increment 1: Basic Info; Increment 2: Product Downloads) mapped against a timeline.

**Change Control:** Requested changes are categorized into classes (1-4) based on impact, with major changes requiring stakeholder review.

> 📌 **Task Table Example:** A team developing a news site creates a matrix where "Review User Scenarios" (Task) is checked against "Basic News Articles" (Function) and "Search Results" (Content).

> 💡 **Incremental News Site Delivery:** 
> - **Increment 1**: Core news display and search functionality.
> - **Increment 2**: User accounts and commenting systems.

---

## Chapter 3
## Web Apps Analysis

### 3.1 Requirements and Analysis Modeling

**Requirement Analysis:** Requirement analysis is the activity of gathering, eliciting, documenting, and validating the functional and non-functional needs of a WebApp from stakeholders.

**User Categories:** Defining user classes (e.g., Guest, Registered User, Admin) by their objectives, background, and how they arrive at the site.

**Elicitation Techniques:**
- **Interviews:** Structured or unstructured sessions to gather goals.
- **Joint Application Development (JAD):** Highly structured workshops with facilitators and stakeholders.
- **Usage Scenarios (Use Cases):** Narrative descriptions of how a user interacts with a specific WebApp function.

**Analysis Model:** The analysis model for WebApps consists of four complementary models: The Content Model, The Interaction Model, The Functional Model, and The Configuration Model.

**Web Apps Estimation:** Estimation for WebApps involves predicting project effort, cost, and schedule using metrics like number of pages, number of use cases, number of content objects, and estimated complexity per increment.

---

### 3.2 The Four Analysis Models

**The Content Model:** Identifies the full spectrum of content (text, graphics, video) and Analysis Classes—user-visible entities manipulated during interaction.

**Content Object:** A named collection of related information (e.g., a product specification including text, photos, and video).

**The Interaction Model:** Uses Use Cases, Sequence Diagrams, and State Diagrams to describe user-system "conversations".

**The Functional Model:** Defines operations applied to content and processing functions independent of content.

**The Configuration Model:** Describes the infrastructure (hardware/network) where the WebApp resides.

---

## Chapter 4
## Web Apps Design

### 4.1 Design Fundamentals and Issues

**Design issues of Web Apps:** Design issues for WebApps include: usability, consistency, navigation clarity, content organization, aesthetic appeal, cross-platform compatibility, performance, security, and scalability.

**Interface Design:** Interface design focuses on the layout and arrangement of elements that users directly interact with, ensuring intuitive and efficient task completion.

**Typography:** Typography in web design involves the selection of fonts, font sizes, line heights, and spacing to enhance readability and convey visual hierarchy.

**Layout design:** Layout design arranges visual elements (headers, footers, sidebars, content areas) on a web page to guide user attention and support content structure.

**Aesthetic Design:** Aesthetic design focuses on color schemes, visual harmony, branding, and emotional appeal to create a pleasing user experience.

**Content Design:** Content design structures the presentation of textual, graphical, and multimedia elements to maximize clarity, scannability, and communication effectiveness.

**Architecture Design:** Architecture design defines the high-level structure of the WebApp, including both conceptual and technical architecture.

**Navigation Design:** Navigation design defines how users move between pages and content objects, including menus, links, breadcrumbs, and search mechanisms.

**Object Oriented Hypermedia Design:** Object Oriented Hypermedia Design (OOHDM) is a method for designing WebApps using object-oriented principles, with steps: Conceptual Design, Navigation Design, Abstract Interface Design, and Implementation.

**Design Metrics for web Apps:** Design metrics for WebApps include: cohesion (how well elements within a module relate), coupling (degree of interdependence between modules), fan-in (number of modules that call a given module), fan-out (number of subordinates a module calls), and page complexity.

---

### 4.2 Design Quality and Architecture

**Design Quality:** Measured by Cohesion (how well code lines within a module relate) and Coupling (degree of interdependence between modules). High cohesion and loose coupling are ideal.

**Fan-In / Fan-Out:** Fan-in is the number of modules that call a specific module (high is good for reusability). Fan-out is the number of subordinates a module has (limit to 7 or fewer).

**Conceptual Architecture:** Conceptual architecture comprises the logical building blocks/subsystems of the WebApp.

**Technical Architecture:** Technical architecture maps logical components to specific hardware and software tiers (e.g., 3-tier: Client, App Server, DB Server).

---

## Chapter 5
## Web Apps Implementation

### 5.1 Client-Side Scripting

**Client side scripting: Java Script:** JavaScript is a client-side scripting language that enables dynamic behavior in web pages, such as form validation, DOM manipulation, event handling, and asynchronous requests.

**Client side scripting: AJAX:** AJAX (Asynchronous JavaScript and XML) allows web pages to send and receive data from a server asynchronously without reloading the entire page.

---

### 5.2 Server-Side Scripting and Frameworks

**Server Side Scripting: PHP:** PHP (Hypertext Preprocessor) is a widely-used open source server-side scripting language specifically designed for web development and embedded in HTML.

**PHP Specifics:**
- **Namespaces:** Map virtual folder structures to physical directories using standards like PSR-4.
- **Traits:** Mechanisms for reusing code across multiple classes without inheritance.
- **Composer:** A dependency management tool used to install and update libraries.

**Framework: PHP MVC frameworks (Code Igniter, Symfony, Zend, CakePHP):** PHP MVC frameworks provide a structured implementation of the Model-View-Controller pattern to organize code, separate concerns, and accelerate development.

**Web Service:** A web service is a software system designed to support interoperable machine-to-machine interaction over a network, often using REST or SOAP protocols.

**REST API:** A stateless, platform-independent way for apps to communicate over HTTP using standard methods like GET, POST, PUT, and DELETE.

---

### 5.3 Model-View-Controller (MVC) and Laravel

**Model-View-Controller (MVC):** An architectural pattern separating data (Model), presentation (View), and logic (Controller).

**Laravel Core Components:**
- **Routing:** Mapping incoming URLs to specific controller methods.
- **Blade Engine:** A powerful templating system allowing layout inheritance via `@extends`, `@section`, and `@yield`.
- **Eloquent ORM:** Technique that converts database data into PHP objects for easier manipulation.
- **Migrations:** Version control for databases, allowing teams to share and modify schemas through code.

**PDO (PHP Data Objects):** A database-independent class for secure queries using prepared statements to prevent SQL Injection.

> 💡 **PHP PDO Query:** Using `$db->prepare('SELECT * FROM book WHERE id = :id')` to safely fetch data using a placeholder.

> 💡 **Laravel Blade Template:** Defining a master layout in `app.blade.php` with `@yield('content')` and extending it in specific views.

---

## Chapter 6
## Web Apps Security

### 6.1 Encryption and Security Fundamentals

**Encryption techniques (digital signatures, certificates, PKI):** Encryption techniques used in web security include digital signatures for authentication and integrity, digital certificates for identity verification, and Public Key Infrastructure (PKI) for managing encryption keys.

**Security threats:** Security threats to WebApps include unauthorized access, data breaches, denial of service, malware injection, and man-in-the-middle attacks.

**Securing client/server interactions:** Securing client/server interactions involves using HTTPS (TLS/SSL), encrypting sensitive data, validating inputs on both client and server, and implementing proper session management.

---

### 6.2 Vulnerabilities and Attacks

**Vulnerabilities at the client (desktop security, phishing, etc.):** Client-side vulnerabilities include desktop security flaws (malware on user machine), phishing attacks (fraudulent sites stealing credentials), cross-site scripting (XSS), and insecure local storage.

**Vulnerabilities at the server (cross-site scripting, SQL injections, etc.):** Server-side vulnerabilities include Cross-Site Scripting (XSS), SQL Injection, Cross-Site Request Forgery (CSRF), file upload exploits, and insecure direct object references.

**Common Attacks:**
- **SQL Injection:** Injecting malicious characters into inputs to execute unintended database commands.
- **Cross-Site Request Forgery (CSRF):** Forcing a logged-in user to send unintended requests.
- **File Upload Vulnerabilities:** Exploiting upload features to execute arbitrary code.

**Building Secure Web Apps:** Building secure WebApps requires: input validation and sanitization, parameterized queries, output encoding, anti-CSRF tokens, secure session management, HTTPS enforcement, regular security patching, and security testing.

> 📌 **SQL Injection Attack Example:** A hacker entering `' OR 1=1 --` into a login form to bypass authentication.

**Practical Defense:** Input validation and sanitization, using HTTPS, implementing anti-CSRF tokens, and regular security patching.

---

## Chapter 7
## Testing Web Apps

### 7.1 Testing Types and Levels

**Testing Levels:**
- **Unit Testing:** Testing individual components/scripts for correctness.
- **Integration Testing:** Testing how components work together, focusing on interfaces.
- **System/Performance Testing:** Evaluating the entire app under expected loads.

**Content Testing:** Content testing verifies that all text, graphics, multimedia, and downloadable files are accurate, up-to-date, correctly formatted, and free of broken links or spelling errors.

**User Interface Testing:** User Interface testing checks that all interface elements (buttons, forms, menus, navigation controls) function correctly, appear consistently, and are usable across supported browsers and devices.

**Navigation Testing:** Navigation testing validates that all internal and external links work, navigation menus correctly direct users, breadcrumbs reflect location, and users cannot reach unintended pages.

**Configuration Testing:** Configuration testing verifies that the WebApp operates correctly across different operating systems, browsers (Chrome, Firefox, Safari, Edge), browser versions, screen resolutions, and device types.

**Security Testing:** Security testing attempts to exploit vulnerabilities such as SQL injection, XSS, CSRF, broken authentication, and insecure direct object references; it includes penetration testing and vulnerability scanning.

**Performance Testing:** Performance testing measures response time, throughput, resource utilization, and stability under normal and peak load conditions, often using load testing and stress testing.

---

### 7.2 Testing Granularity and Strategies

**Testing Granularity Levels:** Testing granularity levels for WebApps range from unit testing (smallest components) to integration testing (interactions) to system testing (full application) to acceptance testing (user validation).

**Scalability:** The ability to handle increasing traffic by adding resources (e.g., Load Balancing) without degrading performance.

**Load Balancer:** A device/service that distributes incoming traffic across multiple servers to ensure availability.

---

## Chapter 8
## Maintenance of Web Applications

### 8.1 Maintenance Activities

**Maintenance of Web Applications:** Maintenance of Web Applications is the set of activities performed after deployment to correct faults, adapt to changing environments, improve performance, or add new features.

**Web Server and Database server load balancing:** Load balancing distributes incoming network traffic across multiple web servers or database servers to prevent overload, reduce response time, and ensure high availability.

**Web apps performance assessment:** Performance assessment involves measuring key metrics such as page load time, time to first byte (TTFB), database query response time, concurrent user capacity, and server resource usage (CPU, memory, I/O).

**Application usage monitoring and report generation:** Application usage monitoring tracks user behavior, page views, session durations, feature usage, error rates, and traffic patterns. Report generation produces regular summaries (daily, weekly, monthly) for stakeholders to inform maintenance priorities and capacity planning.

---

### 8.2 Evolution and Scaling

**Maintenance challenges:** Maintenance challenges include: undocumented code, legacy technology, team turnover, regression risk, content freshness, and balancing new features against bug fixes.

**Scalability approach:** Scalability is achieved through horizontal scaling (adding more servers behind a load balancer), vertical scaling (upgrading existing server resources), caching (CDN, redis), database optimization (indexing, replication, sharding), and code optimization.

**Continuous Improvement:** WebApp maintenance is a continuous process of monitoring, assessing, prioritizing, and releasing updates to keep the application secure, performant, and valuable to users.

---

## Quick Reference Summary

| Chapter | Core Topic               | Key Terms                                                                                                                                                |
| ------- | ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1       | Introduction and Process | WebE, Attributes (Document-Centric, Interactive, Transactional, Workflow, Semantic), Hyper-text, Incremental process, Agile principles                   |
| 2       | Project Management       | Formulation, Planning, Task Table, Macroscopic schedule, Change control classes (1-4), Metrics                                                           |
| 3       | Analysis                 | Requirement analysis, User categories, Elicitation (Interviews, JAD, Use Cases), Content Model, Interaction Model, Functional Model, Configuration Model |
| 4       | Design                   | Interface, Typography, Layout, Aesthetic, Content, Architecture, Navigation, OOHDM, Cohesion, Coupling, Fan-in/Fan-out                                   |
| 5       | Implementation           | JavaScript, AJAX, PHP, Namespaces, Composer, MVC frameworks , Laravel (Routing, Blade, Eloquent, Migrations), PDO, REST API                              |
| 6       | Security                 | Digital signatures, Certificates, SQL Injection, XSS, CSRF, Phishing, Input validation, Anti-CSRF tokens                                                 |
| 7       | Testing                  | Content Testing, UI Testing, Navigation Testing, Configuration Testing, Security Testing, Performance Testing, Load Testing                              |
| 8       | Maintenance              | Load balancing (web and database), Performance assessment, Usage monitoring, Report generation, Scalability                                              |

---
*CSE 3131 — Web Engineering | Dept. of CSE, University of Rajshahi*




