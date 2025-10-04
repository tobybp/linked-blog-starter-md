[[Computing]]
#9/2/25
### What’s an Instruction Set?

Think of an instruction set like a set of rules that tells a processor what it can do. Each type of processor has its own set of instructions, but many of them perform similar tasks, just in different ways.

---

## Types of Instructions

Processors can carry out different types of operations, including:

- Data Transfer – Moving data around (e.g., `LOAD`, `STORE`)
- Arithmetic Operations – Basic math (`ADD`, `SUBTRACT`)
- Comparison Operations – Checking values (e.g., `CMP` to compare numbers)
- Logical Operations – Working with binary logic (`AND`, `OR`, `NOT`)
- Branching – Changing the order of execution (e.g., conditional/unconditional jumps)
- Shift Operations – Moving bits left or right within a register

---
## Machine Code & Instruction Format

Processors don’t understand human languages – they only process machine code, which is a combination of 1s and 0s. The way instructions are stored and processed depends on the processor's word length (how many bits it uses for instructions).

### Typical Instruction Structure

Each instruction is split into two main parts:

1. Opcode (Operation Code) – The actual command (e.g., `ADD`, `SUB`, `LOAD`)
2. Operand(s) – The data used in the operation (this could be a value, memory address, or register)

Example format for a 16-bit processor:

|Opcode|Addressing Mode|Operand|
|---|---|---|
|4 bits|2 bits|10 bits|

---

## Operands & Addressing Modes

The operand refers to the data being used, which can be:
1. An actual value (e.g., `12`)
2. A memory address (where the data is stored)
3. A register (temporary storage inside the CPU)

The addressing mode (often 2 bits long) tells the processor how to interpret the operand.
### Addressing Modes: Immediate vs. Direct
- Immediate Addressing (Mode: `00`)
    - The operand itself is the actual data (e.g., `12` means use the number 12).
    - Limitation: You can’t modify the value during execution.
    
- Direct Addressing (Mode: `01`)
    - The operand is an address, meaning the processor has to go fetch the actual data from memory.

There are other addressing modes too, but we don't have to know them

---

## High vs. Low-Level Languages

- Machine Code - Pure binary instructions (hard to read and write).
- Assembly Language - Uses mnemonics (`LDA`, `ADD`, `MOV`), easier than machine code but still tricky.
- High-Level Languages - Python, Java, etc. (easier for humans to understand).