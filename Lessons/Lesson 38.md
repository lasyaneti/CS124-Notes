# 10/14/21: Anonymous Classes

- Declaration looks the same as creating a new object, except it opens up a method declaration, where you add code to determine behavior
- Anonymous class methods are usually only overrides

```java
public class Person {
    public String getType() {
        return "Person"
    }
}
Person person = new Person();

// RHS is the class to extend/interface to implement
Person student = new Person() {
    @Override
    public String getType() {
        return "Student";
    }
};

System.out.println(person.getType()); // prints "person"
System.out.println(student.getType()); // prints "student"
```

- You cannot create multiple instances of anonymous classes, the point of these is to override one thing from the parent class/interface

## Anonymous Class Rules
- Have no name
- Must extend parent class or implement interface
- INstances are create immediately, no further instances can be created
- Cannot provide constructors 

## Anonymous Classes and Variables
- Anon classes can "capture variables", i.e. access variables that are outside the written anon classes
- **BUT once anon classes capture a variable, the variable cannot be accessed or edited again**
- Loophole: you can still change the property (instance variable value) of the object, you just cannot change the actual object itself, i.e. if you had String str for Object Person, you can do person.str and reassign the value if it is public

```java
interface GetValue {
    int get();
}

// Show variable capture
int i = 10;

GetValue getValue = new GetValue() {
    @Override
    pbulic int get() {
        return i;
    }
};

i = 12; // ERROR: i cannot be captured again
System.out.println(getValue.get());
```