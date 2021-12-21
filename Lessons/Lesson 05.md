# 08/27/21: Compound Conditionals

- Evaluated from left to right 
- Parenthesis can be used to group expressions within a larger statement 
- Short-circuit evaluation is when evaluation stops as soon as the result is found (explained below)

| conditional | what it does |
| ----------- | ------------ |
| && | and (see note) |
| \|\| | or (see note) |

- **Note**
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