# 09/13/21: Multidimensional Arrays 

```java
int[][] bedroom = new int[20][10];
// row * column -> think of 20 as width and 10 as height 
```

- A declared, but uninitialized array is filled with null
- Length of second array doesn't have to be stated because each array inside it can be of a different length

```java
int[][] nonrectangular = new int[2][];
nonrectangular[0] = new int [3];
nonrectangular[1] = new int [5];

/* can fill this nonrectangular array up with something like:
{ {1, 2, 3}, {1, 2, 3, 4, 5} } */
```