**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #files #binaryfiles #sequentialfiles #filemodes

## Different File Modes in C
File modes in C are needed when opening a file, it tells the program what type of operations we want to do with the file.
```
FILE* fptr = fopen(char * fileName, char * fileMode);
```
### The File Modes
File modes in C are as follows:

| Mode | Meaning                                                                                                         |
| ---- | --------------------------------------------------------------------------------------------------------------- |
| r    | opens *existing* file for reading information from it.                                                          |
| w    | *creates* a new file for writing information into it.                                                           |
| a    | *append* , writes to end of existing file.                                                                      |
| r+   | *opens existing file* for both *reading* and *writing*, starts at the beginning.                                |
| w+   | *creates new file* for both *reading* and *writing*, starts at the beginning and *truncates* the existing file. |
| a+   | *opens existing file* for reading and writing, writes to the end of the file                                    |
