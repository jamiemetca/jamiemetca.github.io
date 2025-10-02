02/10/2025

# Setting up C toolchain

Documentation of the steps to setup the GCC toolchain

## Toolchain flow
(C source file) -Compiler-> (Assembly file) -Assembler-> (Object file) -Linker-> (Executable)

For project with more than one source files and libraries it looks more like this;

(C source file) -Compiler-> (Object file #1)
(C source file) -Compiler-> (Object file #2)
(C source file) -Compiler-> (Object file #n)
(Library object file #1)
(Library object file #2)
(Library object file #n)
                                        
All object files would then be organised into an executable by the linker.

## Installing toolchain
- sudo apt update
    - Update packages
- sudo apt install build-essential
    - Install build-essentials includes gcc and other packages such as make which may be useful

## Compile and run file
- gcc hello-world.c -o hello-world
    - without the -o flag. gcc will create an a.out file
    - -o tells gcc to name the file hello-world

./hello-world
    - This runs the executable
