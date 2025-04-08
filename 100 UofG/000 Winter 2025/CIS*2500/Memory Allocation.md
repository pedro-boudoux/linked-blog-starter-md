**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 29-03-2025
**Topics:**  

## Memory Allocation
As you can see in the graph below, in a program there are 4 places in the memory where data can be stored in.
![[Memory Allocation Graph.png]]
### The Stack
The *Stack* is where local variables are stored, variables that are statically declared inside `main()` and used in the program.
```
int main() {

int count = 0;

return 0;

}
```
In the code snippet above,  an integer `count` is declared in `main()`, thus allocating 4 bytes of memory from the stack to hold `count`.

### The Heap
The *Heap* is where dynamically allocated memory is stored

![[Memory Allocation Graph.png]]

