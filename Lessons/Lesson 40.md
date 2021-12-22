# 10/20/21: Algorithms and Lists

- Analyzing algorithms includes thinking about factors like time, storage, complexity, etc. 
- Big O answers the question: **how does the algorithm scale when we try larger and larger inputs?**
  - N is the input size 
  - O(1) is **constant time** (more input doesn't take more steps)
    - Ex: Array look up takes the same amount of time to loop up the value at an index in an array regardless of array size
  - O(N) is linear time (# of steps scales with input size)
    - Ex: In an array for loop, as the array size increases, iteration time increases
- Note: Big O is good because it helps you see the big picture of how algorithms work, but at the same time it is missing a bunch of details for certain algorithms 
- **ArrayList methods**:
  - get = O(1)
  - set = O(1)
  - add = O(N)
  - remove = O(N)
