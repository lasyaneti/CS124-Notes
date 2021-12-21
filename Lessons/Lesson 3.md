# 08/25/21: Operations on Variables

## Comments in Java
| code | what it does |
| ---- | ------------ |
| // | Single line comment |
| /* text */ | Multi line comment |

For example:
``` java
// This is a single line comment

/* This 
is a
multi-line
comment */ 
```

## Shortcut 
- i++ works the same as i += 1 which works the same as i = i + 1
- Note that unlike the others, i++ performs the operation after running code on line (see postfix demo below)

``` java
int i = 5; 
System.out.println(i); // prints 5
i++;
System.out.println(i); // prints 6
System.out.println(i++); // prints 6
System.out.println(i); // prints 7
```

## Operators 
| operator | what it does |
| -------- | ------------ |
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division (truncates answer during int division) |
| % | Modulo (returns remainder from division) |
| = | Assignment (see Note A) |
| ! | Binary negation aka BANG (switches the boolean) |

- **Note A**
    - Single equals (=) is used for assignment, i.e. it assigns value to variable
    - Double equals (==) is used to check equality. In primitive types, it compares the value of the variable. In objects, it compares the reference or address of the object.
``` java
int x = 1;
int y = 1;
System.out.println(x == y); // prints true

String a = "Hello";
String b = "Hello";
System.out.println(a == b); // prints false
```