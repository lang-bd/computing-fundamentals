# Computing Fundamentals (1940s – 2000)

> A bottom-up, hands-on syllabus and technical archive tracing the evolution of computing: from discrete boolean logic and relay circuits to modern microprocessors, compilers, network protocols, and operating systems up to the year 2000.

---

## 🧭 Project Objectives

Modern software engineering builds on heavy abstractions. The goal of this repository is to step backward through the layers:

* Understand hardware at the gate, register, and bus level.
* Explore how bare silicon transitions into machine code, assembly, and compiled languages.
* Trace how batch monitors evolved into preemptive, multi-user, protected-mode operating systems.
* Re-implement minimal simulators, assemblers, and kernel primitives to verify theory with code.

---

## 🗺️ Visual Architecture Map

```
=============================================================================
LEVEL 5: INTERNETWORKING & MODERN KERNELS (Late 1980s – 2000)
         TCP/IP, BSD Sockets, Virtual Memory, Monolithic & Hybrid Kernels
-----------------------------------------------------------------------------
LEVEL 4: MICROPROCESSORS & SYSTEMS PROGRAMMING (1970s – 1980s)
         8-bit/16-bit ISAs (8086, 6502), Real Mode, C Language, UNIX V6/V7
-----------------------------------------------------------------------------
LEVEL 3: TRANSLATION & SUPERVISORS (Late 1950s – 1960s)
         Compilers (FORTRAN, LISP), BNF Syntax, Time-Sharing (CTSS, Multics)
-----------------------------------------------------------------------------
LEVEL 2: STORED-PROGRAM COMPUTING (Late 1940s – 1950s)
         Von Neumann Architecture, Subroutine Stacks, Early Assembly
-----------------------------------------------------------------------------
LEVEL 1: PHYSICAL SUBSTRATES & BOOLEAN LOGIC (1930s – 1940s)
         Relays, Tubes, Gates (NAND/NOR), Adders, Turing Computability
=============================================================================

```

---

## 📖 Comprehensive Syllabus

### Phase 1: Physical Foundations, Logic & Computability (1930s – Late 1940s)

* **1.1 Formal Foundations & Computability**
* Alan Turing (1936): The Universal Turing Machine (UTM), halting problem, state transitions.
* George Boole: Axioms of Boolean algebra, truth tables, and canonical normal forms (SOP, POS).
* Claude Shannon (1937): Mapping Boolean logic to electrical switching circuits and relays.


* **1.2 Combinational & Sequential Circuits**
* Primitive gates (AND, OR, NOT, NAND, NOR, XOR).
* Half adders, full adders, ripple-carry adders, decoders, and multiplexers.
* Bistable multivibrators: SR latch, D latch, and edge-triggered D flip-flops.


* **1.3 First-Generation Electronic Machines**
* Konrad Zuse (Z3): Relay-based binary floating-point computation.
* John Atanasoff & Clifford Berry (ABC): Vacuum tubes, binary arithmetic, and regenerative capacitor storage.
* Eckert & Mauchly (ENIAC): Decimal ring counters, accumulator-based execution, and manual plugboard routing.



---

### Phase 2: The Stored-Program Paradigm & Early Systems (Late 1940s – 1950s)

* **2.1 Stored-Program Architecture**
* John von Neumann (EDVAC report, 1945): Instructions and data in a unified memory space.
* Von Neumann vs. Harvard architectures: Bus contention vs. dual-port isolation.
* The CPU core cycle: Instruction Fetch (IF), Decode (ID), Execute (EX), Memory (MEM), Writeback (WB).
* Delay-line memory (mercury tubes), Williams-Kilburn tubes, and magnetic drums.


* **2.2 Birth of Assembly & Subroutine Mechanics**
* Kathleen Booth (Birkbeck College ARC/APEXC): Invention of symbolic assembly language and mnemonic design.
* David Wheeler & Maurice Wilkes (EDSAC, 1949): "Initial Orders" loader, relocatable code, and the Wheeler Jump (subroutine return addresses).


* **2.3 Discrete Silicon & Core Memory**
* Bardeen, Brattain, and Shockley (1947): Bipolar junction transistors replacing vacuum tubes.
* Jay Forrester & An Wang: Coincident-current magnetic core arrays.



---

### Phase 3: Compilers, High-Level Languages & Time-Sharing (Late 1950s – 1960s)

* **3.1 Compiler Engineering & Grammar Design**
* Grace Hopper: A-0 system, FLOW-MATIC, and English-statement compilation (leading to COBOL).
* John Backus (IBM, 1957): FORTRAN—lexing, parsing, register allocation, and code generation.
* Backus-Naur Form (BNF) & ALGOL 60: Block structure, lexical scope, and structured control flow.
* John McCarthy (MIT, 1958): LISP—s-expressions, function pointers, and garbage collection mechanisms.


* **3.2 Early Operating Supervisors & Batch Processing**
* GM-NAA I/O (1956): First batch operating monitor for the IBM 704.
* Job Control Language (JCL), punch card spools, card-to-tape buffering, and hardware interrupts.


* **3.3 Interactive Computing & Time-Sharing**
* Fernando Corbató (CTSS, 1961): Time-slice round-robin scheduling and multiple user consoles.
* Multics (1965): Hierarchical file systems, dynamic linking, access control lists (ACL), and ring protection.
* Memory virtualization: Base-and-bounds registers, segmentation, and drum swapping.



---

### Phase 4: The Microprocessor Era, C & Classic UNIX (1970s – 1980s)

* **4.1 Microprocessors & Architecture Standards**
* Intel 4004 (1971), 8080, and MOS 6502: Internal registers, ALU flags, and instruction decoders.
* Intel 8086/8088: 16-bit registers, real-mode memory segmentation (`Segment * 16 + Offset`), and Interrupt Vector Tables (IVT).
* RISC vs. CISC principles: Single-cycle execution, load/store architectures, and deep pipelines.


* **4.2 UNIX & Systems Programming in C**
* Ken Thompson & Dennis Ritchie (Bell Labs, 1969–1973): Evolution from B to C; rewriting the UNIX kernel.
* Core abstractions: "Everything is a file descriptor", virtual file systems, standard I/O redirection.
* Process lifecycle primitives: `fork()`, `exec()`, `wait()`, and inter-process communication via `pipe()`.
* Inode-based disk layout: Direct blocks, single/double indirect blocks, and directory tables.


* **4.3 Personal Computer Operating Environments**
* Gary Kildall (CP/M): BDOS (Basic Disk OS), BIOS abstraction, and 8-bit disk formatting.
* MS-DOS/PC-DOS: FAT12/FAT16 file allocation tables, `INT 21h` service calls, `.COM` (flat 64 KB) vs. `.EXE` (relocatable) binary layouts, and memory extensions (EMS/XMS).



---

### Phase 5: Protected Mode, Networking & Millennium Systems (1985 – 2000)

* **5.1 32-Bit Computing & Memory Protection**
* Intel 80386: Global Descriptor Table (GDT), Local Descriptor Table (LDT), Interrupt Descriptor Table (IDT).
* Hardware Paging: Page Directories, Page Tables, 4 KB pages, and control registers (`CR0`, `CR3`).
* Ring 0 (Kernel) vs. Ring 3 (User Space) isolation, context switching, and page fault handling (`#PF`).


* **5.2 Computer Networking & Internet Protocols**
* ARPANET, Vint Cerf, and Bob Kahn: The layered TCP/IP reference architecture.
* Local area networking: Ethernet framing, CSMA/CD, MAC addressing, and packet collision handling.
* BSD Sockets API (1983): Socket descriptors, `bind()`, `listen()`, `accept()`, `connect()`, raw sockets, and packet dissection.


* **5.3 Modern POSIX, Open Source & NT Kernels**
* Richard Stallman (GNU, 1983): Free software toolchains, GCC, Make, and the C standard library.
* Linus Torvalds (1991): Monolithic design of the Linux kernel, task scheduling, and loadable kernel modules.
* David Cutler (Windows NT, 1993): Hybrid kernel architecture, Hardware Abstraction Layer (HAL), and executive objects.
* The Y2K Milestone: Two-digit date storage patterns in legacy codebases, binary remediation, and epoch handling.



---

## 📁 Repository Structure

```text
.
├── 01-logic-and-gates/
│   ├── boolean-eval/               # Truth table and circuit simulators in C
│   └── turing-machine/             # Discrete state-machine tape simulation
├── 02-early-architectures/
│   ├── cpu-8bit-sim/               # Minimal accumulator-based CPU simulator
│   └── von-neumann-vm/             # Stored-program fetch-decode-execute engine
├── 03-toolchains-and-compilers/
│   ├── two-pass-assembler/         # Opcode translation, symbol table, and binary generation
│   ├── recursive-descent-parser/   # Arithmetic expression AST generator
│   └── linker-loader-sim/          # Relocation address resolution
├── 04-microprocessors/
│   ├── 8086-real-mode/             # 16-bit boot sectors (512-byte MBR), BIOS interrupts
│   └── 6502-disassembler/          # Instruction set decoder and register state dumper
├── 05-operating-systems/
│   ├── unix-v6-study/              # Annotated kernel structures, process scheduler, and inode map
│   ├── protected-mode-boot/        # x86 transition from Real Mode to 32-bit Protected Mode
│   └── dos-internals/              # FAT12 directory traversal and MBR inspection
├── 06-networking-and-protocols/
│   ├── raw-packet-sniffer/         # AF_PACKET / raw socket frame analyzer
│   └── tcp-state-sim/              # 3-way handshake and sliding window state machine
└── docs/
    ├── architecture-notes/         # Deep-dive technical writeups and diagrams
    └── reference-papers/           # Index of seminal papers (Shannon, Von Neumann, Ritchie)

```

---

## ⚙️ Development Environment & Tooling

* **Host Platforms:** Linux (Ubuntu 22.04 LTS recommended) / POSIX environments.
* **Languages:** C (ANSI C89 / C99 standards), x86 Assembly (NASM / GNU Assembler `as`).
* **Build System:** GNU Make.
* **Emulators & Virtual Platforms:** QEMU (`qemu-system-i386`), Bochs, DOSBox.
* **Inspection & Debugging Tools:** GDB, `objdump`, `readelf`, `hexdump`, Wireshark / `tcpdump`.

---

## 📚 Essential Reading List

1. **Shannon, Claude E.** (1938). *A Symbolic Analysis of Relay and Switching Circuits*.
2. **Von Neumann, John.** (1945). *First Draft of a Report on the EDVAC*.
3. **Wilkes, M. V., Wheeler, D. J., & Gill, S.** (1951). *The Preparation of Programs for an Electronic Digital Computer*.
4. **Backus, John, et al.** (1957). *The FORTRAN Automatic Coding System*.
5. **Ritchie, Dennis M., & Thompson, Ken.** (1974). *The UNIX Time-Sharing System*.
6. **Lions, John.** (1977). *Lions' Commentary on UNIX 6th Edition with Source Code*.
7. **Patterson, David A., & Hennessy, John L.** *Computer Organization and Design: The Hardware/Software Interface*.
8. **Tanenbaum, Andrew S.** *Operating Systems: Design and Implementation*.

---

## 📜 License

This study repository and all accompanying code implementations are released under the [MIT License](https://www.google.com/search?q=LICENSE).
