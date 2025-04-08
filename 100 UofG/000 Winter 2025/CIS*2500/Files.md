**Class:** [[CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #binaryfiles #files #C #sequentialfiles


There are two types of files which we will be touching up on in this course, they are:
	1. *Sequential Files*
	2. [[Binary Files]]

This note will be going over *Sequential Files*, since when most people think of files they think of sequential files anyway.

## Sequential Files
Normal `.txt` files that we normal humans can read and understand without having to sacrifice a baby goat (unlike [[Binary Files]]).

### Writing Data to Sequential Files
```c
FILE* fptr;
fptr = fopen(fileName, "w");
if (fptr == NULL) {
	// failed to write file
	return -1;
}

// write data to file here and stuff

fclose(fptr);
```

#### fprintf()
The function we use to write data onto our text file is `fprintf()`, it has the following prototype:
```c
int fprintf(FILE* fptr, const char* data);
```
... here is an example of it at use:
```c
int x = 10;
fprintf(fptr, "My favourite number is %d", x);
```
... and that results in a text file looking like:
```
My favourite number is 10
```

### Reading Data from Sequential Files
```c
FILE* fptr;
fptr = fopen(fileName, "r");

if (!fptr) return -1; // if fptr is NULL return -1 for error

// data reading and stuff goes here

fclose(fptr);
```

#### fscanf()
Function used to read values from a sequential file, reads data from the file until the end-of-file has been reached. The function `fscanf()` has the following prototype:
```c
int fscanf(FILE* fptr, const char* format);
```
... here is an example of it at use:
```c
fscanf(fptr, "%d", &arr[i]);
// this will read an integer from a file and store it at the
// ith element of arr
```

### Closing Files
One thing we need to do no matter whether we are reading, or writing to a file is that we must close the file stream.

To do that, we use the function `fclose()`, which takes only one argument, `fptr`.
```c
fclose(fptr);
```
What is basically does is that, once we're done doing whatever operation we were doing with the file, we close access to the file by freeing `fptr` to avoid memory leaks or any other unwanted behaviour.

## File Reading Modes
For file modes, please visit [[File Modes]], I don't want to include it in this note because it pertains to both binary and sequential files.