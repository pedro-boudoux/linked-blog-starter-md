**Class:** [[CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #memory #pointers

## Memory and Pointers
As mentioned before, a pointer is a programming language object that "points to" the memory address of a specified object type.
```c
int val = 10;
int * intPtr = &val;
```
`intPtr` here points to the memory location of the variable `val`.

NOTE: `int* x` means that `x` is a pointer to an integer, *not* an integer.

The `&` operator allows us to discover the address of a variable. When using it in front of a variable, it will tell us the memory address of where that variable is stored.

### Dereferencing
Once you have the address of a variable, you can use it to access the value by dereferencing the pointer using the `*` operator.
```c
int count = 7;

int *ptr = &count;

print("%d\n", *ptr);
```
The above snippet of code declares a variable `count` and then a pointer `ptr` that points to `count`, it then prints the value stored in the memory location that `ptr` points to by using the `*` operator seen in the print statement.

## Null Pointers
`NULL` pointers simply show that the pointer variable doesn't currently point to any location.

## Pointer Arithmetic
C allows us to perform arithmetic (addiction and subtraction) on pointers to array elements.

This gives us an alternative way of accessing the values stored in the array.

```c
int arr[5];
int * p = &arr[0];
```
`p` is a pointer to an integer that points to the first element of `arr`.

If we add an integer `x` to `p`, `p` will then point to the element `x` places after `p` .

Here is a table that should simplify this a little

| Value  | Adress    |
| ------ | --------- |
| `a[0]` | 1000-1003 |
| `a[1]` | 1004-1007 |
| `a[2]` | 1008-1011 |
so if there is a pointer `aPtr = &a[0]` adding 4 to `aPtr` such that `aPtr` becomes `aPtr += 4` would make `aPtr == &a[1]`.
