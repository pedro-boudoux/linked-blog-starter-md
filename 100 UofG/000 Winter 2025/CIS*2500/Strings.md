**Class:** [[Intermediate Programming]]
**Date:** 29-03-2025
**Topics:** #strings #C #pointers 

## What are Strings?
Strings are arrays of characters in which a special character, *the null character* `\0`, marks the end.

### String Literals
A *string literal* (aka a string constant) is a sequence of character enclosed within double quotes.
```
char ch[10] = "abc"; 
// OR
char ch[] = "abc";
// OR
char * ch = "abc";
```
When the C compiler encounters a string literal of length `n` in a program, it sets aside `n+1` bytes of memory to store it plus the null terminator `\0` to mark the end of the string.

String literals are stored in the *Data part* of the memory (read-only). 
