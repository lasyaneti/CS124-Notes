# 09/27/21: Inheritance
- Inheritance allows us to establish relationships between classes: subclasses can *inherit* properties (state and behavior) by extending parent classes
- The **extends** keyword establishes this relation between classes
- All classes that do not have a specified parent class extend the Java Object class

## Hierarchy Rules
- Logic must be used in how you build inheritance. Ex: every student is a person, but not every person is a student. A student can inherit all the features of a person, but a person cannot have all the features of a student. Thus, it's logical to make a student subclass that extends a person class
- Circular extension is illegal: A extends B, B entends A
- Each parent class can have multiple different subclasses: B extends A, C extends A, D extends A
- Each subclass can have further classes of its own: B extends A, C extends B, D extends C

## Super
- Call super() to effectively use parent class' constructors 
- This call must be the first line in a method, you can only call it once
- We know that when you create a constructor, the class loses its default constructor with no arguments. So, when a parent class has a constructor, the subclass MUST call super() and pass appropriate arguments because it inherited the parent class' variables which need to be declared. 
- Private variables cannot be accesses by subclasses, getter methods must be used to gain access. 
- The **protected** keyword allows you to share variables with all subclasses that extend the parent class, while keeping it hidden from the rest of the code. This is only relavant in big projects that work with various Objects. 

```java
public class Person {
    private String name;
    public Person(String setName) {
        name = setName();
    }
}

public class Student extends Person {
    private int id;
    public Student(String setName, int setId) {
        super(setName);
        id = setId;
    }
}

Student student = new Student("Lasya", 123456789);
```

## Object Class and Overriding
- Every single Java class extends the Object class, thus inheriting its methods which can be overriden
- Ex: toString() can be overriden to make it more specific to the current class
- Overriden methods can be annotated (works like a label/flag) that tells Java something about the method. This helps with typos by raising an error.
- When an override method exists, Java will look for the method first in the current class and if it DNE then it goes up the inheritance looking for that method.
```java
public class Pet {
    private String name;
    public Pet(String setName) {
        name = setName;
    }
    @Override 
    public String toString() {
        return "My pet is named " + name;
    }
}

Pet chuchu = new Pet("Chuchu");
System.out.println(chuchu.toString());
```