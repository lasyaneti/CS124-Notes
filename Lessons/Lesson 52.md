# 11/10/21: Sorting Algorithms

- Analyze sorting algorithms by examining time & space taken
- Larger dataset = takes longer to sort, we need to optimize how quickly that rate is increasing (exponential, linear, log, etc. change based on increase in dataset)
- Algorithms we will learn:
  - Bubble Sort
  - Insertion sort
  - Merge Sort
  - Quicksort 

## Bubble Sort
- Not that efficient, but the most simple and intuitive 
- Slow because it moves one position at a time
- You could break out of the loop and end the sorting algorithm using a conditional
- Cases:
  - **Best case** is already sorted array: {1, 2, 3}
  - **Worse case** is when everything is sorted but smallest value is at the end: {1, 2, 3, -1}

``` java
static void bubbleSort(int[] values) {
    if (values == null) {
        throw new IllegalArgumentException();
    }
    for (int i = 0; i < values.length; i++) {
        boolean swapped = false;
        int temp;
        for (int j = 0; j < values.length - 1; j++) {
            // Make the swap if value is out of place
            if (values[j + 1] < values[j]) {
                temp = values[j + 1];
                values[j + 1] = values[j];
                values[j] = temp;
                swapped = true;
            }
        }
        if (!swapped) {
            break;
        }
    }
}

int[] values = {1, 2, 4, 5, 6, -3, 7, 8, -1};
bubbleSort(values);
```

## Insertion Sort

![Visual](/Images/InsertionSort.png)

1. Divides array is a sorted and unsorted part
2. Keeps the sorted part sorted and accepts one element from the unsorted part to place in the sorted part

```java
public static void insertionSort(int[] arr) {
    if (arr == null) {
        throw new IllegalArgumentException();
    }
    for (int i = 1; i < arr.length; i++) {
        int j = i;
        while (j != 0 && arr[j -1] > arr[j]) {
            int temp = arr[j];
            arr[j] = arr[j - 1];
            arr[j - 1] = temp;
            j--;
        }
    }
}    
int[] values = {1, 2, 4, 5, 6, -3, 7, 8, -1};
insertionSort(values);
```