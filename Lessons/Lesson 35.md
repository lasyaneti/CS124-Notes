# 10/11/21 Using Interfaces

## Abstract as a keyword for classes
- Helps create a superclass that cannot be used to create instances of objects
- Can contain methods, which are inherited and accessed by children
- Any abstract methods in an abstract class must be overridden by extended subclasses because of reasons below

## Abstract as a keyword for methods
- Any subclass that extends a superclass with abstract method, MUST override and implement that method 
- Works like a blueprint: helps organize behavior that call subclasses should have 

## More on Abstract
- When you have a normal class with an abstract method, it becomes messy because now you can create instances of that normal class but you cannot access the methods (unless you override)
- Conceptually, an interface is when **separate components exchange information**, a shared boundary must be agreed upon in order to operate co-dependently 
- Further, the interface for any class is the methods that it contains - the points of connection AKA how you can interact with the class
- **Important Note**: 
    - Interitance for classes is limited because you can only extend one class
    - Inheritance for interfaces is flexible because you can implement multiple interfaces, BUT:
      - you must provide a method called simple
      - documenatation becomes super important to avoid running into errors, the compiler doesn't check for your errors.

```java
interface Simple {
    int simple(int first);
}

interface Second {
    void example();
}

public class Parent { }

public class Simpler extends Parent implements Simple, Second {
    // methods of implemented interfaces must be overriden 
    public int simple(int arguement) {
        return arguement + 1;
    }
    public void example() { }
}
```
## Interfaces vs. Abstract Classes
- Similar features except one main difference
- If you design using an abstract class, know that you can only extend one class
- Interfaces are handy when you want to implement multiple

## Comparable 
- A parametrized interface 
- for now create ourComparable, our own version of the Comparable interface 