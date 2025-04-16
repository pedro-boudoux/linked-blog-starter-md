**Class:** [[Intermediate Programming]]
**Date:** 01-04-2025
**Topics:** [[Function Pointers]], [[Pointers]], [[Memory]]

## What are Generic Pointers
A *generic pointer*, `void *` is a pointer that can represent any pointer type. All pointer types can be assigned to *void*, and pointers to *void* can be assigned a *pointer of any type*.
Example:
```c
#include<stdio.h> 
int main() 
{ 
    int a = 10;
    float b = 2.8;
     
    void *ptr;  // generic pointer 
    
    ptr = &a;          
    
   // cannot deference a void ptr, so casting to (int *) on line       12 is essential
    printf("ptr points to an int value = %d", * (int *) ptr);
    
    ptr = &b;
    
   // cannot deference a void ptr, so casting to (float *) on          line 17 is essential
    printf("ptr points to a float value = %f", * (float *) ptr);
    
    return 0; 
} 


```


