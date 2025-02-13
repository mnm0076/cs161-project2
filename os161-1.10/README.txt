Name: Meghan Murphy
COMP 3500 - Project 2

### Completed Tasks:
- Successfully built Binutils and GCC.
- Git is set up and commits exist.
- Reading Code section is completed.
- Encountered fatal errors with System/161 that prevented OS/161 execution.
- Unable to run OS/161 due to missing sys161 configuration.
- Submitting work completed for partial credit.

### Reading Code Section

- `kern/main/main.c`: This is the main entry point of OS/161. It performs the **initial kernel boot sequence**, initializes core components like the console, thread scheduler, and virtual memory system. It also prints the OS version and build information.
  
- `kern/syscall/syscall.c`: Handles **system call execution**. When a user program makes a system call (e.g., `sys_read`), this file **validates arguments and routes execution** to the appropriate kernel function.

- `kern/thread/thread.c`: Manages **threads and process scheduling**. It provides functionality for creating, running, and terminating threads within OS/161.

### System Call Execution Process:
1. **User program makes a system call** (e.g., `sys_open`).
2. **Control goes to `syscall.c`**, which **validates input and checks permissions**.
3. **If valid, `syscall.c` routes execution to a lower-level function**, such as `vfs_open()` in the virtual file system.
4. **The kernel executes the requested operation** and **returns control to the user program**.

This analysis is based on reviewing OS/161 source code.

### Debugging with GDB

Although I was unable to fully debug OS/161, I researched the GDB debugging process. OS/161 uses `sys161-gdb` for debugging, and the common workflow is:

1. Compile OS/161 with debugging symbols using `-g` flag.
2. Run `sys161 -w kernel` to start OS/161 in debug mode.
3. Use `gdb kernel` to attach to the running instance.
4. Set breakpoints with `break function_name` and step through execution.

Due to the Sys161 failure, I could not fully execute these steps, but I understand the debugging process.


