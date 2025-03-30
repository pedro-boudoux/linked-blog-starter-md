**Class:** [[CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #functions 


If you think I'm going to waste my precious time telling you what a function in C is in the big 25 you're greatly mistaken.

Functions are formatted in the following way:

```
returnType functionName(paramType param1, ...) {
	
	// code goes here

return varOfReturnType;
}
```

Functions are stored in the heap part of the memory which means that they can also be accessed by pointers!! Those are called [[Function Pointers]].

### Variable Scope

#### Local Variables
Variables declared inside a function.

#### Global Variables
Variables declared outside of any function (these are banned in [[CIS*2500]]).
