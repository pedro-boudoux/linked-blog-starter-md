**Class:** [[Intermediate Programming]]
**Date:** 07-04-2025
**Topics:**

## Quiz 1

### Section 1

```
nutritious: dairy.o vegan.o nuts.o nuts.h
	gcc -Wall -std=c99 nuts.o dairy.o vegan.o -o nutritious
nuts.o: nuts.c nuts.h
	gcc -Wall -std=c99 -c nuts.c
dairy.o: dairy.c nuts.h
	gcc -Wall -std=c99 -c dairy.c
vegan.o: vegan.c nuts.h
	gcc -Wall -std=c99 -c vegan.c
clean:
	rm *.o
	rm nutritious
```
#### Question 4
Assume that the current folder has 5 files and they are:
```
makefile, nuts.c, vegan.c, dairy.c, nuts.h 
```
Which of the following command or commands are executed when the make utility is run the first time?

a. `gcc -Wall -std=c99 -c dairy.c`
b. All of the options
c. `gcc -Wall -std=c99 -c nuts.c`
d. None of the given choices
e. `gcc -Wall -std=c99 -c vegan.c`

``` title="Solution"
b. All of the given choices
```

#### Question 5
What command or commands will execute when the make command is run after updating file `nuts.h`?

a. None of the given choices
b. Commands on lines 2,4, 6 and 8 
c. Commands on lines 4, 6 and 8
d. Command on line 2
e. Commands on lines 2, 4, 6, 8, 10 and 11

``` title="Solution"
b. Commands on lines 2,4, 6 and 8 
```

### Section 2
Read the code given below to answer questions in this section. Your task is to *spot and fix at least 5 compile-time errors and warnings* in the given code so that it matches the given sample input / output scenario when run. 
Assume that lines 1 - 9 are valid statements.
Given Input / Output Scenario:

Given Code:
```c
#include <stdio.h>
#define MAX 10

void processArray(int toProcess[MAX], int *);

int main()
{
	int toProcess[MAX];
	int i, returnedValue = 0;

	printf("Enter %d values:", MAX);
	for (i = 0; i < MAX; i++) {
		scanf("%d", &toProcess [i]);
	}

	processArray(&toProcess, &returnedValue);

	printf("\nReturned value in main = %d\n", &returnedValue);
	return 0;
}

void processArray(int toProcess, int * sumOdd) {
	
	int i;

	for (i = 0; i <= MAX; i++) {
		
		if (i%2 == 1) {
			printf("%d ", toProcess[i]);
			sumOdd = sumOdd + toProcess[i];
		}
	}
}
```

#### Question 6
Which of the following lines in the given code have compile-time error(s), warning(s) or runtime error? 
Select all that apply.

- [x] Line 16
- [x] Line 26
- [x] Line 28
- [x] Line 22
- [ ] Line 29
- [ ] Line 12
- [x] Line 13
- [ ] Line 30
- [ ] Line 18

``` title="Solution"
All of them
```

## Quiz 2
### Section 1
Use the code given below to answer all questions in this section.
```c


typedef struct temp {

	char email[2][100];
	char supervisorName [25];
	int yearsOfService;
} employeeData;

int main () {

	int result1;
	employeeData manyEmployees [5];

	for (int i = 0; i < 5; i++) {
		result1 = fun1 (manyEmployees[i].supervisorName);
	
	}

	for (int i = 0; i < 5; i++) {
		if (i % 2 == 0) {
			fun2 (&manyEmployees[i].yearsOfService);
		}
	}

	fun3 (manyEmployees);

	return 0;
}
```

#### Question 1
What is the prototype of `fun1`?

a. `int fun1 (char);`
b. `int fun1 (employeeData);`
c. None of the given choices
d. `int fun1 (char [25]);`
e. `void fun1 (char);`

``` title="Solution"
d. int fun1 (char [25]);
```
#### Question 2
What is the prototype of fun2?

a. `void fun2 (int [5]);`
b. None of the given choices
c. `int fun2 (&int);`
d. `void fun2 (int);`
e. `void fun2 (int *);`

``` title="Solution:"
e. void fun2 (int *);
```
#### Question 3
What is the prototype of fun3?

a. `void fun3 (manyEmployees);`
b. None of the given choices
c. `void fun3 (employeeData [5]);`
d. `void fun3 (tmep [5]);`
e. `void fun3 (employeeData);`

``` title="Solution"
c. void fun3 (employeeData [5]);
```
#### Question 4
Assume that a variable is defined as follows:
```
employeeData * empQ = &manyEmployees[0];
```
Which of the following correctly reads `supervisorName` via variable `empQ`.

a. `scanf("%s", &empQ->supervisorName);`
b. `scanf ("%s", *empQ.supervisorName);`
c. `scanf ("%s", empQ->supervisorName);`
d. None of the given choices
e. `scanf ("%s", empQ.supervisorName);`

``` title="Solution"
c. scanf("%s", empQ->supervisorName);
```

### Section 2
#### Question 5
What is the purpose of  the `git clone` command when starting with a GitLab repository?

a. To copy an existing GitLab repository to your local machine
b. None of the given choices
c. To create a new repository on your local machine
d. To delete the repository from GitLab
e. To update your local repository with changes from GitLab

``` title="Solution"
a. To copy an existing GitLab repository to your local machine
```

#### Question 6
Assume that your current folder on your local machine has the following 4 files as shown below (`lab1Main.c`, `lab1A.c`, `lab1B.c` and `makefile`). What is the correct sequence of commands (on the terminal) to add these files to your currently empty GitLab repository, so that you can now see these files on `gitlab.socs.uoguelph.ca` when you login to it using your username and password.
```bash
pedro@archlinux$ ls
lab1Main.c lab1A.c lab1B.c makefile

```


a.
```bash
git push lab1A.c
git push lab1B.c
git push makefile
git push lab1Main.c
git commit -m "This is for Quiz2"
```

b. 
```bash
git add lab1A.c
git add lab1B.c
git add makefile
git add lab1Main.c
git commit -m "This is for Quiz2"
git push
```

c. 
```bash
git commit -m lab1A.c
git commit -m lab1B.c
git commit -m lab1Main.c
git commit -m makefile
```

d.
```bash
git add
git push
git commit
```

```bash title="Solution"
 b.
 
 git add lab1A.c
 git add lab1B.c
 git add makefile
 git add lab1Main.c
 git commit -m "This is for Quiz2"
 git push
 
```
## Quiz 3

#### Question 1
Why does the following code throw an error:
```c
char * ptr = "abc";
free (ptr);
```

a. All the given choices are correct
b. None of the given choices
c. You cannot use free() on pointers that are initialized.
d. You cannot use free() on pointers, unless you allocate memory using malloc(), calloc(), or       realloc().
e. You cannot use free() on pointers - it can be used only with static allocation.

``` title="Solution"
d. You cannot use free() on pointers, unless you allocate memory using malloc(), calloc() or realloc().
```

#### Question 2
What gets printed by the code given below:
```c
char *ptr;
ptr = malloc (sizeof(char) *25);
strcpy (ptr, "Study in the study week!");

ptr = realloc (ptr, sizeof(char) * 2000);
printf("%s \n", ptr);
```

a. None of the given choices

b. "Study in the study week!", because `realloc()` copies the entire string from original location to the newly allocated location.

c. This code throws an error because you cannot use the same pointer (e.g `ptr`) in `realloc()` twice.

d. This code throws an error because you cannot reallocate memory greater than the original.

e. Nothing gets printed on the screeen because `realloc()` overwrites the reallocated memory with `NULL` characters.

``` title="Solution"
b. "Study in the study week!", because realloc() copies the entire string from original location to the newly allocated  location.
```

#### Question 3
Fill in the boxes given below. Assume that in the given code,
- `i` and `ptr` have been declared.
- a character occupies 1 byte in the memory.
- an integer occupies 4 bytes in the memory
- pointer occupies 8 bytes in the memory.

```c
	for (int i = 0; i < 3; i++) {
	
		ptr[i] = malloc (sizeof(char)*(strlen("Quiz3")+1));
		strcpy (ptr[i], "Quiz3");
	}
```

a. What is the size of `(ptr[0])` in bytes? 

b. What is the size of `(&ptr[0])` in bytes?

c. What is the size of `(*ptr [0])`?

``` title="Solution"
a. 8
b. 8
c. 1
```

#### Question 4
Which line or lines in the following code will throw an error:
```c
char * ptr [3];

ptr [0] = malloc (sizeof(char)*2);

ptr [1] = calloc (2, sizeof(char));

ptr [2] = realloc (ptr [2], sizeof(char) * 2);
```

a. None of the given lines
b. Line 18
c. All of the given lines
d. Line 14
e. Line 16

``` title="Solution"
b. Line 18
```

#### Question 5
Given four variables `var1`, `ptr1`, `ptr2`, and `ptr3`, and a memory model as shown below, fill in the given boxes.
```c
int var1 = 5;
int * ptr1 = &var1;
int ** ptr2 = &ptr1;
int * ptr3 = ptr1;
```

| Memory Address | Variable Name |
| -------------- | ------------- |
| 959c0          | var1          |
| 959c4          | ptr1          |
| 959cc          | ptr2          |
| 959dd          | ptr3          |

a. What is the value of `ptr1`?

b. What is the value of `ptr2`?

c. What is the value of `ptr3`?

d. What is the memory address of `ptr1`?

e. What is the memory address of `ptr2`?

f. What is the memory address of `ptr3`?

``` title="Solution A"
a. 959c0
```
``` title="Solution B"
b. 959c4
```
``` title="Solution C"
c. 959c0
```
``` title="Solution D"
d. 959c4
```
``` title="Solution E"
e. 959cc
```
``` title="Solution F"
f. 959dd
```

## Quiz 4
#### Question 1
True or False?
Given a non-empty linked list such as the one given below, the time taken to access the first node of the linked list (e.g., Butterfly) is the same as the time taken to access its last node (e.g., Ant
lion).
![[Pasted image 20250407141608.png]]

- True
- False

``` title=Solution
False
```

#### Question 2
Answer this question using the definitions, linked list and code segment given below. Assume that variable head has been appropriately defined and set as head of the linked list.
```c
// Code Definition:
struct data {
	int num;
	struct data * next;
};
```

**Linked List:**
![[Pasted image 20250407141829.png]]
```c
struct data *ptr2;
```

**Code Segment:**
```c
ptr2 = malloc (sizeof(struct data));

ptr2->num = head->next-next->num - 10;

ptr2->next = head;
```

a. After executing the given code, what is the value of `ptr2->num`?

b. What is the value of `ptr2->next->num`?

c. After executing the given code, What is printed by the following loop:
```c
while (head->next != NULL) 
{
	printf("%d:", head->num);
	head = head->next);
}
```

``` title="Solution A"
a. 24
```
``` title="Solution B"
b. -5
```
``` title="Solution C"
c. -5:20:34:
```

#### Question 3
Given a linked list as shown below:
![[Pasted image 20250407142319.png]]
Which of the following correctly removes the current head, after making the next node in sequence as the new head of the list.

You may assume that *temp* and *head* are both declared appropriately. Variable *head* currently points to the first node in the list as shown in the figure. Variable *temp* currently points to `NULL`.

a.
```c
temp = head;
head = head->next;
free (head);
```

b.
```c
temp = head;
head = head->next;
free(temp);
```

c. None of the given choices

d.
```c
head = head->next;
free(head);
```

e.
```c
free(head);
head = head->next;
```

```c title=Solution
b.

temp = head;
head = head->next;
free(temp);
```

#### Question 4
Given the following struct definition:
```c
struct data {
	int num;
	struct data * next;
};
```
Assume that
- variable *head* has been appropriately defined and set as the head of the linked list.
- The linked list given to function `fun1` is not empty.

What does function `fun1` given below do, when called as `fun1(head)`?
```c
void fun1 (struct data * myHead)
{
	if (myHead != NULL) {
		fun1 (myHead->next);
		printf("%d ", myHead->num);
	}
}
```

a. None of the given choices

b. Prints all nodes of the linked list in reverse order.

c. Prints alternate nodes of the linked list.

d. Prints alternate nodes of the linked list in reverse order.

e. Prints all nodes of the linked list.

``` title=Solution
b. Prints all nodes of the linked list in reverse order.
```

## Quiz 5
#### Question 1
The difference between *pop* and *peek* operations of a Stack ADT is:

a. None of the given choices

b. *pop* returns the top element and removes it too, but *peek* just removes it

c. *pop* returns the top element without removing it, but *peek* returns it and removes it too

d. *pop* removes the top element, whereas *peek* returns the top element

e. *pop* returns the top element and removes it too, but *peek* returns it without removing it

``` title=Solution
e. pop returns the top element and removes it too, but peek returns it without removing it
```

#### Question 2
Suppose that you are required to push 5 char values `5` `i` `q` `u` and `z` (in that order) to a stack s. But the values can be popped at any time. Which of the following is a valid sequence of pop and push operations such that the values are popped from the stack in the following order:
```
q u i z 5 
```
Prototypes of *push* and *pop* operations are given below for convenience:
```c
void push (char element, Stack * s);
char pop (Stack * s);
```
Assume `ch` is defined as a char variable.

a.
```c
push('5', &s);
push('i', &s);
ch = pop (&s);
push ('q', &s);
push ('u', &s);
ch = pop (&s);
push ('z', &s);
ch = pop(&s);
ch = pop(&s);
ch = pop(&s);
```

b. None of the given choices

c.
```c
push ('5', &s);
push ('i', &s);
push ('q', &s);
push ('u', &s);
push ('z', &s);
ch = pop (&s);
ch = pop (&s);
ch = pop (&s);
ch = pop (&s);
ch = pop (&s);
```

d.
```c
push ('q', &s);
push ('u', &s);
push ('i', &s);
push ('z', &s);
push ('5', &s);
ch = pop (&s);
ch = pop (&s);
ch = pop (&s);
ch = pop (&s);
ch = pop (&s);
```

e.
```c
push('5', &s);
push('i', &s);
push('q', &s);
ch = pop (&s);
push ('u', &s);
ch = pop (&s);
ch = pop (&s);
push ('z', &s);
ch = pop (&s);
ch = pop (&s);
```

```c title=Solution
e.
push('5', &s);
push('i', &s);
push('q', &s);
ch = pop (&s);
push ('u', &s);
ch = pop (&s);
ch = pop (&s);
push ('z', &s);
ch = pop (&s);
ch = pop (&s);
```

#### Question 3
Assume that current state of a queue `q` is as follows:
```
(front) 'e' -> 'n' -> 'l' -> 'i' -> 'g' -> 'h' -> 't' (back)
```
What is the state of the queue after the following 4 enqueue and dequeue operations on queue `q` given above? Assume element is declared as a char.
```c
element = dequeue (&q);
element = dequeue(&q);
enqueue('e', &q);
enqueue('n', &q);
```
Prototypes of enqueue and dequeue functions are given below for convenience:
```c
void enqueue(char item, Queue * q);
char dequeue(Queue *q);
```

a. (front) 'l' -> 'i' -> 'g' -> 'h' -> 't' -> 'e' -> 'n' (rear)

b. (front) 'e' -> 'n' -> 'l' -> 'i' -> 'g' -> 'h' -> 't' -> 'e' -> 'n' (rear)

c. None of the given choices

d. (front) 'e' -> 'n' -> 'l' -> 'i' -> 'g' -> 'h' -> 't' (rear)

e. (front) 'e' -> 'n' -> 'e' -> 'n' -> 'l' -> 'i' -> 'g' (rear)

``` title=Solution
a. (front) 'l' -> 'i' -> 'g' -> 'h' -> 't' -> 'e' -> 'n' (rear)
```

## Quiz 6
#### Question 1
You may use the code given in file named `quickSort.c` posted on your course webpage in Contents->Week12 to answer this question.

Given an integer array

```
6, 7, 88, 90, -5, 67, 13, 52
```

What is the state of this array after the first call of Quicksort assuming that the last element in the array is chosen as the pivot.

a. `6, 7, -5, 13, 5m 67, 90, 88`

b. `-5, 7, 6, 13, 52, 67, 90, 88`

c. None of the given choices

d. `6, 7, -5, 13, 88, 67, 90, 52`

e. `-5, 6, 7, 13, 52, 67, 88, 90`

``` title=Solution
a. 6, 7, -5, 13, 52, 67, 90, 88
```

#### Question 2
An array of 10 elements is given below:
```
10, 20, 30, 40, 50, 60, 70, 80, 90, 100
```

a. How many comparisons it would take to find `80`, using the Binary Search Algorithm?

b. How many comparisons would it take it find `80`, using the Linear Search Algorithm?

``` title="Solution A"
a. 2
```
``` title="Solution B"
b. 8
```

#### Question 3
What is the time complexity of the following code in terms of Big O?
```c
for (i = 0; i < 10; i++) {
	if (arr[i] == 1001) {
		return i;
	}
}
```

a. $O(n)$

b. $O(n^2)$

c. $O(\log n)$

d. None of the given choices.

e. $O(1)$

``` title=Solution
e. O(1)
```

#### Question 4
Which of the following array represents the partially sorted array after the first *THREE* complete passes of insertion sort? Assume that the array to be sorted is an integer array.

You may use the insertion sort code (`insertionSort.c`) posted on your course webpage in Contents->Week12 to answer this question.
```
10,9,8,7,6,5,4,3,2,1
```

a. `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`

b. `10, 9, 8, 1, 2, 3, 4, 5, 6, 7,`

c. `8, 9, 10, 7, 6, 5, 4, 3, 2, 1`

d. `1, 2, 3, 10, 9, 8, 7, 6, 5, 4`

e. None of the given choices

``` title=Solution
c. 8, 9, 10, 7, 6, 5, 4, 3, 2, 1
```

#### Question 5
Use the code given in file named `mergeSort.c` posted on your course webpage in Contents->Week12 to answer this question.

How many comparisons does the merge function of mergesort make if the input integer array is:
```
6, 7, 88, 90,    -5, 13, 16, 52
```

a. 6
b. 5
c. 7
d. None of the given choices
e. 8

``` title=Solution
a. 6
```

#### Question 6
Which of the following array represents the partially sorted array after the first *three* complete passes of selection sort? Assume that the array to be sorted is an integer array.

You may use the selection sort code (`selectionSort.c`) posted on your course webpage in Contents->Week11 to answer this question.
```
10, 9, 8, 7, 6, 5, 4, 3, 2, 1
```

a. `1, 2, 3, 7, 6, 5, 4, 8, 9, 10`

b. `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`

c. `10, 9, 8, 7, 6, 1, 2, 3, 4, 5`

d. `1, 2, 3, 4, 5, 10, 9, 8, 7, 6`

e. None of the given choices

``` title="Solution"
a. 1, 2, 3, 7, 6, 5, 4, 8, 9, 10
```

### Section 2
Answer questions in this section using the code given below:
```c
int a = 0, b = 0;
int i, j, k;

for (i = 0; i < n; i++) {
	for (j = n; j > i; j--) {
		a++;
	}
	for (k = 0; k < i; k++) {
		b++;
	}
}
```

#### Question 7
Which of the following graphs correctly show the behaviour of the given code in terms of Big O. Note that axis represents input n, and y axis represents 'number of operations' (hint: for big O analysis, you can treat the y axis to be synonymous with "number of iterations").

a. None of the given choices

b. ![[Pasted image 20250407150530.png]]

c.![[Pasted image 20250407150537.png]]

d.
![[Pasted image 20250407150543.png]]

e.
![[Pasted image 20250407150553.png]]

``` title=Solution
e.
```

#### Question 8
What is the time complexity of the given code in terms of Big O?

a. $O(n)$

b. $O(2^n)$

c. None of the given choices

d. $O(n^2)$

e. $O(n^3)$

