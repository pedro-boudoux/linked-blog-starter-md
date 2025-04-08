**Class:** [[remote/100 UofG/000 Winter 2025/CIS*2500/CIS*2500]]
**Date:** 01-04-2025
**Topics:** [[Algorithms]]

## Sorting Algorithms
All *sorting algorithms* shown in this page will sort the elements in *ascending order* (smallest to largest).

### Bubble Sort
Compares adjacent elements, swapping them if necessary, eventually "bubbling" up the largest element to the end of the array. This is repeated until the array in completely sorted.
Time Complexity:
- *Worst Case:* $O(n^2)$
- *Average Time Complexity:* $O(n^2)$
- *Best Case Time Complexity:* $O(n)$ (the array is already sorted)
```c
void bubbleSort (int array[SIZE])
{
	int temp;

	for (int i = 0; i < SIZE - 1; i++) {
		for (int j = 0; j < SIZE - i - 1; j++) {
			if (array[j] > array[j+1])
			{
				temp = array[j];
				array[j] = array[j+1];
				array[j+1] = temp;
			}
		}
	}
}
```

### Selection Sort
Starting from the first element, looks for the smallest element in the array, and replaces it with the element in the first position. Then repeats this for the element at second position, now looks for the smallest element in the remaining array (array starting at second position). This is repeated, until the array is completely sorted.
Time Complexity:
- *Worst Case:* $O(n^2)$
- *Average Time Complexity:* $O(n^2)$
- *Best Case Time Complexity:* $O(n^2)$ 
```c
void selectionSort (int array [SIZE])
{
	int minVal, minPos;
	int temp;

	for (int i = 0; i < SIZE; i++) {
		minVal = array[i];
		minPos = i;
		for (int j = i + 1; j < SIZE; j++) {
			if (array[j] < minVal) {
			minPos = j;
			minVal = array[j];
			}
		}
		temp = array[i];
		array[i] = array[minPos];
		array[minPos] = temp;
	}
}
```

### Insertion Sort
*Insertion Sort* works by partitioning the array into a sorted and an unsorted part. Elements from the unsorted part are compared with elements in the sorted part and placed at the correct position in the sorted part.
Time Complexity:
- *Worst Case:* $O(n^2)$ 
- *Average Time Complexity:* $O(n^2)$
- *Best Case Time Complexity:* $O(n^2)$ 
```c
void insertionSort (int array[])
{
	int current;
	int i, j;
	
	for (int i = 0; i < SIZE; i++) {
		current = array[i];
		j = i - 1;

		while (j >= 0 && array[j] > current) {
			array[j+1] = array[j];
			j = j - 1;
		}
		array[j+1] = current;
	}
}
```

### Quicksort
Assume that the array to be sorted is indexed from $1$ to $n$.
1. Choose an array element $e$ (the partitioning element), then rearrange the array so that elements $1, ... , i-1$ are less than or equal to $e$, element $i$ contains $e$, and elements $i+1,...,n$ are greater than or equal to $e$.
2. Sort elements $1, ..., i-1$, by using Quicksort recursively.
3. Sort elements, $i+1, ..., n$, by using Quicksort recursively.
Time Complexity:
- *Worst Case:* $O(n \cdot \log{n})$
- *Average Time Complexity:* $O(n \cdot \log{n})$
- *Best Case Time Complexity:* $O(n^2)$ 
```c
void swap (int *a, int * b) 
{
	int temp = *a;
	*a = *b;
	*b = temp;
}

int partition (int *arr, int low, int high)
{
	int pivot, pIndex, i;
	pivot = arr[high];

	pIndex = low;

	for (i = low; i < high; i++) {
		if (arr[i] <= pivot) {
			swap (&arr[i], &arr[pIndex]);
			pIndex++;
		}
	}
	swap (&arr[pIndex], &arr[high]);
	return pIndex;
}

void quickSort (int *arr, int low, int *high)
{
	if (low < high) {
		int pivotIndex = partition (arr, low, high);
		
		quickSort(arr, low, pivotIndex-1);
		quickSort(arr, pivotIndex+1, high);
	}
}
```

### Mergesort
*MergeSort* is a *divide-and-conquer* sorting algorithm. It splits the array into smaller parts, sorts them, and then merges them back together in sorted order.
	1. Splits the array into two halves
	2. Recursively sort each half
	3. Combines the two sorted halves into one sorted array
Time Complexity:
- *Worst Case:* $O(n \cdot \log{n})$
- *Average Time Complexity:* $O(n \cdot \log{n})$
- *Best Case Time Complexity:* $O(n \cdot \log{n})$ 
```c
void merge(int arr[], int left, int mid, int right) {
    int n1 = mid - left + 1;
    int n2 = right - mid;
    int L[n1], R[n2];

	// splits the array in half
    for (int i = 0; i < n1; i++) L[i] = arr[left + i];
    for (int j = 0; j < n2; j++) R[j] = arr[mid + 1 + j];

	
    int i = 0, j = 0, k = left;
    while (i < n1 && j < n2) {
        if (L[i] <= R[j]) arr[k++] = L[i++];
        else arr[k++] = R[j++];
    }
    while (i < n1) arr[k++] = L[i++];
    while (j < n2) arr[k++] = R[j++];
}

void mergeSort(int arr[], int left, int right) {
    if (left < right) {
        int mid = left + (right - left) / 2;
        mergeSort(arr, left, mid);
        mergeSort(arr, mid + 1, right);
        merge(arr, left, mid, right);
    }
}
```
