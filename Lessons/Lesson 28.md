# 09/29/21: Equality and Object Copying

- When we create our own classes, we get to define how equality is tested by overriding the .equals() method
- The object class contains an equality method, which compares if two objects are the exact same object (not the content)

```java
public class Pet {
    Pet(String setName) {
        assert (setName != null) : "Pet must have a name";
        name = setName;
    }
    @Override
    public boolean equals(Object o) {
        if (o == null) {
            return false;
        }
        if (o instanceof Pet) { // check before downcast
            Pet other = (Pet) o;
            return other.name.equals(name); // our definition of equality
        } else {
            return false;
        }
    }
}

Pet first = new Pet("Xyz");
Pet second = new Pet("Chuchu");
System.out.println(second.equals(first)); // prints false
```

## Copy Constructor
- You are not advised to duplicate objects by copying content in Java, the developers didn't provide a clone method for this reason!
- However, you can create your own copy constructor, see below:

```java
// assume class is declared here 
private String name;
public Student(String other) {
    name = other.name;
}
```