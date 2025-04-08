**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 01-04-2025
**Topics:** [[Functions]], [[Pointers]]

## Functions Pointers
A *pointer variable* (see [[Pointers]]) can point to almost anything, including *functions*. 
Below is an example of the initialization of a *function pointer*:
```c
#include <stdio.h>

void printMe(int number) {

printf("printMe: You passed me the number %d \n", number);

}

void (*printMePtr)(int);
printMePtr = &printMe;

```
In the snippet above we define a function `printMe`, then in line 9 we create a pointer to a function that returns `void` and takes an `int` and we call it `printMePtr`, then in line 10 we make that pointer point to the address of `printMe`.

After initializing a *function pointer variable*, we can call it by doing the following:
```c
	(*printMePtr)(10);     // calls and function and passes 10
```

*Function Pointers* point to executable code.

We can *not* allocate nor free memory using function pointers.

A *function pointer* can be passed as an *argument* and can be *returned from a function*.

### Function Pointer Arrays
Just like how we can declare arrays of regular *pointers*, we can also declare arrays of *function pointers*. We can use them instead of a switch statement. Below is a *pointer function array* declaration:
```c
void (*funcPtrArray[]) (int, int) = {func1, func2, func3};
```
This declares an *array of function pointers* named `func1()`, `func2()`, and `func3()`.

Below is an example of *function pointer arrays* in use:
```c title:"Function Pointer Array usage example"
#include <stdio.h>
#include <string.h>

void func1 (char *);
void func2 (char *);
void func3 (char *);

int main () {

	void (*funcPtrArray[])(char *) = {func1, func2, func3};
	int flag = 0;

	while (flag != -1) 
	{
		printf("Enter the function number (1,2, or 3):");
		scanf("%d", &flag);

		if (flag < 4 && flag > 0) {
			(*funcPtrArray[flag-1]) (string);
			// ^ that will call the selected function
		} else {
		flag = -1;
		}
	}

	return -1;

}
```

## Applications of Function Pointers and [[Generic Pointer]]s

### A Search Function
Sets the array pointer to a char pointer since chars are 1 byte and we can easily use them for pointer arithmetic.
```c
int compare (const void* a, const void* b)
{
	if (*(int*)a == *(int*)b) {
	return 1;
	} else {
	return 0;
	}
}

int compareChar (const void* a, const void* b)
{
	if (*(char*)a == *(char*) b)
	{
		return (1);
	}else {
		return (0);
	}
}

int search (void * array, int array_size, int element_size, 
			void* element, 
			int compare(const void*, const void*))
{
	char * ptr = (char *)array;
	int i;
	for (i = 0; i < array_size; i++) {
		if (compare(ptr + i*element_size, element)) {
		return i;
		}
	}
	return (-1); // returns -1 if the element cannot be found
}
```
