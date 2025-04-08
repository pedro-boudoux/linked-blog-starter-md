**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #files #filemodes #binaryfiles #sequentialfiles #C 

## Sequential Access Files
[[Files]] that are read/written in a sequence, without moving around the cursor to any specific spot without having written something before doing so.

## Random Access File
Sometimes we don't want to just read/write to a file in order, often times we find ourselves needing to jump around the file to read specific or write specific values into it, reading/writing records in a *random* order.

This is especially useful for [[Binary Files]] since they contain only raw binary data which makes our cursor arithmetic especially useful for reading and writing data to them.

### Functions
#### Moving to a Location in the File
```
fseek(fptr, offset, from);
```
- `fptr` is the file pointer of the stream we're reading from.
- `offset` is how many bytes we want to offset from that position (negative for backwards, positive for forward).
- `from` one of 3 specific values that tell us where to seek from
	- `SEEK_SET`: beginning of the file
	- `SEEK_CUR`: from the current position
	- `SEEK_END`: from the end of the file

#### Knowing where the Cursor is
```
long int ftell(FILE * fptr);
```
The function `ftell()` takes the file pointer of the stream we're reading from and returns our current position in the file.
