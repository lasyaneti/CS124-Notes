# 09/03/21: Errors and Debugging

## Errors 
- **Checkstyle errors** are caused by incorrect code formatting
    - Ex: missing space after if keyword, incorrect indentation, unused import statements, etc.
- **Compiler errors** are caused because:
    1. Java doesn't understand what you are trying to do
    2. Java understands what you want to do but has noticed a potential problem 
- **Runtime errors** are errors that are not caught by the compiler but is brought up at runtime 

## Assert
- Use the assert keyword to debug 
- Output message can be added
```java
int i = -1;
// detects if i is negative and sends message accordingly
assert i > 1 : i + " is not positive";

// Ex of using assert in SWE: division function, assert that you are not diving by zero
int divide(int dividend, int divisor) {
    assert (divisor != 0);
    int quotient = dividend / divisor;
    return quotient; 
}
System.out.println(divide(4, 2)); // prints 2;
System.out.println(divide(2, 0)); // results in Assertion Error
```