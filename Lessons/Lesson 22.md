# 09/22/21: Constructors

- Good code always initializes object fields immediately after creating the an instance of the object 
- Constructors make this task effective 

## Constructor Rules
- No return type because constructors automatically return a new instance of the Class
- Constructors are called only using the **new** keyword
- Constructors cannot be called using dot notation
- Java always includes a default constructor that takes no arguments and doesn't initialize anything. Once you include a custom constructor, however, this default constructor is deleted - you must add it back if needed. 
- Method overloading works with constructors, you just need different parameters. 
- Constructors must be called the same thing as the object class

```java
class Person {
    String name;
    int age;

    Person(String setName, int setAge) {
        // Input validation is a good coding practice
        if (setAge < 0) {
            age = 0;
        }
        name = setName;
        age = setName;
    }
}

Person me = new Person("Lasya", 18);
```