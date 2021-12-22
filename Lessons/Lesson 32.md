# 10/06/21 Catching Exceptions

- Code after an exception is thrown is not executed

## Try Catch
- A method for error handling
- Handle exceptions and keey the code running without breaking 

```java
String s = "test";
try {
    int i = Integer.parseInt(s);
    System.out.println("Code successful: " + i);
} catch (Exception e) {
    System.out.println(s + " is not a number");
}
```

- There are a variety of exceptions that need to be handled differently
  - **NullPointerException** e
  - **NumberFormatException** e
  - **ArrayIndexOutOfBoundsException** e
  - **Exception** e: useful as the last catch block, takes care of all remaining exceptions
- As soon as an exception is thrown in the try block, Java looks for a catch block to resume running the code