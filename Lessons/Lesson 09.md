# 09/02/21: Functions

- Functions help package sections of code
- Instead of rewritting these sections of code every time you want that functionality, you can just call the function to perform the operation
- Functions should be written for repetitive code
  - This makes the code reuseable and easier to read/work with, BUT **the actual speed of the code remains the same**.
- Functions must specify
  - Return type (stuff that is returned must match this)
  - Datatype if arguments accepted (stuff that is passed must match this)

```java
int addition(int a, int b) {
    return a + b;
}
System.out.println(addition(1, 2)); // prints 3
```