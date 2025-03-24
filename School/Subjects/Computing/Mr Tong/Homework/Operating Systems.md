[[Computing]]
#21/11/24 

## What is an operating system?
- An operating systems acts as a bridge between the physical hardware of a compter and the user or application software.
	- A user is unable to directly communicate with computer hardware.
	- The operating system is stored on the computer's hard drive or SSD, (Secondary storage)
## Hiding the Complexities of Operation
- Complexities behind running operations are hidden from the end user via an Application Programming Interface, also known as an API.
- Users can click a mouse or issue commands to perform more complex operations without having to know how they are carried out.
- For example:
	- Switching between different programs
	- Loading and saving files
	- Recording and playing sounds.
## APIs
- An API serves as a sort of waiter in a restaurant.
- The user looks at the menu and gives the API/waiter your request.
- The waiter takes the request to the kitchen (operating system)
- The kitchen/operating system sends the prepared dish back to the user, via the water/API.
## Functions of an Operating System
- Behind the scenes of the virtual machine created by the OS, there are many functions provided:
	- Memory management
	- Peripheral management of input and output devices
	- Backup management
	- Processor scheduling
## Memory Management
- A computer allows many processes to be running and operating at the same time.
- For example you could listen to music, whilst writing a program, checking emails and printing a document from a web browser that is running in the background.
- The operating system allocates chunks of memory to each process.
- If there isn't enough memory, a program may be swapped out from the memory onto a disk or "virtual memory" and reloaded when needed to be activated.
## Processor Scheduling
- The operating system controls as to which programs can send data to the CPU in order to be processed.
- Instructions from many different operations are queued in order of importance.
## The Scheduler
- This is the operating system's module that is responsible for ensuring that processor time is used as efficiently as possible.
- There are many different ways of scheduling processes, using different scheduling algorithms, such as:
- Round Robin - Each process is given a time slice of the processor in order to use it.
- Shortest job next
- Priority based system
## Task Manager
- On Windows, Task Manager will show the processes that are actively running and the allocation of resources accordingly.
## Backup Store Management
- The operating system keeps track of where all files are stored on its hard disk, or external drives, and where there is space available to perform a save operation/backup.
	- Files can be listed, moved, deleted, protected among other operations.
## IO Device Management
- This communicates with Input and Output devices through the I/O controller, a part of the CPU.
- Checks that a required output device is switched on and ready to receive data
- Also deals with processor "interrupts" such as a printer giving an "out of paper" message.