

# Operating Systems

### Course Information
**Course:** CSE 3241 (Operating Systems)
**Course Type:** Theory, 3 Credit
**Prerequisite:** CSE1111 Introduction to Computer Systems, CSE2121 Data Structure, CSE2231 Computer Architecture and Organization
### Instructor
Mr. Kazi Jahidur Rahman, Assistant Professor, Dept. of CSE, University of Rajshahi 

### Course Motivation
> To develop basics knowledge on Operating system design and principles.

---

## Course Contents

| Area                        | Topics Covered                                                                                                            |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Introduction**            | Functions, evaluation, and types of OS (batch, multi-tasking, time-sharing, real-time, distributed, parallel)             |
| **System Structure**        | Operations, I/O, storage hierarchy, protections, services, and system calls                                               |
| **Process Management**      | Concepts, scheduling, operations, and inter-process communication                                                         |
| **Threads**                 | Benefits and types (user/kernel)                                                                                          |
| **CPU scheduling**          | Criteria, preemptive/non-preemptive algorithms (FCFS, SJF, RR, Priority), and multi-processor scheduling                  |
| **Process Synchronization** | Critical section problem, hardware synchronization, classical problems, and semaphores                                    |
| **Deadlocks**               | Characterization, prevention, avoidance (Bankers algorithm), detection, and recovery                                      |
| **Storage Management**      | Memory Management (paging, segmentation) and Virtual Memory (demand paging, page replacement algorithms, thrashing)       |
| **File Systems**            | Concept, access methods, directory structure, allocation methods (contiguous, linked, indexed), and free-space management |

---

## Textbooks

**Primary Texts:**
1. A. Silberschatz, P. B. Galvin, Greg Gagne — *Operating Systems Concepts*, Wiley Publisher
2. Donovan — *Systems Programming*, McGraw-Hill

---

## Table of Contents

1. [Chapter 1 – Introduction to Operating Systems](#chapter-1)
2. [Chapter 2 – System Structure and OS Operations](#chapter-2)
3. [Chapter 3 – Process Management](#chapter-3)
4. [Chapter 4 – Threads and Concurrency](#chapter-4)
5. [Chapter 5 – CPU Scheduling](#chapter-5)
6. [Chapter 6 – Process Synchronization](#chapter-6)
7. [Chapter 7 – Deadlocks](#chapter-7)
8. [Chapter 8 – Main Memory Management](#chapter-8)
9. [Chapter 9 – Virtual Memory](#chapter-9)
10. [Chapter 10 – File Systems](#chapter-10)

---

## Chapter 1
## Introduction to Operating Systems

### 1.1 Operating System Fundamentals

**Course Overview:** The Operating System (OS) is a fundamental piece of system software that acts as an intermediary between computer hardware and the user. Its primary goals are user convenience (providing a clean abstract model of resources) and efficient use of the computer's resources. An OS acts as a "resource manager," governing the CPU, memory, storage space, and I/O devices to ensure non-interference and security among various programs and users.

**Computer System Components:** A system consists of hardware (CPU, memory, I/O), the OS, application programs, and users.

**The Kernel:** This is the core program that runs at all times on the computer.

**Kernel:** The one program running at all times on the computer.

---

### 1.2 Functions, Evaluation, and Types of OS

**Functions of OS:** The operating system performs functions such as: process management, memory management, file system management, I/O management, security and protection, resource allocation, error detection, and user interface (command-line or graphical).

**Evaluation of OS:** Operating systems have evolved from batch processing systems to multiprogramming, time-sharing, real-time, distributed, and parallel systems, driven by advances in hardware and changing user requirements.

**Types of OS (batch, multi-tasking, time-sharing, real-time, distributed, parallel):**
- **Batch OS:** Jobs are collected, processed in groups (batches) without user interaction. Early systems used punch cards.
- **Multi-tasking OS:** Allows multiple programs to run concurrently by rapidly switching the CPU between them (also called multiprogramming).
- **Time-sharing OS:** An extension of multi-tasking where multiple users interact with the system simultaneously via terminals; the CPU time is shared among users.
- **Real-time OS (RTOS):** Guarantees that critical tasks are completed within strict timing constraints (used in embedded systems, robotics, medical devices).
- **Distributed OS:** Manages a collection of independent computers that appear to users as a single cohesive system; enables resource sharing and load balancing across a network.
- **Parallel OS:** Runs on multiple processors (tightly coupled) to execute a single program faster by dividing work among processors.

---

## Chapter 2
## System Structure and OS Operations

### 2.1 OS Operations

**Operating-System Operations:**
- **User Mode vs. Kernel Mode:** Hardware provides a "mode bit" to distinguish when the system is executing user code (User Mode) versus OS code (Kernel Mode). This prevents user programs from executing privileged instructions that could harm the system.
- **Interrupts:** Modern operating systems are interrupt-driven. Hardware sends signals to the CPU to trigger immediate attention to an event.

**Timer:** To prevent a process from hogging resources or getting stuck in an infinite loop, the OS uses a hardware timer that generates an interrupt after a specific period, allowing the OS to regain control.

---

### 2.2 I/O and Storage Hierarchy

**I/O (Input/Output):** I/O refers to the communication between the computer and external devices (keyboard, mouse, disk, display, network). The OS provides a uniform interface for I/O operations, hiding device-specific details.

**Storage hierarchy:** The storage hierarchy organizes storage devices by speed, cost, and volatility. From fastest (most expensive) to slowest (least expensive): Registers → Cache (L1, L2, L3) → Main Memory (RAM) → Solid-State Drive (SSD) → Magnetic Disk (HDD) → Optical Disk → Magnetic Tape. The OS manages data movement across this hierarchy.

**Spooling:** Overlapping the output of one job with the input of others.

---

### 2.3 Protections, Services, and System Calls

**Protections:** Protection mechanisms control access of processes and users to system resources. The OS enforces isolation between processes to prevent interference and unauthorized access.

**Services:** OS services include: program execution, I/O operations, file system manipulation, communications (IPC, networking), error detection, resource allocation, accounting, and protection/security.

**System Calls:** These provide the primary interface between a running program and the OS. While system calls are low-level, programmers typically use APIs (Application Programming Interfaces) like Win32 or POSIX for ease of use.

**System Call:** A mechanism for an application to request services from the OS kernel.

**Context Switch:** Saving the state of the current process and loading the state of a new one when switching the CPU.

---

## Chapter 3
## Process Management

### 3.1 Process Concept and Layout

**Process Concept:** A **process** is defined as a "program in execution". While a program is a passive entity (like an executable file on disk), a process is an active entity with a program counter, registers, and a memory layout.

**Process Layout in Memory:**
- **Text Section:** Executable code.
- **Data Section:** Global variables.
- **Heap:** Dynamically allocated memory during runtime.
- **Stack:** Temporary data (function parameters, return addresses).

**Process Control Block (PCB):** Each process is represented in the OS by a PCB containing its state, PID, program counter, and CPU registers.

**Process States:** A process transitions through states: **New** (being created), **Ready** (waiting for CPU), **Running** (executing instructions), **Waiting** (waiting for an event/IO), and **Terminated** (finished).

**Process management:** Process management includes creating and terminating processes, scheduling processes, context switching, and inter-process communication (IPC).

**Process scheduling:** Scheduling selects which process from the ready queue will be executed next by the CPU.

**Process operations:** Operations on processes include: process creation (fork, spawn), process termination (exit, abort), process suspension (block/wait), and process resumption (signal/wakeup).

**Inter-process communication (IPC):** IPC mechanisms allow processes to exchange data and synchronize. Methods include: shared memory, message passing (pipes, message queues, sockets), signals, and remote procedure calls (RPC).

> 📌 **Process Analogy:** A program is a recipe (passive), while a process is the activity of a chef actually cooking the cake (active).

---

## Chapter 4
## Threads and Concurrency

### 4.1 Thread Fundamentals

**Threads:** A thread is the basic unit of CPU utilization within a process.

**Multithreading:** Modern processes can have multiple threads sharing the process's resources (code, data, files) while maintaining their own registers and stacks.

**Benefits of threads:** This increases responsiveness (e.g., one thread handles UI while another processes data) and improves performance on multicore systems.

**Benefits and types (user/kernel):**
- **Benefits of threads:** Responsiveness, resource sharing, economy (less overhead than processes), and scalability on multi-processor systems.
- **User threads:** Thread management is done by a thread library in user space (e.g., POSIX Pthreads, Java threads) without kernel intervention. User threads are fast to create and switch but cannot take advantage of multiple cores if the kernel sees only one process.
- **Kernel threads:** Thread management is done by the OS kernel (e.g., Windows threads, Linux threads). Kernel threads are slower to create and manage but can run concurrently on multiple processors, and if one thread blocks, others can continue.

---

## Chapter 5
## CPU Scheduling

### 5.1 Scheduling Fundamentals

**CPU Scheduling Objective:** To maximize CPU utilization and minimize response/waiting time.

**Scheduler:** Selects a process from the **Ready Queue** to execute next on the CPU core.

**Scheduling Schemes:**
- **Non-preemptive:** A process keeps the CPU until it terminates or switches to a waiting state.
- **Preemptive:** The OS can forcibly take the CPU away from a process to give it to a higher-priority task.

**Criteria for scheduling:** Optimized for high **Throughput** (completed processes per time) and low **Turnaround Time** (total time from submission to completion).

**Other scheduling metrics:** CPU utilization (keep CPU as busy as possible), throughput (number of processes completed per unit time), turnaround time (submission to completion time), waiting time (total time spent in ready queue), response time (submission to first response).

---

### 5.2 Scheduling Algorithms

**Preemptive/non-preemptive algorithms (FCFS, SJF, RR, Priority):**
- **FCFS (First-Come, First-Served):** Non-preemptive; processes are executed in order of arrival. Simple but suffers from the convoy effect (short processes wait behind long ones).
- **SJF (Shortest Job First):** Non-preemptive (or preemptive as SRTF); selects the process with the smallest next CPU burst. Optimal in terms of average waiting time but requires knowledge of future burst times.
- **RR (Round Robin):** Preemptive; each process gets a small time quantum (e.g., 10–100 ms). After quantum expires, process is moved to the back of the ready queue. Good for time-sharing systems; performance depends on quantum size.
- **Priority Scheduling:** Assigns a priority to each process; highest priority runs first. Can be preemptive or non-preemptive. Risk of starvation (low-priority processes never run) solved by aging (gradually increase priority of waiting processes).

**Multi-processor scheduling:** In systems with multiple CPUs, scheduling becomes more complex: symmetric multiprocessing (SMP) where all processors are peers and schedule from a common ready queue or per-processor queues; processor affinity (keeping a process on the same processor to preserve cache); load balancing (pushing tasks between processors to keep all busy).

> 💡 **FCFS Scheduling Calculation Example:** If process $P_1$ has a burst time of 24, $P_2$ has 3, and $P_3$ has 3, and they arrive in order $P_1, P_2, P_3$, the average waiting time is $(0 + 24 + 27) / 3 = 17$.

---

## Chapter 6
## Process Synchronization

### 6.1 Critical Section Problem

**Race Condition:** Occurs when multiple processes access and manipulate shared data concurrently, and the final outcome depends on the order of execution.

**Critical Section:** A segment of code where shared resources are accessed. To prevent race conditions, access must be synchronized.

**Critical section problem:** The problem of designing a protocol that processes can use to coordinate access to shared resources. Solutions must satisfy:
1. **Mutual Exclusion:** Only one process at a time can execute in the critical section.
2. **Progress:** If no process is in its critical section, a process that wishes to enter cannot be postponed indefinitely.
3. **Bounded Waiting:** There is a limit on how many other processes can enter the critical section after a process has requested to enter.

---

### 6.2 Synchronization Tools

**Hardware synchronization:** Hardware solutions include: disabling interrupts (for uniprocessor systems, but too coarse), test-and-set (TSL) instruction, compare-and-swap (CAS) instruction, and atomic increment operations. These instructions are executed atomically (cannot be interrupted).

**Synchronization Tools:**
- **Mutex Locks:** A boolean variable used to protect a critical section; a process must `acquire()` the lock before entering and `release()` it afterward.
- **Semaphores:** An integer variable accessed via two atomic operations: `wait()` (decrements) and `signal()` (increments). Binary semaphores (0/1) act like mutexes; counting semaphores allow up to N concurrent accesses.
- **Monitors:** A high-level abstraction that provides a convenient and effective mechanism for process synchronization. A monitor encapsulates shared data and procedures; only one process can be active in the monitor at a time (compiler-enforced mutual exclusion).

**Classical problems of synchronization:** Classic problems used to test synchronization primitives include: the Bounded-Buffer (Producer-Consumer) problem, the Readers-Writers problem, and the Dining Philosophers problem.

---

## Chapter 7
## Deadlocks

### 7.1 Deadlock Characterization

**Definition:** A state where a set of processes are permanently blocked because each is waiting for a resource held by another process in the set.

**Deadlock characterization:** Deadlocks can be described using four necessary conditions that must hold simultaneously.

**Necessary Conditions:** Deadlock requires four conditions to occur simultaneously:
1.  **Mutual Exclusion:** Only one process can use a resource at a time.
2.  **Hold and Wait:** A process holding one resource is waiting for another.
3.  **No Preemption:** Resources cannot be taken away; they must be released voluntarily.
4.  **Circular Wait:** A closed chain of processes exists where each waits for a resource held by the next.

> 📌 **Deadlock Analogy:** A four-way traffic stop where every car waits for the one to its right before proceeding.

---

### 7.2 Deadlock Handling

**Handling:** Options include **Prevention** (ensuring one condition cannot occur), **Avoidance** (Banker's Algorithm), or **Detection and Recovery**.

**Deadlock prevention:** Prevent at least one of the four necessary conditions from occurring:
- Break Mutual Exclusion: Not always possible (some resources are inherently non-sharable).
- Break Hold and Wait: Require process to request all resources at once (may lead to low utilization).
- Break No Preemption: Allow OS to preempt resources from waiting processes (difficult to implement).
- Break Circular Wait: Impose a total ordering of resource types; processes must request resources in increasing order.

**Deadlock avoidance (Banker's algorithm):** Requires processes to declare their maximum resource needs upfront. The OS runs the Banker's Algorithm (a safety algorithm) before granting resource requests; if granting the request would lead to an unsafe state (potential deadlock), the request is denied and the process must wait.

**Deadlock detection:** Periodically run an algorithm that checks the wait-for graph for cycles. If a cycle exists, a deadlock has occurred. Detection can be performed at each resource request or on a timer.

**Deadlock recovery:** Once a deadlock is detected, recovery methods include:
- Abort one or more processes in the deadlock (choosing victim with minimal cost).
- Preempt resources from one process and give them to another (rollback the preempted process to a safe state, potentially causing starvation).

---

## Chapter 8
## Main Memory Management

### 8.1 Address Binding and Translation

**Main Memory Management:** Memory management is the activity of managing the computer's main memory (RAM), keeping track of which parts are in use by which processes, and allocating/deallocating memory as needed.

**Address Binding:** The mapping of instructions and data to physical memory addresses. This can happen at compile, load, or execution time.

**Logical vs. Physical Address:** The CPU generates a **Logical Address** (virtual address), while the **Memory Management Unit (MMU)** translates it into a **Physical Address** in RAM.

> 💡 **Memory Translation Example:** If the relocation register is 14000, a logical address of 346 is mapped to a physical address of 14346 ($14000 + 346$).

---

### 8.2 Paging and Segmentation

**Paging:** Memory is divided into fixed-size blocks called **frames** (physical) and **pages** (logical). This avoids external fragmentation.

**Paging details:** The CPU generates a logical address consisting of a page number (page table index) and an offset within the page. The MMU looks up the page table to find the corresponding physical frame number, then appends the offset to form the physical address.

**Segmentation:** Memory management scheme that divides a process into logical segments (code, data, stack, etc.) of variable sizes. A logical address consists of a segment number and an offset. The segment table contains the base physical address and limit for each segment.

**Translation Lookaside Buffer (TLB):** A fast hardware cache used to speed up the address translation process. The TLB caches recently used page table entries, avoiding slow main memory access for page table lookups.

---

## Chapter 9
## Virtual Memory

### 9.1 Virtual Memory and Demand Paging

**Virtual Memory:** Separates the logical memory perceived by users from the physical memory. It allows programs to run that are larger than the actual RAM by loading only parts of them as needed.

**Demand Paging:** Pages are loaded only when they are accessed during execution. If an accessed page is not in RAM, a **Page Fault** occurs, and the OS must fetch it from the backing store (swap space or the executable file).

**Page fault handling:**
1. Hardware traps to kernel.
2. OS saves process state and determines the needed page.
3. OS checks that the address is valid; finds free frame.
4. OS schedules a disk read to bring the page into the frame.
5. While I/O is pending, OS runs another process.
6. On I/O completion, page table is updated with the frame number.
7. OS restarts the faulting instruction.

---

### 9.2 Page Replacement and Thrashing

**Page Replacement Algorithms:** When RAM is full, the OS must choose a page to swap out. Common algorithms include **FIFO** (First-In, First-Out), **Optimal** (future knowledge), and **LRU** (Least Recently Used).

**Page Replacement Algorithms in detail:**
- **FIFO:** Replaces the oldest page in memory. Simple but can suffer from Belady's anomaly (more frames can lead to more page faults).
- **Optimal (OPT):** Replaces the page that will not be used for the longest time in the future. Optimal but impossible to implement in practice (requires future knowledge); used as a benchmark.
- **LRU (Least Recently Used):** Replaces the page that has not been used for the longest time. Approximates optimal well, but requires hardware support (counter or stack) to track usage.

**Thrashing:** A condition where a process spends more time paging than executing, leading to severe performance drops. Thrashing occurs when the sum of working sets (pages a process actively uses) exceeds the available physical memory. The OS responds by swapping pages in and out constantly, causing very high page fault rates and low CPU utilization.

**Thrashing solution:** Reduce the degree of multiprogramming (run fewer processes) so that active pages of remaining processes fit in memory; or use page fault frequency (PFF) algorithm to adjust memory allocation per process.

---

## Chapter 10
## File Systems

### 10.1 File Concept and Access Methods

**File Concept:** A logical storage unit containing related information.

**File System concept:** The file system provides a uniform logical view of stored information, abstracting away the details of physical storage devices. It manages files, directories, metadata, and free space.

**File Attributes:** Name, identifier, type, location, size, and protection.

**File access methods:** Sequential access (read/write bytes in order, used with tape and simple files), direct/random access (read/write any block by its logical address, used in databases), and indexed access (uses an index block to speed lookups).

**Directory Structure:** Organizes files into folders. Hierarchical (tree-structured) directories are the standard for modern systems. Types include: single-level (all files in one directory), two-level (one directory per user), and tree-structured (any number of nested directories).

---

### 10.2 Allocation Methods and Free-Space Management

**Allocation methods (contiguous, linked, indexed):**
- **Contiguous Allocation:** Each file occupies a contiguous block of disk blocks. Simple but leads to external fragmentation and limits file growth.
- **Linked Allocation:** Each file is a linked list of disk blocks (pointer in each block points to next). No external fragmentation, but random access is slow.
- **Indexed Allocation:** Each file has an index block containing pointers to all its data blocks. Supports efficient random access; index block size determines maximum file size (solved by multi-level indices or linked index blocks).

**Free-space management:** The OS tracks free disk blocks using: bit vector (bitmap where 1 = used, 0 = free), linked list (list of free blocks, possibly grouping multiple blocks per node), grouping (blocks store addresses of other free blocks), or counting (track consecutive free blocks).

**VFS (Virtual File System):** An abstraction layer that allows different file systems (like Linux ext4 and Windows NTFS) to be accessed via a uniform interface.

---

## Quick Reference Summary

| Chapter | Core Topic            | Key Terms                                                                                                             |
| ------- | --------------------- | --------------------------------------------------------------------------------------------------------------------- |
| 1       | Introduction          | Kernel, Batch, Multi-tasking, Time-sharing, Real-time, Distributed, Parallel, Resource manager                        |
| 2       | System Structure      | User/Kernel Mode, Interrupts, Timer, Storage hierarchy, System calls, API (Win32, POSIX)                              |
| 3       | Process Management    | Process (program in execution), PCB, States (New, Ready, Running, Waiting, Terminated), IPC                           |
| 4       | Threads               | Thread (unit of CPU utilization), User threads, Kernel threads, Responsiveness, Multithreading                        |
| 5       | CPU Scheduling        | Preemptive/Non-preemptive, FCFS, SJF, RR, Priority, Throughput, Turnaround time, Multi-processor                      |
| 6       | Synchronization       | Race condition, Critical section, Mutex, Semaphore (wait/signal), Monitor, Classical problems                         |
| 7       | Deadlocks             | Mutual exclusion, Hold and wait, No preemption, Circular wait, Prevention, Banker's algorithm, Detection              |
| 8       | Memory Management     | Logical/Physical address, MMU, Paging (pages/frames), Segmentation, TLB                                               |
| 9       | Virtual Memory        | Demand paging, Page fault, Page replacement (FIFO, Optimal, LRU), Thrashing                                           |
| 10      | File Systems          | File attributes, Directory (hierarchical), Access methods, Allocation (contiguous, linked, indexed), VFS              |

---
*CSE 3241 — Operating Systems | Dept. of CSE, University of Rajshahi*





