# 10/21/21: Linked Lists

- Instead of indexes, each item has (1) value (2) next that points to the next item in the linked list 

![Visual](/Images/LinkedLists.png)

- Size is measured when the next pointer reaches **null** at the end

## Linked List methods 
- get: O(n) because it needs to iterate the whole array
- set: same as above
- add: adds a new item by changeing hte pointer from the previous item and adding another connection
- remove: it just changes the pointer by skipping the item at index, doesn't need to iterate the rest of the list after the index

## Linked List vs. ArrayList
- The main different is that in a Linked List, each item is aware of its position by using pointers to keep track of what is behind/forward, rather than jsut relying on index 
- ArrayList is fast for get/set
- Linked List is fast for add/remove

## Inner Classes
- Inside a SimpleLinkedList class, you can create inner classes and intantialize/use them within the class

```java
public class SimpleLinkedList {
    private Item start;
    private int size;
    // Inner class
    private class Item {
        private Object value;
        private Item next;
        Item() { }
        Item(Object inputValue, Item inputNext) {
            value = inputValue;
            next = inputNext; 
        }
    }
}
```

![Visual](/Images/InnerClass.png)

- Inner classes can have properties and methods as well, which can only be accessed within the class they are in

## Iterating a Linked List
```java
for (Item current = start; current != null; current = current.next) {
    // start at first item
    // continue until the end, i.e. till current hits null
    // increment pushes to the next item
}
```