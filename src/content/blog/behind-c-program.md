---
title: "What Actually Happens When You Run a C Program?"
description: "A systems-level walkthrough of how a C program is compiled, loaded, executed, and terminated."
pubDate: 2026-11-16
tags: ["Systems", "C", "Operating Systems"]
---

# What Actually Happens When You Run a C Program?

## Introduction

When we run a program from the terminal, the operating system and hardware perform a series of steps before, during, and after our code executes.

This article follows a simple C program from source code to process termination.

**Questions to keep in mind:**
- What turns source code into an executable?
- What happens when we ask the operating system to run that executable?
- How is the program represented in memory?
- How does the CPU execute its instructions?

## 1. From Source Code to Executable

### 1.1 Preprocessing
- What does the preprocessor do?
- How are header files and macros handled?
- What does the preprocessed source look like?

### 1.2 Compilation
- How is C translated into assembly?
- What kinds of optimizations can the compiler perform?
- What is the role of the compiler?

### 1.3 Assembly
- What is an assembly language instruction?
- What does the assembler produce?
- What is an object file?

### 1.4 Linking
- Why do object files need to be linked?
- What are symbols and symbol resolution?
- Static linking vs. dynamic linking

## 2. Starting a Program

### 2.1 Executing a Program
- What happens when we enter `./program` in a shell?
- What role does a system call such as `execve()` play?
- What is the difference between a program and a process?

### 2.2 Process Creation and Loading
- How does the operating system load an executable?
- Where do the program's instructions and data go?
- What initial state does the process need before execution?

## 3. A Process's Address Space

### 3.1 Virtual Memory
- Why does each process have a virtual address space?
- How is virtual memory different from physical memory?
- What are pages and page tables?

### 3.2 Memory Layout
- Text segment
- Initialized and uninitialized data
- Heap
- Stack

### 3.3 Stack and Heap in Practice
- Where do local variables live?
- How do function calls use the stack?
- What happens when memory is dynamically allocated?

## 4. Executing Instructions

### 4.1 The CPU and Machine Instructions
- What are registers and the program counter?
- How does the CPU fetch and execute instructions?
- How does compiled C map to machine instructions?

### 4.2 Function Calls
- What happens when one function calls another?
- What information is stored in a stack frame?
- How does a function return to its caller?

## 5. System Calls and Interaction with the OS

- What is a system call?
- How does a program request services from the operating system?
- Example: reading input or writing output

## 6. Program Termination

- What happens when `main()` returns?
- What does `exit()` do?
- How does the operating system reclaim process resources?

## Conclusion

Summarize the path from source code to process termination. Revisit the central idea: running a program involves cooperation between the compiler, linker, operating system, memory system, and CPU.

## References

- Bryant and O'Hallaron, *Computer Systems: A Programmer's Perspective*
- [Add relevant documentation and supplementary sources here]
