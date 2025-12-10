[[Computing]]
#22/2/25
## Assembly Code
- Computers process instructions that are written in machine code only.
- Machine code has an operation code, also known as an opcode, and an operand.
- Assembly language uses mnemonics to represent operation codes and addresses.
- Suggest some typical assembly code mnemonics for common operations carried out by the processor.
## Registers and Accumulator
- In a more simple computer, all calculations may be carried out in a single register known as the "accumulator".
- Other computers can have up to 16 general purpose registers used to hold values that are needed temporarily to perform calculations.
- The assembly code instructions are different for every different computer architecture.
- All instructions for a given computer make up its instruction set.
## Five Common Operations

| Instruction             | Description                                                                                                         |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------- |
| LDA Rd, \<memory ref\>  | Load the value stored in \<memory ref\> into register d                                                             |
| STR Rd, \<memory ref\>  | Store the value in register d into the memory location specified by \<memory ref\>                                  |
| ADD Rd, Rn, \<operand\> | Add the value specified in \<operand\> to the value on the register n and store the result in register d            |
| SUB Rd, Rn, \<operand\> | Subtract the value specified by \<operand\> from the value in the register n and store the result in the register d |
| MOV Rd, \<operand\>     | Copy the value specified by \<operand\> into register d                                                             |
## Immediate and Direct Addressing
The instruction: `SUB R3, R2, #5`
	Uses immediate addressing. It uses the VALUE 5 as the operand.
The instruction: `LDR R1, 300`
	Uses direct addressing. It uses the memory address 300 holding the value as the operand.
## Adding Comments
- Adding a comment can make code easier to understand.
Example with comments:
	`LDR R1, 301  ;load contents of 301 into R1`
	`LDR R2, 302  ; load contents of 302 into R2`
	`ADD R1, R1, R2   ;add R2 to R1, store in R1`
	`LDR R3, 303  ; load contents of 303 into R3`
	`ADD  R1, R1, R3 ;Add R3 to R1, store in R1`
	`STR  R1, 304  ;store result in 304`
## Branch Instructions
- If statements do not exist in assembly language.
- Instead there are compare and branch instructions.

| Instruction            | Definiton                                                                                           |
| ---------------------- | --------------------------------------------------------------------------------------------------- |
| CMP Rn, \<operand>     | Compare the value stored in register n with the value specified by \<operand2>                      |
| B \<label>             | Always branch to the instruction at position \<label> in the program                                |
| B\<condition> \<label> | Conditionally branch to <label> if the last comparison met the conditions specified by <condition>: |
## While Loops
- The equivalent of a while loop can be written by using compare and branch instructions. This is simply done by having the place it branches to, before the branch instruction.
## Logical Bitwise Operators
Instructions to perform AND, NOT, OR, and XOR operations, look like this:

| Instruction             | Definition                                                                                                                                                       |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AND Rd, Rn, \<operand2> | Perform a bitwise logical AND operation between the value in register n and the value specified by \<operand2> and store the result in register d.               |
| ORR Rd, Rn, \<operand2> | Perform a bitwise logical OR operation between the value in register n and the value specified by <operand2> and store the result in register d.                 |
| EOR Rd, Rn, \<operand2> | Perform a bitwise logical exclusive or (XOR) operation between the value in register n and the value specified by <operand2> and store the result in register d. |
| MVN Rd, \<operand2>     | Perform a bitwise logical NOT operation on the value specified by \<operand2> and store the result in register d.                                                |

## Logical Shift Operations
- A logical shift to the left of one bit, moves all bits one place to the left.
Format of the instruction is:
	`LSL Rd, Rn, \<operand>`
		Logically shift the value stored in register n by the number of bits specified by \<operand> and store the result in register d
