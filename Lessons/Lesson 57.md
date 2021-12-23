# 11/17/21: Binary Search

- Sorting algorithm patterns give rise to search algorithms
- In an unsorted array, we would have to interate over it and check every element to find the value

## Binary Search, Conceptually
[Harvard CS50: The Famous PhoneBook Analogy](https://youtu.be/o2LqhHoAXxI)

## Binary Search, Visually
[CS124 Challen](https://youtu.be/0IAwYcS9uCs)

![Binary Search Visually](/Images/BinarySearch.png)

## Binary Search on Array Code
```java
public static boolean search(SearchList list, Comparable value) {
    if (list == null || value == null || list.size() == 0) {
        throw new IllegalArgumentException();
    }
    // Indexes created
    int start = 0;
    int end = list.size() - 2;
    // While loop to search list
    while (start <= end) {
        int midpoint = (start + end) / 2;
        Comparable valAtMidpoint = list.get(midpoint);
        if (valAtMidpoint.compareTo(value) == 0) {
            return true; // Value found
        } else if (valAtMidpoint.compareTo(value) > 0) {
            // Array value is greater than value passed
            // Check lower array, i.e. update end
            // Minus one because we want to get rid of valAtMidpoint
            end = midpoint - 1;
        } else {
            // Array value is lesser than value passed
            // Check upper array, i.e. update start
            // Plus one because we want to get rid of valAtMidpoint
            start = midpoint + 1;
        }
    }
    return false;
}
```

## Runtime
**Best case**: O(log N)
**Worse case**: O(log N)