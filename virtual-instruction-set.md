# Vikram Adve -Virtual Instruction Set Computing

traditional compilation for static languages
- since the early fifties
- linktime optimization in the 80s
- very little change
- machine code still shipped to machine that will execute

virtual instruction set
- shipping an IR
- much richer analysis and transformations
- install time
- just in time
- runtime optimizations to feed back
- not a new idea
- the idea was developed in the 70s at IBM

popular systems
- managed runtimes
- java, cil bytecode
- PTX (cuda), SPIR (OpenCL), LLVM (Renderscript), HSAIL
 - late stage translation to execution (GPUs)

performance and security (native code is pervasive)
- Perf: hpc applications, media, browsers, database systems
- Systems: operating systems, hypervisors, managed language runtimes, daemons

modern software archs.
- native compile is no longer a good match
- dynamic libraries
- user installed software extensions
- many layers of libraries and frameworks
- complex dynamic data structures

modern hardware
- varying memory hierarchies
- varying vector instruction sets
- varying gpu compute hardware
- varying hetero mobile procs

modern sec challenges
- browser extensions
- web pages, JS
- mobile application markets
- BYOD
- secure applications
- analysis requires a higher level rep than machine code
- PNaCL chrome, bytecode + sandbox

machine code analysis though?
- good enough?
- very hard, not good enough
- budget getting a machine code to IR rep then doing analysis
- budget could just be used in analysis

walking back is hard
- memory model is brutally complicated in compiled code rep
- advanced tools resort to dynamic analysis
- instrumentation breaks program
- ! some binary analysis is required

proposal
- all software should be shipped as virtual instruction sets
- different systems can use different isas
- small embedded systems are even ok (see dalvik)
- security is great
- no inherent perf penalties
- perf opportunities to take advantage of info on the machine using to compiled
- technically/commercially feasible / acceptable

components
- LLVM
- secure virtual arch
- hetero parallel VM (ongoing)
- whole system optimizations (new, ongoing)

LLVM
- frontends -> IR
- LLVM JIT/code gen on the machine
- JVM/CIL -> LLVM

IR
- looks a lot like asm
- ssa
- typed memory and registers

used by
- Apple for all compiled systems (native)
- Cray (native)
- OpenGL
- CUDA
- OpenCL
- Renderscript
- PNaCL
- Research

secure virtual arch
- llvm lives between kernel and proc
- almost like a hypervisor (not as privelaged)
- os makes systems calls through the IR
- OS on virtual instruction set
- delayed translation possible

porting an OS to SVA
- a bit of manual work
- take kernel, port to API (like a new arch)
- clang compiles to SVA
- linux has been ported linux/freebsd

lines modified during port
- 5k of 632k
- only for mem safety
- 0.80%

API for SVA-OS
- hardware control (syscall, page table, io)
- state manip (context switch, signal, manip program state)

What is SVA good for
- unique combination of properties
- like JVM and .NET can do program transforms
- OS supervision (like a hypervisor)
- new security solutions
 - memory safety for commodity kernel
 - control flow
 - restrict behavior
