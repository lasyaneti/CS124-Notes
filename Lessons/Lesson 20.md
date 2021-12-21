# 09/20/21 Introduction to Objects 

- Class = blueprint for Object, it defines how a group of objects behave
  - Methods define what the object can do 
  - Instance variables defines properties of the object
  - Class name must be capitalized  
- An instance of an object is a copy of the class

| Class | Instance |
| ----- | -------- |
| City | Chicago |
| City | New York |
| Building | Siebel Center for Computer Science |
| Building | Grainger Engineering Library | 

## Class/Object demo
- Use dot notation to access public instance variables
- Call constructor to create an instance

```java
class Person {
    // Instance Variables
    String name;
    int age;
}

// Constructor
Person me = new Person();

// Dot notation
me.name = "Lasya";
me.age = 18;
System.out.println(me.name);
```