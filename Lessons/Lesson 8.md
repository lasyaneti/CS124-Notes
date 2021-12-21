# 09/01/21: Algorithms I

## Array Length
- Find array length using .length
```java
int[] arr = new int[5];
System.out.println(arr.length); // prints 5
```

## Break
- Break causes loop to exit immediately 
- Handy when you do not need to continue interating over an array once the job is done, reduces runtime

```java
int[] nums = [0, 1, 0, 0, 0];
for (int i = 0; i < nums.length; i++) {
    if (nums[i] == 1) {
        System.out.println("1 was found in nums");
        break;
    }
}
```