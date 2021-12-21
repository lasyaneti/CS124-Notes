# 09/16/21: Maps and Sets

## Map
- Maps are a way for you to store information
- Allows you to create *mappings* between items (Key -> Value)

```java
import java.util.Map;
import java.util.HashMap;

Map<String, Integer> map = new HashMap<>();

// add a mapping 
map.put("Chicago", 3);
map.put("New York", 5);

// change a mapping by using key
map.put("Chicago", 4);

// you can have different keys pointing to the same value
map.put("San Francisco", 4);

// retrieve mapping
map.get("Chicago");
map.get("Seattle"); // returns null if key DNE
map.getOrDefault("Seattle", 0); // handy method to set default value in the case of null

// iterating over a Map
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println(entry.getKey());
    System.out.println(entry.getValue());
}
```
## Set
- Sets are unorder collection of distinct elements
- Items do not have indexes
- Only unique items are stored in a set
- Best use if when order does not matter and items must be unique

```java
import java.util.Set;
import java.util.HashSet;
Set<Integer> set = new HashSet<>();

// add items
set.add(1);
set.add(1); // set still only contains one 1 because it only stores unique valuesSo peSooo
set.add(3);
System.out.println(set);

// check if item exists
set.contains(2);

// remove items by calling the value itself
set.remove(1); 

// iterate over set
for (Integer item : set) {
    System.out.println(item);
}
```