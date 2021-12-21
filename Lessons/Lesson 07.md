# 08/31/21: Loops

## While Loop
- Loops while condition is true 
- Note: int x that is created for the while loop below can be accessed from anywhere in the code
```java
int x = 0;
while (x < 5) {
    System.out.println(x);
    x++;
}
```

## For Loop
- Takes parameters (variable, limit, condition)
- Initializes variable, checks condition, (1) if condition is true, it executed code inside and increments and checks condition and repeat the loop (2) if condition is false, it exits the for loop
- Loops while specified condition is met
- Note: scope of int i that is created in the for loop below is only within the loop
```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```