Name: Meghan Murphy
COMP 3500 - Project 2 Submission

- Successfully built binutils and GCC.
- Git is set up and commits exist.
- Encountered fatal errors with System/161 that prevented OS/161 execution.
- Unable to run OS/161 due to missing sys161 configuration.
- Submitting work completed for partial credit.

### Reading Code Section

- `kern/main/main.c`: The main entry point of OS/161. It initializes the kernel, sets up core system components, and starts the first user process.
- `kern/syscall/syscall.c`: This file contains system call handlers, which allow user programs to interact with the OS kernel.
- `kern/thread/thread.c`: Handles thread management, including creating, running, and destroying threads in OS/161.

- System calls in OS/161 follow a structured process:
  - The user program makes a system call (e.g., `sys_read`).
  - The syscall is handled in `syscall.c`, which checks for valid arguments.
  - If needed, the call is passed to a lower-level function in `vfs.c` or another kernel component.

This is my analysis based on reviewing the source code.
