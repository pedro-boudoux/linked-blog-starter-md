**Class:** [[Intermediate Programming]]
**Date:** 29-03-2025
**Topics:**  #gcc #compiler #compilation #commands 

gcc is the compiler we use to compile C code (duh).

## Actually Compiling
- To compile in C simply type the following command `pedro@archlinux$ gcc <filename.c>` and it will compile your code into an executable file.
- The command can take different arguments which determine how it will compile our file.

## Arguments

`-Wall`: enables the output of warning messages that we can use to avoid future problems in our program.
`-std=c99`: tells the compiler to use the C99 standard of the C programming language.
`-o <name>`: tells the compiler to name the output file to `<name>` rather than the default `a.out`.

