## Help
* man gdb - Gdb manuel
* gdb --help - Gdb help
* (gdb)help - List of classes of commands

* (gdb)help class - List a list of commands in that class
* (gdb)help all - List all commands
* (gdb)help command - Show full documentation of given command
* (gdb)apropos word - Search for commands related to given word


## Start gdb
* gdb progaram - Start gdb with given progarm
* (gdb)file progarm - Start gdb and load progarm
* gdb --args program arg1 arg2 ... - Start gdb and pass arguments
* gdb --pid pid - Start gdb and attach to process


## Show/Set arguments
* (gdb)show args - Show current arguments
* (gdb)set arg1 arg2 - set arguments for run


## Run
* (gdb)run - Run the progarm to be debugged
* (gdb)run arg1 arg2 ... - Run the progarm with given arguments


## Exit/Kill progarm 
* (gdb)detach - Detach from running progarm
* (gdb)kill - kill current executing progarm


## Quit gdb
* (gdb)quit - Quit gdb


## Source code
* (gdb)list - List source code
* (gdb)list function - List source code of given function
* (gdb)list file:function - List source code around given function in given file
* (gdb)list file:linenum - List source code around given linenum in given file


## Breakpoints
* (gdb)break location condition - Set a breakpoint on a given location if given condition is true. Location can be function, linenum, address
* (gdb)info breakpoints - Show breakpoints
* (gdb)delete breakpoint1 breakpoint2 ... - Delete given breakpoints or delete all breakpoints if no breakpoints are given
* (gdb)clear location - Clear breakpoints in given location. Location can be function, linenum, address
* (gdb)enable|disable breakpoint1 breakpoint2 ... - Enable or disable given breakpoints or enable all if no breakpoints are given


## Steping
* (gdb)next(n) - Step over to next line of code
* (gdb)step(s) - Step into subroutine if possible
* (gdb)nexti(ni) - Step over to next instruction
* (gdb)stepi(si) - Step into sub instruction if possible
* (gdb)finish - Continue until the current function returns
* (gdb)continue - Continue until it hints the next breakpoint


## Browsing data
* (gdb)print/fmt expression - Print the value of expression using given format, expresison can be registers(starting with $), address(starting with *), variables and functions(you can call them symbols)
* (gdb)x/fmt address - Print the value of given address using given format
* (gdb)display/fmt expression - Print the value of expression each time the program stops
* (gdb)enable|disable displaynum1 displaynum2 ... - Enable or disable display with given displaynum
* (gdb)info expression, show infos of given expression, expression can be address, breakpoints, watchpoints, displays, registers, etc

fmt is a repeat count followed by a format letter and a size letter.

Format letters are o(octal), x(hex), d(decimal), u(unsigned decimal), t(binary), f(float), a(address), i(instruction), c(char), s(string)


Size letters are b(byte), h(halfword), w(word), g(giant, 8 bytes)
## Stack
* (gdb)backtrack count - Print backtrace of all stack frames or innermost count frames
* (gdb)frame - Print current frame
* (gdb)up - Move up stack trace
* (gdb)down - Move down stack trace
* (gdb)info locals - Print locals variable in current frame
* (gdb)info args - Print function arguments


## Disassemble
* (gdb)disassemble expression - Disassemble a specified section of given expression, expression call be function(symbol), address
* (gdb)set disassembly-flavor - Set the disassembly flavor. The valid values are "att" and "intel", and the default value is "att".


## TUI
* (gdb)tui enable/disable - Enable/Disable gdb TUI interface
