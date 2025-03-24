[[Computing]]
#1/12/24 

## **Assembler and Assembly Language**

- **Translation Requirement**: All programs must be translated into machine code before execution.
- **Assembler Function**: Translates assembly language into machine code.
    - Typically, one assembly code instruction maps to one machine code instruction.
    - Each processor type has its own assembly language and assembler program.

---

## **Source Code and Object Code**

- **Source Code**: The input to the assembler, written in assembly language.
- **Object Code**: The machine code output produced by the assembler.
    - Object code can be saved and executed whenever needed.

---

## **Uses of Assembly Language**

- Assembly language is used when:
    - Execution speed is critical.
    - Memory usage must be minimized.
    - Manipulation of individual bits and bytes is required.
- **Examples**: Embedded systems, real-time systems, sensors, mobile devices, device drivers, and interrupt handlers.

---

## **Compilers**

- **Function**: Translates high-level language (e.g., Visual Basic, Delphi) into object code.
- **Platform-Specific**: Different hardware platforms require specific compilers to produce machine code.

#### **Compilation Process**

- **Phases of Compilation**:
    - Lexical analysis
    - Syntactic analysis
    - Semantic analysis
    - Intermediate code generation and optimization
    - Final machine code generation (only if no errors are found)

#### **Errors Detected by the Compiler**

- Syntax errors
- Missing subroutines
- **Output**: Produces relocatable code if errors are absent, as the compiler does not know the absolute addresses for the object code.

#### **Advantages of a Compiler**

- Object code can run without needing the compiler.
- Faster execution than interpreted code.
- Object code is more secure—harder to reverse-engineer or modify.

---

## **Interpreters**

- **Function**: Translates high-level code into an intermediate form and executes it line by line.
- **No Object Code**: Unlike compilers, no standalone object code is produced.
- **Error Detection**: Scans for syntax errors and stops at the point of error during execution.

#### **Advantages of an Interpreter**

- Useful for educational environments (interactive mode).
- Allows testing of small code sections without recompiling the entire program.
- Available for most high-level programming languages.

---

## **Portability**

- **Platform Dependency**: Machine code generated for one platform (e.g., x86) cannot run on another (e.g., Apple).
- **Bytecode**: Java compiler produces bytecode, which is platform-independent.
    - Requires a JVM (Java Virtual Machine) to translate bytecode into machine code for each platform.

---

## **Using Bytecode**

- Translated bytecode subroutines retain their machine code for future use.
- If a subroutine is not used during runtime, it remains uncompiled to machine code.

---
