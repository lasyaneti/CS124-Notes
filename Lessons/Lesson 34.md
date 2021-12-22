# 10/08/21: Working with Exceptions

- The **finally** block is always executed regardless of exception status and even if there is a return statement above it
- Assert is not used often because it is not enabled by default in playgrounds, it is also used while developing (not in actual products)
- Convert a checked exception into an unchecked exception like so:

```java
try {
    throw new Exception("Had a problem");
} catch (Exception e) {
    System.out.println("Had a problem: " + e);
    throw new IllegalStateException(e);
}
```