# 12/02/21: Generics

- Transforming runtime errors to compiler errors is a good programming practice because it prevents errors during development
- Generics helps generify all classes, meaning you can pass any object

## E
- Type <E> is a placeholder for any element in Java

```java
public class Example<E> {
    // This works because E replaces a type for variable value
    private E value;
    public Example() {
        // Cannot reassign a type
        E = String;
        // This is also wrong, cannot create like this
        value = new E();
    }
}
```

- The compiler automatically replaces the type parameter E with types specified in the code
- The Compiler puts a cast for you automatically **only during compilation**, and then **discards thus information**, i.e. at runtime this information is not avaliable (type erasure)
- There is only one instance of the list itself, making it efficient
- If you do not specify type, it uses Object
- Interfaces can also accept type parameters

## Common Java Naming Conventions for Generic Type Parameters
| E | <K, V> | N |
| - | ------ | - |
| Element in list | Key, value in map | Number |
