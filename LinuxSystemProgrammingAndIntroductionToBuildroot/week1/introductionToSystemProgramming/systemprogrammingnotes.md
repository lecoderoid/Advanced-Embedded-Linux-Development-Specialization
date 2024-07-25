# System Programming
- what is a system software
    - interfacing with the kernel and C lib
    - gui, compiler, debugger, web server, debugger-
- differences relative to *Application Software"
    - does not use higher level libs
    - less os/hardware details abstracted

## Cornerstone of System Programming
- System Calls (syscalls)
    - kernel function invocations from user space (read(), write()). Roughly 300 total
    - shared subset of ~90% implemented by all architectures on linux
- C library (libc)
    - GNU libc (glibc) wrappers for syscalls, threading support and applications
- C Compiler/linker (toolchain)
    - GCC (GNU C compiler)

---

## Invoking System Calls

- not possible to link you user space apps with the Linux kernel
    - not allowed for security/reliability reasons
- how do you invoke syscalls?
    - use a *trap* -  typically a software interrupt
## API (Application Programming Interface)
- is a definition of a piece of software can talk to another piece of software
- software which provides an API is the implementation
- ensures source compatibility
    - source can be compiled for different platforms, works in a specific way
- source code remains portable across diffrent hardware platforms/revisions ex. clib functions like printf(), strcpy()
- exceptions: syscall ~10% architecture differences mentioned

---

# ABI (Application Binary Interface)

- calling conventions, byte ordering, register use
- ensures binary compatibility
- defined/implemented by kernel and toolchain
- defines application interaction with itself, libs, kernel
- byte code specific hardware types, software, compiler/library revisions. Requires match: 
     - [x]  hardware
     - [x] software libraries(especially glibc) 
     - [x] compiler
---

## POSIX (Portable Operating System Interface)

- C APIs for unix-like os 
- started by IEEE in the late 1980s as a way to coalesce the "Unix Wars"
- Open Software Foundation created the Single Unix Specification (SUS)
    - Specification was free
    - eventually incorporated the POSIX standard
- POSIX defines C code API for many concepts
    - file and directory operations
    - clocks and timers
    - semaphores
    - shared memory
    - threads


























































































































