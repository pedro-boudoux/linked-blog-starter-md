**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #binaryfiles #files #structs 

## What is stored in Binary Files?
A binary file stores the binary numbers that correspond to the letters or numbers that are being written into it.
It uses ASCII codes to store character values as numbers into the file.

### Binary Files vs Sequential Files
Both [[Binary Files]] and Sequential [[Files]] store ASCII characters in them, the only difference is how they do it.

Sequential Files contain only ASCII characters, while [[Binary Files]] contains only non-ASCII characters.

In Binary Files, text is still stored using ASCII, but using their 7-bit ASCII numerical code instead.

Numbers are stored in their binary format according to how many bytes their type takes up (`int` 4 bytes vs `float` 8 bytes).

Structures can also be stored in Binary Files. 

This is how an integer would be stored in a binary file:
```c
10383 -> 00000000 00000000 00010100 10001111
```
... if this number was stored in a text file, it would take up 5 bytes but since it was stored in a binary file it only takes up 4.

Binary representations can take up less space but cannot be edited by a text editor.

## Writing Data to Binary Files
Writing data to a binary file requires the `fwrite()` function. This writes the data in binary form (raw bits) and not as ASCII.
```c
fwrite(ptr, size, number, fptr);

// ptr = pointer to data that will be written to disk
// size = # of bytes in each element written
// number = # of elements to be written
// fptr = stream to write the file to
```

## Reading Data to Binary Files
Reading binary data from a binary file is done with `fread()`. It has the same parameters as `fwrite()`.
```c
fread(ptr, size, number, fptr);

// ptr = array that data will be stored in or address of data structure
// size = size of the array of elements
// number = number of array elements
// fptr = stream to read from
```

When `fread()` is used, the system is really just reading the number of bytes equal to *size $\times$ number* and places them all in the data structure (it does not read only one element at a time).

`fread()` ignores boundaries between elements, because it has no way of knowing where they are since [[Binary Files]] simply hold raw bits, it is up to the program to determine where those boundaries are, which shows how important it is to keep track of where the "cursor" reading the file is at.

## Reading and Writing Structures
When it comes to reading and writing structures, the programmer must take into consideration that structures are padded so that each element begins on a 4 byte boundary.

Consider the following structure:
```c
struct generic {

char letter;
int integer;
float decimal;

}

// NOTE THAT:
sizeof(int) = 4 bytes
sizeof(float) = 8 bytes
sizeof(char) = 1 byte
```

Looking at it, one would think that when writing a `struct generic` value to a file, it would take up `4+8+1 = 13` bytes. But you would be wrong to think that since structures are padded because variables that start on a 4 byte boundary are faster to manipulate by the computer.  So in this case the size of `char letter` gets brought up to 4 so that the size of the entire `struct generic` is actually 16 bytes.
*(I guess a simple way of remembering this would be saying that the size of structs are rounded up to the next multiple of 4)*





