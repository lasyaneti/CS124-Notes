# 09/09/21: Algorithms and Strings

## Casting
- Note: int * double = double 
- Casting happens before calculation 
- Cannot cast boolean to int, String to int (need to use method), int to String
- Implicit Casting (no need to cast)
  - byte -> short -> int -> long -> float -> double
- Explicit Casting (need to cast)
  - double -> float -> long -> int -> short -> byte 

```java
double a = 3; // works and stores the value of 3.0

int b = 3.14; // ERROR - need to cast 
int c = (int) 3.14; // truncates 3.14 and stores the value of 3 
```

## Important Note on Strings
- Strings are immutable, i.e. any method calls on a String do not change the actual String value, but simply return a new String 

## Multiline Strings
```java
String multiline1 = "one\n" + "two";

/* tedius, but it looks like
one
two */ 

String multiline2 = """
Line one 
Line two
Line three""";

/* far more efficient, and it looks like
Line one
Line two 
Line three */
```