# 08/25/21 Operations on Variables

## Comments in Java
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
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division (truncates answer during int division) |
| % | Modulo (returns remainder from division) |
| = | Assignment (see Note A) |
| ! | Binary negation aka BANG (switches the boolean) |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |
| == | Equality (see Note A) |
| != | Not equal to aka BANG equals |
| && | and (see Note B) |
| || | or (see Note B) |

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
- **Note B**
    - And (&&) checks if all conditions are true. It first checks if LHS is true, and then if RHS is true. If any codition it checks in not true, it does not check the following conditions and simply returns false. 
    - Or (||) checks if either condition is true. It also checks LHS first, and then RHS. If any condition it checks is true, it does not check any of the following conditions and simply returns true. 
``` java
int i = 1;
int j = 2;
int n = 1;
int m = 2;
System.out.println(i == n && j == m); // prints true
System.out.println(i == j && j == m); // prints false
System.out.println(i == j || j == m); // prints true
System.out.println(i == j || n == m); // prints false
```