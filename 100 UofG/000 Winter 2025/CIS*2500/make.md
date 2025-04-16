**Class:** [[Intermediate Programming]]
**Date:** 29-03-2025
**Topics:**  #makefiles #files #compilation #compiler #commands

## Makefiles
To make it easier to build large programs UNIX/Linux systems use the concept of a *makefile* and *make utility*.{{date:YYYY-MM-DD}}

### Writing makefiles
To get started on using the make utility, you first need to write your makefile.
A makefile is a text file containing the compilation instructions, telling our make utility how and what commands to execute in order to properly compile our complicated multi-file program.
Makefiles usually look like this:

```
output: main.o dependency1.o dependency2.o
	gcc -Wall -std=c99 main.o dependency1.o dependency2.o  -o output

main.o: main.c include.h
	gcc -Wall -std=c99 main.c

dependency1.o: dependency1.c include.h
	gcc -Wall -std=c99 dependency1.c

dependency2.o: dependency2.c include.h
	gcc -Wall -std=c99 dependency2.c

clean: 
	rm *.o output
```

#### Format
The first line of an instruction within a makefile has the target file, followed by its dependencies. 
The second line contains the command that must be executed in order to compile the target file.

## Make Utility
Once we have written our makefile we can use the *make utility* to build (or rebuild!) the program.

Typing in `make` into your terminal checks for the time and date associated with each file to determine if the files are all up to date and recompiles only the outdated files.

Running `make` automatically checks the current directory for a file named `makefile`.

You can also call `make <target>` to just make one of the targets listed in the makefile.

If you for some reason decided to name your makefile anything else other than makefile you can also use the make utility on it by typing `make -f <makefileName>`.

