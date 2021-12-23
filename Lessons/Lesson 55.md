# 11/12/21: Quicksort

- Partitioning
  - Pick a pivot
  - Split (1) all items < pivot (2) all items >= pivot
  - Swap values if they are smaller than pivot, keep updating turtle pivot

## Quicksort Problem Code & Explaination
1. Loop through and compare pivot value to partition at last index
2. Change pivot as you go 
3. If value at last index is out of place, change the partition 

**Question: Pick last index as partition, return pivot index**
```java
public class Partitioner {
    public static int partition(int[] values) {
        if (values == null || values.length == 0) {
            throw new IllegalArgumentException();
        }
        int pivotValue = values[values.length - 1];
        int pivotIndex = 0;

        for (int i = 0; i < values.length; i++) {
            if (values[i] < pivotValue) {
                int temp = values[i];
                values[i] = values[pivotIndex];
                values[pivotIndex] = temp;
                pivotIndex++;
            }
        }

        values[values.length - 1] = values[pivotIndex];
        values[pivotIndex] = pivotValue;

        return pivotIndex;
    }
}
```

![Quicksort Explained](/Images/QuickSort.png)