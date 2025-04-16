**Class:** [[Intermediate Programming]]
**Date:** 29-03-2025
**Topics:**  #recursion #algorithms 

## Recursion
Recursion is when a function invokes itself. The purpose of recursion is to break a large problem into several smaller problems.

Example
```C
int factorial(int n) {

if (n == 1 || n == 0) {
	return 1;
} else {
	return n*factorial(n-1);
}

}
```

As you can see by the code example, the `factorial()` function is a recursive function as it calls itself over and over again while trying to calculate the factorial of a number. 

### Requirements for Recursion
Every recursive process requires 2 things:
1. A *base case* that is processed without recursion, this requires an ending condition that knows when to apply the base case (in the example above the base case is `n = [0,1]`).
2. A method that reduces a particular case to one or more smaller cases. This requires a *recursive call*, in the example above it can be found in `line 6`.

## How does Recursion work?
Recursion uses a data structure called [[Stacks]], to explain how Recursion relates to Stacks, think of a to-do list where you can't finish the big task at the bottom until the smaller task above it is finished. Once the smaller task is done, you can go for the task below it. This relates to Recursion because you can't have `factorial(n)` until you have `factorial(n-1)` and so on...
