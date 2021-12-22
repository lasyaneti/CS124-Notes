# 09/23/21: Encapsulation

- Java enables encapsulation using setters and getters to modify the visibility of object properties 
- **Encapsulation** means to bundle data with methods to hide the information and prevent direct access to users, making it more secure 
- Note: convention is to make setters void return type 

## Who can access/modify based on marked Encapsualtion type
| Public | Private | Protected | Package Private |
| ------ | ------- | --------- | --------------- |
| Anyone | Only code that is a part of that class | N/A | If the variable is not marked as any of the others, it defaults to this |

```java
class Dog {
    private String name;

    Dog(String setName) {
        name = setName;
    }

    // Get
    String getName() {
        return name;
    }
    // Set
    void setName(String setName) {
        name = setName;
    }
}

Dog dog = new Dog("Spot");
dog.setName("Flash");
System.out.println("The dog's name is: " + dog.getName());
```