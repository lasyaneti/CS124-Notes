# 09/17/21: Compilation and Type Inference
## Compilation
- Java programs are run in two steps:
  - **Compilation**: source code is **compiled/translated**; some errors are caught in this stage, these errors are to help us prevent worse errors that could come up during execution. These errors are caught in the development environment so it will ideally be smooth during production.
  - **Execution**: bytecode produced by compiler is **executed**, code is run and it does what you instructed it to do, other types of errors are caught here. All tests are run during development, so ideally in the production environment we do not want any errors. Syntactically valid but logically wrong code is usually what is caught here, ex: int x = 100 / 0;  
- Most IDEs combine both steps and do it for you, but in the terminal you need to type out both commands separately ("javac Example.java" to compile and "java Example" to execute)
- Example.java is human-readable
- Example.class is machine-readable

## Type Inference
- When you declare and initialize a variable at the same time (see below), notice that you told Java the type twice: (1) by saying int (2) by setting it equal to 0

```java
int i = 0;
```

- Type interface allows you to store all types in an umbrella keyword called var 
- Note var is not a type
- Type interface allows you to be more experimental with programming
- If declaration and initialization are done seperately when using var, it will result in an error. Java var must know what the type is and this is only possible if you initialize it to a value at the same time as you declare it. 
```java
var i = 0;
var s = "String";

// error
var = i;
i = 0; 
```