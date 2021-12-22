# 10/22/21: Lists Review and Performance

## Remove Algorithm in Linked Lists
- Previous moves down until it reaches temp (which is also moving down), till it hits the item to be removed
- Change previous.next = temp.next so we skip item at temp
  - Need these Items: first item = START, last item = END
  - Key: previous.next = previous.next.next
  - Remember to change SIZE after add or remove 

```java
public class SimpleLinkedList {
  private Item start;
  private int size;
  private class Item {
    private Object value;
    private Item next;
    Item(Object inputValue, Item inputNext) {
      value = inputValue;
      next = inputNext;
    }
  }
  public void addToFront(Object obj) {
    start = new Item(obj, start);
    size++;
  }
  public String toString() {
    String output = "[ ";
    for (Item current = start; current != null; current = current.next) {
      output += current.value + ", ";
    }
    return output + "]";
  }
  public Object get(int input) {
    return getItem(input).value;
  }
  private Item getItem(int input) {
    if (input < 0 || input > size) {
      throw new IllegalArgumentException();
    }
    int index = 0; 
    for (Item current = start; current != null; current = current.next) {
      if (index == input) {
        return current;
      }
      index++;
    }
    assert false; 
    return null;
  }
  public Object remove(int index) {
    if (index == 0) {
      Item temp = start;
      start = start.next;
      size--;
      return temp.value;
    } else {
      Item prev = getItem(index - 1);
      Item temp = prev.next;
      prev.next = temp.next;
      size--;
      return temp.value;
    }
  }
}

SimpleLinkedList list1 = new SimpleLinkedList();
list1.addToFront("d");
list1.addToFront("c");
list1.addToFront("b");
list1.addToFront("a");
System.out.println(list1);
assert (list1.toString().equals("[ a b c d ]"));
list1.remove(1);
System.out.println(list1);
assert (list1.toString().equals("[ a c d ]"));
list1.remove(2);
System.out.println(list1);
assert (list1.toString().equals("[ a c ]"));
list1.remove(1);
System.out.println(list1);
```
## Big O Comparison
| ArrayList | Linked List |
| --------- | ----------- |
| Get: O(1) | Get: O(n) |
| Set: O(1) | Set: O(n) |
| Add/Remove anywhere: O(n) | Add to front: O(1) |
| | Add to end: O(1) |
| | Add anywhere else: O(n) |



