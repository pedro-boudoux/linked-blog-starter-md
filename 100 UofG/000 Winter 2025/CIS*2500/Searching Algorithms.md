**Class:** [[Intermediate Programming]]
**Date:** 01-04-2025
**Topics:** [[Algorithms]]

## Searching
### Linear Search
*Linear search* starts at the first element in an array and compare each element to the value you are looking for. *Linear search* works with *unsorted arrays*.
```c
int linearSearch(int arr[], int key, int n)
{
	for (int i = 0; i < n; i++)
	{
		if (key == arr[i]) return i;
	}
	return -1;
}
```
The Big-O time complexity of *linear search* is $O(n)$, at the worst possible case (if the element you're looking for is the last one or not in the array). On average, you will find a solution in $n/2$ comparisons where $n$ is the total number of elements.

### Binary Search
*Binary search* requires *ordered data* but is much faster than linear searching. It starts with the middle value and keeps dividing the array in half until the value is found.
```c title:"Binary Search - Iterative"
int binarySearch (int * array, int size, int findMe)
{
	int left = 0;
	int right = size - 1;
	int middle;

	while (left <= right)
	{
		middle = (left + right) / 2;

		if (findMe == *(array+middle)) {
			return middle;
		} else if (findMe > *(array+middle)) {
			left = middle + 1;
		} else {
			right = middle - 1;
		}
	}

	return (-1); // not found

}
```
Recursive Binary Search:
```c title"Binary Search - Recursive"
int binarySearch (int findMe, int arr[10], int left, int right)
{
	int middle = (left + right) / 2;  
	int found;  
	
	if (left > right) {  
		return -1; // not found  
	}  
	else { // base case if found  
		if (findMe == arr [middle]) {  
		found = 1;  
		}  
	else if (findMe < arr [middle]) {  
		found = binarySearch (findMe, arr, left, middle - 1);  
	}  else {  
		found = binarySearch (findMe, arr, middle + 1, right);  
	}  
	
	return found;
	
}
```

