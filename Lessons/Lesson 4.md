# 08/26/21: Conditional Expressions and Statements

- Conditionals return a boolean answer

| conditional | what it does |
| ----------- | ------------ |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |
| == | Equality (see Note A) |
| != | Not equal to aka BANG equals |

## If and If Else
- If statements are evaluated if the condition is true
- Else statements always follow if statements. These are executed only when the if statement is false. These are optional, i.e. not every if statement must be followed by an else. 
- Else if statements are evaluated if the above if statement is false and the statement itself is true. 
``` java
int i = 0;
if (i == 1) {
    System.out.println("i is 1");
} else if (i == -1) {
    System.out.println("i is -1");
} else {
    System.out.println("i is neither 1, nor -1"); // only this is printed 
}
```
## Code Blocks and Variable Scope
- Blocks of code begin with { and end with }
- Variables created inside a code block, are only valid inside that block
``` java
int i = 0; 
if (i == 1) {
    int j = 1;
} 
System.out.println(j); // will result in error because j can only be accessed inside the if block it was created in
```