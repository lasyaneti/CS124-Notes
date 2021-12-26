# 09/07/21: More About Functions

## Void
- Void is a return type that expects no return 
- Nothing to be returned

## Method Overloading 
- There can be multiple functions with the same function name BUT:
  - Arguments must be different 
  - Method signature (includes name and arguement) must be different, i.e. just changing the return type or arguement variable name will not work
- Useful to perform same function with different inputs 

```java
// These work!!
void printThis(int num) {
    System.out.println(num);
}

void printThis(String str) {
    System.out.println(str);
}

void printThis(int a, int b) {
    System.out.println(a + " and " + b);
}

// WRONG because method signature is still the same, the only change made was the arguement variable name
void printThis(int val) {
    System.out.println(val);
}

// WRONG because method signature is still the same, the only change made was the return type
int printThis(int num) {
    System.out.println(num);
    return num;
} 
```
## Variable Redeclaration
- Similar to methods, variables also cannot be redeclared with a new type within the same scope

```java
int i = 0;
boolean i = false; // error here
```

## Enhanced For Loop
- Alternative for loop that doesn't use index 
- Datatype of variable created for the enhanced for loop must match the variable of the data structure you are traversing 
```java
int[] nums = {1, 2, 3, 4, 5};
for (int num : nums) {
    System.out.println(num);
}
```