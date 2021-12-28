# 12/03/21: Streams

Stream is an efficient way of thinking about linear collections (array, list, etc.), usually implemented using the same for loop and return structure 
- Java has various built-in functions in the Stream<T> interface
  - It takes in a stream, outputs a stream after performing the specified action
  - Often uses lambda functions

## Stream Ex 1
Prints 1, 2, 5 (each is held in variable e) on a new line through labmda.

```java
import java.util.stream.Stream;

Stream.of(1, 2, 5).forEach(e -> System.out.println(e));
```

## Stream Ex 2
Prints "hey", "heyhey", "heyheyheyheyhey" (passed String, copied e times) on a new line.

```java
import java.util.stream.Stream;

Stream.of(1, 2, 5)
    .map(e -> "hey".repeat(e))
    .forEach(e -> System.out.println(e));
```

## Terminators
A common use of map is to extract information. Terminators are functions in the stream that end the stream. An example using **sum()**, in which the sum of all the dogs' ages is found.

```java
import java.util.stream.Stream;

int totalAge = Stream.of(new Dog("Chuchu", 16), new Dog("Lulu", 4), new Dog("Shadow", 16)).mapToInt(dog -> dog.getAge()).sum();
```

Another useful terminator is **count()**. The example below counts the number of items in the stream that are odd numbers. 

```java
// Using Stream
import java.util.stream.Stream;

long count = Stream.of(1, 2, 5)
    .filter(e -> e % 2 != 0)
    .count();

System.out.println("# of Odd Items: " + count);

// Normally the above code is written as
int[] values = {1, 2, 5};
int loopCount = 0;
for (int value : values) {
  if (value % 2 != 0) {
    loopCount++;
  }
}
System.out.println(loopCount);
```

## Stream Ex 3
reduce() takes in arguments and flows down the stream, performing the function along each step. In this example, we convert the ints in the stream into Strings, and concatenate them into "125"

```java
String str = Stream.of(1, 2, 5).map(e -> "" + e).reduce("", (a, b) -> a + b);
System.out.println(str);
```

## Stream Ex 4
Both code blocks below perform the same action, which is printing the name of dogs whose age is less than 1. The first is regular, the second uses **method references, which looks like ::**

```java
stream
    .filter(dog -> dog.getAge() <= 1)
    .map(dog -> dog.getName())
    .forEach(name -> {
      System.out.println(name);
    });
```

```java
stream
    .filter(dog -> dog.getAge() <= 1)
    .map(Dog::getName)
    .forEach(System.out::println);
```