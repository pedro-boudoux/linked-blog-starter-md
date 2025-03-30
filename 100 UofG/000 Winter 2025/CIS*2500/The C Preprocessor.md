**Class:** [[CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #C #compilation #macros #includes #conditionalcompilation

The C preprocessor is a process that occurs before [[Compilation]].

It performs 3 operations all of which involve replacing something in the code before sending it over to the compile to turn it into an executable.

## Macro Processing
Macro Processing substitutes values and operations in the code. This means that they do not exist in the memory during runtime and are instead stored with the machine code and behave as if they were manually written into the machine code in the first place.

```
#define LINE_LENGTH 1024
```

Anywhere in your code where `LINE_LENGTH` is used, will be replaced by 1024.

It is a convention to write macro names in UPPER CASE.

Anything beginning with a `#` is a macro, which is defined at the top of the program.

As mentioned before, macros are nice because they're stored with the machine code, meaning that unlike functions, there is not any overhead memory usage.

## Includes
Used for including C header files in your program.
```
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include "myHeaderFile.h"
```
<> is used for system header files that are already built in, "" is used for user header files written by other people (like you!).

## Conditional Compilation
Allows/disallows the compilation of sections of the program based on the outcome of a test performed by the preprocessor.

This is good for testing code.

This is how you include a conditional code snippet into your program, this is awesome for debugging and I wish i attended that lecture:
```
#if *expression*

// code that is only executed if the expression is true

#endif
```

Here's how you can use this to have a debug mode for your program:
```
#ifdef DEBUG // means the code executes iff DEBUG exists

// code goes here

#endif
```
... then we can turn on debugging by compiling with the following [[gcc]] command:
```
pedro@archlinux$ gcc myProgram.c -o output -DDEBUG
```

