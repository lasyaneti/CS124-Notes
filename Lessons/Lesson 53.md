# 11/11/21: Merge Sort

- Merge merges two arrays that are already sorted individually

![Visual](/Images/MergeSort.png)

## Merge Sort Steps
1. Split using mergeSort
2. Merge results using merge
    - Take two sorted arrays
    - Merge by comparing items at index in both arrays
    - Copy smaller number into new array (size = sum of both smaller arrays)
    - Update index

- O(n) because we iterate each element ONCE, n is the size of the big array that combines both smaller arrays
- Recursively sorting arrays is O(n*log-base 2-(n))
- When we are given 1 array, we need to split it into a smaller and smaller arrays that are then sorted and return up via recursion
  - **Base case**: an array with size 1 is naturally sorted

![Visual](/Images/MergeSort2.png)

## Merge Sort Code & Explanation
```java
public class Merger {
    public static int[] marger(int[] a, int[] b) {
        if (a == null || b == null) {
            throw new IllegalArgumentException();
        }
    }
    int[] c = new int[a.length + b.length];
    int aIdx = 0;
    int bIdx = 0;
    for (int i = 0; i < c.length; i++) {
        if (bIdx > b.length || (aIdx < a.length && a[aIdx] > b[bIdx])) {
            c[i] = a[aIdx];
            aIdx++;
        } else if (bIdx < b.length) {
            c[i] = b[bIdx];
            bIdx++;
        }
    }
    return c;
}
```

![Merge Sort Explained](/Images/MergeSort3.png)