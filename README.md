
# Risc V OS Kernel

Little functional OS for Risc V processor from scratch.

RiscV-64IMA(I- basic operations with integers, M- mul/div with integers, A-atomic operations)

Embedded-like system (1 physical thread, virtual memory is actual physical memory) 
### User api for implemented system calls
User api is given in files *"h/syscall_c.hpp
"* and *"h/syscall_cpp.hpp"* .

### Interrupt service routine
Riscv::supervisorTrap() is interrupt service routine for all interrupts, method is implemented in *"src/supervisorTrap.S"*. Causes of interrupt are:
- system call
- software interrupt, generated from timer (generates every 0.1s, pre-configured)
- external interrupt, generated from external controller
Basic hardware data is given in *"lib/hw.h"* .