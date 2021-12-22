# 10/15/21: Lambda Expressions 

- Java is object-oriented, but other languages have other types of programming paradigms
- **Functional programming** is a type of programming paradigm, where functions are treated like first class citizens, i.e. they can be passed as variables
- In Java, functional programming is achieved by using interfaces and **replaces anonymous classes**
- Note: functional interfaces only provide one method, lambda functions only work with these

```java
interface Modify {
    int modify(int value);
}

interface Filter {
    boolean accept(int a, int b);
}
```

- Anonymous classes have a lot of syntax clutter, which lambda expressions avoid 
- Inside the code block of a lambda expression you can add any logic (if else, for loop, etc.), whereas simplified lambda expressions cannot store this kind of logic

```java
interface Modify {
    int modify(int value);
}

// Anonymous class
Modify first = new Modify() {
    @Override
    public int modify(int value) {
        return value + 1;
    }
};

// Lambda expression with code block
Modify second = (value) -> {
    return value + 1;
};

// Lambda expression without code block
Modify third = (value) -> value + 1;
```

- Lambda expressions = funtional programming vs. anonymous classes = object oriented programming 
- Lambda expressions are great to store **simple one line logic functions in variables** (no loops/conditionals), this is functional programming in Java

| Modify | second | value | -> | { |
| ------ | ------ | ----- | -- | - |
| Indicates the interface being implemented | Name of function | Parameter without datatype | Opens lambda expression | Opens code block |