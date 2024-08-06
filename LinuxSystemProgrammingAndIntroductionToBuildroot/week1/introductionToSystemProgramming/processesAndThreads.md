# Processes and Threads

## Processes
- Executable object code, running on hardware
    - ELF (Executable and Linkable Format)
- Necessary resources to run are allocated and managed by the kernel through system calls
    - timers
    - files
    - hardware resources
- referenced by Process ID (pid)
- run on virtualized processor and virtua view of memory
    - appears to software as its own dedicated RAM/CPU

---

## Threads
- unit of activity within a Process
- a proces may be single-threaded or multi-threaded
- each thread has:
    - stack - stores local variables
    - processor state/current location
- memory address space is shared between threads

---

## Linux Threads/Processes and memory
- each process has its own virtual memory
- each thread shares process virtual memory
- sharing memory access between thread?
    - access directly (use synchronization)
- sharing memory access between process?
    - user inter-process communication (IPC)

---

## Linux Signals
- One-way asynchronous notifications sent from:
    - kernel to process 
    - one process to another proces (IPC)
    - a process to itself
- processes setup signal handlers to control how to respond to a signal
    - example ctrl+c or SIGINT to stop a process 
- signal handlers must use signal safe functions which are safe to call asynchronously
    - use of global vars can introduce unsafe scenarios
    - process code can be interrupted at any time by signals

---

## Linux Interprocess Communication (IPC)
- allows process to exchange info without using a common global memor space
    - pipes 
    - semaphores
    - message queues
    - shared memory






































































    


