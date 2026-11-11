
# Computer Systems Fundamentals

> **Document Type:** Software Engineering Fundamentals  
> **Topic:** Understanding Computer Systems  
> **Project:** EnterpriseFlow — Enterprise Asset Management Platform  
> **Document Version:** 1.0  
> **Status:** Completed  
> **Purpose:** To understand the fundamental hardware and software components of a computer system and how programs are translated, executed and managed by the operating system.

---

## 1. Introduction

A computer system is an integrated combination of hardware and software components that work together to receive input, process data, store information and produce output.

Every software application, whether a simple Java program or a large enterprise application, depends on the underlying computer system to execute its instructions.

For example, when an employee accesses the EnterpriseFlow Asset Management Platform to register a company laptop, several computer system components work together:

1. The CPU processes application instructions.
2. RAM temporarily stores the application and the data it needs.
3. Storage retains application files, databases and business records.
4. The operating system manages hardware and software resources.
5. Processes and threads execute the application's operations.
6. The programming language provides instructions used to develop the application.
7. The compiler translates source code into an executable representation.
8. The Java Virtual Machine executes Java bytecode.

Understanding these components is essential for software engineers because application performance, reliability, resource consumption and execution behaviour depend on how computer systems operate.

---

# 2. Central Processing Unit (CPU)

## 2.1 Definition

The Central Processing Unit (CPU) is the primary processing component of a computer. It executes program instructions, performs calculations, processes data and coordinates computational activities.

The CPU is commonly referred to as the brain of the computer because it performs the operations required to execute software.

Whenever a user opens an application, calculates a value, searches a database or processes a transaction, the CPU executes the instructions required to perform those operations.

## 2.2 Major Functions of the CPU

The CPU performs several important functions:

| Function | Description |
|---|---|
| Instruction Fetching | Retrieves instructions from memory. |
| Instruction Decoding | Determines what an instruction requires the CPU to do. |
| Execution | Performs the required operation. |
| Arithmetic Operations | Performs mathematical calculations. |
| Logical Operations | Performs comparisons and logical decisions. |
| Data Processing | Manipulates information according to program instructions. |
| Control Operations | Coordinates the execution of instructions and other CPU activities. |

## 2.3 Major Components of a CPU

### A. Arithmetic Logic Unit (ALU)

The Arithmetic Logic Unit performs arithmetic and logical operations.

Arithmetic operations include:

- Addition.
- Subtraction.
- Multiplication.
- Division.

Logical operations include:

- AND.
- OR.
- NOT.
- Comparisons such as greater than, less than and equality.

For example, when an asset management application calculates the annual depreciation of a laptop, the CPU performs the required arithmetic operations.

### B. Control Unit (CU)

The Control Unit coordinates CPU operations.

It retrieves and decodes instructions and directs the execution of operations within the processor.

### C. Registers

Registers are small, extremely fast storage locations inside the CPU.

They temporarily hold data, memory addresses, instructions and intermediate calculation results required during execution.

### D. CPU Cache

CPU cache is a small, high-speed memory located inside or close to the processor.

It stores frequently accessed instructions and data to reduce the time required to retrieve information from RAM.

CPU cache commonly consists of:

- L1 Cache: Smallest and generally fastest cache.
- L2 Cache: Larger than L1 but generally slower.
- L3 Cache: Often larger and shared among processor cores.

## 2.4 CPU Cores and Clock Speed

### CPU Cores

A CPU core is an individual processing unit capable of executing instructions.

Modern processors commonly contain multiple cores.

For example:

- Dual-core: 2 cores.
- Quad-core: 4 cores.
- Hexa-core: 6 cores.
- Octa-core: 8 cores.

Multiple cores allow a processor to execute multiple instruction streams concurrently.

### Clock Speed

CPU clock speed indicates the number of clock cycles a processor performs per second.

It is measured in Hertz (Hz), commonly expressed in:

- MHz: Megahertz.
- GHz: Gigahertz.

For example, a 3.5 GHz processor has a clock frequency of approximately 3.5 billion cycles per second.

However, clock speed alone does not determine processor performance. Architecture, core count, cache, instruction efficiency, memory performance and workload characteristics also matter.

## 2.5 Practical Example

Consider a Java application that calculates the total value of company assets.

```java
public class AssetCalculator {

    public static void main(String[] args) {

        double laptop = 1200000;
        double printer = 450000;
        double server = 3500000;

        double totalValue = laptop + printer + server;

        System.out.println(
            "Total Asset Value: ₦" + totalValue
        );
    }
}
```

The CPU executes the arithmetic instructions required to calculate the total asset value.

**Key Point:** The CPU executes program instructions and performs the computational operations required by software applications.

---

# 3. Random Access Memory (RAM)

## 3.1 Definition

Random Access Memory (RAM) is the computer's primary volatile memory. It temporarily stores data, instructions and application information that the CPU needs while programs are running.

RAM enables applications to access data much faster than retrieving the same information from conventional storage devices.

Unlike persistent storage, RAM generally loses its contents when the computer loses power.

For example, when an employee opens EnterpriseFlow in a browser, the operating system, browser processes and application data occupy memory while they are being used.

## 3.2 Functions of RAM

RAM performs several important functions:

1. Stores currently running applications.
2. Holds data required by the CPU.
3. Stores temporary application information.
4. Supports multitasking.
5. Reduces the need to repeatedly retrieve information from slower storage.
6. Provides memory space for processes and threads.

## 3.3 Types of RAM

### A. DRAM (Dynamic Random Access Memory)

DRAM is commonly used as the main system memory in computers and servers.

It stores information using capacitors and requires periodic refreshing to retain its contents.

### B. SRAM (Static Random Access Memory)

SRAM is faster and more expensive than DRAM.

It is commonly used in CPU caches rather than as the primary system memory.

### C. DDR Memory

Modern computers commonly use DDR (Double Data Rate) SDRAM.

Examples include:

- DDR3.
- DDR4.
- DDR5.

Different generations have different speeds, bandwidth, power requirements and compatibility specifications.

## 3.4 RAM Capacity and Performance

RAM capacity determines how much data and how many application workloads can be held in memory simultaneously.

Common capacities include:

| RAM Capacity | Typical Usage |
|---|---|
| 4 GB | Basic computing with limited multitasking. |
| 8 GB | Everyday computing and light development. |
| 16 GB | General software development and multitasking. |
| 32 GB | More demanding development environments and virtual machines. |
| 64 GB | Advanced development, virtualization and database workloads. |
| 128 GB+ | Larger server and memory-intensive workloads. |

Actual requirements depend on the operating system, applications, workload and concurrent users.

## 3.5 What Happens When RAM Is Insufficient?

When RAM becomes insufficient, the operating system may move less frequently used memory pages to storage.

This is commonly called paging or swapping.

Because storage is generally slower than RAM, excessive paging can significantly reduce system performance.

For example, if a server runs:

- A Java application.
- A PostgreSQL database.
- Redis.
- Monitoring services.
- Several background processes.

Insufficient memory can cause performance degradation, increased paging or even application termination.

## 3.6 Practical Example: RAM Usage

Consider the following Java program:

```java
import java.util.ArrayList;
import java.util.List;

public class MemoryExample {

    public static void main(String[] args) {

        List<String> employees = new ArrayList<>();

        employees.add("Employee 001");
        employees.add("Employee 002");
        employees.add("Employee 003");

        System.out.println(employees);
    }
}
```

When this program executes:

1. The Java application runs as a process.
2. The JVM uses memory allocated to the Java process.
3. The employee list and its data occupy memory.
4. The CPU accesses the required data during execution.

**Key Point:** RAM provides temporary working space for running applications and their data.

---

# 4. Storage

## 4.1 Definition

Computer storage is the component responsible for retaining data, programs, operating systems and information for future use.

Unlike RAM, persistent storage retains information when the computer is powered off.

Storage is essential because applications need a permanent location to store program files, databases, documents, images, logs and other information.

For example, the EnterpriseFlow platform must permanently store:

- Employee information.
- Asset records.
- Branch details.
- Procurement transactions.
- Depreciation schedules.
- Audit logs.
- Financial reports.

## 4.2 Types of Storage

### A. Hard Disk Drive (HDD)

An HDD is a magnetic storage device that uses rotating disks and mechanical read/write components.

Characteristics:

- Relatively low cost per gigabyte.
- Available in large capacities.
- Slower than modern SSDs.
- Contains moving mechanical components.

Common applications include backups, archival storage and large-capacity data storage.

### B. Solid State Drive (SSD)

An SSD stores information using flash memory rather than rotating mechanical disks.

Characteristics:

- Faster data access than HDDs.
- No moving mechanical components.
- Lower latency.
- Generally more resistant to physical shock.
- Higher cost per gigabyte in many configurations.

### C. NVMe SSD

NVMe (Non-Volatile Memory Express) is a storage protocol designed for high-speed communication with flash storage over PCIe.

NVMe SSDs commonly offer higher performance than traditional SATA SSDs.

## 4.3 Comparison of Storage Technologies

| Feature | HDD | SATA SSD | NVMe SSD |
|---|---|---|---|
| Technology | Magnetic disks | Flash memory | Flash memory |
| Moving Parts | Yes | No | No |
| Performance | Relatively slow | Fast | Very fast |
| Latency | Higher | Lower | Very low |
| Cost per GB | Generally lower | Higher | Varies |
| Typical Usage | Archives and backups | General computing | High-performance systems |

## 4.4 Primary Storage vs Secondary Storage

Primary memory and secondary storage serve different purposes.

| Primary Memory (RAM) | Secondary Storage |
|---|---|
| Temporarily stores active data. | Permanently stores data. |
| Generally volatile. | Non-volatile. |
| Very fast access. | Generally slower than RAM. |
| Used during program execution. | Used for long-term data retention. |
| Limited by installed memory capacity. | Usually offers much larger capacity. |

## 4.5 Practical Example: Enterprise Database Storage

Suppose EnterpriseFlow has 10 branches and maintains records for thousands of company assets.

The application needs a database to permanently store these records.

A database such as PostgreSQL can store information on persistent storage.

Example SQL:

```sql
CREATE TABLE assets (
    asset_id BIGSERIAL PRIMARY KEY,
    asset_name VARCHAR(150) NOT NULL,
    asset_tag VARCHAR(50) UNIQUE NOT NULL,
    purchase_cost NUMERIC(15, 2) NOT NULL,
    branch_id BIGINT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

When an authorized user registers a new asset, the application sends an SQL INSERT statement to PostgreSQL.

The database stores the record on persistent storage, subject to its transaction, caching and durability mechanisms.

**Key Point:** Storage retains software and business information beyond the lifetime of a running program.

---

# 5. Operating System (OS)

## 5.1 Definition

An Operating System (OS) is system software that manages computer hardware and provides services that application software uses to execute.

It acts as an intermediary between computer hardware, application software and users.

Without an operating system, application developers would have to manage hardware resources and low-level device operations themselves.

Examples of operating systems include:

- Microsoft Windows.
- Linux.
- macOS.
- Android.
- iOS.

Server environments commonly use Linux and Windows Server.

## 5.2 Major Responsibilities of an Operating System

### A. Process Management

The operating system creates, schedules and terminates processes.

It determines how CPU resources are allocated among running applications.

### B. Memory Management

The operating system manages RAM allocation and virtual memory.

It ensures that processes receive the memory resources they need, subject to system constraints and protection mechanisms.

### C. File System Management

The operating system manages how files and directories are created, stored, accessed and organized.

Examples include:

- NTFS.
- FAT32.
- exFAT.
- ext4.
- XFS.
- APFS.

### D. Device Management

The operating system manages hardware devices through device drivers and system interfaces.

Examples include:

- Printers.
- Keyboards.
- Network adapters.
- Storage devices.
- Graphics cards.

### E. Security and Access Control

The operating system manages users, permissions, authentication mechanisms and resource access.

### F. Networking

The operating system provides networking capabilities that allow applications to communicate through network interfaces and protocols.

### G. User Interface

The operating system provides interfaces through which users interact with computers.

These may include:

- Graphical User Interface (GUI).
- Command-Line Interface (CLI).

## 5.3 Kernel

The kernel is the core component of an operating system.

It manages critical system resources and provides controlled access to hardware.

Major kernel responsibilities include:

- CPU scheduling.
- Memory management.
- Process management.
- Device management.
- System calls.
- Hardware resource coordination.

For example, when a Java application needs to read a file, it uses operating system services to access the file system.

## 5.4 User Mode and Kernel Mode

Modern operating systems generally separate execution into different privilege levels.

### User Mode

Applications normally execute in user mode.

They have restricted access to hardware and protected operating system resources.

Examples:

- Web browsers.
- Java applications.
- Word processors.
- Database client applications.

### Kernel Mode

The operating system kernel executes in kernel mode with privileged access to system resources.

Applications request privileged services through controlled interfaces such as system calls.

This separation improves system security and stability.

## 5.5 Practical Example

Consider a Java application that needs to save an asset report to a file.

```java
import java.io.FileWriter;
import java.io.IOException;

public class FileExample {

    public static void main(String[] args) {

        try (FileWriter writer =
                new FileWriter("asset-report.txt")) {

            writer.write("EnterpriseFlow Asset Report");

            System.out.println("Report saved successfully.");

        } catch (IOException e) {

            System.out.println(
                "Unable to save report: " + e.getMessage()
            );
        }
    }
}
```

The Java application uses Java's file APIs. The runtime and operating system work together to create and write the file through the underlying file system.

**Key Point:** The operating system manages hardware resources and provides the services required by application software.

---

# 6. Processes

## 6.1 Definition

A process is an instance of a program that is currently executing.

When a program is launched, the operating system creates a process and allocates resources required for its execution.

A process has its own virtual address space and operating system-managed resources.

Examples of processes include:

- Google Chrome.
- Microsoft Word.
- PostgreSQL Server.
- A running Java application.
- A Linux background service.

A program stored on disk is not necessarily running. It becomes a process when the operating system starts executing it.

## 6.2 Components of a Process

A process generally includes:

| Component | Description |
|---|---|
| Process ID (PID) | Unique identifier assigned by the operating system. |
| Program Code | Instructions being executed. |
| Memory Space | Virtual memory allocated to the process. |
| Heap | Memory used for dynamically allocated objects and data. |
| Stack | Memory used for function calls, local variables and execution state. |
| Program Counter | Tracks the next instruction to execute within a thread. |
| Open Handles | References to files, sockets and other operating system resources. |
| Process State | Indicates the current execution status. |

Note: Each thread has its own execution stack and program counter, while threads in the same process share the process's address space and many resources.

## 6.3 Process States

A process may move through different execution states.

Common states include:

1. New: The process is being created.
2. Ready: The process is waiting for CPU scheduling.
3. Running: Its instructions are currently executing.
4. Waiting/Blocked: It is waiting for an event or resource.
5. Terminated: Execution has completed or the process has been stopped.

The operating system manages transitions between these states.

## 6.4 Example: Running a Java Application

Consider:

```java
public class HelloEnterprise {

    public static void main(String[] args) {

        System.out.println(
            "Welcome to EnterpriseFlow"
        );
    }
}
```

When the Java application is launched:

1. The operating system starts the Java runtime process.
2. A process ID is assigned.
3. Memory is allocated.
4. The JVM loads and executes the application.
5. The program displays its output.
6. The process terminates when execution finishes and no remaining non-daemon threads keep it alive.

## 6.5 Process Isolation

Modern operating systems isolate processes to prevent one application's memory from being directly accessed by another application without authorization.

For example, a browser process and a database server process generally operate within separate virtual address spaces.

This helps improve security and system stability.

**Key Point:** A process is a running instance of a program with its own execution environment and operating system-managed resources.

---

# 7. Threads

## 7.1 Definition

A thread is the smallest independently schedulable unit of execution within a process.

A process can contain one or multiple threads.

Threads within the same process share resources such as:

- Process memory.
- Heap.
- Open files and other process resources.

However, each thread has its own:

- Execution stack.
- Program counter.
- Thread-specific execution state.

Threads allow applications to perform multiple activities concurrently.

## 7.2 Why Are Threads Important?

Consider an enterprise application where multiple operations must happen without blocking one another.

For example:

- One thread handles incoming user requests.
- Another processes background notifications.
- Another performs scheduled reporting.
- Another handles a separate background task.

Using multiple threads can improve responsiveness and throughput when designed correctly.

However, concurrency introduces challenges such as:

- Race conditions.
- Deadlocks.
- Thread synchronization.
- Shared data corruption.
- Resource contention.

## 7.3 Process vs Thread

| Feature | Process | Thread |
|---|---|---|
| Definition | Running instance of a program. | Execution unit within a process. |
| Memory | Has its own virtual address space. | Shares the process address space. |
| Resource Usage | Generally heavier. | Generally lighter. |
| Communication | Often requires inter-process communication (IPC). | Can communicate through shared memory. |
| Isolation | Greater isolation. | Less isolation from other threads in the same process. |
| Creation | Generally more resource-intensive. | Generally less resource-intensive. |
| Failure Impact | A process failure is generally isolated from other processes. | An unhandled thread failure may affect the entire process. |

## 7.4 Java Thread Example

Java provides built-in support for multithreading.

```java
public class ThreadExample {

    public static void main(String[] args) {

        Thread assetThread = new Thread(() -> {

            System.out.println(
                "Processing asset records..."
            );

        });

        Thread reportThread = new Thread(() -> {

            System.out.println(
                "Generating financial reports..."
            );

        });

        assetThread.start();
        reportThread.start();
    }
}
```

In this example:

- The main thread executes the `main()` method.
- `assetThread` executes the asset processing task.
- `reportThread` executes the reporting task.

The two worker threads can execute concurrently. Their output order is not guaranteed.

## 7.5 Concurrency vs Parallelism

These concepts are related but different.

**Concurrency** means multiple tasks make progress during overlapping periods. The operating system or runtime may interleave their execution.

**Parallelism** means multiple tasks actually execute simultaneously, typically using multiple CPU cores.

For example, a four-core server may execute different application threads in parallel, depending on workload and scheduling.

**Key Point:** Processes provide independent execution environments, while threads provide multiple execution paths within a process.

---

# 8. Programming Languages

## 8.1 Definition

A programming language is a formal language used to express instructions, algorithms and computational logic that a computer system can execute, directly or through translation by a compiler or interpreter.

Programming languages allow developers to communicate computational instructions to computers in a structured and understandable form.

Examples include:

- Java.
- Python.
- JavaScript.
- C.
- C++.
- C#.
- Go.
- Rust.
- PHP.

## 8.2 Categories of Programming Languages

Programming languages can be classified in several ways.

### A. Low-Level Languages

Low-level languages provide instructions that are closely related to computer hardware.

Examples:

**Machine Language**

Machine language consists of binary instructions that a processor can execute directly.

Example:

```text
10110000 01100001
```

**Assembly Language**

Assembly language uses symbolic instructions representing machine operations.

Example:

```asm
MOV AX, 10
ADD AX, 20
```

Assembly language is architecture-specific and must be translated into machine code by an assembler.

### B. High-Level Languages

High-level programming languages provide abstractions that make software development easier.

Examples:

- Java.
- Python.
- JavaScript.
- C#.

They allow developers to write programs without manually managing every hardware-level operation.

Java example:

```java
public class Addition {

    public static void main(String[] args) {

        int firstNumber = 10;
        int secondNumber = 20;

        int result = firstNumber + secondNumber;

        System.out.println(result);
    }
}
```

This is easier to understand and maintain than writing the equivalent operations directly in machine language.

## 8.3 Compiled and Interpreted Languages

Programming languages can also be discussed according to how their implementations translate and execute programs.

### Compiled Languages

A compiler translates source code into another representation, such as machine code or bytecode, before or during execution.

Examples include:

- C.
- C++.
- Java.

Java is a special case because its source code is normally compiled into bytecode, which is then executed by the JVM.

### Interpreted Execution

An interpreter executes program instructions through an interpreter or runtime environment.

Python and JavaScript are commonly described as interpreted languages, although their modern implementations may use bytecode, just-in-time compilation and other optimization techniques.

The distinction is therefore not always absolute.

## 8.4 Choosing a Programming Language

The choice of programming language depends on several factors:

- Application requirements.
- Performance requirements.
- Security considerations.
- Development team expertise.
- Ecosystem and available libraries.
- Deployment environment.
- Long-term maintainability.
- Integration requirements.

For EnterpriseFlow, Java is a suitable choice for backend development because it provides strong typing, mature enterprise frameworks, concurrency support and a substantial ecosystem.

**Key Point:** Programming languages provide the syntax and structures developers use to implement software logic.

---

# 9. Compiler and Java Virtual Machine (JVM)

This section is particularly important because it explains how Java source code becomes executable instructions.

## 9.1 What Is a Compiler?

A compiler is a software tool that translates source code written in a programming language into another representation that can be executed or processed by a runtime environment.

Depending on the language, a compiler may translate source code into:

- Machine code.
- Intermediate representation.
- Bytecode.

Compilers also identify certain errors during compilation.

For example, Java's compiler checks syntax and type correctness before generating bytecode.

## 9.2 Java Compiler (javac)

Java uses a compiler called `javac`.

The Java compiler translates `.java` source files into `.class` files containing Java bytecode.

Example source file:

`HelloWorld.java`

```java
public class HelloWorld {

    public static void main(String[] args) {

        System.out.println(
            "Hello, Software Engineering!"
        );
    }
}
```

Compile the source file:

```bash
javac HelloWorld.java
```

The compiler generates:

```text
HelloWorld.class
```

The `.class` file contains bytecode rather than ordinary processor-specific machine code.

## 9.3 What Is the Java Virtual Machine (JVM)?

The Java Virtual Machine (JVM) is an execution environment that runs Java bytecode.

It provides an abstraction between Java applications and the underlying operating system and hardware.

The JVM allows the same compiled Java bytecode to run on different operating systems, provided a compatible JVM implementation is available.

This principle is commonly summarized as:

**Write Once, Run Anywhere (WORA).**

For example, a Java application compiled on Windows can generally run on Linux or macOS without recompiling its source code, provided the target system has a compatible Java runtime.

## 9.4 Major Responsibilities of the JVM

### A. Class Loading

The Class Loader loads required Java class files into the JVM.

### B. Bytecode Verification

The Bytecode Verifier checks bytecode for structural and safety constraints before execution.

### C. Execution Engine

The execution engine executes Java bytecode.

It uses:

- An interpreter.
- Just-In-Time (JIT) compilation.
- Runtime optimizations.

### D. Memory Management

The JVM manages memory used by Java applications.

Important memory areas include:

| Memory Area | Purpose |
|---|---|
| Heap | Stores objects and arrays. |
| Java Stacks | Store method frames, local variables and execution state for each thread. |
| Method Area | Stores class metadata and related runtime information. |
| Program Counter Registers | Track execution position for each thread. |
| Native Method Stacks | Support native method execution. |

Modern JVM implementations may organize these areas differently internally.

### E. Garbage Collection

Garbage Collection (GC) automatically identifies and reclaims heap memory occupied by objects that are no longer reachable.

This reduces the need for developers to manually free ordinary Java objects.

However, garbage collection does not eliminate every memory-management problem. Applications can still suffer from memory leaks when unnecessary object references remain reachable.

## 9.5 What Is the Java Runtime Environment (JRE)?

The Java Runtime Environment (JRE) traditionally refers to the JVM together with the libraries and supporting components required to execute Java applications.

The Java Development Kit (JDK) contains the tools needed to develop Java applications, including:

- Java compiler (`javac`).
- Java launcher (`java`).
- Java debugger (`jdb`).
- Java development libraries.
- Runtime components.

Modern Java distributions often package these components differently, but the conceptual distinction remains useful.

| Component | Purpose |
|---|---|
| JDK | Development tools and runtime components. |
| JRE | Runtime environment and supporting libraries. |
| JVM | Executes Java bytecode. |
| javac | Compiles Java source code into bytecode. |

## 9.6 How Java Code Executes

The Java execution process follows these steps:

**Step 1: Write Source Code**

The developer writes Java instructions in a `.java` file.

**Step 2: Compile the Source Code**

The Java compiler (`javac`) translates the source code into bytecode.

**Step 3: Generate Class Files**

The compiler produces `.class` files.

**Step 4: Start the JVM**

The Java launcher starts the runtime environment.

**Step 5: Load Classes**

The Class Loader loads the required classes.

**Step 6: Verify Bytecode**

The JVM verifies the bytecode.

**Step 7: Execute Instructions**

The execution engine interprets bytecode and may compile frequently executed code into native machine code using JIT compilation.

**Step 8: Manage Memory**

The JVM manages memory allocation and garbage collection.

## 9.7 Java Compilation and Execution Example

Create a file called:

`AssetManagement.java`

```java
public class AssetManagement {

    public static void main(String[] args) {

        String assetName = "Dell Latitude Laptop";

        double purchaseCost = 1200000;

        System.out.println(
            "Asset Name: " + assetName
        );

        System.out.println(
            "Purchase Cost: ₦" + purchaseCost
        );
    }
}
```

Compile:

```bash
javac AssetManagement.java
```

Execute:

```bash
java AssetManagement
```

Expected output:

```text
Asset Name: Dell Latitude Laptop
Purchase Cost: ₦1200000.0
```

## 9.8 Java Execution Architecture

The relationship between the different components can be represented as follows:

```text
       JAVA SOURCE CODE
        AssetManagement.java
                |
                |
                v
       JAVA COMPILER (javac)
                |
                |
                v
         JAVA BYTECODE
        AssetManagement.class
                |
                |
                v
          CLASS LOADER
                |
                |
                v
        BYTECODE VERIFIER
                |
                |
                v
          JVM EXECUTION
              ENGINE
                |
          +-----+------+
          |            |
          v            v
      Interpreter    JIT Compiler
          |            |
          +-----+------+
                |
                v
       NATIVE MACHINE CODE
                |
                v
          OPERATING SYSTEM
                |
                v
              CPU
                |
                v
          PROGRAM OUTPUT
```

The diagram illustrates the conceptual execution flow. In practice, JVM execution and operating system interactions involve additional runtime components and optimizations.

**Key Point:** The Java compiler converts source code into bytecode, while the JVM executes that bytecode on the target platform.

---

# 10. How All Computer System Components Work Together

Understanding each component independently is useful, but a software engineer must also understand how they interact.

Consider an employee using EnterpriseFlow to register a company asset.

The following sequence takes place:

### Step 1: Application Launch

The employee opens the EnterpriseFlow application.

The operating system creates and manages the necessary application processes.

### Step 2: Memory Allocation

The operating system allocates memory resources to the application.

The browser or Java application loads the required instructions and data into RAM.

### Step 3: Instruction Execution

The CPU executes instructions required by the application.

### Step 4: Thread Execution

Different application threads may handle user requests, background operations and other activities.

### Step 5: Database Communication

The application communicates with a database server over the network.

The database server executes queries and processes data.

### Step 6: Persistent Storage

The database stores the asset information on persistent storage.

### Step 7: Response

The application receives the result and displays confirmation to the employee.

### Complete Interaction

```text
          EMPLOYEE
              |
              v
       ENTERPRISEFLOW
          APPLICATION
              |
              v
       OPERATING SYSTEM
              |
       +------+------+
       |             |
       v             v
      CPU           RAM
       |             |
       +------+------+
              |
              v
        APPLICATION
          PROCESSES
              |
              v
           THREADS
              |
              v
        DATABASE SERVER
              |
              v
           STORAGE
              |
              v
        SAVED ASSET DATA
```

For a Java backend, the JVM is also part of the application execution path.

The database server may have its own operating system processes, threads, memory and storage.

---

# 11. Why Computer Systems Knowledge Matters to Software Engineers

Software engineers must understand computer systems because software performance and reliability are directly affected by the underlying execution environment.

### 11.1 Performance Optimization

Understanding CPU and memory utilization helps engineers identify performance bottlenecks.

For example, a slow application may be experiencing:

- High CPU utilization.
- Insufficient RAM.
- Excessive garbage collection.
- Slow database queries.
- Storage I/O bottlenecks.

### 11.2 Memory Management

Understanding RAM, heap memory, stacks and garbage collection helps engineers prevent memory-related problems.

### 11.3 Concurrency

Understanding processes and threads helps engineers design applications that handle multiple users and requests efficiently.

### 11.4 Platform Compatibility

Understanding the JVM helps engineers deploy Java applications across different operating systems and environments.

### 11.5 Infrastructure Planning

Understanding CPU, RAM and storage requirements helps engineers determine appropriate server specifications.

For example, a PostgreSQL database server supporting ten branches may require more memory, storage performance and CPU capacity than a small development machine.

### 11.6 Troubleshooting

Computer systems knowledge helps engineers investigate application failures, memory exhaustion, high CPU usage, thread deadlocks and operating system errors.

---

# 12. Summary

A computer system consists of interconnected hardware and software components that work together to execute applications and process information.

The CPU executes program instructions and performs calculations. RAM provides temporary memory for active programs and data, while storage retains information permanently.

The operating system manages computer hardware and software resources. It creates and manages processes, allocates memory, controls devices and provides services to applications.

Processes represent running instances of programs, while threads provide individual execution paths within those processes.

Programming languages enable developers to express computational instructions. Compilers translate source code into another representation, and in Java, the JVM executes the resulting bytecode.

These components work together to make software applications possible.

For a software engineer building EnterpriseFlow, understanding these concepts is essential for developing applications that are efficient, reliable, secure and capable of operating in enterprise environments.

**Final Perspective:**

Software does not execute independently. Every application depends on processor instructions, memory, storage, operating system services and an execution environment.

A professional software engineer must understand not only how to write code, but also how that code is compiled, loaded, executed, managed and supported by the underlying computer system.

---

# 13. Learning Outcomes

After studying this document, the learner should be able to:

1. Define the CPU and explain its major components.
2. Explain how RAM works and why it is necessary.
3. Differentiate between RAM and persistent storage.
4. Identify different storage technologies.
5. Explain the responsibilities of an operating system.
6. Describe the role of the operating system kernel.
7. Differentiate between user mode and kernel mode.
8. Explain what a process is and identify its major states.
9. Explain threads and their relationship with processes.
10. Differentiate between concurrency and parallelism.
11. Identify different categories of programming languages.
12. Explain the role of a compiler.
13. Explain the relationship between Java source code, bytecode and the JVM.
14. Describe how computer system components work together when executing an application.

---

# 14. Review Questions

1. What is the CPU, and what are its primary responsibilities?
2. Explain the functions of the ALU, Control Unit and CPU registers.
3. What is the difference between CPU cores and clock speed?
4. What is RAM, and why is it considered volatile memory?
5. Explain the differences between HDD, SATA SSD and NVMe SSD.
6. Differentiate between primary memory and secondary storage.
7. What is an operating system, and why is it necessary?
8. Explain the responsibilities of the operating system kernel.
9. What is a process, and what happens when a program is executed?
10. Differentiate between a process and a thread.
11. Explain concurrency and parallelism.
12. What is a programming language?
13. Differentiate between low-level and high-level programming languages.
14. What is a compiler?
15. What is the difference between the JDK, JRE and JVM?
16. Explain how Java source code is converted into executable instructions.
17. What is Java bytecode?
18. How does the JVM manage memory?
19. What is garbage collection, and why is it important?
20. Explain how the CPU, RAM, storage and operating system work together when executing an enterprise application.

---

# 15. Practical Assignments

### Assignment 1 — Computer Hardware Investigation

Identify the hardware specifications of your computer.

Document:

- CPU manufacturer and model.
- CPU generation and number of cores.
- CPU clock speed.
- Installed RAM capacity.
- RAM generation (DDR4, DDR5, etc.).
- Storage type (HDD, SATA SSD or NVMe SSD).
- Storage capacity.
- Operating system and version.

### Assignment 2 — Operating System Investigation

On a Windows or Linux machine:

1. Identify running processes.
2. Identify their process IDs.
3. Monitor CPU utilization.
4. Monitor RAM utilization.
5. Identify applications consuming the most resources.
6. Identify available storage capacity.

Suggested Windows commands:

```powershell
Get-ComputerInfo

Get-Process

Get-CimInstance Win32_Processor

Get-CimInstance Win32_OperatingSystem

Get-PhysicalDisk

Get-CimInstance Win32_LogicalDisk
```

Suggested Linux commands:

```bash
lscpu

free -h

lsblk

df -h

ps aux

top
```

### Assignment 3 — Java Development Environment

Install a suitable JDK distribution.

Verify the installation:

```bash
java -version

javac -version
```

Create a Java program called `ComputerSystem.java`.

```java
public class ComputerSystem {

    public static void main(String[] args) {

        System.out.println(
            "Understanding Computer Systems"
        );

        System.out.println(
            "CPU executes instructions."
        );

        System.out.println(
            "RAM stores active application data."
        );

        System.out.println(
            "Storage retains permanent information."
        );

        System.out.println(
            "The operating system manages resources."
        );

    }
}
```

Compile the program:

```bash
javac ComputerSystem.java
```

Execute the program:

```bash
java ComputerSystem
```

Document the compilation and execution process.

### Assignment 4 — Process and Thread Investigation

Write a Java application that:

1. Displays the current thread name.
2. Creates two additional threads.
3. Assigns different tasks to each thread.
4. Executes the threads concurrently.
5. Displays the thread names during execution.

### Assignment 5 — Computer System Architecture

Create a diagram showing the relationship between:

- CPU.
- RAM.
- Storage.
- Operating System.
- Processes.
- Threads.
- Java Compiler.
- JVM.

Explain how each component participates in executing a Java application.

---

**Document Status:** Completed

**Next Learning Topic:** Data Representation, Binary Numbers, Bits, Bytes and Number Systems.
