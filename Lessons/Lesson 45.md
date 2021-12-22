# 10/27/21: Recursion

- Method calls itself 
- Solving a problem using recursion relies on smaller instances of the starting item 
- Interative = loops vs. Recursive = methods that call themselves

## Palindrome
The goal is to make the solution so small that it is really obvious to solve. In this case, you basically just look at the first and last character, until you have a **string with 0 or 1 characters** -> this is our **base case**. Once we hit the base case, we just recurse up. 

```java
boolean isPalindrome(String input) {
    if (input == null) {
        throw new IllegalArguementException();
    }
    // Base case
    if (input.length() <= 1) {
        return true;
    }
    // Check along the way as you make the string shorter
    if (input.charAt(0) != inpur.charAt(input.length() - 1)) {
        return false
    }
    return isPalindrome(input.substring(1, input.length() - 2));
    return true;
}
```

## Recursion strategies
- Make the problem smaller (**key to recursion**)
- Solve the smaller problem first (base case)
- Combine results to reach the final answer