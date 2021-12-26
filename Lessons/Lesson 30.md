# 10/03/21: References

- Objects are created only when the **new** keyword is used
- Fact: Object variables in Java store a reference to an object, rather than the object value/content

| Reference | Object |
| --------- | ------ |
| Net ID | Student |
| Phone Number | Phone |
| Address | Physical Home |

- Changes made to one object is reflected in all references that point to that object because copying a reference does not copy the object, but just creates another pointer to that same reference 

```java
class Person {
    public int age;
}

Person me = new Person();
Person you = me;

/*
me --->
       ---> both refer Person instance with age = 0
you -->
*/
```

- The 8 primitive types do not have references like objects
- **null explained**: null is actually an empty reference, i.e. the object does not have a reference
- **Equality explained**: == tests for reference equality (address of objects), .equals() tests for the equality of value/content 