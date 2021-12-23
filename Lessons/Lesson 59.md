# 11/18/21: Hashing

- The hash function (values/codes/digests/hashes) is used to map data of random sizes to fixed values
- hashCode() depends on reference, unless overriden

## Features of Hash Functions
- **Deterministic**: for an input hash value, function must always return the same hash value
- **Repeatable**: must have the ability to generate the same hash again
- **Fixed range**: within a certain range of values
- **Uniform**: prevents collisions
- Not mandatory, but it is highly reccomended and desirable for a good hash function to take input as evenly as the output range

```java
// Every Java object has a hashCode method
System.out.println("test".hashCode());
System.out.println("testing".hashCode());

// Hash codes of objects with the same values, but different references are different
Car first = new Car("Ford", 100);
Car second = new Car("Ford", 100);
System.out.println(first.hashCode() + " != " + second.hashCode());

// Good hash functions should override the Java object method and write code for the specific type of object

import java.util.Objects;

public class Car {
    String model;
    int odometer;
    @Override
    public int hashCode() {
        return Objects.hash(model, odometer);
    }
}
```

## Additional Info
- Files have download verification, which gives you a unique hashcode for unique files, so you can compare that you downloaded what you were shown online, and that your file was not intercepted by hackers, etc.
- GitHub commits are stored as hashcodes