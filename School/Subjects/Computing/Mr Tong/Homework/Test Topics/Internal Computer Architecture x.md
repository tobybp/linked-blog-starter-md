[[Computing]]
#26/1/25
A computer system is any device that can take a set of inputs, process them into a useful outputs.
For example a Barcode reader takes an input, translates it to digits, validates, looks up product code, name and price, then outputs the product code, name and price. 
## Internal Hardware Components
- A computer system will use all of the hardware and software in order to run
## Parts of the Computer
- Processor
- Main Memory
- Address, control and data buses
- I/O Controllers
## Inside the Base Unit
![[Pasted image 20250126163115.png|600]]
## I/O Controllers
- These are external devices such as mice, keyboards, monitors, printers. 
- Often produced by different manufacturers.
- They cannot be simply connected to the processor.
- An I/O controller for each peripheral acts as an interface between the device and the computer system.
## Device Drivers
- The software that interacts with the I/O controller is called a device driver.
- When you get a new device and plug it in, it is likely that you will need to install new drivers in order for it to communicate with your computer properly.
## Tasks of an I/O Controller
- Converts signals from peripherals into a format that the computer can process, and the other way around.
- Receives I/O requests from CPU and sends control signals to the device it needs to control.
- Also manages data flow to and from the device. This frees the CPU to get on with other processes.
## Sending Information via Buses
- The control bus is used to send control signals.
- The data bus sends the data between the components of the CPU
- The address bus sends memory addresses from the processor to other CPU components.
## System Buses
- The system bus comprises three separate buses.
- Notice the direction of the arrows:
![[Screenshot 2025-01-26 at 17.00.18.png]]
## Control signals
- Memory read: causes data from the addressed location to be placed on the data bus.
- Memory write: causes data on the data bus to be written into the addressed location.
- Bus request: indicates that a device is requesting use of the data bus.
- Bus grant: indicates that the CPU has granted access to the data bus.
- Clock: Used to make sure that operations are in sync.
## Bus Definition
- Buses in a computer consist of a series of parallel wires that transfer data signals between internal components.
- Typically consist of 8, 16, 32, 64 lines of wires.
## Words
- Memory is divided in equal units called `words`.
- Word length is usually 8, 16, 32, 64 bits.
- Each words has a separate memory address.
## Data Bus
- The data bus is bi-directional as data can be sent both directions along the bus.
- The width of the bus is defined by the number of wires or lines it contains.
- If the data bus is the same width as a computer `word`, data can be transferred to and from memory in one singular operation.
	- If there are 16 lines, and a word is 32 bits. It will require two memory access and data transfer operations.
- Bus width affects system performance.
## Address Bus
- This bus carries the address of a memory location in ONE direction from the processor towards the I/O controllers and memory.
- The width of the an address bus determines the maximum possible memory addresses of the system.
## Main memory
- Main memory stores all of the data and instructions that are next to be processed.
- The number of memory addresses is limited by the width of the address bus.
- Each address stores a fixed number of bits determined by the type of processor.
- The smallest addressable unit is a `word`.
## Reading data from memory
![[Pasted image 20250126172123.png]]
## Multipurpose Machines
	- Early on, computers calculated an output using fixed instructions. The could only perform one set of instructions.
- A general purpose computer can perform many different tasks at different times.
- Their programming is not fixed.
- To achieve this, computers are designed in order to allow data and instructions to be stored. This is called the "stored program concept".
## Stored Program Concept
- Machine code instructions are loaded into main memory to be executed by the processor.
- The instructions are fetched one at a time and executed immediately by the processor in order.
## John von Neumann
- The most common implementation of this concept is the von Neumann architecture.
- Instructions and data are stored in a common main memory and transferred using a single shared bus.
## Harvard Architecture
- An alternative model separates the data and instructions into different memories using separate buses.
	- Program instructions and data no longer compete for the same bus.
## Programs and Data Buses
- Program instructions and data may be stored in unequal quantities.
- The Harvard architecture means that different sized memory spaces and word lengths can be used for data and instructions.
	- This is most commonly used in embedded systems with special functions rather than general purpose applications.