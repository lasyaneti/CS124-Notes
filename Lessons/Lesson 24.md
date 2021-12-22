# 09/24/21: Static

## This
- The **this** keyword can be used in object classes to reference the current instance of the class
- It helps distinguish between parameter and instance variables when they have the same variable name

## Unconventional Use Case for this
```java
public class Course {
    private int num;
    Course(String num) {
        this.num = num;
        // LHS is instance variable
        // RHS is variable of passed arguement
    }
}
```

## Typical Use Case for this

![Visual Representation](https://media.geeksforgeeks.org/wp-content/uploads/Constructor-Chaining-In-Java1.png)

```java
public class Course {
    private String number;
    private int enrollment;

    Course(String setNumber, int setEnrollment) {
        number = setNumber;
        enrollment = setEnrollment;
    }
    Course(String setNumber) {
        this(setNumber, 0);
        // a call using 'this' must be the FIRST line of the constructor
        // here, we are calling one constructor from another and passing the required values
    }
}
```

## Static
- The **static** keyword allows us to attach properties to the CLASS itself, rather than a specific INSTANCE of that class
- Static methods are called on the class, not the object (see below)

```java
Person p1 = new Person();
p1.instanceMethod();
Person.staticMethod();
```
- Instance methods can easily access instance variables within the class
- Static methods cannot do this, because it's on the class. So when there is no instance, there is no instance variable initialized, so to avoid confusion the static methods cannot access instance variables. **Thus, static methods must be passed all the information they need to perform their operation**

## Static and Final
- Static goes well with the **final** keyword, which creates a variable that cannot be changed after its initialization, it makes the code more readable and less error-prone.
- When you create your own classes, you can make variables as final
- Variables marked as final are all caps by convention
- The Math class is a common example of this:
```java
public static final double PI = 3.14; 
```
- In the reverse, instance methods CAN access static variables. This logic is useful to create non final static fields. 
- In general, do not mark instance variables as static, unless it is final as well. 