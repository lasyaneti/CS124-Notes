# 10/27/21: Serialization and Searching 

- Jackson is a library used to serialize/deserialize JSON Strings to Java Objects 
- Jackson needs an **empty constructor** and **get methods with conventional method names** in Java object class to operate
- When deserialized, Jackson returns a **NEW object**, i.e. the references do not match up with the original object 

```java
import com.fasterxml.jackson.databind.ObjectMapper;

public class Person {
    private String name;
    private double age;
    // Mandatory empty constructor
    public Person() { }
    // Normal constructor
    public Person(String setName, double setAge) {
        name = setName;
        age = setAge;
    }
    // Get 
    public String getName() {
        return name;
    }
    public double getAge() {
        return age;
    }
    public String toString() {
        return name + " is " + age;
    }
}

Person person = new Person("Geoff", 41.2)
System.out.println(person);
// Jackson triggered here
ObjectMapper mapper = new ObjectMapper();
// Jackson methods for serializing
String json = mapper.writeValueAsString(person);
System.out.println(json);

// Jackson methods for deserializing
Person anotherPerson = mapper.readValue(json, Person.class);
System.out.println(anotherPerson);
```