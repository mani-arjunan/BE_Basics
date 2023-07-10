`# Operating System Basics
    Operating system also known as OS, it is responsible for managing hardware
    running other programs, in os terms running a program is known as process.
* Load and manage processes(running programs).
* Provide interfaces to hardware via system calls(basically provide hardware components via interfaces to our programs eg: for games gpu etc).
* Provides File System.
* Provides basic user interface to interact with our os like launch a program, create a program using a programming language etc.

## Popular Operating System

* unix(a common structure for various family of os's like linux, apple os etc).
* Windows.
* Andriod.
* Apple etc.

## Device Driver

* Device drivers are usually used to control IO devices like keyboard, mouse etc.
* The os provides the interface from keyboard to the programs that are being used.

## Multiprocess

* The primary job of modern operating system is Multiprocess, meaning running multiple processes at the same time(concurrently).
* In this each core of the cpu can execute one code of a process at a time, 
also os's code will also run in the core of the cpu.
* Generally OS code runs on each cores inbetween the processes codes.
* Scheduler decides which process should take which core.
* pre-emptive multitasking
    * CPU receives interrupt.
    * interrupt stores the program counter(the value to maintain which program to run).
    * interrupt invokes handler(appropriate handler for the programs).
    * handler saves rest of state of the CPU for the process.
    * handler does its work.
    * handler invokes the scheduler.
    * scheduler selects which a process to run.
    * scheduler restores state of the CPU for that process.
    * scheduler jumps execution to that process.
    * round robin algorithm is used to determine which process to run next by the scheduler.
* Processes also shares the system memory.
* Its os's job to allocate memory to various processes, also to ensure one memory space is not getting duplicate allocation to another process.
* System calls are used by the processes to call any os specific things that are needed by the processes like file read/write, network requests etc.
* One Process cannot access another process memory address.

## Process storing memory
* code will be stored in a contiguous memory allocation(like array).
* stack will be used to store local variables for the processes, it is also a contigous space of memory address.
* heap will be used to store everything else.