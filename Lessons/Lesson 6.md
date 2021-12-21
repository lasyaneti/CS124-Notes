# 08/30/21: Arrays 

- Sequential data stored with an index 
- Index starts at 0
- The size of an array cannot be changed once it is created 
- If empty array is created and not filled up, it is filled with default values of the specified datatype (0 for int, false for boolean, null for Objects, etc.)

```java
// Method 1: create array, fill it up
int[] arr1 = new int[5];
arr1[0] = 1;
arr1[1] = 2;
arr1[2] = 3;
arr1[3] = 4;
arr1[4] = 5;
// Method 2: assign to array with values 
int[] arr2 = {1, 2, 3, 4, 5};
```