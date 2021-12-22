# 09/20/21: Objects, Continued 

- Instance methods control object behavior 
- Accessed through dot notation and parenthesis (parameters)

```java
class Room {
    double width;
    double height;
    String name;

    String print() {
        return "The " + name + " is " + width + " by " + height;
    }
    String furniture(String items) {
        return "The " + name + " has the following furniture: " + items;
    }
}

// create instance and instantialize variables
Room kitchen = new Room();
kitchen.name = "Kitchen";
kitchen.width = 10;
kitchen.height = 10;

// call instance methods
System.out.println(kitchen.print());
// prints "The kitchen is 10 by 10"
System.out.println(kitchen.furniture("Couch"));
// prints "The kitchen has the following furniture: Couch"
```

## Get and Set
- Getter and setter methods are used to access and modify private instance variables
- Private variables must be declared with the private keyword

## Local vs. Instance
- Local variables are defined in a block of code outside the object class
- Instance variables are defined inside the object class