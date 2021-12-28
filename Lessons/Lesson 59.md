# 11/29/21: Practical Sorting (MP3)

Collections.sort sort an in place sort, i.e. it doesn't return a new list but rather modifies the passed one.

## One Parameter
```java
String[] a = {"Bbb", "B", "Aa", "Aaa", "Cc", "Ccc", "A", "Bb", "C"};
Collections.sort(a);
// a is now: [A, Aa, Aaa, B, Bb, Bbb, C, Cc, Ccc]
```

## Two Parameters: use lambda as the 2nd argument
```java
Collections.sort(a, (s1, s2) -> s1.compareTo(s2));
// a is now: [A, Aa, Aaa, B, Bb, Bbb, C, Cc, Ccc]
```