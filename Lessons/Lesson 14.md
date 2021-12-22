# 09/10/21: null

- null can be tought of as a literal value that is used for objects
- null means the **lack of a reference** for that object
- Primitive types cannot be set to null; however, arrays of primitive types are still objects so these can be set to null 

## Input Validation
- It is a good coding practice to account for null by establishing a set of actions if the passed object is null 
- See example below:
```java
void printName(String name) {
    if (name == null) {
        System.out.println("Name is invalid");
    } else {
        System.out.println("Name is " + name);
    }
}
```