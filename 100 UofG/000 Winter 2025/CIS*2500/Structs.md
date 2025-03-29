A struct is a custom data type which can contain other data types inside (even another struct).  Each *element* inside a struct is called a *member*, members can also be arrays or pointers of data types.

Structs can be defined in C in the following way:
```
struct Student {
char firstName[MAX_LENGTH];
char lastName[MAX_LENGTH];
int id;
float assignmentMarks[4];
}
```

### Typedef
Awesome keyword that allows a programmer (like you or me) to create aliases for words, variables, commands, etc.. If used properly, they can make your code far more readable.

Typedef is often used with structs but can also be used with other things.

Using typedef with structs:
```
typedef struct Student {
char firstName[MAX_LENGTH];
char lastName[MAX_LENGTH];
int id;
float assignmentMarks[4];
}StudentRecord;
```
... this means we can declare a variable like `StudentRecord x;` instead of typing `struct Student x;`.
