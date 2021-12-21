# 09/08/21: Strings 

- String is an object, can be used as a datatype (not primitive)
- Refer to [documentation](https://docs.oracle.com/en/java/javase/14/docs/api/java.base/java/lang/String.html) for methods 
- Strings are enclosed in "double quotes"
- Strings are compatible with non latin text languages (Japanese, etc.) and Unicode (Emojis, etc.) 

## Escape Sequences 
- Use backslask to insert quotes and slashes so Java can read 

| code | what it does |
| ---- | ------------ |
| \\' | Single quotation mark |
| \\" | Double quotation mark |
| \\\\ | Backslash |
| \\n | New Line |
| \\t | Tab with 8 Spaces |

```java
String example = "this is a single quote: \' --> it works.";
System.out.println(example);
```

## String Concatenation
```java
String first = "Lasya";
String last = "Neti";
System.out.println(first + " " + last); // prints "Lasya Neti"
System.out.println(last + ", " + first); // prints "Neti, Lasya"
```

## Java String methods 
| code | what it does |
| ---- | ------------ |
| s.length() | length |
| s.trim() | gets rid of spaces in the front and back |
| s.charAt(1) | returns char at index 1 |
| s.substring(1, 3) | returns substring of given indexes [1, 3) |
| s.equals(str) | checks string value equality |
| s.split(" ") | string is split into array based on arguement |
| Integer.parseInt(s) | string is converted into an int |

- Demo
```java
String a = "Lasya";
System.out.println(a.length()); // prints 5
System.out.println(a.charAt(1)); // prints 'a'
System.out.println(a.substring(1, 3)); // prints "as"
String b = "  Hello";
System.out.println(s.trim()); // prints "Hello"
String c = "Lasya";
System.out.println(a == c); // false (checks for address)
System.out.println(a.equals(c)); // true (checks for value)
String d = "Computer Science";
System.out.println(d.split(" ")); // returns array [Computer, Science]
String e = "12";
System.out.println(Integer.parseInt(e)); // returns int 12
```