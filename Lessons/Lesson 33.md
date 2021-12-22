# 10/07/21: Throwing Exceptions 

- Java allows us to throw our own exceptions 

```java
throw new NullPointerException("Error Message");
```

- **Throwable** is the parent class for all errors you can throw
    - **Error**: should not try to catch -> serious problem, must be alerted to user
    - **Exception**: should try to catch -> because code can be run without this part actually working 

## Checked Exceptions 
- Generated using the **throw** keyword
- MUST be handled by either:
  - Catch
  - Declaring a potential exception using throw (see below)

```java
public void printThis(String str) throws Exception {
    if (str == null) {
        throw new IllegalArguementException();
    }
    System.out.println(str);
}
```

## Unchecked Exceptions AKA runtime exceptions
- Do not handle these with try/catch or throw anything

## Errors
- Absolutely do not handle these
- Serious errors should be brought to the user's attention
