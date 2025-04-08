**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 29-03-2025
**Topics:**  #datastructures #algorithms #C #self-referential #structures, [[Structs]]

## Linked Lists
A *linked list* or *list* is a common structure with many applications, it is one of the easiest structures to build and use.

A *linked list* is more flexible than an *array*, it allows us to insert or delete nodes in itself as needed.

However, we lose the *"random access"* ability than an *array* gives us. Any element in an array can be accessed in the same amount of time. Accessing a *node* in a *linked list* on the other hand, requires us to traverse to that node so the speed depends on whether the *node* is *at the end or the beginning* of a *linked list*.

## What is a Linked List?
A *linked list* consists of a chain of structures (called *nodes*) with each node containing a pointer to the next node in the chain. [[Pointers]] are used to attach the elements into a chain, *elements* in the list are usually structures and each such structure is a called a *node*.

Here is an example of a node structure in C:
```c 
typedef struct node {

	int val;
	struct node* next;

}ListNode;
```

### Adding to the BEGINNING of a Linked List
Let `headLL` be the head of the linked list which we are adding to the beginning of.
```C
node *newNode = malloc(sizeof(node)); // creating a pointer to a new node and allocating memory for it

newNode->val = 20; // giving it a value

newNode->next = headLL; // points our new node to the head

headLL = newNode; // makes the new node the head

```

### Adding to the END of a Linked List
Let `headLL` be the head of the linked list which we are adding to the end of and `newNode` be the node we want to add.
```C
node *tempNode = headLL; 

while (tempNode->next != NULL) {
	tempNode = tempNode->next;
}

tempNode->next = &newNode; // links the last node to the new node
newNode->next = NULL; // makes new node point to NULL

```

## Doubly Linked Lists
A *doubly linked list* is similar to a regular *linked list* except instead of just a pointer to the next node we also have a pointer to the previous node.

Here is an example of a *doubly linked list* in C:
```C
typedef struct doublyNode {

	int val;
	struct node* previous;
	struct node* next;

}DoublyListNode;
```

The benefits of a doubly linked list is that you can always move in either direction in the list, and that there is no need to keep an extra pointer around keeping track of the last element visited.

But, more [[Pointers]] have to be deleted in order to delete an element in a list.

## Circular Lists
*Circular lists* are linked lists in which the last element in the list (tail), points to the first element in the list (head). They can be *singly* or *doubly* linked.

