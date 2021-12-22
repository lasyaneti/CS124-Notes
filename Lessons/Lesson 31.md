# 10/03/21 References and Polymorphism
- Reference type (left side) determines what an object can do or what methods can be called (look at Polymorphism lesson)

```java
public class Person {
    void speak() { }
}
public class Student extends Person {
    void study() { }
}

Student student = new Student();
Person person = student;

// these are valid
student.speak();
student.study();
person.speak();

// results in ERROR
person.study();
```

- Dot notation tells Java to follow the reference variable to the instance of the object it refers to, i.e. back to where it was declared and if there are two references, it will follow either since they both lead to the same
- Java arrays of objects = an array of references