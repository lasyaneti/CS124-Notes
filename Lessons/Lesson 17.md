# 09/15/21: Lists and Type Parameters 
- Lists store sequential data like Arrays, but they are more flexible 
- Arrays cannot be grown or shrunk (fixed size), but Lists can do this 

```java
import java.util.List;
import java.util.ArrayList;

// METHOD 1:
ArrayList<String> arr1 = new ArrayList<String>();

// METHOD 2: no need to respecify ArrayList datatype on the right 
ArrayList<String> arr2 = new ArrayList<>();

// METHOD 3: abstraction is powerful = List is a higher level object of ArrayList 
// Variable is of interface type list, variable references ArrayList class
List<String> arr3 = new ArrayList<String>();

// METHOD 4: most common syntax
List<String> arr4 = new ArrayList<>();
```

## Features of Lists/ArrayLists
- Arrays and Lists have their own benefits and drawbacks in terms of ease of usage
```java
// ARRAY vs. ARRAYLIST INITIALIZATION: array is better
String[] arr2 = {"First Item", "Second Item"};
List<String> list2 = new ArrayList<>(Arrays.asList("First Item", "Second Item"));

// ARRAY vs. ARRAYLIST PRINTING: list is better
System.out.println(arr2); // prints reference
System.out.println(list2); // neatly prints the values in list 

// ARRAY vs. ARRAYLIST ACCESSING ELEMENTS: both are more or less the same
arr[0] = "hello";
System.out.println(arr[0]);

list.set(0, "hello");
System.out.println(list.get(0));

// ARRAY vs. ARRAYLIST SIZE: list is better
String[] arr = new String[5];
System.out.println(arr.length);

List<String> list = new ArrayList<>();
System.out.println(list.size()); // currently 0 
list.add("First Item");
list.add("Second Item");
list.add(1, "Insert Between First and Second Item");
list.remove(2);
System.out.println(list.size()); // now 2
```

## Boxing
- ArrayLists cannot store primitive types, you must box them 
  - byte -> Byte
  - short -> Short
  - int -> Integer
  - long -> Long
  - double -> Double
  - char -> Character
  - boolean -> Boolean
- Boxed types can be set to null because they are objects 
- Autoboxing is when Java automatically boxes (converts primitive type to object) and unboxes (converts object to primitive type) for you, see below
```java
List<Integer> list = new ArrayList<>();
for (int i = 1; i <= 5; i++) {
    // notice how i is of primitive type int but Java autoboxes (int -> Integer) and adds to the list
    list.add(i);
}
// the retrieved Integer value is unboxed and added with 5 (literal int value)
System.out.println(list.get(0) + 5);
```

## More on Lists
- Adding objects of other types to Lists of a defined type will result in imcompatoble types error
- Always provide type parameter for Lists in Java because an undefined type parameter will allow objects of all types and it gets messy
- [Additional concept](https://youtu.be/aMLRDGKbSgQ) explained by prof. Colleen Lewis