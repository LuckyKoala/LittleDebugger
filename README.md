## Little Debugger

### 原理与工具

* [ptrace()](https://man7.org/linux/man-pages/man2/ptrace.2.html) 进程追踪与调试，可以观察和控制另一个进程，查看和修改被追踪进程的内存和寄存器
* [Library to Instrument Executable Formats](https://lief.quarkslab.com) 不同系统的可执行文件格式各不相同，如 [ELF(Linux)](https://linux.die.net/man/5/elf), [PE(Windows)](https://docs.microsoft.com/en-us/windows/win32/debug/pe-format) 和 [MachO(OSX)](https://developer.apple.com/library/archive/documentation/Performance/Conceptual/CodeFootprint/Articles/MachOOverview.html)
* [The DWARF Debugging Standard](http://dwarfstd.org) 调试文件格式，被许多编译器和调试器用于支持源码级别的调试
* [Processor register](https://en.wikipedia.org/wiki/Processor_register) 寄存器
* [Call stack](https://en.wikipedia.org/wiki/Call_stack) 调用栈，每个子过程会创建新的栈帧，包含返回地址，参数等

### Roadmap

* breakpoint(int 3, SIGTRAP, debug register) on function/line (symbol table / line number table)
* display assembly nearby
* read/write register/memory
* watchpoint
* backtrace(call stack)
* single step(ptrace)
