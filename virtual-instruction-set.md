# Vikram Adve -Virtual Instruction Set Computing

Prof. Vikram Adve spoke about virtual instruction set computing and in particular the realization of the ideals of this concept in the LLVM compiler infrastructure. He started by giving an overview of traditional compilers and languages that focus on a monolithic approach to taking a source program and providing an executable. Generally there hasn't been much change in this pipeline since the 80s and machine code is still shipped to a machine that will execute it.

Instead, virtual instruction set computing, is a realization of the idea that a non arch-specific intermediate format can be shipped everywhere to execute on a backend that is arch-specific. Not only is this portable but there are much more interesting things that can be done with a higher level representation like IR (analysis, optimization, etc). There are many systems that subscribe to this ideal: Java, CLR, PTX (cuda), LLVM, etc.

He went on to highlight the importance of abstracting the hardware due to the varying way in which processors work and execute binaries today. He also went on to describe how this idea appears to be popping up in other contexts like PNaCL for the Chrome browser and its extensions.

Further, he contrasted attempts to perform similar feats with machine code and in particular he highlighted the difficulty of analysis for security or otherwise which is very high as you might expect. From performance to correctness machine code is simply not suitable for anything other than execution due to memory models which are non-deterministic or the requirement for dynamic analysis.

He concluded by highlighting the primary ideal: everything should be shipped as IR and not as binary. In their research they have even gone so far as to research the idea of a kernel built to IR for portability and on-the-fly security analysis when new modules are introduced. Through much hard work they have implemented large portions of the linux kernel with the help of the LLVM compiler infrastructure which is widely used all over the world today by companies like Apple.
