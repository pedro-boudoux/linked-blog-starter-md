**Class:** [[CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #memory #C #datastructures #algorithms


## What is Memory?
Memory is the internal storage of the computer, it is organized as a series of bytes each of which has its own address.

| Value | Address |
| ----- | ------- |
| P     | 1000    |
| e     | 1001    |
| d     | 1002    |
| r     | 1003    |
| o     | 1004    |
| \0    | 1005    |
## Pointers
[[Pointers]] are programming language objects where the values "points to" the location (the memory address) where another object is stored.

For more information on [[Pointers]], see [[Pointers]].

## How Arrays are stored
Arrays are just a sequence of memory locations.
Consider the following array:
```
int arr[5] = {1,2,3,4,5};
```
when looking at its memory addresses, it will look like this

| Variable | Address |
| -------- | ------- |
| `arr[0]` | 1000    |
| `arr[1]` | 1001    |
| `arr[2]` | 1002    |
| `arr[3]` | 1003    |
| `arr[4]` | 1004as  |
You can access the address of an element in an array by using `&(a[3])`.
