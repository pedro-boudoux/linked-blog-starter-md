**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #memory #dynamicmemoryallocation #C #pointers #object 

*Dynamic Memory Allocation* is the process of allocating memory space during program execution, allowing for flexible memory usage based on runtime needs.

All values that are stored using *dynamic memory allocation* will be stored in *heap* memory (see [[Memory Allocation]]).

## Functions
### malloc()
```
void * malloc(size_t size);
```
The `malloc()` function returns a generic pointer of the specified size in the function.
*Usage example:*
```
int * arr;
arr = malloc(sizeof(int) * 4);
```
this makes `arr` an array that can hold 4 integer elements.

### realloc()
```
void * realloc(void *ptr, size_t newSize);
```
The `realloc()` function returns a generic pointer replacing `ptr` with a new pointer of the newly specified size.
*Usage example:*
```
int * arr = malloc(sizeof(int) * 4);

arr = realloc(arr, sizeof(int) * 8);
```
this changes the size of `arr` from being able to hold 4 integer elements to 8.

### calloc()
```
void * calloc(size_t num, size_t size);
```
The `calloc()` function allocates memory for an array of `num` elements of `size` size and initializes the values in the array to 0.
*Usage example:*
```
int * arr = calloc(4, sizeof(int));
// thus the array would look like {0,0,0,0}
```
Allocates space for a 4-element array of integers and initializes all values to 0.

### free()
```
void free(void * ptr);
```
Deallocates/releases the memory that was previously dynamically allocated and stored in the *heap*. 

Every `malloc()` requires a free, and arrays of [[Pointers]] require multiple frees.

## Dynamically Allocated Structures
Dynamically allocated structures are created using `malloc()` and a pointer. Elements in a dynamically allocated structure are accessed using the `->` operator *not* the `.` operator.
*Example:*
```
int main() {

struct data {

int count;
float total;

}

struct data *aPtr;
aPtr = malloc(sizeof(struct data));

aPtr->count = 10;
aPtr-> total = 3.5;

printf("%d %f \n", aPtr->count, aPtr->total);

}
```

