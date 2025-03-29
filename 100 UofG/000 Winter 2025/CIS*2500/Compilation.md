## Process of Compilation

### The Compiler
The compiler is what converts the code written in the language of your choice ([[gcc]] in our case) to machine readable code.

### Operations of the Compiler
Our compiler is responsible for two operations:
1. Compiling
2. Linking

#### Linking
The purpose of the compiler's linker is to include different useful libraries that contain useful code that we don't want to waste our time writing ourselves. 
It is useful to include the many libraries we use such as `stdio.h`, `stdlib.h`, `string.h` and many more!
It also links `.o` files that are not yet linked into a single executable program, useful for when your program has many `.c` files.

#### Compiling
As already mentioned, the purpose of compiling is to take the written code and convert it into machine readable code that can be executed.

### Multiple File Compilation
Multiple file compilation is how we compile and link multiple files together into a single executable. 
Here's the command for doing it:
	`pedro@archlinux$ gcc dependencyA.c dependencyB.c main.c -o program`
The two source files are first compiled into their own `.o` files and then sent to the linker and combined together into a single file.
A big problem with this is that it is objectively annoying to have to type this every time and to keep track of all our dependencies. So we use a tool called [[make]] to make our lives a lot easier.