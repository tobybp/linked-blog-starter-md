## Central Processing Unit (CPU)
- The CPU is similar to the human brain but it can't think for itself. 
- Controls, calculates and executes all instructions in a computer
- Processors have a number of different components, each with their own purpose.
	- Arithmetic Logic Unit (ALU)
	- Control Unit (CU)
	- Clock
	- General Purpose Registers
	- Dedicated Registers
## Arithmetic Logic Unit (ALU)
- The problem solving part of the processor.
	- Performs shifts, logical operations, and arithmetic on data.
	- Arithmetic operations include adding, subtracting, multiplication, and division.
	- Logical operations include AND, OR, XOR, NOR, NAND, NOT
	- Shift operations is moving bits either to the left or right in a register.
## Control Unit
- The part of the processor that coordinates all of the other components.
	- Each instruction gets decoded and accepted
	- Individual steps are taken in order to carry out this instruction, such as fetching addresses of data, or fetching the data itself.
	- Each step is kept in time using a clock.
## The System Clock
- This generates a regular ON/OFF signal that is used to keep operations in sync within the processor.
	- Actions generally carried out along the rising edge of the clock tick, when it switches from 0 to 1.
	- Actions take a fixed number of cycles to complete.
## General Purpose Registers
- Outputs from the ALU will need to be stored.
	- Rathe than writing data to RAM or Secondary storage (slow memory), processors contain lots of really fast memory known as registers used to temporarily store results of operations and instructions.
	- The processor can then immediately re-use these results in following actions, e.g. 1 + 2 + 3.
	- Some processors will have a singular general purpose register. This is known as the Accumulator.
## Executing Instructions
- Carrying out sequences of programming instructions will need lots of small bits of information to be held.
	- The processor also needs to hold the instruction that is currently being executed temporarily.
	- Also has to hold the addresses of data that is needed, and the data itself.
	- Keeps track of the instructions that are next to be executed.
## Dedicated Registers
- The processor will use the following dedicated registers:
	- Program Counter (PC), this holds the memory address of the next instruction that is to be executed.
	- Current Instruction Register (CIR), holds the current instruction.
	- Memory Address Register (MAR), holds the address that the processor needs to fetch or store data to.
	- Memory Buffer Register (MBR), temporarily holds data moving between the processor and the main memory.
	- Status Register (SR), holds the current state of operations. Used to set flags (carry or overflow) and detect error conditions.

![[Screenshot 2025-02-03 at 22.11.12.png]]
## Running Programs
- The processor's role is that it carries out instructions given by programs stored in memory.
	- The control unit coordinates the components of the CPU in order to work together to achieve this. Similar to the way a conductor controls an orchestra.
## Fetch-Execute Cycle
- Processors operate in distinct stages and these are used to carry out the program instructions.
	- This is repeated for each instruction within a program.
### Fetch
1) Address of next instruction is fetched from the PC.
2) PC incremented by 1.
3) Instruction stored in location addressed by mAR is transferred to MBR.
4) Instruction transferred from MBR to CIR.
### Decode
5) Instruction in CIR is decoded.
6) Additional data, if required by the instruction, is fetched from memory
7) ... and passed to the registers.
### Execute
8) Instruction is executed by the ALU.
9) Registers are used to store intermediate data or results.
10) The result is stored in the accumulator or general purpose register or memory.
## Factors Affecting Performance
- The fetch-execute cycle is triggered by the clock pulses
- The faster the clock speed, the faster the computer can execute instructions.
## Cache Memory
- Cache memory is a small amount of super fast memory that stores data frequently accessed by the processor.
	- Faster and smaller than RAM, larger and slower than a register.
	- Larger amounts of cache memory improves processing speed.
## Other Factors
- There are other factors that affect performance:
	- Number of cores, allows for more simultaneous instructions.
	- Word length, amount of data that can be processed by the CPU at the same time.
	- Address and data bus width.
## The Role of Interrupts
- An interrupt is a signal given by a software program or hardware device that is sent to the CPU.
## Interrupt Service Routine
- Depending on the type of interrupt, a routine will be run to service it.
- Once the interrupt is serviced, the original values of registers are retrieved and the cycle resumes where it stopped.