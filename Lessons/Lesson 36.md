# 10/12/21: Implementing Interfaces

- **Think of interfaces like contracts**: by implementing, you are agreeing to provide certain methods
- When working with interfaces, you must have a shared understanding of what behaviors to provide 
- If a class has a natural ordering, you should use Comparable and include a compareTo() method
- It is unlikely that a class both uses and implements the same interface

## Two Sides to Abstraction Barrier
| Using | Implementing |
| ----- | ------------ |
| You don't need to implement an interface to use a feature that the interface provides. | You KNOW when you are implementing it because you have to use the implements keyword. The question is how do you know when to use the implements keyword? Just because you use Comparable as an object in your class, you do not need to implement it. Unless you want to access and create methods of Comparable. |